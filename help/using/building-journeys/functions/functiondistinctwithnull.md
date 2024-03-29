---
product: journey optimizer
title: distinctWithNull
description: Meer informatie over de functie clearWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: differentWithNull, function, expression, trip
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# distinctWithNull {#distinctWithNull}

Geeft als resultaat de verschillende waarden of objecten van een bepaalde lijst. Als de lijst ten minste één null-item heeft, wordt een null-waarde weergegeven in de geretourneerde lijst.

De parameter `<listObject>` wordt niet ondersteund in deze functie.

## Categorie

Lijst

## Functiesyntaxis

`distinctWithNull(<parameters>)`

## Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Te verwerken lijst. |

## Handtekeningen en geretourneerde typen

`distinctWithNull(<listInteger>)`

Retourneert een lijst met gehele getallen.

`distinctWithNull(<listDecimal>)`

Retourneert een lijst met decimalen.

`distinctWithNull(<listString>)`

Retourneert een lijst met tekenreeksen.

`distinctWithNull(<listDateTimeOnly>)`

Keert een lijst van datetimes zonder tijdzone terug te overwegen.

`distinctWithNull(<listDateTime>)`

Retourneert een lijst met datetimes.

`distinctWithNull(<listDateOnly>)`

Retourneert een lijst met datums.

`distinctWithNull(<listBoolean>)`

Retourneert een lijst met laarzen.

`distinctWithNull(<listDuration>)`

Retourneert een lijst met tijdsduur.

## Voorbeelden

`distinctWithNull([10,2,10,null])`

Retourneert [10, 2, null]
