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
exl-id: 9864a136-e129-4279-bb09-081b72f584df
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Live-activiteiten maken {#create-mobile-live}

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

   >[!NOTE]
   >
   >Voor **API-teweeggebrachte marketing** campagnes, kunt u een bestaand publiek selecteren dat als eerste segmentatie alvorens het abonnement van APNs channelID van de API nuttige lading te controleren dienst doet.

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe te om **[!UICONTROL Schedule]** van uw campagne in [ te vormen deze sectie ](../campaigns/create-campaign.md#schedule).

1. Klik na configuratie op **[!UICONTROL Review to activate]** en klik vervolgens op **[!UICONTROL Activate]** .

1. Nadat de campagne wordt geactiveerd, gebruik het verstrekte **cURL- verzoek** als malplaatje om het Levende begin van de Activiteit, update, of eindgebeurtenissen teweeg te brengen. Werk de voorbeeldlading vóór uitvoering bij met uw specifieke gegevens.

   Zorg ervoor dat u ook de **[!UICONTROL Campaign ID]** -id&#39;s kopieert en in de lading opneemt.

   ➡️ Verwijs naar de [ API Verplaatste Documentatie van Campagnes ](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) voor authentificatievereisten, met inbegrip van tokens OAuth en API sleutels.

   ![](assets/create-live-3.png)

   +++ Voorbeeld van een Payload for Unitary use cases (door de API geïnitieerde Transactionele campagne)

   Dit nuttige ladingsvoorbeeld is voor individuele campagnes gebruikend **API-teweeggebrachte Transactionele** campagneretype. De meeste velden in het volgende voorbeeld zijn verplicht, alleen `requestId` , `dismissal-date` en `alert` zijn optioneel.

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

   +++ Voorbeeld van een Payload for Broadcast-gebruiksscenario (API-geactiveerde marketingcampagne)

   Dit payload voorbeeld is voor op publiek-gebaseerde campagnes gebruikend **API-teweeggebrachte marketing** campagneretype.

   ```json
   {
       "requestId": "123400000",
       "campaignId": "d32e6f6c-56df-4a98-a2c0-6db6008f8f32",
       "audience": {
           "id": "508f9416-52d0-4898-ba47-08baaa22e9c7"
       },
       "context": {
           "requestPayload": {
               "aps": {
                   "input-push-channel": "V+8UslywEfAAAOq9SbTrLg==",  //apns-channel-id
                   "content-available": 1,
                   "timestamp": 1770808339,
                   "event": "update",   // start | update | end
   
                   // Fields from GameScoreLiveActivityAttributes
                   "content-state": {
                       "homeTeamScore": 33,
                       "awayTeamScore": 49,
                       "statusText": "Wingdom keeps scoring!"
                   },
                   "attributes-type": "GameScoreLiveActivityAttributes",
                   "attributes": {
                       "liveActivityData": {
                           "channelID": "V+8UslywEfAAAOq9SbTrLg=="   //apns-channel-id, must match the "input-push-channel" value
                       }
                   },
                   "alert": {
                       "title": "This is the title for game",
                       "body": "This is the body for body"
                   }
               }
           }
       }
   }
   ```

   +++

Na het ontwerpen van uw Levende activiteit, kunt u het meten van het effect van uw Levende activiteit met [ ingebouwde rapporten ](../reports/campaign-global-report-cja-activity.md) volgen.

## Hoe kan ik-video

Ontdek hoe u iOS Live-activiteiten kunt configureren met Adobe Journey Optimizer om geavanceerde realtime updates te leveren op het iPhone Lock Screen en Dynamic Island.

>[!VIDEO](https://video.tv.adobe.com/v/3479864)
