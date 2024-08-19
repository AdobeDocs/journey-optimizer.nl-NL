---
title: Een itemverzameling opzoeken
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: dc47e2835379fbb2afb768beea6e4a1596f70ee9
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 1%

---


# Een itemverzameling opzoeken {#lookup-item-collection}

U kunt specifieke puntinzameling omhoog zoeken door een verzoek van de GET aan de Bibliotheek API van de Aanbieding te richten die identiteitskaart in de verzoekweg omvat.

**API formaat**

```http
GET /{ENDPOINT_PATH}/item-collections/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt opzoeken. | `itemCollections1234` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een succesvolle reactie keert de details van de puntinzamelingen terug.

```json
{
    "created": "2024-01-31T18:28:52.888Z",
    "modified": "2024-06-28T19:44:13.112Z",
    "etag": 7,
    "schemas": [
        "https://ns.adobe.com/experience/decisioning/item-collection;version=1.2"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "itemCollection1234",
    "name": "Item collection One",
    "description": "Item collection",
    "constraints": [
        {
            "itemCatalogId": "itemCatalog1234",
            "uiModel": "{\"operator\":\"equals\",\"value\":{\"left\":\"_experience.decisioning.decisionitem.itemName\",\"right\":\"Some offer item\"}}"
        }
    ]
}
```
