---
title: Een selectiestrategie verwijderen
description: De strategieën van de selectie bestaan uit inzamelingen verbonden aan beperkingen en rangschikkende methodes om aanbiedingen te bepalen.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: c555e6a6d88f43d7c29e27060d464b8fd21aed96
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Een selectiestrategie verwijderen {#delete-selection-strategy}

Soms kan het nodig zijn een selectiestrategie te verwijderen (DELETE). Dit wordt gedaan door een verzoek van DELETE aan de Bibliotheek API van de Aanbieding uit te voeren gebruikend identiteitskaart van de selectiestrategie u wenst om te schrappen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `selectionStrategy1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de verwijdering bevestigen door een opzoekverzoek (GET) in te dienen bij de selectiestrategie. U ontvangt de HTTP-status 404 (Niet gevonden) omdat de selectiestrategie is verwijderd.
