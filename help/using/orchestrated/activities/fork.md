---
solution: Journey Optimizer
product: journey optimizer
title: De vorkactiviteit gebruiken
description: Leer hoe u de vorkactiviteit in een georkestreerde campagne kunt gebruiken
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 28284b3d42a0e78add3470ef128dd740f9cc9dfd
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# Vertakking {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="Vorkactiviteit"
>abstract="De **activiteit 0} van het Vonk {staat u toe om uitgaande overgangen tot stand te brengen om verscheidene activiteiten tezelfdertijd te beginnen.**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="Overgangen naar vorkactiviteit"
>abstract="Door gebrek, worden twee overgangen gecreeerd met de activiteit van het a **Fork**. Klik **toevoegen overgangsknoop** om een extra uitgaande overgang te bepalen, en zijn etiket in te gaan."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](../create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](../orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de Vraag Modeler ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uitdrukkingen ](../edit-expressions.md) uit | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) Gesplitst [ - ](split.md) wacht [](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

De **[!UICONTROL Fork]** -activiteit is een **[!UICONTROL Flow control]** -component waarmee u meerdere uitgaande overgangen kunt maken, waardoor verschillende activiteiten parallel kunnen worden uitgevoerd.

## De vorkactiviteit configureren{#fork-configuration}

Voer de volgende stappen uit om de **[!UICONTROL Fork]** -activiteit te configureren:

![](../assets/workflow-fork.png)

1. Voeg een **[!UICONTROL Fork]** activiteit aan uw georkestreerde campagne toe.

1. Definieer een **[!UICONTROL Label]** .

1. Wijs een etiket aan elke uitgaande overgang toe. Standaard zijn er twee overgangen beschikbaar.

1. Als u een overgang wilt verwijderen, klikt u op het pictogram ![](../assets/do-not-localize/Smock_Delete_18_N.svg) .

1. Klik indien nodig op **[!UICONTROL Add transition]** om een extra uitgaande overgang toe te voegen.
