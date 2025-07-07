---
solution: Journey Optimizer
product: journey optimizer
title: De vorkactiviteit gebruiken
description: Leer hoe u de vorkactiviteit in een georkestreerde campagne kunt gebruiken
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: a19fe429d34a88c6159ab3b2b4dfa3768bcd24ad
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# Vertakking {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="Vorkactiviteit"
>abstract="De **activiteit 0&rbrace; van het Vonk &lbrace;staat u toe om uitgaande overgangen tot stand te brengen om verscheidene activiteiten tezelfdertijd te beginnen.**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="Overgangen naar vorkactiviteit"
>abstract="Door gebrek, worden twee overgangen gecreeerd met de activiteit van het a **Fork**. Klik **toevoegen overgangsknoop** om een extra uitgaande overgang te bepalen, en zijn etiket in te gaan."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ krijgen begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Toegang en beheert georkestreerde campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen om een georkestreerde campagne ](../gs-campaign-creation.md)<br/><br/>[ tot stand te brengen en te plannen de campagne ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) te controleren | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k <b>[ - ](fork.md)</b> Verzoening [ - ](reconciliation.md) sparen publiek [ - ](save-audience.md) Gesplitst [ - ](split.md) wacht [&#128279;](wait.md) |

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
