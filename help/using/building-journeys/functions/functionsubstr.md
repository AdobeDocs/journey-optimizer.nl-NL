---
product: journey optimizer
title: substr
description: Meer informatie over de substr van de functie
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: substr, function, expression, trip
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# substr {#substr}

Retourneert de subtekenreeks van de tekenreeksexpressie tussen de beginindex en de eindindex. Als de eindindex niet is gedefinieerd, ligt deze tussen de beginindex en het einde.

## Categorie

String

## Functiesyntaxis

`substr(<parameters>)`

## Parameters

| Parameter | type |
|-------------|----------|
| string | string |
| beginIndex | integer |
| endIndex | integer |

## Handtekening en type geretourneerd

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Retourneer een tekenreeks.

## Voorbeeld

`substr("Hello World",6)`

Retourneert &quot;World&quot;.

`substr("Hello World", 0, 5)`

Retourneert &quot;Hello&quot;.
