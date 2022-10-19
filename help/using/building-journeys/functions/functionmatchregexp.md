---
product: journey optimizer
title: matchRegExp
description: Meer informatie over de functie matchRegExp
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

---

# matchRegExp {#matchRegExp}

Retourneert true als de tekenreeks in de eerste parameter overeenkomt met de reguliere expressie in de tweede parameter. Zie voor meer informatie [deze pagina](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Categorie

Tekenreeks

## Functiesyntaxis

`matchRegExp(<parameters>)`

## Parameters

| Parameter | Type |
|--- |--- |
| string | string |
| regexp | string |

## Handtekening en type geretourneerd

`matchRegExp(<string>,<string>)`

Retourneert een Booleaanse waarde.

## Voorbeeld

`matchRegExp("username@adobe.com", "*adobe")`

Retourneert true.
