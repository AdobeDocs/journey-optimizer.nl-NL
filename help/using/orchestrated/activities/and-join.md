---
solution: Journey Optimizer
product: journey optimizer
title: De activiteit AND-join gebruiken
description: Leer hoe u de AND-join-activiteit gebruikt in een georkestreerde campagne
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 32b13d4fd62abc8052c1bf64d8a2d5e97bd0f464
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="AND-join-activiteit"
>abstract="De **en-sluit zich aan** activiteit staat u toe om veelvoudige uitvoeringstakken van een georkestreerde campagne te synchroniseren. De regeling wordt in werking gesteld zodra alle voorgaande activiteiten zijn beëindigd. Op deze manier kunt u ervoor zorgen dat bepaalde activiteiten zijn voltooid voordat u doorgaat met het uitvoeren van de georkestreerde campagne."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](../create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](../orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](../send-messages.md)<br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de Vraag Modeler ](../orchestrated-query-modeler.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uitdrukkingen ](../edit-expressions.md) uit | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ combineert ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) - [ Fork ](fork.md) opnieuw verzoening ](reconciliation.md) - [ Gesplitst ](split.md) - [ wacht ](wait.md)[ |

{style="table-layout:fixed"}

+++

<br/><br/>

De **en-sluit zich aan** activiteit is de controle **activiteit van de a** Stroom. Hiermee kunt u meerdere uitvoeringstakken van een georkestreerde campagne synchroniseren.

Deze activiteit brengt slechts zijn uitgaande overgang teweeg zodra alle binnenkomende overgangen worden geactiveerd, met andere woorden, zodra alle voorafgaande activiteiten zijn geëindigd. Hierdoor kunt u ervoor zorgen dat bepaalde activiteiten zijn voltooid voordat u doorgaat met het uitvoeren van de georkestreerde campagne.

## Vorm en verbind activiteit{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Samenvoegopties"
>abstract="Selecteer de activiteiten waaraan u wilt deelnemen. In de **Primaire reeks** drop-down, kies welke binnenkomende overgangspopulatie u wilt houden."

Voer de volgende stappen uit om de **EN-lid** activiteit te vormen:

![](../assets/workflow-andjoin.png)

1. Voeg veelvoudige activiteiten zoals kanaalactiviteiten toe om minstens twee verschillende uitvoertakken te vormen.
1. Voeg **toe EN-sluit** activiteit aan om het even welke takken.
1. In de **het samenvoegen opties** sectie, controleer alle vorige activiteiten u wenst u zich aansluit.
1. In de **Primaire reeks** drop-down, kies welke binnenkomende overgangspopulatie u wilt houden. De uitgaande overgang kan slechts één van de binnenkomende overgangspopulaties bevatten.

## Voorbeeld{#and-join-example}

In het volgende voorbeeld worden twee georkestreerde campagnevertakkingen getoond met een e-mail- en sms-levering. EN-toetreden zal teweegbrengen wanneer beide binnenkomende overgangen worden toegelaten. De pushberichten worden dan pas verzonden nadat beide leveringen zijn voltooid.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
