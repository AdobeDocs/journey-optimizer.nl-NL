---
product: journey optimizer
title: distinctWithNull
description: Meer informatie over de functie clearWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: differentWithNull, function, expression, trip
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 4%

---

# distinctWithNull {#distinctWithNull}

Geeft als resultaat de verschillende waarden of objecten van een bepaalde lijst. Als de lijst ten minste één null-item heeft, wordt een null-waarde weergegeven in de geretourneerde lijst.

## Categorie

Lijst

## Functiesyntaxis

`distinctWithNull(<parameters>)`

## Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te verwerken lijst. Voor listObject moet dit een veldverwijzing zijn. |
| keyAttributeName | string | Deze parameter is optioneel en alleen voor listObject. Wanneer de parameter niet wordt opgegeven, wordt een object als gedupliceerd beschouwd wanneer alle kenmerken dezelfde waarden hebben. Anders wordt een object als gedupliceerd beschouwd wanneer het opgegeven kenmerk dezelfde waarde heeft. |

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

`distinctWithNull(<listObject>)`

`distinctWithNull(<listObject>,<string>)`

Retourneert een lijst met objecten.

## Voorbeelden

`distinctWithNull([10,2,10,null])`

Retourneert [10, 2, null]
