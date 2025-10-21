---
product: journey optimizer
title: serializeList
description: Meer informatie over de functie serializeList
feature: Journeys
role: Developer
level: Experienced
keywords: serializeList, function, expression, trip
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 5%

---

# serializeList {#serializeList}

Hiermee wordt een bepaalde lijst (elk type behalve listObject) omgezet in een tekenreeks.

## Categorie

Lijst

## Functiesyntaxis

`serializeList(<parameters>)`

## Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Lijst die moet worden omgezet in een tekenreeks. |
| scheidingsteken | string | Scheidingsteken tussen elk lijstelement in de uitvoertekenreeks. |
| addQuotes | boolean | Deze parameter geeft aan of elk element in de uitvoertekenreeks aanhalingstekens moet bevatten (true) of niet (false). |

## Handtekening en type geretourneerd

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Retourneer een tekenreeks.

## Voorbeeld

`serializeList(["Hello","World"], " ", false)`

Retourneert &quot;Hello World&quot;.

`serializeList(["Hello", "World"], ",", true)`

Retourneert &quot;&quot;Hello&quot;,&quot;World&quot;&quot;.
