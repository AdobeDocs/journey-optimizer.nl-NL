---
product: journey optimizer
title: nowWithDelta
description: Meer informatie over de functie nowWithDelta
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: nowWithDelta, function, expression, trip
exl-id: cb1eb221-8532-4637-ac6c-8e058463ac94
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 4%

---

# nowWithDelta {#nowWithDelta}

Retourneert de huidige datumtijd inclusief een verschuiving. Als een tijdzone-id wordt opgegeven, wordt de verschuiving van de tijdzone toegepast. Voor meer informatie over gegevenstypes, verwijs naar [&#x200B; deze pagina &#x200B;](../expression/data-types.md).

## Categorie

Datum

## Functiesyntaxis

`nowWithDelta(<parameters>)`

## Parameters

| Parameter | Beschrijving |
|--- |--- |
| delta | positieve of negatieve gehele waarde |
| datumonderdeel | jaar, maanden, dagen, uren, minuten of seconden als een tekenreeks |
| tijdzone-id | tekenreeksrepresentatie van de tijdzonewaarde. Voor meer, zie [&#x200B; types van Gegevens &#x200B;](../expression/data-types.md). Tijdzone-id moet een tekenreeksconstante zijn. Het kan geen veldverwijzing of expressie zijn. |

## Handtekeningen en type geretourneerd

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Retourneert een dateTime.

## Voorbeelden

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Retourneert precies 2 uur geleden een dateTime.
