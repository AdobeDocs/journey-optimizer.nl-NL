---
product: journey optimizer
title: inLastDays
description: Meer informatie over de functie in LastDays
feature: Journeys
role: Developer
level: Experienced
keywords: inLastDays, function, expression, trip
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 10%

---

# inLastDays {#inLastDays}

Geeft als resultaat waar als een bepaalde dateTime tussen nu en nu is - delta dagen.

## Categorie

Datum

## Functiesyntaxis

`inLastDays(<dateTime>,<delta>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

## Handtekeningen en type geretourneerd

`inLastDays(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

## Voorbeelden

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retourneert true.
