---
product: journey optimizer
title: distinctCountWithNull
description: Meer informatie over de functie differentCountWithNull
feature: Journeys
role: Developer
level: Experienced
keywords: differentCountWithNull, function, expression, trip
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
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
