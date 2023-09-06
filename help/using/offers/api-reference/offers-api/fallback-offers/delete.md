---
title: Een alternatieve aanbieding verwijderen
description: Aan klanten wordt een fallback-aanbieding gestuurd als zij niet in aanmerking komen voor andere aanbiedingen
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
source-git-commit: e8fe3ffd936c4954e8b17f58f1a2628bea0e2e79
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 8%

---

# Een alternatieve aanbieding verwijderen {#delete-fallback-offer}

Het kan soms nodig zijn om (DELETE) een fallback-aanbieding te verwijderen. Dit wordt gedaan door een verzoek van de DELETE aan uit te voeren [!DNL Offer Library] API die de id van de fallback-aanbieding gebruikt die u wilt verwijderen.

**API-indeling**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `fallbackOffer1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwoord**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan de aanbieding te proberen en zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de reserveaanbieding is verwijderd.
