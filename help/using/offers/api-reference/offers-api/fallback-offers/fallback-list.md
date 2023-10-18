---
title: Alternatieve aanbiedingen weergeven
description: Aan klanten wordt een fallback-aanbieding gestuurd als zij niet in aanmerking komen voor andere aanbiedingen
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: dd95c040-d905-4f5a-8cc5-58e39082e57e
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 4%

---

# Alternatieve aanbiedingen weergeven {#list-fallback-offers}

Aan klanten wordt een terugvalaanbieding gestuurd als zij niet in aanmerking komen voor andere aanbiedingen. De stappen om een reserveaanbieding tot stand te brengen bestaan uit het creëren van één of verscheidene vertegenwoordiging, zoals wanneer het creëren van een aanbieding.

U kunt een lijst van alle reservevoorstellen bekijken door één enkel verzoek van de GET aan uit te voeren [!DNL Offer Library] API.

**API-indeling**

```http
GET /{ENDPOINT_PATH}/offers?offer-type=fallback&{QUERY_PARAMS}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Optionele queryparameters om resultaten te filteren op. | `limit=2` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers?offer-type=fallback&limit=2' \
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
| `property` | Een optioneel eigenschapsfilter: <ul><li>De eigenschappen worden gegroepeerd door EN-bewerking.</li><li>Parameters kunnen als volgt worden herhaald: property={PROPERTY_EXPR}[&amp;eigenschap={PROPERTY_EXPR2}...] or property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>Eigenschapexpressies hebben een indeling `[!]field[op]value`, met `op` in `[==,!=,<=,>=,<,>,~]`, die reguliere expressies ondersteunen.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Resultaten sorteren op een bepaalde eigenschap. Als u de naam a - before toevoegt (orderby=-name), worden de items op naam gesorteerd in aflopende volgorde (Z-A). Padexpressies hebben de vorm van door punten gescheiden paden. Deze parameter kan als volgt worden herhaald: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Beperk het aantal geretourneerde entiteiten. | `limit=5` |

**Antwoord**

Een succesvolle reactie keert een lijst van reserveaanbiedingen terug die u toegang tot hebt.

```json
{
      "results": [
        {
            "created": "2023-06-08T14:04:41.011+00:00",
            "modified": "2023-06-08T14:04:41.011+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "fallbackOffer1234",
            "name": "Fallback Offer Web",
            "description": "Fallback Offer Web Description",
            "status": "draft",
            "representations": [
                {
                    "channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "placement": "offerPlacement5678",
                    "components": [
                        {
                            "type": "imagelink",
                            "format": "image/png",
                            "deliveryURL": "https://mysite.com"
                        }
                    ]
                }
            ]
        },
        {
            "created": "2022-10-07T11:23:55.885+00:00",
            "modified": "2022-10-07T11:23:55.885+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.7"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "fallbackOffer5678",
            "name": "Fallback Offer email",
            "status": "approved",
            "representations": [
                {
                    "channel": "https://ns.adobe.com/xdm/channel-types/email",
                    "placement": "offerPlacement1234",
                    "components": [
                        {
                            "type": "component-text",
                            "format": "text/template",
                            "content": "Get free shipping!"
                        }
                    ]
                }
            ],
            "labels": [
                "core/C1"
            ]
        }
    ],
    "count": 2,
    "total": 3,
    "_links": {
        "self": {
            "href": "/offers?offer-type=fallback&href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offers?offer-type=fallback&href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
