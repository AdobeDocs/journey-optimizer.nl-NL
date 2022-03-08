---
product: adobe campaign
title: max
description: Meer informatie over de functie max
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 6%

---

# max{#max}

Geeft als resultaat de maximale waarde tussen een reeks expressies, opgegeven als een lijst of twee expressies. Null-waarden worden genegeerd.

## Categorie

Samenvoeging

## Functiesyntaxis

`max(<parameter>)`

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

`max(<listDuration>)`

Retourneert een duur.

`max(<listInteger>)`

Retourneert een duur.

`max(<listDateTimeOnly>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

`max(<listDateTime>)`

Retourneert een datetime.

`max(<listDateOnly>)`

Retourneert een datum.

`max(<listDecimal>)`

Retourneert een decimaal.

`max(<decimal>,<decimal>)`

Retourneert een decimaal.

`max(<duration>,<duration>)`

Retourneert een duur.

`max(<dateTime>,<dateTime>)`

Retourneert een datetime.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

`max(<integer>,<integer>)`

Retourneert een geheel getal.

## Voorbeelden

`max(@{BarBeacon.inventory},5)`

`max([10,3,8])`

Retourneert 10.

`max([10,null,8])`

Retourneert 10.
