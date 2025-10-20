---
title: Een beslissingsregel maken
description: Beslissingsregels zijn beperkingen die aan een gepersonaliseerd aanbod worden toegevoegd en die op een profiel worden toegepast om te bepalen of het in aanmerking komt voor een aanbieding.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 6a05efca-31bd-46d5-998d-ff3038d9013f
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 8%

---

# Een beslissingsregel maken {#create-decision-rule}

Beslissingsregels zijn beperkingen die aan een gepersonaliseerd aanbod worden toegevoegd en die op een profiel worden toegepast om te bepalen of het in aanmerking komt voor een aanbieding.

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

De volgende lijst toont de geldige waarden die uit het *inhoud-Type* gebied in de verzoekkopbal bestaan:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Inhoudstype | `application/json` |

**API formaat**

```http
POST /{ENDPOINT_PATH}/offer-rules
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |

**Verzoek**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-rules' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Sales rule",
    "description": "Decisioning rule for sales",
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "profile.person.name.firstName.equals(\"Joe\", false)"
    },
    "definedOn": {
        "profile": {
            "schema": {
                "ref": "https://ns.adobe.com/xdm/context/profile_union",
                "version": "1"
            },
            "referencePaths": [
                "person.name.firstName"
            ]
        }
    }
}'
```

**Reactie**

Een geslaagde reactie retourneert informatie over de nieuwe beslissingsregel `id` . U kunt `id` in recentere stappen gebruiken om uw besluitvormingsregel bij te werken of te schrappen of het in een recentere zelfstudie te gebruiken om besluiten, besluitvormingsregels, en reserveaanbiedingen tot stand te brengen.

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
