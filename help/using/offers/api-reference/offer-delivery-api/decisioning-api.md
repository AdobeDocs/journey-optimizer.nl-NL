---
title: Aanbiedingen leveren
description: Het Beheer van het besluit is een inzameling van de diensten en programma's UI die marketers toelaat om de gepersonaliseerde aanbiedingservaringen van de eindgebruiker over kanalen en toepassingen tot stand te brengen en te leveren gebruikend bedrijfslogica en besluitvormingsregels.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 1%

---

# Aanbiedingen leveren met de API voor besluitvorming {#decisioning-api}

Met het Beheer van het Besluit, kunt u de gepersonaliseerde aanbiedingservaringen van de eindgebruiker creëren en leveren, over kanalen en toepassingen gebruikend bedrijfslogica en besluitvormingsregels. Een aanbieding is een marketingbericht waaraan regels kunnen zijn gekoppeld die bepalen wie in aanmerking komt om de aanbieding te zien.

U kunt aanbiedingen maken en leveren door een POST-aanvraag in te dienen bij de [!DNL Decisioning] API.

Deze zelfstudie vereist een goed begrip van API&#39;s, met name wat betreft het beheer van besluiten. Voor meer informatie, zie de [ gids van de ontwikkelaar van het Beheer API van het Besluit ](../getting-started.md). Deze zelfstudie vereist ook dat u een unieke plaatsings-id en een unieke keuze-id-waarde hebt. Als u deze waarden niet hebt verworven, zie de leerprogramma&#39;s voor [ creërend een plaatsing ](../offers-api/placements/create.md) en [ creërend een besluit ](../activities-api/activities/create.md).

## Vereiste koppen {#required-headers}

De volgende lijst toont de geldige waarden die uit *inhoud-Type* bestaan en ** gebieden in de verzoekkopbal goedkeuren:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Accepteren | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Inhoudstype | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |
| Toestemming | `Bearer {ACCESS_TOKEN}` |
| x-gw-ims-org-id | `{IMS_ORG}` |
| x-sandbox-name | `{SANDBOX_NAME}` |
| x-api-key | `{API_KEY}` |

* Alle verzoeken die een lading (POST, PUT, PATCH) bevatten vereisen de inhoud-type kopbal


>[!NOTE]
>
>De machtigingscontrole wordt niet afgedwongen voor afzonderlijke sandboxen. Zolang de bezoeker een geldig teken voorlegde, zal levering API door gaan.

## API-verzoek {#request}

### API-indeling

```https
POST /{ENDPOINT_PATH}/decisions
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/ods` |

### Verzoek

```shell
curl -X POST 'https://platform.adobe.io/data/core/ods/decisions' \
-H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
-H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}....' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'x-request-id: e9ac8d7e-3e77-4b38-8726-555ef1737b32-example' \
-d '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:15ded04b1786ea27",
            "xdm:placementId": "dps:offer-placement:15d9bc01d35e1238"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "example@adobe.com",
                        "primary": true
                    }
                ]
            }
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

| Eigenschap | Beschrijving | Voorbeeld |
| -------- | ----------- | ------- |
| `xdm:propositionRequests` | Dit object bevat de plaatsings- en beslissingsidentificatoren. |  |
| `xdm:propositionRequests.xdm:placementId` | De unieke plaatsings-id. | `"xdm:placementId": "dps:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | De unieke besluit-id. | `"xdm:activityId": "dps:offer-activity:ffed0123"` |
| `xdm:itemCount` | Het aantal voorstellen dat moet worden geretourneerd. Het maximumaantal is 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Dit object bevat informatie over het profiel waarvoor de beslissing wordt gevraagd. Voor een API-aanvraag bevat dit één profiel. |  |
| `xdm:profiles.xdm:identityMap` | Dit object bevat een set eindgebruikers-id&#39;s op basis van de naamruimte-integratiecode van de identiteit. De identiteitskaart kan meer dan één identiteit van elke namespace dragen. Voor meer informatie over namespaces, zie [ deze pagina ](../../../audience/get-started-identity.md). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | De id die door de client wordt gegenereerd en die kan worden gebruikt om een verzoek voor een profielbeslissing uniek te identificeren. Deze ID wordt in het antwoord herhaald en heeft geen invloed op de uitkomst van het besluit. | `"xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"` |
| `xdm:allowDuplicatePropositions` | Dit heeft betrekking op de controlestructuur van de deduplicatieregels. Het bestaat uit een reeks vlaggen die erop wijzen of de zelfde optie over een bepaalde afmeting kan worden voorgesteld. Een markering die is ingesteld op true betekent dat duplicaten zijn toegestaan en niet mogen worden verwijderd over de categorie die wordt aangegeven door de markering. Een vlag die aan vals wordt geplaatst betekent dat de besluitvormingsmotor niet de zelfde voorstel over de afmeting zou moeten doen en in plaats daarvan de volgende beste optie voor één van de subbesluiten kiezen. |  |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Indien ingesteld op true, kunnen meerdere beslissingen dezelfde optie krijgen. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Indien ingesteld op true, kunnen meerdere plaatsingen dezelfde optie krijgen. | `"xdm:acrossPlacements": true` |
| `xdm:enrichedAudience` | Voeg deze parameter toe en plaats het aan &quot;waar&quot;als u een publiek CSV richt | `"xdm:enrichedAudience": true` |
| `xdm:mergePolicy.xdm:id` | Hiermee wordt het samenvoegbeleid geïdentificeerd waarmee de gegevens moeten worden beheerd die door de service voor profieltoegang worden geretourneerd. Als men niet in het verzoek wordt gespecificeerd, zal het Beheer van het Besluit niet langs om het even welke dienst van de profieltoegang overgaan, anders zou het identiteitskaart overgaan die door de bezoeker wordt verstrekt. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Een reeks markeringen waarmee de inhoud van het antwoord wordt opgemaakt. |  |
| `xdm:responseFormat.xdm:includeContent` | Een Booleaanse waarde die, indien ingesteld op `true` , inhoud bevat voor de reactie. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Een object dat wordt gebruikt om op te geven welke aanvullende metagegevens worden geretourneerd. Als deze eigenschap niet wordt opgenomen, worden `xdm:id` en `repo:etag` standaard geretourneerd. | `name` |
| `xdm:responseFormat.xdm:activity` | Deze markering geeft de specifieke metagegevens aan die voor `xdm:activity` worden geretourneerd. | `name` |
| `xdm:responseFormat.xdm:option` | Deze markering geeft de specifieke metagegevens aan die voor `xdm:option` worden geretourneerd. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | Deze markering geeft de specifieke metagegevens aan die voor `xdm:placement` worden geretourneerd. | `name`, `channel`, `componentType` |

### Antwoord

Een geslaagde reactie retourneert informatie over uw voorstel, inclusief de unieke `xdm:propositionId` .

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "dps:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "dps:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "dps:fallback:ccc0222",
        "repo:etag": 5,
        "@type": "https://ns.adobe.com/experience/decisioning/content-component-imagelink",
        "dc:format": "image/png",
        "xdm:deliveryURL": "https://cdn.adobe.com/content/1445323-1134331.png",
        "xdm:content": "https://www.adobe.com/index2.html"
      }
    }
  ],
  "ode:createDate": 1566497582038
}
```

| Eigenschap | Beschrijving | Voorbeeld |
| -------- | ----------- | ------- |
| `xdm:propositionId` | De unieke id voor de proposition-entiteit die is gekoppeld aan een XDM DecisionEvent. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Dit object bevat één beslissingsvoorstel. Er kunnen meerdere opties worden geretourneerd voor de beslissing. Als er geen opties worden gevonden, wordt het fallback-aanbod van het besluit geretourneerd. Voorstellen voor een enkele beslissing bevatten altijd een eigenschap `options` of een eigenschap `fallback` . Indien aanwezig mag de eigenschap `options` niet leeg zijn. |  |
| `xdm:propositions.xdm:activity` | Dit object bevat de unieke id voor een beslissing. | `"xdm:id": "dps:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Dit object bevat de unieke id voor een aanbiedingsplaatsing. | `"xdm:id": "dps:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Dit object bevat één optie, inclusief de unieke id. Indien aanwezig mag dit object niet leeg zijn. | `xdm:id": "dps:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Definieert het type van de component. `@type` fungeert als het verwerkingscontract voor de client. Wanneer de ervaring wordt verzameld, zoekt de componist naar de component(en) die een specifiek type hebben. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | De indeling van de inhoud van het antwoord. | De inhoud van de reactie kan zijn: `text`, `html block` of `image link` |
| `xdm:score` | De score voor een optie die wordt berekend als resultaat van een classificatiefunctie die aan de optie of de beslissing is gekoppeld. Dit veld wordt door de API geretourneerd als een ranking-functie is betrokken bij het bepalen van de score van een aanbieding tijdens de classificatie. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Dit object bevat één fallback-aanbieding, inclusief de unieke id. | `"xdm:id": "dps:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | De fysieke of digitale manifestatie van de bron. De indeling moet meestal het mediatype van de bron bevatten. Het formaat kan worden gebruikt om te bepalen welke software, hardware of andere apparatuur nodig is om de bron weer te geven of te gebruiken. Het wordt geadviseerd om een waarde van een gecontroleerde woordenlijst, bijvoorbeeld, de lijst van [ de Types van Media van Internet ](https://www.iana.org/assignments/media-types/) te selecteren die de formaten van computermedia bepalen. | `"dc:format": "image/png"` of `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | Een optionele URL voor het lezen van het element van een netwerk of servicedetinepunt voor de levering van inhoud. Deze URL wordt gebruikt om het middel openlijk van een gebruikersagent toegang te hebben. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | De tijd toen het bericht van het beslissingsantwoord werd gecreeerd. Dit wordt weergegeven als tijdperk. | `"ode:createDate": 1566497582038` |

**de codes van de Reactie**

De onderstaande tabel bevat een lijst met alle codes die in het antwoord kunnen worden geretourneerd:

| Code | Beschrijving |
|  ---  |  ---  |
| 200 | Geslaagd. Er is een besluit genomen over bepaalde activiteiten |
| 400 | Ongeldige parameter request. Het verzoek kan niet door de server worden begrepen wegens misvormde syntaxis. |
| 403 | Verboden, onvoldoende machtigingen. |
| 422 | Onbewerkbare entiteit. De aanvraagsyntaxis is correct, echter, wegens semantische fouten kan het niet worden verwerkt. |
| 429 | Te veel verzoeken. De gebruiker heeft te veel verzoeken binnen een bepaalde hoeveelheid tijd verzonden. |
| 500 | Interne serverfout. De server heeft een onverwachte voorwaarde aangetroffen waardoor deze de aanvraag niet kan uitvoeren. |
| 503 | Service niet beschikbaar vanwege overbelasting van de server. De server kan het verzoek momenteel niet verwerken vanwege een tijdelijke overbelasting. |

<!-- ## Tutorial video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12) -->

## Volgende stappen {#next-steps}

Door deze API-handleiding te volgen, hebt u aanbiedingen gemaakt en geleverd met de [!DNL Decisions] API. Voor meer informatie, zie het [ overzicht over het Beheer van het Besluit ](../../../offers/get-started/starting-offer-decisioning.md).
