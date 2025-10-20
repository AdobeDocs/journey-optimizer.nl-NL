---
solution: Journey Optimizer
product: journey optimizer
title: Functies
description: Meer informatie over functies
feature: Journeys
role: Engineer
level: Experienced
keywords: functie, expressies, editor, reis
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 31%

---

# Functies {#functions}

Een functie kan verschillende handtekeningen hebben (een andere set geordende parameters). Een functiehandtekening kan 0-N-expressies hebben als geordende parameters.

`<function name>` (`<expression as param 1>`, `<expression as param 2>` , ...,`<expression as param N>`)

Elke functie heeft een specifiek type geretourneerd.

Hier volgt een lijst met ondersteunde functies.

## Belangrijkste functies

| Categorie | Functie |
|-------------|-----------------------|
| Adobe Experience Platform | [ inAudience ](../functions/functioninaudience.md) |
| Samenvoeging | [avg](../functions/functionavg.md) |
| Samenvoeging | [count](../functions/functioncount.md) |
| Samenvoeging | [countOnlyNull](../functions/functioncountonlynull.md) |
| Samenvoeging | [countWithNull](../functions/functioncountwithnull.md) |
| Samenvoeging | [distinctCount](../functions/functiondistinctcount.md) |
| Samenvoeging | [distinctCountWithNull](../functions/functiondistinctcountwithnull.md) |
| Samenvoeging | [max](../functions/functionmax.md) |
| Samenvoeging | [min](../functions/functionmin.md) |
| Samenvoeging | [sum](../functions/functionsum.md) |
| Conversie | [toBool](../functions/functiontobool.md) |
| Conversie | [ toDateOnly ](../functions/functiontodateonly.md) |
| Conversie | [toDateTime](../functions/functiontodatetime.md) |
| Conversie | [toDateTimeOnly](../functions/functiontodatetimeonly.md) |
| Conversie | [toDecimal](../functions/functiontodecimal.md) |
| Conversie | [toDuration](../functions/functiontoduration.md) |
| Conversie | [toInteger](../functions/functiontointeger.md) |
| Conversie | [toString](../functions/functiontostring.md) |
| Datum | [ currentTimeInMillis ](../functions/functioncurrenttimeinmillis.md) |
| Datum | [inLastDays](../functions/functioninlastdays.md) |
| Datum | [inLastHours](../functions/functioninlasthours.md) |
| Datum | [inLastMonths](../functions/functioninlastmonths.md) |
| Datum | [inLastYears](../functions/functioninlastyears.md) |
| Datum | [inNextDays](../functions/functioninnextdays.md) |
| Datum | [inNextHours](../functions/functioninnexthours.md) |
| Datum | [inNextMonths](../functions/functioninnextmonths.md) |
| Datum | [inNextYears](../functions/functioninnextyears.md) |
| Datum | [now](../functions/functionnow.md) |
| Datum | [nowWithDelta](../functions/functionnowwithdelta.md) |
| Datum | [setHours](../functions/functionsethours.md) |
| Datum | [setDays](../functions/functionsetdays.md) |
| Datum | [ updateTimeZone ](../functions/functionupdatetimezone.md) |
| Lijst | [distinct](../functions/functiondistinct.md) |
| Lijst | [distinctWithNull](../functions/functiondistinctwithnull.md) |
| Lijst | [ filter ](../functions/functionfilter.md) |
| Lijst | [getListItem](../functions/functiongetlistitem.md) |
| Lijst | [in](../functions/functionin.md) |
| Lijst | [ snijdt ](../functions/functionintersect.md) |
| Lijst | [ grens ](../functions/functionlimit.md) |
| Lijst | [listSize](../functions/functionlistsize.md) |
| Lijst | [serializeList](../functions/functionserializelist.md) |
| Lijst | [sort](../functions/functionsort.md) |
| Math | [random](../functions/functionrandom.md) |
| Math | [round](../functions/functionround.md) |
| String | [concat](../functions/functionconcat.md) |
| String | [contain](../functions/functioncontain.md) |
| String | [ containIgnoreCase ](../functions/functioncontainwithignorecase.md) |
| String | [endWith](../functions/functionendwith.md) |
| String | [ endWithIgnoreCase ](../functions/functionendwithignorecase.md) |
| String | [ equalIgnoreCase ](../functions/functionequalignorecase.md) |
| String | [indexOf](../functions/functionindexof.md) |
| String | [isEmpty](../functions/functionisempty.md) |
| String | [isNotEmpty](../functions/functionisnotempty.md) |
| String | [lastIndexOf](../functions/functionlastindexof.md) |
| String | [length](../functions/functionlength.md) |
| String | [lower](../functions/functionlower.md) |
| String | [matchRegExp](../functions/functionmatchregexp.md) |
| String | [ notEqualIgnoreCase ](../functions/functionnotequalignorecase.md) |
| String | [replace](../functions/functionreplace.md) |
| String | [replaceAll](../functions/functionreplaceall.md) |
| String | [split](../functions/functionsplit.md) |
| String | [startWith](../functions/functionstartwith.md) |
| String | [startWithIgnoreCase](../functions/functionstartwithignorecase.md) |
| String | [substr](../functions/functionsubstr.md) |
| String | [trim](../functions/functiontrim.md) |
| String | [upper](../functions/functionupper.md) |
| String | [uuid](../functions/functionuuid.md) |
