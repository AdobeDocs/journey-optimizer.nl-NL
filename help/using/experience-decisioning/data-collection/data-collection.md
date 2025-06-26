---
title: Dataverzameling
description: Meer informatie over het verzamelen van feedback over beslissingsbeheer
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer, Developer
level: Experienced
source-git-commit: dd108b67ec252d391418d8af53de696bf9cd167d
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 1%

---

# Verzameling van beslissingsbeheersgegevens {#data-collection}

## Gegevensverzameling

Je kunt feedback over beslissingen in Adobe Experience Platform verzamelen, waaronder welke aanbiedingen worden weergegeven en hoe gebruikers met hen communiceren. Deze gegevens kunnen worden gebruikt voor:

* Het samenstellen van [ beslissingsrapporten ](../cja-reporting.md);
* Gebruikend [ het maximum ](../items.md#capping) regels;
* Bouwend AI modellen <!--add link--> die als rangschikkende methode kunnen worden gebruikt.

## Typen gebeurtenissen

De manier waarop gegevens worden verzameld, varieert afhankelijk van het gebeurtenistype dat u wilt vastleggen.

### Gebeurtenissen van Besluit

Telkens als Beslissing een besluit neemt, wordt de informatie met betrekking tot die besluitvormingsgebeurtenis **automatisch** verzonden naar Adobe Experience Platform. <!--TBC + link-->

### Impressie en klik op gebeurtenissen

Afbeeldingen en klikken in het kader van besluitvormingsbeheer worden als volgt gedefinieerd:

* Een **indruk** gebeurtenis is wanneer een aanbieding aan een gebruiker wordt getoond.

* A **klik** gebeurtenis is wanneer een gebruiker klikt of met een aanbieding in wisselwerking staat.

Feedback op afbeeldingen en klikken wordt vastgelegd afhankelijk van het gebruikte [!DNL Journey Optimizer] kanaal.

**Emails** authored door [!DNL Journey Optimizer] **&#x200B;**&#x200B;sporen automatisch indrukken en klikken.

Nochtans, **vereisen de meeste kanalen** impressies en kliks gegevens die in Adobe Experience Platform als **ervaringsgebeurtenis** moeten worden verzonden. Dit omvat het volgende:

* Web-pagina&#39;s die [ SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=nl-NL){target="_blank"} gebruiken om aanbiedingen terug te geven

* Mobiele apps die [ Adobe Experience Platform Mobile SDK ](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=nl-NL){target="_blank"} gebruiken om aanbiedingen terug te geven - [ leer meer ](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* Kiosks
* Berichten die via toepassingen van derden worden verzonden
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>Kanalen die een beslissing-API-aanvraag gebruiken om aanbiedingen te ontvangen, moeten feedback verzenden als een ervaringsgebeurtenis. Met andere woorden, als de aanbieding instructies over hoe te om vereist terug te geven, kunt u veronderstellen dat u in terugkoppelt als ervaringsgebeurtenissen zou moeten verzenden.

### Aangepaste gebeurtenissen

Feedback op aangepaste gebeurtenissen die aan een voorstel zijn gekoppeld, kan naar Adobe Experience Platform worden verzonden op basis van je eigen voorkeuren. Bijvoorbeeld, als een aanbieding veelvoudige knopen zoals *Geïnteresseerde* heeft, *niet geinteresseerd*, enz., kunt u in die gebeurtenissen willen verzenden afzonderlijk, maar deze kunnen ook binnen als ervaringsgebeurtenissen worden verzonden.

## Feedbackgegevens verzenden

Als u feedbackgegevens wilt verzenden, moet u een gegevensset maken om gebeurtenissen te verzamelen en voor elk gebeurtenistype een ervaringsgebeurtenis definiëren die naar Adobe Experience Platform wordt verzonden.

* Leer hoe te om een dataset tot stand te brengen waar de ervaringsgebeurtenissen in [ deze sectie ](create-dataset.md) zullen worden verzameld.

* Leer hoe te om ervaringsgebeurtenissen te bepalen in terugkoppelt gegevens in [ dit sectie ](schema-requirement.md) te verzenden.
