---
solution: Journey Optimizer
product: journey optimizer
title: De combinatie-activiteit gebruiken
description: Meer informatie over het gebruik van de combinatieactiviteit
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: af3c3a9c-8172-43b0-bba1-4a3d068b9a9e
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 8%

---

# Combineren {#combine}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine"
>title="Combineer activiteit"
>abstract="**combineert** activiteit staat u toe om segmentatie op uw binnenkomende bevolking uit te voeren. U kunt dus meerdere populaties combineren, een deel ervan uitsluiten of gegevens alleen gemeenschappelijk houden voor meerdere doelen."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](../create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](../orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](../send-messages.md)<br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de Vraag Modeler ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uitdrukkingen ](../edit-expressions.md) uit | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ combineert ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) - [ Fork ](fork.md) opnieuw verzoening ](reconciliation.md) - [ Gesplitst ](split.md) - [ wacht ](wait.md)[ |

{style="table-layout:fixed"}

+++

<br/>

**combineer** activiteit is a **richtend** activiteit. Deze activiteit staat u toe om segmentatie op uw binnenkomende bevolking uit te voeren. U kunt dus meerdere populaties combineren, een deel ervan uitsluiten of gegevens alleen gemeenschappelijk houden voor verschillende doelen. Hier volgen de beschikbare segmentatietypen:

<!--
The **Combine** activity can be placed after any other activity, but not at the beginning of the workflow. Any activity can be placed after the **Combine**.
-->

* De **Unie** staat u toe om het resultaat van veelvoudige activiteiten in één enkel doel te hergroeperen.
* **Intersection** staat u toe om slechts de elementen gemeenschappelijk voor de verschillende binnenkomende populaties in de activiteit te houden.
* De **Uitsluiting** staat u toe om elementen van één bevolking volgens bepaalde criteria uit te sluiten.

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

Volg deze gemeenschappelijke stappen beginnen de **te vormen combineren** activiteit:

![](../assets/workflow-combine.png)

1. Voeg veelvoudige activiteiten zoals **toe bouwt publiek** activiteiten om minstens twee verschillende uitvoertakken te vormen.
1. Voeg a **** activiteit aan om het even welke vorige takken combineren.
1. Selecteer het segmentatietype: [ unie ](#union), [ intersection ](#intersection) of [ uitsluiting ](#exclusion).
1. Klik **verdergaan**.
1. In de **Reeksen om zich bij** sectie aan te sluiten, controleer alle vorige activiteiten u wenst u zich aansluit.

## Samenvoegen {#combine-union}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_reconciliation"
>title="Afstemmingsopties"
>abstract="Selecteer het **Type van Verzoening** om te bepalen hoe te om duplicaten te behandelen. Door gebrek, wordt de **optie van Sleutels** geactiveerd, betekenend dat de activiteit slechts één element houdt wanneer de elementen van de verschillende binnenkomende overgangen de zelfde sleutel hebben. Gebruik de **selectie van A kolommen** optie om de lijst van kolommen te bepalen waarop de gegevensverzoening wordt toegepast."

In **combineer** activiteit, kunt u a **Vereniging** vormen. Voor dit, moet u het **Type van Verzoening** selecteren om te bepalen hoe de duplicaten worden behandeld:

* **Sleutels slechts**: dit is de standaardwijze. De activiteit behoudt slechts één element wanneer elementen van de verschillende binnenkomende overgangen dezelfde sleutel hebben. Deze optie kan alleen worden gebruikt als de binnenkomende populaties homogeen zijn.
* **een selectie van kolommen**: selecteer deze optie om de lijst van kolommen te bepalen waarop de gegevensverzoening wordt toegepast. U moet eerst de primaire set (de set met de brondata) selecteren en vervolgens de kolommen die u voor de samenvoeging wilt gebruiken.

## Doorsnede {#combine-intersection}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_reconciliation_options"
>title="Afstemmingsopties voor doorsnede"
>abstract="Selecteer het **Type van Verzoening** om te bepalen hoe te om duplicaten te behandelen. Door gebrek, wordt de **optie van Sleutels** geactiveerd, betekenend dat de activiteit slechts één element houdt wanneer de elementen van de verschillende binnenkomende overgangen de zelfde sleutel hebben. Gebruik de **selectie van A kolommen** optie om de lijst van kolommen te bepalen waarop de gegevensverzoening wordt toegepast."

In **combineer** activiteit, kunt u een **Intersection** vormen. Hiervoor moet u de volgende extra stappen volgen:

1. Selecteer het **Type van Verzoening** om te bepalen hoe de duplicaten worden behandeld. Zie [ Unie ](#union) sectie.
1. U kunt **controleren produceert volledigheid** optie als u wenst om de resterende bevolking te verwerken. Het complement zal de samenvoeging bevatten van de resultaten van alle binnenkomende activiteiten min de doorsnede. Een extra uitgaande overgang zal dan aan de activiteit worden toegevoegd.

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

In **combineer** activiteit, kunt u een **Uitsluiting** vormen. Hiervoor moet u de volgende extra stappen volgen:

1. In de **Reeksen om zich bij** sectie aan te sluiten, selecteer de **Primaire reeks** van de binnenkomende overgangen. Dit is de set waaruit elementen worden uitgesloten. De andere sets komen overeen met de elementen voordat deze worden uitgesloten van de primaire set.
1. Indien nodig, kunt u binnenkomende lijsten manipuleren. Om een doel van een andere dimensie uit te sluiten, moet dit doel worden teruggebracht naar dezelfde doeldimensie als het hoofddoel. Om dit te doen, klik **een regel** in de **sectie van de Regels van de Uitsluiting** toevoegen en de voorwaarden van de afmetingsverandering specificeren. Afstemming van gegevens vindt plaats via een attribuut of een join-functie.
1. U kunt **controleren produceert volledigheid** optie als u wenst om de resterende bevolking te verwerken. Zie de [ sectie van de Intersectie ](#intersection).

## Voorbeelden{#combine-examples}

In het volgende voorbeeld, gebruiken wij a **** activiteit combineren en wij voegen a **unie** toe om alle profielen van de twee vragen terug te winnen: personen tussen 18 en 27 jaar oud en personen tussen 34 en 40 jaar oud.

![](../assets/workflow-union-example.png)

Het volgende voorbeeld toont de **intersection** tussen twee vraagactiviteiten. Het wordt hier gebruikt om profielen op te halen die tussen 18 en 27 jaar oud zijn en waarvan e-mailadres is verstrekt.

![](../assets/workflow-intersection-example.png)

Het volgende **uitsluitings** voorbeeld toont twee vragen die aan filterprofielen worden gevormd die tussen 18 en 27 jaar oud zijn en een Adobe e-maildomein hebben. De profielen met een Adobe-e-maildomein worden dan uitgesloten van de eerste set.

![](../assets/workflow-exclusion-example.png)
