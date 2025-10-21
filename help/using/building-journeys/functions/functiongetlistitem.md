---
product: journey optimizer
title: getListItem
description: Meer informatie over de functie gstListItem
feature: Journeys
role: Developer
level: Experienced
keywords: getListItem, functie, expressie, reis
exl-id: e995f479-bbaa-45f3-9531-e05680c5a723
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 12%

---

# getListItem {#gestListItem}

Retourneert het item van de lijst bij de opgegeven index.

## Categorie

Lijst

## Functiesyntaxis

`getListItem(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| index | integer |

## Handtekeningen en type geretourneerd

`getListItem(<listInteger>,<index>)`

Retourneert een geheel getal.

`getListItem(<listDecimal>,<index>)`

Retourneert een decimaal.

`getListItem(<listString>,<index>)`

Retourneert een tekenreeks.

`getListItem(<listDateTimeOnly>,<index>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

`getListItem(<listDateTime>,<index>)`

Retourneert een datetime.

`getListItem(<listDateOnly>,<index>)`

Retourneert een lijst met datums.

`getListItem(<listBoolean>,<index>)`

Retourneert een Booleaanse waarde.

`getListItem(<listDuration>,<index>)`

Retourneert een duur.

## Voorbeeld

`getListItem([10, 2, 3], 1)`

Retourneert &quot;2&quot;

`getListItem(["A", "B", "C"], 2)`
Retourneert &quot;C&quot;

Voorbeelden met een gebeurtenisveld &#39;event.appVersion&#39; met waarde: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Retourneert `["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

Retourneert &quot;20&quot;
