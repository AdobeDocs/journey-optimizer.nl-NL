---
solution: Journey Optimizer
product: journey optimizer
title: Een aangepaste handeling configureren
description: Leer hoe u een aangepaste handeling configureert
feature: Actions
topic: Administration
role: Admin
level: Experienced
badge: label="Beta" type="Informative"
keywords: handeling, extern, aangepast, reizen, API
hide: true
hidefromtoc: true
source-git-commit: a3c95497fb7304ddd0aa26435f5d0279ff8fdb0f
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 4%

---

# Verbeteringen voor aangepaste acties

U kunt nu API vraagreacties in douaneacties gebruiken en uw reizen ordenen die op deze reacties worden gebaseerd.

Deze mogelijkheid was alleen beschikbaar bij het gebruik van gegevensbronnen. U kunt deze nu gebruiken met aangepaste handelingen.

>[!AVAILABILITY]
>
>Deze functie is momenteel beschikbaar als een persoonlijke bètaversie.

>[!WARNING]
>
>Aangepaste acties mogen alleen worden gebruikt met persoonlijke of interne eindpunten en moeten worden gebruikt met een passende limiet voor afdekkingen of vertragen. Zie [deze pagina](../configuration/external-systems.md).

## De aangepaste handeling definiëren

Bij het definiëren van de aangepaste actie zijn twee verbeteringen beschikbaar gesteld: de toevoeging van de methode GET en het nieuwe veld voor de laadreactie. De andere opties en parameters blijven ongewijzigd. Zie [deze pagina](../action/about-custom-action-configuration.md).

### Eindpuntconfiguratie

De **URL-configuratie** de naam van de sectie is gewijzigd **Eindpuntconfiguratie**.

In de **Methode** vervolgkeuzelijst, kunt u nu selecteren **GET**.

![](assets/action-response1.png){width="70%" align="left"}

### Payloads

De **Handelingsparameters** de naam van de sectie is gewijzigd **Payloads**. Er zijn twee velden beschikbaar:

* De **Verzoek** veld: dit veld is alleen beschikbaar voor aanroepmethoden van POSTEN en PUTTEN.
* De **Antwoord** veld : dit is de nieuwe mogelijkheid . Dit gebied zoals beschikbaar voor alle roepende methodes.

>[!NOTE]
> 
>Beide velden zijn optioneel.

![](assets/action-response2.png){width="70%" align="left"}

1. Klik in het dialoogvenster **Antwoord** veld.

   ![](assets/action-response3.png){width="80%" align="left"}

1. Plak een voorbeeld van de lading die door de vraag is teruggekeerd. Controleer of de veldtypen correct zijn (tekenreeks, geheel getal, enz.). Hier is een voorbeeld van antwoordlading die tijdens de vraag wordt gevangen. Ons lokale eindpunt verzendt het aantal loyaliteitspunten en de status van een profiel.

   ```
   {
   "customerID" : "xY12hye",    
   "status":"gold",
   "points": 1290 }
   ```

   ![](assets/action-response4.png){width="80%" align="left"}

   Telkens wanneer de API wordt aangeroepen, haalt het systeem alle velden op die in het payloadvoorbeeld zijn opgenomen.

1. Laten wij ook CustomerID als vraagparameter toevoegen.

   ![](assets/action-response9.png){width="80%" align="left"}

1. Klikken **Opslaan**.

## De respons in een reis benutten

Voeg gewoon de aangepaste handeling toe aan een reis. U kunt de ladingsgebieden van de reactie in voorwaarden, andere acties en berichtverpersoonlijking dan gebruiken.

U kunt bijvoorbeeld een voorwaarde toevoegen om het aantal loyaliteitspunten te controleren. Wanneer de persoon het restaurant ingaat, verzendt uw lokale eindpunt een vraag met de loyaliteitsinformatie van het profiel. U kunt een push verzenden als het profiel een gouden klant is. En als een fout in de vraag wordt ontdekt, verzend een douaneactie om uw systeembeheerder op de hoogte te brengen.

![](assets/action-response5.png)

1. Voeg uw gebeurtenis en de aangepaste handeling Loyalty toe die u eerder hebt gemaakt.

1. Wijs in de aangepaste actie Loyalty de queryparameter voor de klant-id toe aan de profiel-id. Schakel de optie in **Een alternatief pad toevoegen bij een time-out of fout**.

   ![](assets/action-response10.png)

1. Voeg in de eerste vertakking een voorwaarde toe en gebruik de geavanceerde editor om de velden voor actierespons te benutten, onder **Context** knooppunt.

   ![](assets/action-response6.png)

1. Voeg vervolgens uw pushbericht toe en pas uw bericht aan met de responsvelden. In ons voorbeeld, personaliseren wij de inhoud gebruikend het aantal loyaliteitspunten en de klantenstatus. De velden voor actierespons zijn beschikbaar onder **Contextafhankelijke kenmerken** > **Journey Orchestration** > **Handelingen**.

   ![](assets/action-response8.png)

   >[!NOTE]
   >
   >Elk profiel dat de douaneactie ingaat zal een vraag teweegbrengen. Zelfs als de reactie altijd het zelfde is, zal de Reizen nog één vraag per profiel uitvoeren.

1. Voeg in de vertakking Time-out en Fout een voorwaarde toe en gebruik de ingebouwde **jo_status_code** veld. In ons voorbeeld gebruiken we de
   **http_400** fouttype. Zie [deze sectie](#error-status).

   ```
   @action{ActionLoyalty.jo_status_code} == "http_400"
   ```

   ![](assets/action-response7.png)

1. Voeg een aangepaste actie toe die naar uw organisatie wordt verzonden.

   ![](assets/action-response11.png)

## Foutstatus{#error-status}

De **jo_status_code** veld is altijd beschikbaar, zelfs als er geen antwoordlading is gedefinieerd.

Hier volgen de mogelijke waarden voor dit veld:

* http status code: http_`<HTTP API call returned code>`, bijvoorbeeld http_200 of http_400
* time-outfout: **timedout**
* Fout bij toewijzen: **afgetopt**
* interne fout: **internalError**

Een actieaanroep wordt als fout beschouwd wanneer de geretourneerde http-code groter is dan 2xx of wanneer een fout optreedt. De reis stroomt naar de specifieke onderbreking of foutentak in dergelijke gevallen.

>[!WARNING]
>
>Alleen nieuw gemaakte aangepaste acties bevatten de **jo_status_code** veld uit de doos. Als u deze wilt gebruiken met een bestaande aangepaste handeling, moet u de handeling bijwerken. U kunt bijvoorbeeld de beschrijving bijwerken en opslaan.

## Expressiesyntaxis

Hier volgt de syntaxis:

```json
#@action{myAction.myField} 
```

Hier volgen enkele voorbeelden:

```json
 // action response field
 @action{<action name>.<path to the field>}
 @action{ActionLoyalty.status}
```

```json
 // action response field
 @action{<action name>.<path to the field>, defaultValue: <default value expression>}
 @action{ActionLoyalty.points, defaultValue: 0}
 @action{ActionLoyalty.points, defaultValue: @{myEvent.newPoints}}
```

Zie voor meer informatie over veldverwijzingen [deze sectie](../building-journeys/expression/field-references.md).
