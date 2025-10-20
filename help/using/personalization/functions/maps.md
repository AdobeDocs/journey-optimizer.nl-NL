---
title: Functiebibliotheek met kaarten
description: Functiebibliotheek met kaarten
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---

# Functies toewijzen{#maps}

Gebruik de functies Kaart in personalisatie om interactie met kaarten gemakkelijker te maken.

## Get{#get}

De functie `get` wordt gebruikt om de waarde van een kaart voor een bepaalde sleutel terug te winnen.

**Syntaxis**

```sql
{%= get(map, string) %}
```

**Voorbeeld**

Met de volgende bewerking wordt de waarde van de identiteitskaart voor de sleutel `example@example.com` opgehaald.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Toetsen{#keys}

De functie `keys` wordt gebruikt om alle sleutels voor een bepaalde kaart terug te winnen.

**Syntaxis**

```sql
{%= keys(map) %}
```

**Voorbeeld**

Met de volgende bewerking worden alle toetsen voor de kaart `identityMap` opgehaald.

```sql
{%= keys(identityMap) %}
```

## Waarden{#values}

De functie `values` wordt gebruikt om alle waarden van een bepaalde kaart op te halen.

**Syntaxis**

```sql
{%= values(map) %}
```

**Voorbeeld**

Met de volgende bewerking worden alle waarden voor de kaart `identityMap` opgehaald.

```sql
{%= values(identityMap) %}
```
