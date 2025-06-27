---
solution: Journey Optimizer
product: journey optimizer
title: Georkestreerde campagnes maken met Adobe Journey Optimizer
description: Leer hoe u georkestreerde campagnes kunt maken met Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: ecb62dfc6a04754cb5d549615047cfb8e5e8f518
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Campagne organiseren {#orchestrate}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ krijgen begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Toegang en beheert georkestreerde campagnes ](access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md)<br/><br/>[ creëren en plannen de campagne ](create-orchestrated-campaign.md)<br/><br/><b>[ activiteiten van het Orchestrate ](orchestrate-activities.md)</b><br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleren de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening ](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md)[ |

{style="table-layout:fixed"}

+++

<br/>

Zodra u [ een georkestreerde campagne ](gs-campaign-creation.md) hebt gecreeerd, kunt u beginnen de verschillende taken te ordenen het zal uitvoeren. Hiervoor wordt een visueel canvas verschaft, zodat u een georkestreerd campagnediagram kunt maken. Binnen dit diagram, kunt u diverse activiteiten toevoegen en hen in een opeenvolgende orde verbinden.

## Activiteiten toevoegen {#add}

In dit stadium van de configuratie, wordt het diagram getoond met een beginpictogram, dat het begin van uw georkestreerde campagne vertegenwoordigt. Als u uw eerste activiteit wilt toevoegen, klikt u op de knop **+** die is verbonden met het beginpictogram.

Er wordt een lijst met activiteiten weergegeven die aan het diagram kunnen worden toegevoegd. De beschikbare activiteiten zijn afhankelijk van uw positie binnen het georkestreerde campagnediagram. Bijvoorbeeld, wanneer het toevoegen van uw eerste activiteit, kunt u uw georkestreerde campagne beginnen door een publiek te richten, het georkestreerde campagneweg te verdelen, of a **te plaatsen wacht** activiteit om de georkestreerde campagneuitvoering te vertragen. Anderzijds, na a **bouwt publiek** activiteit, kunt u uw doel met het richten van activiteiten verfijnen, een levering naar uw publiek met kanaalactiviteiten verzenden, of het geordende campagneproces met de activiteiten van de stroomcontrole organiseren.

![](assets/orchestrated-start.png){zoomable="yes"}

Zodra een activiteit aan het diagram is toegevoegd, verschijnt een juiste ruit, toestaand u om het met specifieke montages te vormen. De gedetailleerde informatie over hoe te om elke activiteit te vormen is beschikbaar in [ deze sectie ](activities/about-activities.md).

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

Herhaal dit proces om zoveel activiteiten toe te voegen als u wilt, afhankelijk van de taken die u voor uw georkestreerde campagne wilt uitvoeren. U kunt ook een nieuwe activiteit invoegen tussen twee activiteiten. Om dit te doen, klik **+** knoop op de overgang tussen de activiteiten, selecteer de gewenste activiteit en vorm het in de juiste ruit.

U kunt de naam van de overgangen tussen elke activiteit aanpassen. U doet dit door de overgang te selecteren en het label ervan te wijzigen in het rechterdeelvenster.

![](assets/canvas-transition.png)

## De werkbalk Canvas {#toolbar}

De canvaswerkbalk bevat opties waarmee u de activiteiten eenvoudig kunt manipuleren en in het canvas kunt navigeren:

![](assets/orchestrated-toolbar.png)

![ Veelvoudig pictogram van de selectiemodus ](assets/do-not-localize/canvas-multiple.svg) Uitgezochte veelvoudige activiteiten om hen allen in één keer te schrappen of hen te kopiëren en te kleven. [ Leer hoe te om activiteiten kopiëren-te kleven ](#copy)

![ roteer pictogram ](assets/do-not-localize/canvas-rotate.svg) verdraai het canvas verticaal.

![ Passend aan het het schermpictogram ](assets/do-not-localize/canvas-fit.svg) past het het gezoemniveau van het canvas aan uw scherm aan.

![ het pictogram van het Gezoem uit ](assets/do-not-localize/canvas-zoomout.svg) ![ Gezoem binnen pictogram ](assets/do-not-localize/canvas-zoomin.svg) Gezoem uit of in het canvas.

![ pictogram van de montages van de Campagne ](assets/do-not-localize/canvas-map.svg) opent een momentopname van het canvas dat u toont wordt gevestigd.

## Activiteiten beheren {#manage}

Wanneer u activiteiten toevoegt, zijn er actieknoppen beschikbaar in het deelvenster Eigenschappen, zodat u meerdere bewerkingen kunt uitvoeren.

![](assets/activity-action.png)

![ het pictogram van de Schrapping ](assets/do-not-localize/activity-delete.svg) schrap de activiteit van het canvas.

![ onbruikbaar maken pictogram ](assets/do-not-localize/activity-disable.svg) ![ laat pictogram ](assets/do-not-localize/activity-enable.svg) onbruikbaar maken/laat de activiteit toe. Wanneer de georkestreerde campagne wordt uitgevoerd, worden activiteiten met een handicap en de volgende activiteiten op hetzelfde pad niet uitgevoerd en wordt de georkestreerde campagne gestopt.

{het pictogram van de Pauze ](assets/do-not-localize/activity-pause.svg) ![ hervatten pictogram ](assets/do-not-localize/activity-resume.svg) Pauze/hervat de activiteit. ![ Wanneer de georkestreerde campagne wordt uitgevoerd, pauzeert het bij de gepauzeerde activiteit. De bijbehorende taak en alle taken die deze in hetzelfde pad volgen, worden niet uitgevoerd.

![ het pictogram van het Exemplaar ](assets/do-not-localize/activity-copy.svg) Kopieer de activiteit. [ Leer hoe te om activiteiten kopiëren-te kleven ](#copy)

![ Logboeken en takenpictogram ](assets/do-not-localize/activity-logs.svg) heb toegang tot de logboeken en de taken van de activiteit.

Verscheidene **richtend** activiteiten, zoals **combineren** of **Deduplicatie**, staat u toe om de resterende bevolking te verwerken en het in een extra uitgaande overgang te omvatten. Bijvoorbeeld, als u a **Gesplitste** activiteit gebruikt, bestaat de aanvulling uit de bevolking die om het even welke eerder bepaalde ondergroepen niet aanpast. Activeer de optie **[!UICONTROL Generate complement]** als u deze mogelijkheid wilt gebruiken.

## Verplaatsen of kopiëren {#move-copy}

### Kopiëren en plakken {#copy}

U kunt activiteiten kopiëren en ze in elk georkestreerd campagnecanvas plakken. De doelcampagne kan zich op een ander browsertabblad bevinden.

* Om één activiteit te kopiëren, klik het ![ pictogram van het Exemplaar ](assets/do-not-localize/activity-copy.svg) knoop in de activiteiteneigenschappen ruit.
* Om veelvoudige activiteiten te kopiëren, klik het ![ Meerdere pictogram van de selectiewijze ](assets/do-not-localize/canvas-multiple.svg) op de canvastoolbar.

| Eén activiteit kopiëren | Meerdere activiteiten kopiëren |
|  ---  |  ---  |
|  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

Als u de activiteiten wilt plakken, klikt u op de knop **+** in een overgang en selecteert u &quot;X-activiteit plakken&quot;.

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

<!--## Example {#example}

Here is an orchestrated campaign example designed to send an email to all customers (other than VIP customers) with an email who are interested in coffee machines.

![](assets/workflow-example.png){zoomable="yes"}{zoomable="yes"}

To achieve this, activities below have been added:

* A **[!UICONTROL Fork]** activity that divides the orchestrated campaign into three paths (one for each set of customer),
* **[!UICONTROL Build audience]** activities to target the three sets of customers:

    * Customers with an email,
    * Customers belonging to the pre-existing "Interrested in Coffee Machine(s)" audience,
    * Customers belonging to the pre-existing "VIP ro reward" audience.

* A **[!UICONTROL Combine]** activity that groups together customers with an email and those interested in coffee machines,
* A **[!UICONTROL Combine]** activity that excludes VIP customers,
* An **[!UICONTROL Email delivery]** activity that sends an email to the resulting customers. 

Once you have completed the orchestrated campaign, add en **[!UICONTROL End]** activity at the end of the diagram. This activity allow you to visually mark the end of a workflow and has no functional impact.

After successfully designing the orchestrated campaign diagram, you can execute the orchestrated campaign and track the progress of its various tasks. [Learn how to start an orchestrated campaign and monitor its execution](start-monitor-campaigns.md)-->
