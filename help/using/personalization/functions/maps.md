---
title: Functiebibliotheek met kaarten
description: Functiebibliotheek met kaarten
feature: Personalisatie
topic: Personalisatie
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---

# Functies toewijzen{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) biedt functies om interactie met kaarten eenvoudiger te maken.

## Get{#get}

De functie `get` wordt gebruikt om de waarde van een kaart voor een bepaalde sleutel terug te winnen.

**Indeling**

```sql
{%= get(map, string) %}
```

**Voorbeeld**

De volgende verrichting krijgt de waarde van de identiteitskaart voor de sleutel `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Toetsen{#keys}

De functie `keys` wordt gebruikt om alle sleutels voor een bepaalde kaart terug te winnen.

**Indeling**

```sql
{%= keys(map) %}
```

**Voorbeeld**

Met de volgende bewerking worden alle toetsen voor de kaart `identityMap` opgehaald.

```sql
{%= keys(identityMap) %}
```

## Waarden{#values}

De functie `values` wordt gebruikt om alle waarden van een bepaalde kaart terug te winnen.

**Indeling**

```sql
{%= values(map) %}
```

**Voorbeeld**

Met de volgende bewerking worden alle waarden voor de kaart `identityMap` opgehaald.

```sql
{%= values(identityMap) %}
```
