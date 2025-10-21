---
product: journey optimizer
title: now
description: Meer informatie over de functie
feature: Journeys
role: Developer
level: Experienced
keywords: nu, functie, expressie, reis
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 8%

---

# now {#now}

Retourneert de huidige datum in de datumtijdnotatie. Voor meer informatie over gegevenstypes, verwijs naar [&#x200B; deze pagina &#x200B;](../expression/data-types.md).

## Categorie

Datum

## Functiesyntaxis

`now(<parameter>)`

## Parameters

| Parameter | Beschrijving |
|--- |--- |
| string | Identificatiecode tijdzone (optioneel) |

## Handtekeningen en type geretourneerd

`now()`

`now("<timeZone id>")`

Retourneert een dateTime.

## Voorbeelden

`now()`

Keert 2023-06-03T06 :30Z terug.

`toString(now())`

Retourneert &quot;2023-06-03T06 :30Z&quot;

`now("Europe/Paris")`

Keert 2023-06-03T08 :30+02 :00 terug.
