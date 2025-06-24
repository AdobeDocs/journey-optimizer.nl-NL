---
solution: Journey Optimizer
product: journey optimizer
title: Georkesterde campagne openen en beheren
description: Leer de belangrijkste principes van het maken van georkestreerde campagnes met Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: 7e378cbda6ee2379a8bd795588c328cb14107aa4
workflow-type: tm+mt
source-wordcount: '624'
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
| [ wordt begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/><b>[ Toegang en beheert georkestreerde camapens ](access-manage-orchestrated-campaigns.md)</b> | [ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md)<br/><br/>[ creëren en plannen de campagne ](create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleren de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening ](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md)[ |

{style="table-layout:fixed"}

+++

<br/>

## Toegang tot georkestreerde campagnes

Navigeer naar het menu **[!UICONTROL Campaigns]** en selecteer het tabblad **[!UICONTROL Orchestration]** voor toegang tot de volledige lijst met georkestreerde campagnes.

![ beeld dat de georkestreerde campagneinventaris ](assets/inventory.png){zoomable="yes"}{zoomable="yes"} toont

Elke georkestreerde campagne in de lijst toont informatie zoals de huidige [ status van de campagne ](#status), het bijbehorende kanaal en de markeringen, of de laatste tijd het werd gewijzigd. U kunt de getoonde kolommen aanpassen door ![ te klikken vormt lay-outknoop ](assets/do-not-localize/inventory-configure-layout.svg).

Bovendien zijn er een zoekbalk en filters beschikbaar waarmee u gemakkelijk in de lijst kunt zoeken. U kunt bijvoorbeeld de georkestreerde campagnes filteren om alleen de campagnes weer te geven die aan een bepaald kanaal of label zijn gekoppeld, of de campagnes die tijdens een specifiek datumbereik zijn gemaakt.

## Wat zit er in een georkestreerde campagne? {#gs-ms-campaign-inside}

De georkestreerde campagnedoek is een voorstelling van wat er moet gebeuren. Hierin worden de verschillende taken beschreven die moeten worden uitgevoerd en hoe deze aan elkaar zijn gekoppeld.

![ beeld dat een georkestreerd campagnecanvas ](assets/canvas-example.png){zoomable="yes"}{zoomable="yes"} toont

Elke georkestreerde campagne bevat:

* **Activiteiten**: Een activiteit is een uit te voeren taak. De verschillende activiteiten worden op het diagram weergegeven door pictogrammen. Elke activiteit heeft specifieke eigenschappen en andere eigenschappen die voor alle activiteiten gemeenschappelijk zijn.

  In een geordend campagnediagram, kan een bepaalde activiteit veelvoudige taken veroorzaken, in het bijzonder wanneer er een lijn of terugkerende acties is.

* **Overgangen**: De overgangen verbinden een bronactiviteit met een bestemmingsactiviteit en bepalen hun opeenvolging.

* **Worktables**: De werklijst bevat alle informatie die door de overgang wordt gedragen. Voor elke georkestreerde campagne worden verschillende worktables gebruikt. De gegevens in deze tabellen kunnen gedurende de gehele levenscyclus van de georkestreerde campagne worden gebruikt.

## Campagnestatussen {#status}

Geordende campagnes kunnen meerdere statussen hebben:

terugkerende start à s&#39;executer , fait une query .click close: va continuer et se termienr quand elle sera allée jusqu&#39;au bout du diagram


* **[!UICONTROL Draft]**: De georkestreerde campagne is gemaakt. Het is nog niet gepubliceerd.
* **[!UICONTROL Publishing]**: De georkestreerde campagne wordt gepubliceerd.
* **[!UICONTROL Live]**: De georkestreerde campagne is gepubliceerd en wordt uitgevoerd.
* **[!UICONTROL Scheduled]**: De uitvoering van de georkestreerde campagne is gepland.
* **[!UICONTROL Completed]**: De uitvoering van de georkestreerde campagne is voltooid. De voltooide status wordt automatisch toegewezen tot 3 dagen nadat een campagne berichten die zonder fout verzenden heeft voltooid.
* **[!UICONTROL Closed]**: Deze status wordt weergegeven wanneer een terugkerende campagne is gestopt.
<!--Comment une campaign devient Closed?
[CPR] : A vérifier avec Fred si cette fonctionalité est toujours d'actualité. Normalement c'est sur action de l'utilisateur sur une campaine récurrente only
= pas trouvé--> cexui qsui sont déjà entrés ocnitnuent. on ferme les portes d'entrée.

* **[!UICONTROL Archived]**: De georkestreerde campagne is gearchiveerd. Alle gearchiveerde campagnes worden verwijderd als de planning 30 dagen na de laatste gewijzigde datum wordt gewijzigd. U kunt een gearchiveerde campagne zo nodig dupliceren om eraan te kunnen blijven werken.
<!--Comment une campaign devient Archived?
[CPR] : Soit par action manuel sur une campagne en statut "final" (Completed, Closed, Stopped, etc. ...) bouton bientôt visible. possible pour tout sauf les draft.
= pas trouvé -->
* **[!UICONTROL Stopped]**: De uitvoering van de georkestreerde campagne is gestopt. Als u de campagne opnieuw wilt starten, moet u deze dupliceren. si erreur , restera avec triangle

## Georkesterde campagnes dupliceren en verwijderen {#duplicate-delete}

In sommige gevallen moet u mogelijk een georkestreerde campagne dupliceren, bijvoorbeeld om een campagne uit te voeren die is gestopt of om de uitvoeringsfrequentie van een geplande campagne te wijzigen. Om dit te doen, klik het ![ beeld dat de Meer actieknoop ](assets/do-not-localize/rule-builder-icon-more.svg) toont in de campagneinventaris dan uitgezocht **[!UICONTROL Duplicate]**

<!--Une fois une campaign Scheduled, on ne peut plus changer l'execution frequency = la solution est de dupliquer la campaign ?
[CPR] : Actuellement oui, mais on est en discussion pour pouvoir revenir en mode "draft" et quelles seraient les actions à nouveau disponibles. A vérifier avec Fred-->

Om een campagne te schrappen, klik het ![ beeld dat de Meer actieknoop ](assets/do-not-localize/rule-builder-icon-more.svg) toont dan selecteren **[!UICONTROL Delete]**.

>[!NOTE]
>
>Alleen **[!UICONTROL Draft]** -campagnes kunnen worden verwijderd.
