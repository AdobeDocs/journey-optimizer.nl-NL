---
product: journey optimizer
title: endWithIgnoreCase
description: Meer informatie over de functie endWithIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWithIgnoreCase, function, expression, trip
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 9%

---

# endWithIgnoreCase {#endWithIgnoreCase}

Controleert of de tekenreeks van het eerste argument eindigt met een specifieke tekenreeks (tekenreeks van het tweede argument), waarbij geen rekening wordt gehouden met het geval.

## Categorie

Tekenreeks

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
