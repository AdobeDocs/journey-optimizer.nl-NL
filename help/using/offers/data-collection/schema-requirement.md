---
product: experience platform
solution: Experience Platform
title: Vastleggen van gebeurtenissen configureren
description: Leer hoe u uw aanbiedingsschema configureert om gebeurtenissen vast te leggen
badge: label="Verouderd" type="Informative"
feature: Ranking, Datasets, Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Gegevensverzameling configureren {#schema-requirements}

Om terugkoppelen op gebeurtenistypes buiten besluitvormingsgebeurtenissen te kunnen krijgen, moet u de correcte waarde voor elk gebeurtenistype in een **ervaringsgebeurtenis** plaatsen die in Adobe Experience Platform wordt verzonden.

>[!CAUTION]
>
>Voor elk gebeurtenistype, zorg ervoor het schema dat in de dataset wordt gebruikt de **[!UICONTROL Experience Event - Proposition Interactions]** gebiedsgroep verbonden aan het heeft. [Meer informatie](create-dataset.md)

Hieronder staan de schemavereisten die u in uw code van JavaScript moet uitvoeren.

>[!NOTE]
>
>De gebeurtenissen van het besluit hoeven niet binnen worden verzonden aangezien het beheer van het Besluit deze gebeurtenissen automatisch zal produceren en hen in de **[!UICONTROL ODE DecisionEvents]** dataset <!--to check--> zetten die auto-geproduceerd is.

## Afbeeldingen bijhouden {#track-impressions}

Zorg ervoor dat het gebeurtenistype en de bron als volgt zijn:

**gebeurtenistype van de Ervaring:** `decisioning.propositionDisplay`
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) of partijingestion
+++**lading van de Steekproef:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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

**gebeurtenistype van de Ervaring:** `decisioning.propositionInteract`
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) of partijingestion
+++**lading van de Steekproef:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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

Voor aangepaste gebeurtenissen moet aan het schema dat in de gegevensset wordt gebruikt ook de veldgroep **[!UICONTROL Experience Event - Proposition Interactions]** zijn gekoppeld, maar is er geen specifieke vereiste voor het gebeurtenistype Experience die moet worden gebruikt om deze gebeurtenissen te labelen.

>[!NOTE]
>
>Om uw douanegebeurtenissen te hebben die in [ frequentietoewijzing ](../offer-library/add-constraints.md#capping) worden vermeld, moet u de ervaringsgebeurtenis met Adobe Experience Platform eindpunten verbinden door het naar één van beide eindpunten van de gegevensinzameling van Edge te verzenden:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>Als u het [ Web SDK van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"} of [ Adobe Experience Platform Mobiele SDK ](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} gebruikt, wordt de verbinding automatisch gemaakt.
