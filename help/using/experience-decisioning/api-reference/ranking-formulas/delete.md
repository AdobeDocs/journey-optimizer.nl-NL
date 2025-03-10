---
title: Een waarderingsformule verwijderen
description: Met behulp van de rangschikkingsformules kunt u de functies voor scoring definiëren, die wordt gebruikt om items te rangschikken.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Een waarderingsformule verwijderen {#delete-selection-strategy}

Het kan soms nodig zijn om (DELETE) een rangschikkingsformule te verwijderen. Dit gebeurt door een DELETE-aanvraag uit te voeren naar de bibliotheek-API van de aanbieding met de id van de rangschikkingsformule die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `rankingFormula1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de verwijdering bevestigen door een opzoekverzoek (GET) in te dienen bij de rangschikkingsformule. U moet de HTTP-status 404 (Niet gevonden) ontvangen omdat de rangschikkingsformule is verwijderd.

