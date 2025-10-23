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
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: d93b7ce225294257f49caee6ac08cfb575611a93
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# Een door API geactiveerde campagne uitvoeren {#execute}

Nadat de campagne is geactiveerd, moet u het gegenereerde voorbeeld-cURL-verzoek ophalen en deze in de API gebruiken om de payload te bouwen en de campagne te starten.

## Lees hier meer {#must-read}

* **begin/einddata van de Campagne** - als u een specifieke begin en/of einddatum toen het creëren van de campagne hebt gevormd, zal het niet buiten deze data worden uitgevoerd, en API vraag zal ontbreken.

* **onderbreking van de Vraag** - de vraag aan de Interactieve REST API van de Uitvoering van het Bericht heeft een onderbreking van 60 sec. In het geval van onverwachte onderbrekingen zijn er echter interne herpogingen beschikbaar om de levering te garanderen.

## De campagne activeren {#trigger}

1. Open de campagne en kopieer en plak vervolgens het laadverzoek vanuit de sectie **[!UICONTROL cURL request]** . Deze nuttige lading omvat alle verpersoonlijkings (profiel en context) variabelen die in het bericht worden gebruikt. Het is beschikbaar zodra de campagne live is.

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >De eindpunten in de cURL- sectie verschillen tussen standaard en [ Hoge productie campigns ](../campaigns/api-triggered-high-throughput.md).

1. Gebruik dit cURL-verzoek in de API&#39;s om de payload te bouwen en de campagne te starten. Voor meer informatie, verwijs naar de [ Interactieve documentatie van API van de Uitvoering van het Bericht ](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution), waar alle eindpunten voor standaard en Hoge productie campagnes worden vermeld.

   API vraagvoorbeelden zijn ook beschikbaar op [ deze pagina ](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).
