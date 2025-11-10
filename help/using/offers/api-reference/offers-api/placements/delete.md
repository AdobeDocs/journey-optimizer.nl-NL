---
title: plaatsingen verwijderen
description: Plaatsingen zijn containers die worden gebruikt om uw voorstellen te tonen.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# Een plaatsing verwijderen {#delete-placement}

Soms is het nodig om een plaatsing te verwijderen (DELETE). Dit gebeurt door een DELETE-aanvraag naar de [!DNL Offer Library] API uit te voeren met de id van de plaatsing die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/placements/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | De instantie-id van de plaatsing die u wilt bijwerken. | `offerPlacement1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de verwijdering bevestigen door een opzoekaanvraag (GET) naar de plaatsing te proberen en u moet de HTTP-status 404 (Not Found) ontvangen omdat de plaatsing is verwijderd.
