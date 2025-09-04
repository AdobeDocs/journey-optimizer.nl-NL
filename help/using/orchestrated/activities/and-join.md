---
solution: Journey Optimizer
product: journey optimizer
title: De activiteit AND-join gebruiken
description: Leer hoe u de AND-join-activiteit gebruikt in een geordende campagne
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---


# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="AND-join-activiteit"
>abstract="De **en-sluit zich aan** activiteit staat u toe om veelvoudige uitvoeringstakken van een Geordende campagne te synchroniseren. De regeling wordt in werking gesteld zodra alle voorgaande activiteiten zijn beëindigd. Hierdoor kunt u ervoor zorgen dat bepaalde activiteiten zijn voltooid voordat u doorgaat met het uitvoeren van de geordende campagne."

De **[!UICONTROL And-join]** -activiteit is een **[!UICONTROL Flow control]** -activiteit. Het staat u toe om veelvoudige uitvoeringstakken van een Geordende campagne te synchroniseren.

Deze activiteit brengt slechts zijn uitgaande overgang teweeg zodra alle binnenkomende overgangen worden geactiveerd, met andere woorden, zodra alle voorafgaande activiteiten zijn geëindigd. Hierdoor kunt u ervoor zorgen dat bepaalde activiteiten zijn voltooid voordat u doorgaat met het uitvoeren van de geordende campagne.

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
