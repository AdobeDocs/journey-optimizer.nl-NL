---
product: journey optimizer
title: distinct
description: Meer informatie over de functie afzonderlijk
feature: Journeys
role: Developer
level: Experienced
keywords: verschillend, functie, uitdrukking, reis
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---

# distinct {#distinct}

Geeft als resultaat de verschillende waarden of objecten van een bepaalde lijst. Null-items worden genegeerd.

## Categorie

Lijst

## Functiesyntaxis

`distinct(<parameters>)`

## Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te verwerken lijst. Voor listObject moet dit een veldverwijzing zijn. |
| keyAttributeName | string | Deze parameter is optioneel en alleen voor listObject. Wanneer de parameter niet wordt opgegeven, wordt een object als gedupliceerd beschouwd wanneer alle kenmerken dezelfde waarden hebben. Anders wordt een object als gedupliceerd beschouwd wanneer het opgegeven kenmerk dezelfde waarde heeft. |

## Handtekeningen en geretourneerde typen

`distinct(<listInteger>)`

Retourneert een lijst met gehele getallen.

`distinct(<listDecimal>)`

Retourneert een lijst met decimalen.

`distinct(<listString>)`

Retourneert een lijst met tekenreeksen.

`distinct(<listDateTimeOnly>)`

Keert een lijst van datetimes zonder tijdzone terug te overwegen.

`distinct(<listDateTime>)`

Retourneert een lijst met datetimes.

`distinct(<listDateOnly>)`

Retourneert een lijst met datums.

`distinct(<listBoolean>)`

Retourneert een lijst met laarzen.

`distinct(<listDuration>)`

Retourneert een lijst met tijdsduur.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Retourneert een lijst met objecten.


## Voorbeelden

`distinct([10,2,10,null])`

Retourneert `[10, 2]` .
