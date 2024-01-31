---
product: journey optimizer
title: countOnlyNull
description: Meer informatie over de functie countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull, function, expression, trip
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

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
