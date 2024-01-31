---
product: journey optimizer
title: intersect
description: Meer informatie over het snijpunt van de functie
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: intersect, function, expression, trip
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 8%

---

# intersect{#intersect}

Retourneert de gemeenschappelijke waarden in de twee invoerlijsten. Als een van de twee lijsten null is, wordt een lege lijst geretourneerd.

## Categorie

Lijst

## Functiesyntaxis

`intersect(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| lijst 1 | list |
| lijst 2 | list |

## Handtekeningen en geretourneerde typen

`intersect(listString,listString)`: listString
`intersect(listDecimal,listDecimal)`: listDecimal
`intersect(listInteger,listInteger)`: listInteger
`intersect(listDateTime,listDateTime)`: listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly
`intersect(listDateOnly,listDateOnly)`: listDateOnly
`intersect(listDuration,listDuration)`: listDuration
`intersect(listBoolean,listBoolean)`: listBoolean

Retourneert een lijst.

## Voorbeelden

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Retourneert [&quot;sport&quot;, &quot;nieuws&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "news", "documentary"]
)
```

Hiermee worden algemene items tussen profielkenmerken en een lijst met categorieën geretourneerd.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

Retourneert algemene items tussen profielkenmerken en opgegeven gebeurtenisveld.
