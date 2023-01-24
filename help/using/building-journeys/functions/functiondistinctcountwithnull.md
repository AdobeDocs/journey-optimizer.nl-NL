---
product: journey optimizer
title: distinctCountWithNull
description: Meer informatie over de functie differentCountWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: differentCountWithNull, function, expression, trip
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 21%

---

# distinctCountWithNull {#distinctCountWithNull}

Telt het aantal verschillende waarden inclusief de null-waarden.

>[!NOTE]
>
>Als de doellijst een listObject is, kan deze functie alleen worden gebruikt in aangepaste actiedragers.

## Categorie

Samenvoeging

## Functiesyntaxis

`distinctCountWithNull(<listAny>)`

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

`distinctCountWithNull(<listAny>)`

Retourneert een geheel getal.

## Voorbeeld

`distinctCountWithNull([10,2,10,null])`

Retourneert 3.
