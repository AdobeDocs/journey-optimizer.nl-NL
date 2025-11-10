---
title: Extensie-plaatsing bijwerken
description: Uitgebreide plaatsing bestaat uit inzamelingen verbonden aan beperkingen en rangschikkende methodes om aanbiedingen te bepalen.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# Een extra plaatsing bijwerken {#update-exd-placement}

U kunt een plaatsing wijzigen of bijwerken door een PUT-aanvraag in te dienen bij de bibliotheek-API van de aanbieding.

Raadpleeg de officiële documentatie bij JSON PUT voor meer informatie over JSON PUT, inclusief beschikbare activiteiten.

**Accepteer en inhoud-Type kopballen**

In de volgende tabel worden de geldige waarden weergegeven die bestaan uit de velden Inhoudstype in de aanvraagkoptekst:

| Parameter | Beschrijving |
| --------- | ----------- |
| Inhoudstype | `application/json` |

**API formaat**

```http
PUT /{ENDPOINT_PATH}/exd-placements/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt bijwerken. | `placement1234` |

**Verzoek**

```shell
curl --location --request PUT 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19aca09b0a456e57' \
--H 'Content-Type: application/json' \
--H 'x-gw-ims-org-id: {IMS_ORG}' \
--H 'x-sandbox-name: {SANDBOX_NAME}' \
--H 'x-api-key: {API_KEY}' \
--H 'Authorization: Bearer {ACCESS_TOKEN}' \
--X '{
  "id":"dps:exd-placement:19aca09b0a456e57",
  "description": "Keyboard application",
  "status":"archived"
}'
```

| Parameter | Beschrijving |
| --------- | ----------- |
| `value` | De nieuwe waarde waarmee u de parameter wilt bijwerken. |
| `path` | Het pad van de parameter die moet worden bijgewerkt. |
| `op` | De verrichtingsvraag die wordt gebruikt om de actie te bepalen nodig om de verbinding bij te werken. Bewerkingen zijn: `add` , `replace` , `remove` , `copy` en `test` . |

**Reactie**

Een geslaagde reactie retourneert de bijgewerkte details van de exd-plaatsing, inclusief de id.

```json
{
    "etag": 2,
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
