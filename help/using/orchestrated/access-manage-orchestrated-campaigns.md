---
solution: Journey Optimizer
product: journey optimizer
title: Georkesterde campagne openen en beheren
description: Leer de belangrijkste principes van het maken van georkestreerde campagnes met Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Georkesterde campagne openen en beheren {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Geordende campagne"
>abstract="In dit scherm, kunt u tot de volledige lijst van georkestreerde campagnes toegang hebben, hun huidige status, laatste/volgende uitvoeringsdata controleren, en een nieuwe georkestreerde campagne creëren."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Actie"
>abstract="In deze secties worden alle acties weergegeven die in de georkestreerde campagne worden gebruikt."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](gs-schemas.md)</li><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul><br/><br/><b>[ toegang en beheer georkestreerde campagnes ](access-manage-orchestrated-campaigns.md)</b><br/><br/>[ Zeer belangrijke stappen om een georkestreerde campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [&#128279;](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

## Toegang tot georkestreerde campagnes

Navigeer naar het menu **[!UICONTROL Campaigns]** en selecteer het tabblad **[!UICONTROL Orchestration]** voor toegang tot de volledige lijst met georkestreerde campagnes.

![ beeld dat de georkestreerde campagneinventaris ](assets/inventory.png){zoomable="yes"}{zoomable="yes"} toont

Elke georkestreerde campagne in de lijst toont informatie zoals de huidige [ status van de campagne ](#status), het bijbehorende kanaal en de markeringen, of de laatste tijd het werd gewijzigd. U kunt de getoonde kolommen aanpassen door ![ te klikken vormt lay-outknoop ](assets/do-not-localize/inventory-configure-layout.svg).

Bovendien zijn er een zoekbalk en filters beschikbaar waarmee u gemakkelijk in de lijst kunt zoeken. U kunt bijvoorbeeld de georkestreerde campagnes filteren om alleen de campagnes weer te geven die aan een bepaald kanaal of label zijn gekoppeld, of de campagnes die tijdens een specifiek datumbereik zijn gemaakt.

Het ![ beeld dat de Meer knoop van acties ](assets/do-not-localize/rule-builder-icon-more.svg) in de campagneinventaris toont staat u toe om diverse hieronder gedetailleerde verrichtingen uit te voeren.

![ beeld de campagnevoorraad ](assets/inventory-actions.png)

* **[!UICONTROL View all time report]** / **[!UICONTROL View last 24 hours report]** - Gebruik rapporten om de impact en prestaties van uw georkestreerde campagnes te meten en te visualiseren. [ Leer meer op georkestreerde campagnes die ](../orchestrated/reporting-campaigns.md) melden
* **[!UICONTROL Edit tags]** - Bewerk de tags die aan de campagne zijn gekoppeld.
* **[!UICONTROL Duplicate]** - In sommige gevallen moet u mogelijk een geordende campagne dupliceren, bijvoorbeeld om een gestopt campagne uit te voeren of om de uitvoeringsfrequentie van een geplande campagne te wijzigen.
* **[!UICONTROL Delete]** - Verwijder de campagne. Deze acties zijn alleen beschikbaar voor **[!UICONTROL Draft]** -campagnes.
* **[!UICONTROL Archive]** - Archiveer de campagne. Alle gearchiveerde campagnes worden verwijderd als de planning 30 dagen na de laatste gewijzigde datum doorloopt. Deze actie is beschikbaar voor alle campagnes behalve **[!UICONTROL Draft]** campagnes.

## Wat zit er in een georkestreerde campagne? {#gs-ms-campaign-inside}

De georkestreerde campagnedoek is een voorstelling van wat er moet gebeuren. Hierin worden de verschillende taken beschreven die moeten worden uitgevoerd en hoe deze aan elkaar zijn gekoppeld.

![ beeld dat een georkestreerd campagnecanvas ](assets/canvas-example.png) toont

Elke georkestreerde campagne bevat:

* **Activiteiten**: Een activiteit is een uit te voeren taak. De verschillende activiteiten worden op het diagram weergegeven door pictogrammen. Elke activiteit heeft specifieke eigenschappen en andere eigenschappen die voor alle activiteiten gemeenschappelijk zijn.

  In een geordend campagnediagram, kan een bepaalde activiteit veelvoudige taken veroorzaken, in het bijzonder wanneer er een lijn of terugkerende acties is.

* **Overgangen**: De overgangen verbinden een bronactiviteit met een bestemmingsactiviteit en bepalen hun opeenvolging.

* **Worktables**: De werklijst bevat alle informatie die door de overgang wordt gedragen. Voor elke georkestreerde campagne worden verschillende worktables gebruikt. De gegevens in deze tabellen kunnen gedurende de gehele levenscyclus van de georkestreerde campagne worden gebruikt.

## Campagnestatussen {#status}

Geordende campagnes kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: De georkestreerde campagne is gemaakt. Het is nog niet gepubliceerd.
* **[!UICONTROL Publishing]**: De georkestreerde campagne wordt gepubliceerd.
* **[!UICONTROL Live]**: De georkestreerde campagne is gepubliceerd en wordt uitgevoerd.
* **[!UICONTROL Scheduled]**: De uitvoering van de georkestreerde campagne is gepland.
* **[!UICONTROL Completed]**: De uitvoering van de georkestreerde campagne is voltooid. De voltooide status wordt automatisch toegewezen tot 3 dagen nadat een campagne berichten die zonder fout verzenden heeft voltooid.
* **[!UICONTROL Closed]**: Deze status wordt weergegeven wanneer een terugkerende campagne is gesloten. De campagne gaat door tot alle activiteiten zijn voltooid, maar er kunnen geen profielen meer worden opgenomen in de campagne.
* **[!UICONTROL Archived]**: De georkestreerde campagne is gearchiveerd. Alle gearchiveerde campagnes worden verwijderd als de planning 30 dagen na de laatste gewijzigde datum wordt gewijzigd. U kunt een gearchiveerde campagne zo nodig dupliceren om eraan te kunnen blijven werken.
* **[!UICONTROL Stopped]**: De uitvoering van de georkestreerde campagne is gestopt. Als u de campagne opnieuw wilt starten, moet u deze dupliceren.
