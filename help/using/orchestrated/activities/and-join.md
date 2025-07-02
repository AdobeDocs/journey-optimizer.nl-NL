---
solution: Journey Optimizer
product: journey optimizer
title: De activiteit AND-join gebruiken
description: Leer hoe u de AND-join-activiteit gebruikt in een georkestreerde campagne
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 7de878c316e966129e7dede37f132938d2abbdf8
workflow-type: tm+mt
source-wordcount: '321'
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
| [ worden begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](../create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](../orchestrate-activities.md)<br/><br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de Vraag Modeler ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uitdrukkingen ](../edit-expressions.md) uit | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) Gesplitst [ - ](split.md) wacht [&#128279;](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

De **[!UICONTROL And-join]** -activiteit is een **[!UICONTROL Flow control]** -activiteit. Hiermee kunt u meerdere uitvoeringstakken van een georkestreerde campagne synchroniseren.

Deze activiteit brengt slechts zijn uitgaande overgang teweeg zodra alle binnenkomende overgangen worden geactiveerd, met andere woorden, zodra alle voorafgaande activiteiten zijn geëindigd. Hierdoor kunt u ervoor zorgen dat bepaalde activiteiten zijn voltooid voordat u doorgaat met het uitvoeren van de georkestreerde campagne.

## Vorm en verbind activiteit{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Samenvoegopties"
>abstract="Selecteer de activiteiten waaraan u wilt deelnemen. In de **Primaire reeks** drop-down, kies welke binnenkomende overgangspopulatie u wilt houden."

Voer de volgende stappen uit om de **[!UICONTROL AND-join]** -activiteit te configureren:

![](../assets/workflow-andjoin.png)

1. Voeg veelvoudige activiteiten, zoals kanaalactiviteiten, toe om minstens twee verschillende uitvoertakken tot stand te brengen.

1. Voeg een **[!UICONTROL AND-join]** -activiteit in een van de vertakkingen in.

1. Selecteer onder de sectie **[!UICONTROL Merging options]** alle voorgaande activiteiten waaraan u wilt deelnemen.

1. Kies in de vervolgkeuzelijst **[!UICONTROL Primary set]** de binnenkomende overgangspopulatie die u wilt behouden.

## Voorbeeld{#and-join-example}

Dit voorbeeld illustreert twee gecoördineerde campagnevertakkingen, elk met een e-maillevering, één gericht op gouden leden en ander zilver. **[!UICONTROL AND-join]** activeert zodra beide inkomende overgangen in werking worden gesteld, en SMS zal slechts worden verzonden nadat beide e-mailleveringen, na een vertraging van 7 dagen worden voltooid.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
