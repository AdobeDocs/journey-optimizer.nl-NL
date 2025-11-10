---
title: Een waarderingsformule opzoeken
description: Met behulp van de rangschikkingsformules kunt u de functies voor scoring definiëren, die wordt gebruikt om items te rangschikken.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: f048b2d1-d26b-4987-8acb-3558df506ec2
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 1%

---

# Opzoeken  {#list-ranking-formula}

U kunt specifieke rangschikkingsformule opzoeken door een GET-aanvraag in te dienen bij de API voor de aanbiedingsbibliotheek die de id in het aanvraagpad bevat.

**API formaat**

```http
GET /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt opzoeken. | `rankingFormula1234` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een succesvolle reactie retourneert de details van de rangschikkingsformule.

```json
{
    "created": "2024-08-08T23:45:15.380Z",
    "modified": "2024-10-22T18:15:05.909Z",
    "etag": 36,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/ranking-function"
    ],
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "id": "dps:ranking-function:1947f5372cc4ed74",
    "name": "[Do not delete] - Cypress e2e - edit",
    "description": "some description",
    "returnType": {
        "type": "INTEGER"
    },
    "exdFunction": true,
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "42 = 11"
    }
}
```
