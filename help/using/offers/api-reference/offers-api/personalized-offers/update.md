---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Aangepaste aanbiedingen bijwerken
description: Een gepersonaliseerd aanbod is een aanpasbaar marketingbericht op basis van geschiktheidsregels en -beperkingen.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 9d8f2df6-aa04-4e66-8555-d51c2e409063
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---

# Een persoonlijke aanbieding bijwerken {#update-personalized-offer}

U kunt een gepersonaliseerde aanbieding wijzigen of bijwerken door een PATCH-aanvraag in te dienen bij de [!DNL Offer Library] API

Voor meer informatie over Reparatie JSON, met inbegrip van beschikbare verrichtingen, zie de officiële [ documentatie van het Reparatie JSON ](https://jsonpatch.com/).

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

De volgende lijst toont de geldige waarden die uit het *inhoud-Type* gebied in de verzoekkopbal bestaan:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Inhoudstype | `application/json` |

**API formaat**

```http
PATCH /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | De id van de entiteit die u wilt bijwerken. | `personalizedOffer1234` |

**Verzoek**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated personalized offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated personalized offer description"
    }
]'
```

| Parameter | Beschrijving |
| --------- | ----------- |
| `op` | De verrichtingsvraag die wordt gebruikt om de actie te bepalen nodig om de verbinding bij te werken. Bewerkingen zijn: `add` , `replace` , `remove` , `copy` en `test` . |
| `path` | Het pad van de parameter die moet worden bijgewerkt. |
| `value` | De nieuwe waarde waarmee u de parameter wilt bijwerken. |

**Reactie**

Een geslaagde reactie retourneert de bijgewerkte details van de plaatsing, inclusief de plaatsings-id.

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
