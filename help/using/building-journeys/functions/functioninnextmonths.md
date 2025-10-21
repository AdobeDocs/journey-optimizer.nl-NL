---
product: journey optimizer
title: inNextMonths
description: Meer informatie over de functie in NextMonths
feature: Journeys
role: Developer
level: Experienced
keywords: inNextMonths, function, expression, trip
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# inNextMonths {#inNextMonths}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu + delta maanden bevindt.

## Categorie

Datum

## Functiesyntaxis

`inNextMonths(<dateTime>,<delta>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

## Handtekeningen en type geretourneerd

`inNextMonths(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

## Voorbeelden

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Retourneert true.
