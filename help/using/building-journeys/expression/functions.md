---
solution: Journey Optimizer
product: journey optimizer
title: Functies
description: Meer informatie over functies
feature: Journeys
role: Developer
level: Experienced
keywords: functie, expressies, editor, reis
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 0331f8fe2439d41c08ad88a6d0bd95dd150bab90
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
| Adobe Experience Platform | [&#x200B; inAudience &#x200B;](../functions/functioninaudience.md) |
| Samenvoeging | [avg](../functions/aggregation-functions.md#avg) |
| Samenvoeging | [count](../functions/aggregation-functions.md#count) |
| Samenvoeging | [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) |
| Samenvoeging | [countWithNull](../functions/aggregation-functions.md#countWithNull) |
| Samenvoeging | [distinctCount](../functions/aggregation-functions.md#distinctCount) |
| Samenvoeging | [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) |
| Samenvoeging | [max](../functions/aggregation-functions.md#max) |
| Samenvoeging | [min](../functions/aggregation-functions.md#min) |
| Samenvoeging | [sum](../functions/aggregation-functions.md#sum) |
| Conversie | [toBool](../functions/conversion-functions.md#toBool) |
| Conversie | [&#x200B; toDateOnly &#x200B;](../functions/conversion-functions.md#toDateOnly) |
| Conversie | [toDateTime](../functions/conversion-functions.md#toDateTime) |
| Conversie | [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) |
| Conversie | [toDecimal](../functions/conversion-functions.md#toDecimal) |
| Conversie | [toDuration](../functions/conversion-functions.md#toDuration) |
| Conversie | [toInteger](../functions/conversion-functions.md#toInteger) |
| Conversie | [toString](../functions/conversion-functions.md#toString) |
| Datum | [&#x200B; currentTimeInMillis &#x200B;](../functions/date-functions.md#currentTimeInMillis) |
| Datum | [inLastDays](../functions/date-functions.md#inLastDays) |
| Datum | [inLastHours](../functions/date-functions.md#inLastHours) |
| Datum | [inLastMonths](../functions/date-functions.md#inLastMonths) |
| Datum | [inLastYears](../functions/date-functions.md#inLastYears) |
| Datum | [inNextDays](../functions/date-functions.md#inNextDays) |
| Datum | [inNextHours](../functions/date-functions.md#inNextHours) |
| Datum | [inNextMonths](../functions/date-functions.md#inNextMonths) |
| Datum | [inNextYears](../functions/date-functions.md#inNextYears) |
| Datum | [now](../functions/date-functions.md#now) |
| Datum | [nowWithDelta](../functions/date-functions.md#nowWithDelta) |
| Datum | [setHours](../functions/date-functions.md#setHours) |
| Datum | [setDays](../functions/date-functions.md#setDays) |
| Datum | [&#x200B; updateTimeZone &#x200B;](../functions/date-functions.md#updateTimeZone) |
| Lijst | [distinct](../functions/list-functions.md#distinct) |
| Lijst | [distinctWithNull](../functions/list-functions.md#distinctWithNull) |
| Lijst | [&#x200B; filter &#x200B;](../functions/list-functions.md#filter) |
| Lijst | [getListItem](../functions/list-functions.md#getListItem) |
| Lijst | [in](../functions/list-functions.md#in) |
| Lijst | [&#x200B; snijdt &#x200B;](../functions/list-functions.md#intersect) |
| Lijst | [&#x200B; grens &#x200B;](../functions/list-functions.md#limit) |
| Lijst | [listSize](../functions/list-functions.md#listSize) |
| Lijst | [serializeList](../functions/list-functions.md#serializeList) |
| Lijst | [sort](../functions/list-functions.md#sort) |
| Math | [random](../functions/functionrandom.md) |
| Math | [round](../functions/functionround.md) |
| String | [concat](../functions/functionconcat.md) |
| String | [contain](../functions/functioncontain.md) |
| String | [&#x200B; containIgnoreCase &#x200B;](../functions/functioncontainwithignorecase.md) |
| String | [endWith](../functions/functionendwith.md) |
| String | [&#x200B; endWithIgnoreCase &#x200B;](../functions/functionendwithignorecase.md) |
| String | [&#x200B; equalIgnoreCase &#x200B;](../functions/functionequalignorecase.md) |
| String | [indexOf](../functions/functionindexof.md) |
| String | [isEmpty](../functions/functionisempty.md) |
| String | [isNotEmpty](../functions/functionisnotempty.md) |
| String | [lastIndexOf](../functions/functionlastindexof.md) |
| String | [length](../functions/functionlength.md) |
| String | [lower](../functions/functionlower.md) |
| String | [matchRegExp](../functions/functionmatchregexp.md) |
| String | [&#x200B; notEqualIgnoreCase &#x200B;](../functions/functionnotequalignorecase.md) |
| String | [replace](../functions/functionreplace.md) |
| String | [replaceAll](../functions/functionreplaceall.md) |
| String | [split](../functions/functionsplit.md) |
| String | [startWith](../functions/functionstartwith.md) |
| String | [startWithIgnoreCase](../functions/functionstartwithignorecase.md) |
| String | [substr](../functions/functionsubstr.md) |
| String | [trim](../functions/functiontrim.md) |
| String | [upper](../functions/functionupper.md) |
| String | [uuid](../functions/functionuuid.md) |
