---
title: Een beslissing opzoeken
description: Een beslissing bevat de logica die de selectie van een aanbieding informeert.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: ee242f0f-f331-4f41-9418-938b4ca1dda3
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 1%

---

# Een beslissing opzoeken {#look-up-decision}

U kunt specifieke beslissingen opzoeken door een GET-aanvraag in te dienen bij de [!DNL Offer Library] API die de beslissingen `id` bevat in het aanvraagpad.

**API formaat**

```http
GET /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | De id van de entiteit die u wilt opzoeken. | `offerDecision1234` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert de details van de beslissing, inclusief informatie over uw unieke beslissing `id` .

```json
{
    "created": "2022-11-15T16:35:06.873+00:00",
    "modified": "2023-05-15T15:00:27.641+00:00",
    "etag": 3,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerDecision1234",
    "name": "Test Decision One",
    "status": "draft",
    "startDate": "2021-08-23T07:00:00.000+00:00",
    "endDate": "2021-08-25T07:00:00.000+00:00",
    "fallback": "fallbackOffer1234",
    "criteria": [
        {
            "placements": [
                "offerPlacement1234",
                "offerPlacement5678"
            ],
            "rank": {
                "priority": 0,
                "order": {
                    "orderEvaluationType": "ranking-strategy",
                    "rankingStrategy": "123456789123"
                }
            },
            "profileConstraint": {
                "profileConstraintType": "none"
            },
            "optionSelection": {
                "filter": "offerCollection1234"
            }
        }
    ]
}
```
