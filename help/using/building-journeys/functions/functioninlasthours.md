---
product: journey optimizer
title: inLastHours
description: Meer informatie over de functie inLastHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 15%

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

`inLastHours(@{MyEvent.timestamp}, 4)`

Retourneert true.
