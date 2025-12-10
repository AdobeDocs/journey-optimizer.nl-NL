---
title: Een itemverzameling verwijderen
description: Leer hoe u groepsbeslissingen kunt indelen in verzamelingen.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 7290c857-cbc7-4197-ae13-430adcf1649b
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# Een itemverzameling verwijderen {#delete-decision-item}

Soms is het nodig om een objectverzameling te verwijderen (DELETE). Dit gebeurt door een DELETE-aanvraag uit te voeren naar de bibliotheek-API van de aanbieding met de id van de itemverzameling die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/item-collections/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `itemCollections1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de verwijdering bevestigen door een opzoekverzoek (GET) in te dienen bij de itemverzameling. U zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de puntinzameling is verwijderd.
