---
product: journey optimizer
title: containIgnoreCase
description: Meer informatie over de functie containIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: containIgnoreCase, function, expression, trip
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 13%

---

# containIgnoreCase {#containIgnoreCase}

Controleert of de tweede argumenttekenreeks zich in de eerste argumenttekenreeks bevindt, zonder rekening te houden met de case.

## Categorie

Tekenreeks

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
