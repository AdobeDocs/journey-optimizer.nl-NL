---
title: Een verzamelingskwalificatie opzoeken
description: Met de verzamelingskwalificatietags kunt u uw voorstellen beter organiseren en sorteren.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f31e6a17-c99a-4db9-a301-426a1f0bcc92
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 2%

---

# Een verzamelingskwalificatie opzoeken {#look-up-tag}

U kunt specifieke inzamelingsbepalers (die vroeger &quot;markeringen&quot;worden genoemd opzoeken door een GET verzoek aan te richten [!DNL Offer Library] API die de verzamelingskwalificatie bevat `id` in het aanvraagpad.

**API-indeling**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt opzoeken. | `tag1234` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwoord**

Een succesvolle reactie keert de details van de inzamelingsbepaler met inbegrip van informatie over uw unieke inzamelingsbepaler terug `id`.

```json
{
       "created": "2022-09-16T19:00:02.070+00:00",
    "modified": "2022-09-16T19:00:02.070+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "tag1234",
    "name": "Sneakers"
}
```
