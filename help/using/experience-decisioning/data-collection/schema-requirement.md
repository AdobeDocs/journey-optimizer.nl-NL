---
solution: Journey Optimizer
product: Journey Optimizer
title: Vastleggen van gebeurtenissen configureren
description: Leer hoe u uw aanbiedingsschema configureert om gebeurtenissen vast te leggen
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
version: Journey Orchestration
source-git-commit: 5de16a8f69089e49484104bbae109df111cbf1ed
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Gegevensverzameling configureren {#schema-requirements}

Om terugkoppelen op gebeurtenistypes buiten besluitvormingsgebeurtenissen te kunnen krijgen, moet u de correcte waarde voor elk gebeurtenistype in een **ervaringsgebeurtenis** plaatsen die in Adobe Experience Platform wordt verzonden.

>[!CAUTION]
>
>Voor elk gebeurtenistype, zorg ervoor het schema dat in de dataset wordt gebruikt de **[!UICONTROL Experience Event - Proposition Interactions]** gebiedsgroep verbonden aan het heeft. <!--[Learn more](create-dataset.md)-->

Hieronder staan de schemavereisten die u in uw code van JavaScript moet uitvoeren.

## Afbeeldingen bijhouden {#track-impressions}

Controleer of de volgende velden correct zijn geconfigureerd:

**gebeurtenistype van de Ervaring:** `decisioning.propositionDisplay`

**propositionEventType:** `_experience.decisioning.propositionEventType.display`

**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) of partijingestion

+++**lading van de Steekproef:**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "display": 1
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionDisplay",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b219",
  "timestamp": "2025-10-07T20:22:00Z"
}
```

+++

## Klikken bijhouden {#track-clicks}

Controleer of de volgende velden correct zijn geconfigureerd:

**gebeurtenistype van de Ervaring:** `decisioning.propositionInteract`

**propositionEventType:** `_experience.decisioning.propositionEventType.interact`

**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) of partijingestion

Elk aanbod in een voorstel bevat een trackingtoken. Dit is een unieke id die door Adobe wordt gegenereerd. Dit token moet exact worden doorgegeven zoals het is ontvangen — zonder wijziging — in de corresponderende klik- of impressiegebeurtenis. Overeenkomende trackingtokens zorgen ervoor dat Adobe de actie van de gebruiker precies kan koppelen aan het juiste aanbiedingsbesluit, waardoor downstreamrapportage en op AI gebaseerde optimalisatie mogelijk zijn.

+++**lading van de Steekproef:**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "interact": 1
      },
      "propositionAction": {
        "tokens": [
          "Vx9fwWXmp6/kyYRVOUZWEQ"
        ]
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionInteract",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b765",
  "timestamp": "2025-10-07T20:50:00Z"
}
```

+++

## Aangepaste gebeurtenissen bijhouden {#track-custom-events}

Voor aangepaste gebeurtenissen moet aan het schema dat in de gegevensset wordt gebruikt ook de veldgroep **[!UICONTROL Experience Event - Proposition Interactions]** zijn gekoppeld, maar is er geen specifieke vereiste voor het gebeurtenistype Experience die moet worden gebruikt om deze gebeurtenissen te labelen.

<!--

>[!NOTE]
>
>To have your custom events accounted for in [capping](../items.md#capping), you need to connect the experience event to Adobe Experience Platform endpoints by sending it to either one of these two Edge data collection endpoints:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>If you are using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=nl-NL){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=nl-NL){target="_blank"}, the connection is made automatically.-->

