---
product: journey optimizer
title: toString
description: Meer informatie over de functie toString
feature: Journeys
role: Engineer
level: Experienced
keywords: toString, function, expression, trip
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# toString {#toString}

Zet een argumentwaarde in een koordwaarde om, afhankelijk van zijn type. Voor meer informatie over gegevenstypes, verwijs naar [&#x200B; deze pagina &#x200B;](../expression/data-types.md).

## Categorie

Conversie

## Functiesyntaxis

`toString(<parameter>)`

## Parameters

| Parameter | Beschrijving |
|--- |--- |
| dateTime | converteert de datum in UTC-datumnotatie |
| dateTimeOnly | converteert de datum in UTC-datumnotatie |
| duur | converteren naar het overeenkomstige aantal milliseconden als een tekenreeks |
| integer | converteert naar tekenreeksrepresentatie van de waarde (1 wordt &quot;1&quot;) |
| decimaal | converteert naar tekenreeksrepresentatie van de waarde (1,5 wordt &quot;1,5&quot;) |
| boolean | Zet de booleaanse waarde om als &#39;true&#39; (waar), &#39;false&#39; (onwaar) |

## Handtekeningen en type geretourneerd

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Retourneer een tekenreeks.

## Voorbeeld

`toString(4)`

Retourneert &quot;4&quot;.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Retourneert de tekenreeksrepresentatie van het opgegeven veld dateOnly (XDM Date-veld), bijvoorbeeld &quot;2023-08-18&quot;.

`toString(toDuration(1520))`

Retourneert &quot;PT1.52S&quot;.
