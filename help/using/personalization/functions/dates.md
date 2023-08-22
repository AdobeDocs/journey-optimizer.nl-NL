---
title: Date Time-functiebibliotheek
description: Date Time-functiebibliotheek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3a4a58f8601c67e8e9a2b606a47c6b4bcc2dab05
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 3%

---

# Datumtijdfuncties{#date-time}

Datum- en tijdfuncties worden gebruikt om datum- en tijdbewerkingen uit te voeren op waarden in Journey Optimizer.

## Leeftijd{#age}

De `age` Deze functie wordt gebruikt om de leeftijd vanaf een bepaalde datum op te halen.

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

## Huidige tijd in milliseconden{#current-time}

De `currentTimeInMillis` Deze functie wordt gebruikt om de huidige tijd in epoch milliseconds op te halen.

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

De `dateDiff` wordt gebruikt om het verschil tussen twee datums in aantal dagen op te halen.

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


## Dag van de week{#day-week}

De `dayOfWeek` Deze functie wordt gebruikt om de dag van de week op te halen.

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

De `dayOfYear` Deze functie wordt gebruikt om de dag van het jaar op te halen.

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

## Indelingsdatum{#format-date}

De `formatDate` Deze functie wordt gebruikt om een datumtijdwaarde op te maken. De indeling moet een geldig Java DateTimeFormat-patroon zijn.

**Syntaxis**

```sql
{%= formatDate(datetime, format) %}
```

Waar de eerste tekenreeks het datumkenmerk is en de tweede waarde hoe u de datum wilt omzetten en weergeven.

>[!NOTE]
>
> Als een datumpatroon ongeldig is, wordt de datum teruggezet naar de ISO-standaardindeling.
>
> U kunt functies voor datumnotatie gebruiken die zijn samengevat in [Documentatie oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Voorbeeld**

De volgende bewerking retourneert de datum in de volgende notatie: MM/DD/YY.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

## Datumnotatie met ondersteuning voor landinstellingen{#format-date-locale}

De `formatDate` wordt gebruikt om een datumtijdwaarde op te maken in de corresponderende taalgevoelige representatie, d.w.z. in een gewenste landinstelling. De indeling moet een geldig Java DateTimeFormat-patroon zijn.

**Syntaxis**

```sql
{%= formatDate(datetime, format, locale) %}
```

Waar de eerste tekenreeks het datumkenmerk is, is de tweede waarde hoe u de datum wilt converteren en weergeven en de derde waarde de landinstelling in tekenreeksindeling.

>[!NOTE]
>
> Als een datumpatroon ongeldig is, wordt de datum teruggezet naar de ISO-standaardindeling.
>
> U kunt functies voor datumnotatie gebruiken die zijn samengevat in [Documentatie oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> U kunt opmaak en geldige landinstellingen gebruiken, zoals in [Documentatie oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) en [Ondersteunde landinstellingen](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).


**Voorbeeld**

De volgende bewerking retourneert de datum in de volgende notatie: MM/DD/YY en landinstelling FRANKRIJK.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## Aantal dagen instellen{#set-days}

De `setDays` wordt gebruikt om de dag van de maand voor de bepaalde datum-tijd te plaatsen.

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

De `setHours` wordt gebruikt om het uur van de datum-tijd te plaatsen.

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


## Naar UTC{#to-utc}

De `toUTC` wordt gebruikt om een datetime in UTC om te zetten.


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


## Week van jaar UTC{#week-of-year}

De `weekOfYear` Deze functie wordt gebruikt om de week van het jaar op te halen.

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