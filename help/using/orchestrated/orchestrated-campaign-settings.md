---
solution: Journey Optimizer
product: journey optimizer
title: Instellingen voor georkestreerde campagnes configureren
description: Leer hoe u georkestreerde campagne-instellingen kunt configureren met Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: a9bb3782-a4d1-43fe-ae2a-aef3f17ba588
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 0%

---

# Instellingen voor georkestreerde campagnes configureren {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="Eigenschappen van geordende campagne"
>abstract="Kies in dit scherm de sjabloon die u wilt gebruiken om de geordende campagne te maken en geef een label op. Vouw de **Extra opties** sectie uit om meer montages zoals de georkestreerde interne naam van de campagne, zijn omslag, timezone, en supervisorgroep te vormen. Het wordt hoogst geadviseerd om een supervisorgroep te selecteren zodat de exploitanten worden gealarmeerd als een fout voorkomt."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de Vraag Modeler ](orchestrated-query-modeler.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening ](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md)[ |

{style="table-layout:fixed"}

+++

<br/><br/>

Wanneer u een georkestreerde campagne of georkestreerde campagneactiviteiten op het canvas maakt, hebt u toegang tot geavanceerde instellingen voor de georkestreerde campagne. U kunt bijvoorbeeld een specifieke tijdzone instellen voor de georkestreerde campagne, beheren hoe de georkestreerde campagne zich moet gedragen als er een fout optreedt, of de vertraging beheren waarna de georkestreerde campagnegeschiedenis moet worden gewist.

Deze montages worden pre-gevormd in het malplaatje dat wanneer het creëren van de georkestreerde campagne wordt geselecteerd, maar kunnen worden uitgegeven zoals nodig voor deze specifieke georkestreerde campagne.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## Eigenschappen van geordende campagne {#properties}

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

## Segmenteringsinstellingen  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Segmenteringsinstellingen"
>abstract="In deze sectie kunt u de doeldimensie selecteren voor doelprofielen in de georkestreerde campagne en ervoor kiezen om de worklow-resultaten tussen twee uitvoeringen te houden. Deze optie mag alleen voor testdoeleinden worden gebruikt en mag nooit in een productiegeorkestreerde campagne worden ingeschakeld."

* **[!UICONTROL Targeting dimension]**: selecteer de doeldimensie die u wilt gebruiken voor doelprofielen: ontvangers, begunstigden van contracten, operator, abonnees, enz.

* **[!UICONTROL Keep the result of interim populations between two executions]**: Standaard worden alleen de werktabellen van de laatste uitvoering van de georkestreerde campagne bewaard. Werktafels van eerdere executies worden gezuiverd door een technische georkestreerde campagne, die dagelijks wordt uitgevoerd.

  Als deze optie is ingeschakeld, worden de werktabellen ook bewaard nadat de georkestreerde campagne is uitgevoerd. U kunt het voor testende doeleinden gebruiken en daarom moet **slechts** op ontwikkeling of het opvoeren milieu&#39;s worden gebruikt. Het mag nooit worden gecontroleerd in een productiegeorkestreerde campagne.

## Instellingen voor uitvoering  {#exec-settings}

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

## Instellingen voor foutbeheer  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Instellingen voor foutbeheer"
>abstract="In deze sectie kunt u definiëren hoe fouten tijdens de uitvoering van de georkestreerde campagne moeten worden beheerd. U kunt ervoor kiezen het proces te pauzeren, een bepaald aantal fouten te negeren of de uitvoering van de georkestreerde campagne te stoppen."

* **[!UICONTROL Error management]**: in dit veld kunt u de acties definiëren die moeten worden uitgevoerd als een geordende campagnemaak fouten bevat. Er zijn drie mogelijke opties:

   * **[!UICONTROL Suspend the process]**: De georkestreerde campagne wordt automatisch gepauzeerd en de status verandert in **[!UICONTROL Failed]** . Zodra het probleem is opgelost, hervat u de georkestreerde campagne met de knoppen van **[!UICONTROL Resume]** .
   * **[!UICONTROL Ignore]**: De status van de taak die de fout heeft veroorzaakt, verandert in **[!UICONTROL Failed]** , maar de geordende campagne behoudt de status **[!UICONTROL Started]** . <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Abort the process]**: De georkestreerde campagne wordt automatisch gestopt en de status verandert in **[!UICONTROL Failed]** . Zodra het probleem is opgelost, start u de georkestreerde campagne opnieuw met de knoppen van **[!UICONTROL Start]** .

* **[!UICONTROL Consecutive errors]**: Dit veld wordt beschikbaar wanneer de **[!UICONTROL Ignore]** -waarde wordt geselecteerd in het **[!UICONTROL In case of errors]** -veld. U kunt opgeven hoeveel fouten kunnen worden genegeerd voordat het proces wordt gestopt. Zodra dit aantal wordt bereikt, verandert de georkestreerde campagnestatus in **[!UICONTROL Failed]**. Als de waarde van dit veld 0 is, wordt de geordende campagne nooit gestopt, ongeacht het aantal fouten.


