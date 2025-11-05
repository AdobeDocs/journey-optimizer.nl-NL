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
source-git-commit: d58319d687d113ce680c415524fdea0400cb38f0
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
| Conversie | [ toDateOnly ](../functions/conversion-functions.md#toDateOnly) |
| Conversie | [toDateTime](../functions/conversion-functions.md#toDateTime) |
| Conversie | [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) |
| Conversie | [toDecimal](../functions/conversion-functions.md#toDecimal) |
| Conversie | [toDuration](../functions/conversion-functions.md#toDuration) |
| Conversie | [toInteger](../functions/conversion-functions.md#toInteger) |
| Conversie | [toString](../functions/conversion-functions.md#toString) |
| Datum | [ currentTimeInMillis ](../functions/date-functions.md#currentTimeInMillis) |
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
| Datum | [ updateTimeZone ](../functions/date-functions.md#updateTimeZone) |
| Lijst | [distinct](../functions/list-functions.md#distinct) |
| Lijst | [distinctWithNull](../functions/list-functions.md#distinctWithNull) |
| Lijst | [ filter ](../functions/list-functions.md#filter) |
| Lijst | [getListItem](../functions/list-functions.md#getListItem) |
| Lijst | [in](../functions/list-functions.md#in) |
| Lijst | [ snijdt ](../functions/list-functions.md#intersect) |
| Lijst | [ grens ](../functions/list-functions.md#limit) |
| Lijst | [listSize](../functions/list-functions.md#listSize) |
| Lijst | [serializeList](../functions/list-functions.md#serializeList) |
| Lijst | [sort](../functions/list-functions.md#sort) |
| Math | [random](../functions/functionrandom.md) |
| Math | [round](../functions/functionround.md) |
| String | [concat](../functions/string-functions.md#concat) |
| String | [contain](../functions/string-functions.md#contain) |
| String | [ containIgnoreCase ](../functions/string-functions.md#containIgnoreCase) |
| String | [endWith](../functions/string-functions.md#endWith) |
| String | [ endWithIgnoreCase ](../functions/string-functions.md#endWithIgnoreCase) |
| String | [ equalIgnoreCase ](../functions/string-functions.md#equalIgnoreCase) |
| String | [indexOf](../functions/string-functions.md#indexOf) |
| String | [isEmpty](../functions/string-functions.md#isEmpty) |
| String | [isNotEmpty](../functions/string-functions.md#isNotEmpty) |
| String | [lastIndexOf](../functions/string-functions.md#lastIndexOf) |
| String | [length](../functions/string-functions.md#length) |
| String | [lower](../functions/string-functions.md#lower) |
| String | [matchRegExp](../functions/string-functions.md#matchRegExp) |
| String | [ notEqualIgnoreCase ](../functions/string-functions.md#notEqualIgnoreCase) |
| String | [replace](../functions/string-functions.md#replace) |
| String | [replaceAll](../functions/string-functions.md#replaceAll) |
| String | [split](../functions/string-functions.md#split) |
| String | [startWith](../functions/string-functions.md#startWith) |
| String | [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) |
| String | [substr](../functions/string-functions.md#substr) |
| String | [trim](../functions/string-functions.md#trim) |
| String | [upper](../functions/string-functions.md#upper) |
| String | [uuid](../functions/string-functions.md#uuid) |
