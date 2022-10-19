---
product: journey optimizer
title: endWith
description: Meer informatie over de functie endWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 16%

---

# endWith {#endWith}

Retourneert true als de tweede parameter een achtervoegsel van de eerste parameter is.

## Categorie

Tekenreeks

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
