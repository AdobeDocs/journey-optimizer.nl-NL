---
solution: Journey Optimizer
product: journey optimizer
title: journaalgebeurtenissen - gemeenschappelijke velden
description: journaalgebeurtenissen - gemeenschappelijke velden
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# journaalgebeurtenissen - gemeenschappelijke velden {#sharing-common-fields}

Deze gebiedsgroep zal door de volgende gebeurtenissen worden gedeeld: **tripStepEvent** en **tripStepProfileEvent**.

Dit zijn de algemene XDM-velden die [!DNL Journey Optimizer] naar Adobe Experience Platform verzendt. Voor elke stap die op reis wordt verwerkt, worden gemeenschappelijke velden verzonden. Voor aangepaste handelingen en verbeteringen worden specifiekere velden gebruikt.

Sommige van deze velden zijn alleen beschikbaar in specifieke verwerkingspatronen (het uitvoeren van handelingen, het ophalen van gegevens, enz.) om de grootte van gebeurtenissen te beperken.


>[!NOTE]
>
>Leer meer over de attributen van de reiseigenschappen [ in deze sectie ](../building-journeys/expression/journey-properties.md#journey-properties-fields).


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

Type: tekenreeks

## nodeID {#nodeid-field}

Client node id (vanaf het canvas).

Type: tekenreeks

## stepID {#stepdid-field}

Unieke id van de stap die momenteel wordt verwerkt.

Type: tekenreeks

## stepName {#stepname-field}

Naam van de stap die momenteel wordt verwerkt.

Type: tekenreeks

## stepType {#steptype-field}

Type van de stap.

Type: tekenreeks

Mogelijke waarden:

* Voorwaarde
* Actie
* Planner
* Timer

## stepStatus {#stepstatus-field}

Status van de stap die de status van de stap vertegenwoordigt, wanneer de verwerking ervan is uitgevoerd (en de stapgebeurtenis is geactiveerd).

Type: tekenreeks

De status kan zijn:

* beëindigd: de stap heeft geen overgang en zijn verwerking is met succes geëindigd.
* fout: er is een fout opgetreden tijdens de stapverwerking.
* overgangen: de stap wacht op een gebeurtenis om naar een andere stap over te gaan.
* beperkt: de stap is mislukt op een afkapfout die tijdens een handeling of verrijking is opgetreden.
* timeout: de stap is mislukt op een time-outfout die tijdens een handeling of verrijking is opgetreden.
* instanceTimeout: de stap heeft zijn verwerking tegengehouden, omdat de instantie zijn onderbreking heeft bereikt.

## tripID {#journeyid-field}

ID van de reis.

Type: tekenreeks

## tripVersionID {#journeyversionid-field}

ID van de reisversie. Deze id vertegenwoordigt de identiteitsverwijzing naar de reis, in het geval van de tripStepEvent.

Type: tekenreeks

>[!NOTE]
>
>Voor het oplossen van problemendoeleinden, adviseren wij gebruikend tripVersionID in plaats van tripVersionName wanneer het vragen van reizen.

## tripVersionName {#journeyversionname-field}

Naam van de reisversie.

Type: tekenreeks

>[!NOTE]
>
>Voor het oplossen van problemendoeleinden, adviseren wij gebruikend tripVersionID in plaats van tripVersionName wanneer het vragen van reizen.

## tripVersion {#journeyversion-field}

Versie van de reisversie.

Type: tekenreeks

## instanceID {#instanceid-field}

Interne id van het reisexemplaar.

Type: tekenreeks

## externalKey {#externalkey-field}

Externe sleutel die uit de gebeurtenis is geëxtraheerd om deze te verwerken.

Type: tekenreeks

## parentStepID {#parenstepid-field}

Stap-id van het bovenliggende element van de huidige verwerkte stap in de instantie.

Type: tekenreeks

## parentStepName {#parentstepname-field}

De naam van de stap van het bovenliggende element van de huidige stap.

Type: tekenreeks

## parentTransitionID {#parenttransitionid-field}

Id van de overgang die de instantie naar de verwerkte stap heeft gebracht.

Type: tekenreeks

## parentTransitionName {#parenttransitionname-field}

Naam van de overgang die de instantie aan de verwerkte stap heeft gebracht.

Type: tekenreeks

## inTest {#intest-field}

Vermeld of deze reis in testmodus staat of niet.

Type: boolean

## processingTime {#processingtime-field}

Totale hoeveelheid tijd in milliseconden van de ingang van de instantiestappen aan het eind van de verwerking.

Type: lang

## instanceType {#instancetype-field}

Hiermee wordt het instantietype aangegeven als het een batch of eenheidsinstantie is.

Type: tekenreeks

Waarden: batch/eenheidsprijs

## recienceIndex {#recurrenceindex-field}

Index van de herhaling als de reis partij en terugkerend is (eerste looppas heeft terugkerendIndex = 1).

Type: lang

## isBatchToUnitary {#isbatchtounitary-field}

Geeft aan of deze eenheidsinstantie is geactiveerd door een batchinstantie.

Type: boolean

## batchExternalKey {#batchexternalkey-field}

External Key for batch event.

Type: tekenreeks

## batchInstanceID {#batchinstanceid-field}

this is the batch instance ID.

Type: tekenreeks

## batchUnitaryBranchID {#batchunitarybranchid-field}

als de instantie is geactiveerd door een batchinstantie, is dit de eenheidvertakkings-id.

Type: tekenreeks

## exitCriteriaID

Id van de exitCriteria

Type: tekenreeks

## exitCriteriaName

Naam van de exitCriteria

Type: tekenreeks