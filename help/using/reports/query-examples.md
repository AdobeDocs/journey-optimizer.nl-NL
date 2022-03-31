---
title: Voorbeelden van query's
description: Voorbeelden van query's
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 26ad12c3-0a2b-4f47-8f04-d25a6f037350
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 4%

---

# Voorbeelden van query&#39;s{#query-examples}

Deze sectie maakt een lijst van verscheidene algemeen gebruikte voorbeelden om de Gebeurtenissen van de Stap van de Reis in het meer van Gegevens te vragen.

## Bericht-/handelingsfouten {#message-action-errors}

### Lijst van fouten tijdens reizen {#error-list-journey}

Met deze query kunt u elke fout die tijdens reizen is aangetroffen, weergeven tijdens het uitvoeren van een bericht/handeling.

_Gegevens Meer query_

```sql
SELECT _experience.journeyOrchestration.stepEvents.actionExecutionError, count(distinct _id) FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeName=<'message-name'>
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY _experience.journeyOrchestration.stepEvents.actionExecutionError
```

_Voorbeeld_

```sql
SELECT _experience.journeyOrchestration.stepEvents.actionExecutionError, count(distinct _id) FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeName='Message - 100KB Email with Gateway and Kafkav2'
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '67b14482-143e-4f83-9cf5-cfec0fca3d26'
GROUP BY _experience.journeyOrchestration.stepEvents.actionExecutionError
```

Deze vraag keert alle verschillende fouten terug die terwijl het uitvoeren van een actie in een reis samen met de telling van hoe vaak het voorkwam.

## Op profielen gebaseerde query&#39;s {#profile-based-queries}

### Zoeken of een profiel een specifieke reis heeft ingevoerd {#profile-entered-journey}

_Gegevens Meer query_

```sql
SELECT count(distinct _id) FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>'
```

_Voorbeeld_

```sql
SELECT count(distinct _id) FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = 'ec9efdd0-8a7c-4d7a-a765-b2cad659fa4e' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com'
```

Het resultaat moet groter zijn dan 0. Deze vraag keert het nauwkeurige aantal tijden terug een profiel een reis is ingegaan.

### Zoeken of een profiel een specifiek bericht is verzonden {#profile-specific-message}

**Methode 1:** als de naam van uw bericht niet uniek is in de reis (het wordt gebruikt op veelvoudige plaatsen).

_Gegevens Meer query_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeID='<NodeId in the UI corresponding to the message>' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>'
```

_Voorbeeld_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeID='17ae65a1-02dd-439d-b54e-b56a78520eba' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '67b14482-143e-4f83-9cf5-cfec0fca3d26' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com'
```

Het resultaat moet groter zijn dan 0. Deze vraag vertelt ons slechts of de berichtactie met succes op de reiskant werd uitgevoerd.

**Methode 2:** als de naam van uw bericht uniek is in de reis.

_Gegevens Meer query_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeName='<NodeName in the UI corresponding to the message>' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>'
```

_Voorbeeld_

```sql
SELECT count(distinct _id) FROM journey_step_events WHERE
_experience.journeyOrchestration.stepEvents.nodeID='Message- 100KB Email' AND
_experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.journeyVersionID = '67b14482-143e-4f83-9cf5-cfec0fca3d26' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com'
```

De vraag keert de lijst van alle berichten samen met hun telling terug die voor het geselecteerde profiel wordt aangehaald.

## Zoeken naar alle berichten die een profiel in de afgelopen 30 dagen heeft ontvangen {#message-received-30-days}

_Gegevens Meer query_

```sql
SELECT _experience.journeyOrchestration.stepEvents.nodeName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.nodeType = 'action' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName
```

_Voorbeeld_

```sql
SELECT _experience.journeyOrchestration.stepEvents.nodeName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
_experience.journeyOrchestration.stepEvents.nodeType = 'action' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName
```

De vraag keert de lijst van alle berichten samen met hun telling terug die voor het geselecteerde profiel wordt aangehaald.

### Zoeken naar alle ritten die een profiel in de afgelopen 30 dagen heeft ingevoerd {#profile-entered-30-days}

_Gegevens Meer query_

```sql
SELECT _experience.journeyOrchestration.stepEvents.journeyVersionName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
_experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.journeyVersionName
```

_Voorbeeld_

```sql
SELECT _experience.journeyOrchestration.stepEvents.journeyVersionName, count(distinct _id) FROM journey_step_events
WHERE  _experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
_experience.journeyOrchestration.stepEvents.profileID = 'saurgarg@adobe.com' AND
timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.journeyVersionName
```

De vraag keert de lijst van alle reisnamen samen met het aantal tijden terug het gevraagde profiel de reis inging.

### Aantal profielen dat in aanmerking kwam voor een dagelijkse reis {#profile-qualified}

_Gegevens Meer query_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.profileID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

_Voorbeeld_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.profileID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '100' day)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '180ad071-d42d-42bb-8724-2a6ff0a109f1'
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

De vraag resteert, voor de bepaalde periode, het aantal profielen dat de reis elke dag inging. Als een profiel wordt ingevoerd via meerdere identiteiten, wordt het twee keer geteld. Als terugkeer wordt toegelaten, zou het profielaantal over verschillende dagen kunnen worden gedupliceerd als het de reis op verschillende dag opnieuw inging.

## Vragen op basis van reizen {#journey-based-queries}

### Aantal dagelijkse actieve reizen {#daily-active-journeys}

_Gegevens Meer query_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.journeyVersionID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

_Voorbeeld_

```sql
SELECT DATE(timestamp), count(distinct _experience.journeyOrchestration.stepEvents.journeyVersionID) FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '100' day)
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) desc
```

De vraag keert, voor de bepaalde periode, de telling van unieke reizen terug die elke dag teweegbrachten. Eén enkele reis die op meerdere dagen plaatsvindt, wordt één keer per dag meegeteld.