---
title: Functiebibliotheek
description: Functiebibliotheek
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---

# Samenvoegingsfuncties {#aggregation}

![](../../assets/do-not-localize/badge.png)

Samenvoegfuncties worden gebruikt om meerdere waarden te groeperen en één samenvattingswaarde te maken.

## Aantal{#count}

De functie `count` retourneert het aantal elementen binnen de opgegeven array.

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

De functie `sum` retourneert de som van alle geselecteerde waarden binnen de array.

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

De functie `average` retourneert het rekenkundig gemiddelde van alle geselecteerde waarden binnen de array.

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

De functie `min` retourneert de kleinste van alle geselecteerde waarden binnen de array.

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

De functie `max` retourneert de grootste van alle geselecteerde waarden binnen de array.

**Indeling**

```sql
{%= max(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de hoogste prijs van alle orders.

```sql
{%=max(orders.order.price)%}
```
