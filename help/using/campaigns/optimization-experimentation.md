---
solution: Journey Optimizer
product: journey optimizer
title: Gebruik experimenteren met berichtoptimalisatie
description: Leer hoe u experimenten met inhoud kunt gebruiken om meerdere versies van inhoud te testen en te bepalen welke het beste presteert.
role: User
level: Intermediate
keywords: experimenteren, optimaliseren, A/B testen, content experimenteren, behandelingen
source-git-commit: fec72c63d41a41adce5107082c50a68a7b8c0af2
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Gebruik experimenteren {#experimentation}

>[!NOTE]
>
>Deze pagina biedt een overzicht van het gebruik van experimenten bij het optimaliseren van inhoud. Voor gedetailleerde informatie over inhoudexperimenten, met inbegrip van configuratieopties, metriek, en analyse, zie de [&#x200B; documentatie van het inhoudexperiment &#x200B;](../content-management/get-started-experiment.md).

Met behulp van experimenten kunt u meerdere versies van de inhoud testen om te bepalen wat het beste werkt op basis van vooraf gedefinieerde succeswaarden.

Volg onderstaande stappen om experimenten in te stellen.

Stel dat u de volgende promotieberichten in een campagne wilt testen:

* **Behandeling A**: &quot;20% van uw volgende aankoop&quot;
* **Behandeling B**: &quot;Vrije verschepen op orden boven $50&quot;
* **Behandeling C**: &quot;Krijg uw $10 geschenkkaart&quot;

Volg de onderstaande stappen om experimenten in te stellen en te bepalen welk bericht de meeste aankopen aanstuurt.

1. Creeer a [&#x200B; reis &#x200B;](../building-journeys/journey-gs.md#jo-build) of a [&#x200B; campagne &#x200B;](../campaigns/create-campaign.md).

   >[!NOTE]
   >
   >Als u onderweg bent, voegt u een **[!UICONTROL Action]** -activiteit toe, kiest u een kanaalactiviteit en selecteert u **[!UICONTROL Configure action]** . [Meer informatie](../building-journeys/journey-action.md#add-action)

1. Van het **[!UICONTROL Actions]** lusje, selecteer twee binnenkomende acties, bijvoorbeeld [&#x200B; code-gebaseerde ervaring &#x200B;](../code-based/get-started-code-based.md) en [&#x200B; in-app &#x200B;](../../rp_landing_pages/in-app-landing-page.md).

1. Selecteer **[!UICONTROL Optimization]** in de sectie **[!UICONTROL Create experiment]** .

   ![](assets/msg-optimization-select-experiment.png){width=85%}

1. Ontwerp en configureer uw content-experiment naar wens. [&#x200B; leer hoe &#x200B;](../content-management/content-experiment.md)

   ![](assets/msg-optimization-create-experiment.png){width=85%}

   Zodra het experiment is gedefinieerd, is het van toepassing op alle acties die in die campagne of door de reis **[!UICONTROL Action]** activiteit worden opgenomen, wat betekent dat dezelfde klanten dezelfde aanbiedingen op alle oppervlakken zien.

   >[!NOTE]
   >
   >U kunt andere acties selecteren: de experimentatie is op alle acties van toepassing die aan de campagne of aan de activiteit van de reis [&#x200B; Actie &#x200B;](../building-journeys/journey-action.md) worden toegevoegd.

1. [&#x200B; activeer &#x200B;](review-activate-campaign.md) uw reis of campagne.

Zodra de reis/de campagne levend is, worden de gebruikers willekeurig toegewezen de verschillende inhoudvariaties. [!DNL Journey Optimizer] houdt bij welke variatie meer aankopen drijft en actioneerbare inzichten verstrekt.

Volg het succes van uw campagne met de [&#x200B; reis &#x200B;](../reports/journey-global-report-cja.md) en [&#x200B; campagne &#x200B;](../reports/campaign-global-report-cja-experimentation.md) rapporten. <!--Link to Experimentation journey reportis missing-->

