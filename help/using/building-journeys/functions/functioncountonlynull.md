---
product: adobe campaign
title: countOnlyNull
description: Meer informatie over de functie countOnlyNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 31%

---

# countOnlyNull {#countOnlyNull}

Telt het aantal null-waarden in de lijst.

## Categorie

Samenvoeging

## Functiesyntaxis

`countOnlyNull(<listAny>)`

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

`countOnlyNull(<listAny>)`

Retourneert een geheel getal.

## Voorbeeld

`countOnlyNull([10,2,10,null])`

Retourneert 1.