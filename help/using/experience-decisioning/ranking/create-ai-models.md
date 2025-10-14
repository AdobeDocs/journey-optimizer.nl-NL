---
product: experience platform
solution: Experience Platform
title: AI-modellen maken
description: Leer hoe u AI-modellen maakt om aanbiedingen te beoordelen
feature: Ranking, Decision Management
role: User
level: Intermediate
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 1%

---

# AI-modellen maken {#create-ai-models}

[!DNL Journey Optimizer] laat u toe om **AI modellen** tot stand te brengen om aanbiedingen te rangschikken die op uw bedrijfsdoelstellingen worden gebaseerd.

>[!CAUTION]
>
>Om, AI modellen tot stand te brengen uit te geven of te schrappen, moet u **het Rangschikken van Strategieën** toestemming hebben leiden. [Meer informatie](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Een AI-model maken {#create-ranking-strategy}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_metric"
>title="Optimalisatiemetrisch"
>abstract="[!DNL Journey Optimizer] rangschikt aanbiedingen die op het **worden gebaseerd omzettingspercentage** (het tarief van de Omzetting = Totaal aantal omzettingsgebeurtenissen/Totaal aantal impressiegebeurtenissen). De omzettingspercentage wordt berekend gebruikend twee types van metriek: **de gebeurtenissen van de Impressie** (aanbiedingen die worden getoond) en **de gebeurtenissen van de Omzetting** (aanbiedingen die in kliks via e-mail of Web) resulteren. Deze gebeurtenissen worden automatisch vastgelegd met de Web SDK of de Mobile SDK die is opgegeven."

Voer de volgende stappen uit om een AI-model te maken:

1. Maak een gegevensset waarin conversiegebeurtenissen worden verzameld. [&#x200B; leer hoe &#x200B;](../data-collection/create-dataset.md)

1. Ga naar het menu **[!UICONTROL Decisioning]** > **[!UICONTROL Strategy setup]** en selecteer **[!UICONTROL AI models]** .

   ![](../assets/ai-model-list.png)

   Alle tot nu toe gemaakte AI-modellen worden vermeld.

1. Klik op de knop **[!UICONTROL Create AI model]**.

1. Geef een unieke naam op en indien nodig een beschrijving voor het AI-model.

1. Selecteer het type AI-model dat u wilt maken:

   * **[!UICONTROL Auto-optimization]** optimaliseert aanbiedingen op basis van de prestaties van eerdere aanbiedingen. [Meer informatie](auto-optimization-model.md)
   * **[!UICONTROL Personalized optimization]** optimaliseert en personaliseert aanbiedingen op basis van publiek en biedt prestaties. [Meer informatie](personalized-optimization-model.md)

   ![](../assets/ai-model-types.png)

1. Het gedeelte **[!UICONTROL Optimization metric]** bevat informatie over de conversiegebeurtenis die door het AI-model wordt gebruikt om de rangorde van aanbiedingen te berekenen.

   [!DNL Journey Optimizer] rangschikt aanbiedingen die op het **worden gebaseerd omzettingspercentage** (het tarief van de Omzetting = Totaal aantal omzettingsgebeurtenissen/Totaal aantal impressiegebeurtenissen). De conversiesnelheid wordt berekend aan de hand van twee soorten meetwaarden:
   * **de gebeurtenissen van de Indrukking** (aanbiedingen die worden getoond)
   * **de gebeurtenissen van de Omzetting** (aanbiedingen die in kliks via e-mail of Web) resulteren.

   Deze gebeurtenissen worden automatisch vastgelegd met de Web SDK of de Mobile SDK die is opgegeven. Leer meer in het [&#128279;](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=nl-NL) overzicht van SDK van het Web 0&rbrace; Adobe Experience Platform.

+++ Modellen optimaliseren op aangepaste [!DNL Customer Journey Analytics] metriek

   >[!NOTE]
   >
   >Deze mogelijkheid is alleen beschikbaar voor [!DNL Customer Journey Analytics] -klanten met beheerdersrechten.
   >
   >Voordat u begint, moet u ervoor zorgen dat u Journey Optimizer met Customer Journey Analytics hebt geïntegreerd om Journey Optimizer-gegevenssets te exporteren naar uw standaardgegevensweergaven. [&#x200B; Leer hoe te hefboomwerking  [!DNL Journey Optmizer]  gegevens in  [!DNL Customer Journey Analytics]](../../reports/cja-ajo.md)

   **[!UICONTROL Personalized optimization]** modellen zijn een type van AI model dat u toestaat om bedrijfsdoelstellingen te bepalen en klantengegevens te gebruiken om zaken-georiënteerde modellen op te leiden om gepersonaliseerde aanbiedingen te dienen en KPIs te maximaliseren.

   Door gebrek, gepersonaliseerde optimalisatiemodellen gebruiken **aanbieding klikt** als optimalisering metrisch. Als u met [!DNL Customer Journey Analytics] werkt, kunt u in [!DNL Decisioning] uw eigen maateenheden gebruiken om uw model te optimaliseren.

   Selecteer hiertoe het modeltype **[!UICONTROL Personalized optimization]** en vouw de vervolgkeuzelijst **[!UICONTROL Conversion event]** uit. Alle metriek van uw standaard [!DNL Customer Journey Analytics] [&#x200B; gegevens bekijken &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"} vertoning in de lijst. Selecteer metrisch dat u uw model wilt optimaliseren.

   ![](../assets/ai-model-custom-metrics.png){width=85%}

   >[!NOTE]
   >
   >Metrische gegevens in [!DNL Customer Journey Analytics] maken standaard gebruik van een &quot;Last Touch&quot;-attributiemodel, dat 100% van het krediet toewijst aan het aanraakpunt dat het laatst voor de conversie optreedt.
   >
   >Hoewel het attributiemodel kan worden gewijzigd, zijn niet alle attributiemodellen ideaal voor optimalisatie van het AI-model. We raden u aan zorgvuldig een toewijzingsmodel te selecteren dat is afgestemd op uw optimalisatiedoelstellingen om de nauwkeurigheid en prestaties van het model te garanderen.
   >
   >Voor meer details op beschikbare attributiemodellen en begeleiding op hun gebruik, verwijs naar de [[!DNL Customer Journey Analytics]  documentatie &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-dataviews/component-settings/attribution){target="_blank"}

+++

1. Selecteer de gegevensset(s) waar de conversie- en impressiefeedagen worden verzameld. Leer hoe te om dergelijke datasets in [&#x200B; tot stand te brengen deze sectie &#x200B;](../data-collection/create-dataset.md).

   ![](../assets/ai-model-datasets.png){width=85%}

   >[!CAUTION]
   >
   >Alleen de gegevenssets die zijn gemaakt op basis van schema&#39;s die zijn gekoppeld aan de **[!UICONTROL Experience Event - Proposition Interactions]** -veldgroep (voorheen bekend als mixin), worden weergegeven in de vervolgkeuzelijst.

1. Als u een **[!UICONTROL Personalized optimization]** AI-model maakt, selecteert u het segment dat u wilt gebruiken om het AI-model te trainen.

   <!--➡️ [Discover this feature in video](#video)-->

   >[!NOTE]
   >
   >U kunt maximaal vijf soorten publiek selecteren.

1. Sla het AI-model op en activeer het.

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

Nu telkens als een aanbieding wordt getoond en/of geklikt, wilt u de overeenkomstige gebeurtenis automatisch worden gevangen door de **[!UICONTROL Experience Event - Proposition Interactions]** gebiedsgroep gebruikend het [&#x200B; Web SDK van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=nl-NL#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} of Mobiele SDK.

Als u gebeurtenistypen wilt kunnen verzenden (weergegeven aanbod of aangeklikte aanbieding), moet u de juiste waarde voor elk gebeurtenistype instellen in een ervaringsgebeurtenis die naar Adobe Experience Platform wordt verzonden. [&#x200B; leer hoe &#x200B;](../data-collection/schema-requirement.md)

<!--
## How-to video {#video}

Learn how to create a personalized optimization model and how to apply it to a decision.

>[!VIDEO](https://video.tv.adobe.com/v/3445957?quality=12&captions=dut)-->
