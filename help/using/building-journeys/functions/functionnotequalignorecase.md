---
product: journey optimizer
title: notEqualIgnoreCase
description: Meer informatie over de functie notEqualIgnoreCase
feature: Journeys
role: Engineer
level: Experienced
keywords: notEqualIgnoreCase, function, expression, trip
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 2%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

Controleer of de eerste argumenttekenreeks met de tweede argumenttekenreeks anders is, waarbij rekening wordt gehouden met hoofdletters en kleine letters.

## Categorie

String

## Functiesyntaxis

`notEqualIgnoreCase(<parameters>)`

## Parameters

* string

## Handtekening en type geretourneerd

`notEqualIgnoreCase(<string>,<string>)`

Retourneert een Booleaanse waarde.

## Voorbeeld

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`
