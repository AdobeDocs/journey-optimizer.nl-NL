---
title: Beslissingsregels maken
description: Leer hoe u besluitvormingsregels maakt om te bepalen aan wie aanbiedingen kunnen worden weergegeven
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 4%

---

# Beslissingsregels maken {#create-decision-rules}

## Over beslissingsregels {#about}

Je kunt besluitvormingsregels voor voorstellen maken op basis van gegevens die beschikbaar zijn in Adobe Experience Platform. Beslissingsregels bepalen aan wie een aanbieding kan worden getoond.

U kunt bijvoorbeeld opgeven dat u alleen een &#39;Women&#39;s Winter Clothing Offer&#39; wilt laten zien wanneer (Gender = &#39;Vrouwelijk&#39;) en (Region = &#39;Noordoost&#39;).

➡️ [Ontdek deze functie in video](#video)

Hier volgt een lijst met beperkingen die in acht moeten worden genomen wanneer u werkt met beslissingsregels:

* Wanneer het creëren van een regel, kunt u historische gebeurtenissen gebruiken maar er zijn beperkingen op wanneer deze regels bruikbaar zijn.
* Bij het bepalen van de rand wordt het randprofiel gebruikt waarin geen gebeurtenissen worden opgeslagen. Elke regel die in een randbesluit wordt gebruikt, is daarom ongeldig.
* De reizen die de Besluiten van de Aanbieding gebruiken zullen niet naar historische gebeurtenissen kijken, zodat zullen deze regels ongeldig zijn.
* De verzoeken van het besluit die het hubprofiel gebruiken zullen de laatste 100 ervaringsgebeurtenissen op het profiel bekijken om regels te evalueren die historische ervaringsgebeurtenissen van verwijzingen voorzien.

## Een beslissingsregel maken {#create}

De lijst met nieuwe besluitvormingsregels is toegankelijk in de **[!UICONTROL Components]** -menu.

![](../assets/decision_rules_list.png)

Voer de volgende stappen uit om een beslissingsregel te maken:

1. Ga naar de **[!UICONTROL Rules]** tab, en klik vervolgens op **[!UICONTROL Create rule]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Noem uw regel en verstrek een beschrijving, dan vorm de regel volgens uw behoeften.

   Om dit te doen, de Adobe Experience Platform **Segment Builder** is beschikbaar om u te helpen de voorwaarden van de regel bouwen. [Leer hoe te om segmentdefinities te bouwen](../../audience/creating-a-segment-definition.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >De segmentbouwer die wordt verstrekt om besluitvormingsregels tot stand te brengen heeft sommige specifieke eigenschappen in vergelijking met die gebruikt met **[!UICONTROL Segmentation]** service. Het algemene proces dat in het [Segment Builder](../../audience/creating-a-segment-definition.md) de documentatie is nog geldig om aanbiedingen besluitvormingsregels op te bouwen. Meer informatie in het dialoogvenster [Adobe Experience Platform Segmentation Service-documentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html).

1. Terwijl u nieuwe velden toevoegt en configureert in de werkruimte, worden de **[!UICONTROL Audience properties]** wordt informatie weergegeven over de geschatte profielen die bij het publiek horen. Klikken **[!UICONTROL Refresh estimate]** gegevens bijwerken.

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >Profielramingen zijn niet beschikbaar wanneer regelparameters gegevens bevatten die niet in het profiel staan, zoals contextgegevens. Bijvoorbeeld, een toelatingsregel die het huidige weer om 80 graden vereist te zijn.

1. Klik op **[!UICONTROL Save]** om te bevestigen.

1. Zodra de regel wordt gecreeerd, toont het in **[!UICONTROL Rules]** lijst. U kunt het selecteren om zijn eigenschappen te tonen, en het uitgeven of schrappen.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>Aanbiedingen op basis van gebeurtenissen worden momenteel niet ondersteund in [!DNL Journey Optimizer]. Als u een beslissingsregel maakt op basis van een [event](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"}, je kunt dit object niet gebruiken in een voorstel.

## Video over zelfstudie {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
