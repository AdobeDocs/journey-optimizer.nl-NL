---
title: Beslissingsregels weergeven
description: Beslissingsregels zijn beperkingen die aan een gepersonaliseerd aanbod worden toegevoegd en die op een profiel worden toegepast om te bepalen of het in aanmerking komt voor een aanbieding.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: c4c3e415-bc57-45db-b27f-4a5e9fc1f02c
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 4%

---

# Beslissingsregels weergeven {#list-decision-rules}

Beslissingsregels zijn beperkingen die aan een gepersonaliseerd aanbod worden toegevoegd en die op een profiel worden toegepast om te bepalen of het in aanmerking komt voor een aanbieding. U kunt een lijst met bestaande beslissingsregels in een container weergeven door één GET-aanvraag uit te voeren naar de [!DNL Offer Library] API.

**API formaat**

```http
GET /{ENDPOINT_PATH}/offer-rules?{QUERY_PARAMS}
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
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een succesvolle reactie keert een lijst van besluitvormingsregels terug die u tot hebt toegang.

```json
{
     "results": [
        {
            "created": "2022-09-16T18:59:53.651+00:00",
            "modified": "2022-09-16T18:59:53.651+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerRule1234",
            "name": "Californians with one or more purchases greater than $1000",
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
                 }
        },
        {
            "created": "2023-03-06T15:11:42.178+00:00",
            "modified": "2023-03-06T15:11:42.178+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerRule5678",
            "name": "People born after 1981",
            "description": "Persons with the birth date after 1981",
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "person.birthDate occurs after date(1981, 1, 1)"
            }
        }
    ],
    "count": 2,
    "total": 25,
    "_links": {
        "self": {
            "href": "/offer-rules?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-rules?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
