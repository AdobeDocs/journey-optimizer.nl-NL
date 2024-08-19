---
title: Een itemverzameling verwijderen
description: Met verzamelingen kunt u beslissingsitems categoriseren en groeperen op basis van uw voorkeuren.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: dc47e2835379fbb2afb768beea6e4a1596f70ee9
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# Een itemverzameling verwijderen {#delete-decision-item}

Soms is het nodig om een itemverzameling te verwijderen (DELETE). Dit wordt gedaan door een verzoek van de DELETE aan de Bibliotheek API van de Aanbieding uit te voeren gebruikend identiteitskaart van de puntinzameling u wenst om te schrappen.

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

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan de puntinzameling te proberen. U zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de puntinzameling is verwijderd.
