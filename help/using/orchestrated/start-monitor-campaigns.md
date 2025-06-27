---
solution: Journey Optimizer
product: journey optimizer
title: Gestroomlijnde campagnes met Adobe Journey Optimizer starten en volgen
description: Leer hoe u georkestreerde campagnes met Adobe Journey Optimizer kunt starten en volgen.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: f8afef4729e50b7c9899bf7f2fe282347220dfac
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---

# Uw georkestreerde campagnes starten en controleren {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Georkestreerde campagne publiceren"
>abstract="Als u uw campagne wilt starten, moet u deze publiceren. Zorg ervoor dat alle waarschuwingen zijn gewist voordat u ze publiceert."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ krijgen begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Toegang en beheert georkestreerde campagnes ](access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md)<br/><br/>[ creëren en plannen de campagne ](create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/><b>[ Begin en controleren de campagne ](start-monitor-campaigns.md)</b><br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening [&#128279;](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Nadat u de georkestreerde en ontworpen taken hebt gemaakt die u op het canvas wilt uitvoeren, kunt u deze publiceren en controleren hoe deze wordt uitgevoerd.

U kunt de campagne ook in testmodus uitvoeren om de uitvoering en het resultaat van de verschillende activiteiten te controleren.

## De georkestreerde campagne testen en publiceren {#test}

Met Journey Optimizer kunt u uw georkestreerde campagnes testen voordat u deze publiceert. Hierdoor kunt u de uitvoering en het resultaat controleren van de verschillende taken waaruit de campagne bestaat en heeft deze geen functioneel effect: alle activiteiten op het canvas worden uitgevoerd, behalve voor de activiteiten die van invloed zijn op **[!UICONTROL Save audience]** - en kanaalactiviteiten.

Als u een georkestreerde campagne wilt starten in de testmodus, opent u de geordende campagne en klikt u op de knop **[!UICONTROL Start]** .

![](assets/campaign-start.png){zoomable="yes"}

Zodra de georkestreerde campagne loopt, wordt elke activiteit in het canvas uitgevoerd in opeenvolgende orde, tot het eind van de georkestreerde campagne wordt bereikt.

Klik op de knop **[!UICONTROL Publish]** als uw campagne klaar is om live te gaan. De visuele stroom in het canvas wordt opnieuw gestart, zodat u de profielen in het diagram kunt verwerken.

## Geordende campagnes visuele stroom

Wanneer een georkestreerde campagne, of in testwijze of in productie loopt, kunt u de vooruitgang van de gerichte profielen door de verschillende taken in real time volgen gebruikend een visuele stroom. Hierdoor kunt u snel de status van elke activiteit en het aantal profielen identificeren dat tussen de activiteiten overgaat.

![](assets/workflow-execution.png){zoomable="yes"}

Gegevens die van de ene activiteit naar de andere worden vervoerd via overgangen, worden opgeslagen in een tijdelijke werktabel. Deze gegevens kunnen voor elke overgang worden weergegeven. Selecteer hiertoe een overgang om de eigenschappen ervan in de rechterkant van het scherm te openen.

* Klik op **[!UICONTROL Preview schema]** om het schema van de werktabel weer te geven.
* Klik op **[!UICONTROL Preview results]** om de gegevens te visualiseren die in de geselecteerde overgang worden verzonden.

![](assets/transition.png){zoomable="yes"}

## De uitvoering van de campagne controleren

### Activiteitenuitvoering controleren {#activities}

De visuele indicatoren in elk activiteitenvakje staan u toe om hun uitvoering te controleren:

| Visuele indicator | Beschrijving |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | De activiteit wordt momenteel uitgevoerd. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | De activiteit vereist uw aandacht. Dit kan inhouden dat de verzending van een levering wordt bevestigd of dat de nodige actie wordt ondernomen. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | Er is een fout opgetreden in de activiteit. Om het probleem op te lossen, opent u de georkestreerde campagnelogboeken voor meer informatie. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | De activiteit is met succes uitgevoerd. |

### Logboeken en taken controleren {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Logboeken en taken"
>abstract="De **Logboeken en het 1&rbrace; scherm van taken &lbrace;verstrekken een geschiedenis van de georkestreerde campagneuitvoering, registrerend alle gebruikersacties en ondervonden fouten.**"

Het controleren van logboeken en taken is een zeer belangrijke stap om uw georkestreerde campagnes te analyseren en ervoor te zorgen zij behoorlijk lopen. Ze zijn toegankelijk via het pictogram **[!UICONTROL Logs]** dat beschikbaar is in de werkbalk Handeling en in het deelvenster Eigenschappen van elke activiteit.

Het menu **[!UICONTROL Logs and tasks]** bevat een geschiedenis van de georkestreerde uitvoering van de campagne, waarin alle handelingen van de gebruiker zijn opgenomen en fouten zijn aangetroffen.

![](assets/workflow-logs.png){zoomable="yes"}

Er zijn twee soorten informatie beschikbaar:

* Het tabblad **[!UICONTROL Log]** bevat de uitvoeringsgeschiedenis van alle georkestreerde campagneactiviteiten. De uitgevoerde bewerkingen en uitvoeringsfouten worden chronologisch geïndexeerd.
* Het tabblad **[!UICONTROL Tasks]** bevat details over de uitvoeringsvolgorde van de activiteiten.

Op beide tabbladen kunt u de weergegeven kolommen en hun volgorde kiezen, filters toepassen en het zoekveld gebruiken om snel de gewenste informatie te zoeken.

## Opdrachten voor het uitvoeren van geordende campagne {#execution-commands}

De actiebalk in de rechterbovenhoek bevat opdrachten waarmee u de georkestreerde uitvoering van de campagne kunt beheren. U kunt:

* **[!UICONTROL Start]** / **[!UICONTROL Resume]** de uitvoering van de opdracht   georkestreerde campagne, die dan de status In progress krijgt. Als de georkestreerde campagne is gepauzeerd, wordt deze hervat, anders wordt de campagne gestart en worden de initiële activiteiten vervolgens geactiveerd.

* **[!UICONTROL Pause]** de uitvoering van de georkestreerde campagne, die vervolgens de status Gepauzeerd krijgt. Er zullen geen nieuwe activiteiten worden geactiveerd totdat de activiteiten worden hervat, maar de lopende activiteiten worden niet opgeschort.

* **[!UICONTROL Stop]** een georkestreerde campagne die wordt uitgevoerd en die vervolgens de status Voltooid krijgt. De lopende bewerkingen worden indien mogelijk onderbroken. U kunt de georkestreerde campagne niet hervatten vanaf dezelfde plaats als waar ze is gestopt.
