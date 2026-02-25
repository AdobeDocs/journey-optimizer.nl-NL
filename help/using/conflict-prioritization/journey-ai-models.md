---
title: Reisarbitrage AI-modellen
description: Leer hoe u AI-modellen maakt en gebruikt om reizen voor arbitrage te classificeren. De beste reis wordt dus per profiel geselecteerd op basis van AI-scores.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Beperkte beschikbaarheid" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# AI-modellen gebruiken om reizen te rangschikken {#journey-ai-models}

>[!AVAILABILITY]
>
>Deze functie bevindt zich momenteel in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

Met [!DNL Adobe Journey Optimizer] kunt u bepalen welke ritten een profiel kan invoeren wanneer ze in aanmerking komen voor meer dan het systeem toestaat. Om dit te doen, kunt u [&#x200B; regelreeksen &#x200B;](rule-sets.md) gebruiken om caps op reisingang of gelijktijdig te bepalen. Wanneer een profiel voor meer reizen in aanmerking komt dan het maximum toestaat, bepaalt de prioriteit die aan elke reis wordt toegekend welke ritten worden gekozen.

In plaats van het gebruiken van prioriteit of rangschikkende formules, kunt u **modellen AI** gebruiken om reizen dynamisch te rangschikken die op getrainde modelscores worden gebaseerd. U kunt AI-modellen maken vanuit de sectie **[!UICONTROL Orchestration ranking]** in de gebruikersinterface en deze gebruiken in regelsets om deze toe te passen op reizen.

Voor een overzicht van AI modeltypes beschikbaar in [!DNL Journey Optimizer], zie [&#x200B; begonnen worden met AI modellen &#x200B;](../experience-decisioning/ranking/ai-models.md#ai-model-types) in de Beslissende sectie.

## Een AI-model maken {#create-ai-model}

>[!CAUTION]
>
>Om, AI modellen tot stand te brengen uit te geven of te schrappen, moet u **het Rangschikken van Strategieën** toestemming hebben leiden. [Meer informatie](../administration/high-low-permissions.md#manage-ranking-strategies)

Volg de onderstaande stappen om een AI-model voor de rangschikking van reizen te maken.

1. Maak een gegevensset waarin conversiegebeurtenissen worden verzameld. [&#x200B; leer hoe &#x200B;](../experience-decisioning/data-collection/create-dataset.md)

1. Open de sectie **[!UICONTROL Orchestration ranking]** en selecteer vervolgens de tab **[!UICONTROL AI models]** . De lijst met eerder gemaakte AI-modellen wordt weergegeven.

1. Klik op **[!UICONTROL Create AI model]**.

1. Geef een unieke naam en, indien nodig, een beschrijving voor het AI-model op.

   ![&#x200B; AI de ruit van modeldetails met naam en beschrijvingsgebieden &#x200B;](assets/journey-model-details.png){width="80%"}

   >[!NOTE]
   >
   >Het rangschikkende object is de entiteit waarop de rangschikkingsformule van toepassing is. Standaard is de positie van het waarderingsobject ingesteld op **[!UICONTROL Journey]** .

<!--
1. Select the type of AI model you want to create:

    * **[!UICONTROL Auto-optimization]** optimizes based on past performance. [Learn more](../experience-decisioning/ranking/auto-optimization-model.md)
    * **[!UICONTROL Personalized optimization]** optimizes and personalizes based on audiences and performance. [Learn more](../experience-decisioning/ranking/personalized-optimization-model.md)-->

1. De sectie **[!UICONTROL Optimization metric]** bevat informatie over de conversiegebeurtenis die door het AI-model wordt gebruikt. [!DNL Journey Optimizer] ranks die op het **worden gebaseerd omzettingspercentage** (het tarief van de Omzetting = Totaal aantal omzettingsgebeurtenissen/Totaal aantal impressiegebeurtenissen). De omrekeningskoers wordt berekend aan de hand van:

   * **de gebeurtenissen van de Indrukking** (punten die worden getoond)
   * **de gebeurtenissen van de Omzetting** (punten die in kliks of omzettingen resulteren)

   Deze gebeurtenissen worden automatisch vastgelegd met de Web SDK of de Mobile SDK. Leer meer in het [&#x200B; overzicht van SDK van het Web 0&rbrace; Adobe Experience Platform.](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=nl-NL)

1. Selecteer de gegevensset(s) waar de conversie- en impressiefeedagen worden verzameld. Leer hoe te om dergelijke datasets in [&#x200B; tot stand te brengen deze sectie &#x200B;](../experience-decisioning/data-collection/create-dataset.md).

   ![&#x200B; de selectie van de Dataset voor omzetting en impressiegerelateerde gebeurtenissen &#x200B;](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >Alleen de gegevenssets die zijn gemaakt op basis van schema&#39;s die zijn gekoppeld aan de **[!UICONTROL Experience Event - Proposition Interactions]** -veldgroep (voorheen bekend als mixin), worden weergegeven in de vervolgkeuzelijst.

1. &#x200B;<!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->Selecteer de segmenten die u wilt gebruiken om het AI-model op te leiden.

   >[!NOTE]
   >
   >U kunt maximaal vijf soorten publiek selecteren.

1. Sla het AI-model op en activeer het.

Het AI model is nu beschikbaar wanneer u een regelreeks vormt.

## Het AI-model toewijzen aan een regelset {#assign-ai-model-to-ruleset}

Als u een AI-model wilt gebruiken om uw reizen te rangschikken, moet u het gebruiken in een formule en deze formule toewijzen aan een regelset.

1. Maak een waarderingsformule met het door u gemaakte AI-model. [&#x200B; leer hoe &#x200B;](journey-ranking-formulas.md#create-journey-ranking-formula)

1. Maak in het menu **[!UICONTROL Business rules]** een regelset die u wilt gebruiken voor arbitrage tijdens de rit. [&#x200B; leer hoe &#x200B;](rule-sets.md#Create)

1. Selecteer het domein **[!UICONTROL Journey]** .

1. Stel in de regelseteigenschappen de waarde **[!UICONTROL Ranking method]** in op **[!UICONTROL Formula]** (in plaats van **[!UICONTROL Priority]** ).

1. Selecteer de formule die het AI model gebruikt dat u van de drop-down lijst creeerde.

1. Maak de regels voor het afdekken van de verplaatsingen die u aan de regelset wilt toevoegen. [&#x200B; leer hoe &#x200B;](journey-capping.md#create-rule)

1. Sla de regelset op.

De formule die het AI-model gebruikt, wordt nu toegewezen aan de regelset. Vervolgens kunt u die regel op uw reizen toepassen.

## Pas de regel toe die op een reis is ingesteld {#assign-rule-set-to-journey}

Volg de onderstaande stappen om de regel toe te wijzen die aan een reis is ingesteld.

1. Maak of open de reis waaraan u de regel wilt toewijzen. [&#x200B; leer hoe te om een reis &#x200B;](../building-journeys/journey-gs.md) tot stand te brengen

1. Selecteer in de reiseigenschappen de regelset in de vervolgkeuzelijst. [&#x200B; leer hoe &#x200B;](journey-capping.md#apply-capping).

   >[!NOTE]
   >
   >Er kan slechts één regelset tegelijk op een reis worden toegepast.

1. Bespaar de reis.

Alle ritten die van deze regel gebruikmaken, worden bij toepassing van de lampvoet gerangschikt met de geselecteerde formule aan de hand van het AI-model.
