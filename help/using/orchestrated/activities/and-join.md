---
solution: Journey Optimizer
product: journey optimizer
title: De activiteit AND-join gebruiken
description: Leer hoe u de AND-join-activiteit gebruikt in een georkestreerde campagne
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 25120dd71159d0233783ac4c189f528ff2c93ae3
workflow-type: tm+mt
source-wordcount: '357'
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
| [ wordt begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ Handmatig schema ](../manual-schema.md)</li><li>[ het uploadschema van het Dossier ](../file-upload-schema.md)</li><li>[ Ingest gegevens ](../ingest-data.md)</li></ul>[ toegang en beheer georkestreerde campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen om een georkestreerde campagne ](../gs-campaign-creation.md)<br/><br/>[ tot stand te brengen en te plannen de campagne ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) te controleren | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/><b>[ en-sluit zich aan ](and-join.md)</b> - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) sparen publiek [ - ](save-audience.md) Gesplitst [ - ](split.md) wacht [](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

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
