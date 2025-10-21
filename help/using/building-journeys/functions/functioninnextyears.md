---
product: journey optimizer
title: inNextYears
description: Meer informatie over de functie in NextYear
feature: Journeys
role: Developer
level: Experienced
keywords: inNextYear, function, expression, trip
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# inNextYears {#inNextYears}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu + delta jaar bevindt.

## Categorie

Datum

## Functiesyntaxis

`inNextYears(<dateTime>,<delta>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

## Handtekeningen en type geretourneerd

`inNextYears(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

## Voorbeelden

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Retourneert true.
