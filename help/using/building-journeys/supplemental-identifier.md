---
title: Aanvullende identificatiecode bij door gebeurtenissen veroorzaakte reizen
description: Leer hoe u een aanvullende id kunt gebruiken tijdens een door een gebeurtenis geïnitieerde reis.
badge: label="Beperkte beschikbaarheid" type="Informative"
exl-id: f6ebd706-4402-448a-a538-e9a4c2cf0f8b
source-git-commit: 14a0054c605edd8ff0b63e71fb5c30104ff513ed
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 0%

---

# Aanvullende identificatiecode bij door gebeurtenissen veroorzaakte reizen {#supplemental-id}

>[!CONTEXTUALHELP]
>id="ajo_journey_parameters_supplemental_identifier"
>title="Aanvullende id gebruiken"
>abstract="De aanvullende identificatiecode is een secundaire identificatiecode die aanvullende context biedt voor de uitvoering van een reis. Als u deze wilt definiëren, selecteert u het veld dat u wilt gebruiken als de aanvullende id en kiest u een naamruimte die u hieraan wilt koppelen."

>[!AVAILABILITY]
>
>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

Door gebrek, gebeurtenis-teweeggebrachte reizen worden uitgevoerd in de context van a **profielidentiteitskaart**. Dit betekent dat, zolang het profiel actief is op een bepaalde reis, het niet in staat zal zijn om een andere reis opnieuw te betreden. Om dit te verhinderen, staat Journey Optimizer u toe om a **extra herkenningsteken** in uw gebeurtenissen, zoals een orde identiteitskaart, identiteitskaart van het abonnement, recept identiteitskaart, naast profielidentiteitskaart te vangen.
In dit voorbeeld hebben we een reserverings-id toegevoegd als een aanvullende id.

![](assets/event-supplemental-id.png){width=40% zoomable}

Hierdoor worden door de gebeurtenis geïnitieerde reizen uitgevoerd in de context van de profiel-id die aan de aanvullende id is gekoppeld (hier de boekings-id). Voor elke herhaling van de aanvullende identificator wordt één exemplaar van de reis uitgevoerd. Hierdoor zijn meerdere ingangen van dezelfde profiel-id mogelijk op reizen als ze verschillende boekingen hebben gemaakt.

Bovendien staat Journey Optimizer u toe om attributen van het supplementaire herkenningsteken (b.v. boekingsaantal, receptvernieuwingsdatum, producttype) voor berichtaanpassing te hefboomwerking, die hoogst relevante mededelingen verzekeren. <!--Example: A healthcare provider can send renewal reminders for each prescription in a patient's profile.-->

➡️ [Ontdek deze functie in video](#video)

## Afbeeldingen en beperkingen {#guardrails}

* **Gelijktijdige instantielimieten**: De profielen kunnen niet meer dan 10 gezamenlijke reisinstanties hebben.

<!--* **Array depth**: Supplemental identifier objects can have a maximum depth of 3 levels (2 levels of nesting).

    +++Example

    ```
    [
    (level 1) "Atorvastatin" : {
    "description" : "used to lower cholesterol",
    "renewal_date" : "11/20/25",
    "dosage" : "10mg"
    (level 2) "ingredients" : [
    (level 3) "Atorvastatin calcium",
    "lactose monohydrate",
    "microcrystalline cellulose",
    "other" ]
    }
    ]
    ```

    +++
-->
* **Criteria van de Uitgang**: De criteria van de uitgang, indien teweeggebracht, zouden alle instanties van het profiel levend in de reis op dat ogenblik weggaan. Dit is geen context voor de combinatie profiel-id + aanvullende id.

* **Regels van de Frequentie**: Elke reisinstantie die van het supplementaire gebruik van het herkenningsteken wordt gecreeerd tellen naar frequentie het afschilderen, zelfs als één enkele gebeurtenis in veelvoudige reisinstanties resulteert.

* **het type van Gegevens en schemastructuur**: Het supplementaire herkenningsteken moet van type zijn `string`. Dit kan een onafhankelijk tekenreekskenmerk zijn of een tekenreekskenmerk binnen een array van objecten. Het onafhankelijke tekenreekskenmerk resulteert in één enkele instantie van de rit, terwijl het tekenreekskenmerk binnen een array van objecten resulteert in een unieke instantie van de reis per herhaling van de objectarray. Tekenreeksarrays en -maps worden niet ondersteund.

* **Reisingang**

  Het gedrag van de terugkeer van de reis met supplementaire herkenningstekens volgt het bestaande terugkeerbeleid:

   * Als de reis niet-deelnemer is, kan dezelfde profiel-ID + combinatie van aanvullende id de reis niet opnieuw binnenkomen.
   * Als de reis met een tijdvenster is gecentreerd, kan de zelfde profiel ID + supplementaire combinatie van identiteitskaart na het bepaalde tijdvenster opnieuw ingaan.

## Voeg een aanvullende id toe en gebruik deze voor een reis {#add}

Voer de volgende stappen uit als u een aanvullende id wilt gebruiken voor een rit:

1. **teken de attributen als herkenningsteken in het gebeurtenisschema**

   1. Open het gebeurtenisschema en zoek het kenmerk dat u als aanvullende id wilt gebruiken (bijvoorbeeld de reserverings-id, de abonnement-id) en markeer het als een id. [ Leer hoe te met schema&#39;s ](../data/get-started-schemas.md) te werken

   1. Markeer de id als een **[!UICONTROL Identity]** .

      ![](assets/supplemental-ID-schema.png)

      >[!IMPORTANT]
      >
      >Zorg ervoor u niet de attributen als **Primaire identiteit** merkt.

   1. Selecteer de naamruimte die u aan de aanvullende id wilt koppelen. Dit moet een naamruimte voor niet-persoonlijke id zijn.

1. **voeg extra identiteitskaart aan de gebeurtenis toe**

   1. Maak of bewerk de gewenste gebeurtenis. [ Leer hoe te om een eenheidsgebeurtenis te vormen ](../event/about-creating.md)

   1. Controleer de optie **[!UICONTROL Use supplemental identifier]** in het scherm met gebeurtenisconfiguratie.

      ![](assets/supplemental-ID-event.png)

   1. Gebruik de uitdrukkingsredacteur om de attributen te selecteren u als supplementaire identiteitskaart merkte

      >[!NOTE]
      >
      >Gebruik de expressie-editor in **[!UICONTROL Advanced mode]** om het kenmerk te selecteren.

   1. Nadat u de aanvullende id hebt geselecteerd, wordt de bijbehorende naamruimte in het scherm voor gebeurtenisconfiguratie weergegeven als alleen-lezen.

1. **voeg de gebeurtenis aan de reis** toe

   Sleep de geconfigureerde gebeurtenis naar het reiscanvas. Het zal reizen op basis van zowel profiel-id als aanvullende id activeren.

   ![](assets/supplemental-ID-journey.png)

1. **de supplementaire attributen van identiteitskaart van de Leverage**

   Gebruik de uitdrukkingsredacteur en de verpersoonlijkingsredacteur om attributen van het supplementaire herkenningsteken voor verpersoonlijking of voorwaardelijke logica van verwijzingen te voorzien. Kenmerken zijn toegankelijk via het menu **[!UICONTROL Contextual attributes]** .

   ![](assets/supplemental-ID-perso.png)

   >[!NOTE]
   >
   >Als u met arrays werkt (bijvoorbeeld meerdere voorschriften of beleidsregels), gebruikt u een formule om specifieke elementen te extraheren.

+++ Zie voorbeelden

   In een objectarray met de aanvullende id als `bookingNum` en een kenmerk op hetzelfde niveau als `bookingCountry` , doorloopt de reis het arrayobject op basis van de bookingNum en wordt voor elk object een reisinstantie gemaakt.

   * De volgende expressie in de voorwaardenactiviteit doorloopt de objectarray en controleert of de waarde van `bookingCountry` gelijk is aan &quot;FR&quot;:

     ```
     @event{<event_name>.<object_path>.<object_array_name>.all(currentEventField.<attribute_path>.bookingNum==${supplementalId}).at(0).<attribute_path>.bookingCountry}=="FR"
     ```

   * De volgende expressie in de e-mailverpersoonlijkingseditor doorloopt de objectarray, haalt de `bookingCountry` uit die van toepassing is op de huidige instantie van de reis en geeft deze in de inhoud weer:

     ```
     {{#each context.journey.events.<event_ID>.<object_path>.<object_array_name> as |l|}} 
     
     {%#if l.<attribute_path>.bookingNum = context.journey.technicalProperties.supplementalId%} {{l.<attribute_path>.bookingCountry}}  {%/if%}
     
     {{/each}}
     ```

   * Voorbeeld van de gebeurtenis die wordt gebruikt om de reis te starten:

     ```
     "bookingList": [
           {
               "bookingInfo": {
                   "bookingNum": "x1",
                         "bookingCountry": "US"
               }
           },
           {
               "bookingInfo": {
                   "bookingNum": "x2",
                   "bookingCountry": "FR"
               }
           }
       ]
     ```

+++

1. **publiceer de reis**

   Zodra gevormd, publiceer de reis beginnen gebruikend veelvoudige gezamenlijke ingangen die op supplementaire herkenningstekens worden gebaseerd.

## Voorbeelden van gebruiksgevallen

### **Berichten van de Verlenging van het Beleid**

* **Scenario**: Een verzekeringsleverancier verzendt vernieuwingsherinneringen voor elk actief beleid dat door een klant wordt gehouden.
* **Uitvoering**:
   * Profiel: &quot;John&quot;.
   * Aanvullende id&#39;s: `"AutoPolicy123", "HomePolicy456"`.
   * De reis voert afzonderlijk voor elk beleid uit, met gepersonaliseerde vernieuwingsdata, dekkingsdetails, en premieinformatie.

### **Beheer van het Abonnement**

* **Scenario**: De abonnementendienst verzendt op maat gemaakte berichten voor elk abonnement wanneer een gebeurtenis voor dat abonnement wordt teweeggebracht.
* **Uitvoering**:
   * Profiel: &quot;Jane&quot;.
   * Aanvullende id&#39;s: `"Luma Yoga Program ", "Luma Fitness Program"`.
   * Elke gebeurtenis bevat een abonnement-id en gegevens over dat abonnement. De reis voert afzonderlijk voor elke gebeurtenis/abonnement uit, die gepersonaliseerde vernieuwingsaanbiedingen per abonnement toestaat.

### **Aanbevelingen van het Product**

* **Scenario**: Een e-handelsplatform verzendt aanbevelingen die op specifieke producten worden gebaseerd door een klant worden gekocht.
* **Uitvoering**:
   * Profiel: &quot;Alex&quot;.
   * Aanvullende id&#39;s: `"productID1234", "productID5678"`.
   * De reis voert afzonderlijk voor elk product uit, met gepersonaliseerde upsellingsmogelijkheden.

## Hoe kan ik-video {#video}

Leer hoe u een aanvullende id in [!DNL Adobe Journey Optimizer] kunt inschakelen en toepassen.

>[!VIDEO](https://video.tv.adobe.com/v/3464792?quality=12)
