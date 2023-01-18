---
title: Aanbiedingen leveren
description: Het Beheer van het besluit is een inzameling van de diensten en programma's UI die marketers toelaat om de gepersonaliseerde aanbiedingservaringen van de eindgebruiker over kanalen en toepassingen tot stand te brengen en te leveren gebruikend bedrijfslogica en besluitvormingsregels.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
source-git-commit: f5d5c9dacd640b130dd4bcbaab803ecc7e999d10
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 1%

---

# Aanbiedingen leveren met de API voor besluitvorming {#decisioning-api}

Met het Beheer van het Besluit, kunt u de gepersonaliseerde aanbiedingservaringen van de eindgebruiker creëren en leveren, over kanalen en toepassingen gebruikend bedrijfslogica en besluitvormingsregels. Een aanbieding is een marketingbericht waaraan regels kunnen zijn gekoppeld die bepalen wie in aanmerking komt om de aanbieding te zien.

U kunt voorstellen tot stand brengen en leveren door een verzoek van de POST aan [!DNL Decisioning] API.

Deze zelfstudie vereist een goed begrip van API&#39;s, met name wat betreft het beheer van besluiten. Zie voor meer informatie de [Handleiding voor ontwikkelaars van API voor beheer van beslissingen](../getting-started.md). Deze zelfstudie vereist ook dat u een unieke plaatsings-id en een unieke keuze-id-waarde hebt. Raadpleeg de zelfstudies voor [een plaatsing maken](../offers-api/placements/create.md) en [tot het nemen van een besluit](../activities-api/activities/create.md).

➡️  [Ontdek deze functie in video](#video)

## Kopteksten van het type Inhoud accepteren {#accept-and-content-type-headers}

In de volgende tabel worden de geldige waarden weergegeven waaruit de *Inhoudstype* en *Accepteren* velden in de aanvraagkoptekst:

| Naam koptekst | Waarde |
| ----------- | ----- |
| Accepteren | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Inhoudstype | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

**API-indeling**

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/ode/` |
| `{CONTAINER_ID}` | De container waarin de beslissingen zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Verzoek**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ode/e0bd8463-0913-4ca1-bd84-6309134ca1f6/decisions' \
  -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
  -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0'
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
  -d '{
        "xdm:propositionRequests": [
            {
              "xdm:placementId": "xcore:offer-placement:ffed0456",
              "xdm:activityId": "xcore:offer-activity:ffed0123",
              "xdm:itemCount": 2
            },
            {
              "xdm:placementId": "xcore:offer-placement:ffed0012",
              "xdm:activityId": "xcore:offer-activity:fffc0789"
            }
        ],
        "xdm:profiles": [
            {
              "xdm:identityMap": {
                "SWCUSTID": [
                {
                    "xdm:id": "123@abc.com"
                }
                ]
            },
            "xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"
            }
        ],
        "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
        },
        "xdm:mergePolicy": {
            "xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"
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
| `xdm:propositionRequests` | Dit object bevat de plaatsings- en beslissingsidentificatoren. |
| `xdm:propositionRequests.xdm:placementId` | De unieke plaatsings-id. | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | De unieke besluit-id. | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | Het aantal voorstellen dat moet worden geretourneerd. Het maximumaantal is 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Dit object bevat informatie over het profiel waarvoor de beslissing wordt gevraagd. Voor een API-aanvraag bevat dit één profiel. |
| `xdm:profiles.xdm:identityMap` | Dit object bevat een set eindgebruikers-id&#39;s op basis van de naamruimte-integratiecode van de identiteit. De identiteitskaart kan meer dan één identiteit van elke namespace dragen. Voor meer informatie over naamruimten raadpleegt u [deze pagina](../../../segment/get-started-identity.md). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | De id die door de client wordt gegenereerd en die kan worden gebruikt om een verzoek voor een profielbeslissing uniek te identificeren. Deze ID wordt in het antwoord herhaald en heeft geen invloed op de uitkomst van het besluit. | `"xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"` |
| `xdm:allowDuplicatePropositions` | Dit heeft betrekking op de controlestructuur van de deduplicatieregels. Het bestaat uit een reeks vlaggen die erop wijzen of de zelfde optie over een bepaalde afmeting kan worden voorgesteld. Een markering die is ingesteld op true betekent dat duplicaten zijn toegestaan en niet mogen worden verwijderd over de categorie die wordt aangegeven door de markering. Een vlag die aan vals wordt geplaatst betekent dat de besluitvormingsmotor niet de zelfde voorstel over de afmeting zou moeten doen en in plaats daarvan de volgende beste optie voor één van de subbesluiten kiezen. |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Indien ingesteld op true, kunnen meerdere beslissingen dezelfde optie krijgen. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Indien ingesteld op true, kunnen meerdere plaatsingen dezelfde optie krijgen. | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | Hiermee wordt het samenvoegbeleid geïdentificeerd waarmee de gegevens moeten worden beheerd die door de service voor profieltoegang worden geretourneerd. Als er geen waarde is opgegeven in het verzoek, geeft Beslissingsbeheer geen toegang tot de profieltoegangsservice door, anders geeft het de id door die door de aanroeper is opgegeven. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Een reeks markeringen waarmee de inhoud van het antwoord wordt opgemaakt. |
| `xdm:responseFormat.xdm:includeContent` | Een Booleaanse waarde die, indien ingesteld op `true`bevat inhoud voor de reactie. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Een object dat wordt gebruikt om op te geven welke aanvullende metagegevens worden geretourneerd. Als deze eigenschap niet is opgenomen, `xdm:id` en `repo:etag` worden standaard geretourneerd. | `name` |
| `xdm:responseFormat.xdm:activity` | Deze markering identificeert de specifieke metagegevens die worden geretourneerd voor `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | Deze markering identificeert de specifieke metagegevens die worden geretourneerd voor `xdm:option`. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | Deze markering identificeert de specifieke metagegevens die worden geretourneerd voor `xdm:placement`. | `name`, `channel`, `componentType` |

**Antwoord**

Een succesvol antwoord geeft informatie over uw voorstel, met inbegrip van zijn uniek `xdm:propositionId`.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "xcore:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "xcore:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "xcore:fallback:ccc0222",
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
| `xdm:propositions` | Dit object bevat één beslissingsvoorstel. Er kunnen meerdere opties worden geretourneerd voor de beslissing. Als er geen opties worden gevonden, wordt het fallback-aanbod van het besluit geretourneerd. In de voorstellen voor één besluit is altijd een van de volgende elementen opgenomen: `options` eigenschap of een `fallback` eigenschap. Indien aanwezig, wordt `options` eigenschap mag niet leeg zijn. |
| `xdm:propositions.xdm:activity` | Dit object bevat de unieke id voor een beslissing. | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Dit object bevat de unieke id voor een aanbiedingsplaatsing. | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Dit object bevat één optie, inclusief de unieke id. Indien aanwezig mag dit object niet leeg zijn. | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Definieert het type van de component. `@type` fungeert als verwerkingscontract voor de klant. Wanneer de ervaring wordt verzameld, zoekt de componist naar de component(en) die een specifiek type hebben. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | De indeling van de responsinhoud. | De inhoud van de reactie kan zijn: `text`, `html block`, of `image link` |
| `xdm:score` | De score voor een optie die wordt berekend als resultaat van een classificatiefunctie die aan de optie of de beslissing is gekoppeld. Dit veld wordt door de API geretourneerd als een ranking-functie is betrokken bij het bepalen van de score van een aanbieding tijdens de rangschikking. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Dit object bevat één fallback-aanbieding, inclusief de unieke id. | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | De fysieke of digitale manifestatie van de bron. De indeling moet meestal het mediatype van de bron bevatten. Het formaat kan worden gebruikt om te bepalen welke software, hardware of andere apparatuur nodig is om de bron weer te geven of te gebruiken. U wordt aangeraden een waarde te selecteren in een gecontroleerde woordenlijst, bijvoorbeeld de lijst met [Internetmediatypen](http://www.iana.org/assignments/media-types/) computermedia-indelingen definiëren. | `"dc:format": "image/png"` of `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | Een optionele URL voor het lezen van het element van een netwerk of servicedetinepunt voor de levering van inhoud. Deze URL wordt gebruikt om het middel openlijk van een gebruikersagent toegang te hebben. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | De tijd toen het bericht van het beslissingsantwoord werd gecreeerd. Dit wordt weergegeven als tijdperk. | `"ode:createDate": 1566497582038` |

## Video over zelfstudie {#video}

De volgende video is bedoeld om uw begrip van de componenten van Beslissingsbeheer te steunen.

>[!NOTE]
>
>Deze video is van toepassing op de Offer decisioning toepassingsservice die op Adobe Experience Platform is gebouwd. Het biedt echter algemene richtlijnen voor het gebruik van Aanbieding in de context van Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## Volgende stappen {#next-steps}

Door deze API-handleiding te volgen, hebt u aanbiedingen gemaakt en geleverd met de [!DNL Decisions] API. Zie voor meer informatie de [overzicht van het besluitvormingsbeheer](../../../offers/get-started/starting-offer-decisioning.md).
