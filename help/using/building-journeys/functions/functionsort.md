---
product: journey optimizer
title: sort
description: Meer informatie over de functie sorteren
feature: Journeys
role: Developer
level: Experienced
keywords: sort, function, expression, trip
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---

# sort {#sort}

Hiermee sorteert u een lijst met waarden of objecten in natuurlijke volgorde.

## Categorie

Lijst

## Functiesyntaxis

`sort(<parameters>)`

## Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te sorteren lijst. Voor listObject moet dit een veldverwijzing zijn. |
| keyAttributeName | string | Deze parameter is alleen voor listObject. De kenmerknaam in de objecten in de lijst wordt gebruikt als sleutel voor sorteren. |
| sortingOrder | boolean | Oplopend (true) of aflopend (false) |

## Handtekening en type geretourneerd

`sort(<listInteger>,<boolean>)`

Retourneert een lijst met gehele getallen.

`sort(<listDecimal>,<boolean>)`

Retourneert een lijst met decimalen.

`sort(<listString>,<boolean>)`

Retourneert een lijst met tekenreeksen.

`sort(<listDateTimeOnly>,<boolean>)`

Keert een lijst van datetimes zonder tijdzone terug te overwegen.

`sort(<listDateTime>,<boolean>)`

Retourneert een lijst met datetimes.

`sort(<listDateOnly>,<boolean>)`

Retourneert een lijst met datums.

`sort(<listBoolean>,<boolean>)`

Retourneert een lijst met laarzen.

`sort(<listObject>,<string>,<boolean>)`

Retourneert een lijst met objecten.

## Voorbeeld

`sort(["A", "C", "B"], true)`

Retourneert `["A","B","C"]` .

`sort([1, 3, 2], false)`

Retourneert `[3, 2, 1]` .

`sort(@event{my_event.productListItems}, "SKU", true)`

Retourneert het listObject dat is geordend door het SKU-kenmerk (oplopende volgorde)

