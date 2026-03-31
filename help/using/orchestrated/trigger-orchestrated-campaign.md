---
solution: Journey Optimizer
product: journey optimizer
title: Een geordende campagne activeren met behulp van een signaal
description: Leer hoe te om een Geordende campagne teweeg te brengen gebruikend een signaal in  [!DNL Adobe Journey Optimizer].
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
exl-id: d1fd072d-b143-4752-822f-23f98684ba80
source-git-commit: ec52b62c2d0626b9047eebb54e0a44fee096ec05
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# Trigger Orchestrated campagnes gebruikend een signaal {#trigger-signal}

U kunt een Geordende campagne teweegbrengen door het een signaal te verzenden in plaats van het op een programma in werking te stellen. Het signaal wordt verzonden via een API-aanroep van een extern systeem of externe toepassing. Wanneer u een signaal gebruikt, kunt u parameters doorgeven. Ze worden vervolgens in de georkestreerde campagne beschikbaar gesteld als gebeurtenisvariabelen in de uitvoeringscontext — voor gebruik bij het opgeven van doelen, voorwaarden of expressies.

Het proces van begin tot eind om een Geordende campagne teweeg te brengen gebruikend een signaal:

1. [Plan de campagne die door een signaal moet worden teweeggebracht](#set-an-orchestrated-campaign-to-wait-for-a-signal-configure-signal)
1. [ voegt parameters voor de signaallading ](#add-parameters-for-the-signal-payload-optional-parameters) (facultatief) toe
1. [De campagne bouwen en testen](#build-and-test-the-campaign-build-and-test)
1. [De campagne publiceren en activeren](#publish-and-trigger-the-campaign-publish)

>[!NOTE]
>
>Als u een geordende campagne wilt activeren via een signaal, hebt u de machtiging **[!DNL Publish orchestrated campaigns]** (`orchestrated-campaign.publish` ) nodig. Zie [ ingebouwde toestemmingen ](../administration/ootb-permissions.md).

## Plan de campagne die door een signaal moet worden teweeggebracht {#configure-signal}

Voer de volgende stappen uit om een georkestreerde campagne in te stellen om te beginnen met een signaal in plaats van een schema:

1. Open de geordende campagne die u wilt activeren door een signaal te gebruiken.

1. Open de planningsconfiguratie. [ Leer hoe te om een Geordende campagne ](create-orchestrated-campaign.md#schedule) te plannen.

1. Selecteer **[!UICONTROL Triggered by a signal]** zodat de campagne op een signaal wacht in plaats van op een schema.

   ![ menu van het Programma met teweeggebracht door een geselecteerde signaaloptie ](assets/triggered-oc-scheduler.png){zoomable="yes"}

## Parameters toevoegen voor de signaallading (optioneel) {#parameters}

U kunt parameters in het trekkersignaal overgaan en hen in uw campagne in de uitvoeringscontext-voor voorbeeld, in het richten, voorwaarden, of uitdrukkingen gebruiken. Definieer eerst elke parameter in de planningsinstellingen en geef vervolgens de waarde ervan door wanneer u de trigger-API aanroept.

1. Open de campagneplanner en selecteer **[!UICONTROL Add parameter]**.

1. Bepaal de naam en het gegevenstype van elke parameter om in de signaallading te verzenden. U kunt **waarden van de Test** ook verstrekken die zullen worden gebruikt wanneer u de campagne op testwijze teweegbrengt. [ Leer hoe te om een teweeggebrachte campagne ](#build-and-test) te testen.

   ![ voegt parameter toe om ladingsparameters voor het signaal te bepalen ](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>Als u een parameter in de API vraag overgaat die niet in de planner is bepaald, slaagt de API vraag nog en de parameter wordt verspreid, en u kunt het in uitdrukkingen gebruiken. Nochtans, zal de geordende campagneinterface u niet helpen het-voor voorbeeld gebruiken, zal de activiteit van de Test niet van parameters een lijst maken of tonen die niet in de planner werden bepaald.

## De campagne bouwen en testen {#build-and-test}

Bouw uw campagne op het canvas, dan test naar keuze het in ontwerp door het signaal via API in werking te stellen alvorens u publiceert.

1. Voeg activiteiten (publiek, gericht, leveranties) op het canvas toe en verbind. [ Leer hoe te om campagneactiviteiten te ordenen ](orchestrate-activities.md)

1. Als u parameters in het signaal hebt bepaald, kunt u hen in uw canvaslogica (bijvoorbeeld, in voorwaarden of het richten) telegraferen. In dit voorbeeld wordt de parameter &quot;channel&quot; gebruikt als een voorwaarde in een **[!UICONTROL Test]** -activiteit.

   {de parameter van het 0} Kanaal die als voorwaarde in de activiteit van de Test wordt gebruikt ![](assets/triggered-oc-use-parameters.png)

   Als u een signaalparameter in de expressieeditor wilt gebruiken (bijvoorbeeld om een query te maken in een **[!UICONTROL Build audience]** -activiteit), typt u `$(vars/@<parameterName>)` in het expressieveld. Vervang `<parameterName>` door de parameternaam die in de planner is gedefinieerd, bijvoorbeeld `$(vars/@channel)` . [ Leer hoe te met de uitdrukkingsredacteur ](edit-expressions.md) te werken.

1. Open de campagneplanner, selecteer **[!UICONTROL Copy API request]** en kies het formaat (cURL of HTTP- Verzoek).

   De gekopieerde informatie bevat onder andere de geordende campagne-id, de naam van de sandbox, de organisatie-id en testwaarden voor de parameters als u er enkele hebt toegevoegd.

   ![ de verzoekoptie van het Exemplaar API in planningsconfiguratie ](assets/triggered-oc-copy.png)

   +++Voorbeeld van een cURL-aanvraag met een parameter en een testwaarde

   ```bash
   POST https://platform.adobe.io/ajo/campaign-orchestration/orchestratedCampaigns/1c7529c7-7a8c-491a-a2c6-3d8131d2e17d/trigger
   
   Headers:
   Authorization: Bearer ## Access token ##
   Content-Type: application/json
   x-api-key: ## Provide API Key here ##
   x-api-version: 1
   x-gw-ims-org-id: 123456ABCDEFG@LumaOrg
   x-sandbox-name: prod
   
   Body:
   {
   "variables": {
      "channel": "sms"
   }
   }
   ```

   +++

1. Klik op **[!UICONTROL Start]** om de campagne te starten.

1. Verzend de trekkerAPI vraag gebruikend het steekproefverzoek u van de planner hebt gekopieerd. <!--For the complete API reference, refer to the [Journey Optimizer API documentation](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.-->

Wanneer u met de testresultaten wordt tevredengesteld, [ publiceer de campagne ](#publish).

## De campagne publiceren en activeren {#publish}

Nadat u [ hebt gebouwd en de campagne ](#build-and-test) getest, publiceer de campagne zodat kan het van uw toepassing worden teweeggebracht.

1. Klik op **[!UICONTROL Publish]** in het campagnecanvas. De campagne moet worden gepubliceerd voordat deze vanuit een extern systeem kan worden geactiveerd. [ Leer meer bij het beginnen en het controleren van de campagne ](start-monitor-campaigns.md#publish).

1. Open de campagneplanner, selecteer **[!UICONTROL Copy API request]** en kies het formaat (cURL of HTTP- Verzoek).

   De gekopieerde informatie bevat onder andere de geordende campagne-id, de naam van de sandbox, de organisatie-id en parameters als u er een hebt toegevoegd.

   ![ het verzoek van het Exemplaar API in planningsconfiguratie ](assets/triggered-oc-copy.png)

1. Roep de trigger-API van uw systeem aan.

   >[!IMPORTANT]
   >
   >Voor een levende georkestreerde campagne, dwingt een throttle guardrail a **minimuminterval van één uur** tussen twee API triggeruitvoeringen af. Als u opnieuw API roept alvorens dat interval is verstreken, keert API **HTTP 429** fout (Te veel verzoeken) terug. Deze hulplijn wordt niet toegepast wanneer u een conceptversie activeert om deze te testen.

   Als u parameters aan de signaallading toevoegde, worden de waarden u in de API vraag overgaat blootgesteld als variabelen van de campagnegebeurtenis wanneer de campagne loopt. Als u ze wilt inspecteren, opent u de logboeken van de campagne op de werkbalk van het campagnecanvas. Geef op het tabblad **[!UICONTROL Tasks]** de taak op die overeenkomt met het signaal en klik op het potloodpictogram om de gerelateerde gebeurtenisvariabelen te openen. [ leer hoe te om tot logboeken en taken ](start-monitor-campaigns.md#logs-tasks) toegang te hebben.

   ![ Logboeken en taakscherm waar de variabelen van de campagnegebeurtenis beschikbaar zijn ](assets/trigger-events-variables.png){zoomable="yes"}
