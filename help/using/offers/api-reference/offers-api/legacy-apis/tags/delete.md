---
title: Verzamelingsaanduidingen verwijderen
description: Met de verzamelingskwalificatietags kunt u uw voorstellen beter organiseren en sorteren.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: cc67519e-7a80-49c7-8c8b-c777be633026
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# Een verzamelingskwalificatie verwijderen {#delete-tag}

Het kan soms nodig zijn om (DELETE) een verzamelingskwalificatie (voorheen &quot;tag&quot; genoemd) te verwijderen. Alleen verzamelingsaanduidingen die u in de huurderscontainer maakt, kunnen worden verwijderd. Dit wordt gedaan door een DELETE-aanvraag naar de [!DNL Offer Library] API uit te voeren met behulp van $id van de verzamelingskwalificatie die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waar de inzamelingsbepalende eigenschappen worden gevestigd. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | De instantie-id van de verzamelingskwalificatie die u wilt bijwerken. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**Verzoek**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 202 (Geen inhoud) en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan het inzamelingsbepaler te proberen. U zult een Accept- kopbal in het verzoek moeten omvatten, maar zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat het inzamelingsbepalende karakter uit de container is verwijderd.
