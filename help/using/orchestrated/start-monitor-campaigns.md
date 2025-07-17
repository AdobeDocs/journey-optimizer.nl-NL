---
solution: Journey Optimizer
product: journey optimizer
title: Gestroomlijnde campagnes met Adobe Journey Optimizer starten en volgen
description: Leer hoe u georkestreerde campagnes met Adobe Journey Optimizer kunt starten en volgen.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 0%

---

# Uw georkestreerde campagnes starten en controleren {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Georkestreerde campagne publiceren"
>abstract="Als u uw campagne wilt starten, moet u deze publiceren. Zorg ervoor dat alle fouten zijn gewist voordat u ze publiceert."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul><br/><br/>[ toegang en beheer georkestreerde campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Zeer belangrijke stappen om een georkestreerde campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/><b>[ Begin en controleer de campagne ](start-monitor-campaigns.md)</b><br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [&#128279;](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

Nadat u de georkestreerde en ontworpen taken hebt gemaakt die u op het canvas wilt uitvoeren, kunt u deze publiceren en controleren hoe deze wordt uitgevoerd.

U kunt de campagne ook in testmodus uitvoeren om de uitvoering en het resultaat van de verschillende activiteiten te controleren.

## Uw campagne testen vóór publicatie {#test}

Met [!DNL Journey Optimizer] kunt u georkestreerde campagnes testen voordat u live gaat. Wanneer een campagne wordt gecreeerd, gaat het de **staat van het Ontwerp** door gebrek in. In deze status kunt u de campagne handmatig uitvoeren om de stroom te testen.

Alle activiteiten op het canvas worden uitgevoerd, behalve **[!UICONTROL Save audience]** -activiteiten en kanaalactiviteiten. Er is geen functioneel effect op uw gegevens of publiek.

Een campagne testen:

1. Open de georkestreerde campagne.
2. Klik op **[!UICONTROL Start]**.

![](assets/campaign-start.png){zoomable="yes"}

Elke activiteit in de campagne wordt opeenvolgend uitgevoerd tot het eind van het diagram wordt bereikt.

Tijdens de test kunt u de uitvoering van de campagne besturen met de actiebalk op het canvas. Vanaf dat punt kunt u:

* **Einde** de uitvoering op elk ogenblik.
* **Begin** opnieuw de uitvoering.
* **hervat** de uitvoering als het eerder wegens een kwestie werd gepauzeerd.

Als tijdens de uitvoering een fout of waarschuwing optreedt, wordt u hiervan op de hoogte gesteld via het pictogram **[!UICONTROL Alerts]** / **[!UICONTROL Warning]** op de werkbalk Canvas.

![](assets/campaign-warning.png){zoomable="yes"}

U kunt ontbroken activiteiten ook snel identificeren gebruikend de [ visuele statusindicatoren ](#activities) die direct op elke activiteit worden getoond. Voor gedetailleerde het oplossen van problemen, open de [ logboeken van de campagne ](#logs-tasks), die diepgaande informatie over de fout en zijn context verstrekken.

Nadat de campagne is gevalideerd, kan deze worden gepubliceerd.

## De campagne publiceren {#publish}

Nadat uw campagne is getest en klaar is, klikt u op **[!UICONTROL Publish]** om deze actief te maken.

![](assets/campaign-publish.png){zoomable="yes"}

>[!NOTE]
>
>Als de knop **[!UICONTROL Publish]** is uitgeschakeld (grijs weergegeven), opent u de logbestanden via de actiebalk en controleert u de foutberichten. Alle fouten moeten worden gecorrigeerd voordat u een campagne kunt publiceren.

De visuele stroom begint opnieuw en echte profielen beginnen in real-time door de reis te stromen.

Als de publicatieactie mislukt (bijvoorbeeld als gevolg van ontbrekende berichtinhoud), wordt u gewaarschuwd en moet u het probleem verhelpen voordat u het opnieuw probeert. Bij succesvol publiceren, begint de campagne onmiddellijk uitvoerend (of op programma), beweegt zich van **Ontwerp** aan **Levende** status, en wordt &quot;Gelezen slechts&quot;.

## Campagne uitvoeren {#monitor}

### Visuele controle van de stroom {#flow}

Tijdens het uitvoeren (in test- of live modus) toont de visuele stroom hoe profielen in real-time door de reis bewegen. Het aantal profielen dat de overgang tussen taken maakt, wordt weergegeven.

![](assets/workflow-execution.png){zoomable="yes"}

Gegevens die van de ene activiteit naar de andere worden vervoerd via overgangen, worden opgeslagen in een tijdelijke werktabel. Deze gegevens kunnen voor elke overgang worden weergegeven. Gegevens die tussen activiteiten worden doorgegeven, inspecteren:

1. Selecteer een overgang.
1. Klik in het deelvenster Eigenschappen op **[!UICONTROL Preview schema]** om het schema van de werktabel weer te geven. Selecteer **[!UICONTROL Preview results]** om de getransporteerde gegevens weer te geven.

![](assets/transition.png){zoomable="yes"}

### Indicatoren voor de uitvoering van activiteiten {#activities}

De visuele statusindicatoren helpen u begrijpen hoe elke activiteit uitvoert:

| Visuele indicator | Beschrijving |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | De activiteit wordt momenteel uitgevoerd. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | De activiteit vereist uw aandacht. Dit kan inhouden dat de verzending van een levering wordt bevestigd of dat de nodige actie wordt ondernomen. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | Er is een fout opgetreden in de activiteit. Om het probleem op te lossen, opent u de georkestreerde campagnelogboeken voor meer informatie. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | De activiteit is met succes uitgevoerd. |

### Logboeken en taken {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Logboeken en taken"
>abstract="De **Logboeken en het 1&rbrace; scherm van taken &lbrace;verstrekken een geschiedenis van de georkestreerde campagneuitvoering, registrerend alle gebruikersacties en ondervonden fouten.**"

Het controleren van logboeken en taken is een zeer belangrijke stap om uw georkestreerde campagnes te analyseren en ervoor te zorgen zij behoorlijk lopen. Logbestanden en taken zijn toegankelijk via de knop **[!UICONTROL Logs]** , die beschikbaar is in zowel de test- als de live modus op de canvaswerkbalk of in het deelvenster Eigenschappen van elke activiteit.

Het scherm **[!UICONTROL Logs and tasks]** biedt een complete geschiedenis van de uitvoering van de campagne, waarin alle handelingen van de gebruiker zijn opgenomen en fouten zijn aangetroffen.

![](assets/workflow-logs.png){zoomable="yes"}

Er zijn twee soorten informatie beschikbaar:

* Het tabblad **[!UICONTROL Log]** bevat de chronologische geschiedenis van alle bewerkingen en fouten.
* Het tabblad **[!UICONTROL Tasks]** bevat de stapsgewijze uitvoeringsvolgorde van activiteiten.

Op beide tabbladen kunt u de weergegeven kolommen en hun volgorde kiezen, filters toepassen en het zoekveld gebruiken om snel de gewenste informatie te zoeken.
