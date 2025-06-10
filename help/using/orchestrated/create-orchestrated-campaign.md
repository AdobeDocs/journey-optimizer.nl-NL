---
solution: Journey Optimizer
product: journey optimizer
title: Georkestreerde campagnes maken met Journey Optimizer
description: Leer hoe u een georkestreerde campagne kunt maken met Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 6574735581de0872e78e8e05efea5c6a50dc59b1
workflow-type: tm+mt
source-wordcount: '1668'
ht-degree: 0%

---


# Een georkestreerde campagne maken {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Lijst van georkestreerde campagnes"
>abstract="Het **multi-step** lusje maakt een lijst van alle georkestreerde campagne. Klik op de naam van een geordende campagne om deze te bewerken. Gebruik **creeer georkestreerde campagne** knoop om een nieuwe georkestreerde campagne toe te voegen."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Toegang en beheert georkestreerde camapens ](access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md)<br/><br/><b>[ creëren en vormen de campagne ](create-orchestrated-campaign.md)</b><br/><br/>[ activiteiten van het Orchestrate ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleren de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening ](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md)[ |

{style="table-layout:fixed"}

+++

<br/>

## Maak de campagne {#create}

Voer de volgende stappen uit om een georkestreerde campagne te maken:

1. Om a **georkestreerde campagne** tot stand te brengen, doorblader aan het **Campagnes** menu.

1. Klik op de knop **[!UICONTROL Create orchestrated campaign]** in de rechterbovenhoek van het scherm.

1. In de georkestreerde dialoog van campagneeigenschappen ****, selecteer het malplaatje te gebruiken om de georkestreerde campagne tot stand te brengen (u kunt het gebrek ingebouwde malplaatje ook gebruiken). [ Leer meer over georkestreerde campagnemalplaatjes ](#campaign-templates).

1. Voer een label in voor de georkestreerde campagne. Daarnaast raden we u ten zeerste aan een beschrijving toe te voegen aan uw georkestreerde campagne, in het speciale veld van de sectie **[!UICONTROL Additional options]** van het scherm.

1. Vouw de sectie **[!UICONTROL Additional options]** uit om meer instellingen voor de geordende campagne te configureren.

1. Klik op de knop **[!UICONTROL Create orchestrated campaign]** om het maken van uw georkestreerde campagne te bevestigen.

Uw georkestreerde campagne is nu gemaakt en beschikbaar in de lijst met workflows. U kunt nu het visuele canvas openen en de taken die het gaat uitvoeren, toevoegen, configureren en ordenen. [ Leer hoe te om georkestreerde campagneactiviteiten ](orchestrate-activities.md) te ordenen.

## De instellingen voor de campagne configureren {#settings}

<!--Overview of new admin settings> schemas, execution fields, merge policy. [Learn more](configuration-steps.md)-->

Wanneer u een georkestreerde campagne of georkestreerde campagneactiviteiten op het canvas maakt, hebt u toegang tot geavanceerde instellingen voor de georkestreerde campagne. U kunt bijvoorbeeld een specifieke tijdzone instellen voor de georkestreerde campagne, beheren hoe de georkestreerde campagne zich moet gedragen als er een fout optreedt, of de vertraging beheren waarna de georkestreerde campagnegeschiedenis moet worden gewist.

Deze montages worden pre-gevormd in het malplaatje dat wanneer het creëren van de georkestreerde campagne wordt geselecteerd, maar kunnen worden uitgegeven zoals nodig voor deze specifieke georkestreerde campagne.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

### Eigenschappen van geordende campagne {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Eigenschappen van geordende campagne"
>abstract="Deze sectie verstrekt generische georkestreerde campagneeigenschappen die ook toegankelijk zijn wanneer het creëren van de georkestreerde campagne. U kunt de sjabloon kiezen die u wilt gebruiken om de geordende campagne te maken en een label opgeven. Vouw de sectie Aanvullende opties uit om specifieke instellingen te configureren, zoals de geordende campagne waarin de map of tijdzone wordt opgeslagen."

De sectie **[!UICONTROL Properties]** biedt algemene instellingen die kunnen worden geconfigureerd wanneer u een geordende campagne maakt. Als u de eigenschappen van een bestaande georkestreerde campagne wilt openen, klikt u op de knop **[!UICONTROL Settings]** in de actiebalk boven het georkestreerde campagneccanvas.

![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}

Deze eigenschappen zijn:

* De **[!UICONTROL Label]** van de georkestreerde campagne die in de lijst wordt weergegeven.
* De **[!UICONTROL Internal name]** van de georkestreerde campagne.
* De **[!UICONTROL Folder]** locatie waar de georkestreerde campagne moet worden opgeslagen.
* De standaardwaarde **[!UICONTROL Timezone]** die moet worden gebruikt in alle activiteiten van de georkestreerde campagne. Standaard is de tijdzone van de georkestreerde campagne de tijdzone die is gedefinieerd voor de huidige campagneoperator.
Mogelijke waarden zijn:
   * **de tijdzone van de Server** om de tijdzone van uw organisatie van Adobe Experience Platform te gebruiken
   * **tijdzone van de Exploitant** om de tijdzone van de exploitant te gebruiken die de georkestreerde campagne uitvoert
   * **streek van de Tijd van het gegevensbestand** om de tijdzone van de gegevensbestandserver te gebruiken
   * Een specifieke tijdzone
* Wanneer een geordende campagne mislukt, worden de operatoren die tot de groep met operatoren behoren die in het veld **[!UICONTROL Supervisor(s)]** is geselecteerd, via e-mail op de hoogte gesteld.
* U kunt ook een **[!UICONTROL Description]** van uw georkestreerde campagne invoeren.

### Segmenteringsinstellingen  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Segmenteringsinstellingen"
>abstract="In deze sectie kunt u de doeldimensie selecteren voor doelprofielen in de georkestreerde campagne en ervoor kiezen om de worklow-resultaten tussen twee uitvoeringen te houden. Deze optie mag alleen voor testdoeleinden worden gebruikt en mag nooit in een productiegeorkestreerde campagne worden ingeschakeld."

* **[!UICONTROL Targeting dimension]**: selecteer de doeldimensie die u wilt gebruiken voor doelprofielen: ontvangers, begunstigden van contracten, operator, abonnees, enz.

* **[!UICONTROL Keep the result of interim populations between two executions]**: Standaard worden alleen de werktabellen van de laatste uitvoering van de georkestreerde campagne bewaard. Werktafels van eerdere executies worden gezuiverd door een technische georkestreerde campagne, die dagelijks wordt uitgevoerd.

  Als deze optie is ingeschakeld, worden de werktabellen ook bewaard nadat de georkestreerde campagne is uitgevoerd. U kunt het voor testende doeleinden gebruiken en daarom moet **slechts** op ontwikkeling of het opvoeren milieu&#39;s worden gebruikt. Het mag nooit worden gecontroleerd in een productiegeorkestreerde campagne.

### Instellingen voor uitvoering  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Instellingen voor uitvoering"
>abstract="In deze sectie kunt u instellingen configureren die betrekking hebben op de uitvoering van de workflow, zoals het aantal dagen dat de georkestreerde campagnegeschiedenis wordt bewaard."

* **[!UICONTROL History in days]** - Geeft het aantal dagen aan waarna de historie moet worden gewist. De geschiedenis bevat elementen die gerelateerd zijn aan de georkestreerde campagne: logboeken, taken, gebeurtenissen (technische objecten die gekoppeld zijn aan de georkestreerde campagnebewerking). De standaardwaarde is 30 dagen voor out-of-the-box georchestrated campagnemalplaatjes. De geschiedenis wordt gewist door de technische georkestreerde campagne van de Schoonmaak van het Gegevensbestand, die door gebrek dagelijks wordt uitgevoerd

  >[!IMPORTANT]
  >
  >Als het veld **[!UICONTROL History in days]** leeg blijft, wordt de waarde ervan beschouwd als &quot;1&quot;, wat betekent dat de historie na 1 dag wordt gewist.

* **[!UICONTROL Default affinity]**: Als uw installatie meerdere georkestreerde campagnemeservers bevat, gebruikt u dit veld om de server op te geven waarop de georkestreerde campagne wordt uitgevoerd. Dit dwingt de uitvoering van die georkestreerde campagne op een bepaalde server. U kunt elke bestaande affiniteitsnaam kiezen, maar gebruik geen spaties of leestekens. Als u verschillende servers gebruikt, geeft u verschillende namen op, gescheiden door komma&#39;s.

  >[!IMPORTANT]
  >
  >Als de waarde die in dit veld wordt gedefinieerd, op geen enkele server bestaat, blijft de geordende campagne in behandeling.


* **[!UICONTROL Save SQL queries in log]**: Schakel deze optie in om de SQL-query&#39;s van de workflmulti-step campagne nu op te slaan in de logboeken. Deze functionaliteit is gereserveerd voor geavanceerde gebruikers. Het is van toepassing op georkestreerde campagnes die gerichte activiteiten zoals **[!UICONTROL Build audience]** bevatten. Wanneer deze optie wordt toegelaten, worden de SQL vragen die naar het gegevensbestand tijdens georkestreerde campagneuitvoering worden verzonden getoond in de georkestreerde logboeken van de campagne, die u toestaan om hen te analyseren om vragen te optimaliseren of kwesties te diagnostiseren.

### Instellingen voor foutbeheer  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Instellingen voor foutbeheer"
>abstract="In deze sectie kunt u definiëren hoe fouten tijdens de uitvoering van de georkestreerde campagne moeten worden beheerd. U kunt ervoor kiezen het proces te pauzeren, een bepaald aantal fouten te negeren of de uitvoering van de georkestreerde campagne te stoppen."

* **[!UICONTROL Error management]**: in dit veld kunt u de acties definiëren die moeten worden uitgevoerd als een geordende campagnemaak fouten bevat. Er zijn drie mogelijke opties:

   * **[!UICONTROL Suspend the process]**: De georkestreerde campagne wordt automatisch gepauzeerd en de status verandert in **[!UICONTROL Failed]** . Zodra het probleem is opgelost, hervat u de georkestreerde campagne met de knoppen van **[!UICONTROL Resume]** .
   * **[!UICONTROL Ignore]**: De status van de taak die de fout heeft veroorzaakt, verandert in **[!UICONTROL Failed]** , maar de geordende campagne behoudt de status **[!UICONTROL Started]** . <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Abort the process]**: De georkestreerde campagne wordt automatisch gestopt en de status verandert in **[!UICONTROL Failed]** . Zodra het probleem is opgelost, start u de georkestreerde campagne opnieuw met de knoppen van **[!UICONTROL Start]** .

* **[!UICONTROL Consecutive errors]**: Dit veld wordt beschikbaar wanneer de **[!UICONTROL Ignore]** -waarde wordt geselecteerd in het **[!UICONTROL In case of errors]** -veld. U kunt opgeven hoeveel fouten kunnen worden genegeerd voordat het proces wordt gestopt. Zodra dit aantal wordt bereikt, verandert de georkestreerde campagnestatus in **[!UICONTROL Failed]**. Als de waarde van dit veld 0 is, wordt de geordende campagne nooit gestopt, ongeacht het aantal fouten.

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
