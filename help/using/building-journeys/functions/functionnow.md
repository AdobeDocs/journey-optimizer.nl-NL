---
product: journey optimizer
title: now
description: Meer informatie over de functie
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 14%

---

# now {#now}

Retourneert de huidige datum in de datumtijdnotatie. Raadpleeg voor meer informatie over gegevenstypen [deze pagina](../expression/data-types.md).

## Categorie

Datum

## Functiesyntaxis

`now(<parameter>)`

## Parameters

| Parameter | Beschrijving |
|--- |--- |
| string |  |

## Handtekeningen en type geretourneerd

`now()`

`now("<timeZone id>")`

Retourneert een dateTime.

## Voorbeelden

`now()`

Retourneert 2019-06-03T06:30Z.

`toString(now())`

Retourneert &quot;2019-06-03T06:30Z&quot;

`now("Europe/Paris")`

Retourneert 2019-06-03T08:30+02:00.
