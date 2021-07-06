---
title: Selectie van aanbiedingen in beslissingen configureren
description: Leer hoe u de selectie van aanbiedingen kunt beheren in beslissingen.
feature: Aanbiedingen
topic: Integraties
role: User
level: Intermediate
source-git-commit: a25264cb43f77671c29f18522110fd85d0155697
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 7%

---

# Selectie van aanbiedingen in beslissingen configureren {#offers-selection-in-activities}

## Over de prioriteit Aanbiedingen {#about-offers-priority}

Wanneer meerdere aanbiedingen in aanmerking komen voor een bepaalde plaatsing in een beslissing (voorheen bekend als aanbiedingsactiviteit), worden de aanbiedingen met de hoogste **prioriteit** standaard eerst aan de klanten geleverd. De prioritaire scores van aanbiedingen worden toegewezen wanneer het creëren van een aanbieding (zie [een gepersonaliseerde aanbieding](../offer-library/creating-personalized-offers.md) creëren).

![](../../assets/offer-priority.png)

Bovendien, staat Journey Optimizer u toe om **rangschikkende formules** tot stand te brengen. Dit zijn formules die bepalen welke aanbieding eerst voor een bepaalde plaatsing moet worden gepresenteerd, in plaats van rekening te houden met de prioriteitsscores van de aanbiedingen.

U kunt bijvoorbeeld de prioriteit verhogen van alle aanbiedingen met een einddatum van minder dan 24 uur, of aanbiedingen verhogen van de categorie &quot;actief&quot; als het interessepunt van het profiel &quot;actief&quot; is.

Raadpleeg [deze sectie](../offer-library/create-ranking-formulas.md) voor meer informatie over het maken van een rangschikkingsformule.

## Een waarderingsformule toewijzen aan een plaatsing {#assign-ranking-formula}

Nadat u een rangschikkingsformule hebt gemaakt, kunt u deze toewijzen aan een plaatsing in een beslissing. Volg de onderstaande stappen om dit te doen:

1. Maak een beslissing of bewerk een bestaande beslissing en maak vervolgens de plaatsingen waarin uw aanbiedingen staan (zie [Besluiten maken](../offer-activities/create-offer-activities.md)).

1. Selecteer **[!UICONTROL Ranking]** in de vervolgkeuzelijst voor elke plaatsing.

1. Klik op **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

1. Selecteer de gewenste rangschikkingsformule en klik op **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

De rangschikkingsformule is nu gekoppeld aan de plaatsing.

Indien meerdere aanbiedingen in aanmerking komen om in deze plaatsing te worden gepresenteerd, wordt in het besluit de formule van de rangorde gebruikt om te berekenen welke aanbieding het eerst wordt geleverd.
