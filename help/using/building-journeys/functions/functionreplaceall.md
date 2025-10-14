---
product: journey optimizer
title: replaceAll
description: Meer informatie over de functie replaceAll
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: replaceAll, function, expression, trip
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# replaceAll {#replaceAll}

Vervangt alle instanties die overeenkomen met de doeltekenreeks door de vervangende tekenreeks in de basistekenreeks.

De vervanging vindt plaats vanaf het begin van de tekenreeks tot het einde. Als u bijvoorbeeld &quot;aa&quot; vervangt door &quot;b&quot; in de tekenreeks &quot;aaa&quot;, resulteert dit in &quot;ba&quot; in plaats van &quot;ab&quot;.

## Categorie

String

## Functiesyntaxis

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

Retourneert &quot;hexo Worxd&quot;.

Omdat de doelparameter een RegExp is, moet u, afhankelijk van de tekenreeks die u wilt vervangen, mogelijk enkele tekens verwijderen. Verwijs naar het voorbeeld op [&#x200B; deze pagina &#x200B;](../functions/functionreplace.md#example_2).
