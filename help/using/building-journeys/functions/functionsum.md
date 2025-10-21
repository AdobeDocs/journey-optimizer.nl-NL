---
product: journey optimizer
title: sum
description: Meer informatie over de functiesom
feature: Journeys
role: Developer
level: Experienced
keywords: som, functie, expressie, reis
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# sum {#sum}

Retourneert de som van de waarden van een set expressies. Null-waarden worden genegeerd.

## Categorie

Samenvoeging

## Functiesyntaxis

`sum(<parameters>)`

## Parameters

* listInteger
* listDecimal
* duur
* integer
* decimaal

## Handtekeningen en geretourneerde typen

`sum(<listDecimal>)`

Retourneert een decimaal.

`sum(<listInteger>)`

Retourneert een geheel getal.

`sum(<integer>,<integer>)`

Retourneert een geheel getal.

`sum(<decimal>,<decimal>)`

Retourneert een decimaal.

## Voorbeelden

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Retourneert 21.

`sum([10.5,null,8.1])`

Retourneert 18.6.
