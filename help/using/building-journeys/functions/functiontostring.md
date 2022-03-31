---
product: adobe campaign
title: toString
description: Meer informatie over de functie toString
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 6%

---

# toString {#toString}

Zet een argumentwaarde in een koordwaarde om, afhankelijk van zijn type. Raadpleeg voor meer informatie over gegevenstypen [deze pagina](../expression/data-types.md).

## Categorie

Conversie

## Functiesyntaxis

`toString(<parameter>)`

## Parameters

| Parameter | Beschrijving |
|--- |--- |
| dateTime | converteert de datum in UTC-datumnotatie |
| dateTimeOnly | converteert de datum in UTC-datumnotatie |
| duur | converteren naar het overeenkomstige aantal milliseconden als een tekenreeks |
| integer | converteert naar tekenreeksrepresentatie van de waarde (1 wordt &quot;1&quot;) |
| decimaal | converteert naar tekenreeksrepresentatie van de waarde (1,5 wordt &quot;1,5&quot;) |
| boolean | Zet de booleaanse waarde om als &#39;true&#39; (waar), &#39;false&#39; (onwaar) |

## Handtekeningen en type geretourneerd

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Retourneer een tekenreeks.

## Voorbeeld

`toString(4)`

Retourneert &quot;4&quot;.