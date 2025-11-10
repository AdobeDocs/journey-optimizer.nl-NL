---
title: Een toelatingsregel verwijderen
description: Aan de hand van de kwalificatieregels kunt u bepalen welke kandidaten in aanmerking komen op basis van wat u als doel wilt instellen, zoals profielkenmerken en doelgroepen.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 19baf888-23b7-46de-9d3c-9a0fa8ab2297
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# Een toelatingsregel verwijderen {#delete-eligibility-rule}

Het kan soms nodig zijn om (DELETE) een toelatingsregel te schrappen. Dit gebeurt door een DELETE-aanvraag uit te voeren naar de bibliotheek-API van het aanbod met de id van de geschiktheidsregel die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/eligibility-rules/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `rule1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de verwijdering bevestigen door een opzoekverzoek (GET) bij de regel in te dienen. U zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de regel is verwijderd.
