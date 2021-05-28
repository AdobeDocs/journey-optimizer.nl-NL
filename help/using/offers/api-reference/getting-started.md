---
title: Aan de slag
description: Leer hoe u de bibliotheek-API van de Aanbieding kunt gebruiken om belangrijke bewerkingen uit te voeren met behulp van de beslissingsbeheerengine.
source-git-commit: 741fe2b614e3ded57c4a7ecd9b7333bdd99ab359
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 2%

---

# Handleiding voor ontwikkelaars van API voor beheer van beslissingen

Deze ontwikkelaarsgids verstrekt stappen helpen u beginnen gebruikend [!DNL Offer Library] API. De gids verstrekt dan steekproefAPI vraag om zeer belangrijke verrichtingen uit te voeren gebruikend de Motor van het Beheer van het Besluit.

![](../../assets/do-not-localize/how-to-video.png) [Ontdek deze functie in video](#video)

## Vereisten

Deze handleiding vereist een goed begrip van de volgende onderdelen van Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en): Het gestandaardiseerde kader waardoor de gegevens van de  [!DNL Experience Platform] klantenervaring worden georganiseerd.
   * [Basisbeginselen van de schemacompositie](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html): Leer over de basisbouwstenen van schema&#39;s XDM.
* [Beslissingsbeheer](../../../using/offers/get-started/starting-offer-decisioning.md): Verklaart de concepten en de componenten die voor Ervaring in het algemeen en Offer decisioning in het bijzonder worden gebruikt. Toont de strategieën die voor het kiezen van de beste optie worden gebruikt om tijdens de ervaring van een klant voor te stellen.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html): PQL is een krachtige taal voor het schrijven van expressies over XDM-instanties. PQL wordt gebruikt om besluitvormingsregels te bepalen.

## API-voorbeeldaanroepen lezen

Deze gids verstrekt voorbeeld API vraag om aan te tonen hoe te om uw verzoeken te formatteren. Dit zijn paden, vereiste kopteksten en correct opgemaakte ladingen voor aanvragen. Voorbeeld-JSON die wordt geretourneerd in API-reacties, wordt ook verschaft. Voor informatie over de overeenkomsten die in documentatie voor steekproefAPI vraag worden gebruikt, zie de sectie over [hoe te om voorbeeld API vraag](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request) in [!DNL Experience Platform] het oplossen van problemengids te lezen.

## Waarden verzamelen voor vereiste koppen

Als u [!DNL Platform] API&#39;s wilt aanroepen, moet u eerst de [verificatiezelfstudie](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html) voltooien. Het voltooien van de zelfstudie over verificatie biedt de waarden voor elk van de vereiste headers in alle API-aanroepen [!DNL Experience Platform], zoals hieronder wordt getoond:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Alle verzoeken die een nuttige lading (POST, PUT, PATCH) bevatten vereisen een extra kopbal:

* `Content-Type: application/json`

## Toegang tot een container beheren

Een container is een isolatiemechanisme om verschillende zorgen van elkaar te onderscheiden. De container-id is het eerste padelement voor alle gegevensopslagruimte-API&#39;s. Alle beslissingsobjecten bevinden zich in een container.

Een beheerder kan gelijkaardige principes, middelen, en toegangstoestemmingen in profielen groeperen. Dit vermindert de beheerslast en wordt gesteund door [Adobe Admin Console](https://adminconsole.adobe.com/). Als u profielen wilt maken en gebruikers wilt toewijzen, moet u in uw organisatie productbeheerder voor Adobe Experience Platform zijn. Het is voldoende om in één keer productprofielen te maken die overeenkomen met bepaalde machtigingen en vervolgens gebruikers aan die profielen toe te voegen. Profielen fungeren als groepen waaraan machtigingen zijn verleend en elke echte gebruiker of technische gebruiker in die groep neemt deze machtigingen over.

Op basis van beheerdersrechten kunt u gebruikers machtigingen verlenen of intrekken via de [Adobe Admin Console](https://adminconsole.adobe.com/). Voor meer informatie, zie [Toegangsbeheer overzicht](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html).

### Containers weergeven die toegankelijk zijn voor gebruikers en integratie

**API-indeling**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filtert de lijst van containers door hun vereniging aan productcontexten. | `acp` |
| `{PROPERTY}` | Filtert het type container dat wordt geretourneerd. | `_instance.containerType==decisioning` |

**Verzoek**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwoord**

Een succesvolle reactie keert informatie betreffende besluitvormingsbeheerscontainers terug. Dit omvat een `instanceId` attribuut, waarvan de waarde uw container identiteitskaart is

```json
{
    "_embedded": {
        "https://ns.adobe.com/experience/xcore/container": [
            {
                "instanceId": "{INSTANCE_ID}",
                "schemas": [
                    "https://ns.adobe.com/experience/xcore/container;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2020-09-16T07:54:32.098139Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "containerType": "decisioning",
                    "repo:name": "{REPO_NAME}",
                    "dataCenter": "{DATA_CENTER}",
                    "parentName": "{PARENT_NAME}",
                    "parentId": "{PARENT_ID}"
                },
                "_links": {
                    "self": {
                        "href": "/containers/{INSTANCE_ID}"
                    }
                }
            }
        ]
    },
    "_links": {
        "self": {
            "href": "/?product=acp&property=_instance.containerType==decisioning",
            "@type": "https://ns.adobe.com/experience/xcore/hal/home"
        }
    }
}
```

## Volgende stappen

Dit document behandelt de vereiste kennis die wordt vereist om vraag aan [!DNL Offer Library] API te maken, met inbegrip van het verwerven van uw containeridentiteitskaart. U kunt nu aan de steekproefvraag verdergaan die in deze ontwikkelaarsgids wordt verstrekt en samen met hun instructies volgen.

## Video over zelfstudie {#video}

De volgende video is bedoeld om uw begrip van de componenten van Beslissingsbeheer te steunen.

>[!NOTE]
>
>Deze video is van toepassing op de Offer decisioning toepassingsservice die op Adobe Experience Platform is gebouwd. Het biedt echter algemene richtlijnen voor het gebruik van Aanbieding in de context van Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
