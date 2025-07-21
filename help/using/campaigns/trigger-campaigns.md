---
solution: Journey Optimizer
product: journey optimizer
title: Een campagne bekijken en activeren
description: Meer informatie over het reviseren en activeren van campagnes in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campagne, revisie, validatie, activering, activering, optimaliseren
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# Een door API geactiveerde campagne uitvoeren {#execute}

Nadat de campagne is geactiveerd, moet u het gegenereerde voorbeeld-cURL-verzoek ophalen en deze in de API gebruiken om de payload te bouwen en de campagne te starten.

1. Open de campagne en kopieer en plak vervolgens het laadverzoek vanuit de sectie **[!UICONTROL cURL request]** . Deze nuttige lading omvat alle verpersoonlijkings (profiel en context) variabelen die in het bericht worden gebruikt. Het is beschikbaar zodra de campagne live is.

   ![](assets/api-triggered-curl.png)

1. Gebruik dit cURL-verzoek in de API&#39;s om de payload te bouwen en de campagne te starten. Voor meer informatie, verwijs naar de [ Interactieve documentatie van API van de Uitvoering van het Bericht ](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).


   API vraagvoorbeelden zijn ook beschikbaar op [ deze pagina ](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

   >[!NOTE]
   >
   >Als u een specifieke begin en/of einddatum toen het creëren van de campagne hebt gevormd, zal het niet buiten deze data worden uitgevoerd, en API vraag zal ontbreken.
