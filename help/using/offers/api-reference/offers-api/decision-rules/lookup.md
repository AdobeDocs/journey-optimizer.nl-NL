---
title: Beslissingsregel opzoeken
description: Beslissingsregels zijn beperkingen die aan een gepersonaliseerd aanbod worden toegevoegd en die op een profiel worden toegepast om te bepalen of het in aanmerking komt voor een aanbieding.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 54368710-1021-43c0-87b7-5176cc6c72f7
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# Beslissingsregel opzoeken {#lookup-decision-rule}
U kunt een specifieke besluitvormingsregel opzoeken door een verzoek van de GET tot de [!DNL Offer Library] API die de beslissingsregel bevat `id` in het aanvraagpad.

**API-indeling**

```http
GET /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | De id van de entiteit die u wilt opzoeken. | `offerRule1234` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwoord**

Een succesvolle reactie keert de details van de specifieke besluitvormingsregel terug u omhoog keek, met inbegrip van informatie over zijn unieke beslissingsregel `@id`.

```json
  {
    "created": "2022-09-16T18:59:53.651+00:00",
    "modified": "2022-09-16T18:59:53.651+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerRule1234",
    "name": "Californians with one or more purchases greater than $1000",
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
    }
}
```
