---
title: Een itemverzameling bijwerken
description: Verzamelingen zijn subsets van aanbiedingen die zijn gebaseerd op vooraf gedefinieerde voorwaarden die door een marketmaker zijn gedefinieerd, zoals de categorie van de aanbieding.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: a2b7779d-8c2e-4ff9-8cc3-90846f100c98
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---

# Een itemverzameling bijwerken {#update-item-collection}

U kunt een itemverzameling wijzigen of bijwerken door een PATCH-aanvraag in te dienen bij de bibliotheek-API van het aanbod.

Voor meer informatie over Reparatie JSON, met inbegrip van beschikbare verrichtingen, zie de officiële [ documentatie van het Reparatie JSON ](https://jsonpatch.com/).

**API formaat**

```http
PATCH /{ENDPOINT_PATH}/item-collections/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt bijwerken. | `itemCollections1234` |

**Verzoek**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated item collection"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated item collection description"
    }
]'
```

| Parameter | Beschrijving |
| --------- | ----------- |
| `value` | De nieuwe waarde waarmee u de parameter wilt bijwerken. |
| `path` | Het pad van de parameter die moet worden bijgewerkt. |
| `op` | De verrichtingsvraag die wordt gebruikt om de actie te bepalen nodig om de verbinding bij te werken. Bewerkingen zijn: `add` , `replace` , `remove` , `copy` en `test` . |

**Reactie**

Een geslaagde reactie retourneert de bijgewerkte details van de itemverzameling, inclusief de `id` .

```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
