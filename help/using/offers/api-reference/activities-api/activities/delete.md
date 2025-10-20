---
title: Besluiten verwijderen
description: Een beslissing bevat de logica die de selectie van een aanbieding informeert.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# Een beslissing verwijderen {#delete-decision}

Het kan soms nodig zijn een beslissing te verwijderen (DELETE). Dit gebeurt door een DELETE-aanvraag naar de [!DNL Offer Library] API uit te voeren met behulp van `id` van de beslissing die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `offerDecision1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de verwijdering bevestigen door een opzoekverzoek (GET) in te dienen bij de beslissing. U moet de HTTP-status 404 (Niet gevonden) ontvangen omdat de beslissing is verwijderd.
