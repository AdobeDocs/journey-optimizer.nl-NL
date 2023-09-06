---
title: Een verzameling maken
description: Verzamelingen zijn subsets van aanbiedingen die zijn gebaseerd op vooraf gedefinieerde voorwaarden die door een marketmaker zijn gedefinieerd, zoals de categorie van de aanbieding.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 683f8b86-8545-46d0-a4a8-25c5b3c7b9c3
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 6%

---

# Een verzameling maken {#create-collection}

Verzamelingen zijn subsets van aanbiedingen die zijn gebaseerd op vooraf gedefinieerde voorwaarden die door een marketmaker zijn gedefinieerd, zoals de categorie van de aanbieding.

U kunt een inzameling tot stand brengen door een verzoek van de POST aan [!DNL Offer Library] API.

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

In de volgende tabel worden de geldige waarden weergegeven waaruit de *Inhoudstype* veld in de aanvraagkoptekst:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Inhoudstype | `application/json` |

**API-indeling**

```http
POST /{ENDPOINT_PATH}/offer-collections
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |

**Verzoek**

```shell
curl -X POST 'https://platform.adobe.io/data/core/offer-collections' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Collection with tags",
    "filterType": "any-tags",
    "ids": [
        "tag1234"
    ],
    "labels": [
        "core/C5",
        "custom/myLabel"
    ]
}'
```

**Antwoord**

Een succesvolle reactie keert informatie over de pas gecreëerde inzameling, met inbegrip van zijn uniek terug `id`. U kunt de verzameling gebruiken `id` in latere stappen om uw verzameling bij te werken of te verwijderen of deze in een latere zelfstudie te gebruiken om een beslissing te maken.

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
