---
title: Een verzameling verwijderen
description: Verzamelingen zijn subsets van aanbiedingen die zijn gebaseerd op vooraf gedefinieerde voorwaarden die door een marketmaker zijn gedefinieerd, zoals de categorie van de aanbieding.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---

# Een verzameling verwijderen {#delete-collection}

Het kan soms nodig zijn om (DELETE) een collectie te verwijderen. Dit gebeurt door een DELETE-aanvraag naar de [!DNL Offer Library] API uit te voeren met behulp van `id` van de verzameling die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/offer-collections/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `offerCollection1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' 
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de verwijdering bevestigen door een opzoekverzoek (GET) in te dienen bij de verzameling. U zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de inzameling is verwijderd.
