---
product: journey optimizer
title: startWithIgnoreCase
description: Meer informatie over de functie startWithIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWithIgnoreCase, function, expression, trip
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 14%

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
