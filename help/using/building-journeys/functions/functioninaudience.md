---
product: journey optimizer
title: inPubliek
description: Meer informatie over de functie in Audience
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inPubliek, functie, expressie, reis
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 4%

---

# inPubliek {#inAudience}

Controleert of een individu tot een bepaald publiek behoort.

>[!NOTE]
>
>U kunt maximaal 100 soorten publiek ophalen.

De publieksnaam moet een tekenreeksconstante zijn. Het kan geen veldverwijzing of expressie zijn.

Soorten publiek wordt gedefinieerd in het gedeelte [Adobe Experience Platform](https://platform.adobe.com/audience/overview). De uitdrukkingsredacteur verstrekt een autocompleted lijst van publiek.

Het publiek kan drie statussen hebben:

* bestaande : entiteit blijft in het publiek aanwezig .
* gerealiseerd: entiteit betreedt het publiek.
* verlaten: entiteit verlaat het publiek.

Alleen de personen met de **Realistisch** en **Bestaande** de publieksparticipatiestatistieken worden beschouwd als leden van het publiek . Raadpleeg voor meer informatie over het evalueren van een publiek de [Documentatie voor segmentatieservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`inAudience('audienceName') == true` betekent dat u een segmentLidmaatschap met de ingegaan/bestaande status hebt.

`inAudience('audienceName') == false` betekent dat u een segmentLidmaatschap van de verlaten status hebt.

## Categorie

Adobe Experience Platform

## Functiesyntaxis

`inAudience(<parameter>)`

## Parameters

| Parameter | Beschrijving | Type |
|--- |--- |--- |
| Doelgroep | De publieksnaam | `<string>` |

## Handtekening en type geretourneerd

`inAudience(<string>)`

Retourneert een Booleaanse waarde.

## Voorbeeld

`inAudience("men over 50")`

Uitleg:

De functie wordt geretourneerd **[!UICONTROL true]** als het individu in de reisinstantie deel uitmaakt van het Adobe Experience Platform-publiek met de naam &quot;mannen boven de 50&quot;, **[!UICONTROL false]** anders.
