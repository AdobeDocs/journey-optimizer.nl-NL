---
title: Een extra plaatsing maken
description: De strategieën van de uitbreiding bestaan uit inzamelingen verbonden aan beperkingen en rangschikkende methodes om aanbiedingen te bepalen.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---

# Een extra plaatsing maken {#create-exd-placement}

U kunt een externe plaatsing tot stand brengen door een POST- verzoek aan de Bibliotheek API van de Aanbieding te doen.

**Accepteer en inhoud-Type kopballen**

In de volgende tabel worden de geldige waarden weergegeven die bestaan uit de velden Inhoudstype in de aanvraagkoptekst:

| Parameter | Beschrijving |
| --------- | ----------- |
| Inhoudstype | `application/json` |

**API formaat**

```http
POST /{ENDPOINT_PATH}/exd-placements
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |

**Verzoek**

```shell
curl --location 'https://platform-stage.adobe.io/data/core/dps/exd-placements' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}' \
--data '{
  "name": "Test Exd Placement1 Pants",
  "channel": "https://ns.adobe.com/xdm/channel-types/email",
  "tags":["3d75b849-b344-402b-9d9e-5d750bd46884"],
  "channelConfiguration":"530b76f9-dcd6-4fd5-8c52-38e29b04a60a",
  "description": "compressing alarm",
  "status":"active"
}'
```

**Reactie**

Een geslaagde reactie retourneert de details van de zojuist gemaakte exd-plaatsing, inclusief de id. U kunt de id in latere stappen gebruiken om uw exd-plaatsing bij te werken of te verwijderen.

```json
{
    "id": "dps:exd-placement:19cb038eca47bead",
    "sandboxId": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "etag": 2,
    "createdDate": "2024-11-18T18:48:56.298Z",
    "lastModifiedDate": "2024-11-18T18:57:27.457Z",
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedByClientId": "CJMTestClientACP"
}
```
