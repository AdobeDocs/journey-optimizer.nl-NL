---
solution: Journey Optimizer
product: journey optimizer
title: Campagne Global-rapport
description: Leer hoe u gegevens uit het rapport Campagne Global kunt gebruiken
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: ec1af88c-7b0a-4eaf-97e1-0d9676268fed
badge: label="Beta" type="Informative"
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 2%

---

# Globaal verslag campagne voeren {#objective-report}

Via de knop **[!UICONTROL View report]** hebt u rechtstreeks vanuit uw campagne toegang tot het algemene rapport van de campagne.

De campagne **[!UICONTROL Global report]** is verdeeld in verschillende widgets waarin het succes van uw campagne en de fouten worden beschreven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Raadpleeg deze <!--[section](../reports/global-report.md#modify-dashboard)--> voor meer informatie hierover.

Raadpleeg <!--[this page](global-report.md#list-of-components-global.md)--> voor een gedetailleerde lijst met alle beschikbare metrische informatie in Adobe Journey Optimizer.

## Tabblad Campagne {#campaign-global-objectives}

### Levering {#delivery-global-objectives}

<!--
![](assets/campaign_report_global_1.png)
-->

De **[!UICONTROL Campaign's Statistics]** -widget geeft de belangrijkste informatie met betrekking tot uw campagne:

* **[!UICONTROL Entered profiles]**: Aantal profielen dat de rit is gestart.

* **[!UICONTROL Actions delivered]**: Het totale aantal unieke tijden dat een handeling in de reis is uitgevoerd.

* **[!UICONTROL Actions failed in %]**: Het totale aantal unieke tijden dat een actie tijdens de reis is mislukt in verhouding tot het totale aantal unieke tijden dat een actie is uitgevoerd.

### Doelstellingen {#objective-global}

>[!AVAILABILITY]
>
>De **eigenschap van het het rapport van Doelstellingen** is momenteel slechts beschikbaar voor een reeks organisaties (Beperkte Beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

![](assets/performance_report.gif)

Op het tabblad **[!UICONTROL Objectives]** kunt u de rapporten van uw leveringen perfectioneren door een specifieke meting uit te voeren.

De lijst **[!UICONTROL Objectives]** is gekoppeld aan **[!UICONTROL Datasets]** die een verbinding met een systeem definiëren om aanvullende informatie op te halen. Er is een lijst met ingebouwde **[!UICONTROL Objectives]** beschikbaar, maar u kunt uw eigen lijst toevoegen door nieuwe **[!UICONTROL Dataset]** toe te voegen. Voor de gedetailleerde procedure, verwijs naar deze [ sectie ](../reports/reporting-configuration.md).

Nadat u de doelstellingen hebt geselecteerd waarop u zich wilt richten, geven de twee **[!UICONTROL Performance overview]** - en **[!UICONTROL Campaign objective]** -widgets een gedetailleerd overzicht van de prestaties van de levering.

Met de **[!UICONTROL Campaign objective]** -widget kunt u er ook voor kiezen om uw hoofddoel te vergelijken met een andere metrische waarde.

### Experimentatierapport {#experimentation-global-objectives}

<!--
![](assets/experimentation_report_3.png)
-->

Het tabblad **[!UICONTROL Experimentation]** biedt belangrijke inzichten in de prestaties van elke variant en identificeert de meest succesvolle variant.

Het kan enige tijd duren om de beste uitvoerder te definiëren. Dit wordt aangeduid met dit pictogram ![](assets/experimentation_report_1.png) .

+++Meer informatie over de verschillende maatstaven en widgets die beschikbaar zijn voor het rapport Experimentation.

De **[!UICONTROL Experiment result]** -widget geeft de prestaties van elke variant weer. U kunt de basislijn wijzigen door een van de behandelingen te selecteren in de vervolgkeuzelijst **[!UICONTROL Baseline]** . De beste behandeling wordt weergegeven met een sterpictogram.

De tabel bevat de volgende cijfers:

* **[!UICONTROL Lift over baseline]**: maat voor de procentuele verbetering van de conversiesnelheid van een bepaalde behandeling ten opzichte van de basislijn.

* **[!UICONTROL Confidence]**: Bewijs dat een bepaalde behandeling gelijk is aan de basisbehandeling. [Meer informatie](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

* **[!UICONTROL Unique outbound clicks]**: Het totale aantal klikken over uitgaande kanalen.

* **[!UICONTROL Profiles]**: aantal profielen waarop deze behandeling is gericht.

* **[!UICONTROL Unique outbound clicks/profiles]**: de totale waarde van de metrische waarde voor succes die eerder is geselecteerd bij het maken van uw experimenten, gedeeld door het aantal profielen.

De grafiek van **[!UICONTROL Confidence interval]** meet onzekerheid rond verbetering. Het geeft het procentuele verschil in prestaties weer tussen de basislijn en de best presterende behandeling. [Meer informatie](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences).
+++

Voor diepte-duik in deze resultaten en hoe te om hen te interpreteren, verwijs naar [ deze pagina ](../content-management/get-started-experiment.md#interpret-results).
