---
title: Aangepaste aanbiedingen verwijderen
description: Een gepersonaliseerd aanbod is een aanpasbaar marketingbericht op basis van geschiktheidsregels en -beperkingen.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---

# Een persoonlijke aanbieding verwijderen {#delete-personalized-offer}

Het kan soms nodig zijn om (DELETE) een gepersonaliseerd aanbod te verwijderen. Dit gebeurt door een DELETE-aanvraag naar de [!DNL Offer Library] API uit te voeren met de id van de persoonlijke aanbieding die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `personalizedOffer1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan gepersonaliseerde-aanbieding te proberen en zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de gepersonaliseerde-aanbieding is verwijderd.
