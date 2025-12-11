---
solution: Journey Optimizer
product: journey optimizer
title: Doorlopen van contextafhankelijke gegevens
description: Leer hoe u met de syntaxis Handlebars arrays kunt doorlopen van verschillende contextbronnen
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
hide: true
hidefromtoc: true
keywords: expressie, editor, handlebars, iteratie, arrays, context, personalisatie
source-git-commit: ebe367a91dc1bb20ceeb03b13a6008433fadf023
workflow-type: tm+mt
source-wordcount: '2557'
ht-degree: 0%

---

# Doorlopen van contextafhankelijke gegevens {#personalization-contexts}

Leer hoe u de iteratiesyntaxis van Handlebars gebruikt om dynamische lijsten van gegevens uit diverse bronnen in uw berichten, met inbegrip van gebeurtenissen, de reacties van de douaneactie, en andere contextafhankelijke gegevens te tonen.

## Overzicht {#overview}

Journey Optimizer verleent toegang tot contextafhankelijke gegevens van veelvoudige bronnen tijdens [ berichtverpersoonlijking ](personalize.md). U kunt over series van deze bronnen herhalen gebruikend de syntaxis van Handlebars in inheemse kanalen ([ e-mail ](../email/get-started-email-design.md), [ duw ](../push/create-push.md), [ SMS ](../sms/create-sms.md)) om dynamische inhoud zoals productlijsten, aanbevelingen, of andere herhalende elementen te tonen.

**Beschikbare contextbronnen:**

* **[Gebeurtenissen](#event-data)**: Gegevens van reisgebeurtenissen (bedrijfsgebeurtenissen, eenheidsgebeurtenissen)
* **[Reacties van de Actie van de Douane](#custom-action-responses)**: Gegevens die van externe API vraag via douaneacties zijn teruggekeerd
* **[de raadpleging van de Dataset](#dataset-lookup)**: Verrijkte gegevens die van de datasets van Adobe Experience Platform worden teruggewonnen
* **[Technische eigenschappen](#technical-properties)**: De meta-gegevens van de reis zoals reis identiteitskaart en supplementaire herkenningstekens
* **[context van de Reis](#other-contexts)**: Andere op reis betrekking hebbende gegevens toegankelijk tijdens uitvoering

Deze gids toont u hoe te over series van elk van deze bronnen in uw berichten herhalen, en hoe te met series te werken wanneer het vormen van reisactiviteiten. Begin met [ de iteratiesyntaxis van Handels ](#syntax) om de grondbeginselen van de berichtverpersoonlijking te begrijpen, of aan [ het Werk met series in de uitdrukkingen van de Reis ](#arrays-in-journeys) te leren hoe te om seriegegevens tot douaneacties en datasetraadplegingen over te gaan.

## Titeratiesyntaxis van werkbalken {#syntax}

Handlebars verstrekt `{{#each}}` [ helper ](functions/helpers.md) om over series te herhalen.

+++ Basissyntaxis

```handlebars
{{#each arrayPath as |item|}}
  <!-- Access item properties here -->
  {{item.property}}
{{/each}}
```

**Zeer belangrijke punten:**

* Vervang `arrayPath` door het pad naar uw arraygegevens
* Vervang `item` door de gewenste variabelenaam (bijvoorbeeld `product` , `response` , `element` )
* Eigenschappen van elk item benaderen met `{{item.propertyName}}`
* U kunt meerdere `{{#each}}` -blokken nesten voor arrays van meerdere niveaus

+++

## Gegevens herhalen over gebeurtenissen {#event-data}

De gegevens van de gebeurtenis zijn beschikbaar wanneer uw reis door een [ gebeurtenis ](../event/about-events.md) wordt teweeggebracht. Dit is handig voor het weergeven van gegevens die zijn vastgelegd op het moment dat de reis werd gestart, zoals inhoud van het winkelwagentje, orderitems of formulierverzendingen.

>[!TIP]
>
>U kunt gebeurtenisgegevens combineren met andere bronnen. Zie [ veelvoudige contextbronnen ](#combine-sources) voor voorbeelden combineren.

### Contextpad voor gebeurtenissen

```handlebars
context.journey.events.<event_ID>.<fieldPath>
```

* `<event_ID>`: De unieke id van uw gebeurtenis, zoals geconfigureerd tijdens de rit
* `<fieldPath>`: Het pad naar het veld of de array in het gebeurtenisschema

### Voorbeeld: Items starten van een gebeurtenis

Als uw [ gebeurtenisschema ](../event/experience-event-schema.md) a `productListItems` serie (standaard [ formaat XDM ](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target="_blank"}) omvat, kunt u wortelinhoud als dit tonen:

+++ Voorbeeldcode weergeven

```handlebars
{{#each context.journey.events.event_ID.productListItems as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}
```

+++

### Voorbeeld: geneste arrays in gebeurtenissen

Gebruik geneste `{{#each}}` -blokken voor geneste structuren. Leer meer over het nesten in [ Beste praktijken ](#best-practices).

+++ Voorbeeldcode weergeven

```handlebars
{{#each context.journey.events.event_ID.categories as |category|}}
  <h2>{{category.name}}</h2>
  <ul>
    {{#each category.items as |item|}}
      <li>{{item.title}}</li>
    {{/each}}
  </ul>
{{/each}}
```

+++

## Doorlopen van aangepaste handelingsreacties {#custom-action-responses}

[ de actie van de Douane ](../action/about-custom-action-configuration.md) reacties bevatten gegevens die van externe API vraag zijn teruggekeerd. Dit is nuttig om informatie in real time van uw systemen, zoals loyaliteitspunten, productaanbevelingen, inventarisstatus, of gepersonaliseerde aanbiedingen te tonen.

>[!NOTE]
>
>De acties van de douane moeten met een reactielading worden gevormd om deze eigenschap te gebruiken. Leer meer in [ deze sectie ](../action/action-response.md#config-response). U kunt de reacties van de douaneactie met gebeurtenisgegevens of datasetraadplegingen ook combineren - zie [ veelvoudige contextbronnen ](#combine-sources) voor voorbeelden combineren.

### Contextpad voor aangepaste handelingen

```handlebars
context.journey.actions.<actionName>.<fieldPath>
```

* `<actionName>`: De naam van uw [ douaneactie ](../action/about-custom-action-configuration.md) zoals gevormd in de reis
* `<fieldPath>`: Het pad naar het veld of de array binnen de antwoordlading

### Voorbeeld: productaanbevelingen van een API

Als uw aangepaste actie productaanbevelingen oplevert:

+++ Voorbeeldcode weergeven

**API Reactie:**

```json
{
  "recommendations": [
    {
      "productId": "12345",
      "productName": "Summer Jacket",
      "price": 89.99,
      "imageUrl": "https://example.com/jacket.jpg"
    },
    {
      "productId": "67890",
      "productName": "Running Shoes",
      "price": 129.99,
      "imageUrl": "https://example.com/shoes.jpg"
    }
  ]
}
```

**verpersoonlijking van het Bericht:**

```handlebars
<h2>Recommended for You</h2>
<div class="recommendations">
  {{#each context.journey.actions.GetRecommendations.recommendations as |item|}}
    <div class="product-card">
      <img src="{{item.imageUrl}}" alt="{{item.productName}}" />
      <h3>{{item.productName}}</h3>
      <p class="price">${{item.price}}</p>
    </div>
  {{/each}}
</div>
```

+++

### Voorbeeld: geneste arrays van aangepaste handelingen

Als uw aangepaste handeling geneste arrays retourneert (bijvoorbeeld categorieën met producten). Voor complexere het nestelen patronen, zie [ Beste praktijken ](#best-practices).

+++ Voorbeeldcode weergeven

**API Reactie:**

```json
{    
  "id": "84632848268632",    
  "responses": [
    { "productIDs": [1111, 2222, 3333] },
    { "productIDs": [4444, 5555, 6666] },
    { "productIDs": [7777, 8888, 9999] }
  ]
}
```

**verpersoonlijking van het Bericht:**

```handlebars
<h2>Product Groups</h2>
{{#each context.journey.actions.GetProducts.responses as |response|}}
  <div class="product-group">
    <ul>
      {{#each response.productIDs as |productID|}}
        <li>Product ID: {{productID}}</li>
      {{/each}}
    </ul>
  </div>
{{/each}}
```

+++

### Voorbeeld: Uitkeringen in het kader van het keuzerecht

Dynamische voordelen weergeven op basis van loyaliteitsstatus:

+++ Voorbeeldcode weergeven

**API Reactie:**

```json
{
  "loyaltyTier": "gold",
  "benefits": [
    { "name": "Free shipping", "icon": "truck" },
    { "name": "20% discount", "icon": "percent" },
    { "name": "Priority support", "icon": "headset" }
  ]
}
```

**verpersoonlijking van het Bericht:**

```handlebars
<h2>Your {{context.journey.actions.GetLoyaltyInfo.loyaltyTier}} Member Benefits</h2>
<ul class="benefits">
  {{#each context.journey.actions.GetLoyaltyInfo.benefits as |benefit|}}
    <li>
      <span class="icon-{{benefit.icon}}"></span>
      {{benefit.name}}
    </li>
  {{/each}}
</ul>
```

+++

## Doorlopen van zoekresultaten van gegevensset {#dataset-lookup}

De [ activiteit van de Opzoeken van de Dataset ](../building-journeys/dataset-lookup.md) staat u toe om gegevens van [ datasets van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target="_blank"} tijdens reis runtime terug te winnen. De verrijkte gegevens worden opgeslagen als een array en kunnen in uw berichten worden herhaald.

>[!AVAILABILITY]
>
>De opzoekactiviteit van de Dataset is slechts beschikbaar voor een beperkte reeks organisaties. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

Leer meer over het vormen van de activiteit van de Lookup van de Dataset in [ deze sectie ](../building-journeys/dataset-lookup.md). De raadpleging van de Dataset is bijzonder krachtig wanneer gecombineerd met gebeurtenisgegevens - zie [ Voorbeeld: de gegevens van de gebeurtenis die met datasetraadpleging ](#combine-sources) voor een praktisch gebruiksgeval worden verrijkt.

### Contextpad voor raadpleging van gegevenssets

```handlebars
context.journey.datasetLookup.<activityID>.entities
```

* `<activityID>`: De unieke id van uw opzoekactiviteit in de gegevensset
* `entities`: De array met verrijkte gegevens die uit de gegevensset zijn opgehaald

### Voorbeeld: Productgegevens uit een dataset

Als u een activiteit gebruikt van de Opzoeken van de Dataset om productinformatie terug te winnen die op SKUs wordt gebaseerd:

+++ Voorbeeldcode weergeven

**Configuratie van de Opzoeken van de Dataset:**

* Toetsen opzoeken: `list(@event{purchase_event.products.sku})`
* Te retourneren velden: `["SKU", "category", "price", "name"]`

**verpersoonlijking van het Bericht:**

```handlebars
<h2>Product Details</h2>
<table>
  <thead>
    <tr>
      <th>Product Name</th>
      <th>Category</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    {{#each context.journey.datasetLookup.3709000.entities as |product|}}
      <tr>
        <td>{{product.name}}</td>
        <td>{{product.category}}</td>
        <td>${{product.price}}</td>
      </tr>
    {{/each}}
  </tbody>
</table>
```

+++

### Voorbeeld: gefilterde herhaling met gegevenssetgegevens

Alleen producten van een bepaalde categorie weergeven. Leer meer over voorwaardelijk filtreren in [ Beste praktijken ](#best-practices).

+++ Voorbeeldcode weergeven

```handlebars
<h2>Household Products</h2>
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {{#if product.category = "household"}}
    <div class="product">
      <h3>{{product.name}}</h3>
      <p>Price: ${{product.price}}</p>
    </div>
  {{/if}}
{{/each}}
```

+++

### Voorbeeld: totalen berekenen uit de zoekopdracht van de gegevensset

+++ Voorbeeldcode weergeven

```handlebars
{% let householdTotal = 0 %}
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {%#if product.category = "household"%}
    {% let householdTotal = householdTotal + product.price %}
  {%/if%}
{{/each}}

<p>Your household products total: ${{householdTotal}}</p>
```

+++

## Technische eigenschappen van reis gebruiken {#technical-properties}

De technische eigenschappen van de reis verlenen toegang tot meta-gegevens over de reisuitvoering, zoals reis ID en supplementaire herkenningstekens. Deze kunnen nuttig zijn wanneer gecombineerd met iteratiepatronen, vooral voor het filteren van arrays op basis van specifieke trajectinstanties.

### Beschikbare technische eigenschappen

```handlebars
context.journey.technicalProperties.journeyUID
context.journey.technicalProperties.supplementalId
```

### Voorbeeld: arrayitems filteren met aanvullende id

Wanneer u aanvullende id&#39;s gebruikt bij een door een gebeurtenis geïnitieerde reis met een array, kunt u filteren om alleen het relevante item voor de huidige reisinstantie weer te geven. Leer meer over supplementaire herkenningstekens in [ deze gids ](../building-journeys/supplemental-identifier.md).

**Scenario**: Een reis wordt teweeggebracht met veelvoudige boekingen, maar u wilt informatie slechts voor het specifieke boeken (die door supplementaire identiteitskaart wordt geïdentificeerd) tonen die deze reisinstantie teweegbracht.

+++ Voorbeeldcode weergeven

```handlebars
{{#each context.journey.events.event_ID.bookingList as |booking|}}
  {%#if booking.bookingInfo.bookingNum = context.journey.technicalProperties.supplementalId%}
    <div class="booking-details">
      <h3>Your Booking: {{booking.bookingInfo.bookingNum}}</h3>
      <p>Destination: {{booking.bookingInfo.bookingCountry}}</p>
      <p>Date: {{booking.bookingInfo.bookingDate}}</p>
    </div>
  {%/if%}
{{/each}}
```

+++

### Voorbeeld: reis-id opnemen voor tracering

+++ Voorbeeldcode weergeven

```handlebars
<footer>
  <p>Journey Reference: {{context.journey.technicalProperties.journeyUID}}</p>
</footer>
```

+++

## Meerdere contextbronnen combineren {#combine-sources}

U kunt gegevens uit verschillende bronnen in het zelfde bericht combineren om rijke, gepersonaliseerde ervaringen tot stand te brengen. Deze sectie toont praktische voorbeelden om veelvoudige contextbronnen samen te gebruiken.

**de bronnen van de context u kunt combineren:**

* [ gegevens van de Gebeurtenis ](#event-data) + [ de actierespons van de Douane ](#custom-action-responses)
* [ gegevens van de Gebeurtenis ](#event-data) + [ de raadpleging van de Dataset ](#dataset-lookup)
* [ Veelvoudige bronnen ](#combine-sources) + [ Technische eigenschappen ](#technical-properties)

### Voorbeeld: Winkelobjecten met real-time voorraad

Gebeurtenisgegevens (inhoud van winkelwagentje) combineren met aangepaste actiegegevens (voorraadstatus):

+++ Voorbeeldcode weergeven

```handlebars
<h2>Your Cart</h2>
{{#each context.journey.events.cartEvent.productListItems as |product|}}
  <div class="cart-item">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}

<h2>We Also Recommend</h2>
{{#each context.journey.actions.GetRecommendations.items as |recommendation|}}
  <div class="recommendation">
    <h4>{{recommendation.name}}</h4>
    <p>${{recommendation.price}}</p>
    {{#if recommendation.inStock}}
      <span class="badge">In Stock</span>
    {{else}}
      <span class="badge out-of-stock">Out of Stock</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### Voorbeeld: Gebeurtenisgegevens die zijn verrijkt met zoekopdracht voor gegevenssets

Combineer [ gebeurtenis SKUs ](#event-data) met gedetailleerde productinformatie van de raadpleging van de a [ dataset ](#dataset-lookup):

+++ Voorbeeldcode weergeven

```handlebars
<h2>Your Order Details</h2>
{{#each context.journey.events.orderEvent.productListItems as |item|}}
  <div class="order-item">
    <p><strong>SKU:</strong> {{item.SKU}}</p>
    <p><strong>Quantity:</strong> {{item.quantity}}</p>
    
    <!-- Enrich with dataset lookup data -->
    {{#each context.journey.datasetLookup.1234567.entities as |enrichedProduct|}}
      {{#if enrichedProduct.SKU = item.SKU}}
        <p><strong>Product Name:</strong> {{enrichedProduct.name}}</p>
        <p><strong>Category:</strong> {{enrichedProduct.category}}</p>
        <img src="{{enrichedProduct.imageUrl}}" alt="{{enrichedProduct.name}}" />
      {{/if}}
    {{/each}}
  </div>
{{/each}}
```

+++

### Voorbeeld: Meerdere bronnen combineren met technische eigenschappen

+++ Voorbeeldcode weergeven

```handlebars
<div class="personalized-content">
  <!-- Profile data -->
  <h1>Hello {{profile.person.name.firstName}},</h1>
  
  <!-- Event data iteration -->
  <h2>Your Recent Purchases</h2>
  {{#each context.journey.events.purchaseEvent.items as |purchase|}}
    <div class="purchase">
      <p>{{purchase.productName}} - ${{purchase.price}}</p>
    </div>
  {{/each}}
  
  <!-- Custom action response iteration -->
  <h2>Recommended for You</h2>
  {{#each context.journey.actions.GetPersonalizedRecs.recommendations as |rec|}}
    <div class="recommendation">
      <h3>{{rec.title}}</h3>
      <p>{{rec.description}}</p>
    </div>
  {{/each}}
  
  <!-- Technical properties -->
  <footer>
    <p class="fine-print">Journey ID: {{context.journey.technicalProperties.journeyUID}}</p>
  </footer>
</div>
```

+++

## Andere contexttypen {#other-contexts}

Terwijl deze gids zich op herhaling over series concentreert, zijn andere contexttypes beschikbaar voor verpersoonlijking die typisch geen herhaling vereisen. Deze worden direct benaderd in plaats van via een lus te herhalen:

* **[de attributen van het Profiel ](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"}** (`profile.*`): Individuele profielgebieden van Adobe Experience Platform
* **[Soorten publiek](../audience/about-audiences.md)** (`inAudience()`): De controles van het lidmaatschapsaandeel van het publiek
* **[de besluiten van het Aanbod](../offers/get-started/starting-offer-decisioning.md)**: De aanbiedingen van het besluitvormingsbeheer
* **[attributen van het Doel](../orchestrated/activities/channels.md#add-personalization)** (Beweerde campagnes slechts): Attributen die in het campagnecanvas worden berekend
* **Symbolisch** (`context.token`): De tokens van de zitting of van de authentificatie

Voor volledige verpersoonlijkingssyntaxis en voorbeelden die deze bronnen gebruiken, verwijs naar:

* [Aanpassing toevoegen](personalization-build-expressions.md)
* [Personalization-syntaxis](personalization-syntax.md)

## Werken met arrays in Journey-expressies {#arrays-in-journeys}

Terwijl de vorige secties zich bij herhaling over series in berichtverpersoonlijking gebruikend Handlebars concentreren, werkt u ook met series wanneer het vormen van reisactiviteiten. In deze sectie wordt uitgelegd hoe u arraygegevens uit gebeurtenissen in Journey-expressies kunt gebruiken, met name wanneer u gegevens doorgeeft aan aangepaste handelingen of wanneer u arrays met datasetlookups gebruikt.

>[!IMPORTANT]
>
>Reisexpressies gebruiken een andere syntaxis dan Handlebars personalisatie. In reisconfiguratie (zoals parameters of voorwaarden van de douaneactie), gebruikt u de [ redacteur van de de uitdrukkingsuitdrukking van de Reis ](../building-journeys/expression/expressionadvanced.md) met functies zoals `first`, `all`, en `serializeList`. In berichtinhoud gebruikt u de syntaxis Handlebars met `{{#each}}` lussen.

### Arraywaarden aan aangepaste actieparameters doorgeven {#arrays-to-custom-actions}

Wanneer het vormen van [ douaneacties ](../action/about-custom-action-configuration.md), moet u vaak waarden uit gebeurtenisseries halen en hen als parameters overgaan. Deze sectie behandelt gemeenschappelijke patronen.

Leer meer over het overgaan van inzamelingen in [ inzamelingen van de Pas in de parameters van de douaneactie ](../building-journeys/collections.md#passing-collection).

#### Eén waarde uit een array extraheren

**Geval van het Gebruik**: Krijg een specifiek gebied van een gebeurtenisserie om als vraagparameter in een verzoek van GET over te gaan.

**scenario van het Voorbeeld**: Extraheer eerste SKU met een prijs groter dan 0 van een productlijst.

+++ Voorbeeldcode weergeven

**het schemavoorbeeld van de Gebeurtenis**:

```json
{
  "commerce": {
    "productListItems": [
      { "SKU": "SKU-1", "priceTotal": 10.0 },
      { "SKU": "SKU-2", "priceTotal": 0.0 },
      { "SKU": "SKU-3", "priceTotal": 20.0 }
    ]
  }
}
```

**de actieconfiguratie van de Douane**:

1. Configureer in uw aangepaste handeling een queryparameter (bijvoorbeeld `sku` ) met type `string`
2. Markeer het als `Variable` om dynamische waarden toe te staan

**uitdrukking van de Reis in actieparameter**:

```javascript
@event{YourEventName.commerce.productListItems.first(currentEventField.priceTotal > 0).SKU}
```

**Verklaring**:

* `@event{YourEventName}`: verwijst naar uw reisgebeurtenis
* `.first(currentEventField.condition)`: retourneert het eerste arrayitem dat overeenkomt met de voorwaarde
* `currentEventField`: vertegenwoordigt elk item in de gebeurtenisarray terwijl u deze doorloopt
* `.SKU`: extraheert het SKU-veld van het overeenkomende item
* Resultaat: `"SKU-1"` (een tekenreeks die geschikt is voor de parameter action)

Leer meer over de `first` functie in [ het beheersfuncties van de Inzameling ](../building-journeys/expression/collection-management-functions.md).

+++

#### Een lijst met waarden op basis van een array maken

**geval van het Gebruik**: Creeer een komma-gescheiden lijst van IDs om als vraagparameter over te gaan (b.v., `/products?ids=sku1,sku2,sku3`).

+++ Voorbeeldcode weergeven

**de actieconfiguratie van de Douane**:

1. Een queryparameter (bijvoorbeeld `ids` ) configureren met type `string`
2. Markeren als `Variable`

**uitdrukking van de Reis**:

```javascript
serializeList(
  @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0).SKU},
  ",",
  true
)
```

**Verklaring**:

* `.all(currentEventField.condition)`: retourneert alle arrayitems die overeenkomen met de voorwaarde (retourneert een lijst)
* `currentEventField`: vertegenwoordigt elk item in de gebeurtenisarray terwijl u deze doorloopt
* `.SKU`: hiermee wordt in de lijst alleen SKU-waarden opgenomen
* `serializeList(list, delimiter, addQuotes)`: Voegt de lijst samen tot een tekenreeks
   * `","`: komma als scheidingsteken gebruiken
   * `true`: voeg aanhalingstekens toe rond elk tekenreekselement
* Resultaat: `"SKU-1,SKU-3"` (geschikt voor een queryparameter)

Meer informatie over:

* [&quot;all&quot;](../building-journeys/expression/collection-management-functions.md)
* [` serializeList`](../building-journeys/functions/list-functions.md#serializeList)

De behandeling van de inzameling voor douaneacties wordt behandeld in [ inzamelingen van de Pas in de parameters van de douaneactie ](../building-journeys/collections.md#passing-collection).

+++

#### Een array van objecten doorgeven aan een aangepaste handeling

**geval van het Gebruik**: verzend een volledige serie van voorwerpen in een verzoeklichaam (voor POST of GET met lichaam).

+++ Voorbeeldcode weergeven

**het lichaamsvoorbeeld van het Verzoek**:

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "Product A",
        "price": 20.1,
        "color": "blue"
      }
    ]
  }
}
```

**de actieconfiguratie van de Douane**:

1. Definieer in de hoofdtekst van de aanvraag `products` als type `listObject`
2. Markeren als `Variable`
3. Definieer de objectvelden: `id` , `name` , `price` , `color` (elk wordt toegewezen)

**de configuratie van het canvas van de Reis**:

1. Stel in de modus Geavanceerd de verzamelingsexpressie in:

   ```javascript
   @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0)}
   ```

1. In de interface voor verzamelingstoewijzing:
   * Kaart `id` → `productListItems.SKU`
   * Kaart `name` → `productListItems.name`
   * Kaart `price` → `productListItems.priceTotal`
   * Kaart `color` → `productListItems.color`

Journey Optimizer maakt de array met objecten die overeenkomen met de payload-structuur van de handeling.

>[!NOTE]
>
>Wanneer u werkt met gebeurtenisarrays, gebruikt u `currentEventField` om naar elk item te verwijzen. Gebruik `currentDataPackField` voor gegevensbronverzamelingen (Adobe Experience Platform). Gebruik `currentActionField` voor aangepaste actieverzamelingen.

Leer meer in [ inzamelingen van de pas in de parameters van de douaneactie ](../building-journeys/collections.md#passing-collection).

+++

### Arrays met datasetraadplegingen gebruiken {#arrays-with-dataset-lookup}

Wanneer het gebruiken van de [ activiteit van de Lookup van de Dataset ](../building-journeys/dataset-lookup.md), kunt u een serie van waarden als raadplegingssleutels overgaan om verrijkte gegevens terug te winnen.

**Voorbeeld**: Bekijk productdetails voor alle SKUs in een gebeurtenisserie.

+++ Voorbeeldcode weergeven

**de configuratie van de Opzoekup van de 0} Dataset:**

In het veld Opzoeksleutels gebruikt u `list()` om een arraypad om te zetten in een lijst:

```javascript
list(@event{purchaseEvent.productListItems.SKU})
```

Dit leidt tot een lijst van alle waarden van SKU omhoog in de dataset te kijken. De resultaten zijn beschikbaar als serie bij `context.journey.datasetLookup.<activityID>.entities` die u over in uw bericht kunt herhalen (zie [ over de resultaten van de datasetraadpleging herhalen ](#dataset-lookup)).

+++

### Beperkingen en patronen {#array-limitations}

Houd rekening met deze beperkingen wanneer u werkt met arrays in ritten:

#### Geen dynamische lusbewerking over arrays in transportflow

De reizen kunnen geen dynamische lijnen tot stand brengen waar één actieknooppunt veelvoudige tijden voor elk punt in een serie wordt uitgevoerd. Dit is bedoeld om problemen met runaway-prestaties te voorkomen.

**wat u niet** kunt doen:

* Een aangepaste handeling één keer per arrayitem dynamisch uitvoeren
* Meerdere reistakken maken op basis van arraylengte

**Aanbevolen patronen in plaats daarvan**:

1. **verzend alle punten meteen**: Ga de volledige serie of een geserialiseerde lijst tot één enkele douaneactie over die alle punten verwerkt. Zie [ een lijst van waarden van een serie ](#arrays-to-custom-actions) bouwen.

2. **de externe samenvoeging van het Gebruik**: Heb uw externe API veelvoudige IDs goedkeuren en gecombineerde resultaten in één enkele vraag terugkeren.

3. **pre-compute in AEP**: Gebruik [ gegevens verwerkte attributen ](../audience/computed-attributes.md) om waarden van series op het profielniveau vooraf te berekenen.

4. **Enige waardeextractie**: Als u slechts één waarde nodig hebt, haal het gebruikend `first` of `head`. Zie [ één enkele waarde van een serie ](#arrays-to-custom-actions) extraheren.

Leer meer in [ Grafieken en beperkingen ](../start/guardrails.md).

#### Overwegingen voor arraygrootte

Grote arrays kunnen de reisprestaties beïnvloeden:

* **de series van de Gebeurtenis**: Houd gebeurtenislading onder totaal 50KB
* **de actieantwoorden van de Actie van de Douane**: De nuttige lading van de reactie zou onder 100KB moeten zijn
* **de raadplegingsresultaten van de Dataset**: Beperk het aantal raadplegingssleutels en teruggekeerde entiteiten

### Volledig voorbeeld: gebeurtenisarray naar aangepaste handeling {#complete-example}

Hier volgt een volledige workflow waarin wordt getoond hoe u een gebeurtenisarray kunt gebruiken met een aangepaste handeling.

**Scenario**: Wanneer een gebruiker hun kar verlaat, verzendt het kartgegevens naar een externe aanbeveling API om gepersonaliseerde suggesties te krijgen, dan hen in een e-mail te tonen.

+++ Volledig voorbeeld weergeven

**Stap 1: Vorm de douaneactie**

Maak een aangepaste handeling &quot;GetCartRecommendations&quot;:

* **Methode**: POST
* **URL**: `https://api.example.com/recommendations`
* **het lichaam van het Verzoek**:

```json
{
  "cartItems": [
    {
      "sku": "string",
      "price": 0,
      "quantity": 0
    }
  ]
}
```

* `cartItems` markeren als type `listObject` en `Variable`
* Definieer velden: `sku` (string), `price` (number), `quantity` (integer)

Leer meer in [ een douaneactie ](../action/about-custom-action-configuration.md) vormen.

**Stap 2: Vorm antwoordlading**

In de douaneactie, vorm de reactie:

```json
{
  "recommendations": [
    {
      "productId": "string",
      "productName": "string",
      "price": 0,
      "imageUrl": "string"
    }
  ]
}
```

Leer meer in [ de vraagreacties van API van het Gebruik ](../action/action-response.md).

**Stap 3: Bouw de actie in de reis**

1. Voeg de aangepaste handeling toe nadat de gebeurtenis waarmee u het winkelwagentje hebt verlaten, is uitgevoerd
1. In de modus Geavanceerd voor de `cartItems` -verzameling:

   ```javascript
   @event{cartAbandonment.commerce.productListItems.all(currentEventField.quantity > 0)}
   ```

1. De verzamelingsvelden toewijzen:
   * `sku` → `productListItems.SKU`
   * `price` → `productListItems.priceTotal`
   * `quantity` → `productListItems.quantity`

**Stap 4: Gebruik de reactie in uw e-mail**

Doorloop de aanbevelingen in uw e-mailinhoud:

```handlebars
<h2>We noticed you left these items in your cart</h2>
{{#each context.journey.events.cartAbandonment.productListItems as |item|}}
  <div class="cart-item">
    <p>{{item.name}} - Quantity: {{item.quantity}}</p>
  </div>
{{/each}}

<h2>You might also like</h2>
{{#each context.journey.actions.GetCartRecommendations.recommendations as |rec|}}
  <div class="recommendation">
    <img src="{{rec.imageUrl}}" alt="{{rec.productName}}" />
    <h3>{{rec.productName}}</h3>
    <p>${{rec.price}}</p>
  </div>
{{/each}}
```

**Stap 5: Test uw configuratie**

Alvorens een levende reis in werking te stellen, test de douaneactie gebruikend de &quot;Send testverzoek&quot;eigenschap in de actieconfiguratie om het gebouwde verzoek en de waarden te verifiëren.

1. De wijze van de de reistest van het gebruik [](../building-journeys/testing-the-journey.md)
2. Trigger met voorbeeldgebeurtenisgegevens, inclusief een `productListItems` -array
3. Controleren of de aangepaste handeling de juiste arraystructuur ontvangt
4. Controle de [ logboeken van de actietest ](../action/action-response.md#test-mode-logs)
5. Een voorbeeld van de e-mail bekijken om te controleren of beide arrays correct worden weergegeven

Leer meer in [ problemen oplossen uw douaneacties ](../action/troubleshoot-custom-action.md).

+++

## Best practices {#best-practices}

Volg deze tips en trucs bij het doorlopen van contextuele gegevens om een onderhoudsvriendelijke, krachtige personalisatie te maken.

### Beschrijvende variabelenamen gebruiken

Kies variabelenamen die duidelijk aangeven waar u doorheen gaat. Hierdoor wordt uw code beter leesbaar en eenvoudiger te onderhouden. Leer meer over [ verpersoonlijkingssyntaxis ](personalization-syntax.md):

+++ Voorbeeld weergeven

```handlebars
<!-- Good -->
{{#each products as |product|}}
{{#each users as |user|}}
{{#each recommendations as |recommendation|}}

<!-- Less clear -->
{{#each items as |item|}}
{{#each array as |element|}}
```

+++

### Lege arrays verwerken

Gebruik de component `{{else}}` om fallback-inhoud op te geven wanneer een array leeg is. Leer meer over [ helperfuncties ](functions/helpers.md):

+++ Voorbeeld weergeven

```handlebars
{{#each context.journey.actions.GetRecommendations.items as |item|}}
  <div>{{item.name}}</div>
{{else}}
  <p>No recommendations available at this time.</p>
{{/each}}
```

+++

### Combineren met voorwaardelijke hulplijnen

Gebruik `{{#if}}` binnen lussen voor voorwaardelijke inhoud. Leer meer over [ voorwaardelijke regels ](create-conditions.md) en zie voorbeelden in [ de actieresultaten van de Douane ](#custom-action-responses) en [ de raadplegings ](#dataset-lookup) secties van de Dataset.

+++ Voorbeeld weergeven

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    {{#if product.onSale}}
      <span class="badge">On Sale!</span>
    {{/if}}
    {{#if product.newArrival}}
      <span class="badge">New</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### Herhaling van prestaties beperken

Bij grote arrays kunt u het aantal herhalingen beperken:

+++ Voorbeeld weergeven

```handlebars
<!-- Display only first 5 items -->
{{#each context.journey.actions.GetProducts.items as |product|}}
  {{#if @index < 5}}
    <div>{{product.name}}</div>
  {{/if}}
{{/each}}
```

+++

### Metagegevens van arrays openen

Handlebars verstrekt speciale variabelen binnen lijnen die met geavanceerde iteratiepatronen helpen:

* `@index`: Huidige iteratie-index (op basis van 0)
* `@first`: waar voor de eerste herhaling
* `@last`: waar voor de laatste herhaling

+++ Voorbeeld weergeven

```handlebars
{{#each products as |product|}}
  <div class="product {{#if @first}}featured{{/if}}">
    {{@index}}. {{product.name}}
  </div>
{{/each}}
```

+++

>[!NOTE]
>
>Deze Handlebars variabelen (`@index`, `@first`, `@last`) zijn slechts beschikbaar binnen `{{#each}}` lijnen in berichtverpersoonlijking. Wanneer u met arrays werkt in Journey-expressies (zoals wanneer u het eerste item van een array ophaalt voordat u doorgeeft aan een aangepaste handeling), gebruikt u arrayfuncties zoals [`head`](../personalization/functions/arrays-list.md#head) , [`first`](../building-journeys/expression/collection-management-functions.md) of [`all`](../building-journeys/expression/collection-management-functions.md) . Zie [ Werk met series in de uitdrukkingen van de Reis ](#arrays-in-journeys) voor meer details.

## Problemen oplossen {#troubleshooting}

Heb je problemen met iteratie? In deze sectie worden gemeenschappelijke problemen en oplossingen besproken.

### Array wordt niet weergegeven

**Uitgave**: Uw serieherhaling toont geen inhoud.

+++ Mogelijke oorzaken en oplossingen weergeven

**Mogelijke oorzaken en oplossingen**:

1. **Onjuiste weg**: Verifieer de nauwkeurige weg aan uw serie die op de contextbron wordt gebaseerd:
   * Voor [ gebeurtenissen ](#event-data): `context.journey.events.<event_ID>.<fieldPath>`
   * Voor [ douaneacties ](#custom-action-responses): `context.journey.actions.<actionName>.<fieldPath>`
   * Voor [ datasetraadplegingen ](#dataset-lookup): `context.journey.datasetLookup.<activityID>.entities`

2. **Serie is leeg**: Voeg een `{{else}}` clausule toe om te controleren als de serie geen gegevens heeft. Zie [ Beste praktijken ](#best-practices) voor voorbeelden.

3. **Gegevens nog niet beschikbaar**: Verzeker de douaneactie, de gebeurtenis, of activiteit van de datasetraadpleging is uitgevoerd vóór de berichtactiviteit in uw reisstroom.

+++

### Syntaxisfouten

**Uitgave**: De bevestiging van de uitdrukking ontbreekt of het bericht geeft niet terug.

+++ Algemene fouten weergeven

**Gemeenschappelijke fouten**:

* Ontbrekende afsluitende tags: Elke `{{#each}}` moet een `{{/each}}` hebben. De iteratiesyntaxis van het overzicht [ Handlebars ](#syntax) voor juiste structuur.
* Onjuiste variabelenaam: zorg ervoor dat de variabelenaam overal in het blok consistent wordt gebruikt. Zie [ Beste praktijken ](#best-practices) voor het noemen van overeenkomsten.
* Onjuiste padscheidingstekens: gebruik punten (`.`) geen schuine strepen of andere tekens

+++

### Uw herhalingen testen

Gebruik [ de wijze van de 0} reistest om uw herhalingen te verifiëren. ](../building-journeys/testing-the-journey.md) Dit is vooral belangrijk wanneer het gebruiken van [ douaneacties ](#custom-action-responses) of [ datasetraadplegingen ](#dataset-lookup):

+++ Teststappen weergeven

1. Begin uw reis op [ testwijze ](../building-journeys/testing-the-journey.md)
2. De gebeurtenis of aangepaste handeling activeren met voorbeeldgegevens
3. Controle de [ berichtvoorproef ](../content-management/preview.md) om de herhalingsvertoningen correct te verifiëren
4. De logboeken van de de testwijze van het overzicht voor om het even welke fouten (zie [ Logboeken van de actietest van de Douane van de actie ](../action/action-response.md#test-mode-logs))

+++

## Verwante onderwerpen {#related-topics}

**fundamentals van Personalization:** [ begonnen met verpersoonlijking ](personalize.md) | [ voeg verpersoonlijking ](personalization-build-expressions.md) toe | [ syntaxis van Personalization ](personalization-syntax.md) | [ de functies van de Helper ](functions/helpers.md) | [ creeer voorwaardelijke regels ](create-conditions.md)

**configuratie van de Reis:** [ Ongeveer gebeurtenissen ](../event/about-events.md) | [ vorm douaneacties ](../action/about-custom-action-configuration.md) | [ de inzamelingen van de pas in de parameters van de douaneactie ](../building-journeys/collections.md#passing-collection) | [ API van het Gebruik vraagreacties in douaneacties ](../action/action-response.md) | [ los uw douaneacties ](../action/troubleshoot-custom-action.md) problemen op | [ de gegevens van Adobe Experience Platform van het Gebruik in reizen ](../building-journeys/dataset-lookup.md) | [ Aanvullende herkenningstekens van het Gebruik in reizen ](../building-journeys/supplemental-identifier.md) | [ Grafieken en beperkingen ](../start/guardrails.md) | [ Test uw reis ](../building-journeys/testing-the-journey.md)

**de uitdrukkingsfuncties van de Reis:** [ Geavanceerde uitdrukkingsredacteur ](../building-journeys/expression/expressionadvanced.md) | [ het beheersfuncties van de Inzameling ](../building-journeys/expression/collection-management-functions.md) (eerst, allen, laatste) | [ functies van de Lijst ](../building-journeys/functions/list-functions.md) (serializeList, filter, soort) | [ de functies van de Serie ](../personalization/functions/arrays-list.md) (hoofd, staart)

**Personalization gebruiksgevallen:** [ de verlaten e-mail van de Kunst ](personalization-use-case-helper-functions.md) | [ de statusbericht van de Orde ](personalization-use-case.md)

**ontwerp van het Bericht:** [ begonnen met e-mailontwerp ](../email/get-started-email-design.md) | [ creeer dupberichten ](../push/create-push.md) | [ creeer SMS berichten ](../sms/create-sms.md) | [ Voorproef en test uw inhoud ](../content-management/preview-test.md)

