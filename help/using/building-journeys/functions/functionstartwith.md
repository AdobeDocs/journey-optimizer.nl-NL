---
product: journey optimizer
title: startWith
description: Meer informatie over de functie startWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWith, function, expression, trip
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 8%

---

# startWith {#startWith}

Retourneert true als de tweede parameter een voorvoegsel van de eerste is.

## Categorie

String

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
