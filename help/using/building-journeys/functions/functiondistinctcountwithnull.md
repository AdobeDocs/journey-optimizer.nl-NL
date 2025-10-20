---
product: journey optimizer
title: distinctCountWithNull
description: Meer informatie over de functie differentCountWithNull
feature: Journeys
role: Engineer
level: Experienced
keywords: differentCountWithNull, function, expression, trip
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# distinctCountWithNull {#distinctCountWithNull}

Telt het aantal verschillende waarden inclusief de null-waarden.

De parameter `<listObject>` wordt niet ondersteund in deze functie.

## Categorie

Samenvoeging

## Functiesyntaxis

`distinctCountWithNull(<listAny>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Handtekening en type geretourneerd

`distinctCountWithNull(<listAny>)`

Retourneert een geheel getal.

## Voorbeeld

`distinctCountWithNull([10,2,10,null])`

Retourneert 3.
