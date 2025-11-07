---
product: journey optimizer
title: inSegment
description: Meer informatie over de functie in Segment
feature: Journeys
role: Developer
level: Experienced
keywords: inSegment, functie, expressie, reis
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 4%

---

# inSegment {#inSegment}

Controleert of een individu tot een bepaald publiek behoort.

>[!NOTE]
>
>U kunt maximaal 100 soorten publiek ophalen.

De publieksnaam moet een tekenreeksconstante zijn. Het kan geen veldverwijzing of expressie zijn.

Het publiek wordt bepaald in [ Adobe Experience Platform ](https://platform.adobe.com/audience/overview). De uitdrukkingsredacteur verstrekt een autocompleted lijst van publiek.

Soorten publiek kan twee statussen hebben:

* gerealiseerd: Entiteit komt in aanmerking voor de segmentdefinitie.
* verlaten: De entiteit verlaat de segmentdefinitie.

Slechts zullen de individuen met de **Realized** status van de publieksparticipatie als leden van het publiek worden beschouwd. Voor meer op hoe te om een publiek te evalueren, verwijs naar de [ documentatie van de Dienst van de Segmentatie ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`inSegment('segmentName') == true` betekent dat u een segmentLidmaatschap met de ingegaan/bestaande status hebt.

`inSegment('segmentName') == false` betekent dat u een segmentLidmaatschap van de verlaten status hebt.

## Categorie

Adobe Experience Platform

## Functiesyntaxis

`inSegment(<parameter>)`

## Parameters

| Parameter | Beschrijving | Type |
|--- |--- |--- |
| Segment | De publieksnaam | `<string>` |

## Handtekening en type geretourneerd

`inSegment(<string>)`

Retourneert een Booleaanse waarde.

## Voorbeeld

`inSegment("men over 50")`

Uitleg:

De functie retourneert **[!UICONTROL true]** als de persoon binnen de reisinstantie deel uitmaakt van het Adobe Experience Platform-publiek met de naam &quot;men boven 50&quot;, anders **[!UICONTROL false]** .
