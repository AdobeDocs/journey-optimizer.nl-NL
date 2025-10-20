---
title: Een extra plaatsing opzoeken
description: Uitgebreide plaatsing bestaat uit inzamelingen verbonden aan beperkingen en rangschikkende methodes om aanbiedingen te bepalen.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---

# Een extra plaatsing opzoeken {#list-exd-placement}

U kunt specifieke exportmogelijkheden opzoeken door een GET-aanvraag in te dienen bij de API voor de aanbiedingsbibliotheek die de id bevat in het aanvraagpad.

**API formaat**

```http
GET /{ENDPOINT_PATH}/exd-placements/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt opzoeken. | `placement1234` |

**Verzoek**

```shell
curl --location 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19c5fa7448c6fcab' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}'
```

**Reactie**

Een geslaagde reactie retourneert de details van de exd-plaatsing.

```json
{
    "created": "2024-11-14T20:56:45.540Z",
    "modified": "2024-11-14T20:56:45.540Z",
    "etag": 1,
    "schemas": [
        "exd-placement"
    ],
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "id": "dps:exd-placement:19c5fa7448c6fcab",
    "name": "Test Exd Placement1 Car",
    "description": "brand panel",
    "tags": [
        "3d75b849-b344-402b-9d9e-5d750bd46884"
    ],
    "channel": "https://ns.adobe.com/xdm/channel-types/email",
    "channelConfiguration": "530b76f9-dcd6-4fd5-8c52-38e29b04a60a",
    "status": "active"
}            
```
