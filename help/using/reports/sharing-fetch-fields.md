---
solution: Journey Optimizer
product: journey optimizer
title: Velden voor het ophalen van gegevens van journeyStep-gebeurtenissen
description: Velden voor het ophalen van gegevens van journeyStep-gebeurtenissen
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 4%

---

# Velden voor het ophalen van gegevens van journeyStep-gebeurtenissen {#sharing-fetch-fields}

Deze veldgroep wordt gedeeld door de tripStepEvent en de tripStepProfileEvent.

Tijdens een stapverwerking, kunnen wij geen gegevens halen op gebiedsgroepen.

## fetchTotalTime {#fetchtotaltime-field}

Totale hoeveelheid tijd die in gegevens wordt doorgebracht halen in millis tijdens de stapverwerking.

Type: lang

## fetchTypeInError {#fetchtypeinerror-field}

Definieert of de fout Ophalen in zich op Adobe Experience Platform of op een aangepaste gegevensbron bevindt.

Type: string

Waarden:
* aep
* aangepast

## fetchError {#fetcherror-field}

Type fout dat gebeurt wanneer de gegevens worden opgehaald verwerkt.

Type: string

Waarden:
* http
* begrenzen
* timedout
* error

## fetchErrorCode {#fetcherrorcode-field}

Code voor ophalen fout. Wordt weergegeven als de fout een code heeft, zoals een HTTP-code. Wanneer actionExecError bijvoorbeeld http is, vertegenwoordigt code 404 de HTTP 404-fout.

Type: string

## fetchOriginError {#fetchoriginerror-field}

Een time-out kan in twee gevallen optreden:

* bij de eerste poging wordt de handeling uitgevoerd. In dit geval is de uitvoering niet voltooid en is er geen onderliggende fout
* bij een nieuwe poging: in dit geval, beschrijft actionExecOrigError/actionExecOrigErrorCode de fout die op de poging alvorens wordt ontmoet opnieuw.

Bijvoorbeeld, worden de gegevens gehaald van de Verenigde Dienst van het Profiel en HTTP 500 fout is teruggekeerd bij de eerste poging. De fetch wordt opnieuw geprobeerd, maar de duur van de 2 pogingen overschrijdt de onderbreking. Vervolgens wordt de uitvoering van de handeling gecodeerd als een time-out. Het actieonderdeel ziet er als volgt uit:

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

Type: string

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

De foutcode van het systeem [!DNL Journey Optimizer] vraagt. Het kan bijvoorbeeld een 404, 500, enzovoort zijn.

Type: string

## fetchCount {#fetchcount-field}

Hoeveel keer worden de gegevens opgehaald, ongeacht het type bron.

Type: lang

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

De totale hoeveelheid tijd die nodig is om de gegevens van Adobe Experience Platform op te halen in millis. Opmerking: deze hoeveelheid tijd wordt berekend vanaf het tijdstip waarop de motor de verrijkingsgebeurtenis naar de verrijkingsdienst verzendt en de reactie ontvangt .

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
