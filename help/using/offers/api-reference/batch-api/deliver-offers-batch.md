---
title: Batchbeslissing-API
description: Leer hoe u de Batch-API voor besluitvorming gebruikt om de beste aanbiedingen voor gesegmenteerde profielen te selecteren binnen een vooraf gedefinieerd beslissingsbereik.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 817a77c5717804ccae36db3dd8920008ab127684
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 1%

---

# Biedt aanbiedingen met de [!DNL Batch Decisioning] API

De [!DNL Batch Decisioning] API staat organisaties toe om de functionaliteit van de offer decisioning voor alle profielen in een bepaald segment in één vraag te gebruiken. De aanbiedingsinhoud voor elke profielen in het segment wordt geplaatst in een dataset van Adobe Experience Platform waar het voor de werkschema&#39;s van de douanepartij beschikbaar is.

Met de [!DNL Batch Decisioning] API, kunt u een dataset met de beste aanbiedingen voor alle profielen in een segment van Adobe Experience Platform voor een beslissingswerkingsgebied bevolken. Een organisatie kan bijvoorbeeld batch-beslissingen willen uitvoeren, zodat ze aanbiedingen naar een leverancier van berichten kunnen verzenden. Die aanbiedingen worden dan gebruikt als inhoud die voor partijberichtlevering aan het zelfde segment van gebruikers wordt verzonden.

Hiertoe zou de organisatie:

* Voer de [!DNL Batch Decisioning] API, die twee verzoeken bevat:

   1. A **Batchaanvraag** om de status van batchwerkbelasting te verkrijgen.

   2. A **Batchverzoek POST** om een werkbelasting naar batchverwerking te starten, kunt u kiezen.

* Exporteer de dataset naar de API van de leverancier van de berichtlevering.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

## Aan de slag {#getting-started}

Voordat u deze API gebruikt, moet u de volgende vereiste stappen uitvoeren.

### De beslissing voorbereiden

Volg de onderstaande stappen om uw beslissingen voor te bereiden:

* Om een besluitresultaat uit te voeren, creeer een dataset gebruikend het schema van de Gebeurtenissen van het Besluit van de ODE.

* Creeer een segment van het Platform dat zou moeten worden geëvalueerd en dan worden bijgewerkt. Zie de [segmentatiedocumentatie](http://www.adobe.com/go/segmentation-overview-en) om meer over te leren hoe te om de evaluatie van het segmentlidmaatschap bij te werken.

* In Adobe Journey Optimizer een beslissing maken (met een beslissingsbereik dat bestaat uit een besluit-ID en een plaatsings-ID). Zie de [deel over de afbakening van de besluitvormingsgebieden](../../offer-activities/create-offer-activities.md) van de handleiding voor het maken van beslissingen voor meer informatie.

### API-vereisten

Voor alle aanvragen voor Batchbeslissing zijn de volgende extra headers vereist:

* `Content-Type`: `application/json`
* `x-request-id`: Een unieke tekenreeks die de aanvraag identificeert.
* `x-sandbox-name`: De naam van de sandbox.
* `x-sandbox-id`: De sandbox-id.

## Informatie ophalen over een batchbeslissing {#retrieve-information-on-a-batch-decision}

Om informatie over een specifiek besluit terug te winnen, doe een verzoek van de GET aan `/workloads/decisions` eindpunt terwijl het verstrekken van de overeenkomstige waarde van werklastidentiteitskaart voor uw besluit.

**API-indeling**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | De container waarin de beslissingen zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | De UUID die wordt gegenereerd door Offer decisioning die één werkbelasting identificeert. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: {ACCESS_TOKEN}'
```

**Antwoord**

```json
{
    "@id": "f395ab1f-dfaf-48d4-84c9-199ad6354591",
    "xdm:imsOrgId": "{IMS_ORG}",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Eigenschap | Beschrijving | Voorbeeld |
| -------- | ----------- | ------- |
| `@id` | De UUID die wordt gegenereerd door Offer decisioning die één werkbelasting identificeert. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | ID IMS-organisatie | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | De container-id | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | De tijd waarop de aanvraag voor beslissingswerkbelasting is gemaakt. | `1648076994405` |
| `ode:status` | De status van de werklast begint met &quot;QUEUED&quot; en verandert in &quot;PROCESSING&quot;, &quot;INGESTING&quot;, &quot;COMPLETED&quot; of &quot;ERROR&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Hier worden meer details weergegeven, zoals sparkJobId en batchID als de status &quot;PROCESSING&quot; of &quot;INGESTING&quot; is. De foutdetails worden weergegeven als de status &quot;ERROR&quot; is. |  |

## Een batchproces starten {#start-a-batch-process}

Als u een werkbelasting wilt starten om beslissingen over batchprocessen te nemen, vraagt u een POST aan de `/workloads/decisions` eindpunt.

**API-indeling**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | De container waarin de beslissingen zich bevinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Verzoek**

```shell
curl -X POST 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions' \
-H 'x-request-id: f671a589-eb7b-432f-b6b9-23d5b796b4dc' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: {ACCESS_TOKEN}' \
-d '{
  "xdm:segmentIds": [
    "609028e4-e66c-4776-b0d9-c782887e2273"
  ],
  "xdm:dataSetId": "6196b4a1a63bd118dafe093c",
  "xdm:propositionRequests": [
        {
            "xdm:activityId": "xcore:offer-activity:1410cdcda196707b",
            "xdm:placementId": "xcore:offer-placement:1410c4117306488a",
            "xdm:itemCount": 1
        }
  ],
  "xdm:includeContent": false
}'
```

| Eigenschap | Beschrijving | Voorbeeld |
| -------- | ----------- | ------- |
| `xdm:segmentIds` | De unieke id van het segment. Het kan slechts één waarde bevatten. | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | De output dataSet dat beslissingsgebeurtenissen kunnen worden geschreven in. | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | Een omslag die placementId en activityId bevat |  |
| `xdm:activityId` | De unieke identificatiecode van het besluit. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | De unieke plaatsings-id. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | Dit is een facultatief gebied dat het aantal punten zoals opties toont die voor het beslissingswerkingsgebied worden gevraagd. Standaard retourneert de API één optie per bereik, maar u kunt expliciet om meer opties vragen door dit veld op te geven. Voor elk bereik kunnen minimaal 1 en maximaal 30 opties worden aangevraagd. | `1` |
| `xdm:includeContent` | Dit is een optioneel veld en is `false` standaard. Indien `true`De inhoud van het aanbod is opgenomen in de besluitvormingsgebeurtenissen van de dataset. | `false` |

Zie de [Beslissingsbeheerdocumentatie](../../get-started/starting-offer-decisioning.md) voor een overzicht van de belangrijkste concepten.

**Antwoord**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Eigenschap | Beschrijving | Voorbeeld |
| -------- | ----------- | ------- |
| `@id` | De UUID die wordt gegenereerd door Offer decisioning die één werkbelasting identificeert. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | De id voor uw IMS-organisatie. | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | Uw container-id. | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | De tijd toen het verzoek van de beslissingswerklast werd gecreeerd. | `1648078924834` |
| `ode:status` | De status van de werklast. | `ode:status: "QUEUED"` |

## Serviceniveaus {#service-levels}

De tijd van begin tot eind voor elke partijbeslissing is de duur van de tijd de werkbelasting aan het beslissingsresultaat beschikbaar in outputdataset wordt gecreeerd. De segmentgrootte in de lading van het de verzoeksalaris van de POST is de belangrijkste factor die de eind-aan-eind partijbeslissingstijd beïnvloedt. Hieronder vindt u enkele waarnemingen voor verschillende segmentgrootten:

* segmentgrootte &lt;= 10K: 6 minuten
* segmentgrootte &lt;= 1M: 10 minuten
* segmentgrootte &lt;= 15M: 75 minuten

## Beperkingen {#limitations}

De volgende beperkingen bestaan met [!DNL Batch Decisioning] API:

* **Eén batchtaak**: Momenteel, slechts kan één enkele partijbaan per dataset tegelijkertijd worden in werking gesteld. Eventuele andere verzoeken zouden reageren met HTTP 429 (Te veel verzoeken).
* **Frequentiecorrectie**: Een batch wordt uitgevoerd zonder de profielmomentopname die één keer per dag plaatsvindt. De [!DNL Batch Decisioning] API kapt de frequentie en laadt altijd profielen van de meest recente momentopname.

## Volgende stappen {#next-steps}

Door deze API-handleiding te volgen, hebt u de werklaststatus gecontroleerd en aanbiedingen geleverd via de [!DNL Batch Decisioning] API. Zie voor meer informatie de [overzicht van het besluitvormingsbeheer](../../get-started/starting-offer-decisioning.md).
