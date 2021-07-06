---
title: Een segment maken
description: Leer hoe u segmenten maakt
feature: Journeys
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: 9e93a97ff793fec9fdf4aecd645f1df95b65b31a
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 6%

---

# Segmenten maken {#build-segments}

In dit voorbeeld, zullen wij een segment bouwen om alle klanten te richten die in Atlanta, San Francisco, of Seattle en na 1980 worden geboren. Al deze klanten hadden de toepassing Luma in de laatste 7 dagen moeten openen en vervolgens binnen 2 uur na het openen van de toepassing een aankoop moeten doen.

1. Open het menu **[!UICONTROL Segments]** en klik op de knop **[!UICONTROL Create segment]**.

   ![](../assets/create-segment.png)

   Het scherm van de segmentdefinitie staat u toe om alle vereiste gebieden te vormen om uw segment te bepalen. Leer hoe te om segmenten in [de documentatie van de Dienst van de Segmentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html) te vormen.

   ![](../assets/segment-builder.png)

1. Geef in het deelvenster **[!UICONTROL Segment properties]** een naam en beschrijving (optioneel) voor het segment op.

   ![](../assets/segment-properties.png)

1. Sleep de gewenste velden vanuit het linkerdeelvenster naar de werkruimte in het midden en configureer ze op basis van uw behoeften.

   >[!NOTE]
   >
   >Merk op dat de gebieden beschikbaar in de linkerruit afhankelijk van variëren hoe **XDM Individual Profile** en **XDM ExperienceEvent** schema&#39;s voor uw organisatie zijn gevormd.  Meer informatie vindt u in de [Experience Data Model (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl).

   ![](../assets/drag-fields.png)

   In dit voorbeeld, moeten wij op **Attributes** en **Gebeurtenissen** gebieden vertrouwen om het segment te bouwen:

   * **Kenmerken**: profielen die leven in Atlanta, San Francisco of Seattle, geboren na 1980

      ![](../assets/add-attributes.png)

   * **Gebeurtenissen**: profielen die de toepassing Luma in de laatste 7 dagen hebben geopend en die vervolgens binnen 2 uur na het openen van de toepassing een aankoop hebben gedaan.

      ![](../assets/add-events.png)

1. Terwijl u nieuwe velden toevoegt en configureert in de werkruimte, wordt het deelvenster **[!UICONTROL Segment Properties]** automatisch bijgewerkt met informatie over de geschatte profielen die tot het segment behoren.

   ![](../assets/segment-estimate.png)

1. Wanneer het segment gereed is, klikt u op **[!UICONTROL Save]**. Deze wordt weergegeven in de lijst met Adobe Experience Platform-segmenten. Er is een zoekbalk beschikbaar waarmee u een bepaald segment in de lijst kunt zoeken.

Het segment kan nu worden gebruikt voor uw reizen. Raadpleeg [deze sectie](../segment/about-segments.md) voor meer informatie.

## Video over zelfstudie{#create-segment-video}

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
