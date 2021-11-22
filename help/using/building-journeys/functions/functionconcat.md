---
product: adobe campaign
title: concat
description: Meer informatie over het functieconcept
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '40'
ht-degree: 20%

---

# concat {#concat}

Voegt twee tekenreeksparameters of een lijst met tekenreeksen samen.

## Categorie

Tekenreeks

## Functiesyntaxis

`concat(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| Lijst | listString |
| string | string |

## Handtekening en type geretourneerd

`concat(<string>,<string>)`

`concat(<listString>)`

Retourneert een tekenreeks.

## Voorbeeld

`concat("Hello","World")`

Retourneert &quot;HelloWorld&quot;.

`concat(["Hello"," ","World"])`

Retourneert &quot;Hello World&quot;.
