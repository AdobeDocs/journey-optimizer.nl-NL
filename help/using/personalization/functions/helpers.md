---
title: Helpers
description: Helpers
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: e8ace59ea50d35de1f1b3b9a6417e5eb7961c236
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 1%

---

# Helpers {#gs-helpers}

## Standaardwaarde voor alternatieven{#default-value}

De `Default Fallback Value` helper wordt gebruikt om een standaardreservewaarde terug te keren als een attribuut leeg of ongeldig is. Dit mechanisme werkt voor Profielkenmerken en Reisgebeurtenissen.

**Syntaxis**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

In dit voorbeeld wordt de waarde `there` weergegeven als het `firstName` -kenmerk van dit profiel leeg of null is.

## Voorwaarden{#if-function}

De hulpfunctie `if` wordt gebruikt om een voorwaardelijk blok te definiëren.
Als de uitdrukkingsevaluatie waar terugkeert, wordt het blok teruggegeven anders wordt het overgeslagen.

**Syntaxis**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Na de hulpfunctie `if` kunt u een instructie `else` invoeren om een codeblok op te geven dat moet worden uitgevoerd als dezelfde voorwaarde false is.
De instructie `elseif` geeft een nieuwe voorwaarde op die moet worden getest als de eerste instructie false retourneert.


**Formaat**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**Voorbeelden**

1. **geeft verschillende opslagverbindingen terug die op voorwaardelijke uitdrukkingen** worden gebaseerd

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalog</a>
   {%/if%}
   ```

1. **bepaal de uitbreiding van het e-mailadres**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **voeg een voorwaardelijke verbinding** toe

   Met de volgende bewerking voegt u een koppeling toe naar de website &#39;www.adobe.com/academia&#39; voor profielen met alleen de e-mailadressen &#39;.edu&#39;, naar de website &#39;www.adobe.com/org&#39; voor profielen met de e-mailadressen &#39;.org&#39; en de standaard-URL &#39;www.adobe.com/users&#39; voor alle andere profielen:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Voorwaardelijke inhoud die op publiekslidmaatschap wordt gebaseerd**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Meer over publiek en de segmentatieservice leren, verwijs naar [ deze sectie ](../../audience/about-audiences.md).


## Tenzij{#unless}

De hulpfunctie `unless` wordt gebruikt om een voorwaardelijk blok te definiëren. Als de evaluatie van de expressie false retourneert, wordt het blok gerenderd als dit tegengesteld is aan de `if` helper.

**Syntaxis**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Voorbeeld**

Enige inhoud renderen op basis van extensie e-mailadres:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

## Elk{#each}

De hulpfunctie `each` wordt gebruikt om een array te doorlopen.
De syntaxis van de hulplijn is ```{{#each ArrayName}}``` YourContent `{{/each}}`
Wij kunnen naar de individuele seriepunten verwijzen door het sleutelwoord **dit** binnen het blok te gebruiken. De index van het element van de array kan worden gerenderd met `{{@index}}` .

**Syntaxis**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Voorbeeld**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Voorbeeld**

Een lijst met producten weergeven die deze gebruiker in zijn winkelwagentje heeft:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

>[!NOTE]
>
>U kunt de `each` helper ook gebruiken om arrays die uit aangepaste handelingsreacties zijn geretourneerd, te doorlopen. Voor een voorbeeld om over genestelde series van een reactie van de douaneactie te herhalen, zie [ Gebruikend de reacties van de douaneactie in inheemse kanalen ](../../action/action-response.md#response-in-channels).

## Met{#with}

De `with` helper wordt gebruikt om het evaluatietoken van malplaatje-deel te veranderen.

**Syntaxis**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

De hulpfunctie `with` is nuttig om ook een sneltoetsvariabele te definiëren.

**Voorbeeld**

Wordt gebruikt met voor het aliasing van lange variabelenamen naar kortere namen:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Laat{#let}

Met de functie `let` kan een expressie worden opgeslagen als een variabele die later in een query moet worden gebruikt.

**Syntaxis**

```sql
{% let variable = expression %} {{variable}}
```

**Voorbeeld**

In het volgende voorbeeld kunt u de totale som van prijzen voor producten in de winkelwagen berekenen met prijzen tussen 100 en 1000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

## Opzoeken gegevensset {#dataset-lookup}

>[!AVAILABILITY]
>
>Deze functie is momenteel beschikbaar voor alle klanten als een beperkte beschikbaarheidsrelease.
>
>Momenteel kan de hulpfunctie `datasetLookup` binnen expressiefragmenten voor een beperkte set klanten worden gebruikt. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

De `datasetLookup` helper wint gegevens van het verslagdatasets van Adobe Experience Platform tijdens verpersoonlijking terug zodat kunt u gebiedswaarden gebruiken die niet op het profiel of in de gebeurtenislading worden opgeslagen.

**Syntaxis**

```sql
{{datasetLookup datasetId="datasetId" id="key" result="store" required=false}}
```

Verwijzing opgehaalde velden met `{{result.fieldId}}` , waarbij `result` de waarde is die u doorgeeft aan de parameter `result` .

Voor dataset enablement, parameterdetails, voorbeelden, en het testen, zie {de gegevens van Adobe Experience Platform van 0} Gebruik voor verpersoonlijking [.](../aep-data-perso.md)

## Metagegevens van uitvoering {#execution-metadata}

Met de `executionMetadata` -hulpfunctie kunt u op dynamische wijze aangepaste sleutel-waardeparen vastleggen en opslaan in de context van de berichtuitvoering.

**Syntaxis**

```
{{executionMetadata key="your_key" value="your_value"}}
```

In deze syntaxis verwijst `key` naar de naam van de metagegevens en is `value` de metagegevens die moeten worden voortgezet.

**Gebruiksscenario**

Met deze functie kunt u contextafhankelijke informatie toevoegen aan elke native actie van uw campagnes of reizen. Op deze manier kunt u contextgegevens voor levering in realtime naar externe systemen exporteren voor verschillende doeleinden, zoals reeksspatiëring, analyse, personalisatie en downstreamverwerking.

>[!NOTE]
>
>* De functie van Meta-gegevens van de Uitvoering wordt niet gesteund door [ douaneacties ](../../action/action.md).
>* De functie Metagegevens van de Uitvoering is niet zichtbaar wanneer de inhoud zelf wordt getoond.

U kunt bijvoorbeeld de functie Metagegevens uitvoeren gebruiken om een specifieke id toe te voegen aan elke levering die naar elk profiel wordt verzonden. Deze informatie wordt tijdens runtime gegenereerd en de verrijkte metagegevens voor uitvoering kunnen vervolgens worden geëxporteerd voor afstemming op een extern rapportageplatform.

**hoe het** werkt

Selecteer een element uit de inhoud van uw kanaal in een campagne of een rit en voeg, met de personalisatie-editor, de `executionMetadata` -hulplijn toe aan dit element.


Tijdens runtime wordt de metagegevenswaarde toegevoegd aan de bestaande **[!UICONTROL Message Feedback Event Dataset]** met het volgende schema:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!NOTE]
>
>Leer meer op datasets in [ deze sectie ](../../data/get-started-datasets.md).

**Beperkingen**

Er is een bovengrens van 2kb op de belangrijkste waardeparen per actie. Als de limiet van 2 kB wordt overschreden, wordt het bericht nog steeds geleverd, maar een van de sleutelwaardeparen kan worden afgekapt.

Metagegevens worden niet vastgelegd voor profielen die zijn uitgesloten van de handeling. Wanneer een profiel van het ontvangen van een bericht wordt uitgesloten, wordt geen meta-gegevensingang gecreeerd voor dat profiel in de dataset.

**Voorbeeld**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

In dit voorbeeld, uitgaande van `profile.person.name.firstName` = &quot;Alex&quot;, is de resulterende entiteit:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

## Coderen {#url-parameter-encryption-helper}

>[!AVAILABILITY]
>
>Deze functie is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.
>
>Deze mogelijkheid is momenteel alleen beschikbaar voor het e-mailkanaal.

Met de functie `Encrypt` kunt u elke expressiewaarde tijdens het renderen coderen (doorgaans een profielkenmerk, een token of zelfs een stringified JSON-structuur die u in de expressie maakt) voordat deze in een queryparameter wordt geschreven voor het bijhouden van koppelingen of het landen van pagina&#39;s.

Waarden die als normale tekst in de URL worden weergegeven (inclusief PII of andere vertrouwelijke gegevens), zijn niet leesbaar wanneer de koppeling wordt gecontroleerd of doorgestuurd. Alleen de waarden die u met deze hulplijn omsluit, worden gecodeerd. De rest van de URL blijft ongewijzigd.

**Gebruiksscenario**

Met deze hulp kunt u gevoelige profielgegevens (PII) beschermen voordat u deze opneemt in gerenderde uitvoer.

**Vereiste**

Een beheerder moet ten minste één actieve sleutel maken in het sleutelregister op sandboxniveau. [ leer hoe te om sleutels tot stand te brengen en te beheren ](../url-parameter-encryption.md#create-keys)

>[!NOTE]
>
>Het gebruiken van een ingetrokken of anders niet-actieve sleutel zou de verpersoonlijking moeten veroorzaken om bij teruggeven tijd te ontbreken zodat wordt een bericht niet verzonden met een ongeldige sleutel.

**Syntaxis**

```text
{{encrypt dataPath keyName="keyName" version="version" result="variableName"}}
```

**Gebruik**

Deze hulp codeert gevoelige gegevens en slaat het resultaat in een malplaatjevariabele op. <!--The encryption is performed using the AES-256-GCM algorithm.-->

U kunt de hulp op één parameter, verscheidene, of alle parameters in een verbinding, afhankelijk van uw ontwerp URL en lengtebeperkingen toepassen.

* **Input**: `dataPath` (gegevensverwijzing die aan een koord moet oplossen), `keyName` (encryptie zeer belangrijke herkenningsteken), `version` (facultatieve zeer belangrijke versie), `result` (veranderlijke naam voor gecodeerde output)
* **Output**: maakt de gecodeerde waarde beschikbaar in de gespecificeerde `result` variabele.
* **formaat van het Resultaat**: De resultaatvariabele bevat een punt-gescheiden koord: `keyName.version.nonce.authTag.cipherText` (alle segmenten behalve `keyName` en `version` zijn URL-veilige Base64 die zonder het opvullen wordt gecodeerd).
* **Statische zeer belangrijke vereisten**: `keyName` en `version` moeten statische koordliterals (de dynamische verwijzingen worden niet gesteund) zijn.
* **Standaardversie**: De `version` parameter is facultatief; als weggelaten, lost de encryptiesleuteldienst de standaardversie op

**Voorbeelden**

| Voorbeeldexpressie | Resultaat |
| --- | --- |
| `{{encrypt profile.person.email keyName="email-key" version="1" result="enc"}}{{enc}}` | `email-key.1.RkFrZU5vbmNlQUJD.T3V0cHV0QXV0aFRhZ0Fh.am9obkBleGFtcGxlLmNvbQ` |
| `{{encrypt profile.person.name.firstName keyName="pii-key" version="2" result="encName"}}{{encName}}` | `pii-key.2.U29tZVJhbmRvbUlW.QXV0aGVudGljYXRpb25UYQ.Sm9obg` |

**Guardrails**

* Decryptie wordt buiten [!DNL Journey Optimizer] afgehandeld op de bestemmingspagina&#39;s, apps of API&#39;s. De belangrijkste levenscyclus en omwenteling van het plan met uw veiligheidsteam zodat kunnen de historische ladingen nog worden gedecrypteerd waar nodig.

* Ingetrokken sleutels mogen niet worden gebruikt voor nieuwe versleuteling. Volg uw beveiligingsbeleid voor roteren en uit bedrijf nemen.

* Het coderingsproces dat bronintensief is, waarbij de functie `Encrypt` wordt gebruikt, kan van invloed zijn op de doorvoer tijdens de rendertijd.
