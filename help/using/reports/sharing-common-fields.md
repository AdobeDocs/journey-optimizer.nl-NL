---
title: journaalgebeurtenissen gemeenschappelijke velden
description: journaalgebeurtenissen gemeenschappelijke velden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 6d744c0289e81ab2229f02c44ead43943b945b89
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# journaalgebeurtenissen gemeenschappelijke velden {#sharing-common-fields}

Deze veldgroep wordt gedeeld door de tripStepEvent en de tripStepProfileEvent.

Dit zijn de gemeenschappelijke gebieden XDM die [!DNL Journey Optimizer] naar Adobe Experience Platform. Voor elke stap die op reis wordt verwerkt, worden gemeenschappelijke velden verzonden. Voor aangepaste handelingen en verbeteringen worden specifiekere velden gebruikt.

Sommige van deze velden zijn alleen beschikbaar in specifieke verwerkingspatronen (uitvoering van handelingen, ophalen van gegevens, enz.) om de omvang van gebeurtenissen te beperken.

## ingang {#entrance-field}

Geeft aan of de gebruiker de reis heeft betreden. Als dit niet het geval is, gaan we ervan uit dat de waarde onwaar is.

Type: boolean

Waarden: true/false

## intrede {#reentrance-field}

Geeft aan of de gebruiker de reis opnieuw is gestart met hetzelfde exemplaar. Als dit niet het geval is, gaan we ervan uit dat de waarde onwaar is.

Type: boolean

Waarden: true/false

## instanceEnded {#instance-ended-field}

Geeft aan of de instantie is beëindigd (geslaagd of niet).

Type: boolean

## eventID {#eventid-field}

Gebeurtenis-id tijdens de verwerking, voor de stapverwerking. Als de gebeurtenis een externe gebeurtenis is, is de waarde eventId. Als de gebeurtenis een interne gebeurtenis is, is de waarde de interne eventId (zoals scheduledNotificationReceived, executedAction, enz.).

Type: string

## nodeID {#nodeid-field}

Client node id (vanaf het canvas).

Type: string

## stepID {#stepdid-field}

Unieke id van de stap die momenteel wordt verwerkt.

Type: string

## stepName {#stepname-field}

Naam van de stap die momenteel wordt verwerkt.

Type: string

## stepType {#steptype-field}

Type van de stap.

Type: string

Mogelijke waarden:

* Voorwaarde
* Actie
* Planner
* Timer

## stepStatus {#stepstatus-field}

Status van de stap die de status van de stap vertegenwoordigt, wanneer de verwerking ervan is uitgevoerd (en de stapgebeurtenis is geactiveerd).

Type: string

De status kan zijn:

* beëindigd: de stap heeft geen overgang en de verwerking ervan is voltooid.
* fout: er is een fout opgetreden tijdens de stapverwerking.
* overgangen: de stap wacht op een gebeurtenis om over te gaan naar een andere stap.
* beperkt: de stap is mislukt op een begrenzingsfout die tijdens een handeling of verrijking is opgetreden.
* timedout: de stap is mislukt op een time-outfout die tijdens een handeling of verrijking is opgetreden.
* instanceTimeout: de stap heeft de verwerking gestopt, omdat de instantie de time-out heeft bereikt.

## tripID {#journeyid-field}

ID van de reis.

Type: string

## tripVersionID {#journeyversionid-field}

ID van de reisversie. Deze id vertegenwoordigt de identiteitsverwijzing naar de reis, in het geval van de tripStepEvent.

Type: string

## tripVersionName {#journeyversionname-field}

Naam van de reisversie.

Type: string

## tripVersion {#journeyversion-field}

Versie van de reisversie.

Type: string

## instanceID {#instanceid-field}

Interne id van het reisexemplaar.

Type: string

## externalKey {#externalkey-field}

Externe sleutel die uit de gebeurtenis is geëxtraheerd om deze te verwerken.

Type: string

## parentStepID {#parenstepid-field}

Stap-id van het bovenliggende element van de huidige verwerkte stap in de instantie.

Type: string

## parentStepName {#parentstepname-field}

De naam van de stap van het bovenliggende element van de huidige stap.

Type: string

## parentTransitionID {#parenttransitionid-field}

Id van de overgang die de instantie naar de verwerkte stap heeft gebracht.

Type: string

## parentTransitionName {#parenttransitionname-field}

Naam van de overgang die de instantie aan de verwerkte stap heeft gebracht.

Type: string

## inTest {#intest-field}

Vermeld of deze reis in testmodus staat of niet.

Type: boolean

## processingTime {#processingtime-field}

Totale hoeveelheid tijd in milliseconden van de ingang van de instantiestappen aan het eind van de verwerking.

Type: lang

## instanceType {#instancetype-field}

Hiermee wordt het instantietype aangegeven als het een batch of eenheidsinstantie is.

Type: string

Waarden: partij/eenheid

## recienceIndex {#recurrenceindex-field}

Index van de herhaling als de reis partij en terugkerend is (eerste looppas heeft terugkerendIndex = 1).

Type: lang

## isBatchToUnitary {#isbatchtounitary-field}

Geeft aan of deze eenheidsinstantie is geactiveerd door een batchinstantie.

Type: boolean

## batchExternalKey {#batchexternalkey-field}

External Key for batch event.

Type: string

## batchInstanceID {#batchinstanceid-field}

this is the batch instance ID.

Type: string

## batchUnitaryBranchID {#batchunitarybranchid-field}

als de instantie is geactiveerd door een batchinstantie, is dit de eenheidvertakkings-id.

Type: string
