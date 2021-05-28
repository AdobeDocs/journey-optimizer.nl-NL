---
title: Functiebibliotheek
description: Functiebibliotheek
source-git-commit: cd1b07bbb4b247d1d8c0cc87be9e4bdad22377ed
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# Rekenkundige functies {#maths}

![](../../assets/do-not-localize/badge.png)

Rekenkundige functies worden gebruikt voor het uitvoeren van basisberekeningen op waarden.

## Toevoegen{#add}

De functie `+` (optellen) wordt gebruikt om de som twee argumentuitdrukkingen te vinden.

**Indeling**

```sql
{%= double + double %}
```

**Voorbeeld**

De volgende transactie geeft de prijs van twee verschillende producten weer.

```sql
{%= product1.price + product2.price %}
```

## Vermenigvuldigen{#multiply}

De functie `*` (vermenigvuldiging) wordt gebruikt om het product van twee argumentuitdrukkingen te vinden.

**Indeling**

```sql
{%= double * double %}
```

**Voorbeeld**

Bij de volgende bewerking worden het product van de inventaris en de prijs van een product gevonden om de brutowaarde van het product te bepalen.

```sql
{%= product.inventory * product.price %}
```

## Aftrekken{#substract}

De functie `-` (aftrekken) wordt gebruikt om het verschil van twee argumentuitdrukkingen te vinden.

**Indeling**

```sql
{%= double - double %}
```

**Voorbeeld**

De volgende transactie vindt het prijsverschil tussen twee verschillende producten.

```sql
{%= product1.price - product2.price %}
```

## Verdelen{#divide}

De functie `/` (delen) wordt gebruikt om het quotiënt van twee argumentuitdrukkingen te vinden.

**Indeling**

```sql
{%= double / double %}
```

**Voorbeeld**

Met de volgende bewerking wordt het quotiënt gevonden tussen de totale verkochte producten en het totale verdiende geld om de gemiddelde kosten per object te zien.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## Herinnering{#remainder}

De functie `%` (restbepaling bij deling/restbepaling) wordt gebruikt om de rest te zoeken na het delen van de twee argumentexpressies.

**Indeling**

```sql
{%= double % double %}
```

**Voorbeeld**

De volgende bewerking controleert of de leeftijd van de persoon met vijf personen kan worden gedeeld.

```sql
{%= person.age % 5 = 0 %}
```
