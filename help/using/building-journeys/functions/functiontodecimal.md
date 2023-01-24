---
product: journey optimizer
title: toDecimal
description: Meer informatie over de functie toDecimal
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: decimaal, functie, expressie, transport
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 9%

---

# toDecimal {#toDecimal}

Zet een argumentwaarde in een decimale waarde om, afhankelijk van het type.

## Categorie

Conversie

## Functiesyntaxis

`toDecimal(<parameter>)`

## Parameters

| Parameter | Beschrijving |
|--- |--- |
| string | converteert de tekenreekswaarde als een decimaal |
| dateTime | zet de datum om als aantal milliseconden (epoch milliseconds) |
| boolean | Zet de booleaanse waarde om als 1 indien true, 0 indien false |
| integer | wordt omgezet in decimaal (voorbeeld.: 1 wordt 1,0) |

## Handtekeningen en geretourneerde typen

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Retourneer een decimaal.

## Voorbeelden

`toDecimal("4.0")`

Retourneert 4.0.
