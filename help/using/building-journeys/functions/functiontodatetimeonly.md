---
product: journey optimizer
title: toDateTimeOnly
description: Meer informatie over de functie toDateTime
feature: Journeys
role: Engineer
level: Experienced
keywords: toDateTimeOnly, functie, expressie, transport
exl-id: db54c119-5080-403a-b254-43645be6b4a8
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 7%

---

# toDateTimeOnly{#toDateTimeOnly}

Zet een argumentwaarde in een waarde van de datumtijd slechts om.

## Categorie

Conversie

## Functiesyntaxis

`toDateTimeOnly(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd in de notatie ISO-8601 of &quot;JJJ-MM-DD&quot; (XDM-datumnotatie) | string |
| datumtijd | dateTime |

## Handtekeningen en geretourneerde typen

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`
<!--`toDateTimeOnly(<integer>,<integer>,<integer>)`
`toDateTimeOnly(<integer>,<integer>,<integer>,<integer>,<integer>,<integer>)`-->

Retourneer een datetime zonder rekening te houden met tijdzone.

## Voorbeelden

`toDateTimeOnly ("2023-08-18")`

keert dateTime terug die 2023-08-18T00 :00: 00.000 vertegenwoordigt

`toDateTimeOnly(now())`

<!--`toDateTimeOnly(2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000.

`toDateTimeOnly(2016,8,18)`

Returns 2016-08-18T00:00:00.000.-->
