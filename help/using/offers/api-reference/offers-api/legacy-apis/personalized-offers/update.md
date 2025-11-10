---
title: Aangepaste aanbiedingen bijwerken
description: Een gepersonaliseerd aanbod is een aanpasbaar marketingbericht op basis van geschiktheidsregels en -beperkingen.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ef785c6-06b4-40ce-a8e5-6a9d5101a408
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---

# Een persoonlijke aanbieding bijwerken {#update-personalized-offer}

U kunt een gepersonaliseerde aanbieding wijzigen of bijwerken door een PATCH-aanvraag in te dienen bij de [!DNL Offer Library] API

Voor meer informatie over Reparatie JSON, met inbegrip van beschikbare verrichtingen, zie de officiële [ documentatie van het Reparatie JSON ](https://jsonpatch.com/).

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

De volgende lijst toont de geldige waarden die uit *inhoud-Type* bestaan en ** gebieden in de verzoekkopbal goedkeuren:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Accepteren | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Inhoudstype | `Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**API formaat**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waarin de gepersonaliseerde aanbiedingen zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Verzoek**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0f4bc230-13df-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
            "op": "add",
            "path": "/_instance/xdm:representations/-",
            "value": {
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3",
                "xdm:components": [
    {
                        "@type": "https://ns.adobe.com/experience/offer-management/content-component-text",
                        "dc:format": "text/plain",
                        "dc:language": ["en"],
                        "xdm:content": "Here is your first sale offer!"
                    }
                ]
            }
    }
]'
```

| Parameter | Beschrijving |
| --------- | ----------- |
| `op` | De verrichtingsvraag die wordt gebruikt om de actie te bepalen nodig om de verbinding bij te werken. Bewerkingen zijn: `add` , `replace` en `remove` . |
| `path` | Het pad van de parameter die moet worden bijgewerkt. |
| `value` | De nieuwe waarde waarmee u de parameter wilt bijwerken. |

**Reactie**

Een geslaagde reactie retourneert de bijgewerkte gegevens van de persoonlijke aanbieding, inclusief `id` .

```json
{
    "instanceId": "0f4bc230-13df-11eb-bc55-c11be7252432",
    "@id": "xcore:personalized-offer:124e181c8b0d7878",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T20:50:32.018624Z",
    "repo:lastModifiedDate": "2023-10-21T20:50:32.018624Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
