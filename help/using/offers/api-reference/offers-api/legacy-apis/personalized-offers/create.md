---
title: Een persoonlijke aanbieding maken
description: Een gepersonaliseerd aanbod is een aanpasbaar marketingbericht op basis van geschiktheidsregels en -beperkingen.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 234bee17-c830-4bc0-b258-182804df4cb3
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 6%

---

# Een persoonlijke aanbieding maken {#create-personalized-offer}

Een gepersonaliseerd aanbod is een aanpasbaar marketingbericht op basis van geschiktheidsregels en -beperkingen.

U kunt een gepersonaliseerde aanbieding tot stand brengen door een POST- verzoek aan [!DNL Offer Library] API te doen, terwijl het verstrekken van uw container identiteitskaart

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

De volgende lijst toont de geldige waarden die uit *inhoud-Type* bestaan en ** gebieden in de verzoekkopbal goedkeuren:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Accepteren | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Inhoudstype | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**API formaat**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | De container waarin de gepersonaliseerde aanbiedingen zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Verzoek**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
        "xdm:name": "Sale offer",
        "xdm:status": "draft",
        "xdm:representations": [
        {
                "xdm:components": [
                {
                        "dc:language": [
                            "en"
                    ],
                        "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                        "dc:format": "text/html"
                }
                ],
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
        }
    ],
        "xdm:selectionConstraint": {
            "xdm:startDate": "2023-10-01T16:00:00Z",
            "xdm:endDate": "2021-12-13T16:00:00Z",
            "xdm:eligibilityRule": "xcore:eligibility-rule:124e0faf5b8ee89b"
        },
        "xdm:rank": {
            "xdm:priority": 1
    },
        "xdm:cappingConstraint": {
            "xdm:globalCap": 150
    },
        "xdm:tags": [
            "xcore:tag:124e147572cd7866"
    ]
}'
```

**Reactie**

Een geslaagde reactie retourneert informatie over de zojuist gemaakte persoonlijke aanbieding, inclusief de unieke instantie-id en plaatsing `@id` . U kunt de instantie-id in latere stappen gebruiken om uw persoonlijke aanbieding bij te werken of te verwijderen.

```json
{
    "instanceId": "0f4bc230-13df-11eb-bc55-c11be7252432",
    "@id": "xcore:personalized-offer:124e181c8b0d7878",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T20:50:32.018624Z",
    "repo:lastModifiedDate": "2023-10-21T20:50:32.018624Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```

## Beperkingen {#limitations}

Aanbiedingsweergaven en sommige aanbodbeperkingen worden momenteel niet ondersteund door de mobiele [!DNL Experience Edge] workflows, bijvoorbeeld `Capping` . De veldwaarde `Capping` geeft aan hoe vaak een aanbieding voor alle gebruikers kan worden weergegeven. Voor meer details, zie [ de geschiktheidsregels en beperkingsdocumentatie van de Aanbieding ](../../../../offer-library/creating-personalized-offers.md).
