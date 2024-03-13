---
product: journey optimizer
title: inNextMonths
description: Meer informatie over de functie in NextMonths
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextMonths, function, expression, trip
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 12%

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
