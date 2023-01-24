---
product: journey optimizer
title: toBool
description: Meer informatie over de functie toBool
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: tobool, function, expression, trip
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 7%

---

# toBool {#toBool}

Zet een argumentwaarde in een booleaanse waarde om, afhankelijk van het type.

* Van tekenreeks: probeer de tekenreekswaarde om te zetten als een booleaanse waarde, van &quot;true&quot; als de tekenreekswaarde &quot;true&quot; is, anders false
* Uit numeriek: true als de numerieke waarde niet gelijk is aan 0, false in andere gevallen

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
