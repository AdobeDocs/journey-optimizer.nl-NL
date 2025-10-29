---
solution: Journey Optimizer
product: journey optimizer
title: Velden voor het uitvoeren van acties van journeyStep-gebeurtenissen
description: Velden voor het uitvoeren van acties van journeyStep-gebeurtenissen
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 2%

---

# Velden voor het uitvoeren van acties van journeyStep-gebeurtenissen {#sharing-execution-fields}

Deze veldgroep wordt gedeeld door de tripStepEvent en de tripStepProfileEvent.

Als in de stap een actie moet worden verwerkt, worden die velden toegevoegd aan de gebeurtenislading.

## actionID {#actionid-field}

Id van de handeling die wordt uitgevoerd.

Type: tekenreeks

## actionName {#actionname-field}

Naam van de handeling. Als er geen naam is ingesteld, wordt de stepName uitgevoerd.

Type: tekenreeks

## actionType {#actionType-field}

Type handeling.

Type: tekenreeks

## actionParameterized {#actionparameterized-field}

Hiermee wordt aangegeven of de handeling al dan niet wordt geparametriseerd.

Type: boolean

## actionExecutionTime {#actionexecutiontime-field}

De hoeveelheid tijd (in milliseconden) die is besteed aan het uitvoeren van een huidige handeling.

Type: lang

Het `actionExecutionTime` gebied vertegenwoordigt de totale tijd (in milliseconden) die wordt genomen om de actie uit te voeren, met inbegrip van zowel de tijd het bestede verzoek wachtend in de rij (als de vertraging wordt gevormd en de tariefgrens wordt bereikt) en de daadwerkelijke uitvoeringstijd (met inbegrip van netwerklatentie aan het externe eindpunt).

Het veld `Timestamp` geeft de eindtijd van de uitvoering van de handeling aan. Wanneer u wilt bepalen wanneer het profiel het aangepaste actieknooppunt heeft ingevoerd, trekt u `actionExecutionTime` van `Timestamp` af.

Bijvoorbeeld als `Timestamp` &quot;2025-02-04 09 :39: 03 UTC&quot;is en `actionExecutionTime` 1.813.227 ms (~31 minuten) is, ging het profiel de knoop bij ongeveer &quot;2025-02-04 09 :08: 32 UTC&quot;binnen.


## actionExecutionError {#actionexecutionerror-field}

Type fout dat optreedt wanneer de handeling wordt aangeroepen.

Type: tekenreeks

Waarden:

* http
* begrenzen
* timeout
* fout

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Fout bij uitvoeren van code voor handeling. Wordt weergegeven als de fout een code heeft, zoals een HTTP-code.

Type: tekenreeks

## actionExecutionOriginError {#actionexecutionoriginerror-field}

Een time-out kan in twee gevallen optreden:

* bij de eerste poging wordt een handeling uitgevoerd. In dit geval is de uitvoering niet voltooid, dus is er geen onderliggende fout
* voor een nieuwe poging: in dit geval beschrijft actionExecOrigError/actionExecOrigErrorCode de fout die bij de poging vóór het opnieuw proberen wordt ontmoet.

Er wordt bijvoorbeeld een e-mail verzonden en er wordt een HTTP 500-fout geretourneerd bij de eerste poging. De fetch wordt opnieuw geprobeerd, maar de duur van de 2 pogingen overschrijdt de onderbreking. Vervolgens wordt de uitvoering van de handeling gecodeerd als een time-out. Het actieonderdeel ziet er als volgt uit:

```
    ...
    "actionId": "myActionId",
    "actionName": "My mail sending",
    "actionType": "acsRestAction",
    "actionParameterized": true,
    "actionExecError": "timedout",
    "actionExecOrigError": "http",
    "actionExecOrigErrorCode": "500"
```

Type: tekenreeks

## actionExecutionOriginCode {#actionexecutionorigincode-field}

Foutcode van de actionExecOrigError.

Type: tekenreeks

## actionOriginEndpoint {#actionoriginendpoint}

URI van het eindpunt van de douaneactie dat in de actie wordt gebruikt.

Type: tekenreeks

## actionOriginMethod {#actionoriginmethod}

Hier wordt de methode beschreven die in de HTTP-aanvraag (GET of POST) wordt gebruikt.

Type: tekenreeks

## actionOriginIsMTLS {#actionoriginismtls}

Dit beschrijft of MTLS voor het eindpunt wordt toegelaten.

Type: boolean

## actionIsProxy {#actionisproxy}

Dit beschrijft of een volmacht van HTTP met bepaalde IP adreswaaier voor de vraag wordt gebruikt.

Type: boolean

## actionExecutionOriginStartTime {#actionexecutionoriginstarttime}

Dit beschrijft de timestamp waarop de HTTP- aanvraag in werking wordt gesteld. In het geval van een nieuwe poging is dit de tijdstempel waarop de uiteindelijke poging opnieuw wordt uitgevoerd. De tijdstempel gebruikt de ISO8601-indeling in UTC-tijdzone.

Merk op dat dit timestamp typisch lichtjes zal zijn nadat het profiel de knoop van de douaneactie ingaat, of beduidend nadat het de knoop in het geval van throttling ingaat.

Type: tijdstempel

## actionExecutionOriginTime {#actionexecutionorigintime}

Dit beschrijft de reactietijd van de vraag van HTTP. In het geval van een nieuwe poging is dit de tijd die de uiteindelijke poging om opnieuw te proberen neemt. Het meet de tijd van wanneer het HTTP- verzoek in werking wordt gesteld aan wanneer de volledige reactie van de server is teruggekeerd. Merk op dat dit om het even welke tijd die in de rij in het geval van vertraging wordt doorgebracht uitsluit.

Type: lang

## actionIsThrottled {#actionisthrottled}

Dit beschrijft of de throttling voor het eindpunt wordt toegelaten.

Type: boolean

## actionWaitTime {#actionwaittime}

Dit beschrijft wanneer de gevormde tariefgrens voor een vertraagd eindpunt wordt geraakt, worden de vraag een rij gevormd en verwerkt bij het gevormde tarief. Dit gebied rapporteert de hoeveelheid tijd de vraag besteed wachtend in de rij alvorens wordt uitgevoerd. Alleen opgegeven als actionIsThrottled == true.

Type: lang

## actionBusinessType {#actionbusinesstype-field}

Geeft het type actie aan.

Waarden:

* bouwen
   * ACS-e-mail
   * ACS SMS
   * ACS Push
* klant
   * Epsilon
   * ...

Type: tekenreeks

## deliveryJobID {#deliveryjobid-field}

Dit beschrijft de identiteitskaart van de leveringstaak voor de partijreis.

Type: tekenreeks

## batchDeliveryID {#batchdeliveryid-field}

Dit beschrijft leveringsId voor de partijreis.

Type: tekenreeks

## fromSegmentTrigger {#fromsegmenttrigger-field}

Dit beschrijft als de Reis van de Partij van het Segment van het Publiek wordt teweeggebracht.

Type: boolean

## actionSchedulerCount {#actionschedulercount-field}

Aantal verzoeken van het plannerbericht die naar de plannerdienst tijdens de stapverwerking worden verzonden.

Type: lang
