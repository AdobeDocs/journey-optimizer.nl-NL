---
solution: Journey Optimizer
product: journey optimizer
title: Belangrijke stappen voor het maken van georkestreerde campagnes
description: Leer de belangrijkste principes van het maken van georkestreerde campagnes met Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# Belangrijke stappen voor het maken van georkestreerde campagnes {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Geordende campagne"
>abstract="In dit scherm, kunt u tot de volledige lijst van georkestreerde campagnes toegang hebben, hun huidige status, laatste/volgende uitvoeringsdata controleren, en een nieuwe georkestreerde campagne creëren."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de Vraag Modeler ](orchestrated-query-modeler.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening ](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md)[ |

{style="table-layout:fixed"}

+++

<br/><br/>

U kunt georkestreerde campagnes in een visueel canvas bouwen om kanaalprocessen zoals segmentatie, campagneuitvoering, dossierverwerking te ontwerpen.

## Toegang tot georkestreerde campagnes

Blader in het menu **[!UICONTROL Campaigns]** naar het tabblad In meerdere stappen om de volledige lijst met georkestreerde campagnes te openen.

Elk georkestreerde campagne in de lijst toont informatie over zijn huidige [ status ](#status), de laatste tijd het werd uitgevoerd of, en de volgende geplande uitvoeringsdatum en tijd gewijzigd.

U kunt de weergegeven kolommen aanpassen door op het pictogram **[!UICONTROL Configure column for a custom layout]** in de rechterbovenhoek van de lijst te klikken. Hierdoor kunt u aanvullende informatie aan de lijst toevoegen, zoals de laatste foutactie voor elke georkestreerde campagne of de toegepaste doeldimensie.

Bovendien zijn er een zoekbalk en filters beschikbaar waarmee u gemakkelijk in de lijst kunt zoeken. U kunt bijvoorbeeld de georkestreerde campagnes filteren om alleen de campagnes weer te geven die tot een campagne behoren, of de campagnes die tijdens een bepaald datumbereik zijn verwerkt.

Als u een georkestreerde campagne wilt dupliceren of verwijderen, klikt u op de knop Ovaal en selecteert u **[!UICONTROL Duplicate]** of **[!UICONTROL Delete]** .

>[!NOTE]
>
>Wanneer een georkestreerde campagne in uitvoering is, kunt u deze dupliceren, maar u kunt deze niet verwijderen.

## Wat zit er in een georkestreerde campagne? {#gs-ms-campaign-inside}

De georkestreerde campagnedoek is een voorstelling van wat er moet gebeuren. Hierin worden de verschillende taken beschreven die moeten worden uitgevoerd en hoe deze aan elkaar zijn gekoppeld.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Elke georkestreerde campagne bevat:

* **Activiteiten**: Een activiteit is een uit te voeren taak. De verschillende activiteiten worden op het diagram weergegeven door pictogrammen. Elke activiteit heeft specifieke eigenschappen en andere eigenschappen die voor alle activiteiten gemeenschappelijk zijn.

  In een geordend campagnediagram, kan een bepaalde activiteit veelvoudige taken veroorzaken, in het bijzonder wanneer er een lijn of terugkerende acties is.

* **Overgangen**: De overgangen verbinden een bronactiviteit met een bestemmingsactiviteit en bepalen hun opeenvolging.

* **Worktables**: De werklijst bevat alle informatie die door de overgang wordt gedragen. Voor elke georkestreerde campagne worden verschillende worktables gebruikt. De gegevens in deze tabellen kunnen gedurende de gehele levenscyclus van de georkestreerde campagne worden gebruikt.

## Statussen en levenscyclus {#status}

Campagnes kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: De georkestreerde campagne is gemaakt en opgeslagen.
* **[!UICONTROL In progress]**: De georkestreerde campagne wordt momenteel uitgevoerd.
* **[!UICONTROL Finished]**: De uitvoering van de georkestreerde campagne is voltooid.
* **[!UICONTROL Paused]**: De georkestreerde campagne is gepauzeerd.
* **[!UICONTROL Erroneous]**: Er is een fout opgetreden tijdens de georkestreerde campagne. Open de georkestreerde campagne en open de logboeken en de taken om de fout te identificeren en het op te lossen.
