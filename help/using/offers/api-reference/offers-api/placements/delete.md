---
title: plaatsingen verwijderen
description: Plaatsingen zijn containers die worden gebruikt om uw voorstellen te tonen.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 4%

---

# Een plaatsing verwijderen {#delete-placement}

Het kan soms nodig zijn om een plaatsing te verwijderen (DELETE). Dit wordt gedaan door een verzoek van de DELETE aan uit te voeren [!DNL Offer Library] API die identiteitskaart van de plaatsing gebruikt u wenst om te schrappen.

**API-indeling**

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

**Antwoord**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan de plaatsing te proberen en zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de plaatsing is verwijderd.
