---
product: journey optimizer
title: limiet
description: Meer informatie over de functielimiet
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 5%

---

# limiet {#limit}

Retourneert de eerste of laatste N-elementen van een lijst.

>[!NOTE]
>
>Als de doellijst een listObject is, kan deze functie alleen worden gebruikt in aangepaste actiedragers.

## Categorie

Lijst

## Functiesyntaxis

`limit(<parameters>)`

## Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te sorteren lijst. Voor listObject moet dit een veldverwijzing zijn. |
| numberOfItems | integer | Aantal items dat moet worden geretourneerd uit de opgegeven lijst. |
| firstOrLastItems | boolean | Deze parameter is optioneel (standaard true). true retourneert de eerste items. false retourneert de laatste items. |

## Handtekening en type geretourneerd

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

Retourneert een lijst met tekenreeksen.

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

Retourneert een lijst met gehele getallen.

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

Retourneert een lijst met decimalen.

`limit(<listBoolean>,<integer>)`
`limit(<listBoolean>,<integer>,<boolean>)`

Retourneert een lijst met laarzen.

`limit(<listDateOnly>,<integer>)`
`limit(<listDateOnly>,<integer>,<boolean>)`

Retourneert een lijst met datums.

`limit(<listDateTimeOnly>,<integer>)`
`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Keert een lijst van datetimes zonder tijdzone terug te overwegen.

`limit(<listDateTime>,integer>)`
`limit(<listDateTime>,<integer>,<boolean>)`

Retourneert een lijst met datetimes.

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

Retourneert een lijst met tijdsduur.

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

Retourneert een lijst met objecten.

## Voorbeeld

`limit(["A", "B", "C", "D", "E"], 3)`

Retourneert `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Retourneert `["C","D","E"]`.
