---
title: Een verzamelingskwalificatie maken
description: Met de verzamelingskwalificatietags kunt u uw voorstellen beter organiseren en sorteren.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 84f0efa5-28af-4569-994c-12d87828a277
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 1%

---

# Een verzamelingskwalificatie maken {#create-tag}

U kunt een kwalificatie voor een verzameling maken (voorheen bekend als &#39;tag&#39;) door een POST-aanvraag in te dienen bij de [!DNL Offer Library] -API en uw container-id op te geven.

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

De volgende lijst toont de geldige waarden die uit *inhoud-Type* bestaan en ** gebieden in de verzoekkopbal goedkeuren:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Accepteren | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Inhoudstype | `application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"` |

**API formaat**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waar de inzamelingsbepalende eigenschappen worden gevestigd. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Verzoek**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Holiday sales and promotions"
    }'
```

**Reactie**

Een geslaagde reactie retourneert informatie over de nieuwe verzamelingskwalificatie, inclusief de unieke instantie-id en plaatsing `@id` . U kunt de instantie-id in latere stappen gebruiken om de verzamelingskwalificatie bij te werken of te verwijderen. U kunt uw unieke kwalificatie voor verzamelingen `@id` in latere zelfstudies gebruiken om verzamelingen en persoonlijke aanbiedingen te maken.

```json
{
  "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "@id": "xcore:tag:124e147572cd7866",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T20:34:34.486296Z",
    "repo:lastModifiedDate": "2023-10-21T20:34:34.486296Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
