---
product: journey optimizer
title: replace
description: Meer informatie over de functie replace
feature: Journeys
role: Developer
level: Experienced
keywords: replace, function, expression, trip
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---

# replace {#replace}

Vervangt de eerste instantie die overeenkomt met de doeltekenreeks door de vervangende tekenreeks in de basistekenreeks.

De vervanging vindt plaats vanaf het begin van de tekenreeks tot het einde. Als u bijvoorbeeld &quot;aa&quot; vervangt door &quot;b&quot; in de tekenreeks &quot;aaa&quot;, resulteert dit in &quot;ba&quot; in plaats van &quot;ab&quot;.

## Categorie

String

## Functiesyntaxis

`replace(<parameters>)`

## Parameters

| Parameter | Type |
|-----------|--------------|
| basis | string |
| target | tekenreeks (RegExp) |
| vervanging | string |

## Handtekening en type geretourneerd

`replace(<base>,<target>,<replacement>)`

Retourneer een tekenreeks.

## Voorbeeld 1

`replace("Hello World", "l", "x")`

Retourneert &quot;Hexlo World&quot;.

## Voorbeeld 2 {#example_2}

Omdat de doelparameter een RegExp is, moet u, afhankelijk van de tekenreeks die u wilt vervangen, mogelijk enkele tekens verwijderen. Hier volgt een voorbeeld:

* te evalueren tekenreeks: `|OFFER_A|OFFER_B`
* opgegeven door een profielkenmerk `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Te vervangen tekenreeks: `|OFFER_A`
* Tekenreeks vervangen door: `''`
* U moet `\\` vóór het `|` -teken toevoegen.

De expressie is:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

De geretourneerde tekenreeks is: `|OFFER_B`

U kunt ook de tekenreeks maken die moet worden vervangen door een bepaald kenmerk:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`
