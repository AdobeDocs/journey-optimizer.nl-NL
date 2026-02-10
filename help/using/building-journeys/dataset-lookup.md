---
solution: Journey Optimizer
product: journey optimizer
title: ' [!DNL Adobe Experience Platform]  gegevens van het gebruik in reizen'
description: Leer hoe te om de Activiteit van de Opzoeken van de Dataset in  [!DNL Adobe Journey Optimizer]  te gebruiken om klantenreizen met externe gegevens van  [!DNL Adobe Experience Platform] te verrijken.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Beperkte beschikbaarheid" type="Informative"
exl-id: b6f54a79-b9e7-4b3a-9a6f-72d5282c01d3
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# [!DNL Adobe Experience Platform] -gegevens gebruiken tijdens reizen {#datalookup}

>[!CONTEXTUALHELP]
>id="ajo_journey_dataset_lookup"
>title="Opzoekactiviteit gegevensset"
>abstract="Met de **[!UICONTROL Dataset lookup]** -activiteit kunt u tijdens runtime dynamisch gegevens ophalen uit [!DNL Adobe Experience Platform] -recordgegevenssets. Door gebruik te maken van deze mogelijkheid hebt u toegang tot gegevens die mogelijk niet in het profiel of de lading van de gebeurtenis zijn opgeslagen, zodat uw klanteninteractie zowel relevant als tijdig is."

Met de **[!UICONTROL Dataset lookup]** -activiteit kunt u tijdens runtime dynamisch gegevens ophalen uit [!DNL Adobe Experience Platform] -recordgegevenssets. Door gebruik te maken van deze mogelijkheid hebt u toegang tot gegevens die mogelijk niet in het profiel of de lading van de gebeurtenis zijn opgeslagen, zodat uw klanteninteractie zowel relevant als tijdig is.

Belangrijkste voordelen:

* **Echte - tijd verpersoonlijking**: De klantenervaringen van de spoorstaaf gebruikend verrijkte gegevens.
* **Dynamische besluitvorming**: De externe gegevens van het gebruik om reislogica en acties te drijven.
* **Verbeterde Toegang van gegevens**: Haal productmeta-gegevens, het tarief lijsten, of relationele gegevens terug verbonden aan specifieke sleutels.

>[!AVAILABILITY]
>
>Deze activiteit is slechts beschikbaar voor een reeks organisaties (Beperkte Beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

## Meer lezen {#must-read}

Herzie deze vereisten alvorens u datasetraadplegingen vormt.

### Gegevensset inschakelen

De dataset moet voor raadpleging in [!DNL Adobe Experience Platform] worden toegelaten. De gedetailleerde informatie is beschikbaar in deze sectie: [ gegevens van het 1} Gebruik  [!DNL Adobe Experience Platform] .](../data/lookup-aep-data.md)

### Beperkingen en beperkingen

* Maximaal 10 opzoekactiviteiten voor gegevenssets per reis.
* Maximaal 20 geselecteerde velden.
* Maximaal 50 toetsen in de array met opzoeksleutels.
* De verrijkte gegevensgrootte is beperkt tot 10KB.

### Aanvullende prestatieoverwegingen

De volgende aanbevelingen zijn een leidraad om vertragingen in de leverbaarheid te voorkomen:

| Overwegingen | Aanbevolen limiet | Beschrijving |
| ------- | ------- | ------- |
| Kenmerken per opzoekopdracht | Maximaal 20 | Het aantal gegevensvelden dat per record wordt opgehaald in één opzoekactiviteit. |
| Opzoeken | Tot 5 per reis | Elke reis kan tot 5 afzonderlijke raadplegingsactiviteiten bevatten. Elke raadpleging kan een verschillende dataset richten. |

## Vorm de opzoekactiviteit van de Dataset {#configure}

Voer de volgende stappen uit om de **[!UICONTROL Dataset lookup]** -activiteit te configureren:

1. Ontgrendel de categorie **[!UICONTROL Orchestration]** en zet een **[!UICONTROL Dataset lookup]** -activiteit neer op uw canvas.

   ![[!DNL Adobe Experience Platform] activiteit van de datasetraadpleging in reis ](assets/aep-data-activity.png)

1. Voeg een label en beschrijving toe.

1. Selecteer in het veld **[!UICONTROL Dataset]** de gegevensset met de benodigde kenmerken.

   >[!NOTE]
   >
   >Als de dataset u zoekt niet in de lijst toont, zorg ervoor u het voor raadpleging hebt toegelaten. Voor meer details, verwijs naar [ ](#must-read) sectie moet lezen.

1. Selecteer de specifieke gebieden u van de dataset wilt halen.

   * U kunt alleen bladknooppunten selecteren (velden op het laagste niveau van het schema). Het veld moet een primitieve waarde zijn (tekenreeks, getal, boolean, datum, enz.).

   * Lijsten (arrays) en kaarten (sleutelwaardeobjecten) kunnen niet worden geselecteerd.

   +++Voorbeeld

   ![ het gebiedsselectie van de Dataset die primitieve gegevenstypes en structuur tonen ](assets/aep-data-leaf-primitive.png)

   +++

1. Kies in het veld **[!UICONTROL Lookup key(s)]** een verbindingssleutel die bestaat in zowel de kenmerken van het beslissingspunt als de gegevensset. Deze sleutel wordt gebruikt door het systeem om in de geselecteerde dataset te zoeken.

   * Toetsen kunnen expressies zijn die zijn afgeleid van de reiscontext, zoals SKU&#39;s, e-mailadressen of andere id&#39;s. Voorbeeld: `@profile.email` of `list(@event{purchase_event.products.sku})` .

   * Slechts **koorden** of **lijsten van koorden** worden gesteund.

   +++Voorbeeld

   ![ de redacteur van de Uitdrukking met de raadpleging van het gegevenssetgebied en koordfuncties ](assets/aep-data-strings.png)

   +++

## Verrijkte gegevens gebruiken tijdens de rit

De gegevens die door de **[!UICONTROL Dataset lookup]** -activiteit worden opgehaald, worden in de Journey-context opgeslagen als een array van objecten. Het is beschikbaar in de redacteur van de reisuitdrukking en verpersoonlijkingsredacteur, toelatend voorwaardelijke logica en gepersonaliseerd overseinen die op verrijkte gegevens worden gebaseerd.

* **Redacteur van de Uitdrukking van de Reis**:

  Open de editor van **[!UICONTROL Advanced mode]** en gebruik de syntaxis: `@datasetLookup{MyDatasetLookUpActivity1.entities}` . [ Leer hoe te met de geavanceerde uitdrukkingsredacteur te werken ](../building-journeys/expression/expressionadvanced.md)

* **Redacteur van Personalization**:

  Gebruik de syntaxis: `{{context.journey.datasetLookup.1482319411.entities}}`.

>[!NOTE]
>
>Verrijkte gegevens zijn van voorbijgaande aard en zijn alleen beschikbaar tijdens de uitvoering van de reis en bij de personalisatie van uitgaande activiteiten (e-mail, push, SMS, enz.)

## Voorbeelden van gebruiksgevallen

+++Filteren op basis van productcategorie

**Scenario**:Send een coupon aan gebruikers die meer dan $40 aan huisproducten uitgeven.

**de stroom van de Reis**:

1. **Gebeurtenis van de Aankoop**: Vang SKUs van de kar van de gebruiker.

1. **de opzoekactiviteit van 0} Dataset:**

   * Gegevensset: `products-dataset` (SKU als primaire sleutel).
   * Opzoektoetsen: `list(@event{purchase_event.products.sku})`.
   * Te retourneren velden: `["SKU", "category", "price"]`.

1. **de activiteit van de Voorwaarde**:

   * Filter SKU&#39;s waarbij de categorie &quot;huishouden&quot; is.

     ```
     @event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookupActivity1.entities.all(currentDatasetLookupField.category == 'household').sku} ) )} 
     ```

   OF

   * De totale uitgaven voor huishoudelijke producten samenvoegen en vergelijken met de drempel van 40 dollar.

     ```
     sum(@event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookUpActivity1.entities.all(currentDatasetLookupField.category == 'household').sku} ) )}.price}, ',', true ) > 40
     ```

1. **Redacteur van Personalization**:

   Gebruik de verrijkte gegevens om de e-mailinhoud aan te passen:

   ```
   {% let householdTotal = 0 %}
   {{#each journey.datasetlookup.3709000.entities as |product|}}
   {%#if get(product, "category") = "household"%}
   {% let householdTotal = householdTotal + product.price %}{%/if%}
   {{/each}}
   "Hi, thanks for spending " + {%= householdTotal %} + " on household products. Here is your reward!"
   ```

+++

+++Personalization gebruikt externe loyaliteitsgegevens

**Scenario**: Identificeer welke e-mailrekening voor een profiel een Status van de Loyaliteit van Platinum heeft. In dit scenario, wordt de loyaliteitsrekening geassocieerd aan een e-mailidentiteitskaart en de loyaliteitsgegevens zijn niet beschikbaar in de standaard opslag van de profielraadpleging.

**de stroom van de Reis**:

1. **Trigger van de Gebeurtenis van het Profiel**: Leg e-mail IDs van het profiel of gebeurteniscontext vast.

1. **de activiteit van de Opzoeken van de Dataset van 0}:**
   * Gegevensset: `loyalty-member-dataset` (e-mail als primaire sleutel).
   * Opzoektoetsen: `@profile.email`.
   * Te retourneren velden: `["email", "loyaltyTier"]`.

1. **de activiteit van de Voorwaarde**:

   Vertakken de reis die op de loyaliteitsrij wordt gebaseerd:

   ```
   @datasetLookup{MyDatasetLookUpActivity1.entity.loyaltyMember.loyaltyTier} == 'Platinum'
   ```

1. **Redacteur van Personalization**:

   Gebruik de verrijkte gegevens van de loyaliteitsrij om uitgaande mededeling te personaliseren:

   ```
   {{context.journey.datasetLookup.1482319411.entity.loyaltyMember.loyaltyTier}}
   ```
