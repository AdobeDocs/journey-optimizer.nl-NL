---
product: journey optimizer
title: inPubliek
description: Meer informatie over de functie in Audience
feature: Journeys
role: Developer
level: Experienced
keywords: inPubliek, functie, expressie, reis
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 3%

---

# inPubliek {#inAudience}

Controleert of een individu tot een bepaald publiek behoort.

>[!NOTE]
>
>U kunt maximaal 100 soorten publiek ophalen.

De publieksnaam moet een tekenreeksconstante zijn. Het kan geen veldverwijzing of expressie zijn.

Het publiek wordt bepaald in [&#x200B; Adobe Experience Platform &#x200B;](https://platform.adobe.com/audience/overview). De uitdrukkingsredacteur verstrekt een autocompleted lijst van publiek.

Soorten publiek kan twee statussen hebben:

* gerealiseerd: Entiteit komt in aanmerking voor de segmentdefinitie.
* verlaten: De entiteit verlaat de segmentdefinitie.

Slechts zullen de individuen met de **Realized** status van de publieksparticipatie als leden van het publiek worden beschouwd. Voor meer op hoe te om een publiek te evalueren, verwijs naar de [&#x200B; documentatie van de Dienst van de Segmentatie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=nl-NL#interpret-segment-results).

`inAudience('audienceName') == true` betekent dat u een segmentLidmaatschap met de ingegaan status hebt.

`inAudience('audienceName') == false` betekent dat u een segmentLidmaatschap van de verlaten status hebt.


>[!IMPORTANT]
>
>Als u de naam van een bestaand publiek wijzigt, worden niet automatisch verwijzingen naar dat publiek in uw reisuitdrukkingen bijgewerkt. Als uw voorwaardenknooppunt `inAudience('oldAudienceName')` gebruikt, moet u de expressie handmatig bewerken om de nieuwe naam te gebruiken. Als dit niet gebeurt, wordt de reisconditie verbroken.

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

De functie retourneert **[!UICONTROL true]** als de persoon binnen de reisinstantie deel uitmaakt van het Adobe Experience Platform-publiek met de naam &quot;men boven 50&quot;, anders **[!UICONTROL false]** .

