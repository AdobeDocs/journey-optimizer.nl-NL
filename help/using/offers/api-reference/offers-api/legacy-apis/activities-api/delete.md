---
title: Besluiten verwijderen
description: Een beslissing bevat de logica die de selectie van een aanbieding informeert.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 36a87d98-fd61-416e-83a1-e267a7b4d455
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 2%

---

# Een beslissing verwijderen {#delete-decision}

Het kan soms nodig zijn een beslissing te verwijderen (DELETE). Slechts kunnen de besluiten die u in de huurderscontainer creeert worden geschrapt. Dit gebeurt door een DELETE-aanvraag naar de [!DNL Offer Library] API uit te voeren met behulp van $id van de fallback-aanbieding die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waarin de beslissingen zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | De zaak-id van de beslissing. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**Verzoek**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 202 (Geen inhoud) en een lege hoofdtekst.

U kunt de verwijdering bevestigen door een opzoekverzoek (GET) in te dienen bij de beslissing. U zult een Accept- kopbal in het verzoek moeten omvatten, maar zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat het besluit uit de container is verwijderd.
