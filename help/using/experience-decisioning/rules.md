---
title: Besluitvormingsregels
description: Leer hoe u met beslissingsregels werkt
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Beperkte beschikbaarheid"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---

# Besluitvormingsregels {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Beslissingsregels maken"
>abstract="Met beslissingsregels kunt u het publiek voor beslissingsitems definiëren door beperkingen toe te passen, rechtstreeks op het niveau van de beslissingsitems of binnen een specifieke selectiestrategie. Hierdoor kunt u precies bepalen welke items aan wie moeten worden gepresenteerd."

## Over beslissingsregels {#about}

Met beslissingsregels kunt u het publiek voor beslissingsitems definiëren door beperkingen toe te passen, rechtstreeks op het niveau van de beslissingsitems of binnen een specifieke selectiestrategie. Hierdoor kunt u precies bepalen welke items aan wie moeten worden gepresenteerd.

Laten we bijvoorbeeld een scenario overwegen waarin u beslissingsitems hebt die Yoga-gerelateerde producten bevatten die zijn ontworpen voor vrouwen. Met beslissingsregels kunt u aangeven dat deze items alleen mogen worden weergegeven in profielen waarvan het geslacht &quot;Vrouwelijk&quot; is en die in &#39;Yoga&#39; een &#39;Belangenpunt&#39; hebben aangegeven.

>[!NOTE]
>
>Naast de besluitvormingsregels op het niveau van de item- en selectiestrategie kunt u ook het doelpubliek op campagnereniveau definiëren. [Meer informatie](../campaigns/create-campaign.md#audience)

De lijst met besluitvormingsregels is toegankelijk in het **[!UICONTROL Strategy setup]** -menu.

![](assets/decision-rules-list.png)

## Een beslissingsregel maken {#create}

Voer de volgende stappen uit om een beslissingsregel te maken:

1. Navigeren naar **[!UICONTROL Strategy setup]** / **[!UICONTROL Decision rules]** klik vervolgens op **[!UICONTROL Create rule]** knop.

1. Het scherm van de besluitvormingsregels opent. Geef de regel een naam en geef een beschrijving op.

1. Bouw de beslissingsregel aan uw behoeften gebruikend de Bouwer van het Segment van Adobe Experience Platform. Hiertoe kunt u verschillende gegevensbronnen gebruiken, zoals profielkenmerken, soorten publiek of contextgegevens die uit Adobe Experience Platform afkomstig zijn. [Leer hoe u contextgegevens kunt gebruiken](#context-data)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >De opsteller van het Segment die wordt verstrekt om besluitvormingsregels tot stand te brengen stelt wat specifieke kenmerken in vergelijking met die gebruikt met de dienst van de Segmentatie van Adobe Experience Platform.  Nochtans, is het globale proces dat in de documentatie wordt beschreven nog geldig om besluitvormingsregels te bouwen. [Leer hoe te om segmentdefinities te bouwen](../audience/creating-a-segment-definition.md)

1. Terwijl u nieuwe velden toevoegt en configureert in de werkruimte, worden de **[!UICONTROL Audience properties]** wordt informatie weergegeven over de geschatte profielen die bij het publiek horen. Klikken **[!UICONTROL Refresh estimate]** gegevens bijwerken.

   >[!NOTE]
   >
   >Profielramingen zijn niet beschikbaar wanneer regelparameters gegevens bevatten die niet in het profiel staan, zoals contextgegevens.

1. Als uw beslissingsregel gereed is, klikt u op **[!UICONTROL Save]**. De gemaakte regel wordt in de lijst weergegeven en kan worden gebruikt in besluitvormingselementen en selectiestrategieën om de presentatie van beslissingsitems in profielen te regelen.

