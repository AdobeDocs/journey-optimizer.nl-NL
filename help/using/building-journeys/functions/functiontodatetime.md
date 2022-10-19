---
product: journey optimizer
title: toDateTime
description: Meer informatie over de functie toDateTime
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 2b487e60-593e-4bf7-9639-f469ba0f5cdc
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 7%

---

# toDateTime {#toDateTime}

Zet parameters om in een datumtijdwaarde, afhankelijk van hun types.

## Categorie

Conversie

## Functiesyntaxis

`toDateTime(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd in ISO-8601-indeling | string |
| tijdzone-id | string |
| datumtijd zonder tijdzone | dateTimeOnly |
| geheel-getalwaarde van een tijdperk in milliseconden | integer |

>[!NOTE]
>
>Tijdzone-id moet een tekenreeksconstante zijn. Het kan geen veldverwijzing of expressie zijn. Raadpleeg voor meer informatie over gegevenstypen [deze pagina](../expression/data-types.md).

## Handtekeningen en geretourneerde typen

`toDateTime(<string>)`

`toDateTime(<stringified time zone id>, <dateTimeOnly>)`

`toDateTime(<integer>)`

Retourneer een **dateTime**.

<!--`toDateTime(<year>,<month>,<dayOfMonth>,<hour>,<minute>,<second>)`

Returns a date time with default time zone UTC.

`toDateTime(<year>,<month>,<dayOfMonth>)`
`toDateTime(<stringified timeZone>,<year>,<month>,<dayOfMonth>)`
`toDateTime(<timeZone>,<year>,<month>,<dayOfMonth>)`

Return a datetime where hour, minute and second set to 0.

`toDateTime(<stringified timeZone>,<year>,<month>,<dayOfMonth>,<hour>,<minute>,<second>)`
`toDateTime(<string>)`
`toDateTime(<string>,<integer>)`
`toDateTime(<stringified timeZone>,<dateTimeOnly)`

`toDateTime(<timeZone>,<integer>)`

Return a datetime.

-->

## Voorbeelden

`toDateTime ("2016-08-18T23:17:59.123Z")`

Retourneert 2016-08-18T23:17:59,123Z

`toDateTime(toDateTimeOnly("UTC", "2016-08-18T23:17:59.123"))`

Retourneert 2016-08-18T23:17:59,123Z

`toDateTime(1560762190189)`

Retourneert 2019-06-17T09:03:10,189Z

<!--`toDateTime ("2016-08-18T23:17:59.123", "UTC")`

Returns 2016-08-18T23:17:59.123Z.

`toDateTime("Z",2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000Z.

`toDateTime("Z",2016,8,18)`

Returns 2016-08-18T00:00:00.000Z.-->
