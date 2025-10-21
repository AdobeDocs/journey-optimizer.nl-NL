---
product: journey optimizer
title: setDays
description: Meer informatie over de functie setDays
feature: Journeys
role: Developer
level: Experienced
keywords: setDays, function, expression, trip
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 6%

---

# setDays {#setDays}

Hiermee stelt u alleen de dag van een datumtijd of datumtijd in. Als u bijvoorbeeld wilt wachten tot een bepaalde dag van de maand, kunt u de dag forceren.

## Categorie

Datum

## Functiesyntaxis

`setDays(<parameter>)`

## Parameters

| Parameter | Type |
|--- |--- |
| datumtijd | dateTime |
| datumtijd zonder tijdzone te overwegen | dateTimeOnly |
| dagen | integer |

## Handtekeningen en type geretourneerd

`setDays(<dateTime>,<days>)`

Retourneert een datetime.

`setDays(<dateTimeOnly>,<days>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

## Voorbeelden

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Keert 2023-12-25T01 :11: 00Z terug.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`
