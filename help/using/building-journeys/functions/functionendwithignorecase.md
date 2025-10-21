---
product: journey optimizer
title: endWithIgnoreCase
description: Meer informatie over de functie endWithIgnoreCase
feature: Journeys
role: Developer
level: Experienced
keywords: endWithIgnoreCase, function, expression, trip
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 3%

---

# endWithIgnoreCase {#endWithIgnoreCase}

Controleert of de tekenreeks van het eerste argument eindigt met een specifieke tekenreeks (tekenreeks van het tweede argument), waarbij geen rekening wordt gehouden met het geval.

## Categorie

String

## Functiesyntaxis

`endWithIgnoreCase(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| string | string |
| achtervoegsel | string |

## Handtekening en type geretourneerd

`endWithIgnoreCase(<string>,<string>)`

Retourneert een Booleaanse waarde.

## Voorbeeld

`endWithIgnoreCase("rowing is great", "AT")`

Retourneert true.
