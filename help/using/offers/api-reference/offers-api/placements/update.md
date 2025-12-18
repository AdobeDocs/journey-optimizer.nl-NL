---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: een plaatsing bijwerken
description: Plaatsingen zijn containers die worden gebruikt om uw voorstellen te tonen.
feature: Decision Management, API
badge: label="Verouderd" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 6990918c-e736-4f28-9ac6-9ac3101b069f
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 4%

---

# Een plaatsing bijwerken {#update-placement}

>[!TIP]
>
>Het besluit, de nieuwe beslissingsmogelijkheden van [!DNL Adobe Journey Optimizer], is nu beschikbaar via de op code gebaseerde ervaring en e-mailkanalen! [Meer informatie](../../../../experience-decisioning/gs-experience-decisioning.md)


U kunt een plaatsing wijzigen of bijwerken door een PATCH-aanvraag in te dienen bij de [!DNL Offer Library] API.

Voor meer informatie over Reparatie JSON, met inbegrip van beschikbare verrichtingen, zie de officiële [&#x200B; documentatie van het Reparatie JSON &#x200B;](https://jsonpatch.com/).

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

De volgende lijst toont de geldige waarden die uit het *inhoud-Type* gebied in de verzoekkopbal bestaan:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Inhoudstype | `application/json` |

**API formaat**

```http
PATCH /{ENDPOINT_PATH}/placements/{ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | De id van de entiteit die u wilt bijwerken. | `offerPlacement1234` |

**Verzoek**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated placement"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated placement description"
    }
]'
```

| Parameter | Beschrijving |
| --------- | ----------- |
| `op` | De verrichtingsvraag die wordt gebruikt om de actie te bepalen nodig om de verbinding bij te werken. Bewerkingen zijn: `add` , `replace` , `remove` , `copy` en `test` . |
| `path` | Het pad van de parameter die moet worden bijgewerkt. |
| `value` | De nieuwe waarde waarmee u de parameter wilt bijwerken. |

**Reactie**

Een geslaagde reactie retourneert de bijgewerkte details van de plaatsing, inclusief de unieke plaatsing `id` .

```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
