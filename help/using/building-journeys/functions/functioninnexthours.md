---
product: journey optimizer
title: inNextHours
description: Meer informatie over de functie in NextHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextHours, function, expression, trip
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# inNextHours {#inNextHours}

Retourneert true als een bepaalde datum of dateTime zich tussen nu en nu + delta-uren bevindt.

## Categorie

Datum

## Functiesyntaxis

`inNextHours(<dateTime>,<delta>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd | dateTime |
| delta | integer |

## Handtekeningen en type geretourneerd

`inNextHours(<dateTime>,<integer>)`

Retourneert een Booleaanse waarde.

## Voorbeelden

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retourneert true.
