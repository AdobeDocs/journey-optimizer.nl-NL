---
title: Beslissingsregels verwijderen
description: Beslissingsregels zijn beperkingen die aan een gepersonaliseerd aanbod worden toegevoegd en die op een profiel worden toegepast om te bepalen of het in aanmerking komt voor een aanbieding.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 7c02041c-b022-4027-b932-294b207add80
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 3%

---

# Een beslissingsregel verwijderen {#delete-decision-rule}

Het kan soms nodig zijn om (DELETE) een besluitvormingsregel te schrappen. Alleen beslissingsregels die u maakt in de huurderscontainer, kunnen worden verwijderd. Dit wordt gedaan door een DELETE-aanvraag naar de [!DNL Offer Library] API uit te voeren met behulp van de instantie-id van de beslissingsregel die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waarin de beslissingsregels zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | De instance-id van de beslissingsregel die u wilt bijwerken. | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**Verzoek**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 202 (Geen inhoud) en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan de besluitregel te proberen. U zult een Accept- kopbal in het verzoek moeten omvatten, maar zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de besluitregel uit de container is verwijderd.
