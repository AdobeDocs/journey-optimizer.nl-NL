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
source-git-commit: 6b8983d3f3fa989bd7190fc6a8b51fa8989b2293
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 1%

---

# Globaal verslag campagne voeren {#objective-report}

Het algemene rapport van de campagne kan direct van uw Campagne met het **[!UICONTROL View report]** knop.

De campagne **[!UICONTROL Global report]** is verdeeld in verschillende widgets waarin het succes en de fouten van uw campagne worden beschreven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Raadpleeg voor meer informatie hierover [sectie](../reports/global-report.md#modify-dashboard).

Voor een gedetailleerde lijst van elke metrisch beschikbaar in Adobe Journey Optimizer, verwijs naar [deze pagina](global-report.md#list-of-components-global.md)

## Tabblad Campagne {#campaign-global-objectives}

### Levering {#delivery-global-objectives}

![](assets/campaign_report_global_1.png)

De **[!UICONTROL Campaign's Statistics]** widget geeft de belangrijkste informatie met betrekking tot uw campagne:

* **[!UICONTROL Entered profiles]**: Aantal profielen dat de reis is begonnen.

* **[!UICONTROL Actions delivered]**: Het totale aantal unieke tijden dat een actie in de reis is uitgevoerd.

* **[!UICONTROL Actions failed in %]**: Het totale aantal unieke tijden dat een actie tijdens de reis is mislukt in verhouding tot het totale aantal unieke tijden dat een actie is uitgevoerd.

### Doelstellingen {#objective-global}

>[!AVAILABILITY]
>
>De **Doelstellingen** Deze functie is momenteel alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

![](assets/performance_report.gif)

De **[!UICONTROL Objectives]** kunt u de rapporten van uw leveringen perfectioneren door zich op één specifieke metrische waarde te richten.

De **[!UICONTROL Objectives]** vermeld **[!UICONTROL Datasets]** die een verbinding met een systeem definiëren om aanvullende informatie op te halen. Een lijst met ingebouwde **[!UICONTROL Objectives]** is beschikbaar maar u kunt uw eigen item toevoegen door nieuwe toe te voegen **[!UICONTROL Dataset]**. Voor de gedetailleerde procedure, zie [sectie](../campaigns/reporting-configuration.md).

Nadat u de doelstellingen hebt geselecteerd waarop u zich wilt richten, worden de twee **[!UICONTROL Performance overview]** en **[!UICONTROL Campaign objective]** widgets zullen een gedetailleerde samenvatting van uw leveringsprestaties verstrekken.

Met de **[!UICONTROL Campaign objective]** widget, kunt u ook kiezen om uw hoofddoel met een andere metrische waarde te vergelijken.

### Experimentatierapport {#experimentation-global-objectives}

![](assets/experimentation_report_3.png)

De **[!UICONTROL Experimentation]** tab geeft belangrijke inzichten in de prestaties van elke variant en geeft de meest succesvolle variant aan.

Het kan enige tijd duren om de beste uitvoerder te definiëren. Dit pictogram geeft dit weer. ![](assets/experimentation_report_1.png).

+++Leer meer over de verschillende metriek en widgets beschikbaar voor het rapport van de Experimentatie.

De **[!UICONTROL Experiment result]** widget geeft de prestaties van elke variant weer. U kunt uw basislijn wijzigen door een van de behandelingen te kiezen in het menu **[!UICONTROL Baseline]** de vervolgkeuzelijst. De beste behandeling wordt weergegeven met een sterpictogram.

De tabel bevat de volgende cijfers:

* **[!UICONTROL Lift over baseline]**: Meting van de procentuele verbetering van de conversiesnelheid van een bepaalde behandeling ten opzichte van de uitgangswaarde.

* **[!UICONTROL Confidence]**: Bewijs dat een bepaalde behandeling gelijk is aan de basisbehandeling. [Meer informatie](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Unique outbound clicks]**: Het totale aantal klikken over uitgaande kanalen.

* **[!UICONTROL Profiles]**: Aantal profielen waarop deze behandeling is gericht.

* **[!UICONTROL Unique outbound clicks/profiles]**: De totale waarde van de metrische waarde van Succes, die eerder werd geselecteerd toen het creëren van uw Experimenten, gedeeld door het aantal profielen.

De **[!UICONTROL Confidence interval]** in grafiek wordt onzekerheid over de verbetering gemeten . Het geeft het procentuele verschil in prestaties weer tussen de basislijn en de best presterende behandeling. [Meer informatie](../campaigns/experiment-calculations.md#confidence-intervals).
+++

Raadpleeg voor een diepgaande analyse van deze resultaten en de manier waarop u deze kunt interpreteren de volgende bronnen: [deze pagina](../campaigns/get-started-experiment.md#interpret-results).

