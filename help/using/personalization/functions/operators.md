---
title: Functiebibliotheek
description: Functiebibliotheek
source-git-commit: ca739254e8b113d6f511573c0aa427427b263b3b
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 8%

---

# Operatoren {#operators}

![](../../assets/do-not-localize/badge.png)

## Booleaanse functies

Booleaanse functies worden gebruikt voor het uitvoeren van Booleaanse logica op verschillende elementen.

### en{#and}

De functie `and` wordt gebruikt om een logische samenhang tot stand te brengen.

**Indeling**

```sql
{%= query1 and query2 %}
```

**Voorbeeld**

De volgende operatie zal alle mensen met een thuisland als Frankrijk en geboortejaar 1985 terugsturen.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### of{#or}

De functie `or` wordt gebruikt om een logische scheiding tot stand te brengen.

**Indeling**

```sql
{%= query1 or query2 %}
```

**Voorbeeld**

De volgende operatie zal alle mensen terugsturen die in Frankrijk of in 1985 in het land van herkomst wonen.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Format**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->





## Vergelijkingsfuncties

Vergelijkingsfuncties worden gebruikt om verschillende expressies en waarden met elkaar te vergelijken en om waar of onwaar overeenkomstig te retourneren.

### Equals (Is gelijk aan){#equals}

De functie `=` (equals) controleert of één waarde of expressie gelijk is aan een andere waarde of expressie.

**Indeling**

```sql
{%= expression = value %}
```

**Voorbeeld**

De volgende operatie controleert of het thuisadresland Frankrijk is.

```sql
{%= profile.homeAddress.country = "France" %}
```

### Niet gelijk{#notequal}

De functie `!=` (niet gelijk aan) controleert of één waarde of expressie **niet** gelijk is aan een andere waarde of expressie.

**Indeling**

```sql
{%= expression != value %}
```

**Voorbeeld**

De volgende operatie controleert of het thuisadresland niet Frankrijk is.

```sql
{%= profile.homeAddress.country != "France" %}
```

### Greater than{#greaterthan}

De functie `>` (groter dan) wordt gebruikt om te controleren of de eerste waarde groter is dan de tweede waarde.

**Indeling**

```sql
{%= expression1 > expression2 %}
```

**Voorbeeld**

De volgende bewerking definieert personen die strikt na 1970 geboren zijn.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Greater than or equal to{#greaterthanorequal}

De functie `>=` (groter dan of gelijk aan) wordt gebruikt om te controleren of de eerste waarde groter dan of gelijk aan de tweede waarde is.

**Indeling**

```sql
{%= expression1 >= expression2 %}
```

**Voorbeeld**

In de volgende bewerking worden personen gedefinieerd die in of na 1970 zijn geboren.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Less than{#lessthan}

De vergelijkingsfunctie `<` (kleiner dan) wordt gebruikt om te controleren of de eerste waarde minder is dan de tweede waarde.

**Indeling**

```sql
{%= expression1 < expression2 %}
```

**Voorbeeld**

In de volgende bewerking worden personen gedefinieerd die vóór 2000 zijn geboren.

```sql
{%= profile.person.birthYear < 2000 %}
```

### Less than or equal to{#lessthanorequal}

De vergelijkingsfunctie `<=` (kleiner dan of gelijk aan) wordt gebruikt om te controleren of de eerste waarde kleiner dan of gelijk aan de tweede waarde is.

**Indeling**

```sql
{%= expression1 <= expression2 %}
```

**Voorbeeld**

De volgende bewerking definieert personen die in 2000 of eerder zijn geboren.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Bewerkingen met getallen**

