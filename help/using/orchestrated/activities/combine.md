---
solution: Journey Optimizer
product: journey optimizer
title: De combinatie-activiteit gebruiken
description: Meer informatie over het gebruik van de combinatieactiviteit
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: af3c3a9c-8172-43b0-bba1-4a3d068b9a9e
source-git-commit: cb335fd5610d70d801ae1c32dfe4d3ca9d1160ab
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 9%

---

# Combineren {#combine}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine"
>title="Combineer activiteit"
>abstract="**combineert** activiteit staat u toe om segmentatie op uw binnenkomende bevolking uit te voeren. U kunt dus meerdere populaties combineren, een deel ervan uitsluiten of gegevens alleen gemeenschappelijk houden voor meerdere doelen."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](../create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](../orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](../send-messages.md)<br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de Vraag Modeler ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uitdrukkingen ](../edit-expressions.md) uit | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ combineert ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) - [ Fork ](fork.md) opnieuw verzoening [&#128279;](reconciliation.md) - [ Gesplitst ](split.md) - [ wacht ](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

De **[!UICONTROL Combine]** activiteit is een type van **[!UICONTROL Targeting]** activiteit die u toelaat om uw binnenkomende bevolking effectief te segmenteren. Hiermee kunt u meerdere populaties samenvoegen, specifieke segmenten uitsluiten of alleen de gegevens behouden die over verschillende doelen worden gedeeld.

De volgende segmentatieopties zijn beschikbaar:

* **[!UICONTROL Union]** : voegt de resultaten van meerdere activiteiten samen tot één gezamenlijk doel.

* **[!UICONTROL Intersection]**: behoudt alleen de elementen die gemeenschappelijk zijn voor alle binnenkomende populaties.

* **[!UICONTROL Exclusion]**: verwijdert elementen uit één populatie op basis van opgegeven criteria.

## De combinatieactiviteit configureren {#combine-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_merging_options"
>title="Samenvoegopties voor doorsnede"
>abstract="Met de doorsnede kunt u alleen de elementen behouden die gemeenschappelijk zijn voor de verschillende binnenkomende populaties in de activiteit. Controleer in de sectie Sets to join alle vorige activiteiten waaraan u wilt deelnemen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_merging_options"
>title="Samenvoegopties voor uitsluiting"
>abstract="Met deze uitsluiting kunt u elementen op basis van bepaalde criteria uitsluiten van één populatie. Controleer in de sectie Sets to join alle vorige activiteiten waaraan u wilt deelnemen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_options"
>title="Selecteer het segmentatietype"
>abstract="Selecteer hoe u het publiek wilt combineren. De **Unie** staat u toe om het resultaat van veelvoudige activiteiten in één enkel doel te hergroeperen. **Intersection** staat u toe om slechts de elementen gemeenschappelijk voor de verschillende binnenkomende populaties in de activiteit te houden. De **Uitsluiting** staat u toe om elementen van één bevolking volgens bepaalde criteria uit te sluiten. "

Voer de volgende algemene stappen uit om de **[!UICONTROL Combine]** -activiteit te configureren:

![](../assets/orchestrated-combine.png)

1. Voeg meerdere activiteiten, zoals **[!UICONTROL Build audience]** -activiteiten, toe om ten minste twee verschillende uitvoeringstakken te vormen.
1. Voeg een **[!UICONTROL Combine]** activiteit aan om het even welke vorige takken toe.
1. Selecteer het segmentatietype: [ unie ](#union), [ intersection ](#intersection) of [ uitsluiting ](#exclusion).
1. Klik op **[!UICONTROL Continue]**.
1. Controleer in de sectie **[!UICONTROL Sets to join]** alle vorige activiteiten waaraan u wilt deelnemen.

## Samenvoegen {#combine-union}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_reconciliation"
>title="Afstemmingsopties"
>abstract="Selecteer het **Type van Verzoening** om te bepalen hoe te om duplicaten te behandelen. Door gebrek, wordt de **optie van Sleutels** geactiveerd, betekenend dat de activiteit slechts één element houdt wanneer de elementen van de verschillende binnenkomende overgangen de zelfde sleutel hebben. Gebruik de **selectie van A kolommen** optie om de lijst van kolommen te bepalen waarop de gegevensverzoening wordt toegepast."

In de **[!UICONTROL Combine]** -activiteit kunt u een **[!UICONTROL Union]** configureren. Hiervoor moet u de optie **[!UICONTROL Reconciliation type]** selecteren om te definiëren hoe duplicaten worden verwerkt:

* **[!UICONTROL Keys only]**: Dit is de standaardmodus. De activiteit behoudt slechts één element wanneer elementen van de verschillende binnenkomende overgangen dezelfde sleutel hebben. Deze optie kan alleen worden gebruikt als de binnenkomende populaties homogeen zijn.
* **[!UICONTROL A selection of columns]**: selecteer deze optie om de lijst met kolommen te definiëren waarop de afstemming van gegevens wordt toegepast. U moet eerst de primaire set (de set met de brondata) selecteren en vervolgens de kolommen die u voor de samenvoeging wilt gebruiken.

In het volgende voorbeeld gebruiken we een **[!UICONTROL Combine]** -activiteit en voegen we een **[!UICONTROL Union]** toe om alle profielen van de twee query&#39;s op te halen: leden van Loyalty&#39;s en kopers om een groter publiek te vormen.

![](../assets/orchestrated-union-example.png)

## Doorsnede {#combine-intersection}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_reconciliation_options"
>title="Afstemmingsopties voor doorsnede"
>abstract="Selecteer het **Type van Verzoening** om te bepalen hoe te om duplicaten te behandelen. Door gebrek, wordt de **optie van Sleutels** geactiveerd, betekenend dat de activiteit slechts één element houdt wanneer de elementen van de verschillende binnenkomende overgangen de zelfde sleutel hebben. Gebruik de **selectie van A kolommen** optie om de lijst van kolommen te bepalen waarop de gegevensverzoening wordt toegepast."

In de **[!UICONTROL Combine]** -activiteit kunt u een **[!UICONTROL Intersection]** configureren. Hiervoor moet u de volgende extra stappen volgen:

1. Selecteer **[!UICONTROL Reconciliation type]** om te bepalen hoe de duplicaten worden behandeld. Zie [ Unie ](#union) sectie.
1. U kunt de optie **[!UICONTROL Generate completement]** inschakelen als u de resterende populatie wilt verwerken. Het complement zal de samenvoeging bevatten van de resultaten van alle binnenkomende activiteiten min de doorsnede. Een extra uitgaande overgang zal dan aan de activiteit worden toegevoegd.

In het volgende voorbeeld wordt de **[!UICONTROL Intersection]** tussen twee queryactiviteiten getoond. Het wordt hier gebruikt om profielen op te halen met een Loyalty-lidmaatschap en wiens laatste aankoop minder dan een maand geleden was.

![](../assets/orchestrated-intersection-example.png)


## Uitsluiting {#combine-exclusion}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_options"
>title="Uitsluitingsregels"
>abstract="Indien nodig, kunt u binnenkomende lijsten manipuleren. Om een doel van een andere dimensie uit te sluiten, moet dit doel worden teruggebracht naar dezelfde doeldimensie als het hoofddoel. Om dit te doen, voegt de klik een regel in de sectie van de Regels van de Uitsluiting toe en specificeert de voorwaarden van de afmetingsverandering. Afstemming van gegevens vindt plaats via een attribuut of een join-functie."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_sets"
>title="Te combineren sets selecteren"
>abstract="In de **Reeksen om zich bij** sectie aan te sluiten, selecteer de **Primaire reeks** van de binnenkomende overgangen. Dit is de set waaruit elementen worden uitgesloten. De andere sets komen overeen met de elementen voordat deze worden uitgesloten van de primaire set."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_exclusion"
>title="Uitsluitingsregels"
>abstract="Indien nodig, kunt u binnenkomende lijsten manipuleren. Om een doel van een andere dimensie uit te sluiten, moet dit doel worden teruggebracht naar dezelfde doeldimensie als het hoofddoel. Om dit te doen, voegt de klik een regel in de sectie van de Regels van de Uitsluiting toe en specificeert de voorwaarden van de afmetingsverandering. Afstemming van gegevens vindt plaats via een attribuut of een join-functie."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_complement"
>title="Combineren genereert een complement"
>abstract="Schakel de optie Aanvulling genereren in of uit om de resterende populatie in een extra overgang te verwerken."

In de **[!UICONTROL Combine]** -activiteit kunt u een **[!UICONTROL Exclusion]** configureren. Hiervoor moet u de volgende extra stappen volgen:

1. Selecteer in de sectie **[!UICONTROL Sets to join]** de **[!UICONTROL Primary set]** van de binnenkomende overgangen. Dit is de set waaruit elementen worden uitgesloten. De andere sets komen overeen met de elementen voordat deze worden uitgesloten van de primaire set.
1. Indien nodig, kunt u binnenkomende lijsten manipuleren. Om een doel van een andere dimensie uit te sluiten, moet dit doel worden teruggebracht naar dezelfde doeldimensie als het hoofddoel. Klik hiertoe op **[!UICONTROL Add a rule]** in de sectie **[!UICONTROL Exclusion rules]** en geef de voorwaarden voor het wijzigen van de afmetingen op. Afstemming van gegevens vindt plaats via een attribuut of een join-functie.
1. U kunt de optie **[!UICONTROL Generate completement]** inschakelen als u de resterende populatie wilt verwerken. Zie de [ sectie van de Intersectie ](#intersection).

In het volgende **[!UICONTROL Exclusion]** -voorbeeld worden twee query&#39;s weergegeven die zijn geconfigureerd voor filterprofielen die een product hebben aangeschaft. De profielen die geen loyaliteitslidmaatschap hebben worden dan uitgesloten van de eerste reeks.

Waarom: Je voert een loyaliteitscampagne, dus niet-leden zijn irrelevant.

![](../assets/orchestrated-exclusion-example.png)

