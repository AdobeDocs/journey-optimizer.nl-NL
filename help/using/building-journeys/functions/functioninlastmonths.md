---
product: journey optimizer
title: inLastMonths
description: Meer informatie over de functie in LastMonths
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastMonths, function, expression, trip
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 14%

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

`inLastMonths(toDateTime('2010-12-12T01:11:00Z'), 4)`

Retourneert true.
