---
product: journey optimizer
title: Datumfuncties
description: Meer informatie over datumfuncties
feature: Journeys
role: Developer
level: Experienced
keywords: datum, functies, expressie, reis, tijd
version: Journey Orchestration
source-git-commit: 42abfcc9711d87b2dc00df47e964dad07443f0ed
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 6%

---

# Datumfuncties {#date-functions}

Met Date-functies kunt u datum- en tijdwaarden bewerken en gebruiken in uw reisexpressies. Deze functies zijn essentieel voor op tijd-gebaseerde voorwaarden, planning, en tijdberekeningen in uw klantenreizen.

Gebruik datumfuncties wanneer u dit moet doen:

* Hiermee wordt de huidige tijd of datum opgehaald met specifieke tijdzone-verwerking
* Controleren of een datum binnen een specifiek tijdbereik (verleden of toekomst) valt
* Datum- en tijdcomponenten wijzigen (uren, dagen, tijdzones)
* Op tijd gebaseerde berekeningen en vergelijkingen uitvoeren
* Omzetten tussen verschillende tijdnotaties en weergaven

De functies van de datum verstrekken nauwkeurige controle over tijdslogica, toestaand u om tijd-gevoelige reiswegen en voorwaarden tot stand te brengen die aan specifieke tijdkaders en programma&#39;s antwoorden.

## currentTimeInMillis {#currentTimeInMillis}

Geeft de huidige tijd in epoch milliseconds.

+++Syntaxis

`currentTimeInMillis()`

+++

+++Parameters

Deze functie gebruikt geen parameters.

+++

+++Handtekeningen en type geretourneerd

`currentTimeInMillis()`

Retourneert een geheel getal.

+++

+++Voorbeelden

`currentTimeInMillis()`

Retourneert &quot;1544712617131&quot;.

+++

## inLastDays {#inLastDays}

Geeft als resultaat waar als een bepaalde dateTime tussen nu en nu is - delta dagen.

+++Syntaxis

`inLastDays(<dateTime>,<delta>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

+++

+++Handtekeningen en type geretourneerd

`inLastDays(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retourneert true.

+++

## inLastHours {#inLastHours}

Retourneert true als de opgegeven datumtijd tussen nu en nu ligt - delta-uren.

+++Syntaxis

`inLastHours(<dateTime>,<delta>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

+++

+++Handtekeningen en type geretourneerd

`inLastHours(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retourneert true.

`inLastHours(@event{MyEvent.timestamp}, 4)`

Retourneert true.

+++

## inLastMonths {#inLastMonths}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu bevindt - delta-maanden.

+++Syntaxis

`inLastMonths(<dateTime>,<delta>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

+++

+++Handtekeningen en type geretourneerd

`inLastMonths(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retourneert true.

+++

## inLastYears {#inLastYears}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu bevindt - delta-jaren.

+++Syntaxis

`inLastYears(<dateTime>,<delta>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

+++

+++Handtekeningen en type geretourneerd

`inLastYears(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retourneert true.

+++

## inNextDays {#inNextDays}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu + delta dagen bevindt.

+++Syntaxis

`inNextDays(<dateTime>,<delta>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

+++

+++Handtekeningen en type geretourneerd

`inNextDays(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retourneert true.

+++

## inNextHours {#inNextHours}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu + delta-uren bevindt.

+++Syntaxis

`inNextHours(<dateTime>,<delta>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

+++

+++Handtekeningen en type geretourneerd

`inNextHours(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retourneert true.

+++

## inNextMonths {#inNextMonths}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu + delta maanden bevindt.

+++Syntaxis

`inNextMonths(<dateTime>,<delta>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

+++

+++Handtekeningen en type geretourneerd

`inNextMonths(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Retourneert true.

+++

## inNextYears {#inNextYears}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu + delta jaar bevindt.

+++Syntaxis

`inNextYears(<dateTime>,<delta>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

+++

+++Handtekeningen en type geretourneerd

`inNextYears(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Retourneert true.

+++

## now {#now}

Retourneert de huidige datum in de datumtijdnotatie. Voor meer informatie over gegevenstypes, verwijs naar [&#x200B; deze pagina &#x200B;](../expression/data-types.md).

+++Syntaxis

`now(<parameter>)`

+++

+++Parameters

| Parameter | Beschrijving |
|--- |--- |
| string | Identificatiecode tijdzone (optioneel) |

+++

+++Handtekeningen en type geretourneerd

`now()`

`now("<timeZone id>")`

Retourneert een dateTime.

+++

+++Voorbeelden

`now()`

Keert 2023-06-03T06 :30Z terug.

`toString(now())`

Retourneert &quot;2023-06-03T06 :30Z&quot;

`now("Europe/Paris")`

Keert 2023-06-03T08 :30+02 :00 terug.

+++

## nowWithDelta {#nowWithDelta}

Retourneert de huidige datumtijd inclusief een verschuiving. Als een tijdzone-id wordt opgegeven, wordt de verschuiving van de tijdzone toegepast. Voor meer informatie over gegevenstypes, verwijs naar [&#x200B; deze pagina &#x200B;](../expression/data-types.md).

+++Syntaxis

`nowWithDelta(<parameters>)`

+++

+++Parameters

| Parameter | Beschrijving |
|--- |--- |
| delta | positieve of negatieve gehele waarde |
| datumonderdeel | jaar, maanden, dagen, uren, minuten of seconden als een tekenreeks |
| tijdzone-id | tekenreeksrepresentatie van de tijdzonewaarde. Voor meer, zie [&#x200B; types van Gegevens &#x200B;](../expression/data-types.md). Tijdzone-id moet een tekenreeksconstante zijn. Het kan geen veldverwijzing of expressie zijn. |

+++

+++Handtekeningen en type geretourneerd

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Retourneert een dateTime.

+++

+++Voorbeelden

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Retourneert precies 2 uur geleden een dateTime.

+++

## setHours {#setHours}

Hiermee stelt u alleen de uren van een datumtijd of datumtijd in. Als u bijvoorbeeld tot een bepaald uur wilt wachten, kunt u het uur forceren.

+++Syntaxis

`setHours(<parameter>)`

+++

+++Parameters

| Parameter | Type |
|--- |--- |
| datumtijd | dateTime |
| datumtijd zonder tijdzone te overwegen | dateTimeOnly |
| uren | integer |

+++

+++Handtekeningen en type geretourneerd

`setHours(<dateTime>,<hours>)`

Retourneert een datetime.

`setHours(<dateTimeOnly>,<hours>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

+++

+++Voorbeelden

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Keert 2023-12-12T04 :11: 00Z terug.

`setHours(nowWithDelta(1, "days"), 20)`

Keert morgen bij 8 :XY PM terug, XY die de notulen op het ogenblik van de huidige tijdevaluatie zijn. Als de evaluatie bij 2 :45 AM gebeurt, zal de teruggekeerde tijd 8 :45 PM zijn.

+++

## setDays {#setDays}

Hiermee stelt u alleen de dag van een datumtijd of datumtijd in. Als u bijvoorbeeld wilt wachten tot een bepaalde dag van de maand, kunt u de dag forceren.

+++Syntaxis

`setDays(<parameter>)`

+++

+++Parameters

| Parameter | Type |
|--- |--- |
| datumtijd | dateTime |
| datumtijd zonder tijdzone te overwegen | dateTimeOnly |
| dagen | integer |

+++

+++Handtekeningen en type geretourneerd

`setDays(<dateTime>,<days>)`

Retourneert een datetime.

`setDays(<dateTimeOnly>,<days>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

+++

+++Voorbeelden

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Keert 2023-12-25T01 :11: 00Z terug.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`

+++

## updateTimeZone {#updateTimeZone}

Retourneert een nieuwe datumtijd met een nieuwe tijdzone op hetzelfde moment.

+++Syntaxis

`updateTimeZone(<parameters>)`

+++

+++Parameters

* tijdzone-id: tekenreeks
* dateTime

+++

+++Handtekening en type geretourneerd

`updateTimeZone(<dateTime>,<timeZone id>)`

Retourneert een datetime.

+++

+++Voorbeelden

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Keert 2023-08-28T17 :15: 30.123+02 :00 terug.

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

Als de waarde van het tijdstempelveld `2021-11-16T16:55:12.939318+01:00` is, retourneert de functie `2021-11-17T02:55:12.942115+11:00` .

+++

