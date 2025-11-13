---
solution: Journey Optimizer
product: journey optimizer
title: Een bericht voor live-activiteiten maken
description: Leer hoe u een Live-activiteit maakt in Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: bfd36dddb5795cd8b6eeb164f70b6cf3fdcb5750
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 1%

---

# Live-activiteiten maken {#create-mobile-live}

>[!BEGINSHADEBOX]

* [Aan de slag met Live-activiteiten](get-started-mobile-live.md)
* [Live activity-configuratie](mobile-live-configuration.md)
* [Integratie van live-activiteiten met Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)
* **[creeer een Levende activiteit](create-mobile-live.md)**
* [Veelgestelde vragen](mobile-live-faq.md)
* [Rapport voor live-activiteitencampagne](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

Nadat u uw mobiele configuratie hebt geconfigureerd en uw mobiele Adobe Experience Platform SDK hebt geïmplementeerd, kunt u uw Live-activiteiten starten in Journey Optimizer:

1. Open het menu **[!UICONTROL Campaigns]** en klik op **[!UICONTROL Create campaign]** .

1. Selecteer het **API teweeggebrachte** campagnetype.

   * Selecteer **API-teweeggebrachte Marketing** voor op publiek-gebaseerde campagnes

   * Selecteer **API-teweeggebrachte Transactie** voor individuele campagnes.

   >[!IMPORTANT]
   >
   > Merk op dat voor **API-teweeggebrachte Transactionele**, **[!UICONTROL High Throughput]** optie niet zou moeten worden toegelaten.

   ![](assets/create-live-1.png)

1. Bewerk in de sectie **[!UICONTROL Properties]** de items **[!UICONTROL Title]** en **[!UICONTROL Description]** van uw campagne.

1. Kies **[!UICONTROL Actions]** in de sectie **[!UICONTROL Live activity]** en selecteer of maak een nieuwe configuratie.

   Leer meer over Levende activiteitenconfiguratie op [ deze pagina ](mobile-live-configuration.md).

   ![](assets/create-live-2.png)

1. Klik op **[!UICONTROL Create experiment]** om uw inhoudexperiment te configureren en behandelingen te maken om de prestaties te meten en de beste optie voor uw doelgroep te identificeren. [Meer informatie](../content-management/content-experiment.md)

1. Van het **[!UICONTROL Audience]** lusje, kies uw **[!UICONTROL Identity type]** [ Leer meer ](../audience/about-audiences.md).

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe te om **[!UICONTROL Schedule]** van uw campagne in [ te vormen deze sectie ](../campaigns/create-campaign.md#schedule).

1. Klik na configuratie op **[!UICONTROL Review to activate]** en klik vervolgens op **[!UICONTROL Activate]** .

1. Nadat de campagne wordt geactiveerd, gebruik het verstrekte **cURL- verzoek** als malplaatje om het Levende begin van de Activiteit, update, of eindgebeurtenissen teweeg te brengen. Werk de voorbeeldlading vóór uitvoering bij met uw specifieke gegevens.

   Zorg ervoor dat u ook de **[!UICONTROL Campaign ID]** -id&#39;s kopieert en in de lading opneemt.

   ➡️ Verwijs naar de [ API Verplaatste Documentatie van Campagnes ](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) voor authentificatievereisten, met inbegrip van tokens OAuth en API sleutels.

   ![](assets/create-live-3.png)

   +++ Voorbeeld van een individuele lading

   De meeste velden in het volgende voorbeeld zijn verplicht, alleen `requestId` , `dismissal-date` en `alert` zijn optioneel.

   ```json
   {
       "requestId": "your-request-id",
       "campaignId": "your-campaign-id",
       "recipients": [
   {
       "type": "aep",
       "userId": "testemail@gmail.com",
       "namespace": "email",
       "context": {
        "requestPayload": {
       "aps": {
       "content-available": 1,
       "timestamp": 1756984054,              // current epoch time
       "dismissal-date": 1756984084,         // optional – auto remove when event="end"
       "event": "update",                    // start | update | end
   
       // Fields from FoodDeliveryLiveActivityAttributes
       "content-state": {
         "orderStatus": "Delivered"
       },
   
       "attributes-type": "FoodDeliveryLiveActivityAttributes",
       "attributes": {
         "restaurantName": "Pizza",
         "liveActivityData": {
           "liveActivityID": "orderId1"       // customer reference ID
         }
       },
   
       "alert": {
         "title": "Order Delivered!",
         "body": "Your pizza has arrived."
       }
     }
   }
   }
   }
   ]
   }
   ```

   +++

Na het ontwerpen van uw Levende activiteit, kunt u het meten van het effect van uw Levende activiteit met [ ingebouwde rapporten ](../reports/campaign-global-report-cja-activity.md) volgen.
