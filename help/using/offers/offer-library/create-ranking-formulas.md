---
title: Rangschikkingsformules maken
description: Leer hoe u rangschikkingsformules maakt in Adobe Experience Platform.
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---

# Rangschikkingsformules maken {#create-ranking-formulas}

## Informatie over rangschikkingsformules {#about-ranking-formulas}

**Met behulp van** rangschikkingsformules kunt u regels definiëren die bepalen welke aanbieding eerst voor een bepaalde plaatsing moet worden gepresenteerd, in plaats van rekening te houden met de prioriteitsscores van de aanbiedingen.

Rangschikkingsformules worden uitgedrukt in **PQL-syntaxis** en kunnen profielkenmerken, contextgegevens en kenmerken gebruiken. Raadpleeg de [speciale documentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html) voor meer informatie over het gebruik van de PQL-syntaxis.

Zodra een rangschikkende formule is gecreeerd, kunt u het aan een plaatsing in een besluit (dat vroeger als aanbiedingsactiviteit wordt bekend) toewijzen. Voor meer op dit, zie [Vorm aanbiedingen selectie in besluiten](../offer-activities/configure-offer-selection.md).

## Een waarderingsformule {#create-ranking-formula} maken

Voer de volgende stappen uit om een rangschikkingsformule te maken:

* Open het menu **[!UICONTROL Components]** en selecteer vervolgens het tabblad **[!UICONTROL Rankings]**.

* Klik **[!UICONTROL Create formula]** om een nieuwe rangschikkingsformule tot stand te brengen.

   ![](../../assets/ranking-create-formula.png)

* Geef de naam, beschrijving en formule van de waarderingsformule op.

   In dit voorbeeld willen we de prioriteit van alle aanbiedingen verhogen met het kenmerk &quot;hot&quot; als het werkelijke weer heet is. Om dit te doen, **contextData.wind=hot** werd overgegaan in de beslissingsvraag.

   ![](../../assets/ranking-syntax.png)

* Klik op **[!UICONTROL Save]**. Uw rangschikkingsformule wordt gecreeerd, kunt u het van de lijst selecteren om details te krijgen en het uit te geven of te schrappen.

   Het is nu klaar om in een besluit worden gebruikt om in aanmerking komende aanbiedingen voor een plaatsing te rangschikken (zie [Aanbiedingen selecteren in besluiten vormen](../offer-activities/configure-offer-selection.md)).

   ![](../../assets/ranking-formula-created.png)
