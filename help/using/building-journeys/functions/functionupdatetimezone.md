---
product: journey optimizer
title: updateTimeZone
description: Meer informatie over de functie updateTimeZone
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: updateTimeZone, functie, expression, trip
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 10%

---

# updateTimeZone {#updateTimeZone}

Retourneert een nieuwe datumtijd met een nieuwe tijdzone op hetzelfde moment.

## Categorie

Datum

## Functiesyntaxis

`updateTimeZone(<parameters>)`

## Parameters

* tijdzone-id: string
* dateTime

## Handtekening en type geretourneerd

`updateTimeZone(<dateTime>,<timeZone id>)`

Retourneert een datetime.

## Voorbeelden

`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Retourneert 2019-08-28T17:15:30.123+02:00.

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@{MyExpEvent.timestamp}, "Australia/Sydney")`

Als de waarde van het tijdstempelveld gelijk is aan `2021-11-16T16:55:12.939318+01:00`, dan retourneert de functie `2021-11-17T02:55:12.942115+11:00`.
