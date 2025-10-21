---
product: journey optimizer
title: startWithIgnoreCase
description: Meer informatie over de functie startWithIgnoreCase
feature: Journeys
role: Developer
level: Experienced
keywords: startWithIgnoreCase, function, expression, trip
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 8%

---

# startWithIgnoreCase {#startWithIgnoreCase}

Retourneert true als de tweede parameter een voorvoegsel van de eerste is zonder rekening te houden met hoofdletters en kleine letters.

## Categorie

String

## Functiesyntaxis

`startWithIgnoreCase(<parameters>)`

## Parameters

| Parameter | Type |
|-------------|--------|
| string | string |
| prefix | string |

## Handtekening en type geretourneerd

`startWithIgnoreCase(<string>,<string>)`

Retourneer een booleaanse waarde.

## Voorbeeld

`startWithIgnoreCase("rowing is great", "RO")`

Retourneert true.
