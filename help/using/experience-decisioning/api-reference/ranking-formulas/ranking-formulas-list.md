---
title: Classificatieformules weergeven
description: Met behulp van de rangschikkingsformules kunt u de functies voor scoring definiëren, die wordt gebruikt om items te rangschikken.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 8b07be08-b37c-4535-82d8-3304340cbcad
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---

# Classificatieformules weergeven {#list-ranking-formulas}

Een rangschikkingsformule bestaat uit een rangschikkingsfunctie die bepaalt hoe deze moet worden gerangschikt.

U kunt een lijst van alle rangschikkingsformules bekijken door één enkele GET- verzoek aan de Bibliotheek API van de Aanbieding uit te voeren.

**API formaat**

```http
GET /{ENDPOINT_PATH}/ranking-formulas?{QUERY_PARAMS}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | exdFunction. | `property=exdFunction%3D%3Dtrue` |

## Query-parameters gebruiken {#using-query-parameters}

U kunt queryparameters gebruiken om de resultaten te filteren en te pagineren wanneer u bronnen weergeeft.

### Paginering {#paging}

De gemeenschappelijkste vraagparameters voor het pagineren omvatten:

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `property` | Een optioneel eigenschapsfilter: <ul><li>De eigenschappen worden gegroepeerd door EN-bewerking.</li><li>De parameters kunnen als zo worden herhaald: property= {PROPERTY_EXPR}[&amp;property= {PROPERTY_EXPR2}... ] of property= {PROPERTY_EXPR1}[, {PROPERTY_EXPR2}.. ]</li><li>Eigenschapexpressies hebben de notatie `[ !]field[op]value` en ondersteunen `op` in `[==,!=,<=,>=,<,>,~]` reguliere expressies.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Resultaten sorteren op een bepaalde eigenschap. Als u de naam a - before toevoegt (orderby=-name), worden de items op naam gesorteerd in aflopende volgorde (Z-A). Padexpressies hebben de vorm van door punten gescheiden paden. Deze parameter kan als volgt worden herhaald: `orderby=field1[,-fields2,field3,...]` | `orderby=id`, `-name` |
| `limit` | Beperk het aantal geretourneerde entiteiten. | `limit=5` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/ranking-formulas?property=exdFunction%3D%3Dtrue&limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een succesvolle reactie keert een lijst van rangschikkende formules terug die u toegang tot hebt.

```json
{
    "results": [
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
        },
        {
            "created": "2024-05-03T13:06:22.361Z",
            "modified": "2024-10-18T22:47:35.396Z",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/ranking-function;version=0.3"
            ],
            "createdBy": "FD62391F5B44DF970A494124@AdobeID",
            "lastModifiedBy": "6F8A6FF05F4011C40A494005@AdobeID",
            "id": "xcore:ranking-function:18ca80c5b15c5e11",
            "name": "doc test exd",
            "description": "",
            "returnType": {
                "type": "INTEGER"
            },
            "exdFunction": true,
            "expression": {
                "type": "PQL",
                "format": "pql/text",
                "value": "false"
            }
        }
    ],
    "count": 2,
    "total": 50,
    "_links": {
        "self": {
            "href": "/ranking-formulas?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/ranking-formulas?orderby=-modified&limit=2&start=2024-10-18T22:22:35.048Z",
            "type": "application/json"
        }
    }
}
```
