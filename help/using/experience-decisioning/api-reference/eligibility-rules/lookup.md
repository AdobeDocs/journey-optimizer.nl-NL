---
title: Een toelatingsregel opzoeken
description: Aan de hand van de kwalificatieregels kunt u bepalen welke kandidaten in aanmerking komen op basis van wat u als doel wilt instellen, zoals profielkenmerken en doelgroepen.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: a74f4c87-0b89-4583-97f5-df8e2a30a19b
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 1%

---

# Een toelatingsregel opzoeken {#list-eligibility-rule}

U kunt specifieke toelatingsregels opzoeken door een GET-aanvraag in te dienen bij de API voor de bibliotheek van het aanbod die de id in het aanvraagpad bevat.

**API formaat**

```http
GET /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt opzoeken. | `rule1234` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een succesvol antwoord retourneert de details van de toelatingsregel.

```json
{
    "created": "2024-10-28T01:18:08.506Z",
    "modified": "2024-10-28T01:18:08.506Z",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/eligibility-rule"
    ],
    "createdBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
    "lastModifiedBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
    "id": "dps:eligibility-rule:19af09a9ae45a8d3",
    "name": "dasdsa",
    "description": "",
    "exdRule": false,
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "personalEmail.address.equals(\"youz@adobe.com\", false)"
    },
    "segmentModel": {
        "lifecycleState": "published",
        "expression": {
            "isValid": true,
            "logicalOperator": "and",
            "profileAttributesContainer": {
                "exclude": false,
                "items": [
                    {
                        "comparisonType": "equals",
                        "component": {
                            "id": "profile.personalEmail.address",
                            "__entity__": true,
                            "type": "Sz"
                        },
                        "isCaseSensitive": false,
                        "isPlaceholder": false,
                        "originalLocation": [],
                        "value": [
                            "youz@adobe.com"
                        ],
                        "itemType": "segmentRule"
                    }
                ],
                "logicalOperator": "and",
                "itemType": "segmentContainer"
            },
            "xEventAttributesContainer": {
                "exclude": false,
                "items": [],
                "logicalOperator": "then",
                "itemType": "eventTypeCardContainer"
            },
            "itemType": "segmentDefinition"
        },
        "isMissingAnsibleModel": false,
        "relationalExpression": false,
        "deprecated": {
            "status": false,
            "reason": ""
        },
        "description": "",
        "evaluationInfo": {
            "batch": {
                "enabled": true
            },
            "continuous": {
                "enabled": false
            },
            "synchronous": {
                "enabled": false
            }
        },
        "labels": [],
        "tags": [],
        "canHaveFolder": true,
        "mergePolicyId": "24526dbe-d615-4d41-9ebb-fd7f2b3dcdc2",
        "name": "dasdsa",
        "namespace": "ups"
    }
}
```
