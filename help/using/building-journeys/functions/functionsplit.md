---
product: journey optimizer
title: split
description: Meer informatie over de functie splitsen
feature: Journeys
role: Developer
level: Experienced
keywords: split, function, expression, trip
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 5%

---

# split {#split}

Splitst de eerste argumenttekenreeks op met een scheidingstekenreeks (tweede argumenttekenreeks, die een reguliere expressie kan zijn) om een lijst met tekenreeksen (tokens) te maken.

## Categorie

String

## Functiesyntaxis

`split(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| invoertekenreeks | string |
| scheidingstekenreeks | string |

## Handtekeningen en type geretourneerd

`split(<input string>, <separator string>)`

Retourneert een listString.

## Voorbeeld

`split("A_B_C", "_")`

Retourneert `["A","B","C"]`

Voorbeeld met een gebeurtenisveld &#39;event.appVersion&#39; met waarde: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Retourneert `["20", "45", "2", "3434"]`
