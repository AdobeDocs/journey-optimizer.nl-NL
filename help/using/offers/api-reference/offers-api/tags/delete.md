---
title: Verzamelingsaanduidingen verwijderen
description: Met de verzamelingskwalificatietags kunt u uw voorstellen beter organiseren en sorteren.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# Een verzamelingskwalificatie verwijderen {#delete-tag}

Het kan soms nodig zijn om (DELETE) een verzamelingskwalificatie (voorheen &quot;tag&quot; genoemd) te verwijderen. Dit wordt gedaan door een DELETE- verzoek aan de Bibliotheek API van de Aanbieding uit te voeren gebruikend identiteitskaart van de inzamelingskwalificatie u wenst om te schrappen.

**API formaat**

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

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan het inzamelingsbepaler te proberen. U zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de inzamelingskwalificatie is verwijderd.