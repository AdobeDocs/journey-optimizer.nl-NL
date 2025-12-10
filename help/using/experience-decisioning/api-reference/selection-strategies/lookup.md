---
title: Een selectiestrategie zoeken
description: De strategieën van de selectie bestaan uit inzamelingen verbonden aan beperkingen en rangschikkende methodes om aanbiedingen te bepalen.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: db590963-b45b-4844-ac12-775cc955b03e
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 1%

---

# Een selectiestrategie zoeken {#list-selection-strategy}

U kunt een specifieke selectiestrategie opzoeken door een GET-aanvraag in te dienen bij de API voor de aanbiedingsbibliotheek die de id bevat in het aanvraagpad.

**API formaat**

```http
GET /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt opzoeken. | `selectionStrategy1234` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Als de reactie succesvol was, worden de details van de selectiestrategie geretourneerd.

```json
{
    "created": "2024-02-08T03:01:50.924Z",
    "modified": "2024-02-16T23:03:03.019Z",
    "etag": 4,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/selection-strategy;version=0.2"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "selectionStrategy1234",
    "name": "Selection Strategy One",
    "description": "Selection Strategy",
    "rank": {
        "priority": 1,
        "order": {
            "orderEvaluationType": "static"
        }
    },
    "profileConstraint": {
        "profileConstraintType": "eligibilityRule",
        "eligibilityRule": "offerRule1234"
    },
    "optionSelection": {
        "filter": "itemCollection1234",
    }
}
```
