---
title: Batchbeslissing-API
description: Leer hoe u de Batch-API voor besluitvorming gebruikt om de beste aanbiedingen voor de profielen van het publiek te selecteren binnen een vooraf gedefinieerd beslissingsbereik.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---


# Aanbiedingen leveren met behulp van de [!DNL Batch Decisioning] API {#deliver-offers-batch}

Met de API van [!DNL Batch Decisioning] kunnen organisaties de beslissingsfunctionaliteit voor alle profielen in een bepaald publiek in één aanroep gebruiken. De aanbiedingsinhoud voor elke profielen in het publiek wordt geplaatst in een dataset van Adobe Experience Platform waar het voor de werkschema&#39;s van de douanepartij beschikbaar is.

Met de API van [!DNL Batch Decisioning] kunt u een dataset vullen met de beste aanbiedingen voor alle profielen in een Adobe Experience Platform-publiek voor beslissingsbereik. Een organisatie wil bijvoorbeeld [!DNL Batch Decisioning] uitvoeren, zodat ze aanbiedingen naar een leverancier van berichten kan verzenden. Die aanbiedingen worden dan gebruikt als inhoud die voor partijberichtlevering aan het zelfde publiek van gebruikers wordt verzonden.

Om dit te doen, zou de organisatie:

* Voer de API [!DNL Batch Decisioning] uit, die twee verzoeken bevat:

   1. A **verzoek van de POST van de Partij** om een werkbelasting te beginnen aan de selectie van de de partijprocesaanbieding.

   2. A **verzoek van GET van de Partij** om de status van de partijwerkbelasting te krijgen.

* Exporteer de dataset naar de API van de leverancier van de berichtlevering.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=nl-NL) to learn more about exporting audiences.) -->

>[!NOTE]
>
>U kunt de batch ook bepalen via de Journey Optimizer-interface. Voor meer informatie, verwijs naar [&#x200B; deze sectie &#x200B;](../../batch-delivery.md), die informatie over globale eerste vereisten en beperkingen verstrekt om rekening te houden met wanneer het gebruiken van partijbeslissing.

* **het aantal lopende partijbanen per dataset**: Tot vijf partijbanen kunnen in een tijd, per dataset worden in werking gesteld. Om het even welke andere partijverzoeken met de zelfde outputdataset worden toegevoegd aan de rij. Er wordt een taak in de wachtrij opgehaald om te worden verwerkt zodra de vorige taak is voltooid.
* **het in kaart brengen van de Frequentie**: Een partijlooppas van de profielmomentopname die eens per dag voorkomt. De API van [!DNL Batch Decisioning] kapt de frequentie in en laadt altijd profielen van de recentste momentopname.

## Aan de slag {#getting-started}

Voordat u deze API gebruikt, moet u de volgende vereiste stappen uitvoeren.

### De beslissing voorbereiden {#prepare-decision}

Om één of meerdere besluiten voor te bereiden, zorg ervoor u een dataset, een publiek, en een besluit hebt gecreeerd. Die eerste vereisten zijn gedetailleerd in [&#x200B; deze sectie &#x200B;](../../batch-delivery.md).

### API-vereisten {#api-requirements}

Alle [!DNL Batch Decisioning] verzoeken vereisen de volgende kopballen naast degenen die in de [&#x200B; gids van de ontwikkelaar van het Beheer API van het Besluit &#x200B;](../getting-started.md) worden bedoeld:

* `Content-Type`: `application/json`
* `x-request-id`: Een unieke tekenreeks die de aanvraag identificeert.
* `x-sandbox-name`: De naam van de sandbox.

## Een batchproces starten {#start-a-batch-process}

Als u een werkbelasting wilt starten om beslissingen over batchprocessen te nemen, vraagt u een POST-aanvraag naar het `/workloads/decisions` -eindpunt.

>[!NOTE]
>
>De gedetailleerde informatie over de verwerkingstijd van partijbanen is beschikbaar in [&#x200B; deze sectie &#x200B;](../../batch-delivery.md).

**API formaat**

```https
POST {ENDPOINT_PATH}/workloads/decisions
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/dwm` |

**Verzoek**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dwm/workloads/decisions' \
-H 'x-request-id: f671a589-eb7b-432f-b6b9-23d5b796b4dc' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
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
| `xdm:activityId` | De unieke identificatiecode van het besluit. |  |
| `xdm:dataSetId` | De output dataSet dat beslissingsgebeurtenissen kunnen worden geschreven in. | `6196b4a1a63bd118dafe093c` |
| `xdm:includeContent` | Dit is een optioneel veld en is standaard `false` . Als `true`, is de aanbiedingsinhoud inbegrepen in de besluitvormingsgebeurtenissen van dataset. | `false` |
| `xdm:itemCount` | Dit is een facultatief gebied dat het aantal punten zoals opties toont die voor het beslissingswerkingsgebied worden gevraagd. Standaard retourneert de API één optie per bereik, maar u kunt expliciet om meer opties vragen door dit veld op te geven. Voor elk bereik kunnen minimaal 1 en maximaal 30 opties worden aangevraagd. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | De unieke plaatsings-id. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:propositionRequests` | Een omslag die `placementId` en `activityId` bevat |  |
| `xdm:segmentIds` | De waarde is een array die de unieke id van het publiek bevat. Het kan slechts één waarde bevatten. | `609028e4-e66c-4776-b0d9-c782887e2273` |

Verwijs naar de [&#x200B; documentatie van het Beheer van het Besluit &#x200B;](../../get-started/starting-offer-decisioning.md) voor een overzicht van de belangrijkste concepten en eigenschappen.

**Reactie**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Eigenschap | Beschrijving | Voorbeeld |
| -------- | ----------- | ------- |
| `@id` | De UUID die door besluitvormingsbeheer wordt geproduceerd dat één enkele werkbelasting identificeert. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | De organisatie-id. | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | De tijd toen het verzoek van de beslissingswerklast werd gecreeerd. | `1648078924834` |
| `ode:status` | De status van de werklast. | `ode:status: "QUEUED"` |

## Informatie ophalen over een batchbeslissing {#retrieve-information-on-a-batch-decision}

Om informatie over een specifieke beslissing terug te winnen, doe een GET verzoek aan het `/workloads/decisions` eindpunt terwijl het verstrekken van de overeenkomstige waarde van werklastidentiteitskaart voor uw besluit.

**API formaat**

```https
GET {ENDPOINT_PATH}/workloads/decisions/{WORKLOAD_ID}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor gegevensopslagruimte-API&#39;s. | `https://platform.adobe.io/data/core/dwm` |
| `{WORKLOAD_ID}` | De UUID die door besluitvormingsbeheer wordt geproduceerd dat één enkele werkbelasting identificeert. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dwm/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}'
```

**Reactie**

```json
{
   "@id": "f395ab1f-dfaf-48d4-84c9-199ad6354591",
    "xdm:imsOrgId": "{IMS_ORG}",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Eigenschap | Beschrijving | Voorbeeld |
| -------- | ----------- | ------- |
| `@id` | De UUID die door besluitvormingsbeheer wordt geproduceerd dat één enkele werkbelasting identificeert. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | Organisatie-id | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | De tijd waarop de aanvraag voor beslissingswerkbelasting is gemaakt. | `1648076994405` |
| `ode:status` | De status van de werklast begint met &quot;QUEUED&quot; en verandert in &quot;PROCESSING&quot;, &quot;INGESTING&quot;, &quot;COMPLETED&quot; of &quot;ERROR&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Hier worden meer details weergegeven, zoals sparkJobId en batchID als de status &quot;PROCESSING&quot; of &quot;INGESTING&quot; is. De foutdetails worden weergegeven als de status &quot;ERROR&quot; is. |  |

## Volgende stappen {#next-steps}

Door deze API-handleiding te volgen, hebt u de status van de werkbelasting gecontroleerd en aanbiedingen gedaan via de API [!DNL [!DNL Batch Decisioning]]. Voor meer informatie, zie het [&#x200B; overzicht over het Beheer van het Besluit &#x200B;](../../get-started/starting-offer-decisioning.md).
