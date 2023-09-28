---
title: Verzamelingen weergeven
description: Verzamelingen zijn subsets van aanbiedingen die zijn gebaseerd op vooraf gedefinieerde voorwaarden die door een marketmaker zijn gedefinieerd, zoals de categorie van de aanbieding.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f27ffbe0-a61a-428a-bc37-db6b56e38a83
source-git-commit: bee5e067e70e065c9db14448c42224a9ec09c5bf
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 3%

---

# Verzamelingen weergeven {#list-collections}

Verzamelingen zijn subsets van aanbiedingen die zijn gebaseerd op vooraf gedefinieerde voorwaarden die door een marketmaker zijn gedefinieerd, zoals de categorie van de aanbieding.

U kunt een lijst van alle inzamelingen bekijken door één enkel verzoek van de GET aan uit te voeren [!DNL Offer Library] API.

**API-indeling**

```http
GET /{ENDPOINT_PATH}/offer-collections?{QUERY_PARAMS}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Optionele queryparameters om resultaten te filteren op. | `limit=2` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-collections?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Query-parameters gebruiken {#using-query-parameters}

U kunt queryparameters gebruiken om de resultaten te filteren en te pagineren wanneer u bronnen weergeeft.

### Paginering {#paging}

De gemeenschappelijkste vraagparameters voor het pagineren omvatten:

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `property` | Een optioneel eigenschapsfilter: <ul><li> De eigenschappen worden gegroepeerd door EN-bewerking. <br><br> - Parameters kunnen als volgt worden herhaald: property=`<property-expr>`[&amp;eigenschap=`<property-expr2>`...] or property=`<property-expr1>`[&amp;`<property-expr2>`...] <br><br> - Eigenschapexpressies hebben een indeling `[!]field[op]` waarde, met op in `[==,!=,'<=',>=,<,>,~]`, die reguliere expressies ondersteunen  </li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Resultaten sorteren op een bepaalde eigenschap. Als u de naam a - before toevoegt (orderby=-name), worden de items op naam gesorteerd in aflopende volgorde (Z-A). Padexpressies hebben de vorm van door punten gescheiden paden. Deze parameter kan als volgt worden herhaald: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Beperk het aantal geretourneerde entiteiten. | `limit=5` |

**Antwoord**

Een succesvolle reactie keert een lijst van inzamelingen terug die binnen de container aanwezig zijn u toegang tot hebt.

```json
{
        "results": [
        {
            "created": "2022-09-16T18:59:23.063+00:00",
            "modified": "2022-09-16T18:59:23.063+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.4"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerCollection1234",
            "name": "Test Collection with tags",
            "filterType": "any-tags",
            "ids": [
                "tag1234"
            ],
            "labels": [
                "core/C5",
                "custom/myLabel"
            ]
        },
        {
            "created": "2023-05-15T12:50:49.887+00:00",
            "modified": "2023-05-15T12:50:49.887+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.4"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerCollection5678",
            "name": "Test Collection with offers",
            "filterType": "offers",
            "ids": [
                "personalizedOffer1234",
                "personalizedOffer5678"
            ]
        }
    ],
    "count": 2,
    "total": 9,
    "_links": {
        "self": {
            "href": "/offer-collections?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-collections?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
