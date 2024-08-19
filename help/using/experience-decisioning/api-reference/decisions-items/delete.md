---
title: Een beslissingsitem verwijderen
description: Beslissingsitems zijn marketingaanbiedingen die u kunt maken en indelen in verzamelingen en catalogi.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: c555e6a6d88f43d7c29e27060d464b8fd21aed96
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# Een beslissingsitem verwijderen {#delete-decision-item}

Het kan soms nodig zijn een beslissing te verwijderen (DELETE). Dit wordt gedaan door een verzoek van DELETE aan de Bibliotheek API van de Aanbieding uit te voeren gebruikend identiteitskaart van het besluitvormingspunt u wenst om te schrappen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `offerItem1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan het besluitpunt te proberen. U zou HTTP status 404 (niet Gevonden) moeten ontvangen omdat het besluitpunt is verwijderd.
