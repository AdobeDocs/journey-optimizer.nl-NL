---
solution: Journey Optimizer
product: journey optimizer
title: Problemen met de uitvoering van uw livetraject oplossen
description: Leer hoe u fouten in de uitvoering van live reizen kunt oplossen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: problemen oplossen, problemen oplossen, reis, controle, fouten
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: a93f08cf2da1f2b19296359d1200a6dddacbc1f2
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 21%

---

# Problemen met de uitvoering van uw livetraject oplossen {#troubleshooting-execution}

In deze sectie, leer hoe te om reisgebeurtenissen problemen op te lossen, controleer als de profielen uw reis inging, hoe zij door het navigeren, en als de berichten worden verzonden.

U kunt fouten ook oplossen voordat u een reis test of publiceert. Leer hoe [&#x200B; op deze pagina &#x200B;](troubleshooting.md).

Als u binnenkomende acties gebruikt, leer hoe te om hen [&#x200B; op deze pagina &#x200B;](troubleshooting-inbound.md) problemen op te lossen.

## Controleren of gebeurtenissen correct zijn verzonden {#checking-that-events-are-properly-sent}

Het startpunt van een journey is altijd een gebeurtenis. U kunt tests uitvoeren met tools zoals Postman.

U kunt controleren of de API-aanroep die u via deze tools verzendt, correct is verzonden of niet. Als een fout wordt geretourneerd, betekent dit dat er een probleem is met uw aanroep. Controleer opnieuw de payload, de koptekst (vooral de organisatie-id) en de bestemmings-URL. U kunt de beheerder vragen wat de juiste URL is.

Gebeurtenissen worden niet rechtstreeks van de bron naar de ritten verplaatst. Reizen vertrouwen inderdaad op Adobe Experience Platform-API&#39;s voor streaming-opname. Dientengevolge, in het geval van gebeurtenis verwante kwesties, kunt u naar [&#x200B; documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=nl-NL){target="_blank"} voor het Streamen van opname APIs het oplossen van problemen verwijzen.

Als uw reis er niet in slaagt testwijze met fout `ERR_MODEL_RULES_16` toe te laten, zorg ervoor de gebruikte gebeurtenis een [&#x200B; identiteit namespace &#x200B;](../audience/get-started-identity.md) omvat wanneer het gebruiken van een kanaalactie.

De naamruimte identity wordt gebruikt om de testprofielen op unieke wijze te identificeren. Bijvoorbeeld, als e-mail wordt gebruikt om de testprofielen te identificeren, zou de identiteit namespace **E-mail** moeten worden geselecteerd. Als het unieke herkenningsteken het telefoonaantal is, dan zou de identiteit namespace **Telefoon** moeten worden geselecteerd.

## Controleren of mensen de reis betreden {#checking-if-people-enter-the-journey}

Reisrapportage meet de toegang van mensen tot een reis in real-time.

Als u het evenement met succes verzendt, maar geen toegang ziet tot de reis, betekent dit dat er iets mis gaat tussen het verzenden van het evenement en de ontvangst van het evenement op de reis.

U kunt het oplossen van problemen met de hieronder vragen beginnen:

* Weet u zeker dat de journey waar u de eerste gebeurtenis verwacht, in de testmodus of live is?
* Hebt u de gebeurtenis opgeslagen voordat u de payload uit de payloadvoorvertoning hebt gekopieerd?
* Bevat de gebeurtenispayload een gebeurtenis-id?
* Hebt u de juiste URL gebruikt?
* Hebt u de payloadstructuur van de streamingopname-API’s gevolgd en de voorvertoning van de payloadstructuur in het deelvenster voor gebeurtenisconfiguratie gebruikt? Zie [deze pagina](../event/about-creating.md#preview-the-payload).
* Gebruikt u de juiste sleutel-waardeparen in de kopbal van uw gebeurtenis?

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

## Controleren hoe mensen door de reis navigeren {#checking-how-people-navigate-through-the-journey}

De journalistiek meet de voortgang van individuen binnen een reis. Het is gemakkelijk te bepalen waar en waarom een persoon is gestopt.

Controleer bijvoorbeeld het volgende:

* Komt het door een voorwaarde die de persoon uitsluit? De voorwaarde is bijvoorbeeld ‘geslacht = man’ en de persoon is een vrouw. Deze controle kan door een zakelijke gebruiker worden uitgevoerd als de voorwaarde niet te complex is.
* Komt het doordat een aanroep aan een databron niet wordt beantwoord? Wanneer de journey in de testmodus verkeert, is deze informatie in testmoduslogboeken te zien. Wanneer de journey live is, kan een beheerder directe aanroepen aan de databron testen en het ontvangen antwoord controleren. Een beheerder kan de journey ook dupliceren en testen.

## Controleren of berichten zijn verzonden {#checking-that-messages-are-sent-successfully}

Als individuen de juiste manier in de reis stromen maar geen berichten ontvangen zij zouden moeten ontvangen, kunt u controleren of:

* [!DNL Journey Optimizer] heeft correct rekening gehouden met de aanvraag om het bericht te verzenden. Zakelijke gebruikers hebben toegang tot het bericht dat ze geacht worden te zijn verzonden en controleren of de tijd van de meest recente uitvoering overeenkomt met de uitvoeringstijd van uw reis. Ze kunnen ook de meest recente ontvangen API-oproepen/gebeurtenissen controleren.
* [!DNL Journey Optimizer] heeft het bericht verzonden. Controleer de reisrapportering om ervoor te zorgen dat er geen fouten zijn.

In het geval van een bericht dat via een douaneactie wordt verzonden, is het enige wat tijdens reistest kan worden gecontroleerd het feit dat de vraag van het systeem van de douaneactie tot een fout of niet leidt. Als de oproep aan het externe systeem dat aan de douaneactie is gekoppeld niet tot een fout leidt maar niet tot het verzenden van een bericht leidt, zouden sommige onderzoeken aan de kant van het externe systeem moeten worden gedaan.

## Dubbele items begrijpen in Reisstapgebeurtenissen {#duplicate-step-events}

### Waarom zie ik veelvoudige ingangen met de zelfde reisinstantie, profiel, knoop, en verzoek IDs?

Wanneer het vragen van de gegevens van de Gebeurtenissen van de Stap van de Reis, kunt u soms waarnemen wat om dubbele logboekingangen voor de zelfde reisuitvoering lijkt te zijn. Deze vermeldingen hebben identieke waarden voor:

* `profileID` - De profielidentiteit
* `instanceID` - De identificatie van de instantie van de reis
* `nodeID` - Het specifieke knooppunt van de rit
* `requestID` - De aanvraag-id

Nochtans, hebben deze ingangen **verschillende `_id` waarden**, die de belangrijkste indicator is die dit scenario van daadwerkelijke gegevensduplicatie onderscheidt.

### Wat veroorzaakt dit gedrag?

Dit komt door backend auto-schrapende verrichtingen (ook genoemd &quot;het opnieuw in evenwicht brengen&quot;) in de architectuur van de microdiensten van Adobe Journey Optimizer voor. Tijdens perioden van hoge belasting of systeemoptimalisatie:

1. Een gebeurtenis van de reisstap begint verwerking en aan de dataset van de Gebeurtenissen van de Stap van de Reis het programma geopend
2. Een auto-schrapende verrichting herverdeelt werkbelasting over de dienstinstanties
3. Dezelfde gebeurtenis kan opnieuw worden verwerkt door een andere service-instantie, waardoor een tweede logbestandvermelding met een andere `_id` wordt gemaakt

Dit is een verwacht systeemgedrag en werkt **zoals ontworpen**.

### Is er enig effect op de uitvoering van de reis of de levering van berichten?

**Nr.** Het effect is beperkt tot alleen loggen. Adobe Journey Optimizer heeft ingebouwde deduplicatiemechanismen bij de laag van de berichtuitvoering die verzekeren:

* Er wordt slechts één bericht (e-mail, SMS, pushmelding, enz.) verzonden naar elk profiel
* Handelingen worden slechts eenmaal uitgevoerd
* De uitvoering van de reis verloopt correct

U kunt dit verifiëren door de `ajo_message_feedback_event_dataset` te vragen of de logboeken van de actieuitvoering te controleren - u zult zien dat slechts één bericht daadwerkelijk werd verzonden, ondanks de dubbele ingangen van de de reisstap gebeurtenis.

### Hoe kan ik deze gevallen in mijn vragen identificeren?

Bij het analyseren van de gegevens van de Gebeurtenissen van de Stap van de Reis:

1. **Controle het `_id` gebied**: De ware systeem-vlakke duplicaten zouden het zelfde `_id` hebben. Verschillende `_id` -waarden geven afzonderlijke logitems aan ten opzichte van het hierboven beschreven opnieuw in evenwicht brengen-scenario.

2. **verifieer berichtlevering**: De verwijzing met bericht koppelt gegevens terug om slechts één bericht te bevestigen werd verzonden:

   ```sql
   SELECT
     timestamp,
     _experience.customerJourneyManagement.messageExecution.messageExecutionID,
     _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
   FROM ajo_message_feedback_event_dataset
   WHERE
     _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journeyVersionID>'
     AND TO_JSON(identityMap) like '%<profileID>%'
   ORDER BY timestamp DESC;
   ```

3. **Groep door unieke herkenningstekens**: Wanneer het tellen van uitvoeringen, gebruik `_id` om nauwkeurige tellingen te krijgen:

   ```sql
   SELECT
     COUNT(DISTINCT _id) as unique_executions
   FROM journey_step_events
   WHERE
     _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
     AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID>'
   ```

### Wat moet ik doen als ik dit observeer?

Dit is normaal systeemgedrag en **geen actie wordt vereist**. Het dubbele registreren wijst niet op een probleem met uw reisconfiguratie of berichtlevering.

Als u rapporten of analyses bouwt die op de Gebeurtenissen van de Stap van de Reis worden gebaseerd:

* `_id` gebruiken als primaire sleutel voor het tellen van unieke gebeurtenissen
* Kruisverwijzing met bericht terugkoppelt datasets wanneer het analyseren van berichtlevering
* Houd er rekening mee dat timinganalyse items kan weergeven die binnen een paar seconden van elkaar zijn geclusterd

Voor meer informatie over het vragen van de Gebeurtenissen van de Stap van de Reis, zie [&#x200B; Voorbeelden van vragen &#x200B;](../reports/query-examples.md).

## Metrische verschillen in dashboard oplossen {#dashboard-metrics}

Als de metriek in het **Overzicht** dashboard wordt getoond niet het daadwerkelijke aantal reizen in **doorbladert** lusje, verifieer het volgende:

* Ervoor zorgen dat de betreffende reizen in de afgelopen 24 uur verkeer hebben gehad, aangezien reizen zonder recente activiteiten van het dashboard worden uitgesloten.
* Controleer of u de juiste toegangsmachtigingen hebt om alle reizen in uw organisatie weer te geven.
* Laat maximaal 30 minuten staan voordat metrische gegevens worden vernieuwd nadat u wijzigingen hebt aangebracht in uw reizen.

Als de discrepanties blijven bestaan, contacteer de Steun van Adobe met screenshots van zowel het Overzicht als Browse lusjes voor onderzoek.
