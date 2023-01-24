---
product: journey optimizer
title: startWith
description: Meer informatie over de functie startWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWith, function, expression, trip
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 14%

---

# startWith {#startWith}

Retourneert true als de tweede parameter een voorvoegsel van de eerste is.

## Categorie

Tekenreeks

## Functiesyntaxis

`startWith(<parameters>)`

## Parameters

| Parameter | Type |
|-------------|--------|
| string | string |
| prefix | string |

## Handtekening en type geretourneerd

`startWith(<string>,<string>)`

Retourneer een booleaanse waarde.

## Voorbeeld

`startWith("Hello World", "Hello")`

Retourneert true.

`startWith("Hello World", "World")`

Retourneert false.
