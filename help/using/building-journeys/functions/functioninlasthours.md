---
product: journey optimizer
title: inLastHours
description: Meer informatie over de functie inLastHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastHours, function, expression, trip
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 12%

---

# inLastHours {#inLastHours}

Retourneert true als de opgegeven datumtijd tussen nu en nu ligt - delta-uren.

## Categorie

Datum

## Functiesyntaxis

`inLastHours(<dateTime>,<delta>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

## Handtekeningen en type geretourneerd

`inLastHours(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

## Voorbeelden

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

Retourneert true.

`inLastHours(@event{MyEvent.timestamp}, 4)`

Retourneert true.
