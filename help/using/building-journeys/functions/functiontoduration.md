---
product: journey optimizer
title: toDuration
description: Meer informatie over de functie toDuration
feature: Journeys
role: Developer
level: Experienced
keywords: toDuration, function, expression, trip
exl-id: c78e30c5-99ee-4dc7-a03a-17f7ee65f83a
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---

# toDuration {#toDuration}

Zet een argumentwaarde in een duur om. Voor meer informatie over gegevenstypes, verwijs naar [&#x200B; deze pagina &#x200B;](../expression/data-types.md).

## Categorie

Conversie

## Functiesyntaxis

`toDuration(<parameter>)`

## Parameters

| Parameter | Beschrijving |
|--- |--- |
| string | formaten die gebaseerd zijn op de ISO-8601-duurnotatie PnDTnHnMn.nS met dagen waarvan wordt aangenomen dat ze precies 24 uur zijn |
| integer | aantal milliseconden |

Als tekenreeksexpressie: geaccepteerde notaties zijn gebaseerd op de ISO-8601-duurnotatie PnDTnHnMn.nS met dagen die worden beschouwd als precies 24 uur.

De tekenreeks begint met een optioneel teken, aangeduid met het negatieve of positieve ASCII-symbool. Indien negatief, wordt de hele periode genegeerd. De ASCII-letter &quot;P&quot; staat vervolgens in hoofdletters of kleine letters. Er zijn dan vier secties, elk bestaande uit een getal en een achtervoegsel. De secties hebben achtervoegsels in ASCII van &quot;D&quot;, &quot;H&quot;, &quot;M&quot; en &quot;S&quot; gedurende dagen, uren, minuten en seconden, die in hoofdletters of in kleine letters worden geaccepteerd. De achtervoegsels moeten op volgorde voorkomen. De ASCII-letter &quot;T&quot; moet vóór het eerste exemplaar van een uur-, minuut- of tweede sectie plaatsvinden, indien aanwezig. Ten minste één van de vier delen moet aanwezig zijn en indien &quot;T&quot; aanwezig is, moet er ten minste één deel na &quot;T&quot; aanwezig zijn. Het nummerdeel van elke sectie moet uit een of meer ASCII-cijfers bestaan. Het getal kan worden voorafgegaan door het negatieve of positieve ASCII-symbool. Het aantal dagen, uren en minuten moet worden geparseerd. Het aantal seconden moet samen met de optionele breuk parseren. Het decimale punt kan een punt of een komma zijn. Het fractionele deel kan van nul tot 9 cijfers hebben.

## Handtekeningen en type geretourneerd

`toDuration(<string>)`

`toDuration(<integer>)`

Retourneert een duur.

## Voorbeelden

`toDuration("PT10H")`

Geeft een duur van 10 uur.

`toDuration("PT4S")`

Retourneert de duur van 4s.

`toDuration(4000)`

Retourneert de duur van 4s.
