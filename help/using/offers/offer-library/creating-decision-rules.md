---
title: Beslissingsregels maken
description: Leer hoe u besluitvormingsregels maakt om te bepalen aan wie aanbiedingen kunnen worden weergegeven
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 4%

---

# Beslissingsregels maken {#create-decision-rules}

Je kunt besluitvormingsregels voor voorstellen maken op basis van gegevens die beschikbaar zijn in Adobe Experience Platform. Beslissingsregels bepalen aan wie een aanbieding kan worden getoond.

U kunt bijvoorbeeld opgeven dat u alleen een &#39;Women&#39;s Winter Clothing Offer&#39; wilt laten zien wanneer (Gender = &#39;Vrouwelijk&#39;) en (Region = &#39;Noordoost&#39;).

➡️ [Ontdek deze functie in video](#video)

De lijst met nieuwe besluitvormingsregels is toegankelijk in de **[!UICONTROL Components]** -menu.

![](../../assets/decision_rules_list.png)

Voer de volgende stappen uit om een beslissingsregel te maken:

1. Ga naar de **[!UICONTROL Rules]** tab, en klik vervolgens op **[!UICONTROL Create rule]**.

   ![](../../assets/offers_decision_rule_creation.png)

1. Noem uw regel en verstrek een beschrijving, dan vorm de regel volgens uw behoeften.

   Om dit te doen, **Segment Builder** is beschikbaar om u te helpen de voorwaarden van de regel bouwen. [Meer informatie](../../segment/about-segments.md)

   In dit voorbeeld, zal de regel klanten richten die het &quot;Gouden&quot;loyaliteitsniveau hebben.

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >De segmentbouwer die wordt verstrekt om besluitvormingsregels tot stand te brengen heeft sommige specifieke eigenschappen in vergelijking met die gebruikt met **[!UICONTROL Audience Destinations]** service. De **[!UICONTROL Segments]** is niet beschikbaar voor gebruik. Nochtans, is het globale proces dat in de documentatie van de Bouwer van het Segment wordt beschreven nog geldig om aanbiedingen besluitvormingsregels te bouwen.

1. Klikken **[!UICONTROL Save]** ter bevestiging.

1. Zodra de regel wordt gecreeerd, toont het in de lijst van regels. U kunt het selecteren om zijn eigenschappen te tonen en het uit te geven of te schrappen.

   ![](../../assets/rule_created.png)

>[!CAUTION]
>
>Aanbiedingen op basis van gebeurtenissen worden momenteel niet ondersteund in [!DNL Journey Optimizer]. Als u een beslissingsregel maakt op basis van een [event](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}, kunt u deze niet gebruiken in een aanbieding.

## Video over zelfstudie {#video}

>[!NOTE]
>
>Deze video is van toepassing op de Offer decisioning toepassingsservice die op Adobe Experience Platform is gebouwd. Het biedt echter algemene richtlijnen voor het gebruik van Aanbieding in de context van Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
