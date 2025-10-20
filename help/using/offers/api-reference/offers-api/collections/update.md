---
title: Verzamelingen bijwerken
description: Verzamelingen zijn subsets van aanbiedingen die zijn gebaseerd op vooraf gedefinieerde voorwaarden die door een marketmaker zijn gedefinieerd, zoals de categorie van de aanbieding.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 7d766f0a-4fcb-434a-bbfd-e18ade71ae56
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 3%

---

# Een verzameling bijwerken {#update-collection}

U kunt een verzameling wijzigen of bijwerken door een PATCH-aanvraag in te dienen bij de [!DNL Offer Library] API

Voor meer informatie over Reparatie JSON, met inbegrip van beschikbare verrichtingen, zie de officiële [&#x200B; documentatie van het Reparatie JSON &#x200B;](https://jsonpatch.com/).

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

De volgende lijst toont de geldige waarden die uit het *inhoud-Type* gebied in de verzoekkopbal bestaan:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Inhoudstype | `application/json` |

**API formaat**

```http
PATCH /{ENDPOINT_PATH}/offer-collections/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt bijwerken. | `offerCollection1234` |

**Verzoek**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated offer collection"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated offer collection description"
    }
]'
```

| Parameter | Beschrijving |
| --------- | ----------- |
| `op` | De verrichtingsvraag die wordt gebruikt om de actie te bepalen nodig om de verbinding bij te werken. Bewerkingen zijn: `add` , `replace` , `remove` , `copy` en `test` . |
| `path` | Het pad van de parameter die moet worden bijgewerkt. |
| `value` | De nieuwe waarde waarmee u de parameter wilt bijwerken. |

**Reactie**

Een geslaagde reactie retourneert de bijgewerkte details van de verzameling, inclusief de unieke verzameling `id` .

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
