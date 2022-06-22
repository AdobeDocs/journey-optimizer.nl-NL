---
title: Voorbeelden van query's voor gegevensset
description: Voorbeelden van query's voor gegevensset
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 1de18fa479a54c09751324a67793ce50e5657ce3
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---

# Gebruiksgevallen voor gegevensset {#tracking-datasets}

Op deze pagina vindt u de lijst met Adobe Journey Optimizer-gegevenssets en verwante gebruiksgevallen:

[Dataset over e-mailvolgervaringen](../start/datasets-query-examples.md#email-tracking-experience-event-dataset)
[Gegevensset voor feedbackgebeurtenis](../start/datasets-query-examples.md#message-feedback-event-dataset)
[Dataset met gebeurtenissen voor het bijhouden van pushmeldingen](../start/datasets-query-examples.md#push-tracking-experience-event-dataset)
[Reisstapgebeurtenis](../start/datasets-query-examples.md#journey-step-event)
[Gegevensset over beslissende gebeurtenis aanbieden](../start/datasets-query-examples.md#ode-decisionevents)
[Dataset voor goedgekeurde service](../start/datasets-query-examples.md#consent-service-dataset)
[Gegevensset BCC-feedbackgebeurtenis](../start/datasets-query-examples.md#bcc-feedback-event-dataset)

## Dataset over e-mailvolgervaringen{#email-tracking-experience-event-dataset}

_Naam in de interface: Dataset voor CJM-e-mailtrackingervaring_

Systeemdataset voor het invoeren van e-mailvolgervaringsgebeurtenissen van Journey Optimizer.

Het verwante schema is CJM Email Tracking Experience Event-schema.

Deze vraag toont de tellingen van verschillende e-mailinteractie (opent, klikt) voor een bepaald bericht:

```sql
select
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageInteraction.interactionType
```

Deze vraag toont de verdeling van tellingen van verschillende e-mailinteracties (opent, klikt) door bericht voor een bepaalde reis:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
limit 100;
```

## Gegevensset voor feedbackgebeurtenis{#message-feedback-event-dataset}

_Naam in de interface: Dataset voor CJM-feedbackgebeurtenis_

Dataset voor het invoeren van feedback over e-mail- en pushtoepassingen van Journey Optimizer.

Het verwante schema is CJM Message Feedback Event-schema.

Deze vraag toont de tellingen van verschillende e-mail terugkoppelt status (verzonden, stuit, enz.) voor een bepaald bericht:

```sql
select
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus;
```

Deze vraag toont de uitsplitsing van tellingen van verschillende e-mail terugkoppelt status (verzonden, stuit, enz.) door bericht voor een bepaalde reis:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
limit 100;
```

Op geaggregeerd niveau wordt het domeinniveaurapport (gesorteerd op topdomeinen): Domeinnaam, Bericht verzonden, Stemmen

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

E-mail verzendt dagelijks:

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

Zoeken of bepaalde e-mailid een e-mail heeft ontvangen of niet en zo niet, wat was de fout, de stuiterende categorie, de code:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

Zoek de lijst met alle afzonderlijke e-mailbiedingen met een bepaalde fout, stuiterende categorie of code in de laatste x uur/dagen of gekoppeld aan een bepaalde berichtlevering:

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

Harde stuitsnelheid op geaggregeerd niveau:

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

Permanente fouten gegroepeerd op stuitercode:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

## Dataset met gebeurtenissen voor het bijhouden van pushmeldingen {#push-tracking-experience-event-dataset}

_Naam in de interface: Dataset voor CJM-gebeurtenis voor het bijhouden van push_

Dataset voor het opnemen van gebeurtenissen voor het bijhouden van mobiele gegevens voor push vanuit Journey Optimizer.

Het verwante schema is CJM Push Tracking Experience Event-schema.

Voorbeeld van query:

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from cjm_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from cjm_email_tracking_experience_event_dataset
  group by _experience.customerJourneyManagement.pushChannelContext.platform
```
## Reisstapgebeurtenis{#journey-step-event}

_Interne naam: Gebeurtenissen van de Stap van de reis (systeemdataset)_

Dataset voor het opnemen van step gebeurtenissen in de reis.

Het verwante schema is een Dagboekstapgebeurtenisschema voor Journey Orchestration.

Deze vraag toont de indeling van de aantallen van het actiesucces door actielabel voor een bepaalde reis:

```sql
select
    _experience.journeyOrchestration.stepEvents.actionName AS actionLabel,
    count(1) actionSuccessCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.actionID IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionType IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode IS NULL
group by
    _experience.journeyOrchestration.stepEvents.actionName;   
```

Deze vraag toont de uitsplitsing van stap ingegaan tellingen door nodeId &amp; nodeLabel voor een bepaalde reis. nodeId is hier inbegrepen aangezien nodeLabel het zelfde voor verschillende wegknopen kan zijn.

```sql
select
    _experience.journeyOrchestration.stepEvents.nodeID AS nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName AS nodeLabel,
    count(1) stepEnteredCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = TRUE
     AND _experience.journeyOrchestration.stepEvents.eventID IS DISTINCT FROM 'createInstance'
group by
    _experience.journeyOrchestration.stepEvents.nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName; 
```

## Gegevensset over beslissende gebeurtenis aanbieden{#ode-decisionevents}

_Naam in de interface: ODE DecisionEvents (systeem dataset)_

Dataset voor het opnemen van aanbiedingsvoorstellen aan de gebruikers.

Het verwante schema is ODE DecisionEvents.

In deze query worden alle voorstellen weergegeven die de vorige dag zijn geretourneerd:

```sql
SELECT date_format(Decision.Timestamp, 'MM/dd/yyyy') as Date
,HOUR(Decision.timestamp) as Hour
,COUNT(*)  as Count
FROM ode_decisionevents_b699fa78_efec_41b1_99fa_78efecc1b1ef_decision AS Decision
WHERE date_format(Decision.timestamp, 'MM/dd/yyyy') = date_format(CURRENT_DATE, 'MM/dd/yyyy') and Decision._experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:13ab41890a335ad6'
GROUP BY date_format(Decision.Timestamp, 'MM/dd/yyyy')
,HOUR(Decision.timestamp)
ORDER BY 1, 2 DESC;
```

Deze vraag toont het aantal tijden die aanbiedingen over de laatste 30 dagen van een bepaalde activiteit/een besluit en zijn bijbehorende aanbiedingsprioriteit werden voorgesteld.

```sql
select proposedOffers.id,proposedOffers.name, po._experience.decisioning.ranking.priority, count(proposedOffers.id) as ProposedCount from (
select explode(propositionexplode.selections) AS proposedOffers from
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20200925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

## Dataset voor goedgekeurde service{#consent-service-dataset}

_Naam in de interface: CJM de Dataset van de Dienst van de Goedkeuring (systeemdataset)_

Dataset voor Journey Optimizer-service voor toestemming.

Het verwante schema is CJM Consent Service Schema.

Vraag om e-mailadressen weer te geven waarvoor toestemming is verleend om e-mail te ontvangen:

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

Vraag om toestemmingswaarde voor een e-mailidentiteitskaart terug te keren waar e-mailidentiteitskaart de input zou zijn:

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```

## Gegevensset BCC-feedbackgebeurtenis{#bcc-feedback-event-dataset}

_Naam in de interface: AJO BCC Dataset voor feedbackgebeurtenis (gegevensset systeem)_

Dataset om informatie voor BCC Berichten op te slaan.

Vraag alle BCC-berichten binnen 2 dagen op (voor een bepaalde campagne):

```sql
SELECT bcc.*
FROM ajo_bcc_feedback_event_dataset AS bcc
WHERE 
    bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID = '<message-execution-id>' AND 
    bcc.timestamp >= now() - INTERVAL '2' day; 
```

Vraag met terugkoppelt dataset om gebruikers te tonen die (alle stuitingen en onderdrukking) niet ontvingen en die ingang BCC voor een bepaald bericht hebben:

```sql
SELECT 
    distinct bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS OriginalRecipientAddress 
FROM ajo_bcc_feedback_event_dataset  AS bcc 
WHERE 
    bcc.timestamp > now() - INTERVAL '2' DAY AND     bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND      bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress != '' AND
    ( 
            bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress NOT IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
            mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent'
        )  
    OR     bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
        mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND 
            mfe._experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category = 'async' AND 
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus
```
