---
title: Een beslissingsitem bijwerken
description: Beslissingsitems zijn marketingaanbiedingen die u kunt maken en indelen in verzamelingen en catalogi.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: b924b7d0-bbed-409e-8173-0685fc41d7de
source-git-commit: b057d198d3c5b12121ee50d7a97ff4b33b8209b4
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# Een beslissingsitem bijwerken {#update-decision-items}

U kunt een besluitvormingspunt wijzigen of bijwerken door een verzoek van de PATCH aan de Bibliotheek API van de Aanbieding te doen.

Voor meer informatie over Reparatie JSON, met inbegrip van beschikbare verrichtingen, zie de officiële [&#x200B; documentatie van het Reparatie JSON &#x200B;](https://jsonpatch.com/).

**API formaat**

```http
PATCH /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt bijwerken. | `offerItem1234` |

**Verzoek**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}' \
-d '[
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemName",
        "value": "Updated offer item"
    },
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemDescription",
        "value": "Updated offer item description"
    }
]'
```

| Parameter | Beschrijving |
| --------- | ----------- |
| `value` | De nieuwe waarde waarmee u de parameter wilt bijwerken. |
| `path` | Het pad van de parameter die moet worden bijgewerkt. |
| `op` | Het type bewerking dat moet worden uitgevoerd. Bewerkingen zijn: `add` , `replace` , `remove` , `copy` en `test` . |

**Reactie**

Een geslaagde reactie retourneert de details van het bijgewerkte item, inclusief de id. U kunt de id in latere stappen gebruiken om uw beslissingsitem bij te werken of te verwijderen.

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
