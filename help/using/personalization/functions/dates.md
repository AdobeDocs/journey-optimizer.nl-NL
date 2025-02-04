---
title: Date Time-functiebibliotheek
description: Date Time-functiebibliotheek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3eab04f28b1daab556c4b4395d67f28d292fc52b
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 3%

---

# Datumtijdfuncties{#date-time}

Datum- en tijdfuncties worden gebruikt om datum- en tijdbewerkingen uit te voeren op waarden in Journey Optimizer.

## Dagen toevoegen {#add-days}

De functie `addDays` past een bepaalde datum met een bepaald aantal dagen aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.

**Syntaxis**

```sql
{%= addDays(date, number) %}
```

+++Example

* Invoer: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Uitvoer: `2024-11-11T17:19:51Z`

+++

## Uren toevoegen {#add-hours}

De functie `addHours` past een bepaalde datum met een bepaald aantal uren aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.

**Syntaxis**

```sql
{%= addHours(date, number) %}
```

+++Example

* Invoer: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Uitvoer: `2024-11-01T18:19:51Z`

+++

## Minuten toevoegen {#add-minutes}

De functie `addMinutes` past een bepaalde datum met een opgegeven aantal minuten aan, waarbij positieve waarden worden gebruikt voor verhogen en negatieve waarden voor verlagen

**Syntaxis**

```sql
{%= addMinutes(date, number) %}
```

+++Example

* Invoer: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Uitvoer: `2024-11-01T18:09:51Z`

+++

## Maanden toevoegen {#add-months}

De functie `addMonths` past een bepaalde datum met een bepaald aantal maanden aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.

**Syntaxis**

```sql
{%= addMonths(date, number) %}
```

+++Example

* Invoer: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Uitvoer: `2025-01-01T17:19:51Z`

+++

## Seconden toevoegen {#add-seconds}

In `addSeconds` wordt een bepaalde datum met een opgegeven aantal seconden aangepast, waarbij positieve waarden worden gebruikt voor verhogen en negatieve waarden voor verlagen.

**Syntaxis**

```sql
{%= addSeconds(date, number) %}
```

+++Example

* Invoer: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Uitvoer: `2024-11-01T17:20:01Z`

+++

## Jaren toevoegen {#add-years}

In `addYears` wordt een bepaalde datum met een opgegeven aantal jaren aangepast met positieve waarden voor verhogen en negatieve waarden voor verlagen.

**Syntaxis**

```sql
{%= addYears(date, number) %}
```

+++Example

* Invoer: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Uitvoer: `2026-11-01T17:19:51Z`

+++

## Leeftijd{#age}

De functie `age` wordt gebruikt om de leeftijd vanaf een bepaalde datum op te halen.

**Syntaxis**

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

## Leeftijd in dagen {#age-days}

De functie `ageInDays` berekent de leeftijd van een bepaalde datum in dagen, d.w.z. het aantal dagen dat is verstreken tussen de gegeven datum en de huidige datum, negatief voor toekomstige datums en positief voor eerdere datums.

**Syntaxis**

```sql
{%= ageInDays(date) %}
```

+++Example

currentDate = 2025-01-07T12 :17: 10.720122+05:30 (Azië/Kolkata)

* Invoer: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Uitvoer: `5`

+++

## Leeftijd in maanden {#age-months}

De functie `ageInMonths` berekent de leeftijd van een bepaalde datum in maanden, d.w.z. het aantal maanden dat is verstreken tussen de gegeven datum en de huidige datum, negatief voor toekomstige datums en positief voor datums in het verleden.

**Syntaxis**

```sql
{%= ageInMonths(date) %}
```

+++Example

currentDate = 2025-01-07T12 :22: 46.993748+05:30 (Azië/Kolkata)

* Invoer: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Uitvoer: `12`

+++

## Datums vergelijken {#compare-dates}

De functie `compareDates` vergelijkt de eerste invoerdatum met de andere. Retourneert 0 als date1 gelijk is aan date2, -1 als date1 voor date2 komt en 1 als date1 na date2 komt.

**Syntaxis**

```sql
{%= compareDates(date1, date2) %}
```

+++Example

* Invoer: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Uitvoer: `-1`

+++

## ZonedDateTime converteren {#convert-zoned-date-time}

De functie `convertZonedDateTime` zet een datum-tijd om in een bepaalde tijdzone.

**Syntaxis**

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

+++Example

* Invoer: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Uitvoer: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

## Huidige tijd in milliseconden{#current-time}

De functie `currentTimeInMillis` wordt gebruikt om de huidige tijd in epoch milliseconds terug te winnen.

**Syntaxis**

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

## Datumverschil{#date-diff}

De functie `dateDiff` wordt gebruikt om het verschil tussen twee datums in aantal dagen op te halen.

**Syntaxis**

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Dag van de maand {#day-month}

De `dayOfWeek` retourneert het getal dat de dag van de maand vertegenwoordigt.

**Syntaxis**

```sql
{%= dayOfMonth(datetime) %}
```

+++Example

* Invoer: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Uitvoer: `5`

+++


## Dag van de week {#day-week}

De functie `dayOfWeek` wordt gebruikt om de dag van de week terug te winnen.

**Syntaxis**

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Dag van jaar{#day-year}

De functie `dayOfYear` wordt gebruikt om de dag van het jaar op te halen.

**Syntaxis**

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Binnen seconden diff {#diff-seconds}

De functie `diffInSeconds` retourneert het verschil tussen twee datums in seconden.

**Syntaxis**

```sql
{%= diffInSeconds(endDate, startDate) %}
```

+++Example

* Invoer: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Uitvoer: `50`

+++

## Uren extraheren {#extract-hours}

De functie `extractHours` extraheert de uurcomponent uit een bepaald tijdstempel.

**Syntaxis**

```sql
{%= extractHours(date) %}
```

+++Example

* Invoer: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `17`

+++

## Minuten extraheren {#extract-minutes}

De functie `extractMinutes` extraheert de component minute uit een bepaald tijdstempel.

**Syntaxis**

```sql
{%= extractMinutes(date) %}
```

+++Example

* Invoer: `{%= extractMinute(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `19`

+++

## Maanden uitnemen {#extract-months}

De functie `extractMonth` extraheert de component month uit een opgegeven tijdstempel.

**Syntaxis**

```sql
{%= extractMonths(date) %}
```

+++Example

* Invoer: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `11`

+++

## Seconden extraheren {#extract-seconds}

De functie `extractSeconds` extraheert de tweede component uit een bepaald tijdstempel.

**Syntaxis**

```sql
{%= extractSeconds(date) %}
```

+++Example

* Invoer: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `51`

+++

## Indelingsdatum{#format-date}

De functie `formatDate` wordt gebruikt om een datumtijdwaarde op te maken. De indeling moet een geldig Java DateTimeFormat-patroon zijn.

**Syntaxis**

```sql
{%= formatDate(datetime, format) %}
```

Waar de eerste tekenreeks het datumkenmerk is en de tweede waarde hoe u de datum wilt omzetten en weergeven.

>[!NOTE]
>
> Als een datumpatroon ongeldig is, wordt de datum teruggezet naar de ISO-standaardindeling.
>
> U kunt de datum die functies gebruiken Java zoals samengevat in [ documentatie van het Oracle ](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html) {_blank}

**Voorbeeld**

De volgende bewerking retourneert de datum in de volgende notatie: MM/DD/YY.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

## Datumnotatie met ondersteuning voor landinstellingen{#format-date-locale}

De functie `formatDate` wordt gebruikt om een datumtijdwaarde op te maken in de corresponderende taalgevoelige representatie, d.w.z. in een gewenste landinstelling. De indeling moet een geldig Java DateTimeFormat-patroon zijn.

**Syntaxis**

```sql
{%= formatDate(datetime, format, locale) %}
```

Waar de eerste tekenreeks het datumkenmerk is, is de tweede waarde hoe u de datum wilt converteren en weergeven en de derde waarde de landinstelling in tekenreeksindeling.

>[!NOTE]
>
> Als een datumpatroon ongeldig is, wordt de datum teruggezet naar de ISO-standaardindeling.
>
> U kunt de datum het formatteren functies van Java zoals samengevat in [ documentatie van het Oracle ](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html) gebruiken.
>
> U kunt het formatteren en geldige scènes gebruiken zoals samengevat in [ documentatie van het Oracle ](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) en [ Gesteunde scènes ](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Voorbeeld**

De volgende bewerking retourneert de datum in de volgende notatie: MM/DD/YY en landinstelling FRANKRIJK.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## Get CurrentZonedDateTime {#get-current-zoned-date-time}

De functie `getCurrentZonedDateTime` retourneert de huidige datum en tijd met informatie over de tijdzone.

**Syntaxis**

```sql
{%= getCurrentZonedDateTime() %}
```

+++Example

* Invoer: `{%= getCurrentZonedDateTime() %}`
* Uitvoer: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

## Verschil in uren {#hours-difference}

De functie `diffInHours` retourneert het verschil tussen twee datums in termen van uren.

**Syntaxis**

```sql
{%= diffInHours(endDate, startDate) %}
```

+++Example

* Invoer: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Uitvoer: `10`

+++

## Verschil in minuten{#diff-minutes}

De functie `diffInMinutes` wordt gebruikt om het verschil tussen twee datums in termen van minuten te retourneren.

**Syntaxis**

```sql
{%= diffInMinutes(endDate, startDate) %}
```

+++Example

* Invoer: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Uitvoer: `60`

+++

## Verschil in maanden {#months-difference}

De functie `diffInMonths` retourneert het verschil tussen twee datums in termen van maanden.

**Syntaxis**

```sql
{%= diffInMonths(endDate, startDate) %}
```

+++Example

* Invoer: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Uitvoer: `3`

+++

## Aantal dagen instellen{#set-days}

De functie `setDays` wordt gebruikt om de dag van de maand voor de bepaalde datum-tijd te plaatsen.

**Syntaxis**

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Uren instellen{#set-hours}

De functie `setHours` wordt gebruikt om het uur van de datum-tijd te plaatsen.

**Syntaxis**

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Tot op heden {#to-date-time}

De functie `ToDateTime` zet een tekenreeks om in datum. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer.

**Syntaxis**

```sql
{%= toDateTime(string, string) %}
```

+++Example

* Invoer: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Uitvoer: `2024-11-01T17:19:51Z`

+++

## Naar UTC{#to-utc}

De functie `toUTC` wordt gebruikt om een datetime in UTC om te zetten.

**Syntaxis**

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Korten naar begin van dag {#truncate-day}

De functie `truncateToStartOfDay` wordt gebruikt om een bepaalde datum-tijd te wijzigen door het te plaatsen aan het begin van de dag met de tijd die aan 00:00 wordt geplaatst.

**Syntaxis**

```sql
{%= truncateToStartOfDay(date) %}
```

+++Example

* Invoer: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Uitvoer: `2024-11-01T00:00Z`

+++

## truncateToStartOfQuarter {#truncate-quarter}

De functie `truncateToStartOfQuarter` wordt gebruikt om een datum-tijd tot de eerste dag van zijn kwart (b.v., Jan 1, Apr 1, jul 1, okt 1) om 00:00 af te kappen.

**Syntaxis**

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

+++Example

* Invoer: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `2024-10-01T00:00Z`

+++

## truncateToStartOfWeek {#truncate-week}

De functie `truncateToStartOfWeek` wijzigt een bepaalde datum-tijd door het aan het begin van de week (Maandag om 00:00) te plaatsen.

**Syntaxis**

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

+++Example

* Invoer: `truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Uitvoer: `2024-11-18T00:00Z // monday`

+++

## truncateToStartOfYear {#truncate-year}

De functie `truncateToStartOfYear` wordt gebruikt om een bepaalde datum-tijd te wijzigen door het te beknotten aan de eerste dag van het jaar (1 januari) om 00:00.

**Syntaxis**

```sql
{%= truncateToStartOfYear(dateTime) %}
```

+++Example

* Invoer: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `2024-01-01T00:00Z`

+++

## Week van jaar {#week-of-year}

De functie `weekOfYear` wordt gebruikt om de week van het jaar op te halen.

**Syntaxis**

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Verschil in jaren {#diff-years}

De functie `diffInYears` wordt gebruikt om het verschil tussen twee datums in termen van jaren te retourneren.

**Syntaxis**

```sql
{%= diffInYears(endDate, startDate) %}: int
```

+++Example

* Invoer: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Uitvoer: `5`

+++
