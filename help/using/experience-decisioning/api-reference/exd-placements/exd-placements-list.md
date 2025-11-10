---
title: Extra plaatsing weergeven
description: De uitgebreide plaatsen bestaan uit inzamelingen verbonden aan beperkingen en rangschikkende methodes om aanbiedingen te bepalen.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---

# Extra plaatsing weergeven {#list-exd-placements}

U kunt een lijst van alle uitgebreide plaatsen bekijken door één enkel GET verzoek aan de Bibliotheek API van de Aanbieding uit te voeren.

**API formaat**

```http
GET /{ENDPOINT_PATH}/exd-placements?{QUERY_PARAMS}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |

## Query-parameters gebruiken {#using-query-parameters}

U kunt queryparameters gebruiken om de resultaten te filteren en te pagineren wanneer u bronnen weergeeft. U kunt filteren op status, kanaal en channelConfiguration.

### Paginering {#paging}

De gemeenschappelijkste vraagparameters voor het pagineren omvatten:

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `property` | Een optioneel eigenschapsfilter: <ul><li>De eigenschappen worden gegroepeerd door EN-bewerking.</li><li>De parameters kunnen als zo worden herhaald: property= {PROPERTY_EXPR}[&amp;property= {PROPERTY_EXPR2}... ] of property= {PROPERTY_EXPR1}[, {PROPERTY_EXPR2}.. ]</li><li>Eigenschapexpressies hebben de notatie `[ !]field[op]value` en ondersteunen `op` in `[==,!=,<=,>=,<,>,~]` reguliere expressies.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Resultaten sorteren op een bepaalde eigenschap. Als u de naam a - before toevoegt (orderby=-name), worden de items op naam gesorteerd in aflopende volgorde (Z-A). Padexpressies hebben de vorm van door punten gescheiden paden. Deze parameter kan als volgt worden herhaald: `orderby=field1[,-fields2,field3,...]` | `orderby=id`, `-name` |
| `limit` | Beperk het aantal geretourneerde entiteiten. | `limit=5` |

**Verzoek**

```shell
curl --location --request GET 'https://platform-stage.adobe.io/data/core/dps/exd-placements' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}' \
--data '{"query":"","variables":{}}'
```

**Reactie**

Een geslaagde reactie retourneert een lijst met uitgebreide plaatsingen waartoe u toegang hebt.

```json
{
    "results": [
        {
            "created": "2024-11-14T23:30:29.820Z",
            "modified": "2024-11-14T23:30:29.820Z",
            "etag": 1,
            "schemas": [
                "exd-placement"
            ],
            "createdBy": "14D546EA60B67E540A494010@658557135fa10b860a494019",
            "lastModifiedBy": "14D546EA60B67E540A494010@658557135fa10b860a494019",
            "id": "dps:exd-placement:19c61da45ed96159",
            "name": "testing-alfa",
            "description": "atest",
            "tags": [
                "35801d6b-6371-449d-9083-d895fc120569"
            ],
            "channel": "https://ns.adobe.com/xdm/channel-types/email",
            "channelConfiguration": "fb8e9621-a5e8-485f-9f3f-d040c601ebc4",
            "status": "active"
        },
        {
            "created": "2024-10-22T00:18:17.997Z",
            "modified": "2024-10-22T05:04:15.315Z",
            "etag": 2,
            "schemas": [
                ""
            ],
            "createdBy": "71486D7B5F4011980A494030@AdobeID",
            "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
            "id": "dps::19a7426d533db126",
            "name": "Test Exd Placement capacitor",
            "description": "Wooden system",
            "status": "archived"
        }
    ],
    "count": 2,
    "total": 2,
    "_links": {
        "self": {
            "href": "/exd-placements?orderby=-modified&limit=50",
            "type": "application/json"
        }
    }
}
```
