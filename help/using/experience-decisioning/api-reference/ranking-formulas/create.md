---
title: Een waarderingsformule maken
description: Met behulp van de rangschikkingsformules kunt u de functies voor scoring definiëren, die wordt gebruikt om items te rangschikken.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 2eb3ca65-f9f2-4483-ac6a-7bd896b0e516
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---

# Een waarderingsformule maken {#create-ranking-formula}

U kunt een rangschikkingsformule tot stand brengen door een POST- verzoek aan de Bibliotheek API van de Aanbieding te doen.

**Accepteer en inhoud-Type kopballen**

In de volgende tabel worden de geldige waarden weergegeven die bestaan uit de velden Inhoudstype in de aanvraagkoptekst:

| Naam koptekst | Waarde |
| --------- | ----------- | 
| Inhoudstype | application/json |

**API formaat**

```http
POST /{ENDPOINT_PATH}/ranking-formulas 
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |

**Verzoek**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/ranking-formulas' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Ranking Function DPS",
    "description": "Ranking  function description",
    "exdFunction": true,
    "returnType": {
        "type": "integer"
    },
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "if(offer.rank.priority.isNotNull(), offer.rank.priority, 0) * if(offer.tags.intersects(boosted.tags), 2, 1)"
    },
    "definedOn": {
        "offer": {
            "schema": {
                "altId": "_experience.offer-management.personalized-offer",
                "version": "0"
            }
        },
        "boosted": {
            "schema": {
                "altId": "_xdm.context.foo",
                "version": "0"
            }
        }
    }
}'
```

**Reactie**

Een succesvol antwoord retourneert de details van de zojuist gemaakte waarderingsformule inclusief de `id` . U kunt `id` in recentere stappen gebruiken om uw het rangschikken formule bij te werken of te schrappen.

```json
{
    "etag": 1,
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
