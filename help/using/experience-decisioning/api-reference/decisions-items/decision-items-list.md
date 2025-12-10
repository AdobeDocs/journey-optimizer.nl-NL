---
title: Beslissingsitems weergeven
description: Beslissingsitems zijn marketingaanbiedingen die u kunt maken en indelen in verzamelingen en catalogi.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: ac618861-276f-4f9c-95d3-7df0b5132be9
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Beslissingsitems weergeven {#list-decision-items}

Met Journey Optimizer kunt u marketingaanbiedingen maken, ook wel &#39;beslissingsitems&#39; genoemd, die u kunt maken en indelen in een gecentraliseerde catalogus en verzamelingen. Ze bestaan uit standaard- en aangepaste kenmerken die precies op uw behoeften zijn afgestemd. Bovendien, nemen zij profielbeperkingen op die u toestaan om te bepalen aan wie een besluitpunt kan worden getoond.

U kunt een lijst van alle besluitvormingspunten bekijken door één enkel GET verzoek aan de Bibliotheek API van de Aanbieding uit te voeren.

**API formaat**

```http
GET /{ENDPOINT_PATH}/offer-items?{QUERY_PARAMS}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Optionele queryparameters om resultaten te filteren op. | `limit=2` |

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
curl -X GET '<https://platform.adobe.io/data/core/dps/offer-items?limit=2>' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**Reactie**

Een succesvolle reactie retourneert een lijst met aangeboden objecten waartoe u toegang hebt. Het knooppunt `_<imsOrg>` bevat kenmerken voor aangepaste beslissingsitems.

```json
{
    "results": [
        {
            "created": "2024-06-10T16:00:34.014Z",
            "modified": "2024-07-09T22:59:21.507Z",
            "etag": 1,
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerItem5678",
            "_experience": {
                "decisioning": {
                    "offeritem": {
                        "fCapConstraintsLastIndex": 0,
                        "lifecycleStatus": "draft"
                    },
                    "decisionitem": {
                        "itemCalendarConstraints": {
                            "endDate": "2030-12-31T08:00:00.000Z",
                            "startDate": "2024-06-10T04:00:00.000Z"
                        },
                        "itemCatalogID": "itemCatalong1234",
                        "itemConstraints": {
                            "eligibilityRule": "rule1234",
                            "profileConstraintType": "eligibilityRule"
                        },
                        "itemDescription": "Offer item description",
                        "itemID": "offerItem5678",
                        "itemLabels": [],
                        "itemName": "Offer Item One",
                        "itemPriority": 1,
                        "itemTags": []
                    }
                }
            },
            "_<imsOrg>": {
                "some_field": "some value"
            }
        },
        {
            "created": "2024-06-04T17:51:52.849Z",
            "modified": "2024-06-28T18:29:27.951Z",
            "etag": 5,
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerItem1234",
            "_experience": {
                "decisioning": {
                    "offeritem": {
                        "frequencyCappingConstraints": [],
                        "fCapConstraintsLastIndex": 0,
                        "lifecycleStatus": "approved"
                    },
                    "decisionitem": {
                        "itemCalendarConstraints": {
                            "endDate": "2030-12-31T08:00:00.000Z",
                            "startDate": "2024-06-01T07:00:00.000Z"
                        },
                        "itemCatalogID": "itemCatalong1234",
                        "itemConstraints": {
                            "profileConstraintType": "none"
                        },
                        "itemDescription": "Offer item description",
                        "itemID": "offerItem1234",
                        "itemLabels": [],
                        "itemName": "Offer Item Two",
                        "itemPriority": 2,
                        "itemTags": []
                    }
                }
            },
            "YOUR_CUSTOM_ATTRIBUTES": {
                "some_field": "some value",
                "some_boolean_field": true
            }
        }
    ],
    "count": 2,
    "total": 844,
    "_links": {
        "self": {
            "href": "/offer-items?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-items?orderby=-modified&limit=2&start=2024-06-28T03:44:15.630Z",
            "type": "application/json"
        }
    }
}
```
