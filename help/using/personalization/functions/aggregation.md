---
title: Samenvoegingsfuncties, bibliotheek
description: Samenvoegingsfuncties, bibliotheek
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 3%

---

# Samenvoegingsfuncties {#aggregation}

Samenvoegfuncties worden gebruikt om meerdere waarden te groeperen en één samenvattingswaarde te maken.

## Gemiddelde{#average}

De functie `average` retourneert het rekenkundig gemiddelde van alle geselecteerde waarden binnen de array.

**Syntaxis**

```sql
{%= average(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de gemiddelde prijs van alle orders.

```sql
{%=average(orders.order.price)%}
```

## Aantal{#count}

De functie `count` retourneert het aantal elementen binnen de opgegeven array.

**Syntaxis**

```sql
{%= count(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert het aantal orders in de array.

```sql
{%= count(orders) %}
```

## Maximum{#max}

De functie `max` retourneert de grootste van alle geselecteerde waarden binnen de array.

**Syntaxis**

```sql
{%= max(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de hoogste prijs van alle orders.

```sql
{%=max(orders.order.price)%}
```

## Minimaal{#min}

De functie `min` retourneert het laagste van alle geselecteerde waarden binnen de array.

**Syntaxis**

```sql
{%= min(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de laagste prijs van alle orders.

```sql
{%=min(orders.order.price) %}
```

## Som{#sum}

De functie `sum` retourneert de som van alle geselecteerde waarden binnen de array.

**Syntaxis**

```sql
{%= sum(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de som van de prijzen van alle orders.

```sql
{%=sum(orders.order.price)%}
```
