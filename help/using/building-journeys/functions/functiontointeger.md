---
product: journey optimizer
title: toInteger
description: Meer informatie over de functie toInteger
feature: Journeys
role: Developer
level: Experienced
keywords: toInteger, function, expression, trip
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

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
| decimaal | converteert naar geheel getal door het decimale gedeelte te verwijderen (1,5 wordt bijvoorbeeld 1). |
| boolean | Zet de booleaanse waarde om als 1 indien waar (true), 0 indien onwaar (false) |

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
