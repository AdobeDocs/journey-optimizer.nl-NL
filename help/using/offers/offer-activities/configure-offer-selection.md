---
title: Selectie van aanbiedingen in beslissingen configureren
description: Leer hoe u de selectie van aanbiedingen kunt beheren in beslissingen
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: f2174848c70610fc543ea9ddf766f0f7e579053a
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 5%

---

# Selectie van aanbiedingen in beslissingen configureren {#offers-selection-in-decisions}

Als verscheidene aanbiedingen voor een bepaalde plaatsing verkiesbaar zijn, kunt u de methode kiezen die de beste aanbieding voor elk profiel zal selecteren wanneer het vormen van een besluit. Je kunt voorstellen plaatsen op:
* Voorstelprioriteit
* Willekeurige formule
* [AI-rangschikking](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## Voorstelprioriteit {#offer-priority}

Wanneer meerdere aanbiedingen in aanmerking komen voor een bepaalde plaatsing in een besluit, worden standaard de aanbiedingen met de hoogste **prioriteit** wordt eerst aan de klanten geleverd.

![](../assets/offer-priority.png)

De prioritaire scores van aanbiedingen worden toegewezen wanneer het creëren van een aanbieding. Leer hoe u een persoonlijke aanbieding kunt maken in [deze sectie](../offer-library/creating-personalized-offers.md).

## Willekeurige formule {#assign-ranking-formula}

Met Journey Optimizer kunt u niet alleen prioriteit bieden, maar ook **rangschikkingsformules**. Dit zijn formules die bepalen welke aanbieding eerst voor een bepaalde plaatsing moet worden gepresenteerd, in plaats van rekening te houden met de prioriteitsscores van de aanbiedingen.

U kunt bijvoorbeeld de prioriteit verhogen van alle aanbiedingen met een einddatum van minder dan 24 uur, of aanbiedingen verhogen van de categorie &quot;actief&quot; als het interessepunt van het profiel &quot;actief&quot; is.

Leer hoe u een waarderingsformule maakt in [deze sectie](../ranking/create-ranking-formulas.md).

Nadat een formule is gemaakt, kunt u deze toewijzen aan een plaatsing in een beslissing. Volg de onderstaande stappen om dit te doen:

1. Maak een beslissing of bewerk een bestaande beslissing. Zie [Besluiten maken](../offer-activities/create-offer-activities.md).

1. Voeg de plaatsingen toe die uw voorstellen zullen bevatten. Zie [Plaatsen maken](../offer-library/creating-placements.md).

1. Voeg voor elke plaatsing een verzameling toe. Zie [Verzamelingen maken](../offer-library/creating-collections.md).

1. Selecteren **[!UICONTROL Formula]** als de waarderingsmethode klikt u op **[!UICONTROL Add ranking]**.

   ![](../assets/offer-activity-ranking.png)

1. Selecteer de gewenste formule en klik op **[!UICONTROL Select]**.

   ![](../assets/ranking-selection.png)

De rangschikkingsformule is nu gekoppeld aan de plaatsing.

Als meerdere aanbiedingen in aanmerking komen om in deze plaatsing te worden gepresenteerd, wordt in de beslissing de geselecteerde formule gebruikt om te berekenen welke aanbieding het eerst wordt geleverd.

## AI-rangschikking {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

U kunt ook een getraind modelsysteem gebruiken dat aanbiedingen voor een bepaald profiel automatisch rangschikt door een AI-model te selecteren. Leer hoe u een AI-model maakt in [deze sectie](../ranking/create-ranking-strategies.md).

Nadat u een AI-model hebt gemaakt, kunt u het toewijzen aan een plaatsing in een beslissing. Hiervoor voert u de volgende stappen uit:

1. Maak een beslissing of bewerk een bestaande beslissing. Zie [Besluiten maken](../offer-activities/create-offer-activities.md).

1. Voeg de plaatsingen toe die uw voorstellen zullen bevatten. Zie [Plaatsen maken](../offer-library/creating-placements.md).

1. Voeg voor elke plaatsing een verzameling toe. Zie [Verzamelingen maken](../offer-library/creating-collections.md).

1. Kies ervoor om voorstellen te plaatsen op **[!UICONTROL AI ranking]** in de vervolgkeuzelijst en klik op **[!UICONTROL Add ranking]**.

   ![](../assets/ranking-selection-ai-ranking.png)

1. Selecteer het AI-model dat u hebt gemaakt. Alle details van het model worden weergegeven.

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. Klik op **[!UICONTROL Select]**. Het AI-model is nu gekoppeld aan de plaatsing.

Indien meerdere aanbiedingen in aanmerking komen, bepaalt het opgeleide modelsysteem welke aanbieding eerst voor een bepaalde plaatsing moet worden gepresenteerd.

