---
product: journey optimizer
title: inLastMonths
description: Meer informatie over de functie in LastMonths
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastMonths, function, expression, trip
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# inLastMonths {#inLastMonths}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu bevindt - delta-maanden.

## Categorie

Datum

## Functiesyntaxis

`inLastMonths(<dateTime>,<delta>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

## Handtekeningen en type geretourneerd

`inLastMonths(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

## Voorbeelden

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retourneert true.
