---
title: Beslissingsregels verwijderen
description: Beslissingsregels zijn beperkingen die aan een gepersonaliseerd aanbod worden toegevoegd en die op een profiel worden toegepast om te bepalen of het in aanmerking komt voor een aanbieding.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7c02041c-b022-4027-b932-294b207add80
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# Een beslissingsregel verwijderen {#delete-decision-rule}

Het kan soms nodig zijn een beslissingsregel te schrappen (DELETE). Alleen beslissingsregels die u maakt in de huurderscontainer, kunnen worden verwijderd. Dit wordt gedaan door een verzoek van de DELETE aan uit te voeren [!DNL Offer Library] API die instance-id gebruikt van de beslissingsregel die u wilt verwijderen.

**API-indeling**

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

**Antwoord**

Een geslaagde reactie retourneert HTTP-status 202 (Geen inhoud) en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan de besluitvormingsregel te proberen. U zult een Accept- kopbal in het verzoek moeten omvatten, maar zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de besluitregel uit de container is verwijderd.
