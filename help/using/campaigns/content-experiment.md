---
title: Een contentexperiment maken
description: Leer hoe u een content-experiment kunt maken in uw campagnes
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: e81e21f714a3c5450defa1129e1e2b9969dc1de7
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 1%

---

# Een inhoudexperiment maken {#content-experiment}

>[!AVAILABILITY]
>
>De **Inhoud experimenteren** Deze functie is momenteel alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

Met Journey Optimizer Content Experiment kunt u meerdere behandelingen voor de afgifte definiëren. Het betrokken publiek wordt willekeurig toegewezen aan elke behandeling om te bepalen welke behandeling het best presteert ten opzichte van de maatstaf van belangstelling. U kunt kiezen om de leveringsinhoud, het onderwerp, of de afzender te variëren.

>[!NOTE]
>
>Alvorens met de Experimenteer van de Inhoud te beginnen, zorg ervoor dat uw rapporteringsconfiguratie voor uw douanedatasets wordt geplaatst. Meer informatie in [deze sectie](reporting-configuration.md).

In het onderstaande voorbeeld is de leveringsdoelstelling opgesplitst in twee groepen, die elk 45% van de doelpopulatie vertegenwoordigen, en een holdoutgroep van 10%, die de levering niet zal ontvangen.

Elke persoon in het doelpubliek ontvangt één versie van een e-mail, met een onderwerpregel die één van de volgende twee is:

* een rechtstreekse bevordering van een aanbod van 10 % voor de nieuwe collectie en een afbeelding .
* de andere reclame maakt alleen reclame voor een speciale aanbieding zonder de 10 % korting zonder afbeelding te specificeren .

Het doel is hier te zien of zullen de ontvangers met e-mail afhankelijk van het ontvangen experiment interactie aangaan. Daarom zullen wij **[!UICONTROL Email Opens]** als het primaire doel metrisch in deze Content Experiment.

![](assets/content_experiment.png)

## Uw campagne maken {#campaign-experiment}

1. Van de **[!UICONTROL Campaigns]** pagina, klikt u op **[!UICONTROL Create campaign]**.

   ![](assets/content_experiment_1.png)

1. Selecteer vervolgens het kanaal **[!UICONTROL Surface]** wilt u gebruiken voor deze levering. Raadpleeg voor meer informatie de [Kanaaloppervlakken](../configuration/channel-surfaces.md) pagina.

   ![](assets/content_experiment_2.png)

1. Klik op **[!UICONTROL Create]**.

1. Stel de **[!UICONTROL Properties]** van je levering:
   * **[!UICONTROL Title]**
   * **[!UICONTROL Description]**
   * **[!UICONTROL Category]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactional]**

1. Als u uw inhoudexperiment wilt starten, schakelt u het **[!UICONTROL Content experiment]** optie. De **[!UICONTROL Content experiment]** wordt weergegeven.

   ![](assets/content_experiment_3.png)

1. Bepaal het publiek om te richten. Om dit te doen, klik **[!UICONTROL Select audience]** om de lijst met beschikbare Adobe Experience Platform-segmenten weer te geven. [Meer informatie over segmenten](../segment/about-segments.md)

   In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [Meer informatie](get-started-experiment.md#content-experiment-work)

1. Om uw campagne op een specifieke datum of op een terugkomende frequentie uit te voeren, vorm de sectie van het Programma. [Meer informatie](create-campaign.md)

1. Klikken **[!UICONTROL Edit content]** om uw verschillende functies aan te passen **[!UICONTROL Treatments]**.

   ![](assets/content_experiment_4.png)

## Uw behandelingen maken {#treatment-experiment}

1. Van de **[!UICONTROL Edit content]** begin uw behandeling aan te passen A.

   Voor deze behandeling zullen wij het speciale aanbod rechtstreeks in de onderwerpregel specificeren.

   ![](assets/content_experiment_5.png)

1. Na het ontwerpen van de eerste behandeling, kunt u het beste **[!UICONTROL More actions]** klikt u op **[!UICONTROL Duplicate]**.

   U kunt er ook voor kiezen een nieuwe behandeling helemaal opnieuw te starten door op de knop **[!UICONTROL Content experiment]** knop ![](assets/content_experiment_16.png) om toegang te krijgen tot de geavanceerde opties **[!UICONTROL Add treatment]**.

   ![](assets/content_experiment_7.png)

1. Wijzig de **[!UICONTROL Title]** van uw behandeling om ze beter te onderscheiden.

   ![](assets/content_experiment_8.png)

1. Pas uw tweede behandeling naar wens aan.

   Hier kiezen we ervoor het aanbod niet op te geven in het **[!UICONTROL Subject line]**.

   ![](assets/content_experiment_9.png)

Zodra uw behandelingen gepersonaliseerd zijn, kunt u beginnen uw Experiment van de Inhoud te vormen.

## Uw inhoudexperiment configureren {#configure-experiment}

1. Wanneer beide leveringen zijn gepersonaliseerd, wordt vanaf de **[!UICONTROL Edit content]** venster, selecteert u **[!UICONTROL Configure content experiment]**.

   ![](assets/content_experiment_10.png)

1. Selecteer de doelstellingen die u voor uw experiment wilt instellen.

   Voor ons experiment selecteren we **[!UICONTROL Email open]** om te testen of ontvangers hun e-mails zullen openen als de promotiecode zich op de onderwerpregel bevindt.

   ![](assets/content_experiment_11.png)

1. Kies of u een **[!UICONTROL Holdout]** groeperen voor levering. Deze groep zal geen inhoud van deze campagne ontvangen.

   Als u de schakelbalk inschakelt, neemt dit automatisch 10% van uw bevolking in beslag. Indien nodig kunt u dit percentage aanpassen.

   ![](assets/content_experiment_12.png)

1. Vervolgens kunt u een exact percentage toewijzen aan elk **[!UICONTROL Treatment]** of schakelt u gewoon de **[!UICONTROL Distribute evenly]** schakelbalk.

   ![](assets/content_experiment_13.png)

1. Klikken **[!UICONTROL Save]** wanneer uw configuratie wordt geplaatst.

1. Wanneer uw inhoudexperiment gereed is, kunt u klikken **[!UICONTROL Review to activate]** om een overzicht van de campagne weer te geven. Waarschuwt de weergave als een parameter onjuist is of ontbreekt.

   ![](assets/content_experiment_15.png)

1. Controleer of uw campagne correct is geconfigureerd en klik vervolgens op **[!UICONTROL Activate]** om te starten.

   ![](assets/content_experiment_14.png)

Na het vormen van uw experimenteren en campagne, kunt u het succes van uw levering met het rapport van de Campagne volgen.

## Doelstellingen {#objectives-global}

>[!AVAILABILITY]
>
>De functie voor het experimenteren met inhoud is momenteel alleen beschikbaar voor een set organisaties (beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

![](assets/performance_report.gif)

De **[!UICONTROL Objectives]** kunt u in uw campagnerapport de rapporten van uw leveringen perfectioneren door zich op één specifieke metrische waarde te richten.

De **[!UICONTROL Objectives]** vermeld **[!UICONTROL Datasets]** die een verbinding met een systeem definiëren om aanvullende informatie op te halen. Een lijst met ingebouwde **[!UICONTROL Objectives]** is beschikbaar maar u kunt uw eigen item toevoegen door nieuwe toe te voegen **[!UICONTROL Dataset]**. Voor de gedetailleerde procedure, zie [sectie](reporting-configuration.md).

Nadat u de doelstellingen hebt geselecteerd waarop u zich wilt richten, worden de twee **[!UICONTROL Performance overview]** en **[!UICONTROL Campaign objective]** widgets zullen een gedetailleerde samenvatting van uw leveringsprestaties verstrekken.

Met de **[!UICONTROL Campaign objective]** widget, kunt u ook kiezen om uw hoofddoel met een andere metrische waarde te vergelijken.

Houd er rekening mee dat elke widget indien nodig kan worden vergroot of verkleind en verwijderd. Raadpleeg voor meer informatie hierover [sectie](../reports/global-report.md#modify-dashboard).

## Experimentatierapport {#experimentation-global}

>[!AVAILABILITY]
>
>De functie voor het experimenteren met inhoud is momenteel alleen beschikbaar voor een set organisaties (beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

![](assets/experimentation_report_3.png)

Van uw campagne **[!UICONTROL Global report]** de **[!UICONTROL Experimentation]** tabblad bevat de belangrijkste informatie met betrekking tot de manier waarop elke variant wordt uitgevoerd en of er een best presterende variant is.

Het kan enige tijd duren om de beste uitvoerder te definiëren. Dit pictogram geeft dit weer. ![](assets/experimentation_report_1.png).

De **[!UICONTROL Experiment result]** widget geeft de prestaties van elke variant weer. U kunt uw basislijn wijzigen door een van de behandelingen te kiezen in het menu **[!UICONTROL Baseline]** de vervolgkeuzelijst. De beste behandeling wordt weergegeven met een sterpictogram.

De tabel bevat de volgende cijfers:

* **[!UICONTROL Profiles]**: Aantal profielen waarop deze behandeling is gericht.

* **[!UICONTROL Unique outbound clicks]**: Het totale aantal klikken over uitgaande kanalen.

* **[!UICONTROL Count per profile]**: Totale waarde van de metrische waarde van de doelstelling Experiment gedeeld door het aantal profielen.

* **[!UICONTROL Confidence interval]**: Percentage verschil in prestaties tussen de basislijn en de best presterende behandeling. [Meer informatie](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Average lift]**: Percentage verbetering van de conversiesnelheid van een gegeven behandeling ten opzichte van de uitgangswaarde. [Meer informatie](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confidence]**: Bewijs dat een bepaalde behandeling gelijk is aan de basisbehandeling. [Meer informatie](../campaigns/experiment-calculations.md#understand-confidence)

Raadpleeg voor een diepgaande analyse van deze resultaten en de manier waarop u deze kunt interpreteren de volgende bronnen: [deze pagina](../campaigns/get-started-experiment.md#interpret-results).
