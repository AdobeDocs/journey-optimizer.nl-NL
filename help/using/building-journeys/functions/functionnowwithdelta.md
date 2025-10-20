---
product: journey optimizer
title: nowWithDelta
description: Meer informatie over de functie nowWithDelta
feature: Journeys
role: Engineer
level: Experienced
keywords: nowWithDelta, function, expression, trip
exl-id: cb1eb221-8532-4637-ac6c-8e058463ac94
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 4%

---

# nowWithDelta {#nowWithDelta}

Retourneert de huidige datumtijd inclusief een verschuiving. Als een tijdzone-id wordt opgegeven, wordt de verschuiving van de tijdzone toegepast. Voor meer informatie over gegevenstypes, verwijs naar [ deze pagina ](../expression/data-types.md).

## Categorie

Datum

## Functiesyntaxis

`nowWithDelta(<parameters>)`

## Parameters

| Parameter | Beschrijving |
|--- |--- |
| delta | positieve of negatieve gehele waarde |
| datumonderdeel | jaar, maanden, dagen, uren, minuten of seconden als een tekenreeks |
| tijdzone-id | tekenreeksrepresentatie van de tijdzonewaarde. Voor meer, zie [ types van Gegevens ](../expression/data-types.md). Tijdzone-id moet een tekenreeksconstante zijn. Het kan geen veldverwijzing of expressie zijn. |

## Handtekeningen en type geretourneerd

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Retourneert een dateTime.

## Voorbeelden

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Retourneert precies 2 uur geleden een dateTime.
