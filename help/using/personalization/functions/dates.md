---
title: Date Time-functiebibliotheek
description: Date Time-functiebibliotheek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: f06e1e03b3660be36b32437647a8329d0c0d296e
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Datumtijdfuncties{#date-time}

Datum- en tijdfuncties worden gebruikt om datum- en tijdbewerkingen uit te voeren op waarden in Journey Optimizer.

## Leeftijd{#age}

De `age` Deze functie wordt gebruikt om de leeftijd vanaf een bepaalde datum op te halen.

**Indeling**

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

## Huidige tijd in milliseconden{#current-time}

De `currentTimeInMillis` Deze functie wordt gebruikt om de huidige tijd in epoch milliseconds op te halen.

**Indeling**

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

De `dateDiff` wordt gebruikt om het verschil tussen twee datums in aantal dagen op te halen.

**Indeling**

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


## Dag van de week{#day-week}

De `dayOfWeek` Deze functie wordt gebruikt om de dag van de week op te halen.

**Indeling**

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

## Dag van het jaar{#day-year}

De `dayOfYear` wordt gebruikt om de dag van het jaar terug te winnen.

**Indeling**

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

## Indelingsdatum{#format-date}

De `formatDate` Deze functie wordt gebruikt om een datumtijdwaarde op te maken. De indeling moet een geldig Java DateTimeFormat-patroon zijn.

**Indeling**

```sql
{%= formatDate(datetime, format) %}
```

Waar de eerste tekenreeks het datumkenmerk is en de tweede waarde hoe u de datum wilt omzetten en weergeven.

>[!NOTE]
>
> Als een datumpatroon ongeldig is, wordt de datum teruggezet naar de ISO-standaardindeling.
>
> U kunt functies voor datumnotatie in Java gebruiken als een overzicht [in de documentatie bij Oracles](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Voorbeeld**

De volgende bewerking retourneert de datum in de volgende notatie: DD-MM-YY.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## Aantal dagen instellen{#set-days}

De `setDays` wordt gebruikt om de dag van de maand voor de bepaalde datum-tijd te plaatsen.

**Indeling**

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

De `setHours` wordt gebruikt om het uur van de datum-tijd te plaatsen.

**Indeling**

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


## Naar UTC{#to-utc}

De `toUTC` wordt gebruikt om een datetime in UTC om te zetten.


**Indeling**

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


## Week van jaar UTC{#week-of-year}

De `weekOfYear` Deze functie wordt gebruikt om de week van het jaar op te halen.

**Indeling**

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