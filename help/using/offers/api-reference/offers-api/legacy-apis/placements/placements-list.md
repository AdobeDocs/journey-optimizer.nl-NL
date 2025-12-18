---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Plaatsingen weergeven
description: Plaatsingen zijn containers die worden gebruikt om uw voorstellen te tonen.
feature: Decision Management, API
badge: label="Verouderd" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 52fbf683-d86f-43c6-be1a-c06141b64b16
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 2%

---

# Plaatsingen weergeven {#list-placements}

>[!TIP]
>
>Het besluit, de nieuwe beslissingsmogelijkheden van [!DNL Adobe Journey Optimizer], is nu beschikbaar via de op code gebaseerde ervaring en e-mailkanalen! [Meer informatie](../../../../../experience-decisioning/gs-experience-decisioning.md)


Plaatsingen zijn containers die worden gebruikt om uw voorstellen te tonen. Een plaatsing helpt ervoor te zorgen dat de juiste aanbiedingsinhoud op de juiste plaats binnen uw bericht verschijnt. Wanneer u inhoud aan een aanbieding toevoegt, wordt u gevraagd een plaatsing te selecteren waarin die inhoud kan worden weergegeven.

U kunt een lijst weergeven met alle plaatsen in een container door één GET-aanvraag uit te voeren voor de [!DNL Offer Library] API.

**API formaat**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PLACEMENT}&{QUERY_PARAMS}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waarin de plaatsingen zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `SCHEMA_PLACEMENT}` | Bepaalt het schema verbonden aan plaatsingen. | `https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4` |
| `{QUERY_PARAMS}` | Optionele queryparameters om resultaten te filteren op. | `limit=2` |

## Query-parameters gebruiken {#using-query-parameters}

U kunt queryparameters gebruiken om de resultaten te filteren en te pagineren wanneer u bronnen weergeeft.

### Paginering {#paging}

De gemeenschappelijkste vraagparameters voor het pagineren omvatten:

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `q` | Een optionele queryreeks die u wilt zoeken in geselecteerde velden. De querytekenreeks moet in kleine letters worden geschreven en kan worden omgeven door dubbele aanhalingstekens om te voorkomen dat deze wordt verdeeld en om speciale tekens te vermijden. De tekens `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` hebben een speciale betekenis en moeten met een backslash worden beschermd wanneer deze in de queryreeks worden weergegeven. | Website JSON |
| `qop` | Past EN of OF exploitant op waarden in q vraagkoordparam toe. | `AND` / `OR` |
| `field` | Optionele lijst met velden waarop u wilt zoeken. Deze param kan als zo worden herhaald: field=field1 [, field=field2,... ] en (de weguitdrukkingen zijn in de vorm van punt gescheiden wegen zoals _instance.xdm :name) | `_instance.xdm:name` |
| `orderBy` | Resultaten sorteren op een bepaalde eigenschap. Als u een `-` vóór titel (`orderby=-title` ) toevoegt, worden items op titel gesorteerd in aflopende volgorde (Z-A). | `-repo:createdDate` |
| `limit` | Beperk het aantal geretourneerde plaatsen. | `limit=5` |

**Verzoek**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2' \
  -H 'Accept: *,application/json' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een succesvolle reactie keert een lijst van plaatsen terug die binnen de container aanwezig zijn u toegang tot hebt.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4",
    "requestTime": "2023-10-21T19:48:51.843067Z",
    "_embedded": {
    "results": [
        {
                "instanceId": "0feb6a80-0f32-11eb-8110-e17787c335b5",
            "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
            ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2023-10-15T22:02:05.480449Z",
                "repo:lastModifiedDate": "2023-10-15T22:13:00.278175Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "New placement name",
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "xdm:description": "Updated placement description",
                    "@id": "xcore:offer-placement:12466ef35fc5baa0"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
            }
        },
        {
                "instanceId": "269192b0-f8f2-11ea-8723-916b9fbadc53",
            "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
            ],
                "repo:etag": 1,
                "repo:createdDate": "2023-09-17T14:29:10.107121Z",
                "repo:lastModifiedDate": "2023-09-17T14:29:10.107121Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:name": "demo placement",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "@id": "xcore:offer-placement:1221fac4e7340521"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
            }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
        }
    ],
        "total": 17,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=269192b0-f8f2-11ea-8723-916b9fbadc53&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
