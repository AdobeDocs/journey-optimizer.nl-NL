---
title: Beslissingsregels bijwerken
description: Beslissingsregels zijn beperkingen die aan een gepersonaliseerd aanbod worden toegevoegd en die op een profiel worden toegepast om te bepalen of het in aanmerking komt voor een aanbieding.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 33da2c42-0c6c-49d3-bad8-1a85a5172cd8
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 5%

---

# Een beslissingsregel bijwerken {#update-decision-rule}

U kunt een fallback-aanbieding maken door een POST aan de [!DNL Offer Library] API, terwijl het verstrekken van uw container identiteitskaart

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

In de volgende tabel worden de geldige waarden weergegeven waaruit de *Inhoudstype* en *Accepteren* velden in de aanvraagkoptekst:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Accepteren | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Inhoudstype | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"` |

**API-indeling**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waarin de beslissingsregels zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | De instance-id van de beslissingsregel die u wilt bijwerken. | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**Verzoek**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
        "op": "replace",
        "path": "/_instance/xdm:name",
        "value": "Sales and discounts rule"
        }
    ]'
```

**Antwoord**

Een geslaagde reactie retourneert de bijgewerkte details van de beslissingsregel, inclusief de unieke instantie-id en beslissingsregel `@id`.


```json
{
    "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b",
    "repo:etag": 2,
    "repo:createdDate": "2023-10-21T20:13:43.048666Z",
    "repo:lastModifiedDate": "2023-10-21T20:25:43.705861Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
