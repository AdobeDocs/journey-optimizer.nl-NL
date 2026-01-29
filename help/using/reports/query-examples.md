---
solution: Journey Optimizer
product: journey optimizer
title: Voorbeelden van query's
description: Voorbeelden van query's
feature: Reporting, Journeys
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 26ad12c3-0a2b-4f47-8f04-d25a6f037350
source-git-commit: 4a15ee3ac4805880ce80f788e4619b501afb3d8b
workflow-type: tm+mt
source-wordcount: '3337'
ht-degree: 1%

---

# Voorbeelden van query&#39;s{#query-examples}

Deze sectie verstrekt algemeen gebruikte voorbeelden om de Gebeurtenissen van de Stap van de Reis in het meer van Gegevens te vragen. Voordat u naar specifieke gebruiksgevallen gaat, is het belangrijk dat u de belangrijkste id&#39;s begrijpt die worden gebruikt in de gegevens van reisgebeurtenissen.

Zorg ervoor dat de gebieden die in uw vragen worden gebruikt waarden in het overeenkomstige schema hebben geassocieerd.

## Belangrijke id&#39;s {#key-identifiers}

+++Wat is het verschil tussen id, instanceID en profileID

* id: uniek voor alle items van de step-gebeurtenis. Twee verschillende step-gebeurtenissen kunnen niet dezelfde id hebben.
* instanceID: instanceID is het zelfde voor alle step gebeurtenissen verbonden aan een profiel binnen een reis uitvoering. Als een profiel de reis opnieuw ingaat, zal een verschillende instanceID worden gebruikt. Deze nieuwe instanceID zal voor alle step gebeurtenissen van de opnieuw ingegaan instantie (van begin tot eind) gelijk zijn.
* profileID: de identiteit van het profiel die overeenkomt met de naamruimte van de reis.

>[!NOTE]
>
>Voor het oplossen van problemendoeleinden, adviseren wij gebruikend tripVersionID in plaats van tripVersionName wanneer het vragen van reizen. Leer meer over de attributen van de reiseigenschappen [&#x200B; in deze sectie &#x200B;](../building-journeys/expression/journey-properties.md#journey-properties-fields).

+++

## Basis gebruiksgevallen/gemeenschappelijke vragen {#common-queries}

+++Hoeveel profielen een reis in een bepaald tijdkader inging

Deze vraag geeft het aantal verschillende profielen die de bepaalde reis in het bepaalde tijdkader inging.

_de vraag van het meer van Gegevens_

```sql
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND _experience.journeyOrchestration.stepEvents.instanceType = 'unitary'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour);
```

Leer hoe te [&#x200B; verworpen gebeurtenistypen in reis_step_events &#x200B;](../reports/sharing-field-list.md#discarded-events) problemen oplossen.

+++

+++Welke regel ertoe heeft geleid dat een profiel geen bepaalde reis heeft gemaakt

Deze vraag keert de verworpen regels en regelinformatie terug wanneer een profiel om een reis wegens maximum of geschiktheidsregels wordt verhinderd in te gaan.

_Voorbeeld_

```sql
SELECT 
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.ID AS RULESET_ID,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.name AS RULESET_NAME,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.rejectedRules.ID AS RULE_ID,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.rejectedRules.name AS RULE_NAME
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard'
AND
    _experience.journeyOrchestration.stepEvents.journeyVersionID='3855072d-79c3-438a-a5c3-c77fd6843812'
AND
    timestamp >= to_date('2025-05-16')
```

+++

+++Welke regel ertoe heeft geleid dat een profiel geen reisactie heeft ontvangen

Deze vraag keert de details van de step gebeurtenis voor profielen terug die tijdens een reis werden verworpen en geen reisactie ontvingen. Het helpt identificeren waarom de profielen wegens bedrijfsregels zoals rustige uurbeperkingen werden verworpen.

_de vraag van het meer van Gegevens_

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.profileID,
    _experience.journeyOrchestration.stepEvents.instanceID,
    _experience.journeyOrchestration.stepEvents.journeyID,
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.actionExecutionError,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType,
    DATE(timestamp),
    timestamp
FROM journey_step_events
WHERE
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType = '<eventType>' AND
    _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>' AND
    _experience.journeyOrchestration.stepEvents.instanceID = '<instanceID>';
```

_Voorbeeld_

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.profileID,
    _experience.journeyOrchestration.stepEvents.instanceID,
    _experience.journeyOrchestration.stepEvents.journeyID,
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.actionExecutionError,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType,
    DATE(timestamp),
    timestamp
FROM journey_step_events
WHERE
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'quietHours' AND
    _experience.journeyOrchestration.stepEvents.journeyVersionID = '6f21a072-6235-4c39-9f6a-9d9f3f3b2c3a' AND
    _experience.journeyOrchestration.stepEvents.instanceID = 'unitary_089dc93a-1970-4875-9660-22433b18e500';
```


De vraagresultaten tonen zeer belangrijke gebieden die helpen de reden voor profielverwerping identificeren:

* **actionExecutionError** - Wanneer reeks aan `businessRuleProfileDiscarded`, wijst dit op het profiel werd verworpen toe aan een bedrijfsregel. Het veld `eventType` bevat aanvullende details over de specifieke bedrijfsregel die de verwijdering heeft veroorzaakt.

* **eventType** - specificeert het type van bedrijfsregel die verwerpen veroorzaakte:
   * `quietHours`: Profiel is verwijderd vanwege configuratie van stille uren
   * `forcedDiscardDueToQuietHours`: Profiel is geforceerd verwijderd omdat de maximale hoeveelheid vervorming is bereikt voor profielen die in stille uren zijn bewaard

+++

+++Hoeveel fouten voorkwamen op elke knoop van een specifieke reis voor een bepaalde hoeveelheid tijd

Deze vraag telt de duidelijke profielen die fouten bij elke knoop van een reis ervoeren, die door knoopnaam wordt gegroepeerd. Het omvat alle soorten fouten van de actieuitvoering en haal fouten.

_de vraag van het meer van Gegevens_

```sql
SELECT
_experience.journeyOrchestration.stepEvents.nodeName,
count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour)
AND
  (_experience.journeyOrchestration.stepEvents.actionExecutionError is not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode is not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionOriginCode is not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionOriginError is not NULL
    OR _experience.journeyOrchestration.stepEvents.fetchError is not NULL
    OR _experience.journeyOrchestration.stepEvents.fetchErrorCode is not NULL
  )
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

+++

+++Hoeveel gebeurtenissen van een specifieke reis in een bepaald tijdkader werden verworpen

Deze vraag telt het totale aantal gebeurtenissen die van een reis werden verworpen. Het filter filtert voor diverse verworpen gebeurteniscodes met inbegrip van de fouten van de segmentuitvoer, de teruggooi van de verzender, en staatsmachine verwerpen.

_de vraag van het meer van Gegevens_

```sql
SELECT
count(_id) AS NUMBER_OF_EVENTS_DISCARDED
FROM journey_step_events
WHERE (
   _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'error'
   OR _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard'
   OR _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode = 'discard'
   OR _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode is not null
)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour);
```

+++

+++Wat gebeurt er met een specifiek profiel in een specifieke reis in een specifieke tijdspanne

Deze vraag keert alle step gebeurtenissen en de dienstgebeurtenissen voor het bepaalde profiel en reis voor de gespecificeerde tijd in chronologische orde terug.

_de vraag van het meer van Gegevens_

```sql
SELECT
timestamp,
_experience.journeyOrchestration.stepEvents.journeyVersionID,
_experience.journeyOrchestration.stepEvents.profileID,
_experience.journeyOrchestration.stepEvents.nodeName,
_experience.journeyOrchestration.stepEvents.journeyNodeProcessed,
_experience.journeyOrchestration.serviceType,
to_json(_experience.journeyOrchestration.profile),
to_json(_experience.journeyOrchestration.serviceEvents)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour)
AND
  (
    _experience.journeyOrchestration.stepEvents.profileID='<profileID>'
    OR _experience.journeyOrchestration.profile.ID='<profileID>'
  );
ORDER BY timestamp;
```

+++

+++Hoeveel tijd is verstreken tussen twee knopen 

Deze vragen kunnen, bijvoorbeeld, worden gebruikt om de tijd te schatten die in een wachttijdactiviteit wordt doorgebracht. Dit staat u toe om ervoor te zorgen dat de wachttijdactiviteit correct wordt gevormd.

_de vraag van het meer van Gegevens_

```sql
WITH

START_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_START,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of node before wait activity>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
),

END_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_END,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of wait activity node>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
)

SELECT 

    T1.INSTANCE_ID AS INSTANCE_ID,
    T1.NODE_NAME AS START_NODE_NAME,
    T2.NODE_NAME AS END_NODE_NAME,
    DATEDIFF(millisecond,T1.TS_START,T2.TS_END) AS ELAPSED_TIME_MS
    
FROM

    START_NODE_INFO AS T1,
    END_NODE_INFO AS T2
    
WHERE

    T1.INSTANCE_ID = T2.INSTANCE_ID
```

_de vraag van het meer van Gegevens_

```sql
WITH

START_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_START,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of node before wait activity>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
),

END_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_END,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of wait activity node>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
)

SELECT 

    AVG(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS AVERAGE_ELAPSED_TIME,
    MIN(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS MIN_ELAPSED_TIME,
    MAX(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS MAX_ELAPSED_TIME
    
FROM

    START_NODE_INFO AS T1,
    END_NODE_INFO AS T2
    
WHERE

    T1.INSTANCE_ID = T2.INSTANCE_ID
```

+++

+++De details van een serviceEvent controleren 

De dataset van de Gebeurtenissen van de Stap van de Reis bevat alle stepEvents en serviceEvents. stepEvents worden gebruikt bij de rapportage, aangezien ze betrekking hebben op activiteiten (gebeurtenis, acties, enz.) van profielen tijdens een reis. serviceEvents worden opgeslagen in de zelfde dataset, en zij wijzen op extra informatie voor het zuiveren doeleinden, bijvoorbeeld de reden voor een ervaringsgebeurtenis verwerpen.

Hier is een voorbeeld van vraag om de details van een serviceEvent te controleren:

_de vraag van het meer van Gegevens_

```sql
SELECT

     _experience.journeyOrchestration.profile.ID, 
     _experience.journeyOrchestration.journey.versionID, 
     to_json(_experience.journeyOrchestration.serviceEvents) 

FROM journey_step_event 

WHERE _experience.journeyOrchestration.serviceType is not null;
```

## Bericht-/handelingsfouten {#message-action-errors}

+++Lijst van fouten tijdens reizen

Met deze query kunt u elke fout die tijdens reizen is aangetroffen, weergeven tijdens het uitvoeren van een bericht/handeling.

```sql
SELECT _experience.journeyOrchestration.stepEvents.actionExecutionError, count(distinct _id) AS ERROR_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeName = '<message-name>'
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY _experience.journeyOrchestration.stepEvents.actionExecutionError
ORDER BY ERROR_COUNT DESC;
```

_de output van de Steekproef_

| actionExecutionError | ERROR_COUNT |
|---|---|
| TimedOut | 145 |
| ErrorConnecting | 87 |
| InvalidResponse | 23 |

Deze vraag keert alle verschillende fouten terug die terwijl het uitvoeren van een actie in een reis samen met de telling van hoe vaak elke fout voorkwam, die door frequentie wordt bevolen.

+++

## Op profielen gebaseerde query&#39;s {#profile-based-queries}

+++Zoeken of een profiel een specifieke reis heeft ingevoerd

Deze vraag controleert of een specifiek profiel een reis inging door de gebeurtenissen te tellen verbonden aan die profiel en reiscombinatie.

```sql
SELECT count(distinct _id) AS EVENT_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>';
```

_de output van de Steekproef_

| EVENT_COUNT |
|---|
| 3 |

Deze vraag keert het nauwkeurige aantal tijden terug een profiel een reis is ingegaan. Een resultaat groter dan 0 bevestigt dat het profiel de reis inging.

+++

+++Zoeken of een profiel een specifiek bericht is verzonden

Methode 1: als de naam van uw bericht niet uniek is in de reis (het wordt gebruikt op veelvoudige plaatsen).

```sql
SELECT count(distinct _id) AS MESSAGE_SENT_COUNT 
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.nodeID = '<NodeId in the UI corresponding to the message>' 
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL 
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>';
```

_de output van de Steekproef_

| MESSAGE_SENT_COUNT |
|---|
| 1 |

Een resultaat groter dan 0 bevestigt dat de berichtactie met succes werd uitgevoerd. Deze vraag vertelt ons slechts of de berichtactie met succes op de reiskant werd uitgevoerd.

Methode 2: als de naam van uw bericht uniek is in de reis.

```sql
SELECT count(distinct _id) AS MESSAGE_SENT_COUNT 
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.nodeName = '<NodeName in the UI corresponding to the message>' 
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL 
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>';
```

_de output van de Steekproef_

| MESSAGE_SENT_COUNT |
|---|
| 1 |

De query retourneert het aantal keren dat het bericht is aangeroepen voor het geselecteerde profiel.

+++

+++Zoeken naar alle berichten die een profiel in de afgelopen 30 dagen heeft ontvangen

Met deze query worden alle berichthandelingen voor een specifiek profiel in de afgelopen 30 dagen opgehaald, gegroepeerd op berichtnaam.

```sql
SELECT _experience.journeyOrchestration.stepEvents.nodeName AS MESSAGE_NAME, 
       count(distinct _id) AS MESSAGE_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL 
AND _experience.journeyOrchestration.stepEvents.nodeType = 'action' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' 
AND timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName
ORDER BY MESSAGE_COUNT DESC;
```

_de output van de Steekproef_

| MESSAGE_NAME | MESSAGE_COUNT |
|---|---|
| Welkom-e-mail | 1 |
| Productaanbeveling | 3 |
| Herinnering voor afhandeling van winkelwagentje | 2 |
| Wekelijkse nieuwsbrief | 4 |

De vraag keert de lijst van alle berichten samen met hun telling terug die voor het geselecteerde profiel wordt aangehaald.

+++

+++Zoeken naar alle ritten die een profiel in de afgelopen 30 dagen heeft ingevoerd

Deze vraag keert alle reizen terug die een specifiek profiel binnen de laatste 30 dagen, samen met de ingangstelling voor elke reis is ingegaan.

```sql
SELECT _experience.journeyOrchestration.stepEvents.journeyVersionName AS JOURNEY_NAME, 
       count(distinct _id) AS ENTRY_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeType = 'start' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' 
AND timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.journeyVersionName
ORDER BY ENTRY_COUNT DESC;
```

_de output van de Steekproef_

| JOURNEY_NAME | ENTRY_COUNT |
|---|---|
| Welkomstreis v2 | 1 |
| Aanbevelingen voor producten | 5 |
| Campagne voor opnieuw engagement | 2 |

De vraag keert de lijst van alle reisnamen samen met het aantal tijden terug het gevraagde profiel ingegaan elke reis.

+++

+++Aantal profielen dat in aanmerking kwam voor een dagelijkse reis

Deze vraag verstrekt een dagelijkse uitsplitsing van het aantal verschillende profielen die een reis over een gespecificeerde tijdspanne inging.

```sql
SELECT DATE(timestamp) AS ENTRY_DATE, 
       count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS PROFILES_COUNT 
FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) DESC;
```

_de output van de Steekproef_

| ENTRY_DATE | PROFILES_COUNT |
|---|---|
| 25-11-2024 | 1.245 |
| 24-11-2024 | 1.189 |
| 23-11-2024 | 15.340 |
| 22-11-2024 | 1.205 |
| 21-11-2024 | 1.167 |

De vraag keert, voor de bepaalde periode, het aantal profielen terug dat de reis elke dag inging. Als een profiel wordt ingevoerd via meerdere identiteiten, wordt het twee keer geteld. Als de terugkeer wordt toegelaten, zou het profielaantal over verschillende dagen kunnen worden gedupliceerd als het de reis op een verschillende dag opnieuw inging.

Leer hoe te [&#x200B; verworpen gebeurtenistypen in reis_step_events &#x200B;](../reports/sharing-field-list.md#discarded-events) problemen oplossen.


+++

## Vragen met betrekking tot het leespubliek {#read-segment-queries}

+++Tijd die nodig is om een doelexporttaak te voltooien

Deze vraag berekent de duur van een publiek de uitvoerbaan door het tijdverschil tussen te vinden wanneer de baan een rij werd gevormd en wanneer het eindigde.

```sql
select DATEDIFF (minute,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'queued') ,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'finished')) AS export_job_runtime;
```

De vraag keert het tijdverschil, in notulen, tussen terug wanneer de publiek uitvoerbaan een rij werd gevormd en wanneer het definitief eindigde.

+++

+++Aantal profielen dat tijdens de rit is verwijderd omdat het dubbele profielen waren

Deze vraag telt het aantal verschillende profielen die wegens instantie duplicatiefouten tijdens de Gelezen activiteit van het Publiek werden verworpen.

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_DUPLICATION'
```

De vraag keert alle profielID terug die door de reis werden verworpen omdat zij duplicaten waren.

+++

+++Aantal profielen dat door de reis wegens ongeldige namespace is verworpen

Deze query retourneert het aantal profielen dat is verwijderd omdat deze een ongeldige naamruimte of een ontbrekende identiteit voor de vereiste naamruimte hadden.

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_BAD_NAMESPACE'
```

De query retourneert alle profiel-id&#39;s die door de rit zijn verwijderd omdat ze een ongeldige naamruimte of geen identiteit voor die naamruimte hadden.

+++

+++Aantal profielen dat door de reis wegens geen identiteitskaart werd verworpen

Deze vraag telt de profielen die werden verworpen omdat zij een identiteitskaart ontbraken die voor reisuitvoering wordt vereist.

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NO_IDENTITY_MAP'
```

De vraag keert alle profielID terug die door de reis werden verworpen omdat de identiteitskaart ontbrak.

+++

+++Aantal profielen dat tijdens de rit is weggegooid omdat de rit zich in het testknooppunt bevond en het profiel geen testprofiel was

Deze vraag identificeert profielen die werden verworpen toen de reis op testwijze liep maar het profiel had niet de testProfile attributen die aan waar werd geplaatst.

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NOT_A_TEST_PROFILE'
```

De vraag keert alle profielID terug die door de reis werden verworpen omdat de uitvoerbaan op testwijze werd in werking gesteld maar het profiel had niet de testProfile attributen geplaatst aan waar.

+++

+++Aantal profielen dat door de reis wegens een interne fout werd verworpen

Deze vraag keert de telling van profielen terug die wegens interne systeemfouten tijdens reisuitvoering werden verworpen.

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_INTERNAL'
```

De vraag keert alle profielID terug die door de reis wegens één of andere interne fout werden verworpen.

+++

+++Overzicht van het leespubliek voor een bepaalde reisversie

Deze vraag verstrekt een uitvoerig overzicht van de Gelezen activiteit van de Publiek, met inbegrip van de details van de segmentuitvoer baan, gebeurteniscodes, statussen, en profieltellingen voor alle stadia van het proces van de publieksuitvoer.

_de vraag van het meer van Gegevens_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator'
```

Het zal alle de dienstgebeurtenissen terugkeren met betrekking tot de bepaalde reisversie. We kunnen de handelsketen volgen:

* onderwerp maken
* werkgelegenheid exporteren
* exporttaakbeëindiging (met maateenheden voor geëxporteerde profielen)
* verwerking van worker beëindigd

We kunnen ook problemen ontdekken zoals:

* fouten in onderwerp of de schepping van de uitvoerbaan (met inbegrip van onderbrekingen op de vraag van de publieksuitvoer API)
* uitvoerbanen die kunnen worden vastgehouden (wanneer voor een bepaalde reisversie geen enkele gebeurtenis plaatsvindt met betrekking tot de beëindiging van de exporttaken)
* problemen met workers als we een gebeurtenis voor het beëindigen van exporttaken hebben ontvangen, maar geen eindversie voor verwerking door worker één

BELANGRIJK: als er geen gebeurtenis is die door deze vraag wordt geretourneerd, kan dit aan een van de volgende redenen zijn te wijten:

* de reisversie heeft het schema niet bereikt
* als de reisversie de uitvoerbaan zou moeten teweegbrengen door de organisator te roepen, ging iets fout op de stroomopwaartse stroom: kwestie op reisplaatsing, bedrijfsgebeurtenis of kwestie met planner.

+++


+++Ontvang leesfouten voor een bepaalde reisversie

Deze query filtert voor specifieke foutgebeurteniscodes met betrekking tot leesfouten in het publiek, zoals fouten bij het maken van onderwerpen, API-aanroepfouten, time-outs en mislukte exporttaken.

_de vraag van het meer van Gegevens_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
        'ERROR_TOPIC_CREATION',
        'ERROR_EXPORTJOB_APICALL',
        'ERROR_EXPORTJOB_APICALL_TIMEOUT',
        'ERROR_EXPORTJOB_FAILED'
    )
```

+++

+++Status exporttaak ophalen

Deze query haalt de verwerkingsstatus van doelexporttaken op en geeft aan of dit gelukt of mislukt is, samen met maatstaven voor het exporteren van profielen.

_de vraag van het meer van Gegevens_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT 
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
        'INFO_EXPORTJOB_SUCCEEDED',
        'ERROR_EXPORTJOB_FAILED'
    )
```

Als er geen record wordt geretourneerd, betekent dit dat:

* er is een fout opgetreden tijdens het maken van een onderwerp of taak exporteren
* de exporttaak is nog actief

+++

+++Metrische gegevens over geëxporteerde profielen ophalen, inclusief gegevens over verwijderde taken en exporttaken voor elke exporttaak

Deze vraag combineert verworpen profieltellingen met de metriek van de uitvoerbaan om een volledige mening van publiek te verstrekken de uitvoerprestaties voor elke individuele uitvoerbaan.

_de vraag van het meer van Gegevens_

```sql
WITH
  
DISCARDED_EXPORTED_PROFILES AS (
  
    SELECT
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID AS EXPORTJOB_ID,
        count(distinct _experience.journeyOrchestration.profile.ID) AS DISCARDED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'ERROR_INSTANCE_DUPLICATION',
            'ERROR_INSTANCE_BAD_NAMESPACE',
            'ERROR_INSTANCE_NO_IDENTITY_MAP',
            'ERROR_INSTANCE_NOT_A_TEST_PROFILE',
            'ERROR_INSTANCE_INTERNAL'
        )
    GROUP BY
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID
 
),
  
SEGMENT_EXPORT_METRICS AS (
  
    SELECT
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID AS EXPORTJOB_ID,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal) AS TOTAL_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized) AS SUCCESS_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed) AS FAILED_EXPORTED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'INFO_EXPORTJOB_SUCCEEDED',
            'ERROR_EXPORTJOB_FAILED'
        )
    GROUP BY
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID
  
)
  
SELECT
    sum(T2.TOTAL_EXPORTED_PROFILES_COUNT),
    sum(T2.SUCCESS_EXPORTED_PROFILES_COUNT),
    sum(T2.FAILED_EXPORTED_PROFILES_COUNT),
    sum(T1.DISCARDED_PROFILES_COUNT)
FROM
    DISCARDED_EXPORTED_PROFILES AS T1,
    SEGMENT_EXPORT_METRICS AS T2
WHERE T1.EXPORTJOB_ID = T2.EXPORTJOB_ID
```

+++

+++Hiermee krijgt u geaggregeerde metriek (doelgroepen, exporttaken en verwijderde bestanden) voor alle exporttaken

Deze vraag aggregeert algemene metriek over alle uitvoerbanen voor een bepaalde reisversie, nuttig voor terugkomende reizen of zaken gebeurtenis-teweeggebrachte reizen met onderwerp hergebruik.

_de vraag van het meer van Gegevens_

```sql
WITH
  
DISCARDED_EXPORTED_PROFILES AS (
  
    SELECT
        _experience.journeyOrchestration.journey.versionID AS JOURNEYVERSION_ID,
        count(distinct _experience.journeyOrchestration.profile.ID) AS DISCARDED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'ERROR_INSTANCE_DUPLICATION',
            'ERROR_INSTANCE_BAD_NAMESPACE',
            'ERROR_INSTANCE_NO_IDENTITY_MAP',
            'ERROR_INSTANCE_NOT_A_TEST_PROFILE',
            'ERROR_INSTANCE_INTERNAL'
        )
    GROUP BY
        _experience.journeyOrchestration.journey.versionID
),
  
SEGMENT_EXPORT_METRICS AS (
  
    SELECT
        _experience.journeyOrchestration.journey.versionID AS JOURNEYVERSION_ID,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal) AS TOTAL_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized) AS SUCCESS_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed) AS FAILED_EXPORTED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'INFO_EXPORTJOB_SUCCEEDED',
            'ERROR_EXPORTJOB_FAILED'
        )
    GROUP BY
          _experience.journeyOrchestration.journey.versionID
 
)
  
SELECT
    sum(T2.TOTAL_EXPORTED_PROFILES_COUNT),
    sum(T2.SUCCESS_EXPORTED_PROFILES_COUNT),
    sum(T2.FAILED_EXPORTED_PROFILES_COUNT),
    sum(T1.DISCARDED_PROFILES_COUNT)
FROM
    DISCARDED_EXPORTED_PROFILES AS T1,
    SEGMENT_EXPORT_METRICS AS T2
WHERE T1.JOURNEYVERSION_ID = T2.JOURNEYVERSION_ID
```

Deze query is anders dan de vorige.

Het keert de algemene metriek voor een bepaalde reisversie terug, ongeacht de banen die voor het kunnen lopen (in het geval van terugkerende reizen, teweeggebrachte bedrijfsgebeurtenissen degenen die onderwerphergebruik leveraging).

+++

## Vragen in verband met de kwalificatie van het publiek {#segment-qualification-queries}

+++Profiel dat is verwijderd vanwege een ander publiek dan geconfigureerd

Deze vraag identificeert profielen die werden verworpen omdat hun status van de publieksrealisatie niet de configuratie van de Kwalificatie van het Publiek van de reis (b.v., die voor &quot;wordt gevormd&quot;maar profiel &quot;verlaten&quot;) aanpast.

_de vraag van het meer van Gegevens_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID
FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version id>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SEGMENT_REALISATION_CONDITION_MISMATCH'
```

_Voorbeeld_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID
FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = 'a868f3c9-4888-46ac-a274-94cdf1c4159d' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SEGMENT_REALISATION_CONDITION_MISMATCH'
```

Deze vraag keert alle profielID terug die door de reisversie wegens verkeerde publieksrealisatie werden verworpen.

+++

+++De gebeurtenissen van de Kwalificatie van het publiek die door een andere reden voor een specifiek profiel worden verworpen

Deze vraag wint al publiekskwalificatie of externe gebeurtenissen terug die voor een specifiek profiel wegens interne de dienstfouten werden verworpen.

_de vraag van het meer van Gegevens_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID, _experience.journeyOrchestration.serviceEvents.dispatcher.projectionID
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID = '<profile-id>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

_Voorbeeld_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID, _experience.journeyOrchestration.serviceEvents.dispatcher.projectionID
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID = 'mandee@adobe.com' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

Deze query retourneert alle gebeurtenissen (externe gebeurtenissen/kwalificatiegebeurtenissen voor het publiek) die vanwege een andere reden voor een profiel zijn genegeerd.

+++

## Op gebeurtenissen gebaseerde query&#39;s {#event-based-queries}

+++Controleren of een zakelijke gebeurtenis is ontvangen voor een reis

Deze vraag telt het aantal tijden een bedrijfsgebeurtenis door een reis, gegroepeerd door datum, binnen een gespecificeerd tijdkader werd ontvangen.

```sql
SELECT DATE(timestamp), count(distinct _id)
FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.nodeName = '<node-name-corresponding-to-business-event>' AND
_experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
WHERE DATE(timestamp) > (now() - interval '<last x hours>' hour)
```

+++

+++Controleren of een externe gebeurtenis van een profiel is verwijderd omdat er geen gerelateerde reis is gevonden

Deze vraag identificeert wanneer een externe gebeurtenis voor een specifiek profiel werd verworpen omdat er geen actieve of passende reis was die werd gevormd om die gebeurtenis te ontvangen.

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp) FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID = '<eventId>' AND
_experience.journeyOrchestration.profile.ID = '<profileID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'EVENT_WITH_NO_JOURNEY'
```

Leer hoe te [&#x200B; verworpen gebeurtenistypen in reis_step_events &#x200B;](../reports/sharing-field-list.md#discarded-events) problemen oplossen.

+++

+++Controleren of een externe gebeurtenis van een profiel om een andere reden is verwijderd

Deze query haalt externe gebeurtenissen op die zijn genegeerd voor een specifiek profiel vanwege interne servicefouten, samen met de gebeurtenis-id en foutcode.

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp), _experience.journeyOrchestration.serviceEvents.dispatcher.eventID, _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID='<profileID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID='<eventID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

Leer hoe te [&#x200B; verworpen gebeurtenistypen in reis_step_events &#x200B;](../reports/sharing-field-list.md#discarded-events) problemen oplossen.

+++

+++Controleer de telling van alle gebeurtenissen die door stateMachine door errorCode worden verworpen

Deze vraag aggregeert alle gebeurtenissen die door de machine van de reisstaat worden verworpen, die door foutencode wordt gegroepeerd helpen de gemeenschappelijkste redenen voor verwerping identificeren.

```sql
SELECT _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode, COUNT() FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' GROUP BY _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode
```

Leer hoe te [&#x200B; verworpen gebeurtenistypen in reis_step_events &#x200B;](../reports/sharing-field-list.md#discarded-events) problemen oplossen.

+++

+++Alle verwijderde gebeurtenissen controleren omdat toegang niet is toegestaan

Deze vraag identificeert alle gebeurtenissen die werden verworpen omdat een profiel probeerde om een reis opnieuw in te gaan wanneer de ingang niet in de reisconfiguratie werd toegestaan.

```sql
SELECT DATE(timestamp), _experience.journeyOrchestration.profile.ID,
_experience.journeyOrchestration.journey.versionID,
_experience.journeyOrchestration.serviceEvents.stateMachine.eventCode 
FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' AND _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode='reentranceNotAllowed'
```

Leer hoe te [&#x200B; verworpen gebeurtenistypen in reis_step_events &#x200B;](../reports/sharing-field-list.md#discarded-events) problemen oplossen.

+++

## Zoekopdrachten voor Ingageable Profiles {#engageable-profiles-queries}

Deze vragen helpen u uw Engageable Aantal Profielen controleren en analyseren. Een meetbaar profiel is een uniek profiel dat de afgelopen twaalf maanden is gebruikt voor reizen of campagnes. Leer meer over [&#x200B; Engageable Profielen en vergunningsgebruik &#x200B;](../audience/license-usage.md#what-is-engageable-profile).

>[!IMPORTANT]
>
>**Beste praktijken voor het vragen van toe te voegen Profielen:**
>* Zorg ervoor dat elk veld zonder aggregaat is opgenomen in de `GROUP BY` -component
>* Vermijd het van verwijzingen voorzien van datasets die niet in uw zandbak bestaan - bevestig datasetnamen in Platform UI
>* Gebruik `distinct` bij het tellen van unieke profielen om dubbele waarden in naamruimten te voorkomen
>* Wanneer u `LIMIT` gebruikt, plaatst u deze aan het einde van de query na `ORDER BY` -componenten

+++Unieke profielen tellen die worden gebruikt door een specifieke reis

Deze vraag keert het aantal verschillende profielen terug die door een specifieke reis zijn bezeten, die tot uw Engageable Aantal Profielen bijdraagt.

```sql
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
AND timestamp > (now() - interval '12' month);
```

Deze vraag helpt u begrijpen hoeveel unieke profielen een specifieke reis aan uw [&#x200B; toe te laten &#x200B;](../audience/license-usage.md) telling van Profielen in de afgelopen 12 maanden heeft bijgedragen.

+++

+++Telprofielen per reis in de laatste twaalf maanden

Deze vraag toont het aantal unieke profielen die door elke reis in uw organisatie in de voorbije 12 maanden worden geëngageerd, die u helpen identificeren welke reizen het meest aan uw [&#x200B; Engageable Aantal Profielen &#x200B;](../audience/license-usage.md) bijdragen.

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.journeyVersionID AS JOURNEY_VERSION_ID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName AS JOURNEY_NAME,
    count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '12' month)
GROUP BY 
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName
ORDER BY ENGAGED_PROFILES DESC;
```

_de output van de Steekproef_

| JOURNEY_VERSION_ID | JOURNEY_NAME | ENGAGED_PROFILES |
|---|---|---|
| 67b14482-143e-4f83-9cf5-cfec0fca3d26 | Welkomstcampagne v2 | 125.450 |
| a3c21b89-456d-4e21-b8f3-9a8e7c6d5432 | Reis voor starten van product | 98.230 |
| f9e8d7c6-b5a4-3210-9876-543210fedcba | Terugplaatsingsstroom | 45.670 |

Deze uitvoer helpt u te identificeren welke reizen de meeste profielen in dienst nemen en levert het belangrijkst een bijdrage aan uw Engageable Aantal Profielen.

>[!NOTE]
>
>Deze query groepeert zich door zowel `journeyVersionID` als `journeyVersionName` . Beide velden moeten worden opgenomen in de component `GROUP BY` omdat ze zijn geselecteerd in de query. Als u velden weglaat uit de component `GROUP BY` , mislukt de query.

+++

+++Telprofielen die de afgelopen 30 dagen dagelijks door reizen zijn gebruikt

Deze vraag verstrekt een dagelijkse uitsplitsing van onlangs betrokken profielen, die u helpen spikes in [&#x200B; identificeren Engageable Aantal Profielen &#x200B;](../audience/license-usage.md).

```sql
SELECT 
    DATE(timestamp) AS ENGAGEMENT_DATE,
    count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '30' day)
GROUP BY DATE(timestamp)
ORDER BY ENGAGEMENT_DATE DESC;
```

_de output van de Steekproef_

| ENGAGEMENT_DATE | ENGAGED_PROFILES |
|---|---|
| 25-11-2024 | 8.450 |
| 24-11-2024 | 7.820 |
| 23-11-2024 | 125.340 |
| 22-11-2024 | 9.230 |
| 21-11-2024 | 8.670 |

Met deze uitvoer kunt u dagelijkse trends volgen en bepalen wanneer grote aantallen profielen worden gebruikt. In dit voorbeeld, toont 23 November een significante piek (125.340 profielen) in vergelijking met typisch dagelijkse overeenkomst (~8.000 profielen), die onderzoek zou rechtvaardigen om te begrijpen welke reis of campagne de toename in uw [&#x200B; toe te laten Aantal Profielen &#x200B;](../audience/license-usage.md) veroorzaakte.

+++

+++Reizen identificeren waarbij onlangs een groot publiek betrokken was

Deze vraaghulp identificeert welke reizen grote aantallen nieuwe profielen in recente tijdsperiodes hebben geëngageerd, die plotselinge verhogingen in [&#x200B; toe te laten &#x200B;](../audience/license-usage.md) telling van Profielen kunnen verklaren.

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.journeyVersionID AS JOURNEY_VERSION_ID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName AS JOURNEY_NAME,
    DATE(timestamp) AS ENGAGEMENT_DATE,
    count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '7' day)
AND _experience.journeyOrchestration.stepEvents.nodeType = 'start'
GROUP BY 
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName,
    DATE(timestamp)
HAVING count(distinct _experience.journeyOrchestration.stepEvents.profileID) > 1000
ORDER BY ENGAGEMENT_DATE DESC, ENGAGED_PROFILES DESC;
```

_de output van de Steekproef_

| JOURNEY_VERSION_ID | JOURNEY_NAME | ENGAGEMENT_DATE | ENGAGED_PROFILES |
|---|---|---|---|
| 67b14482-143e-4f83-9cf5-cfec0fca3d26 | Zwarte vrijdagcampagne | 23-11-2024 | 125.340 |
| a3c21b89-456d-4e21-b8f3-9a8e7c6d5432 | Reis voor starten van product | 22-11-2024 | 45.230 |
| f9e8d7c6-b5a4-3210-9876-543210fedcba | Nieuwsbrief van feestdag | 21-11-2024 | 32.150 |

Deze zoekopdracht filtert op reizen die de afgelopen 7 dagen meer dan 1.000 profielen per dag hebben gebruikt. Uit de resultaten blijkt welke specifieke reizen en data verantwoordelijk zijn voor grote profielvluchten. Pas de componentendrempel `HAVING` aan op basis van uw behoeften (wijzig bijvoorbeeld `> 1000` in `> 10000` voor grotere drempels).

+++

+++Totaal aantal unieke profielen voor alle reizen in de laatste twaalf maanden

Deze query bevat een aantal unieke profielen die tijdens alle reizen in de afgelopen 12 maanden zijn gebruikt, zodat u een overzicht krijgt van uw op een reis gebaseerde betrokkenheid.

```sql
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS TOTAL_ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '12' month);
```

_de output van de Steekproef_

| TOTAL_ENGAGED_PROFILES |
|---|
| 2.547.890 |

Dit ene getal staat voor het totale aantal unieke profielen dat in de afgelopen twaalf maanden door ten minste één reis is gebruikt.

>[!NOTE]
>
>Deze vraag telt duidelijke profiel IDs in de de gebeurtenisdataset van de de reisstap. De daadwerkelijke die Aantal van Profielen van Engageable in het [&#x200B; dashboard van het Gebruik van de Vergunning &#x200B;](../audience/license-usage.md) worden getoond kan lichtjes verschillen, aangezien het ook profielen omvat die door campagnes en andere mogelijkheden van Journey Optimizer voorbij reizen worden aangehaald.

+++

## Algemene vragen op basis van reizen {#journey-based-queries}

+++Aantal dagelijkse actieve reizen

Deze vraag keert een dagelijks aantal unieke reisversies terug die activiteit hadden, die u helpen patronen van de reisuitvoering in tijd begrijpen.

```sql
SELECT DATE(timestamp) AS ACTIVITY_DATE, 
       count(distinct _experience.journeyOrchestration.stepEvents.journeyVersionID) AS ACTIVE_JOURNEYS
FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) DESC;
```

_de output van de Steekproef_

| ACTIVITY_DATE | ACTIVE_JOURNEYS |
|---|---|
| 25-11-2024 | 12 |
| 24-11-2024 | 15 |
| 23-11-2024 | 14 |
| 22-11-2024 | 11 |
| 21-11-2024 | 13 |

De vraag keert, voor de bepaalde periode, de telling van unieke reizen terug die elke dag teweegbrachten. Eén enkele reis die op meerdere dagen plaatsvindt, wordt één keer per dag meegeteld.


+++

## Vragen over reistijden {#journey-instances-queries}

+++Aantal profielen in een specifieke status op een specifieke tijd

Deze vraag gebruikt Gemeenschappelijke Uitdrukkingen van de Lijst (CTEs) om profielen te identificeren die momenteel bij een specifieke knoop in een reis wachten door profielen te vinden die door de knoop maar nog niet aan de volgende knopen zijn overgegaan.

_de vraag van het meer van Gegevens_

```sql
WITH
 
INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS (
 
    SELECT
        STEP_EVENTS.timestamp AS TS,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID AS ID
    FROM
        journey_step_events AS STEP_EVENTS
    WHERE
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>'
 
),
 
INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS (
 
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME = '<specific node name>' AND
        <filter on time for profile in specific node>
 
),
 
INSTANCES_PASSED_IN_NEXT_NODES AS (
     
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME in (<list of next node names from the specific node>)
 
),
 
INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS (
 
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1
 
    EXCEPT
     
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NEXT_NODES AS T1
 
)
 
SELECT
    DATE_FORMAT(T1.TS,'<date pattern>') AS DATETIME,
    count(T1.ID) AS INSTANCES_COUNT
FROM
    INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1,
    INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS T2
WHERE
    T1.ID = T2.ID
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

_Voorbeeld_

```sql
WITH
 
INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS (
 
    SELECT
        STEP_EVENTS.timestamp AS TS,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID AS ID
    FROM
        journey_step_events AS STEP_EVENTS
    WHERE
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009'
 
),
 
INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS (
 
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME = 'slack_bso_tests - test1' AND
        T1.TS > (now() - interval '18 hour')
 
),
 
INSTANCES_PASSED_IN_NEXT_NODES AS (
     
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME in ('slack_bso_tests - test2')
 
),
 
INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS (
 
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1
 
    EXCEPT
     
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NEXT_NODES AS T1
 
)
 
SELECT
    DATE_FORMAT(T1.TS,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(T1.ID) AS INSTANCES_COUNT
FROM
    INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1,
    INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS T2
WHERE
    T1.ID = T2.ID
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

+++

+++Hoeveel profielen zijn de reis in de specifieke periode verlaten

Deze vraag telt de reisinstanties die tijdens een gespecificeerde tijdspanne, met inbegrip van uitgang wegens voltooiing, fouten, onderbrekingen, of het begrenzen fouten verlieten.

_de vraag van het meer van Gegevens_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    <timestamp filter>
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

_Voorbeeld_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    STEP_EVENTS.timestamp > (now() - interval '22 hour')
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

+++

+++Hoeveel profielen verlaat de reis in de specifieke periode met knoop/status

Deze vraag verstrekt een gedetailleerde specificatie van weggangen, die de knoopnaam en uitgangsstatus voor elke verlaten instantie tonen helpen identificeren waar en waarom de profielen de reis verlaten.

_de vraag van het meer van Gegevens_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus AS EXIT_STATUS,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    <timestamp filter>
GROUP BY
    DATETIME, NODE_NAME, EXIT_STATUS
ORDER BY
    DATETIME DESC
```

_Voorbeeld_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus AS EXIT_STATUS,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    STEP_EVENTS.timestamp > (now() - interval '22 hour')
GROUP BY
    DATETIME, NODE_NAME, EXIT_STATUS
ORDER BY
    DATETIME DESC
```

+++

## Zoekopdrachten die betrekking hebben op prestatiewaarden van aangepaste handelingen {#query-custom-action}

+++ Het totale aantal succesvolle vraag, fouten en verzoeken per seconde van elk eindpunt over een specifieke tijdspanne

Deze vraag verstrekt prestatiesmetriek voor de acties van douaneHTTP, met inbegrip van totale vraag, succesvolle vraag, foutentellingen door type (4xx, 5xx, onderbrekingen, beperkt), en productie in verzoeken per seconde voor elk eindpunt.

_Vraag van het meer van Gegevens_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (<actionExecutionOriginStartTime filter> OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND <timestamp filter>))
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

_Voorbeeld_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND timestamp > (now() - interval '1' day)))
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

+++

+++ De reeks van de tijd succesvolle vraag, fouten en productie van elk eindpunt over een specifieke tijdspanne

Deze vraag verstrekt de zelfde prestatiesmetriek zoals de vorige vraag maar georganiseerd als tijdreeks, die toont hoe eindpuntprestaties in tijd met minuut-door-minuut granulariteit variëren.

_Vraag van het meer van Gegevens_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(COALESCE(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, timestamp), 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (<actionExecutionOriginStartTime filter> OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND
           <timestamp filter>))
GROUP BY 
    ENDPOINT, SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

_Voorbeeld_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(COALESCE(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, timestamp), 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND
           timestamp > (now() - interval '1' day)))
GROUP BY 
    ENDPOINT, SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

+++

+++Responslatentie van elk eindpunt op 50e, 95e, 99e en 99,9e percentiel over een specifieke periode

Deze vraag berekent de percentielen van de reactietijd voor de eindpunten van de douaneactie, die u latentiedistributie helpen begrijpen en prestatiesoutliers bij verschillende percentiele drempels identificeren.

_Vraag van het meer van Gegevens_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS SUCCESSFUL_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

_Voorbeeld_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS SUCCESSFUL_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

+++

+++De tijdreeks van de percentielen van de reactievertraging van elk eindpunt over een specifieke tijdspanne

Deze vraag verstrekt latentiepercentielen die als tijdreeks worden georganiseerd, die u toestaan om te volgen hoe de tijden van de eindpuntreactie in tijd op verschillende percentielniveaus veranderen.

_Vraag van het meer van Gegevens_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,    
    COUNT(1) AS SUCCESSFUL_CALLS,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

_Voorbeeld_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,    
    COUNT(1) AS SUCCESSFUL_CALLS,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

+++

+++ Wachttijd in wachtrij op vertraagde eindpunten op 50e en 95e percentiel over een specifieke tijdsperiode

Deze vraag analyseert rij wachttijden voor vertraagde eindpunten, die de 50e en 95e percentiele wachttijden tonen om u te helpen het effect van het vertragen op uw douaneacties begrijpen.

_Vraag van het meer van Gegevens_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

_Voorbeeld_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

+++

+++ De reeks van de rij wachttijdpercentielen voor elk vertraagd eindpunt

Deze vraag verstrekt rij wachttijdpercentielen als tijdreeks, toestaand u om te controleren hoe het vertragen tijden over tijd op elk eindpunt wacht.

_Vraag van het meer van Gegevens_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

_Voorbeeld_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

+++

+++ Aantal fouten door type en code voor een specifiek eindpunt over een specifieke tijdspanne

Deze vraag verstrekt een gedetailleerde uitsplitsing van fouten voor een specifiek eindpunt, gegroepeerd door foutentype en foutencode, met inbegrip van informatie over pogingen opnieuw proberen.

_Vraag van het meer van Gegevens_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionExecutionError AS ERROR_TYPE,
    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode AS ERROR_CODE,
    COUNT(1) AS CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionOriginError IS NOT NULL THEN 1 END) AS CALLS_WITH_RETRY
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint = '<endpoint URI>' AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL AND
    (<actionExecutionOriginStartTime filter>) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND <timestamp filter>))
GROUP BY 
    ERROR_TYPE, ERROR_CODE
ORDER BY
    ERROR_TYPE, ERROR_CODE;
```

_Voorbeeld_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionExecutionError AS ERROR_TYPE,
    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode AS ERROR_CODE,
    COUNT(1) AS CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionOriginError IS NOT NULL THEN 1 END) AS CALLS_WITH_RETRY
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint = 'https://example.com/my/endpoint' AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL AND
    (_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND timestamp > (now() - interval '1' day)))
GROUP BY 
    ERROR_TYPE, ERROR_CODE
ORDER BY
    ERROR_TYPE, ERROR_CODE;
```

+++

