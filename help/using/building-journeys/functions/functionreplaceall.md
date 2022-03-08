---
product: adobe campaign
title: replaceAll
description: Meer informatie over de functie replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 6%

---

# replaceAll {#replaceAll}

Replaces all occurrences matching the target string by the replacement string in the base string.

The replacement proceeds from the beginning of the string to the end, for example, replacing &quot;aa&quot; with &quot;b&quot; in the string &quot;aaa&quot; will result in &quot;ba&quot; rather than &quot;ab&quot;.

## Categorie

Tekenreeks

## Function syntax

`replaceAll(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|--------------|
| basis | string |
| target | tekenreeks (RegExp) |
| vervanging | string |

## Handtekening en type geretourneerd

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Retourneert een tekenreeks.

## Voorbeeld{#example}

`replaceAll("Hello World", "l", "x")`

Returns &quot;Hexxo Worxd&quot;.

Omdat de doelparameter een RegExp is, moet u, afhankelijk van de tekenreeks die u wilt vervangen, mogelijk enkele tekens verwijderen. Raadpleeg het voorbeeld in [deze pagina](../functions/functionreplace.md#example_2).
