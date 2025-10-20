---
product: journey optimizer
title: toDateTime
description: Meer informatie over de functie toDateTime
feature: Journeys
role: Engineer
level: Experienced
keywords: toDateTime, function, expression, trip
exl-id: 2b487e60-593e-4bf7-9639-f469ba0f5cdc
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

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
>Tijdzone-id moet een tekenreeksconstante zijn. Het kan geen veldverwijzing of expressie zijn. Voor meer informatie over gegevenstypes, verwijs naar [&#x200B; deze pagina &#x200B;](../expression/data-types.md).

## Handtekeningen en geretourneerde typen

`toDateTime(<string>)`

`toDateTime(<stringified time zone id>, <dateTimeOnly>)`

`toDateTime(<integer>)`

Keer a **dateTime** terug.

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

`toDateTime ("2023-08-18T23:17:59.123Z")`

Keert 2023-08-18T23 :17: 59.123Z terug

`toDateTime(toDateTimeOnly("UTC", "2023-08-18T23:17:59.123"))`

Keert 2023-08-18T23 :17: 59.123Z terug

`toDateTime(1560762190189)`

Keert 2023-06-17T09 :03: 10.189Z terug

<!--`toDateTime ("2016-08-18T23:17:59.123", "UTC")`

Returns 2016-08-18T23:17:59.123Z.

`toDateTime("Z",2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000Z.

`toDateTime("Z",2016,8,18)`

Returns 2016-08-18T00:00:00.000Z.-->
