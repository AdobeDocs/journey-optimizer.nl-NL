---
product: experience platform
solution: Experience Platform
title: Vastleggen van gebeurtenissen configureren
description: Leer hoe u uw aanbiedingsschema configureert om gebeurtenissen vast te leggen
feature: Ranking, Datasets, Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Gegevensverzameling configureren {#schema-requirements}

Als u feedback wilt krijgen over andere gebeurtenistypen dan beslissingsgebeurtenissen, moet u de juiste waarde voor elk gebeurtenistype in een **Experience, gebeurtenis** die naar Adobe Experience Platform wordt verzonden.

>[!CAUTION]
>
>Voor elk gebeurtenistype, zorg ervoor het schema in de dataset wordt gebruikt heeft **[!UICONTROL Experience Event - Proposition Interactions]** veldgroep die eraan is gekoppeld. [Meer informatie](create-dataset.md)

Hieronder vindt u de schemavereisten die u in uw JavaScript-code moet implementeren.

>[!NOTE]
>
>Beslissingsgebeurtenissen hoeven niet te worden verzonden omdat het beheer van het besluit deze gebeurtenissen automatisch zal genereren en in de **[!UICONTROL ODE DecisionEvents]** gegevensset<!--to check--> die automatisch wordt gegenereerd.

## Afbeeldingen bijhouden {#track-impressions}

Zorg ervoor dat het gebeurtenistype en de bron als volgt zijn:

**Gebeurtenistype Experience:** `decisioning.propositionDisplay`
**Bron:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) of batch ingestie
+++**Bemonsteringslading:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for "nextBestOffer"
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for "nextBestOffer"
        }
    ]
}
```

+++

## Klikken bijhouden {#track-clicks}

Zorg ervoor dat het gebeurtenistype en de bron als volgt zijn:

**Gebeurtenistype Experience:** `decisioning.propositionInteract`
**Bron:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) of batch ingestie
+++**Bemonsteringslading:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

+++

## Aangepaste gebeurtenissen bijhouden {#track-custom-events}

Voor douanegebeurtenissen, moet het schema dat in de dataset wordt gebruikt ook hebben **[!UICONTROL Experience Event - Proposition Interactions]** veldgroep die eraan is gekoppeld, maar er is geen specifieke vereiste met betrekking tot het type ervaringsgebeurtenis dat moet worden gebruikt om deze gebeurtenissen van tags te voorzien.

>[!NOTE]
>
>Als u aangepaste gebeurtenissen wilt laten opnemen in [frequentiecalculatie](../offer-library/add-constraints.md#capping), moet u de ervaringsgebeurtenis met Adobe Experience Platform eindpunten verbinden door het naar één van beide eindpunten van de gegevensinzameling van Edge te verzenden:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>Als u het [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}, wordt de verbinding automatisch gemaakt.
