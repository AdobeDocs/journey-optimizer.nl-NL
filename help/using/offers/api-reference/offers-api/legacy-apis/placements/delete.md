---
title: plaatsingen verwijderen
description: Plaatsingen zijn containers die worden gebruikt om uw voorstellen te tonen.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 944efb12-6745-4bb2-be52-293e23925350
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---

# Een plaatsing verwijderen {#delete-placement}

Soms is het nodig om een plaatsing te verwijderen (DELETE). Alleen de plaatsen die u maakt in de container van de huurder kunnen worden verwijderd. Dit gebeurt door een DELETE-aanvraag uit te voeren naar de [!DNL Offer Library] API met de instantie-id van de plaatsing die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waarin de plaatsingen zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | De instantie-id van de plaatsing die u wilt bijwerken. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Verzoek**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 202 (Geen inhoud) en een lege hoofdtekst.

U kunt de verwijdering bevestigen door een opzoekaanvraag (GET) in te dienen bij de plaatsing. U zult een Accept- kopbal in het verzoek moeten omvatten, maar zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de plaatsing uit de container is verwijderd.
