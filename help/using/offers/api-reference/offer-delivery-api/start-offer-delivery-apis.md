---
title: Aan de slag met API's voor levering van aanbiedingen
description: Meer informatie over de beschikbare API's voor persoonlijke aanbiedingen.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: d9d2e763b04ec725cc389b1d535df4df06103018
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# Aan de slag met API&#39;s voor levering van aanbiedingen {#about-decisioning-apis}

U kunt voorstellen leveren gebruikend of **Beslissing** of de **Randbeslissing** API. Daarnaast worden de **Batchbeslissing** API staat u toe om aanbiedingen aan alle profielen in een bepaald publiek in één vraag te leveren. De aanbiedingsinhoud voor elke profielen in het publiek wordt geplaatst in een dataset van Adobe Experience Platform waar het voor de werkschema&#39;s van de douanepartij beschikbaar is.

Op deze pagina vindt u informatie over specifieke functies die beschikbaar zijn bij de **Beslissing** en **Randbeslissing** API&#39;s. Terwijl beide u toestaan om aanbiedingen aan uw klanten te leveren, adviseren wij gebruikend **Randbeslissing** API waar mogelijk voor binnenkomende gebruiksgevallen en voor betere latentie en doorvoer op uw platform.

Raadpleeg de volgende secties voor meer informatie over het werken met de API&#39;s:
* [API voor besluitvorming](decisioning-api.md)
* [Edge-API voor besluitvorming](edge-decisioning-api.md)
* [Batchbeslissing-API](batch-decisioning-api.md)

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

## Edge-API-mogelijkheden voor besluitvorming {#edge}

**Unieke aanvraag voor ervaringsgebeurtenissen en beslissingsverzoeken**

Met de Edge Decisioning-API kunt u in één aanvraag de ervaringsgebeurtenis zelf verzenden samen met de beslissingsaanvraag, in plaats van twee verschillende aanvragen te hebben.

Als een klant bijvoorbeeld uw website bezoekt, bevat de aanvraag de ervaringsgebeurtenis (het bezoek van de klant aan de pagina) en wordt een aanbieding teruggestuurd om de bezochte pagina te vullen.

**Opslag van contextgegevens in Adobe Experience Platform**

Contextgegevens verwijzen naar gegevens die u alleen kent op het moment dat u een aanbieding wilt terugsturen. Bijvoorbeeld de kleur van het aangekochte artikel, het weer op het moment van de aankoop, enz.

Wanneer contextgegevens worden doorgegeven met een Edge-API-aanvraag voor besluitvorming, worden gegevens opgeslagen in het Adobe Experience Platform-profiel, zodat ze later opnieuw kunnen worden gebruikt.

>[!NOTE]
>
>Opdat de contextgegevens worden opgeslagen, moet u een specifiek geconfigureerd XDM-schema hebben.

**Bijwerken van de teller voor frequentiecattering**

Als voor sommige van uw aanbiedingen de functie voor het toewijzen van frequenties is ingeschakeld om te bepalen hoe vaak het aantal bijschriften wordt teruggezet, wordt de teller in minder dan 3 seconden bijgewerkt en beschikbaar in een besluit van de Edge Decisioning API. [Leer hoe u beperkingen aan een aanbieding kunt toevoegen](../../offer-library/add-constraints.md)

## API-mogelijkheden voor besluitvorming {#decisioning}

De hieronder vermelde functies zijn alleen beschikbaar met de API voor besluitvorming. Gebruik de API voor besluitvorming als u een van deze toepassingen wilt gebruiken om aan uw vereisten te voldoen. Anders raden we u aan de Edge-API&#39;s voor besluitvorming te gebruiken.

* **Inhoud en kenmerken van aanbiedingen**: u kunt ervoor kiezen om de inhoud en kenmerken van een aanbieding niet te retourneren met een speciale optie.
* **Metagegevens aanbieden**: een optie inschakelen om de metagegevens van een aanbieding te retourneren.
* **Samenvoegbeleid**: gebruik in uw aanvraag een ander samenvoegbeleid dan het beleid dat aan uw sandbox is gekoppeld.
* **Decisitiegebeurtenissen en frequentiecapping**: blokbeslissingsgebeurtenissen worden niet geteld door een willekeurige frequentiecapping die plaatsvindt.
* **Proposities dupliceren**: schakel een optie in om voorstellingen niet te dedupliceren.
