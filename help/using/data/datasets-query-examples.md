---
solution: Journey Optimizer
product: journey optimizer
title: Voorbeelden van query's voor gegevensset
description: Voorbeelden van query's voor gegevensset
feature: Journeys, Reporting, Use Cases, Datasets, Data Management
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: dataset, optimizer, gebruiksgevallen
exl-id: 26ba8093-8b6d-4ba7-becf-b41c9a06e1e8
source-git-commit: 967e5ed75a7a3d37b37749f464a3b96e10b1f35a
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 0%

---

# Voorbeelden van query {#query-examples}

Op deze pagina vindt u de lijst met Adobe Journey Optimizer-gegevenssets en verwante gebruiksgevallen:

* [Dataset over e-mailvolgervaringen](#email-tracking-experience-event-dataset)
* [Gegevensset voor feedbackgebeurtenis](#message-feedback-event-dataset)
* [Dataset met gebeurtenissen voor het bijhouden van pushmeldingen](#push-tracking-experience-event-dataset)
* [Reisstapgebeurtenis](#journey-step-event)
* [Dataset voor beslissingsgebeurtenis](#ode-decisionevents)
* [Gegevensset BCC-feedbackgebeurtenis](#bcc-feedback-event-dataset)
* [Entiteitsgegevens](#entity-dataset)

Om de volledige lijst van gebieden en attributen voor elk schema te bekijken, raadpleeg het [ het schemawoordenboek van Journey Optimizer ](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=nl-NL){target="_blank"}.

Zie ook verscheidene algemeen gebruikte [ voorbeelden aan de Gebeurtenissen van de Stap van de Vraag ](../reports/query-examples.md).


## Dataset over e-mailvolgervaringen{#email-tracking-experience-event-dataset}

_Naam in de interface: De Dataset van de Gebeurtenis van de Ervaring van AJO e-mail het Volgen_

Systeemdataset voor het invoeren van e-mailvolgervaringsgebeurtenissen van Journey Optimizer.

Het verwante schema is AJO Email Tracking Experience Event-schema.

Deze vraag toont de tellingen van verschillende e-mailinteractie (opent, klikt) voor een bepaald bericht:

```sql
select
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from ajo_email_tracking_experience_event_dataset
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
from ajo_email_tracking_experience_event_dataset
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

_Naam in de interface: De Dataset van de Gebeurtenis van de Terugkoppeling van het Bericht van AJO_

Dataset voor het invoeren van feedback over e-mail- en pushtoepassingen van Journey Optimizer.

Het verwante schema is AJO Message Feedback Event-schema.

Deze vraag toont de tellingen van verschillende e-mail terugkoppelt status (verzonden, stuit, enz.) voor een bepaald bericht:

```sql
select
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from ajo_message_feedback_event_dataset
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
from ajo_message_feedback_event_dataset
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

Op geaggregeerd niveau, rapport op domeinniveau (gesorteerd op topdomeinen): Domeinnaam, Bericht verzonden, Stemmen

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

E-mail verzendt dagelijks:

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

Zoeken of een bepaalde e-mailid een e-mail heeft ontvangen of niet en zo niet, wat was de fout, de stuiterende categorie, de code:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

Zoek de lijst met alle afzonderlijke e-mailbiedingen met een bepaalde fout, stuiterende categorie of code in de laatste x uur/dagen of gekoppeld aan een bepaalde berichtlevering:

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

Harde stuitsnelheid op geaggregeerd niveau:

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

Permanente fouten gegroepeerd op stuitercode:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

>[!NOTE]
>
>In sommige ritten is `messageID` mogelijk niet uniek voor elke afzonderlijke levering. Als een rit dezelfde handeling opnieuw naar hetzelfde profiel verzendt, kan dezelfde `messageID` opnieuw worden gebruikt. Als u gebeurtenissen op het individuele verzendniveau nauwkeurig wilt bijhouden of kenmerken, combineert u daarom de velden `journeyVersionID` , `journeyActionID` en `batchInstanceID` (voor batchritten) of `identityMap` voor nauwkeurigere uniciteit.


### Identificeer quarantined adressen na een ISP stroomonderbreking{#isp-outage-query}

In het geval van een stroomonderbreking van Internet Service Provider (ISP), moet u e-mailadressen identificeren die verkeerd als grenzen (quarantined) voor specifieke domeinen, tijdens een timeframe worden aangebracht. Gebruik de volgende query om deze adressen op te halen:

```sql
SELECT
    _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
    timestamp AS EventTime,
    _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.reason AS "Invalid Recipient"
FROM ajo_message_feedback_event_dataset
WHERE
    eventtype = 'message.feedback' AND
    DATE(timestamp) BETWEEN '<start-date-time>' AND '<end-date-time>' AND
    _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND
    _experience.customerJourneyManagement.emailChannelContext.address ILIKE '%domain.com%'
ORDER BY timestamp DESC;
```

waarbij de datumnotatie: `YYYY-MM-DD HH:MM:SS` is.

Zodra geïdentificeerd, verwijder die adressen uit de onderdrukkingslijst van Journey Optimizer. [Meer informatie](../configuration/manage-suppression-list.md#remove-from-suppression-list).




## Dataset met gebeurtenissen voor het bijhouden van pushmeldingen {#push-tracking-experience-event-dataset}

_Naam in de interface: De Dataset van de Gebeurtenis van de Ervaring van AJO het Push Volgen_

Dataset voor het opnemen van gebeurtenissen voor het bijhouden van mobiele gegevens voor push vanuit Journey Optimizer.

Het verwante schema is AJO Push Tracking Experience Event-schema.

Voorbeeld van query:

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from ajo_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from ajo_email_tracking_experience_event_dataset
  group by _experience.customerJourneyManagement.pushChannelContext.platform
```

## Reisstapgebeurtenis{#journey-step-event}

_Interne naam: De Gebeurtenissen van de Stap van de reis (systeemdataset)_

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


Zie ook verscheidene algemeen gebruikte [ voorbeelden aan de Gebeurtenissen van de Stap van de Vraag ](../reports/query-examples.md).



## Dataset voor beslissingsgebeurtenis{#ode-decisionevents}

_Naam in de interface: ODE DecisionEvents (systeemdataset)_

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
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20230925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

<!--
## Consent Service Dataset{#consent-service-dataset}

_Name in the interface: CJM Consent Service Dataset (system dataset)_

Dataset for Journey Optimizer Consent service.

The related schema is CJM Consent Service Schema.

Query to list email IDs that have consented to receive email:

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

Query to return consent value for an email ID where email ID would be the input:

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```
-->

## Gegevensset BCC-feedbackgebeurtenis{#bcc-feedback-event-dataset}

_Naam in de interface: De Dataset van de Gebeurtenis van de Feedback van AJO BCC (systeemdataset)_

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
        FROM ajo_message_feedback_event_dataset AS mfe 
        WHERE 
            mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent'
        )  
    OR     bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM ajo_message_feedback_event_dataset AS mfe 
        WHERE 
        mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND 
            mfe._experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category = 'async' AND 
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus
```

## Entiteitsgegevens{#entity-dataset}

_Naam in de interface: ajo_entity_dataset (systeemdataset)_

Dataset om entiteitmeta-gegevens voor berichten op te slaan die naar het eind worden verzonden - gebruiker.

Het verwante schema is het AJO-entiteitsschema.

Deze dataset geeft u toegang tot markeerder bepaalde meta-gegevens die u toestaat om betere rapporteringsinzichten te krijgen wanneer de datasets van Journey Optimizer uit voor het melden van visualisatie in externe hulpmiddelen worden uitgevoerd. Dit wordt bereikt gebruikend het messageID attribuut dat diverse datasets zoals de Dataset van de Terugkoppeling van het Bericht en de Datasets van de Gebeurtenis van de Ervaring helpt verbinden om details van een berichtlevering van het verzenden naar het volgen op een profielniveau te krijgen.

**Belangrijke nota&#39;s**

* Een ingang voor een bericht wordt gecreeerd slechts nadat de reis of de campagne wordt gepubliceerd.

* 30 minuten na de publicatie van de campagne/reis kunt u de vermelding zien.

>[!NOTE]
>
>Voorlopig zijn er twee vermeldingen voor elke berichtpublicatie in de entiteitsdataset om toekomstige compatibiliteitsredenen. Dit beïnvloedt uw capaciteit om te gebruiken sluit zich aan bij vragen zoals nodig over datasets aan om de gewenste informatie te halen.

Als u, in uw rapporten, de e-mails wilt sorteren die door een specifieke reis volgens de actie worden verzonden die hen verzond. u kunt zich bij de dataset van de Terugkoppeling van het Bericht met de dataset van de Entiteit aansluiten. De volgende velden moeten worden gebruikt: `_experience.decisioning.propositions.scopeDetails.correlationID` en `_id field in entity dataset` .

De volgende vraag helpt u het bijbehorende berichtmalplaatje voor een bepaalde campagne krijgen:

```sql
SELECT
  AE._experience.customerJourneyManagement.entities.channelDetails.template
from
  ajo_entity_dataset AE
    WHERE AE._experience.customerJourneyManagement.entities.campaign.campaignVersionID = 'd7a01136-b113-4ef2-8f59-b6001f7eef6e'
```

Met de volgende query krijgt u de gegevens over de reis en het e-mailonderwerp die aan alle feedbackgebeurtenissen zijn gekoppeld:

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject 
from 
  ajo_entity_dataset AE 
  INNER JOIN ajo_message_feedback_event_dataset MF ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```

U kunt gebeurtenissen van de reisstap, de Terugkoppeling van het Bericht en het volgen datasets vastmaken om de statistieken voor een bepaald profiel te krijgen:

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.PROFILEID,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.NODENAME
from 
  ajo_entity_dataset AE 
  INNER JOIN ajo_message_feedback_event_dataset MF 
    ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
    INNER JOIN journey_step_events JE
    ON AE._experience.customerJourneyManagement.entities.journey.journeyActionID = JE._experience.journeyOrchestration.stepEvents.actionID
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```
