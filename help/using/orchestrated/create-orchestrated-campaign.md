---
solution: Journey Optimizer
product: journey optimizer
title: Georkestreerde campagnes maken met Journey Optimizer
description: Leer hoe u een georkestreerde campagne kunt maken met Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 450f83eb53068df10a63d39d1a43483ad3c7e803
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 1%

---


# Een georkestreerde campagne maken {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Lijst van georkestreerde campagnes"
>abstract="Het **multi-step** lusje maakt een lijst van alle georkestreerde campagne. Klik op de naam van een geordende campagne om deze te bewerken. Gebruik **creeer georkestreerde campagne** knoop om een nieuwe georkestreerde campagne toe te voegen."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md) | <b>[ creeer een georkestreerde campagne ](create-orchestrated-campaign.md)</b><br/><br/>[ Geordende campagnes ](orchestrated-campaign-settings.md)<br/><br/>[ activiteiten van het Orchestrate ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening ](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md)[ |

{style="table-layout:fixed"}

+++

<br/>

## Maak de campagne

Voer de volgende stappen uit om een georkestreerde campagne te maken:

1. Om a **georkestreerde campagne** tot stand te brengen, doorblader aan het **Campagnes** menu.

1. Klik op de knop **[!UICONTROL Create orchestrated campaign]** in de rechterbovenhoek van het scherm.

1. In de georkestreerde dialoog van campagneeigenschappen ****, selecteer het malplaatje te gebruiken om de georkestreerde campagne tot stand te brengen (u kunt het gebrek ingebouwde malplaatje ook gebruiken). [ Leer meer over georkestreerde campagnemalplaatjes ](#campaign-templates).

1. Voer een label in voor de georkestreerde campagne. Daarnaast raden we u ten zeerste aan een beschrijving toe te voegen aan uw georkestreerde campagne, in het speciale veld van de sectie **[!UICONTROL Additional options]** van het scherm.

1. Vouw de sectie **[!UICONTROL Additional options]** uit om meer instellingen voor de geordende campagne te configureren.

1. Klik op de knop **[!UICONTROL Create orchestrated campaign]** om het maken van uw georkestreerde campagne te bevestigen.

Uw georkestreerde campagne is nu gemaakt en beschikbaar in de lijst met workflows. U kunt nu het visuele canvas openen en de taken die het gaat uitvoeren, toevoegen, configureren en ordenen. [ Leer hoe te om georkestreerde campagneactiviteiten ](orchestrate-activities.md) te ordenen.

## De instellingen voor de campagne configureren

Overzicht van nieuwe beheerinstellingen> schema&#39;s, uitvoeringsvelden, samenvoegbeleid. [Meer informatie](configuration-steps.md)

## Werken met georkestreerde campagnemalplaatjes {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Geordende campagnesjablonen"
>abstract="Geordende campagnemalplaatjes bevatten vooraf geconfigureerde instellingen en activiteiten die opnieuw kunnen worden gebruikt voor het maken van nieuwe geordende campagne."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Eigenschappen van geordende campagne"
>abstract="Geordende campagnemalplaatjes bevatten vooraf geconfigureerde instellingen en activiteiten die opnieuw kunnen worden gebruikt voor het maken van nieuwe georkestreerde campagnes. In dit scherm, ga het etiket van het geordende campagnemalplaatje in en vorm zijn montages zoals zijn interne naam, omslag en uitvoeringsomslagen, timezone, en supervisorgroep."

Geordende campagnemalplaatjes bevatten vooraf geconfigureerde instellingen en activiteiten die opnieuw kunnen worden gebruikt voor het maken van nieuwe georkestreerde campagnes. U kunt het malplaatje van uw georkestreerde campagne van de georkestreerde campagneeigenschappen selecteren, wanneer het creëren van een georkestreerde campagne. Er wordt standaard een lege sjabloon weergegeven.

U kunt een sjabloon maken op basis van een bestaande georkestreerde campagne of een nieuwe sjabloon maken op basis van een blanco sjabloon. Beide methoden worden hieronder beschreven.

>[!BEGINTABS]

>[!TAB  creeer een malplaatje van een bestaande georkestreerde campagne ]

Voer de volgende stappen uit om een georkestreerd campagnemalplaatje te maken op basis van een bestaande georkestreerde campagne:

1. Open aan het **menu van de Campagne** en doorblader aan de georkestreerde campagne om als malplaatje te bewaren.
1. Klik de drie punten op het recht van de naam van de georkestreerde campagne, en kies **Exemplaar als malplaatje**.
1. Bevestig het maken van de sjabloon in het pop-upvenster.
1. In het georkestreerde canvas van het campagnemalplaatje, controleer, voeg, en vorm de activiteiten toe zoals nodig.
1. Blader aan de montages, van de **knoop van Montages**, om de naam van het georkestreerde campagnemalplaatje te veranderen, en een beschrijving in te gaan.
1. Selecteer de **omslag** en **uitvoeringsomslag** van het malplaatje. De map is de locatie waar de georkestreerde campagnemalplaatje wordt opgeslagen. De uitvoeringsmap is de map waarin georkestreerde campagnes worden opgeslagen die op basis van deze sjabloon zijn gemaakt.
1. Sla uw wijzigingen op.

Het georkestreerde campagnemalplaatje is nu beschikbaar in de malplaatjelijst. U kunt een geordende campagne maken op basis van deze sjabloon. Deze geordende campagne wordt vooraf geconfigureerd met de instellingen en activiteiten die in de sjabloon zijn gedefinieerd.


>[!TAB  creeer een malplaatje van kras ]


Voer de volgende stappen uit om een geheel nieuwe geordende campagnemalplaatje te maken:

1. Open aan het **menu van de Campagne** en doorblader aan de **Malplaatjes** tabel. U kunt de lijst van beschikbare georkestreerde campagnemalplaatjes zien.
1. Klik op de knop **[!UICONTROL Create template]** in de rechterbovenhoek van het scherm.
1. Voer het label in en open de extra opties om een beschrijving van de georkestreerde campagnemalplaatje in te voeren.
1. Selecteer de map en de uitvoeringsmap van de sjabloon. De map is de locatie waar de georkestreerde campagnemalplaatje wordt opgeslagen. De uitvoeringsmap is de map waarin georkestreerde campagnes worden opgeslagen die op basis van deze sjabloon zijn gemaakt.
1. Klik **creeer** knoop om uw montages te bevestigen.
1. In het georkestreerde canvas van het campagnemalplaatje, voeg en vorm de activiteiten toe zoals nodig.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Sla uw wijzigingen op.

Het georkestreerde campagnemalplaatje is nu beschikbaar in de malplaatjelijst. U kunt een geordende campagne maken op basis van deze sjabloon. Deze geordende campagne wordt vooraf geconfigureerd met de instellingen en activiteiten die in de sjabloon zijn gedefinieerd.

>[!ENDTABS]
