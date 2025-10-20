---
product: journey optimizer
title: inLastYears
description: Meer informatie over de functie in LastYear
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastYear, function, expression, trip
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# inLastYears {#inLastYears}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu bevindt - delta-jaren.

## Categorie

Datum

## Functiesyntaxis

`inLastYears(<dateTime>,<delta>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

## Handtekeningen en type geretourneerd

`inLastYears(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

## Voorbeelden

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retourneert true.
