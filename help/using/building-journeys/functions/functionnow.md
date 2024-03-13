---
product: journey optimizer
title: now
description: Meer informatie over de functie
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: nu, functie, expressie, reis
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 9%

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

Retourneert 2023-06-03T06:30Z.

`toString(now())`

Retourneert &quot;2023-06-03T06:30Z&quot;

`now("Europe/Paris")`

Retourneert 2023-06-03T08:30+02:00.
