---
title: Een verzameling verwijderen
description: Verzamelingen zijn subsets van aanbiedingen die zijn gebaseerd op vooraf gedefinieerde voorwaarden die door een marketmaker zijn gedefinieerd, zoals de categorie van de aanbieding.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 6%

---

# Een verzameling verwijderen {#delete-collection}

Het kan soms nodig zijn een verzameling te verwijderen (DELETE). Dit wordt gedaan door een verzoek van de DELETE aan uit te voeren [!DNL Offer Library] API die de `id` van de verzameling die u wilt verwijderen.

**API-indeling**

```http
DELETE /{ENDPOINT_PATH}/offer-collections/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `offerCollection1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwoord**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan de inzameling te proberen. U zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de inzameling is verwijderd.
