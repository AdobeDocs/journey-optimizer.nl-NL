---
product: journey optimizer
title: toBool
description: Meer informatie over de functie toBool
feature: Journeys
role: Engineer
level: Experienced
keywords: tobool, function, expression, trip
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# toBool {#toBool}

Zet een argumentwaarde in een booleaanse waarde om, afhankelijk van het type.

* Van tekenreeks: probeer de tekenreekswaarde om te zetten als een booleaanse waarde, van &quot;true&quot; als de tekenreekswaarde &quot;true&quot; is, anders false
* Uit numeriek: true wanneer de numerieke waarde niet gelijk is aan 0, anders false

## Categorie

Conversie

## Functiesyntaxis

`toBool(<parameter>)`

## Parameters

* decimaal
* boolean
* string
* integer

## Handtekeningen en geretourneerde typen

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Retourneer een booleaanse waarde.

## Voorbeelden

`toBool("true")`

`toBool(1)`

Retourneert true.

`toBool("this is not a boolean")`

Retourneert false.
