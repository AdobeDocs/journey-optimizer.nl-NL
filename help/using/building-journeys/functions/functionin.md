---
product: journey optimizer
title: in
description: Meer informatie over de functie in
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 629b7aa3-8904-453b-ba3c-c6a333b13c81
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 15%

---

# in {#in}

Controleert of de waarde van het eerste argument in de lijst voorkomt. De controle wordt uitgevoerd door Gelijk op elke argumentwaarde. De waarde wordt true geretourneerd als de argumentwaarde wordt gevonden, anders false.

Het type van `<expression>` moet overeenkomen met items in de lijst. Typen items in de lijst moeten, ter herinnering, met elkaar overeenkomen.

## Categorie

Lijst

## Functiesyntaxis

`in(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| Tekenreeks | Tekenreeks |
| Boolean | Boolean |
| Geheel | Geheel |
| Decimaal | Decimaal |
| Duur | Duur |
| DateTime | DateTime |
| DateTimeOnly | DateTimeOnly |
| Lijst | listString |
| Lijst | listBoolean |
| Lijst | listInteger |
| Lijst | listDecimal |
| Lijst | listDuration |
| Lijst | listDateTime |
| Lijst | listDateTimeOnly |
| Lijst | listDateOnly |

## Handtekening en type geretourneerd

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Retourneer een booleaanse waarde.

## Voorbeeld

`in(4,[4,5,3,4])`

Retourneert true.

`in(8,[4,5,3,4])`

Retourneert false.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
