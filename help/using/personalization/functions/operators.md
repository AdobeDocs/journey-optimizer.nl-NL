---
title: Operatorfuncties, bibliotheek
description: Operatorfuncties, bibliotheek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 7%

---

# Operatoren {#operators}

## Booleaanse functies {#boolean-functions}

Booleaanse functies worden gebruikt voor het uitvoeren van Booleaanse logica op verschillende elementen.

### en{#and}

De `and` Deze functie wordt gebruikt om een logische combinatie te maken.

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

De `or` Deze functie wordt gebruikt om een logische scheiding te maken.

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

## Vergelijkingsfuncties {#comparison-functions}

Vergelijkingsfuncties worden gebruikt om verschillende expressies en waarden met elkaar te vergelijken en om waar of onwaar overeenkomstig te retourneren.

### Equals (Is gelijk aan){#equals}

De `=` (equals) functie controleert of één waarde of expressie gelijk is aan een andere waarde of expressie.

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

De `!=` (niet gelijk aan) functie controleert of één waarde of expressie **niet** gelijk aan een andere waarde of expressie.

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

De `>` (groter dan) wordt gebruikt om te controleren of de eerste waarde groter is dan de tweede waarde.

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

De `>=` (groter dan of gelijk aan) functie wordt gebruikt om te controleren of de eerste waarde groter dan of gelijk aan de tweede waarde is.

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

De `<` (kleiner dan) vergelijkingsfunctie wordt gebruikt om te controleren of de eerste waarde kleiner is dan de tweede waarde.

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

De `<=` (kleiner dan of gelijk aan) vergelijkingsfunctie wordt gebruikt om te controleren of de eerste waarde kleiner dan of gelijk is aan de tweede waarde.

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
