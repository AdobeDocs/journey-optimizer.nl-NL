---
title: Selectie van aanbiedingen in beslissingen configureren
description: Leer hoe u de selectie van aanbiedingen kunt beheren in beslissingen.
feature: Aanbiedingen
topic: Integraties
role: User
level: Intermediate
source-git-commit: 3db5756236b6ac05d9b95b8b051dd99dc7d5cf7e
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 5%

---

# Selectie van aanbiedingen in beslissingen configureren {#offers-selection-in-activities}

Als verscheidene aanbiedingen voor een bepaalde plaatsing verkiesbaar zijn, kunt u de methode kiezen die de beste aanbieding voor elk profiel zal selecteren wanneer het vormen van een besluit (eerder genoemd als aanbiedingsactiviteit). Je kunt voorstellen plaatsen op:
* Voorstelprioriteit
* Willekeurige formule

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
