---
title: Gegevensverzameling
description: Meer informatie over het verzamelen van feedback over beslissingsbeheer
feature: Offers, Datasets
topic: Integrations
role: User
level: Intermediate
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---

# Verzameling van beslissingsbeheersgegevens {#data-collection}

## Gegevensverzameling

U kunt feedback van offer decisioning verzamelen in Adobe Experience Platform, inclusief welke aanbiedingen worden weergegeven en hoe gebruikers met hen communiceren. Deze gegevens kunnen worden gebruikt voor:
* Samenstellen [Beslissingsbeheerrapporten](../reports/get-started-events.md);
* Gebruiken [frequentiecalculatie](../offer-library/add-constraints.md#capping) regels;
* Gebouw [AI-modellen](../ranking/create-ranking-strategies.md) die als waarderingsmethode kunnen worden gebruikt.

## Typen gebeurtenissen

De manier waarop gegevens worden verzameld, varieert afhankelijk van het gebeurtenistype dat u wilt vastleggen.

### Gebeurtenissen van Besluit

Telkens wanneer het besluitvormingsbeheer een besluit neemt, wordt informatie over dat beslissingsfeit **automatisch** naar Adobe Experience Platform verzonden voor alle kanalen. [Meer informatie](../reports/get-started-events.md)

### Impressie en klik op gebeurtenissen

Afbeeldingen en klikken in het kader van besluitvormingsbeheer worden als volgt gedefinieerd:

* An **indruk** gebeurtenis is wanneer een aanbieding aan een gebruiker wordt getoond.

* A **klikken** gebeurtenis is wanneer een gebruiker klikt of met een aanbieding in wisselwerking staat.

Feedback op afbeeldingen en klikken wordt vastgelegd op basis van de [!DNL Journey Optimizer] kanaal dat wordt gebruikt.

**E-mails** gemaakt door [!DNL Journey Optimizer] **automatisch** impressies bijhouden en klikken.

Maar **meeste kanalen** impressies en klikgegevens vereisen die als een **Experience, gebeurtenis**. Dit omvat:

* Webpagina&#39;s die de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"} om aanbiedingen te renderen

* Mobiele toepassingen met de [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* Kiosks
* Berichten die via toepassingen van derden worden verzonden
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>Kanalen die een beslissing-API-aanvraag gebruiken om aanbiedingen te ontvangen, moeten feedback verzenden als een ervaringsgebeurtenis. Met andere woorden, als de aanbieding instructies over hoe te om vereist terug te geven, kunt u veronderstellen dat u in terugkoppelt als ervaringsgebeurtenissen zou moeten verzenden.

### Aangepaste gebeurtenissen

Feedback op aangepaste gebeurtenissen die aan een voorstel zijn gekoppeld, kan naar Adobe Experience Platform worden verzonden op basis van je eigen voorkeuren. Als een aanbieding bijvoorbeeld meerdere knoppen bevat, zoals *Geïnteresseerd*, *Niet geïnteresseerd*, enzovoort, wilt u deze gebeurtenissen mogelijk afzonderlijk verzenden, maar deze kunnen ook worden verzonden als ervaringsgebeurtenissen.

## Feedbackgegevens verzenden

Als u feedbackgegevens wilt verzenden, moet u een gegevensset maken om gebeurtenissen te verzamelen en voor elk gebeurtenistype een ervaringsgebeurtenis definiëren die naar Adobe Experience Platform wordt verzonden.

* Leer hoe te om een dataset tot stand te brengen waar de ervaringsgebeurtenissen in zullen worden verzameld [deze sectie](create-dataset.md).

* Leer hoe u ervaringsgebeurtenissen definieert die u wilt verzenden in feedbackgegevens in [deze sectie](schema-requirement.md).
