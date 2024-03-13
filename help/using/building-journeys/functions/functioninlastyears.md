---
product: journey optimizer
title: inLastYears
description: Meer informatie over de functie in LastYear
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastYear, function, expression, trip
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 12%

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
