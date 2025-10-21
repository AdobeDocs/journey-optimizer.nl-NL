---
product: journey optimizer
title: countWithNull
description: Meer informatie over de functie countWithNull
feature: Journeys
role: Developer
level: Experienced
keywords: countWithNull, function, expression, trip
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# countWithNull {#countWithNull}

Telt alle elementen van de lijst met inbegrip van ongeldige waarden.

De parameter `<listObject>` wordt niet ondersteund in deze functie.

## Categorie

Samenvoeging

## Functiesyntaxis

`countWithNull(<listAny>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Handtekening en type geretourneerd

`countWithNull(<listAny>)`

Retourneert een geheel getal.

## Voorbeeld

`countWithNull([10,2,10,null])`

Retourneert 4.
