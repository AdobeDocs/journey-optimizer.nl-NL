---
title: Rangschikkingsmethoden
description: Leer hoe u met waarderingsmethoden werkt
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Rangschikkingsmethoden {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Rangschikkingsformules maken"
>abstract="Met indelingen kunt u regels definiëren die bepalen welk item als eerste moet worden weergegeven, in plaats van rekening te houden met de prioriteitsscores van het item. Nadat u een waarderingsmethode hebt gemaakt, kunt u deze toewijzen aan een selectiestrategie om te bepalen welke items als eerste moeten worden geselecteerd."

Met behulp van rankeringsmethoden kunt u items voor een bepaald profiel rangschikken. Nadat u een waarderingsmethode hebt gemaakt, kunt u deze toewijzen aan een selectiestrategie om te bepalen welke items als eerste moeten worden geselecteerd.

Er zijn twee typen waarderingsmethoden beschikbaar:

* **Formulas** staat u toe om regels te bepalen die zullen bepalen welk punt eerst, eerder dan rekening houdend met de prioritaire scores van het punt moeten worden voorgesteld.

* **AI modellen** staan u toe om opgeleide modelsystemen te gebruiken die hefboomwerking veelvoudige gegevenspunten zullen bepalen welk punt eerst zou moeten worden voorgesteld.

## Classificatiemethoden maken {#create}

Ga als volgt te werk om een waarderingsmethode te maken:

1. Navigeer naar het menu **[!UICONTROL Strategy setup]** en selecteer vervolgens het menu **[!UICONTROL Formulas]** of **[!UICONTROL AI models]** , afhankelijk van het type positie dat u wilt gebruiken.

1. Klik op de knop **[!UICONTROL Create formula]** of **[!UICONTROL Create AI model]** in de rechterbovenhoek van het scherm.

   ![](assets/ranking-create.png)

1. Configureer de formule of het AI-model naar wens en sla het op.

   Gedetailleerde informatie over het maken van rangschikkingsformules en AI-modellen is beschikbaar in de documentatie van het besluitvormingsbeheer:

   * [Beoordelingsformule](../offers/ranking/create-ranking-formulas.md)
   * [AI-modellen](../offers/ranking/ai-models.md)

   >[!NOTE]
   >
   >De nestdiepte in een rangschikkingsformule is beperkt tot 30 niveaus. Dit wordt gemeten door de `)` haakjes sluiten in de PQL-tekenreeks te tellen. Een regeltekenreeks kan maximaal 8 kB groot zijn voor UTF-8-gecodeerde tekens. Dit komt overeen met 8.000 ASCII-tekens (1 byte elk) of 2.000-4.000 niet-ASCII-tekens (2-4 bytes elk). [ leer meer over het Beslissen van gidsen &amp; beperkingen ](gs-experience-decisioning.md#guardrails)

Een beslissingsbeleid ondersteunt maximaal 10 selectiestrategieën en besluitvormingselementen samen. [ leer meer over het Beslissen van gidsen &amp; beperkingen ](gs-experience-decisioning.md#guardrails)

+++ Modellen optimaliseren op aangepaste [!DNL Customer Journey Analytics] metriek

>[!NOTE]
>
>Deze mogelijkheid is alleen beschikbaar voor [!DNL Customer Journey Analytics] -klanten met beheerdersrechten.
>
>Voordat u begint, moet u ervoor zorgen dat u Journey Optimizer met Customer Journey Analytics hebt geïntegreerd om Journey Optimizer-gegevenssets te exporteren naar uw standaardgegevensweergaven. [ Leer hoe te hefboomwerking  [!DNL Journey Optmizer]  gegevens in  [!DNL Customer Journey Analytics]](../reports/cja-ajo.md)

De gepersonaliseerde optimalisatiemodellen zijn een type van AI model dat u toestaat om bedrijfsdoelstellingen te bepalen en klantengegevens te gebruiken om zaken-georiënteerde modellen op te leiden om gepersonaliseerde aanbiedingen te dienen en KPIs te maximaliseren. De gedetailleerde informatie over hoe te om tot een gepersonaliseerd AI model te leiden is beschikbaar in de [ documentatie van het besluitvormingsbeheer ](../offers/ranking/personalized-optimization-model.md).

Door gebrek, gepersonaliseerde optimalisatiemodellen gebruiken **aanbieding klikt** als optimalisering metrisch. Als u met [!DNL Customer Journey Analytics] werkt, kunt u in [!DNL Decisioning] uw eigen maateenheden gebruiken om uw model te optimaliseren.

U doet dit door het scherm voor het maken van het gepersonaliseerde AI-model te openen en de vervolgkeuzelijst **[!UICONTROL Conversion event]** uit te vouwen. Alle metriek van uw standaard [!DNL Customer Journey Analytics] [ gegevensmening ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"}  vertoning in de lijst. Selecteer de metrische waarde waarop u het model wilt optimaliseren en voltooi vervolgens het maken van het AI-model op de gebruikelijke manier.

![](assets/ai-ranking-custom-metrics.png)

>[!NOTE]
>
>Metrische gegevens in [!DNL Customer Journey Analytics] maken standaard gebruik van een &quot;Last Touch&quot;-attributiemodel, dat 100% van het krediet toewijst aan het aanraakpunt dat het laatst voor de conversie optreedt.
>
>Hoewel het attributiemodel kan worden gewijzigd, zijn niet alle attributiemodellen ideaal voor optimalisatie van het AI-model. We raden u aan zorgvuldig een toewijzingsmodel te selecteren dat is afgestemd op uw optimalisatiedoelstellingen om de nauwkeurigheid en prestaties van het model te garanderen.
>
>Voor meer details op beschikbare attributiemodellen en begeleiding op hun gebruik, verwijs naar de [[!DNL Customer Journey Analytics]  documentatie ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-dataviews/component-settings/attribution){target="_blank"} 

+++

## Kenmerken van besluitvormingsposten in formules gebruiken {#items}

De rangschikkende formules worden uitgedrukt in **syntaxis van PQL** en kunnen hefboomwerking diverse attributen zoals profielattributen, [ contextgegevens ](context-data.md) en attributen met betrekking tot uw besluitvormingspunten.

Om attributen met betrekking tot uw beslissingspunten in formules te hefboomwerking, zorg ervoor u de syntaxis hieronder in de code van uw rangschikkende formule volgt. Breid elke sectie voor meer informatie uit:

+++Standaardeigenschappen van besluitvormingsposten voor hefboomwerking

![](assets/formula-attribute.png)

+++

+++Aangepaste kenmerken van besluitvormingspunten voor hefboomwerking

![](assets/formula-attribute-custom.png)

+++
