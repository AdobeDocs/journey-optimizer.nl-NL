---
title: Beslissingen weergeven
description: Een beslissing bevat de logica die de selectie van een aanbieding informeert.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 123ed057-e15f-4110-9fc6-df0e9cb5b038
source-git-commit: 5fa3c0c39de43450b199a41c4a4a032674dd4887
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 3%

---

# Beslissingen weergeven {#list-decisions}

Een beslissing bevat de logica die de selectie van een aanbieding informeert.

U kunt een lijst van alle besluiten binnen een container bekijken door één enkel verzoek van de GET aan uit te voeren [!DNL Offer Library] API.

**API-indeling**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ACTIVITIES}&{QUERY_PARAMS}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waarin de beslissingen zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ACTIVITIES}` | Bepaalt het schema verbonden aan besluiten. | `https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5` |
| `{QUERY_PARAMS}` | Optionele queryparameters om resultaten te filteren op. | `limit=2` |

**Verzoek**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
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
| `q` | Een optionele queryreeks die u wilt zoeken in geselecteerde velden. De querytekenreeks moet in kleine letters worden geschreven en kan worden omgeven door dubbele aanhalingstekens om te voorkomen dat deze wordt verdeeld en om speciale tekens te vermijden. De tekens `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` hebben een speciale betekenis en moeten met een backslash worden beschermd wanneer deze in de queryreeks wordt weergegeven. | `default` |
| `qop` | Past EN of OF exploitant op waarden in q vraagkoordparam toe. | `AND` / `OR` |
| `field` | Optionele lijst met velden waarop u wilt zoeken. Deze param kan als zo worden herhaald: field=field1[,field=field2,...] en (padexpressies hebben de vorm van door punten gescheiden paden, zoals _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Resultaten sorteren op een bepaalde eigenschap. Een `-` vóór titel (`orderby=-title`) sorteert objecten op titel in aflopende volgorde (Z-A). | `-repo:createdDate` |
| `limit` | Beperk het aantal geretourneerde beslissingen. | `limit=5` |

**Antwoord**

Een succesvolle reactie keert een lijst van besluiten terug die binnen de container aanwezig zijn u toegang tot hebt.

```json
{
    "results": [
        {
            "created": "2022-07-05T09:02:02.835+00:00",
            "modified": "2022-08-16T21:40:58.573+00:00",
            "etag": 12,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerDecision1234",
            "name": "Test Decision One",
            "status": "live",
            "startDate": "2022-05-18T00:09:57.706+00:00",
            "endDate": "2032-08-13T21:40:58.235+00:00",
            "fallback": "fallbackOffer1234",
            "criteria": [
                {
                    "placements": [
                        "offerPlacement1234",
                        "offerPlacement5678"
                    ],
                    "rank": {
                        "priority": 0,
                        "order": {
                            "orderEvaluationType": "ranking-strategy",
                            "rankingStrategy": "123456789123"
                        }
                    },
                    "profileConstraint": {
                        "profileConstraintType": "none"
                    },
                    "optionSelection": {
                        "filter": "offerCollection1234"
                    }
                }
            ]
        },
        {
            "created": "2022-09-05T14:12:13.773+00:00",
            "modified": "2022-09-05T14:12:13.773+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerDecision5678",
            "name": "Test Decision Two",
            "status": "live",
            "startDate": "2022-08-31T21:00:00.000+00:00",
            "endDate": "2023-02-03T22:00:00.000+00:00",
            "fallback": "fallbackOffer5678",
            "criteria": [
                {
                    "placements": [
                        "offerPlacement1234"
                    ],
                    "rank": {
                        "priority": 2
                    },
                    "optionSelection": {
                        "filter": "offerCollection5678"
                    }
                },
                {
                    "placements": [
                        "offerPlacement5678"
                    ],
                    "rank": {
                        "priority": 1
                    },
                    "optionSelection": {
                        "filter": "offerCollection1234"
                    }
                }          
            ]
        }
    ],
    "count": 2,
    "total": 21,
    "_links": {
        "self": {
            "href": "/offer-decisions?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-decisions?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
