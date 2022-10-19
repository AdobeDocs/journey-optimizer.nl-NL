---
product: journey optimizer
title: inNextHours
description: Meer informatie over de functie in NextHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 15%

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

`inNextHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

Retourneert true.
