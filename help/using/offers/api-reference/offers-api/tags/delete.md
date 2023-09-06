---
title: Verzamelingsaanduidingen verwijderen
description: Met de verzamelingskwalificatietags kunt u uw voorstellen beter organiseren en sorteren.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: e8fe3ffd936c4954e8b17f58f1a2628bea0e2e79
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---

# Een verzamelingskwalificatie verwijderen {#delete-tag}

Het kan soms nodig zijn om (DELETE) een verzamelingskwalificatie (voorheen bekend als &quot;tag&quot;) te verwijderen. Dit wordt gedaan door een verzoek van de DELETE aan uit te voeren [!DNL Offer Library] API gebruikt de id van de verzamelingskwalificatie die u wilt verwijderen.

**API-indeling**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `tag1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwoord**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan het inzamelingsbepaler te proberen en zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat het is verwijderd.
