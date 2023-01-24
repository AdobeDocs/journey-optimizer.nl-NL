---
product: journey optimizer
title: notEqualIgnoreCase
description: Meer informatie over de functie notEqualIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: notEqualIgnoreCase, function, expression, trip
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 9%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

Controleer of de eerste argumenttekenreeks met de tweede argumenttekenreeks anders is, waarbij rekening wordt gehouden met hoofdletters en kleine letters.

## Categorie

Tekenreeks

## Functiesyntaxis

`notEqualIgnoreCase(<parameters>)`

## Parameters

* string

## Handtekening en type geretourneerd

`notEqualIgnoreCase(<string>,<string>)`

Retourneert een Booleaanse waarde.

## Voorbeeld

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
