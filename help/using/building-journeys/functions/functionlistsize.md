---
product: journey optimizer
title: listSize
description: Meer informatie over de functie listSize
feature: Journeys
role: Engineer
level: Experienced
keywords: listSize, function, expression, trip
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# listSize {#listSize}

Telt het aantal elementen in de lijst.

## Categorie

Lijst

## Functiesyntaxis

`listSize(<parameters>)`

## Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te verwerken lijst. Voor listObject moet dit een veldverwijzing zijn. Een listObject kan geen null-object bevatten. |

## Handtekeningen en type geretourneerd

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Retourneer een geheel getal.

`listSize(<listObject>)`

## Voorbeeld

`listSize([10,2,3])`

Retourneert 3.

`listSize(@event{my_event.productListItems})`

Retourneert het aantal objecten in de opgegeven array met objecten (type listObject).
