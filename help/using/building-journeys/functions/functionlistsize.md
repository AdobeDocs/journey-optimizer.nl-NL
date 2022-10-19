---
product: journey optimizer
title: listSize
description: Meer informatie over de functie listSize
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 31%

---

# listSize {#listSize}

Telt het aantal elementen in de lijst.

## Categorie

Lijst

## Functiesyntaxis

`listSize(<parameters>)`

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

## Handtekeningen en type geretourneerd

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

`listSize(<listPoint>)`

Retourneer een geheel getal.

## Voorbeeld

`listSize([10,2,3])`

Retourneert 3.
