---
solution: Journey Optimizer
product: journey optimizer
title: Problemen met de uitvoering van uw livetraject oplossen
description: Leer hoe u fouten in de uitvoering van live reizen kunt oplossen
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: problemen oplossen, problemen oplossen, reis, controle, fouten
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '1592'
ht-degree: 16%

---

# Problemen met de uitvoering van uw livetraject oplossen {#troubleshooting-execution}

In deze sectie, leer hoe te om reisgebeurtenissen problemen op te lossen, controleer als de profielen uw reis inging, hoe zij door het navigeren, en als de berichten worden verzonden.

U kunt fouten ook oplossen voordat u een reis test of publiceert. Leer hoe [ op deze pagina ](troubleshooting.md).

Als u binnenkomende acties gebruikt, leer hoe te om hen [ op deze pagina ](troubleshooting-inbound.md) problemen op te lossen.

## Controleren of gebeurtenissen correct zijn verzonden {#checking-that-events-are-properly-sent}

Het startpunt van een journey is altijd een gebeurtenis. U kunt tests uitvoeren met tools zoals Postman.

U kunt controleren of de API-aanroep die u via deze tools verzendt, correct is verzonden of niet. Als een fout wordt geretourneerd, betekent dit dat er een probleem is met uw aanroep. Controleer opnieuw de payload, de koptekst (vooral de organisatie-id) en de bestemmings-URL. U kunt de beheerder vragen wat de juiste URL is.

Gebeurtenissen worden niet rechtstreeks van de bron naar de ritten verplaatst. Reizen vertrouwen inderdaad op de streaming opname-API&#39;s van [!DNL Adobe Experience Platform] . Dientengevolge, in het geval van gebeurtenis verwante kwesties, kunt u naar [[!DNL Adobe Experience Platform]  documentatie ](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"} voor het Streamen van opname APIs het oplossen van problemen verwijzen.

Als uw reis er niet in slaagt testwijze met fout `ERR_MODEL_RULES_16` toe te laten, zorg ervoor de gebruikte gebeurtenis een [ identiteit namespace ](../audience/get-started-identity.md) omvat wanneer het gebruiken van een kanaalactie.

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

>>
**voor de reizen van de Kwalificatie van het Publiek met het stromen publiek**: Als u een activiteit van de Kwalificatie van het Publiek als het punt van de reisingang gebruikt, ben zich ervan bewust dat niet alle profielen die voor het publiek worden gekwalificeerd noodzakelijkerwijs de reis wegens tijdsfactoren, snelle uitgang van het publiek zullen ingaan, of als de profielen reeds in het publiek alvorens te publiceren waren. Leer meer over [ het stromen overwegingen van de publiekskwalificatie timing ](audience-qualification-events.md#streaming-entry-caveats).

## Problemen met overgangen in testmodi oplossen {#troubleshooting-test-transitions}

Als testprofielen uw reis in testmodus niet doorlopen of als de visuele stroom geen groene pijlen geeft die de stap vooruit aangeven, kan het probleem gerelateerd zijn aan de validatie van de overgang. Deze sectie bevat richtlijnen voor het diagnosticeren en oplossen van algemene problemen met de testmodus.

### Testprofielen worden niet verder verwerkt

Als testprofielen de reis ingaan maar niet voorbij de aanvankelijke stap vooruit, controleer het volgende:

* **de begindatum van de Reis** - de gemeenschappelijkste oorzaak is wanneer de de begindatum van de reis in de toekomst wordt geplaatst. De profielen van de test worden onmiddellijk verworpen als de huidige tijd buiten de gevormde reis [ begin en einddata/tijd ](journey-properties.md#dates) venster valt. Oplossen:
   * Controleren of de begindatum van de reis in de toekomst niet is ingesteld
   * Zorg ervoor dat de huidige tijd binnen het actieve datumvenster van de reis valt
   * Werk indien nodig de eigenschappen van de reis bij om de begindatum aan te passen

* **het profielconfiguratie van de Test** - bevestig dat het profiel correct als testprofiel in [!DNL Adobe Experience Platform] wordt gemarkeerd. Zie [ hoe te om testprofielen ](../audience/creating-test-profiles.md) voor meer informatie tot stand te brengen.

* **Identiteit namespace** - verzeker de identiteit namespace die in de gebeurtenisconfiguratie wordt gebruikt aanpast namespace van uw testprofiel.

### Null-overgangsindicatoren

Tijdens het technische oplossen van problemen, kunt u een `isValidTransition` bezit tegenkomen die aan ongeldig in de technische details van de reis wordt geplaatst. Deze eigenschap alleen voor de gebruikersinterface is niet van invloed op de verwerking van back-end of de reisprestaties. Een null-waarde kan echter aangeven:

* **verkeerde configuratie van de Reis** - de datum van het reisbegin wordt geplaatst in de toekomst, veroorzakend testgebeurtenissen om stil worden verworpen
* **Beschadigde overgang** - in zeldzame gevallen, kunnen de wegknopen moeten worden opnieuw aangesloten

Als u blijvende overgangsproblemen tegenkomt:

1. Controleren of de begindatum van de rit actueel is
1. Testmodus deactiveren en opnieuw activeren
1. Als het probleem zich blijft voordoen, kunt u overwegen om de betrokken transportknooppunten te dupliceren en opnieuw aan te sluiten
1. Voor onopgeloste gevallen, contacteer steun met reislogboeken, beïnvloede profiel IDs, en details over de ongeldige overgang

>[!NOTE]
>
>Herinner dat de gebeurtenissen die buiten het actieve datumvenster van de reis worden verzonden stil zonder foutenmelding worden verworpen. Verifieer altijd eerst uw configuratie van de reistijdtiming wanneer het oplossen van problemen van de profielprogressie van de testtest.

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

Gebruik deze sectie om te begrijpen waarom dubbele rijen in de Gebeurtenissen van de Stap van de Reis kunnen verschijnen.

### Waarom zie ik veelvoudige ingangen met de zelfde reisinstantie, profiel, knoop, en verzoek IDs?

Wanneer het vragen van de gegevens van de Gebeurtenissen van de Stap van de Reis, kunt u soms waarnemen wat om dubbele logboekingangen voor de zelfde reisuitvoering lijkt te zijn. Deze vermeldingen hebben identieke waarden voor:

* `profileID` - De profielidentiteit
* `instanceID` - De identificatie van de instantie van de reis
* `nodeID` - Het specifieke knooppunt van de rit
* `requestID` - De aanvraag-id

Nochtans, hebben deze ingangen **verschillende `_id` waarden**, die de belangrijkste indicator is die dit scenario van daadwerkelijke gegevensduplicatie onderscheidt.

### Wat veroorzaakt dit gedrag?

Dit is het gevolg van automatische schalingsbewerkingen met backend (ook wel &#39;opnieuw in evenwicht brengen&#39; genoemd) in de microservicearchitectuur van [!DNL Adobe Journey Optimizer] . Tijdens perioden van hoge belasting of systeemoptimalisatie:

1. Een gebeurtenis van de reisstap begint verwerking en aan de dataset van de Gebeurtenissen van de Stap van de Reis het programma geopend
2. Een auto-schrapende verrichting herverdeelt werkbelasting over de dienstinstanties
3. Dezelfde gebeurtenis kan opnieuw worden verwerkt door een andere service-instantie, waardoor een tweede logbestandvermelding met een andere `_id` wordt gemaakt

Dit is een verwacht systeemgedrag en werkt **zoals ontworpen**.

### Is er enig effect op de uitvoering van de reis of de levering van berichten?

**Nr.** Het effect is beperkt tot alleen loggen. [!DNL Adobe Journey Optimizer] heeft ingebouwde deduplicatiemechanismen bij de laag van de berichtuitvoering die verzekeren:

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

Voor meer informatie over het vragen van de Gebeurtenissen van de Stap van de Reis, zie [ Voorbeelden van vragen ](../reports/query-examples.md).

## Metrische verschillen in dashboard oplossen {#dashboard-metrics}

Als de metriek in het **Overzicht** dashboard wordt getoond niet het daadwerkelijke aantal reizen in **doorbladert** lusje, verifieer het volgende:

* Ervoor zorgen dat de betreffende reizen in de afgelopen 24 uur verkeer hebben gehad, aangezien reizen zonder recente activiteiten van het dashboard worden uitgesloten.
* Controleer of u de juiste toegangsmachtigingen hebt om alle reizen in uw organisatie weer te geven.
* Laat maximaal 30 minuten staan voordat metrische gegevens worden vernieuwd nadat u wijzigingen hebt aangebracht in uw reizen.

Als de discrepanties blijven bestaan, contacteer de Steun van Adobe met screenshots van zowel het Overzicht als Browse lusjes voor onderzoek.
