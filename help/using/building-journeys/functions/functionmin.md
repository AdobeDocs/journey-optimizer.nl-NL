---
product: journey optimizer
title: min
description: Meer informatie over de functie min
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: min, functie, expressie, transport
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 4%

---

# min {#min}

Geeft als resultaat de minimumwaarde tussen een reeks expressies, opgegeven als een lijst of twee expressies. Null-waarden worden genegeerd.

## Categorie

Samenvoeging

## Functiesyntaxis

`min(<parameters>)`

## Parameters

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duur
* integer
* decimaal
* dateTime
* dateTimeOnly

## Handtekeningen en geretourneerde typen

`min(<listDuration>)`

Retourneert een duur.

`min(<listInteger>)`

Retourneert een duur.

`min(<listDateTimeOnly>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

`min(<listDateTime>)`

Retourneert een datetime.

`min(<listDateOnly>)`

Retourneert een datum.

`min(<listDecimal>)`

Retourneert een decimaal.

`min(<decimal>,<decimal>)`

Retourneert een decimaal.

`min(<duration>,<duration>)`

Retourneert een duur.

`min(<dateTime>,<dateTime>)`

Retourneert een datetime.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

`min(<integer>,<integer>)`

Retourneert een geheel getal.

## Voorbeelden

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Retourneert 3.

`min([10,null,8])`

Retourneert 8.
