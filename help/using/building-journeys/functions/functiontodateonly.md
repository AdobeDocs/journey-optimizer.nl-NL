---
product: journey optimizer
title: toDateOnly
description: Meer informatie over de functie toDateOnly
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateOnly, functie, expressie, reis
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 1af75a0e6bfc2c3b9c565c3190f46d137a68d32e
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 5%

---

# toDateOnly{#toDateOnly}

Zet een argument in een dateOnly typewaarde om. Meer over gegevenstypes leren, verwijs naar deze [ sectie ](../expression/data-types.md).

## Categorie

Conversie

## Functiesyntaxis

`toDateOnly(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| Tekenreeksrepresentatie van een datum als &quot;YYYY-MM-DD&quot; (XDM-indeling). Ook steunt formaat ISO-8601: slechts **volledig-datum** deel wordt overwogen (verwijs naar [ RFC 3339, sectie 5.6 ](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | string |
| datumtijd | dateTime |
| datumtijd zonder tijdzone | dateTimeOnly |
| geheel-getalwaarde van een tijdperk in milliseconden | integer |

## Handtekeningen en geretourneerde typen

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Retourneert een waarde van het type dateOnly.

## Voorbeelden

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

retourneren alle objecten dateOnly die 2023-08-18 vertegenwoordigen.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Retourneert alleen date.
