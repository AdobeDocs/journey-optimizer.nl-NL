---
product: journey optimizer
title: setDays
description: Meer informatie over de functie setDays
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 9%

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

`setDays(toDateTime('2010-12-12T01:11:00Z'), 25)`

Retourneert 2010-12-25T01:11:00Z.

`setDays(toDateTimeOnly(@{MyEvent.registrationDate}), 1)`
