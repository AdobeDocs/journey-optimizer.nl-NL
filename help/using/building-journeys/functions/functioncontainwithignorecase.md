---
product: journey optimizer
title: containIgnoreCase
description: Meer informatie over de functie containIgnoreCase
feature: Journeys
role: Developer
level: Experienced
keywords: containIgnoreCase, function, expression, trip
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 7%

---

# containIgnoreCase {#containIgnoreCase}

Controleert of de tweede argumenttekenreeks zich in de eerste argumenttekenreeks bevindt, zonder rekening te houden met de case.

## Categorie

String

## Functiesyntaxis

`containIgnoreCase(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| string | string |
| doorzocht tekenreeks | string |

## Handtekening en type geretourneerd

`containIgnoreCase(<string>,<string>)`

Retourneert een Booleaanse waarde.

## Voorbeeld

`containIgnoreCase("rowing is great", "GREAT")`

Retourneert true.
