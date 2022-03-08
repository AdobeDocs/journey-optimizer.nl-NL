---
title: Een segment maken
description: Leer hoe u segmenten maakt
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 5%

---

# Segmenten maken {#build-segments}

In dit voorbeeld, zullen wij een segment bouwen om alle klanten te richten die in Atlanta, San Francisco, of Seattle en na 1980 worden geboren. Al deze klanten hadden de toepassing Luma in de laatste 7 dagen moeten openen en vervolgens binnen 2 uur na het openen van de toepassing een aankoop moeten doen.

1. Toegang krijgen tot **[!UICONTROL Segments]** en klikt u op de knop **[!UICONTROL Create segment]** knop.

   ![](assets/create-segment.png)

   Het scherm van de segmentdefinitie staat u toe om alle vereiste gebieden te vormen om uw segment te bepalen. Leer hoe te om segmenten in te vormen [Documentatie voor segmentatieservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target=&quot;_blank&quot;}.

   ![](assets/segment-builder.png)

1. In de **[!UICONTROL Segment properties]** Geef een naam en een beschrijving (optioneel) voor het segment op.

   ![](assets/segment-properties.png)

1. Sleep de gewenste velden vanuit het linkerdeelvenster naar de werkruimte in het midden en configureer ze op basis van uw behoeften.

   >[!NOTE]
   >
   >De velden in het linkervenster zijn afhankelijk van de manier waarop de **Afzonderlijk XDM-profiel** en **XDM ExperienceEvent** De schema&#39;s zijn gevormd voor uw organisatie.  Meer informatie in het dialoogvenster [XDM-documentatie (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target=&quot;_blank&quot;}.

   ![](assets/drag-fields.png)

   In dit voorbeeld moeten we erop vertrouwen **Attributen** en **Gebeurtenissen** velden voor het samenstellen van het segment:

   * **Attributen**: profielen die leven in Atlanta, San Francisco of Seattle, geboren na 1980

      ![](assets/add-attributes.png)

   * **Gebeurtenissen**: profielen die de toepassing Luma in de laatste 7 dagen hebben geopend en die vervolgens binnen 2 uur na het openen van de toepassing een aankoop hebben gedaan.

      ![](assets/add-events.png)

1. Terwijl u nieuwe velden toevoegt en configureert in de werkruimte, worden de **[!UICONTROL Segment Properties]** wordt automatisch bijgewerkt met informatie over de geschatte profielen die tot het segment behoren.

   ![](assets/segment-estimate.png)

1. Als het segment gereed is, klikt u op **[!UICONTROL Save]**. Deze wordt weergegeven in de lijst met Adobe Experience Platform-segmenten. Er is een zoekbalk beschikbaar waarmee u een bepaald segment in de lijst kunt zoeken.

Het segment kan nu worden gebruikt voor uw reizen. Raadpleeg [deze sectie](../segment/about-segments.md) voor meer informatie.

## Video over zelfstudie{#create-segment-video}

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
