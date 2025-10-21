---
product: journey optimizer
title: concat
description: Meer informatie over het functieconcept
feature: Journeys
role: Developer
level: Experienced
keywords: concat, functie, expressie, reis
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 9%

---

# concat {#concat}

Voegt twee tekenreeksparameters of een lijst met tekenreeksen samen.

## Categorie

String

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
