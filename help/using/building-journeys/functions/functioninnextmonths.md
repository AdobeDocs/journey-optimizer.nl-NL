---
product: journey optimizer
title: inNextMonths
description: Meer informatie over de functie in NextMonths
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 15%

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

`inNextMonths(toDateTime('2020-01-12T01:11:00Z'), 4)`

Retourneert true.
