---
product: experience platform
solution: Experience Platform
title: Vastleggen van gebeurtenissen configureren
description: Leer hoe u uw aanbiedingsschema configureert om gebeurtenissen vast te leggen
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 17d37da6e6325d36df0f63122fa37f416e3f2c4c
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Vastleggen van gebeurtenissen configureren {#schema-requirements}

U moet nu beschikken over:

* het AI-model heeft gecreëerd,
* gedefinieerd welk type gebeurtenis u wilt vastleggen - weergegeven aanbod (indruk) en/of aangeklikte aanbieding (conversie);
* en in welke gegevensset u de gebeurtenisgegevens wilt verzamelen.

Telkens wanneer een aanbieding wordt getoond en/of geklikt, wilt u dat de overeenkomstige gebeurtenis automatisch wordt gevangen door **[!UICONTROL Experience Event - Proposition Interactions]** veldgroep met de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target=&quot;_blank&quot;} of Mobile SDK.

Als u gebeurtenistypen wilt kunnen verzenden (weergegeven aanbod of aangeklikte aanbieding), moet u de juiste waarde voor elk gebeurtenistype instellen in een ervaringsgebeurtenis die naar Adobe Experience Platform wordt verzonden. Hieronder vindt u de schemavereisten die u in uw JavaScript-code moet implementeren:

### Weergegeven scenario voorstellen

**Type gebeurtenis:** `decisioning.propositionDisplay`
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
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for “nextBestOffer”
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for “nextBestOffer”
        }
    ]
}
```

+++

### Aangeboden scenario

**Type gebeurtenis:** `decisioning.propositionInteract`
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
