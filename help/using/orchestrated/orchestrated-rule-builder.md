---
solution: Journey Optimizer
product: journey optimizer
title: Werken met de regelbouwer
description: Leer hoe u regels maakt voor uw georkestreerde campagnes
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---


# Werken met de regelbouwer {#orchestrated-rule-builder}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening ](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md)[ |

{style="table-layout:fixed"}

+++

<br/>

Geordende campagnes komen met een regelbouwer die het proces vereenvoudigt om het gegevensbestand te filtreren dat op diverse criteria wordt gebaseerd. De bouwer van de regel beheert zeer complexe en lange vragen efficiënt, die grotere flexibiliteit en precisie aanbieden.

Het steunt ook vooraf bepaalde filters binnen voorwaarden, die gebruikers machtigen om vragen te verfijnen terwijl het gebruiken van geavanceerde uitdrukkingen en exploitanten voor uitvoerige publiek richtend en segmenteringsstrategieën.

## Heb toegang tot de regelbouwer

De bouwer van de regel is beschikbaar wanneer het bouwen van een vraag in een **[!UICONTROL Build audience]** activiteit om een publiek te richten. Hiermee kunt u opgeven voor welke populatie u zich wilt richten en eenvoudig nieuwe soorten publiek maken die zijn afgestemd op uw behoeften.

![ beeld dat een activiteit van het bouwstijlpubliek toont ](assets/rule-builder-query.png)

## Interface van Rule builder {#interface}

De regelbouwer verstrekt een centraal canvas waar u uw vraag en een eigenschappenruit bouwt die informatie over de regel verstrekt.

![ Beeld die de interface van de regelbouwer tonen ](assets/rule-builder-interface.png)

* Het **centrale canvas** is waar u toevoegt en de verschillende componenten combineert om uw regel te bouwen. Een werkbalk bevat opties voor het eenvoudig manipuleren van de regelcomponenten:

  | Werkbalkpictogram | Beschrijving |
  |--- |--- |
  | ![ Beweging omhoog selectiepictogram ](assets/do-not-localize/rule-builder-icon-up.svg) | Verplaats de component omhoog een rij. |
  | ![ Beweging onderaan selectiepictogram ](assets/do-not-localize/rule-builder-icon-down.svg) | Verplaats de component een rij omlaag. |
  | ![ het selectiepictogram van de Groep ](assets/do-not-localize/rule-builder-icon-group.svg) | Plaats twee componenten in een groep. |
  | ![ Ungroup selectiepictogram ](assets/do-not-localize/rule-builder-icon-ungroup.svg) | Scheid de componenten van één groep. |
  | ![ breid al pictogram ](assets/do-not-localize/rule-builder-icon-expand.svg) uit | Vouw alle groepen uit. |
  | ![ Vouw al pictogram ](assets/do-not-localize/rule-builder-icon-collapse.svg) samen | Vouw alle groepen samen. |
  | ![ verwijder al pictogram ](assets/do-not-localize/rule-builder-icon-delete.svg) | Alle groepen en componenten verwijderen. |

* Het deelvenster **[!UICONTROL Rule properties]** bevat informatie over uw regel. Het staat u toe om diverse handelingen uit te voeren om de regel te controleren en ervoor te zorgen het uw behoeften aanpast.

  Dit deelvenster wordt weergegeven wanneer u een query samenstelt om een publiek te maken. [ leer hoe te om uw vraag te controleren en te bevestigen ](build-query.md#check-and-validate-your-query)
