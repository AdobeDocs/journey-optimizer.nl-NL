---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Aangepaste aanbiedingen verwijderen
description: Een gepersonaliseerd aanbod is een aanpasbaar marketingbericht op basis van geschiktheidsregels en -beperkingen.
feature: Decision Management, API
badge: label="Verouderd" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---

# Een persoonlijke aanbieding verwijderen {#delete-personalized-offer}

>[!TIP]
>
>Het besluit, de nieuwe beslissingsmogelijkheden van [!DNL Adobe Journey Optimizer], is nu beschikbaar via de op code gebaseerde ervaring en e-mailkanalen! [Meer informatie](../../../../experience-decisioning/gs-experience-decisioning.md)


Het kan soms nodig zijn om (DELETE) een gepersonaliseerd aanbod te verwijderen. Dit gebeurt door een DELETE-aanvraag naar de [!DNL Offer Library] API uit te voeren met de id van de persoonlijke aanbieding die u wilt verwijderen.

**API formaat**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | De id van de entiteit die u wilt verwijderen. | `personalizedOffer1234` |

**Verzoek**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reactie**

Een geslaagde reactie retourneert HTTP-status 200 en een lege hoofdtekst.

U kunt de schrapping bevestigen door een raadpleging (GET) verzoek aan gepersonaliseerde-aanbieding te proberen en zou een status 404 van HTTP (niet Gevonden) moeten ontvangen omdat de gepersonaliseerde-aanbieding is verwijderd.
