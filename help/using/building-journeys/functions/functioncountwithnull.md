---
product: journey optimizer
title: countWithNull
description: Meer informatie over de functie countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull, function, expression, trip
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 28%

---

# countWithNull {#countWithNull}

Telt alle elementen van de lijst met inbegrip van ongeldige waarden.

## Categorie

Samenvoeging

## Functiesyntaxis

`countWithNull(<listAny>)`

## Parameters

| Parameter | Type |
|-----------|------------------|
| Lijst | listString |
| Lijst | listBoolean |
| Lijst | listInteger |
| Lijst | listDecimal |
| Lijst | listDuration |
| Lijst | listDateTime |
| Lijst | listDateTimeOnly |
| Lijst | listDateOnly |

## Handtekening en type geretourneerd

`countWithNull(<listAny>)`

Retourneert een geheel getal.

## Voorbeeld

`countWithNull([10,2,10,null])`

Retourneert 4.
