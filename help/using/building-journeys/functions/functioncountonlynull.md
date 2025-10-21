---
product: journey optimizer
title: countOnlyNull
description: Meer informatie over de functie countOnlyNull
feature: Journeys
role: Developer
level: Experienced
keywords: countOnlyNull, function, expression, trip
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 7%

---

# countOnlyNull {#countOnlyNull}

Telt het aantal null-waarden in de lijst.

De parameter `<listObject>` wordt niet ondersteund in deze functie.

## Categorie

Samenvoeging

## Functiesyntaxis

`countOnlyNull(<listAny>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Handtekening en type geretourneerd

`countOnlyNull(<listAny>)`

Retourneert een geheel getal.

## Voorbeeld

`countOnlyNull([10,2,10,null])`

Retourneert 1.
