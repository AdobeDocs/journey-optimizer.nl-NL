---
product: journey optimizer
title: serializeList
description: Meer informatie over de functie serializeList
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: serializeList, function, expression, trip
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 18%

---

# serializeList {#serializeList}

Hiermee wordt de lijst (elk type) in de eerste parameter omgezet in een tekenreeks. De tweede parameter vertegenwoordigt het te gebruiken scheidingsteken. De derde parameter is een booleaanse waarde die aangeeft of elk element van de expressie aanhalingstekens moet bevatten.

## Categorie

Lijst

## Functiesyntaxis

`serializeList(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| Tekenreeks | Tekenreeks |
| Boolean | Boolean |
| DateTimeOnly | DateTimeOnly |
| Lijst | listString |
| Lijst | listBoolean |
| Lijst | listPoint |
| Lijst | listDecimal |
| Lijst | listDuration |
| Lijst | listDateTime |
| Lijst | listDateTimeOnly |
| Lijst | listDateOnly |

## Handtekening en type geretourneerd

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

`serializeList(<listPoint>,<string>,<boolean>)`

Retourneer een tekenreeks.

## Voorbeeld

`serializeList(["Hello","World"], " ", false)`

Retourneert &quot;Hello World&quot;.

`serializeList(["Hello", "World"], ",", true)`

Retourneert &quot;&quot;Hello&quot;,&quot;World&quot;&quot;.
