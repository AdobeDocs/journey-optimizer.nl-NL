---
product: journey optimizer
title: countWithNull
description: Meer informatie over de functie countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull, function, expression, trip
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

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
