---
product: journey optimizer
title: matchRegExp
description: Meer informatie over de functie matchRegExp
feature: Journeys
role: Engineer
level: Experienced
keywords: matchRegExp, function, expression, trip
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 7%

---

# matchRegExp {#matchRegExp}

Retourneert true als de tekenreeks in de eerste parameter overeenkomt met de reguliere expressie in de tweede parameter. Voor meer informatie, zie [ deze pagina ](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Categorie

String

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

`matchRegExp("12345", "\\d+")`

Retourneert true.
