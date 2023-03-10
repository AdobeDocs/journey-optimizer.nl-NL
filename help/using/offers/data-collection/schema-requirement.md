---
product: experience platform
solution: Experience Platform
title: Vastleggen van gebeurtenissen configureren
description: Leer hoe u uw aanbiedingsschema configureert om gebeurtenissen vast te leggen
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---

# Gegevensverzameling configureren {#schema-requirements}

<!--To send in feedback data, you must define how the experience events will be captured.-->

Als u feedback wilt krijgen over andere gebeurtenistypen dan beslissingsgebeurtenissen, moet u de juiste waarde voor elk gebeurtenistype in een **Experience, gebeurtenis** die naar Adobe Experience Platform wordt verzonden.

Voor elk gebeurtenistype, zorg ervoor het schema in de dataset wordt gebruikt heeft **[!UICONTROL Experience Event - Proposition Interactions]** veldgroep die eraan is gekoppeld. [Meer informatie](create-dataset.md)

Hieronder vindt u de schemavereisten die u in uw JavaScript-code moet implementeren.

>[!NOTE]
>
>Beslissingsgebeurtenissen hoeven niet te worden verzonden omdat het beheer van het besluit deze gebeurtenissen automatisch zal genereren en in de **[!UICONTROL ODE DecisionEvents]** gegevensset<!--to check--> die automatisch wordt gegenereerd.

## Afbeeldingen bijhouden

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

## Klikken bijhouden

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

## Aangepaste gebeurtenissen bijhouden

Voor douanegebeurtenissen, moet het schema dat in de dataset wordt gebruikt ook hebben **[!UICONTROL Experience Event - Proposition Interactions]** veldgroep die eraan is gekoppeld, maar er is geen specifieke vereiste met betrekking tot het type ervaringsgebeurtenis dat moet worden gebruikt om deze gebeurtenissen van tags te voorzien.

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision. For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->
