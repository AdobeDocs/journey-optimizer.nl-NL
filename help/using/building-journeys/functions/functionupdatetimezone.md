---
product: journey optimizer
title: updateTimeZone
description: Meer informatie over de functie updateTimeZone
feature: Journeys
role: Developer
level: Experienced
keywords: updateTimeZone, functie, expression, trip
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 6%

---

# updateTimeZone {#updateTimeZone}

Retourneert een nieuwe datumtijd met een nieuwe tijdzone op hetzelfde moment.

## Categorie

Datum

## Functiesyntaxis

`updateTimeZone(<parameters>)`

## Parameters

* tijdzone-id: tekenreeks
* dateTime

## Handtekening en type geretourneerd

`updateTimeZone(<dateTime>,<timeZone id>)`

Retourneert een datetime.

## Voorbeelden

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Keert 2023-08-28T17 :15: 30.123+02 :00 terug.

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

Als de waarde van het tijdstempelveld `2021-11-16T16:55:12.939318+01:00` is, retourneert de functie `2021-11-17T02:55:12.942115+11:00` .
