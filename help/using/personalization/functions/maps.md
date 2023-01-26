---
title: Functiebibliotheek met kaarten
description: Functiebibliotheek met kaarten
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 5%

---

# Functies toewijzen{#maps}

Gebruik de functies Kaart in verpersoonlijking om interactie met kaarten gemakkelijker te maken.

## Get{#get}

De `get` wordt gebruikt om de waarde van een kaart voor een bepaalde sleutel terug te winnen.

**Syntaxis**

```sql
{%= get(map, string) %}
```

**Voorbeeld**

Met de volgende bewerking wordt de waarde van het identiteitsoverzicht voor de sleutel opgehaald `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Toetsen{#keys}

De `keys` wordt gebruikt om alle sleutels voor een bepaalde kaart terug te winnen.

**Syntaxis**

```sql
{%= keys(map) %}
```

**Voorbeeld**

Met de volgende bewerking worden alle toetsen voor de kaart opgehaald `identityMap`.

```sql
{%= keys(identityMap) %}
```

## Waarden{#values}

De `values` wordt gebruikt om alle waarden van een bepaalde kaart op te halen.

**Syntaxis**

```sql
{%= values(map) %}
```

**Voorbeeld**

Met de volgende bewerking worden alle waarden voor de kaart opgehaald `identityMap`.

```sql
{%= values(identityMap) %}
```
