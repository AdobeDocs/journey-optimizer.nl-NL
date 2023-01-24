---
product: journey optimizer
title: concat
description: Meer informatie over het functieconcept
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: concat, functie, expressie, reis
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

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
