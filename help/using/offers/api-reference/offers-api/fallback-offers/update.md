---
title: Een alternatieve aanbieding bijwerken
description: Aan klanten wordt een fallback-aanbieding gestuurd als zij niet in aanmerking komen voor andere aanbiedingen
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7ff69887-620f-4bc0-b8ff-5144ff30696c
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 7%

---

# Een alternatieve aanbieding bijwerken {#update-fallback-offer}

U kunt een fallback-aanbieding in uw container wijzigen of bijwerken door een PATCH-aanvraag in te dienen bij de [!DNL Offer Library] API.

Raadpleeg voor meer informatie over JSON Patch, inclusief beschikbare bewerkingen, de officiële [JSON-patchdocumentatie](http://jsonpatch.com/).

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

In de volgende tabel worden de geldige waarden weergegeven waaruit de *Inhoudstype* en *Accepteren* velden in de aanvraagkoptekst:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Accepteren | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Inhoudstype | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"` |

**API-indeling**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waar de reserveaanbiedingen worden gevestigd. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | De instantie-id van de fallback-aanbieding. | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**Verzoek**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
            "op": "replace",
            "path": "/_instance/xdm:status",
            "value": "approved"
        }
    ]
```

| Parameter | Beschrijving |
| --------- | ----------- |
| `op` | De verrichtingsvraag die wordt gebruikt om de actie te bepalen nodig om de verbinding bij te werken. Bewerkingen omvatten: `add`, `replace`, en `remove`. |
| `path` | Het pad van de parameter die moet worden bijgewerkt. |
| `value` | De nieuwe waarde waarmee u de parameter wilt bijwerken. |

**Antwoord**

Een succesvolle reactie retourneert de bijgewerkte details van de fallback-aanbieding, inclusief de unieke instantie-id en de fallback-aanbieding `@id`.

```json
{
    "instanceId": "b3966680-13ec-11eb-9c20-8323709cfc65",
    "@id": "xcore:fallback-offer:124e2e764b1ac1b9",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T22:28:11.111732Z",
    "repo:lastModifiedDate": "2020-10-21T22:33:08.676919Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
