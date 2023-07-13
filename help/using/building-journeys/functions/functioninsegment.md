---
product: journey optimizer
title: inSegment
description: Meer informatie over de functie in Segment
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment, functie, expressie, reis
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 5%

---

# inSegment {#inSegment}

Controleert of een individu tot een bepaald publiek behoort.

>[!NOTE]
>
>U kunt maximaal 100 soorten publiek ophalen.

De publieksnaam moet een tekenreeksconstante zijn. Het kan geen veldverwijzing of expressie zijn.

Soorten publiek wordt gedefinieerd in het gedeelte [Adobe Experience Platform](https://platform.adobe.com/audience/overview). De uitdrukkingsredacteur verstrekt een autocompleted lijst van publiek.

Het publiek kan drie statussen hebben:

* bestaande: entiteit blijft in het publiek.
* gerealiseerd: entiteit betreedt het publiek.
* verlaten: entiteit verlaat het publiek.

Alleen personen met de **Gerealiseerd** en **Bestaande** de publieksparticipatiestatistieken worden beschouwd als leden van het publiek . Raadpleeg voor meer informatie over het evalueren van een publiek de [Documentatie voor segmentatieservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results).

`IF inSegment('segmentName') == true` betekent dat u een segmentLidmaatschap met de ingegaan/bestaande status hebt.

`ELSE inSegment('segmentName') == false` betekent dat u een segmentLidmaatschap van de verlaten status hebt.

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

De functie wordt geretourneerd **[!UICONTROL true]** als het individu in de reisinstantie deel uitmaakt van het Adobe Experience Platform-publiek met de naam &quot;mannen boven de 50&quot;, **[!UICONTROL false]** anders.
