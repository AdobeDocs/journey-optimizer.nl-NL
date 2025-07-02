---
solution: Journey Optimizer
product: journey optimizer
title: Gebruik de activiteit van de Wacht in georkestreerde campagnes
description: Leer hoe te om de activiteit van de Wacht in georkestreerde campagnes te gebruiken
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 28284b3d42a0e78add3470ef128dd740f9cc9dfd
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 1%

---

# Wachten {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Wachtactiviteit"
>abstract="**wacht** activiteit wordt gebruikt om de overgang van een activiteit aan een andere te vertragen."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](../create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](../orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de Vraag Modeler ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uitdrukkingen ](../edit-expressions.md) uit | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) Gesplitst [ - ](split.md) wacht [](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

De **[!UICONTROL Wait]** -activiteit is een **[!UICONTROL Flow control]** -component die wordt gebruikt om een vertraging tussen twee activiteiten in een georkestreerde campagne in te voeren. Dit helpt ervoor te zorgen dat uw follow-upactiviteiten een beter tijdstip hebben en relevanter zijn voor de betrokkenheid van gebruikers.

U kunt bijvoorbeeld een paar dagen na het verzenden van een e-mailbericht wachten om te controleren of het bericht wordt geopend en vervolgens klikken voordat u een vervolgbericht verzendt.

## Configuratie{#wait-configuration}

Voer de volgende stappen uit om de **[!UICONTROL Wait]** -activiteit te configureren:

1. Voeg een **[!UICONTROL Wait]** activiteit in uw georkestreerde campagne toe.

1. Selecteer het type Wacht dat het beste bij uw behoeften past:

   * **[!UICONTROL Duration]**: geef een vertraging op in seconden, minuten, uren of dagen voordat u verdergaat met de volgende activiteit.

   * **[!UICONTROL Fixed time]**: stel een specifieke datum en tijd in waarna de volgende activiteit begint.

   ![](../assets/wait_activity.png)

## Voorbeeld{#wait-example}

Het volgende voorbeeld illustreert de **[!UICONTROL Wait]** activiteit in een typisch gebruikscase.  Er wordt een e-mail met een promotiecode verzonden naar profielen die hun verjaardagen vieren. Na 29 dagen wordt een SMS verzonden naar dezelfde groep als een herinnering dat hun verjaardagspromotiecode bijna verlopen is.

![](../assets/wait-example.png)
