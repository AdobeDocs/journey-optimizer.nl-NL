---
solution: Journey Optimizer
product: journey optimizer
title: Georkestreerde campagnes maken met Adobe Journey Optimizer
description: Leer hoe u georkestreerde campagnes kunt maken met Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 0%

---

# Gestroomlijnde campagneactiviteiten ordenen {#orchestrate}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de Vraag Modeler ](orchestrated-query-modeler.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening ](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md)[ |

{style="table-layout:fixed"}

+++

<br/><br/>

Zodra u [ een georkestreerde campagne ](gs-campaign-creation.md) hebt gecreeerd, of van het georkestreerde campagnemenu of binnen een campagne, kunt u beginnen de verschillende taken te ordenen het zal uitvoeren. Hiervoor wordt een visueel canvas verschaft, zodat u een georkestreerd campagnediagram kunt maken. Binnen dit diagram, kunt u diverse activiteiten toevoegen en hen in een opeenvolgende orde verbinden.

## Activiteiten toevoegen {#add}

In dit stadium van de configuratie, wordt het diagram getoond met een beginpictogram, dat het begin van uw georkestreerde campagne vertegenwoordigt. Als u uw eerste activiteit wilt toevoegen, klikt u op de knop **+** die is verbonden met het beginpictogram.

Er wordt een lijst met activiteiten weergegeven die aan het diagram kunnen worden toegevoegd. De beschikbare activiteiten zijn afhankelijk van uw positie binnen het georkestreerde campagnediagram. Bijvoorbeeld, wanneer het toevoegen van uw eerste activiteit, kunt u uw georkestreerde campagne beginnen door een publiek te richten, het georkestreerde campagneweg te verdelen, of a **te plaatsen wacht** activiteit om de georkestreerde campagneuitvoering te vertragen. Anderzijds, na a **bouwt publiek** activiteit, kunt u uw doel met het richten van activiteiten verfijnen, een levering naar uw publiek met kanaalactiviteiten verzenden, of het geordende campagneproces met de activiteiten van de stroomcontrole organiseren.

![](assets/workflow-start.png){zoomable="yes"}

Zodra een activiteit aan het diagram is toegevoegd, verschijnt een juiste ruit, toestaand u om de onlangs toegevoegde activiteit met specifieke montages te vormen. De gedetailleerde informatie over hoe te om elke activiteit te vormen is beschikbaar in [ deze sectie ](activities/about-activities.md).

![](assets/workflow-configure-activities.png){zoomable="yes"}

Herhaal dit proces om zoveel activiteiten toe te voegen als u wilt, afhankelijk van de taken die u voor uw georkestreerde campagne wilt uitvoeren. U kunt ook een nieuwe activiteit invoegen tussen twee activiteiten. Om dit te doen, klik **+** knoop op de overgang tussen de activiteiten, selecteer de gewenste activiteit en vorm het in de juiste ruit.

Om een activiteit te verwijderen, selecteer het op het canvas en klik **Schrapping** pictogram in de activiteiteneigenschappen.

>[!TIP]
>
>U kunt de naam van de overgangen tussen elke activiteit aanpassen. U doet dit door de overgang te selecteren en het label ervan te wijzigen in het rechterdeelvenster.

## De werkbalk {#toolbar}

De werkbalk in de rechterbovenhoek van het canvas bevat opties waarmee u de activiteiten eenvoudig kunt manipuleren en op het canvas kunt navigeren:

* **Veelvoudige selectiemodus**: Selecteer veelvoudige activiteiten om hen allen in één keer te schrappen of hen te kopiëren en te kleven. Zie [deze sectie](#copy).
* **roteer**: Verdraai verticaal het canvas.
* **Passend aan het scherm**: Pas het het gezoemniveau van het canvas aan uw scherm aan.
* **Gezoem uit** / **Gezoem binnen**: Gezoem uit of in het canvas.
* **kaart van de Vertoning**: Opent een momentopname van het canvas die u toont wordt gevestigd.

![](assets/workflow-toolbar.png){zoomable="yes"}{width="50%"}

## Activiteiten beheren {#manage}

Wanneer u activiteiten toevoegt, zijn er actieknoppen beschikbaar in het deelvenster Eigenschappen, zodat u meerdere bewerkingen kunt uitvoeren.

![](assets/activity-action.png){zoomable="yes"}

U kunt:

* **Schrap** de activiteit van het canvas.
* **onbruikbaar maken/laat** de activiteit toe. Wanneer de georkestreerde campagne wordt uitgevoerd, worden activiteiten met een handicap en de volgende activiteiten op hetzelfde pad niet uitgevoerd en wordt de georkestreerde campagne gestopt.
* **Pauze/hervat** de activiteit. Wanneer de georkestreerde campagne wordt uitgevoerd, pauzeert het bij de gepauzeerde activiteit. De bijbehorende taak en alle taken die deze in hetzelfde pad volgen, worden niet uitgevoerd.
* **Exemplaar** de activiteit. Zie [deze sectie](#copy).
* **beweging** een activiteit en al zijn kindknopen aan een andere overgang. Zie [ deze sectie ](#move)
* Heb toegang tot de opties van de activiteit **Uitvoering**.
* Heb toegang tot de Logboeken en de taken van de activiteit ****.

Verscheidene **richtend** activiteiten, zoals **combineren** of **Deduplicatie**, staat u toe om de resterende bevolking te verwerken en het in een extra uitgaande overgang te omvatten. Bijvoorbeeld, als u a **Gesplitste** activiteit gebruikt, bestaat de aanvulling uit de bevolking die om het even welke eerder bepaalde ondergroepen niet aanpast. Om dit vermogen te gebruiken, activeer **aanvult** optie.

![](assets/workflow-split-complement.png)

## Verplaatsen of kopiëren {#move-copy}

### Kopiëren en plakken {#copy}

U kunt georkestreerde campagneactiviteiten kopiëren en ze in elke werkstroom plakken. De doelgeorkestreerde campagne kan in een verschillende browser tabel zijn.

Voor het kopiëren van activiteiten hebt u twee mogelijkheden:

* Kopieer één activiteit gebruikend de actieknoop.

  ![](assets/workflow-copy.png){zoomable="yes"}{width="70%"}

* Kopieer meerdere activiteiten met de werkbalkknop.

  ![](assets/workflow-copy-2.png){zoomable="yes"}{width="70%"}

Als u de gekopieerde activiteiten wilt plakken, klikt u op de knop **+** in een overgang en selecteert u &quot;X-activiteit plakken&quot;.

![](assets/workflow-copy-3.png){zoomable="yes"}{width="50%"}

### Activiteiten verplaatsen en hun onderliggende knooppunten verplaatsen {#move}

Met Journey Optimizer kunt u een activiteit samen met de volledige inhoud van de onderliggende knooppunten (inclusief alle overgangen en activiteiten in de onderliggende knooppunten) verplaatsen naar het einde van een andere overgang binnen dezelfde geordende campagne.

Dit proces verbreekt de verbinding tussen de activiteit en alles in de uitgaande overgang van de oorspronkelijke locatie en verplaatst deze naar de nieuwe doelovergang.

Een activiteit verplaatsen:

1. Selecteer de activiteit die u wilt verplaatsen.
1. In de de eigenschappen van de activiteit ruit, klik de **knoop van de Beweging**.
1. Selecteer de overgang waar u de activiteit en zijn uitgaande overgang wilt plaatsen, dan bevestig.

![](assets/activity-move.png)

## Execution options {#execution}

Met alle activiteiten kunt u de uitvoeropties ervan beheren. Selecteer een activiteit en klik op de **opties van de Uitvoering** knoop. Hiermee kunt u de uitvoeringsmodus en het gedrag van de activiteit definiëren in het geval van fouten.

![](assets/workflow-execution-options.png){zoomable="yes"}{width="70%"}

### Properties

Het **gebied van de Uitvoering** staat u toe om de uit te voeren actie te bepalen wanneer de taak is begonnen.

Het **Maximale uitvoeringstijd** gebied staat u toe om een duur zoals &quot;30s&quot;of &quot;1h&quot;te specificeren. Als de activiteit niet wordt gebeëindigd nadat de gespecificeerde duur is verstreken, wordt een alarm teweeggebracht. Dit heeft geen invloed op de werking van de georkestreerde campagne.

Het **gebied van de tijdzone** staat u toe om de tijdzone van de activiteit te selecteren. Met Adobe Journey Optimizer kunt u de tijdsverschillen tussen meerdere landen op hetzelfde moment beheren. De toegepaste instelling wordt geconfigureerd wanneer de instantie wordt gemaakt.

**het 1} gebied van de affiniteit {staat u toe om een georkestreerde campagne of een georkestreerde campagneactiviteit te dwingen om op een bepaalde machine uit te voeren.** Hiervoor moet u een of meer affiniteiten opgeven voor de georkestreerde campagne of activiteit in kwestie.

Het **gebied van het Gedrag** staat u toe om de te volgen procedure te bepalen als de asynchrone taken worden gebruikt.

### Foutbeheer

Het **In geval van fout** gebied staat u toe om de uit te voeren actie te specificeren als de activiteit een fout ontmoet.

### Initialisatiescript

Het **manuscript van de Initialisatie** laat u variabelen initialiseren of activiteiteneigenschappen wijzigen. Klik **geef code** knoop uit en typ het fragment van uit te voeren code. Het script wordt aangeroepen wanneer de activiteit wordt uitgevoerd.

## Voorbeeld {#example}

Hier is een georkestreerd campagnevoorbeeld dat is ontworpen om een e-mail naar alle klanten (behalve klanten van VIP) met een e-mail te verzenden die in koffiemachines geinteresseerd zijn.

![](assets/workflow-example.png){zoomable="yes"}{zoomable="yes"}

Hiervoor zijn de volgende activiteiten toegevoegd:

* Een **[!UICONTROL Fork]** activiteit die de georkestreerde campagne in drie wegen (één voor elke reeks klant) verdeelt,
* **[!UICONTROL Build audience]** -activiteiten om zich te richten op de drie groepen klanten:

   * Klanten met een e-mail,
   * Klanten die behoren tot het reeds bestaande publiek &quot;Interrested in Coffee Machine(s)&quot;,
   * Klanten die tot het reeds bestaande &quot;VIP of bonus&quot;-publiek behoren.

* Een **[!UICONTROL Combine]** activiteit die klanten met een e-mail en degenen groepeert die in koffiemachines geinteresseerd zijn,
* Een **[!UICONTROL Combine]** -activiteit die VIP-klanten uitsluit,
* Een **[!UICONTROL Email delivery]** -activiteit die een e-mail naar de resulterende klanten verzendt.

Als u de georkestreerde campagne hebt voltooid, voegt u en **[!UICONTROL End]** activiteit toe aan het einde van het diagram. Met deze activiteit kunt u visueel het einde van een werkstroom markeren en heeft deze geen invloed op de functionaliteit.

Nadat het georkestreerde campagnediagram met succes is ontworpen, kunt u de georkestreerde campagne uitvoeren en de vooruitgang van zijn diverse taken volgen. [ Leer hoe te om een georkestreerde campagne te beginnen en zijn uitvoering te controleren ](start-monitor-campaigns.md)
