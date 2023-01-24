---
product: journey optimizer
title: distinctCount
description: Meer informatie over de functie differentCount
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: differentCount, function, expression, trip
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 28%

---

# distinctCount{#distinctCount}

Telt het aantal verschillende waarden waarbij de null-waarden worden genegeerd.

## Categorie

Samenvoeging

## Functiesyntaxis

`distinctCount(<listAny>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| Lijst | listString |
| Lijst | listBoolean |
| Lijst | listInteger |
| Lijst | listDecimal |
| Lijst | listDuration |
| Lijst | listDateTime |
| Lijst | listDateTimeOnly |
| Lijst | listDateOnly |

## Handtekening en type geretourneerd

`distinctCount(<listAny>)`

Retourneert een geheel getal.

## Voorbeeld

`distinctCount([10,2,10,null])`

Retourneert 2.
