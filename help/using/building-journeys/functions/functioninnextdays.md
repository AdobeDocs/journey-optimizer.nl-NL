---
product: journey optimizer
title: inNextDays
description: Meer informatie over de functie in NextDays
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextDays, function, expression, trip
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# inNextDays {#inNextDays}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu + delta dagen bevindt.

## Categorie

Datum

## Functiesyntaxis

`inNextDays(<dateTime>,<delta>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

## Handtekeningen en type geretourneerd

`inNextDays(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

## Voorbeelden

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retourneert true.
