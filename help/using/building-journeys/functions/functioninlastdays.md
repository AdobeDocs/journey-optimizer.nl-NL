---
product: journey optimizer
title: inLastDays
description: Meer informatie over de functie in LastDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays, function, expression, trip
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 12%

---

# inLastDays {#inLastDays}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu bevindt - delta dagen.

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
