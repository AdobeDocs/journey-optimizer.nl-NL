---
title: Een beslissingsitem verwijderen
description: Beslissingsitems zijn marketingaanbiedingen die u kunt maken en indelen in verzamelingen en catalogi.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 0fd608e0-df71-4e2d-8304-d7d5561c7c7a
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Een beslissingsitem verwijderen {#delete-decision-item}

Als u een beslissingsitem wilt verwijderen, voert u een DELETE-aanvraag uit naar de bibliotheek-API van het aanbod met de id van het beslissingsitem dat u wilt verwijderen.

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

U kunt de verwijdering bevestigen door een opzoekverzoek (GET) in te dienen bij het beslissingsonderdeel. U zou HTTP status 404 (niet Gevonden) moeten ontvangen omdat het besluitpunt is verwijderd.
