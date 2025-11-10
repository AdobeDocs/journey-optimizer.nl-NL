---
product: experience platform
solution: Experience Platform
title: Contextgegevens en beslissingsverzoeken
description: Leer hoe u contextgegevens doorgeeft in beslissingsverzoeken.
badge: label="Verouderd" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 45d060ce-0a12-4a6e-a594-ec10cdff8f38
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Contextgegevens en beslissingsverzoeken {#context-data-decisioning}

Deze sectie begeleidt u door contextgegevens in Beslissingsverzoeken over te gaan en hen in kwalificatieregels te gebruiken.

>[!BEGINSHADEBOX]

Om verder te gaan, kunt u hefboomcontext in **het rangschikken formules** ook gebruiken om uw aanbiedingen op te voeren. De gedetailleerde voorbeelden van het rangschikken formules leveraging contextgegevens zijn beschikbaar in [ deze sectie ](../offers/ranking/create-ranking-formulas.md#context-data).

>[!ENDSHADEBOX]

## Contextgegevens in beslissingsverzoeken doorgeven

Contextgegevens in beslissingsverzoeken worden gedefinieerd met behulp van de sleutel: `xdm:ContextData` .

De attributen van contextgegevens worden niet gedreven door XDM schema. U kunt om het even welke contextgegevens in JSON als deel van het Beslissingsverzoeklading overgaan.

Hier volgt een voorbeeld van een verzoek tot besluitvorming met contextgegevens (zie `xdm:ContextData`):

```
curl --location 'https://platform-stage.adobe.io/data/core/ods/decisions' \
--header 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
--header 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
--header 'Authorization: Bearer eyJhbGciOi....' \
--header 'x-api-key: {{api_key}}' \
--header 'x-gw-ims-org-id: {{ims_org}}' \
--header 'x-sandbox-name: {{sandbox_name}}' \
--header 'x-request-id: {{$guid}}' \
--data-raw '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:19978bf95ebfc8fb",
            "xdm:placementId": "dps:offer-placement:199772e1c90d50ac"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "test@test.com",
                        "primary": true
                    }
                ]
            },
            "xdm:contextData": [
                {
                    "@type": "_xdm.context.additionalParameters;version=1",
                    "xdm:data": {
                        "xdm:channel": "mobile",
                        "xdm:language": "en",
                        "xdm:isThirdParty": true,
                        "xdm:mobileVersion": "3.0.5106",
                        "xdm:mobileVersionMajor": "3",
                        "xdm:mobileVersionMinor": "0",
                        "xdm:mobileVersionPatch": "125",
                        "xdm:deviceType": "iOS",
                        "xdm:features": [
                            "p1000",
                            "p1001"
                        ]
                    }
                }
            ]
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}'
```

## Contextgegevens gebruiken in subsidiabiliteitsregels

Hier zijn voorbeelden die illustreren hoe te om contextgegevens te gebruiken die in beslissingsverzoeken in toelatingsregels worden overgegaan.

* Beleenbaar als de kenmerken van de contextgegevens een bepaalde waarde bevatten:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where contextData.features AND (select personetic from contextData.features where personetic.contains("123"))
  ```

* Komt in aanmerking als het kanaal niet leeg is en gelijk is aan mobiel:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where !contextData.channel.isNull() AND contextData.channel!="" AND contextData.channel="mobile"
  ```
