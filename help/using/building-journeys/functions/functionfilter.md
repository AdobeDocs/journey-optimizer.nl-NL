---
product: journey optimizer
title: filter
description: Meer informatie over het filter function
feature: Journeys
role: Developer
level: Experienced
keywords: filter, functie, expressie, transport
exl-id: 05e3d2ba-1a27-4f27-88cc-3d83eb3b14af
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 6%

---

# filter{#filter}

Retourneert een listObject met objecten waarvan het kenmerk key overeenkomt met een van de opgegeven sleutelwaarden.

## Categorie

Lijst

## Functiesyntaxis

`filter(<parameters>)`

## Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToFilter | listObject | lijst met te filteren objecten. Dit moet een veldverwijzing zijn. |
| keyAttributeName | string | kenmerknaam in de objecten van de opgegeven lijst, gebruikt als sleutel voor filteren |
| keyValueList | list | array van sleutelwaarden voor filteren |

## Handtekeningen en geretourneerde typen

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Retourneert een listObject.

## Voorbeelden

Hier volgt een voorbeeld van een payload die wordt doorgegeven in een binnenkomende gebeurtenis &quot;myevent&quot;:

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

U kunt de volgende expressie gebruiken:

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Retourneert een listObject met de twee objecten met &#39;product2&#39; en &#39;product3&#39; als id.
