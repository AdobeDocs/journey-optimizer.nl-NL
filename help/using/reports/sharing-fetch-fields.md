---
solution: Journey Optimizer
product: journey optimizer
title: Velden voor het ophalen van gegevens van journeyStep-gebeurtenissen
description: Velden voor het ophalen van gegevens van journeyStep-gebeurtenissen
feature: Journeys, Reporting
topic: Content Management
role: Engineer, Admin
level: Experienced
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 3%

---

# Velden voor het ophalen van gegevens van journeyStep-gebeurtenissen {#sharing-fetch-fields}

Deze veldgroep wordt gedeeld door de tripStepEvent en de tripStepProfileEvent.

Tijdens een stapverwerking, kunnen wij geen gegevens halen op gebiedsgroepen.

## fetchTotalTime {#fetchtotaltime-field}

Totale hoeveelheid tijd die in gegevens wordt doorgebracht halen in millis tijdens de stapverwerking.

Type: lang

## fetchTypeInError {#fetchtypeinerror-field}

Definieert of de fout Ophalen in zich op Adobe Experience Platform of op een aangepaste gegevensbron bevindt.

Type: tekenreeks

Waarden:

* aep
* aangepast

## fetchError {#fetcherror-field}

Type fout dat gebeurt wanneer de gegevens worden opgehaald verwerkt.

Type: tekenreeks

Waarden:

* http
* begrenzen
* timedout
* fout

## fetchErrorCode {#fetcherrorcode-field}

Code voor ophalen fout. Wordt weergegeven als de fout een code heeft, zoals een HTTP-code. Wanneer actionExecError bijvoorbeeld http is, vertegenwoordigt code 404 de HTTP 404-fout.

Type: tekenreeks

## fetchOriginError {#fetchoriginerror-field}

Een time-out kan in twee gevallen optreden:

* bij de eerste poging wordt de handeling uitgevoerd. In dit geval is de uitvoering niet voltooid, dus is er geen onderliggende fout
* voor een nieuwe poging: in dit geval beschrijft actionExecOrigError/actionExecOrigErrorCode de fout die bij de poging vóór het opnieuw proberen wordt ontmoet.

Bijvoorbeeld, worden de gegevens gehaald van de Verenigde Dienst van het Profiel en HTTP 500 fout is teruggekeerd bij de eerste poging. De fetch wordt opnieuw geprobeerd, maar de duur van de 2 pogingen overschrijdt de onderbreking. Vervolgens wordt de uitvoering van de handeling gecodeerd als een time-out. Het actieonderdeel ziet er als volgt uit:

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

Type: tekenreeks

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

De foutcode van het systeem [!DNL Journey Optimizer] vraagt. Het kan bijvoorbeeld een 404, 500, enzovoort zijn.

Type: tekenreeks

## fetchCount {#fetchcount-field}

Hoeveel keer worden de gegevens opgehaald, ongeacht het type bron.

Type: lang

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

De totale hoeveelheid tijd die nodig is om de gegevens van Adobe Experience Platform op te halen in millis. Opmerking: deze hoeveelheid tijd wordt berekend vanaf het tijdstip waarop de motor het verrijkingsevenement naar de verrijkingsdienst verzendt en de reactie ontvangt.

Type: lang

## fetchPlatformCount {#fetchplatformcount-field}

Hoeveel keer worden de gegevens opgehaald uit Adobe Experience Platform.

Type: lang

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

De hoeveelheid tijd die nodig is om de aangepaste gegevens op te halen in millis. Opmerking: deze hoeveelheid tijd wordt berekend vanaf het tijdstip waarop de motor de verrijkingsgebeurtenis naar de verrijkingsdienst verzendt en de reactie ontvangt

Type: lang

## fetchCustomCount {#fetchcustomcount-field}

Hoeveel keer worden de douanegegevens gehaald van externe systemen.

Type: lang
