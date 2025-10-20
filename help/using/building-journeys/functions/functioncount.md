---
product: journey optimizer
title: count
description: Meer informatie over het aantal functies
feature: Journeys
role: Engineer
level: Experienced
keywords: aantal, functie, expressie, reis
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 5%

---

# count {#count}

Telt de elementen van de lijst die geen rekening houden met de ongeldige waarden.

## Categorie

Samenvoeging

## Functiesyntaxis

`count(<listAny>)`

`count(<listObject>)`

## Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te verwerken lijst. Voor listObject moet dit een veldverwijzing zijn. Een listObject kan geen null-object bevatten. |

## Handtekeningen en type geretourneerd

`count(<listAny>)`

Retourneert een geheel getal.

## Voorbeeld

`count([10,2,10,null])`

Retourneert 3.

`count(@event{my_event.productListItems})`

Retourneert het aantal objecten in de opgegeven array met objecten (type listObject). Opmerking: een listObject kan geen null-object bevatten
