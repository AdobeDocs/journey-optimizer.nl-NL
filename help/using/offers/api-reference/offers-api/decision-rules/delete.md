---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Beslissingsregels verwijderen
description: Beslissingsregels zijn beperkingen die aan een gepersonaliseerd aanbod worden toegevoegd en die op een profiel worden toegepast om te bepalen of het in aanmerking komt voor een aanbieding.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 4%

---

# Een beslissingsregel verwijderen {#delete-decision-rule}

Het kan soms nodig zijn om (DELETE) een besluitvormingsregel te schrappen. Dit gebeurt door een DELETE-aanvraag naar de [!DNL Offer Library] API uit te voeren met behulp van `id` van de beslissingsregel die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `offerRule1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan de besluitregel te proberen en zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de besluitregel is verwijderd.
