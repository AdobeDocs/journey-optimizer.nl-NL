---
product: adobe campaign
title: avg
description: Meer informatie over de functie avg
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 12%

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

`avg(@{BarBeacon.inventory},5)`

`avg([10,3,8])`

Retourneert 7.0.

`avg(10.2, 3)`

Retourneert 6.6.