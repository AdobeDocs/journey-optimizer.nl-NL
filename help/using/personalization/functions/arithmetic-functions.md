---
title: Rekenkundige functiebibliotheek
description: Rekenkundige functiebibliotheek
feature: Personalisatie
topic: Personalisatie
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 3%

---

# Rekenkundige functies {#maths}

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
