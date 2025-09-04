---
product: journey optimizer
title: avg
description: Meer informatie over de functie avg
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: avg, function, expression, trip
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---

# avg {#avg}

Geeft als resultaat de gemiddelde waarde tussen een reeks expressies, opgegeven als een lijst of twee expressies. Null-waarden worden genegeerd.


## Categorie

Samenvoeging

## Functiesyntaxis

`avg(<parameter>)`

## Parameters

Ondersteunde typen:

* listInteger
* listDecimal
* decimaal
* integer

## Handtekeningen en type geretourneerd

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Retourneert een decimaal.

## Voorbeelden

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Retourneert 7.0.

`avg(10.2, 3)`

Retourneert 6.6.
