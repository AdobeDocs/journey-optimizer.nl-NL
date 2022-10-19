---
solution: Journey Optimizer
product: journey optimizer
title: Velden voor het uitvoeren van acties van journeyStep-gebeurtenissen
description: Velden voor het uitvoeren van acties van journeyStep-gebeurtenissen
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 4%

---

# Velden voor het uitvoeren van acties van journeyStep-gebeurtenissen {#sharing-execution-fields}

Deze veldgroep wordt gedeeld door de tripStepEvent en de tripStepProfileEvent.

Als in de stap een actie moet worden verwerkt, worden die velden toegevoegd aan de gebeurtenislading.

## actionID {#actionid-field}

Id van de handeling die wordt uitgevoerd.

Type: string

## actionName {#actionname-field}

Naam van de handeling. Als er geen naam is ingesteld, wordt de stepName uitgevoerd.

Type: string

## actionType {#actionType-field}

Type handeling.

Type: string

## actionParameterized {#actionparameterized-field}

Hiermee wordt aangegeven of de handeling al dan niet wordt geparametriseerd.

Type: boolean

## actionExecutionTime {#actionexecutiontime-field}

De hoeveelheid tijd (in milliseconden) die is besteed aan het uitvoeren van een huidige handeling.

Type: lang

## actionExecutionError {#actionexecutionerror-field}

Type fout dat optreedt wanneer de handeling wordt aangeroepen.

Type: string

Waarden:
* http
* begrenzen
* timeout
* error

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Code voor uitvoeringsfout van handeling. Wordt weergegeven als de fout een code heeft, zoals een HTTP-code.

Type: string

## actionExecutionOriginError {#actionexecutionoriginerror-field}

Een time-out kan in twee gevallen optreden:

* bij de eerste poging wordt een handeling uitgevoerd. In dit geval is de uitvoering niet voltooid en is er geen onderliggende fout
* bij een nieuwe poging: in dit geval, beschrijft actionExecOrigError/actionExecOrigErrorCode de fout die op de poging alvorens wordt ontmoet opnieuw.

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

Type: string

## actionExecutionOriginCode {#actionexecutionorigincode-field}

Foutcode van de actionExecOrigError.

Type: string

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

Type: string

## deliveryJobID {#deliveryjobid-field}

Dit beschrijft de identiteitskaart van de leveringstaak voor de partijreis.

Type: string

## batchDeliveryID {#batchdeliveryid-field}

Dit beschrijft leveringsId voor de partijreis.

Type: string

## fromSegmentTrigger {#fromsegmenttrigger-field}

Dit beschrijft als de Reis van de Partij van het Segment van het Publiek wordt teweeggebracht.

Type: boolean

## actionSchedulerCount {#actionschedulercount-field}

Aantal verzoeken van het plannerbericht die naar de plannerdienst tijdens de stapverwerking worden verzonden.

Type: lang
