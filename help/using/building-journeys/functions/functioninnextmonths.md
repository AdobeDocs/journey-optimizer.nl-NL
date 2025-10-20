---
product: journey optimizer
title: inNextMonths
description: Meer informatie over de functie in NextMonths
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextMonths, function, expression, trip
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
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
