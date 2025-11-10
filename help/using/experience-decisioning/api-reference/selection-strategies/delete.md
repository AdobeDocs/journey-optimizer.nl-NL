---
title: Een selectiestrategie verwijderen
description: De strategieën van de selectie bestaan uit inzamelingen verbonden aan beperkingen en rangschikkende methodes om aanbiedingen te bepalen.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 774f3773-bc39-46c4-b32c-143abbd45696
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# Een selectiestrategie verwijderen {#delete-selection-strategy}

Het kan soms nodig zijn om (DELETE) een selectiestrategie te verwijderen. Dit gebeurt door een DELETE-aanvraag uit te voeren naar de bibliotheek-API van de aanbieding met de id van de selectiestrategie die u wilt verwijderen.

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

U kunt de verwijdering bevestigen door een opzoekaanvraag (GET) in te dienen bij de selectiestrategie. U ontvangt de HTTP-status 404 (Niet gevonden) omdat de selectiestrategie is verwijderd.
