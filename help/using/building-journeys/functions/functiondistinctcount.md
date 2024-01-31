---
product: journey optimizer
title: distinctCount
description: Meer informatie over de functie differentCount
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: differentCount, function, expression, trip
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 4%

---

# distinctCount{#distinctCount}

Telt het aantal verschillende waarden waarbij de null-waarden worden genegeerd.

## Categorie

Samenvoeging

## Functiesyntaxis

`distinctCount(<listAny>)`

## Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te verwerken lijst. Voor listObject moet dit een veldverwijzing zijn. |
| keyAttributeName | string | Deze parameter is optioneel en alleen voor listObject. Wanneer de parameter niet wordt opgegeven, wordt een object als gedupliceerd beschouwd wanneer alle kenmerken dezelfde waarden hebben. Anders wordt een object als gedupliceerd beschouwd wanneer het opgegeven kenmerk dezelfde waarde heeft. |

## Handtekening en type geretourneerd

`distinctCount(<listAny>)`

Retourneert een geheel getal.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Retourneert een lijst met objecten.


## Voorbeeld

`distinctCount([10,2,10,null])`

Retourneert 2.

`distinctCount(@event{my_event.productListItems})`

Retourneert het aantal strikt verschillende objecten in de opgegeven array met objecten (type listObject).

`distinctCount(@event{my_event.productListItems}, "SKU")`

Retourneert het aantal objecten met een duidelijke waarde van het kenmerk &quot;SKU&quot;{}.
