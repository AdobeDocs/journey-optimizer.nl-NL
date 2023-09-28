---
solution: Journey Optimizer
product: journey optimizer
title: Verbeteringen voor aangepaste acties
description: Meer informatie over de nieuwste verbeteringen voor aangepaste acties
feature: Actions
topic: Administration
role: Admin
level: Experienced
badge: label="Beta" type="Informative"
keywords: handeling, extern, aangepast, reizen, API
exl-id: 8f47b605-7179-4522-b50c-0ea34b09bd22
source-git-commit: 2e06ca80a74c6f8a16ff379ee554d57a69ceeffd
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 4%

---

# API-aanroepreacties gebruiken in aangepaste handelingen {#custom-action-enhancements}

U kunt API vraagreacties in douaneacties gebruiken en uw reizen organiseren die op deze reacties worden gebaseerd.

>[!AVAILABILITY]
>
>Deze functie is momenteel beschikbaar in bèta.

<!--
You can now leverage API call responses in custom actions and orchestrate your journeys based on these responses.

This capability was previously only available when using data sources. You can now use it with custom actions. 
-->

## Belangrijke opmerkingen{#custom-action-enhancements-notes}

<!--
* Custom actions should only be used with private or internal endpoints, and used with an appropriate capping or throttling limit. See [this page](../configuration/external-systems.md). 
-->

* Scalaire arrays worden ondersteund bij een payload als reactie:

  ```
  "dummyScalarArray": [
  "val1",
  "val2"
  ]
  ```

* Heterogene arrays worden niet ondersteund bij een payload als reactie:

  ```
  "dummyRandomArray": [
  20,
  "aafw",
  false
  ]
  ```

<!--
## Best practices{#custom-action-enhancements-best-practices}

A capping limit of 5000 calls/s is defined for all custom actions. This limit has been set based on customers usage, to protect external endpoints targeted by custom actions. You need to take this into account in your audience-based journeys by defining an appropriate reading rate (5000 profiles/s when custom actions are used). If needed, you can override this setting by defining a greater capping or throttling limit through our Capping/Throttling APIs. See [this page](../configuration/external-systems.md).

You should not target public endpoints with custom actions for various reasons:

* Without proper capping or throttling, there is a risk of sending too many calls to a public endpoint that may not support such volume.
* Profile data can be sent through custom actions, so targeting a public endpoint could lead to inadvertently sharing personal information externally.
* You have no control on the data being returned by public endpoints. If an endpoint changes its API or starts sending incorrect information, those will be made available in communications sent, with potential negative impacts.
-->

<!--
## Define the custom action {#define-custom-action}

When defining the custom action, two enhancements have been made available: the addition of the GET method and the new payload response field. The other options and parameters are unchanged. See [this page](../action/about-custom-action-configuration.md).

### Endpoint configuration {#endpoint-configuration}

The **URL configuration** section has been renamed **Endpoint configuration**.

In the **Method** drop-down, you can now select **GET**.

![](assets/action-response1.png){width="70%" align="left"}

### Payloads {#payloads-new}

The **Action parameters** section has been renamed **Payloads**. Two fields are available:

* The **Request** field: this field is only available for POST and PUT calling methods.
* The **Response** field: this is the new capability. This field as available for all calling methods.

>[!NOTE]
> 
>Both these fields are optional.

![](assets/action-response2.png){width="70%" align="left"}
-->

## Aangepaste actie configureren {#config-response}

1. Maak de aangepaste handeling. Zie [deze pagina](../action/about-custom-action-configuration.md).

1. Klik in het dialoogvenster **Antwoord** veld.

   ![](assets/action-response2.png){width="80%" align="left"}

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

## De respons in een reis benutten {#response-in-journey}

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

## Logboeken van testmodi {#test-mode-logs}

Via de testmodus hebt u toegang tot statuslogboeken die gerelateerd zijn aan aangepaste actieantwoorden. Als u aangepaste acties hebt gedefinieerd met reacties op uw reis, ziet u een **actionsHistory** sectie op die logboeken die de nuttige lading tonen door het externe eindpunt (als reactie van die douaneactie) is teruggekeerd. Dit kan zeer nuttig in termen van het zuiveren zijn.

![](assets/action-response12.png)

## Foutstatus {#error-status}

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

## Expressiesyntaxis {#exp-syntax}

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
