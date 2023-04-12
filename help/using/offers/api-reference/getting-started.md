---
title: Aan de slag
description: Leer hoe u de bibliotheek-API van de Aanbieding kunt gebruiken om toetsbewerkingen uit te voeren met de beslissingsengine.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 3%

---

# Handleiding voor ontwikkelaars van API voor beheer van beslissingen {#decision-management-api-developer-guide}

Deze handleiding voor ontwikkelaars bevat stappen waarmee u de functie [!DNL Offer Library] API. De gids verstrekt dan steekproefAPI vraag voor het uitvoeren van zeer belangrijke verrichtingen gebruikend de bepalingsmotor.

➡️ [Meer informatie over de componenten van Beslissingsbeheer vindt u in deze video](#video)

## Vereisten {#prerequisites}

Deze handleiding vereist een goed begrip van de volgende onderdelen van Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}: Het gestandaardiseerde kader waardoor [!DNL Experience Platform] organiseert de gegevens van de klantenervaring.
   * [Basisbeginselen van de schemacompositie](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html){target="_blank"}: Leer over de basisbouwstenen van schema&#39;s XDM.
* [Beslissingsbeheer](../../../using/offers/get-started/starting-offer-decisioning.md): Hierin worden de concepten en componenten beschreven die worden gebruikt voor het nemen van een besluit over de ervaring in het algemeen en het nemen van besluiten in het bijzonder. Toont de strategieën die voor het kiezen van de beste optie worden gebruikt om tijdens de ervaring van een klant voor te stellen.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}: PQL is een krachtige taal voor het schrijven van expressies over XDM-instanties. PQL wordt gebruikt om besluitvormingsregels te bepalen.

## API-voorbeeldaanroepen lezen {#reading-sample-api-calls}

Deze gids verstrekt voorbeeld API vraag om aan te tonen hoe te om uw verzoeken te formatteren. Dit zijn paden, vereiste kopteksten en correct opgemaakte ladingen voor aanvragen. Voorbeeld-JSON die wordt geretourneerd in API-reacties, wordt ook verschaft. Voor informatie over de conventies die worden gebruikt in documentatie voor voorbeeld-API-aanroepen raadpleegt u de sectie over [voorbeeld-API-aanroepen lezen](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} in de [!DNL Experience Platform] gids voor probleemoplossing.

## Waarden verzamelen voor vereiste koppen {#gather-values-for-required-headers}

Om vraag te maken aan [!DNL Adobe Experience Platform] API&#39;s, moet u eerst de [verificatiezelfstudie](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target="_blank"}. Het voltooien van de zelfstudie over verificatie biedt de waarden voor elk van de vereiste kopteksten in alle [!DNL Experience Platform] API-aanroepen, zoals hieronder wordt getoond:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Alle verzoeken die een nuttige lading (POST, PUT, PATCH) bevatten vereisen een extra kopbal:

* `Content-Type: application/json`

## Toegang tot een container beheren {#manage-access-to-container}

Een container is een isolatiemechanisme om verschillende zorgen van elkaar te onderscheiden. De container-id is het eerste padelement voor alle gegevensopslagruimte-API&#39;s. Alle beslissingsobjecten bevinden zich in een container.

Een beheerder kan gelijkaardige principes, middelen, en toegangstoestemmingen in profielen groeperen. Dit vermindert de beheerslast en wordt gesteund door [Adobe Admin Console](https://adminconsole.adobe.com/). Als u profielen wilt maken en gebruikers wilt toewijzen, moet u in uw organisatie productbeheerder voor Adobe Experience Platform zijn. Het is voldoende om in één keer productprofielen te maken die overeenkomen met bepaalde machtigingen en vervolgens gebruikers aan die profielen toe te voegen. Profielen fungeren als groepen waaraan machtigingen zijn verleend en elke echte gebruiker of technische gebruiker in die groep neemt deze machtigingen over.

Op basis van de beheerdersrechten kunt u gebruikers machtigingen verlenen of intrekken via de [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}. For more information, see the [Access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html){target="_blank"}.

### Containers weergeven die toegankelijk zijn voor gebruikers en integratie {#list-containers-accessible-to-users-and-integrations}

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

Een succesvolle reactie keert informatie betreffende besluitvormingsbeheerscontainers terug. Dit omvat een `instanceId` -kenmerk, waarvan de waarde de container-id is.

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

## Volgende stappen {#next-steps}

Dit document bevatte de vereiste kennis die nodig was om oproepen te doen aan de [!DNL Offer Library] API, inclusief het aanschaffen van uw container-id. U kunt nu aan de steekproefvraag verdergaan die in deze ontwikkelaarsgids wordt verstrekt en samen met hun instructies volgen.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## Hoe kan ik-video {#video}

De volgende video is bedoeld om uw begrip van de componenten van Beslissingsbeheer te steunen.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

