---
product: adobe campaign
title: containIgnoreCase
description: Meer informatie over de functie containIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 14%

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