---
product: journey optimizer
title: setHours
description: Meer informatie over de functie setHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setHours, function, expression, trip
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 4%

---

# setHours {#setHours}

Hiermee stelt u alleen de uren van een datumtijd of datumtijd in. Als u bijvoorbeeld tot een bepaald uur wilt wachten, kunt u het uur forceren.

## Categorie

Datum

## Functiesyntaxis

`setHours(<parameter>)`

## Parameters

| Parameter | Type |
|--- |--- |
| datumtijd | dateTime |
| datumtijd zonder tijdzone te overwegen | dateTimeOnly |
| uren | integer |

## Handtekeningen en type geretourneerd

`setHours(<dateTime>,<hours>)`

Retourneert een datetime.

`setHours(<dateTimeOnly>,<hours>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

## Voorbeelden

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Keert 2023-12-12T04 :11: 00Z terug.

`setHours(nowWithDelta(1, "days"), 20)`

Keert morgen bij 8 :XY PM terug, XY die de notulen op het ogenblik van de huidige tijdevaluatie zijn. Als de evaluatie bij 2 :45 AM gebeurt, zal de teruggekeerde tijd 8 :45 PM zijn.
