---
solution: Journey Optimizer
product: journey optimizer
title: Gebruik de activiteit van de Wacht in georkestreerde campagnes
description: Leer hoe te om de activiteit van de Wacht in georkestreerde campagnes te gebruiken
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 17%

---

# Wachten {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Wachtactiviteit"
>abstract="**wacht** activiteit wordt gebruikt om de overgang van een activiteit aan een andere te vertragen."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de Vraag Modeler ](orchestrated-query-modeler.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening ](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md)[ |

{style="table-layout:fixed"}

+++

<br/><br/>

**wacht** activiteit is de controle **activiteit van de a** Stroom. Het wordt gebruikt om een bepaalde hoeveelheid tijd toe te staan om tussen twee uit te voeren activiteiten over te gaan. Bijvoorbeeld als u een aantal dagen wilt wachten na een e-mailleveringsactiviteit om het aantal open- en klikacties tijdens die periode te analyseren voordat u follow-upbewerkingen gaat uitvoeren (herinneringsmail, doelgroep maken, enz.).

## Configuratie{#wait-configuration}

Volg deze stappen om **te vormen wachten** activiteit:

1. Voeg a **toe wacht** activiteit in uw georkestreerde campagne.

1. Specificeer de **Duur** van het wachten tussen de binnenkomende en uitgaande overgangen.

1. Selecteer de tijdeenheid op het **gebied van Punten**: seconden, notulen, uren, dagen.

## Voorbeeld{#wait-example}

Het volgende voorbeeld illustreert **wacht** activiteit in een typisch gebruiksgeval. U stuurt een e-mailuitnodiging voor een evenement. 24 uur nadat het is verzonden, wordt een SMS-verzending naar dezelfde populatie verzonden.

![](../assets/workflow-wait-example.png)
