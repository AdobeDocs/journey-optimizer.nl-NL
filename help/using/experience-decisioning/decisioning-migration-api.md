---
title: Migratie-API voor besluitvorming
description: Leer hoe u de API voor beslissingsmigratieservice gebruikt om beslissingsbeheerobjecten te migreren tussen sandboxen met automatische resolutie van afhankelijkheid en ondersteuning voor terugdraaien.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
source-git-commit: 398d4c2ab3a2312a0af5b8ac835f7d1f49a61b5b
workflow-type: tm+mt
source-wordcount: '1154'
ht-degree: 0%

---


# Migratie-API voor besluitvorming {#decisioning-migration-api}

Met de API voor beslissingsmigratieservice kunt u beslissingsbeheerobjecten migreren van de ene naar de andere sandbox. Het migratieproces wordt uitgevoerd als asynchrone workflows die afhankelijkheidsanalyse, uitvoering en optionele terugdraaimogelijkheden omvatten.

Met deze API kunt u uw beslissingsinhoud naadloos overbrengen tussen omgevingen (bijvoorbeeld van ontwikkeling naar staging of staging naar productie) en tegelijk de integriteit en relaties van de gegevens behouden.

Om over de voordelen en de mogelijkheden van Beslissing in vergelijking met het beheer van het Besluit te leren, verwijs naar [&#x200B; deze pagina &#x200B;](migrate-to-decisioning.md).

## Mogelijkheden {#capabilities}

De API voor de beslissingsmigratieservice biedt de volgende mogelijkheden:

* **Analyse van de Afhankelijkheid** - identificeer alle vereiste gebiedsdelen tussen bron en doelzandbakken, met inbegrip van attributen, segmenten, en datasetvereisten.
* **Flexibel migratiewerkingsgebied** - de migraties van de Looppas bij zandbak, aanbieding, of beslissingsniveau dat op uw behoeften wordt gebaseerd.
* **de steun van het Terugschroeven van prijzen** - keert een voltooide migratie terug als de kwesties tijdens bevestiging worden ontdekt.

## Vereisten {#prerequisites}

### Vereiste machtigingen {#permissions}

Als u de migratie-API wilt gebruiken, hebt u de juiste machtigingen nodig in zowel de bron- als doelsandboxen:

**zandbak van Source** - lees toegang tot de voorwerpen van het Beslissingsbeheer

**zandbak van het Doel** - creeer en geef toegang tot Beslissende voorwerpen uit

Tot de gebruikelijke machtigingen behoren:

* Beslissing beheren/weergeven
* Besluiten beheren/weergeven
* Aanbiedingen beheren
* Rangestrategieën beheren
* Campagnes beheren (als u campagnerelateerde artefacten migreert)
* Gegevensstromen beheren/weergeven (als u een gegevensstroom maakt)
* Schema&#39;s beheren/weergeven

>[!NOTE]
>
>Leer hoe te om de toestemmingen van Beslissing in [&#x200B; toe te wijzen deze sectie &#x200B;](gs-experience-decisioning.md#steps). Voor de volledige lijst van toestemmingen, verwijs naar de [&#x200B; Ingebouwde toestemmingen &#x200B;](../administration/ootb-permissions.md#ootb-permissions) pagina.

### De doelsandbox voorbereiden {#target-sandbox-preparation}

Controleer voordat u een migratie uitvoert of de doelsandbox correct is geconfigureerd:

* **Attributen** - verifieer dat de vereiste profielattributen en contextattributen in de doelzandbak bestaan, of voorbereidingen treffen afbeeldingen voor hen.
* **Segmenten** - verzeker vereiste segmenten in de doelzandbak bestaan, of van plan zijn om hen in kaart te brengen gebruikend namespace en identiteitskaart
* **Dataset** - identificeer een datasetnaam voor de migratie (`dependency.datasetName`) te gebruiken.
* **DataStream** - besluit of de migratie een gegevensstroom (`createDataStream`) zou moeten tot stand brengen.

Voor meer informatie over zandbakbeheer, verwijs naar [&#x200B; Gebruik en wijs zandbakken &#x200B;](../administration/sandboxes.md) toe.

## Basisprincipes van API&#39;s {#api-basics}

### Basis-URL&#39;s {#base-urls}

Gebruik de volgende basis-URL&#39;s, afhankelijk van uw omgeving:

* **Productie**: `https://platform.adobe.io`
* **het Staging**: `https://platform-stage.adobe.io`

### Verificatie {#authentication}

Voor alle API-aanvragen zijn de volgende headers vereist:

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `x-api-key: <CLIENT_API_KEY>`
* `Content-Type: application/json`

Voor gedetailleerde instructies bij vestiging authentificatie, verwijs naar de [&#x200B; de authentificatiegids van Journey Optimizer &#x200B;](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

### Workflowmodel {#workflow-model}

Elke API-aanroep maakt of haalt een bron van een workflow op. Workflows zijn asynchrone bewerkingen die de voortgang en de resultaten van migratietaken volgen.

Een werkstroom heeft de volgende eigenschappen:

* `id` - Unieke workflow-id (UUID)
* `status` - Huidige workflowstatus: `New`, `Running`, `Completed`, `Failed` of `Cancelled`
* `result` - Workflowuitvoer na voltooiing (inclusief migratieresultaten en waarschuwingen)
* `errors` - Gestructureerde foutdetails wanneer mislukt
* `_etag` - Versie-id die wordt gebruikt voor verwijderbewerkingen (alleen voor servicegebruikers)
* `_links.self` - Workflow URL voor het ophalen van status

## Migratieworkflow {#migration-workflow}

Het migratieproces bestaat uit twee hoofdstappen: het analyseren van afhankelijkheden en het uitvoeren van de migratie. Voer de volgende stappen uit om een geslaagde migratie te garanderen.

### Stap 1: Afhankelijkheden analyseren {#analyze-dependencies}

Voordat u gaat migreren, gebruikt u de afhankelijkheidsworkflow om te bepalen wat er moet worden toegewezen van beslissingsbeheer aan besluitvorming in de doelsandbox. Met deze analyse kunt u de relaties tussen objecten begrijpen en de benodigde toewijzingen voorbereiden.

#### Een afhankelijkheidsworkflow maken {#create-dependency-workflow}

Gebruik de volgende API-aanroep om een workflow voor afhankelijkheidsanalyse te maken.

**API formaat**

```http
POST /migration/service/dependency
```

**zandbak-vlakke gebiedsdeel (geadviseerd eerst)**

Begin met een zandbak-vlakke analyse om een volledige mening van alle gebiedsdelen te krijgen:

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/dependency" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "requestLevel": "sandbox"
  }'
```

**Offer-vlakke gebiedsdeel**

Als u alleen afhankelijkheden voor specifieke aanbiedingen wilt analyseren, stelt u `requestLevel: "offer"` in en verstrekt u een `offersList` -array met de aanbod-id&#39;s die u wilt analyseren.

**besluit-vlakke gebiedsdeel**

Als u alleen afhankelijkheden voor specifieke beslissingen wilt analyseren, stelt u `requestLevel: "decision"` in en verstrekt u een `decisionsList` -array met de beslissing-id&#39;s die u wilt analyseren.

#### Status afhankelijkheidswerkstroom controleren {#poll-dependency-status}

Opiniepeilen de afhankelijkheidsworkflow om te controleren of de analyse is voltooid.

**API formaat**

```http
GET /migration/service/dependency/{id}
```

**Verzoek**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/dependency/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

Wanneer het veld `status` `Completed` weergeeft, is de afhankelijkheidsanalyse gereed. Gebruik de workflowuitvoer om uw migratie-afhankelijkheidstoewijzingen te maken:

* **profileAttributeDependency** - de attributen van het bronprofiel van Kaarten aan de attributen van het doelprofiel
* **contextAttributeDependency** - de attributen van de broncontext van Kaarten aan de attributen van de doelcontext
* **segmentsDependency** - Kaarten bronsegmentsleutels aan doelsegmentherkenningstekens (`{segmentNamespace, segmentId}`)
* **datasetName** - specificeert de naam van de doeldataset voor de migratie

### Stap 2: De migratie uitvoeren {#execute-migration}

Nadat u de afhankelijkheden hebt geanalyseerd en uw toewijzingen hebt voorbereid, kunt u de migratie uitvoeren.

#### Een migratieworkflow maken {#create-migration-workflow}

Gebruik de gebiedsafhankelijkheidstoewijzingen van Stap 1 om uw migratie te vormen en uit te voeren.

**API formaat**

```http
POST /migration/service/migrations
```

**zandbak-vlakke migratie**

Alle beslissingsobjecten migreren van de ene naar de andere sandbox:

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/migrations" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributeDependency": {
        "sourceAttr1": "targetAttr1"
      },
      "segmentsDependency": {
        "sourceSegmentKey1": {
          "segmentNamespace": "<TARGET_SEGMENT_NAMESPACE>",
          "segmentId": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributeDependency": {
        "sourceCtx1": "targetCtx1"
      },
      "datasetName": "<TARGET_DATASET_NAME>"
    },
    "requestLevel": "sandbox"
  }'
```

**verschuiving-vlakke**

Als u alleen specifieke aanbiedingen wilt migreren, gebruikt u `requestLevel: "offer"` en voegt u een array `offersList` toe:

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**besluit-vlakke migratie**

Als u alleen specifieke beslissingen wilt migreren, gebruikt u `requestLevel: "decision"` en voegt u een array `decisionsList` toe:

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

#### Migratiestatus bewaken {#poll-migration-status}

Opiniepeiling de migratieworkflow om de voortgang ervan te volgen.

**API formaat**

```http
GET /migration/service/migrations/{id}
```

**Verzoek**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/migrations/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

**de resultaten van de Migratie**

Wanneer het veld `status` `Completed` weergeeft, is de migratie gelukt. De workflow `result` bevat:
* Toewijzingen van gemigreerde objecten
* Alle waarschuwingen die tijdens de migratie zijn aangetroffen

Wanneer het veld `status` `Failed` weergeeft, bekijkt u de array `errors[]` en het veld `result.error` voor meer informatie over wat er fout is gegaan.

## Uw migratie valideren {#validate-migration}

Nadat de migratie is voltooid, controleert u of alle objecten correct zijn gemigreerd.

### Controlelijst voor validatie {#validation-checklist}

1. **Segmenten** - verifieer dat alle referenced segmenten correct in de doelzandbak volgens uw afbeeldingen oplossen.
2. **Attributen** - bevestig dat alle profielattributen en contextattributen in de doelzandbak bestaan en correct in kaart gebracht.
3. **Beslissende voorwerpen** - Overzicht gemigreerde voorwerpen in het gebruikersinterface van Journey Optimizer:
   * Voorstellen (beslissingspunten)
   * Subsidiabiliteitsregels
   * Beoordelingsformule
   * Selectiestrategieën
   * Beslissingsbeleid
4. **het testen van DataStream** - als een gegevensstroom werd gecreeerd, test runtime levering gebruikend Edge Interact API.

### Voorbeeld {#test-runtime-delivery}

Als uw migratie een datastream heeft gemaakt, kunt u de levering van de aanbieding testen aan de hand van het volgende voorbeeld:

```shell
curl --request POST \
  --url "https://edge.adobedc.net/ee/or2/v1/interact?configId=<DATASTREAM_ID>" \
  --header "Content-Type: application/json" \
  --header "x-request-id: <uuid>" \
  --data '{ "events": [ ... ] }'
```

## Een migratie terugdraaien {#rollback}

Als u tijdens de validatie problemen ontdekt, kunt u een voltooide migratie terugdraaien om de vorige status van de doelsandbox te herstellen.

### Een terugdraaiworkflow maken {#create-rollback-workflow}

Start een terugdraaiactie door een terugdraaiworkflow te maken die verwijst naar de migratie die u wilt terugdraaien.

**API formaat**

```http
POST /migration/service/rollbacks/{migrationWorkflowId}
```

Vervang `{migrationWorkflowId}` door de id van de migratieworkflow die u wilt terugdraaien.

**Verzoek**

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/rollbacks/<MIGRATION_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

### Terugdraaistatus van monitor {#poll-rollback-status}

Opiniepeiling de terugdraaiworkflow om de voortgang te volgen.

**API formaat**

```http
GET /migration/service/rollbacks/{rollbackWorkflowId}
```

**Verzoek**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/rollbacks/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

## Gelijktijdige workflows verwerken {#handle-concurrency}

Met de migratie-API kan slechts één workflow tegelijk per organisatie worden uitgevoerd. Als u probeert om een nieuw werkschema tot stand te brengen terwijl een andere lopend is, zult u a **409 Conflict** foutenreactie ontvangen (&quot;een werkschema is reeds lopend...&quot;).

In dit geval wacht u tot de actieve workflow is voltooid of haalt u de workflow-id op en bekijkt u de status. Nadat de huidige workflow is voltooid, kunt u een nieuwe maken.

## Koppelingsverwijzing naar entiteit {#entity-mapping}

Bij de migratie van beslissingsbeheer naar besluitvorming worden de entiteiten als volgt toegewezen:

| Beslissingsbeheer | Beslissing |
|-------------------|-------------|
| Voorstel | Beslissingsitem |
| Verzameling voorstellen | Itemverzameling |
| Subsidiabiliteitsregel | Subsidiabiliteitsregel |
| Willekeurige formule | Willekeurige formule |
| Besluit | Selectiestrategie + beslissingsbeleid |
| Campaign | Campagne *(basisinhoud slechts)* |
| Plaatsing | Oppervlak + kanaalconfiguratie |
| Tag | Verenigde markering |

## Opschonen van workflow {#cleanup}

De middelen van het werkschema kunnen door de dienstgebruikers slechts worden geschrapt. Voor verwijderingsbewerkingen is een `If-Match` header met de `_etag` -waarde van de workflow vereist.

**Beschikbare schrappingsverrichtingen:**

* `DELETE /migration/service/dependency/{id}`
* `DELETE /migration/service/migrations/{id}`
* `DELETE /migration/service/rollbacks/{id}`

>[!NOTE]
>
>De schrapping van het werkschema is slechts beschikbaar aan de dienstrekeningen met aangewezen toestemmingen. Als u een werkschemabron moet schrappen, contacteer uw systeembeheerder.

## Verwante onderwerpen {#related-topics}

* [&#x200B; Migreer van het beheer van Besluit aan Beslissing &#x200B;](migrate-to-decisioning.md) - begrijp de voordelen en de mogelijkheden van het migreren aan Beslissing
* [Aan de slag met beslissing](gs-experience-decisioning.md)
* [Beslissingsinstructies en beperkingen](decisioning-guardrails.md)
* [Aan de slag met beslissing-API&#39;s](api-reference/getting-started.md)
