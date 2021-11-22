---
title: Samenvoegingsfuncties, bibliotheek
description: Samenvoegingsfuncties, bibliotheek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 3%

---

# Samenvoegingsfuncties {#aggregation}

Samenvoegfuncties worden gebruikt om meerdere waarden te groeperen en één samenvattingswaarde te maken.

## Aantal{#count}

De `count` function retourneert het aantal elementen binnen de opgegeven array.

**Indeling**

```sql
{%= count(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert het aantal orders in de array.

```sql
{%= count(orders) %}
```

## Som{#sum}

De `sum` Deze functie retourneert de som van alle geselecteerde waarden binnen de array.

**Indeling**

```sql
{%= sum(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de som van de prijzen van alle orders.

```sql
{%=sum(orders.order.price)%}
```

## Gemiddelde{#average}

De `average` Deze functie retourneert het rekenkundig gemiddelde van alle geselecteerde waarden binnen de array.

**Indeling**

```sql
{%= average(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de gemiddelde prijs van alle orders.

```sql
{%=average(orders.order.price)%}
```

## Minimaal{#min}

De `min` Deze functie retourneert het kleinste van alle geselecteerde waarden binnen de array.

**Indeling**

```sql
{%= min(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de laagste prijs van alle orders.

```sql
{%=min(orders.order.price)%}
```

## Maximum{#max}

De `max` functie retourneert de grootste van alle geselecteerde waarden binnen de array.

**Indeling**

```sql
{%= max(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de hoogste prijs van alle orders.

```sql
{%=max(orders.order.price)%}
```
