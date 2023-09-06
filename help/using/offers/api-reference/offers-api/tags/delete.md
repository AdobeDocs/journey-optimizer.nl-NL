---
title: Verzamelingsaanduidingen verwijderen
description: Met de verzamelingskwalificatietags kunt u uw voorstellen beter organiseren en sorteren.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: ccc3ad2b186a64b9859a5cc529fe0aefa736fc00
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# Een verzamelingskwalificatie verwijderen {#delete-tag}

Het kan soms nodig zijn om (DELETE) een verzamelingskwalificatie (voorheen bekend als &quot;tag&quot;) te verwijderen. Alleen verzamelingsaanduidingen die u in de huurderscontainer maakt, kunnen worden verwijderd. Dit wordt gedaan door een verzoek van de DELETE aan uit te voeren [!DNL Offer Library] API die $id gebruikt van de inzamelingskwalificatie u wenst om te schrappen.

**API-indeling**

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

**Antwoord**

Een geslaagde reactie retourneert HTTP-status 202 (Geen inhoud) en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan het inzamelingsbepaler te proberen. U zult een Accept- kopbal in het verzoek moeten omvatten, maar zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat het inzamelingsbepalende karakter uit de container is verwijderd.
