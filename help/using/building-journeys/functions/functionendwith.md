---
product: journey optimizer
title: endWith
description: Meer informatie over de functie endWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWith, function, expression, trip
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 8%

---

# endWith {#endWith}

Retourneert true als de tweede parameter een achtervoegsel van de eerste parameter is.

## Categorie

String

## Functiesyntaxis

`endWith(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| string | string |
| achtervoegsel | string |

## Handtekening en type geretourneerd

`endWith(<string>,<string>)`

Retourneert een Booleaanse waarde.

## Voorbeeld

`endWith("Hello World", "World")`

Retourneert true.

`endWith("Hello World", "Hello")`

Retourneert false.
