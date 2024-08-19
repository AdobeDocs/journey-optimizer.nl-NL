---
title: Een selectiestrategie maken
description: De strategieën van de selectie bestaan uit inzamelingen verbonden aan beperkingen en rangschikkende methodes om aanbiedingen te bepalen.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: dcff8803404228bbed40e998d802bb6c0f4ac67e
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 1%

---


# Een selectiestrategie maken {#create-selection-strategy}

U kunt een selectiestrategie maken door een POST aan te vragen bij de API voor de bibliotheek van het aanbod.

**Accepteer en inhoud-Type kopballen**

In de volgende tabel worden de geldige waarden weergegeven die bestaan uit de velden Inhoudstype in de aanvraagkoptekst:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Inhoudstype | `application/json` |

**API formaat**

```http
POST /{ENDPOINT_PATH}/selection-strategies 
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |

**Verzoek**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/selection-strategies' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{    
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
}'
```

**Reactie**

Een geslaagde reactie retourneert de details van de nieuwe selectiestrategie inclusief de id. U kunt de id in latere stappen gebruiken om uw selectiestrategie bij te werken of te verwijderen.

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
