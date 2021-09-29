---
title: Selectie van aanbiedingen in beslissingen configureren
description: Leer hoe u de selectie van aanbiedingen kunt beheren in beslissingen.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 7%

---

# Selectie van aanbiedingen in beslissingen configureren {#offers-selection-in-activities}

Als verscheidene aanbiedingen voor een bepaalde plaatsing verkiesbaar zijn, kunt u de methode kiezen die de beste aanbieding voor elk profiel zal selecteren wanneer het vormen van een besluit (eerder genoemd als aanbiedingsactiviteit). Je kunt voorstellen plaatsen op:
* Voorstelprioriteit
* Willekeurige formule
* [AI-classificatie](#use-ranking-strategy)  (alleen voor bepaalde gebruikers in eerste instantie)

![](../../assets/offer-rank-by.png)

## Voorstelprioriteit {#about-offers-priority}

Wanneer meerdere aanbiedingen in aanmerking komen voor een bepaalde plaatsing in een beslissing (voorheen bekend als aanbiedingsactiviteit), worden de aanbiedingen met de hoogste **prioriteit** standaard eerst aan de klanten geleverd.

![](../../assets/offer-priority.png)

De prioritaire scores van aanbiedingen worden toegewezen wanneer het creëren van een aanbieding. Leer hoe u een gepersonaliseerde aanbieding maakt in [deze sectie](../offer-library/creating-personalized-offers.md).

## Willekeurige formule {#assign-ranking-formula}

Naast het aanbieden van prioriteit, staat Journey Optimizer u toe om **rangschikkende formules te creëren**. Dit zijn formules die bepalen welke aanbieding eerst voor een bepaalde plaatsing moet worden gepresenteerd, in plaats van rekening te houden met de prioriteitsscores van de aanbiedingen.

U kunt bijvoorbeeld de prioriteit verhogen van alle aanbiedingen met een einddatum van minder dan 24 uur, of aanbiedingen verhogen van de categorie &quot;actief&quot; als het interessepunt van het profiel &quot;actief&quot; is.

Leer hoe u een rangschikkingsformule maakt in [deze sectie](../offer-library/create-ranking-formulas.md).

Zodra een rangschikkende formule is gecreeerd, kunt u het aan een plaatsing in een besluit (dat vroeger als aanbiedingsactiviteit wordt bekend) toewijzen. Volg de onderstaande stappen om dit te doen:

1. Maak een beslissing of bewerk een bestaande beslissing. Zie [Besluiten maken](../offer-activities/create-offer-activities.md).

1. Voeg de plaatsingen toe die uw voorstellen zullen bevatten. Zie [Plaatsen maken](../offer-library/creating-placements.md).

1. Voeg voor elke plaatsing een verzameling toe. Zie [Verzamelingen maken](../offer-library/creating-collections.md).

1. Kies ervoor aanbiedingen te rangschikken op **[!UICONTROL Ranking]** in de vervolgkeuzelijst en klik vervolgens op **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

1. Selecteer de gewenste rangschikkingsformule en klik op **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

De rangschikkingsformule is nu gekoppeld aan de plaatsing.

Indien meerdere aanbiedingen in aanmerking komen om in deze plaatsing te worden gepresenteerd, wordt in het besluit de formule van de rangorde gebruikt om te berekenen welke aanbieding het eerst wordt geleverd.

## AI-rangschikking {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can also use an trained model system that automatically ranks offers to display for a given profile by selecting a ranking strategy. Learn how to create a ranking strategy in [this section](../offer-library/create-ranking-strategies.md).

>[!CAUTION]
>
>Het gebruik van de AI-rangschikking is momenteel beschikbaar in een vroeg stadium en alleen voor bepaalde gebruikers.

Zodra een rangschikkingsstrategie is gecreeerd, kunt u het aan een plaatsing in een besluit (dat vroeger als aanbiedingsactiviteit wordt bekend) toewijzen. Hiervoor voert u de volgende stappen uit:

1. Maak een beslissing of bewerk een bestaande beslissing. Zie [Besluiten maken](../offer-activities/create-offer-activities.md).

1. Voeg de plaatsingen toe die uw voorstellen zullen bevatten. Zie [Plaatsen maken](../offer-library/creating-placements.md).

1. Voeg voor elke plaatsing een verzameling toe. Zie [Verzamelingen maken](../offer-library/creating-collections.md).

1. Kies ervoor aanbiedingen te rangschikken op **[!UICONTROL AI ranking]** in de vervolgkeuzelijst.

   ![](../../assets/ranking-selection-ai-ranking.png)

1. Klik op **[!UICONTROL Add ranking]**.

   ![](../../assets/ranking-selection-ai-ranking-add.png)

1. Selecteer de waarderingsstrategie die u hebt gemaakt. Alle details van de classificatiestrategie worden weergegeven.

   ![](../../assets/ranking-selection-ai-ranking-selected.png)

1. Klik op **[!UICONTROL Select]**.

De rangschikkingsstrategie is nu gekoppeld aan de plaatsing.

Indien meerdere aanbiedingen in aanmerking komen, bepaalt het opgeleide modelsysteem welke aanbieding eerst voor een bepaalde plaatsing moet worden gepresenteerd.

<!--Result? Describe the impact for the user, i.e. what's the effect of selecting this ranking strategy for this collection/placement.-->

<!--Click **[!UICONTROL Next]** to confirm and save your decision.-->
