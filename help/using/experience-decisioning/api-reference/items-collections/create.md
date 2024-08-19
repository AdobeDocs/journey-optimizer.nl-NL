---
title: Een itemverzameling maken
description: Met verzamelingen kunt u beslissingsitems categoriseren en groeperen op basis van uw voorkeuren.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: dcff8803404228bbed40e998d802bb6c0f4ac67e
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# Een itemverzameling maken {#create-decision-items}

U kunt een puntinzameling tot stand brengen door een verzoek van de POST aan de Bibliotheek API van de Aanbieding te doen.

**Accepteer en inhoud-Type kopballen**

In de volgende tabel worden de geldige waarden weergegeven die bestaan uit de velden Inhoudstype in de aanvraagkoptekst:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Inhoudstype | `application/json` |

**API formaat**

```http
POST /{ENDPOINT_PATH}/item-collections
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |

**Verzoek**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/item-collections' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{     
    "name": "Item collection One",
    "description": "Item collection",
    "constraints": [
        {
            "itemCatalogId": "itemCatalog1234",
            "uiModel": "{\"operator\":\"equals\",\"value\":{\"left\":\"_experience.decisioning.decisionitem.itemName\",\"right\":\"Some offer item\"}}"
        }
    ]
}'
```

**Reactie**

Een geslaagde reactie retourneert de details van het nieuwe besluitvormingspunt, inclusief de id. U kunt de id in latere stappen gebruiken om uw beslissingsitem bij te werken of te verwijderen.

```json
{
    "etag": 1,
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
