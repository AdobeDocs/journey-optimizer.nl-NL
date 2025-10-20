---
title: Operatorfuncties, bibliotheek
description: Operatorfuncties, bibliotheek
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 2%

---

# Operatoren {#operators}

## Booleaanse functies {#boolean-functions}

Booleaanse functies worden gebruikt voor het uitvoeren van Booleaanse logica op verschillende elementen.

### en{#and}

De functie `and` wordt gebruikt om een logische combinatie te maken.

**Syntaxis**

```sql
{%= query1 and query2 %}
```

**Voorbeeld**

De volgende operatie zal alle mensen met een thuisland als Frankrijk en geboortejaar 1985 terugsturen.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### of{#or}

De functie `or` wordt gebruikt om een logische scheiding te maken.

**Syntaxis**

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

**Syntax**

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

### Gelijk{#equals}

De functie `=` (equals) controleert of een waarde of expressie gelijk is aan een andere waarde of expressie.

**Syntaxis**

```sql
{%= expression = value %}
```

**Voorbeeld**

De volgende operatie controleert of het thuisadresland Frankrijk is.

```sql
{%= profile.homeAddress.country = "France" %}
```

### Niet gelijk{#notequal}

De `!=` (niet gelijk aan) functie controleert of één waarde of uitdrukking **&#x200B;**&#x200B;niet gelijk aan een andere waarde of een uitdrukking is.

**Syntaxis**

```sql
{%= expression != value %}
```

**Voorbeeld**

De volgende operatie controleert of het thuisadresland niet Frankrijk is.

```sql
{%= profile.homeAddress.country != "France" %}
```

### Groter dan{#greaterthan}

De functie `>` (groter dan) wordt gebruikt om te controleren of de eerste waarde groter is dan de tweede waarde.

**Syntaxis**

```sql
{%= expression1 > expression2 %}
```

**Voorbeeld**

De volgende bewerking definieert personen die strikt na 1970 geboren zijn.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Groter dan of gelijk aan{#greaterthanorequal}

De functie `>=` (groter dan of gelijk aan) wordt gebruikt om te controleren of de eerste waarde groter dan of gelijk is aan de tweede waarde.

**Syntaxis**

```sql
{%= expression1 >= expression2 %}
```

**Voorbeeld**

In de volgende bewerking worden personen gedefinieerd die in of na 1970 zijn geboren.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Minder dan{#lessthan}

De vergelijkingsfunctie `<` (kleiner dan) wordt gebruikt om te controleren of de eerste waarde kleiner is dan de tweede waarde.

**Syntaxis**

```sql
{%= expression1 < expression2 %}
```

**Voorbeeld**

In de volgende bewerking worden personen gedefinieerd die vóór 2000 zijn geboren.

```sql
{%= profile.person.birthYear < 2000 %}
```

### Kleiner dan of gelijk aan{#lessthanorequal}

De vergelijkingsfunctie `<=` (kleiner dan of gelijk aan) wordt gebruikt om te controleren of de eerste waarde kleiner dan of gelijk is aan de tweede waarde.

**Syntaxis**

```sql
{%= expression1 <= expression2 %}
```

**Voorbeeld**

De volgende bewerking definieert personen die in 2000 of eerder zijn geboren.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Verrichtingen met aantallen**
