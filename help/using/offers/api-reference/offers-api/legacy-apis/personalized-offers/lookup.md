---
title: Een persoonlijk aanbod opzoeken
description: Een gepersonaliseerd aanbod is een aanpasbaar marketingbericht op basis van geschiktheidsregels en -beperkingen.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 679f2229-19c6-47f9-b293-e1c3c8dcb61e
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Een persoonlijk aanbod opzoeken {#look-up-personalized-offer}

Een gepersonaliseerd aanbod is een aanpasbaar marketingbericht op basis van geschiktheidsregels en -beperkingen.

U kunt omhoog specifieke gepersonaliseerde aanbiedingen kijken door een verzoek van GET aan de **API te doen van de Bibliotheek van de Aanbieding** die of de gepersonaliseerde aanbieding `@id` of de naam van de gepersonaliseerde aanbieding in de verzoekweg omvat.

**API formaat**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PERSONALIZED_OFFER}&{QUERY_PARAMS}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waarin de gepersonaliseerde aanbiedingen zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_PERSONALIZED_OFFER}` | Bepaalt het schema verbonden aan gepersonaliseerde aanbiedingen. | `https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5` |
| `id` | Een tekenreeks die wordt gebruikt om overeen te komen met de eigenschap `@id` van de entiteiten. De tekenreeks komt exact overeen. De parameters &quot;id&quot; en &quot;name&quot; kunnen niet samen worden gebruikt. | `xcore:personalized-offer:124cc332095cfa74` |
| `name` | Een koord dat wordt gebruikt om het xdm :name bezit van de entiteiten aan te passen. De tekenreeks komt exact overeen met hoofdletters, maar er kunnen jokertekens worden gebruikt. De parameters `id` en `name` kunnen niet samen worden gebruikt | `Discount offer` |

**Verzoek**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&name=Discount%20offer' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een succesvol antwoord geeft de details van de plaatsing terug, inclusief informatie over uw container-id, instantie-id en, unieke gepersonaliseerde aanbieding `@id` .

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5",
    "requestTime": "2023-10-21T20:59:16.238585Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2023-10-20T20:01:02.927874Z",
                "repo:lastModifiedDate": "2023-10-20T20:01:02.927874Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Discount offer",
                    "xdm:representations": [
                        {
                            "xdm:components": [
                                {
                                    "dc:language": [
                                        "en"
                                    ],
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-json",
                                    "dc:format": "application/json"
                                }
                            ],
                            "xdm:placement": "xcore:offer-placement:12428d436d87dc84"
                        }
                    ],
                    "xdm:rank": {
                        "xdm:priority": 1
                    },
                    "xdm:selectionConstraint": {
                        "xdm:startDate": "2023-10-01T16:00:00Z",
                        "xdm:endDate": "2021-12-13T16:00:00Z",
                        "xdm:eligibilityRule": "xcore:eligibility-rule:124cb4511da781fc"
                    },
                    "xdm:status": "draft",
                    "xdm:cappingConstraint": {
                        "xdm:globalCap": 150
                    },
                    "xdm:tags": [
                        "xcore:tag:1246d138ec8cca1f"
                    ],
                    "@id": "xcore:personalized-offer:124cc332095cfa74"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5#fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                        "@type": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&name=Discount%20offer",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
