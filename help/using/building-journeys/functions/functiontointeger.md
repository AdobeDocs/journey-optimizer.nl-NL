---
product: journey optimizer
title: toInteger
description: Meer informatie over de functie toInteger
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toInteger, function, expression, trip
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 9%

---

# toInteger {#toInteger}

Zet een argumentwaarde in een geheel getal om.

## Categorie

Conversie

## Functiesyntaxis

`toInteger(<parameter>)`

## Parameters

| Parameter | Beschrijving |
|--- |--- |
| string | converteert de tekenreekswaarde als een geheel getal |
| dateTime | zet de datum om als aantal milliseconden (epoch milliseconds) |
| decimaal | converteert naar geheel getal door het decimale gedeelte te verwijderen (voorbeeld: 1,5 wordt 1) |
| boolean | Zet de booleaanse waarde om als 1 indien true, 0 indien false |

## Handtekeningen en type geretourneerd

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Retourneer een geheel getal.

## Voorbeelden

`toInteger("4")`

Retourneert 4.
