---
solution: Journey Optimizer
product: journey optimizer
title: Segmentdefinities samenstellen
description: Leer hoe u publiek kunt maken met segmentdefinities
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 4%

---

# Segmentdefinities samenstellen {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Een regel maken"
>abstract="Met de methode voor het maken van buildregels kunt u een nieuwe publieksdefinitie maken met Adobe Experience Platform Audienation Service."

In dit voorbeeld bouwen we een publiek dat gericht is op alle klanten die in Atlanta, San Francisco of Seattle wonen en na 1980 geboren zijn. Al deze klanten hadden de toepassing Luma in de laatste 7 dagen moeten openen en vervolgens binnen 2 uur na het openen van de toepassing een aankoop moeten doen.

➡️ [Leer hoe u in deze video een publiek kunt maken](#video-segment)

1. Toegang krijgen tot **[!UICONTROL Audiences]** en klikt u op de knop **[!UICONTROL Create audience]** knop.

   ![](assets/create-segment.png)

   In het scherm voor segmentdefinitie kunt u alle vereiste velden configureren om uw publiek te definiëren. Leer hoe te om publiek in te vormen [Documentatie voor segmentatieservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"}.

   ![](assets/segment-builder.png)

1. In de **[!UICONTROL Audience properties]** Geef een naam en een beschrijving (optioneel) voor de doelgroep op.

   ![](assets/segment-properties.png)

1. Sleep de gewenste velden vanuit het linkerdeelvenster naar de werkruimte in het midden en configureer ze op basis van uw behoeften.

   >[!NOTE]
   >
   >De velden in het linkervenster zijn afhankelijk van de manier waarop de **Afzonderlijk XDM-profiel** en **XDM ExperienceEvent** De schema&#39;s zijn gevormd voor uw organisatie.  Meer informatie in het dialoogvenster [XDM-documentatie (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}.

   ![](assets/drag-fields.png)

   In dit voorbeeld moeten we erop vertrouwen **Attributen** en **Gebeurtenissen** velden voor het opbouwen van het publiek:

   * **Attributen**: profielen die leven in Atlanta, San Francisco of Seattle, geboren na 1980

     ![](assets/add-attributes.png)

   * **Gebeurtenissen**: profielen die de toepassing Luma in de laatste 7 dagen hebben geopend en die vervolgens binnen 2 uur na het openen van de toepassing een aankoop hebben gedaan.

     ![](assets/add-events.png)

1. Terwijl u nieuwe velden toevoegt en configureert in de werkruimte, worden de **[!UICONTROL Audience Properties]** wordt automatisch bijgewerkt met informatie over de geschatte profielen die bij het publiek horen.

   ![](assets/segment-estimate.png)

1. Als het publiek klaar is, klikt u op **[!UICONTROL Save]**. Deze wordt weergegeven in de lijst met Adobe Experience Platform-doelgroepen. Er is een zoekbalk beschikbaar waarmee u een bepaald publiek in de lijst kunt zoeken.

Het publiek kan nu worden gebruikt voor uw reizen. Raadpleeg [deze sectie](../audience/about-audiences.md) voor meer informatie.

## Hoe kan ik-video{#video-segment}

Leer hoe u een publiek kunt maken.

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
