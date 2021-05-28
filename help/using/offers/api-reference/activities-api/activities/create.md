---
title: Besluiten maken
description: Een beslissing bevat de logica die de selectie van een aanbieding informeert.
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# Een beslissing maken

U kunt een beslissing (die eerder als aanbiedingsactiviteit wordt bekend) tot stand brengen door een verzoek van de POST aan [!DNL Offer Library] API te richten, terwijl het verstrekken van uw containeridentiteitskaart

## Kopteksten van het type Inhoud accepteren

In de volgende tabel worden de geldige waarden weergegeven die bestaan uit de velden *Content-Type* en *Accept* in de aanvraagkoptekst:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Accepteren | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Inhoudstype | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"` |

**API-indeling**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waarin de beslissingen zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Verzoek**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Activity 1",
        "xdm:startDate": "2020-10-01T16:00:00Z",
        "xdm:endDate": "2021-12-13T16:00:00Z",
        "xdm:status": "live",
        "xdm:criteria": [
            {
                "xdm:placements": [
                    "xcore:offer-placement:122204529514a2c0"
                ],
                "xdm:optionSelection": {
                    "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                }
            }
        ],
        "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef"
    }'
```

**Antwoord**

Een succesvolle reactie retourneert informatie over de nieuwe beslissing, inclusief de unieke instantie-id en plaatsing `@id`. U kunt de instantie-id in latere stappen gebruiken om uw beslissing bij te werken of te verwijderen.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T20:02:09.694067Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
