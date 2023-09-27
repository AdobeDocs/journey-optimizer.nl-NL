---
title: Een plaatsing maken
description: Plaatsingen zijn containers die worden gebruikt om uw voorstellen te tonen.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7b735873-86f5-466f-b079-5e84d9f03a08
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 8%

---

# Een plaatsing maken {#create-placement}

U kunt een plaatsing tot stand brengen door een verzoek van de POST aan [!DNL Offer Library] API.

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

In de volgende tabel worden de geldige waarden weergegeven waaruit de *Inhoudstype* veld in de aanvraagkoptekst:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Inhoudstype | `application/json` |

**API-indeling**

```http
POST /{ENDPOINT_PATH}/placements
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |

**Verzoek**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/placements' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "New placement",
    "description": "Placement description",
    "componentType": "html",
    "channel": "https://ns.adobe.com/xdm/channel-types/email",
    "itemCount": 1,
    "allowDuplicatePlacements": false,
    "returnContent": true,
    "returnMetaData": {
        "decisionName": false,
        "offerName": false,
        "offerAttributes": false,
        "offerPriority": false,
        "placementName": false,
        "channelType": false,
        "contentType": false
    }
}'
```

**Antwoord**

Een geslaagde reactie retourneert de details van de nieuwe plaatsing en plaatsing `id`. U kunt de volgende stappen gebruiken om uw plaatsing bij te werken of te verwijderen. U kunt uw unieke plaatsing gebruiken `id` in recentere zelfstudies om besluiten, besluitvormingsregels, en reserveaanbiedingen tot stand te brengen.

```json
{
    "etag": 1,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
