---
title: Labels verwijderen
description: Met labels kunt u uw voorstellen beter organiseren en doorlopen.
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 3%

---

# Een tag verwijderen

Soms is het nodig om een tag te verwijderen (DELETE). Alleen tags die u maakt in de container van de huurder, kunnen worden verwijderd. Dit wordt gedaan door een verzoek van DELETE aan [!DNL Offer Library] API uit te voeren gebruikend $id van de markering u wenst om te schrappen.

**API-indeling**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waarin de tags zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | De instantie-id van de tag die u wilt bijwerken. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

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

U kunt de verwijdering bevestigen door een opzoekverzoek (GET) in te dienen bij de tag. U moet een header Accept in de aanvraag opnemen, maar u moet de HTTP-status 404 (Niet gevonden) ontvangen omdat de tag uit de container is verwijderd.
