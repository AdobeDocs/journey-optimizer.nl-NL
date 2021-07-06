---
title: Beslissingsregels maken
description: Leer hoe je beslissingsregels maakt in Adobe Experience Platform.
feature: Aanbiedingen
topic: Integraties
role: User
level: Intermediate
source-git-commit: 0e5cc9101ff382ce9fde442da38eb46aa28e9c77
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---

# Beslissingsregels maken {#creating-decision-rules}

Je kunt besluitvormingsregels voor voorstellen maken op basis van gegevens die beschikbaar zijn in Adobe Experience Platform. Beslissingsregels bepalen aan wie een aanbieding kan worden getoond.

U kunt bijvoorbeeld opgeven dat u alleen een &#39;Women&#39;s Winter Clothing Offer&#39; wilt laten zien wanneer (Gender = &#39;Vrouwelijk&#39;) en (Region = &#39;Noordoost&#39;).

➡️ [Ontdek deze functie in video](#video)

De lijst van gecreeerde besluitvormingsregels is toegankelijk in **[!UICONTROL Components]** menu.

![](../../assets/decision_rules_list.png)

Voer de volgende stappen uit om een beslissingsregel te maken:

1. Ga naar het **[!UICONTROL Rules]** lusje, dan klik **[!UICONTROL Create rule]**.

   ![](../../assets/offers_decision_rule_creation.png)

1. Noem uw regel en verstrek een beschrijving, dan vorm de regel volgens uw behoeften.

   Om dit te doen, is **de Bouwer van het Segment** van Adobe Experience Platform beschikbaar om u te helpen de voorwaarden van de regel bouwen. Raadpleeg de [specifieke documentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html) voor meer informatie over het gebruik ervan.

   In dit voorbeeld, zal de regel klanten richten die het &quot;Gouden&quot;loyaliteitsniveau hebben.

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >De opsteller van het Segment die wordt verstrekt om besluitvormingsregels tot stand te brengen heeft sommige specifieke eigenschappen in vergelijking met die gebruikt met de **[!UICONTROL Audience Destinations]** dienst. Het tabblad **[!UICONTROL Segments]** is bijvoorbeeld niet beschikbaar voor gebruik. Nochtans, is het globale proces dat in de documentatie van de Bouwer van het Segment wordt beschreven nog geldig om aanbiedingen besluitvormingsregels te bouwen.

1. Klik **[!UICONTROL Save]** om te bevestigen.

1. Zodra de regel wordt gecreeerd, toont het in de lijst van regels. U kunt het selecteren om zijn eigenschappen te tonen en het uit te geven of te schrappen.

   ![](../../assets/rule_created.png)

## Video over zelfstudie {#video}

>[!NOTE]
>
>Deze video is van toepassing op de Offer decisioning toepassingsservice die op Adobe Experience Platform is gebouwd. Het biedt echter algemene richtlijnen voor het gebruik van Aanbieding in de context van Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
