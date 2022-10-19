---
product: journey optimizer
title: startWithIgnoreCase
description: Meer informatie over de functie startWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 15%

---

# startWithIgnoreCase {#startWithIgnoreCase}

Retourneert true als de tweede parameter een voorvoegsel van de eerste is zonder rekening te houden met hoofdletters en kleine letters.

## Categorie

Tekenreeks

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
