---
title: Gegevensverzameling
description: Meer informatie over het verzamelen van feedback over beslissingsbeheer
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: d690e066e5a6ec51b0cc86f9e4f375e72cd7f661
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

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

1. Aan de ene kant, sommige kanalen **automatisch** impressies bijhouden en klikken. Deze zijn als volgt:

   * E-mails geschreven door [!DNL Journey Optimizer]
   * Mobiele pushmeldingen gemaakt door [!DNL Journey Optimizer]

   <!--If Adobe renders the offer visually to the end user on the channel, you can assume that Adobe will auto-send in the feedback.-->

1. Aan de andere kant vereisen sommige kanalen dat indrukken en klikgegevens als een **Experience, gebeurtenis**.

   Alle kanalen die een beslissing-API-aanvraag gebruiken om aanbiedingen te ontvangen, moeten feedback verzenden als een ervaringsgebeurtenis. Dit omvat:

   * Webpagina&#39;s die de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"} om aanbiedingen te renderen
   * Mobiele toepassingen met de [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} om aanbiedingen te renderen
   * Kiosks
   * Berichten die via toepassingen van derden worden verzonden

   >[!NOTE]
   >
   >Als de aanbieding instructies over hoe te om te geven nodig heeft, kunt u veronderstellen dat u in terugkoppelt als ervaringsgebeurtenissen zou moeten verzenden.

### Aangepaste gebeurtenissen

Feedback op aangepaste gebeurtenissen die aan een voorstel zijn gekoppeld, kan naar Adobe Experience Platform worden verzonden op basis van je eigen voorkeuren. Als een aanbieding bijvoorbeeld meerdere knoppen bevat, zoals *Geïnteresseerd*, *Niet geïnteresseerd*, enzovoort, wilt u deze gebeurtenissen mogelijk afzonderlijk verzenden, maar deze kunnen ook worden verzonden als ervaringsgebeurtenissen. <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## Feedbackgegevens verzenden

Als u feedbackgegevens wilt verzenden, moet u een gegevensset maken om gebeurtenissen te verzamelen en voor elk gebeurtenistype een ervaringsgebeurtenis definiëren die naar Adobe Experience Platform wordt verzonden.

* Leer hoe te om een dataset tot stand te brengen waar de ervaringsgebeurtenissen in zullen worden verzameld [deze sectie](create-dataset.md).

* Leer hoe u ervaringsgebeurtenissen definieert die u wilt verzenden in feedbackgegevens in [deze sectie](schema-requirement.md).

