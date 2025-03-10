---
solution: Journey Optimizer
product: journey optimizer
title: Instellingen voor meerdere stappen configureren
description: Leer hoe u instellingen voor meerdere stappen voor campagnes configureert met Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 0%

---


# Instellingen voor meerdere stappen configureren {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="Eigenschappen van meerdere stappen"
>abstract="Kies in dit scherm de sjabloon die u wilt gebruiken om de campagne met meerdere stappen te maken en geef een label op. Vouw de **Extra opties** sectie uit om meer montages zoals de multi-step interne naam van de campagne, zijn omslag, timezone, en supervisorgroep te vormen. Het wordt hoogst geadviseerd om een supervisorgroep te selecteren zodat de exploitanten worden gealarmeerd als een fout voorkomt."

Als u een campagne met meerdere stappen maakt of meerdere campagneactiviteiten op het canvas ordent, hebt u toegang tot geavanceerde instellingen voor de campagne met meerdere stappen. U kunt bijvoorbeeld een specifieke tijdzone instellen voor de campagne met meerdere stappen, beheren hoe de campagne met meerdere stappen zich moet gedragen in het geval van een fout, of de vertraging beheren waarna de campagnegeschiedenis met meerdere stappen moet worden leeggemaakt.

Deze instellingen worden vooraf geconfigureerd in de geselecteerde sjabloon wanneer u de campagne voor meerdere stappen maakt, maar kunnen worden bewerkt zoals nodig voor deze specifieke campagne met meerdere stappen.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## Eigenschappen van meerdere stappen {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Eigenschappen van meerdere stappen"
>abstract="Deze sectie verstrekt generische multi-step campagneeigenschappen die ook toegankelijk zijn wanneer het creëren van de multi-step campagne. U kunt de sjabloon kiezen die u wilt gebruiken om de campagne met meerdere stappen te maken en u kunt een label opgeven. Vouw de sectie Aanvullende opties uit om specifieke instellingen te configureren, zoals de campagne voor het opslaan van mappen of tijdzones in meerdere stappen."

De sectie **[!UICONTROL Properties]** biedt algemene instellingen die kunnen worden geconfigureerd wanneer u een campagne met meerdere stappen maakt. Als u de eigenschappen van een bestaande campagne met meerdere stappen wilt openen, klikt u op de knop **[!UICONTROL Settings]** in de actiebalk boven het campagneccanvas met meerdere stappen.


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


Deze eigenschappen zijn:

* The **[!UICONTROL Label]** of the multi-step campagne that displays in the list.
* De **[!UICONTROL Internal name]** van de multi-step campagne.
* De locatie **[!UICONTROL Folder]** waar de campagne met meerdere stappen moet worden opgeslagen.
* De standaardinstelling **[!UICONTROL Timezone]** die moet worden gebruikt in alle activiteiten van de meerstapse campagne. Standaard is de tijdzone van de campagne in meerdere stappen de tijdzone die is gedefinieerd voor de huidige campagneoperator.
Mogelijke waarden zijn:
   * **de tijdzone van de Server** om de tijdzone van uw organisatie van Adobe Experience Platform te gebruiken
   * **tijdzone van de Exploitant** om de tijdzone van de exploitant te gebruiken die de multi-step campagne uitvoert
   * **streek van de Tijd van het gegevensbestand** om de tijdzone van de gegevensbestandserver te gebruiken
   * Een specifieke tijdzone
* Wanneer een campagne in meerdere stappen mislukt, worden de operatoren die tot de groep met operatoren behoren die in het veld **[!UICONTROL Supervisor(s)]** is geselecteerd, via e-mail op de hoogte gesteld.
* U kunt ook een **[!UICONTROL Description]** van uw multi-step campagne invoeren.

## Segmenteringsinstellingen  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Segmenteringsinstellingen"
>abstract="In deze sectie kunt u de doeldimensie selecteren voor doelprofielen in de campagne met meerdere stappen en ervoor kiezen om de werkloverresultaten tussen twee uitvoeringen te behouden. Deze optie mag alleen voor testdoeleinden worden gebruikt en mag nooit worden ingeschakeld in een meerfasencampagne voor productie."

* **[!UICONTROL Targeting dimension]**: selecteer de doeldimensie die u wilt gebruiken voor doelprofielen: ontvangers, begunstigden van contracten, operator, abonnees, enz.

* **[!UICONTROL Keep the result of interim populations between two executions]**: Standaard blijven alleen de werktabellen van de laatste uitvoering van de campagne met meerdere stappen behouden. Werktafels van eerdere uitvoeringen worden opgeschoond door een technische meerfasencampagne, die dagelijks wordt uitgevoerd.

  Als deze optie is ingeschakeld, worden de werktabellen ook bewaard nadat de campagne met meerdere stappen is uitgevoerd. U kunt het voor testende doeleinden gebruiken en daarom moet **slechts** op ontwikkeling of het opvoeren milieu&#39;s worden gebruikt. Het mag nooit worden gecontroleerd in een meerfasencampagne voor de productie.

## Instellingen voor uitvoering  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Instellingen voor uitvoering"
>abstract="In deze sectie kunt u instellingen configureren die betrekking hebben op de uitvoering van de workflow, zoals het aantal dagen dat de campagnegeschiedenis in meerdere stappen wordt bijgehouden."

* **[!UICONTROL History in days]** - Geeft het aantal dagen aan waarna de historie moet worden gewist. De geschiedenis bevat elementen die gerelateerd zijn aan de campagne in meerdere stappen: logboeken, taken, gebeurtenissen (technische objecten die gekoppeld zijn aan de campagnebewerking in meerdere stappen). De standaardwaarde is 30 dagen voor uit-van-de-doos multi-step campagnemalplaatjes. Het leegmaken van de geschiedenis wordt uitgevoerd door de technische multi-step campagne van de Schoonmaakbeurt van het Gegevensbestand, die door gebrek dagelijks wordt uitgevoerd

  >[!IMPORTANT]
  >
  >Als het veld **[!UICONTROL History in days]** leeg blijft, wordt de waarde ervan beschouwd als &quot;1&quot;, wat betekent dat de historie na 1 dag wordt gewist.

* **[!UICONTROL Default affinity]**: Als uw installatie meerdere etappes campagnemeservers bevat, gebruikt u dit veld om de server op te geven waarop de campagne met meerdere stappen wordt uitgevoerd. Dit dwingt de uitvoering van die multi-step campagne op een bepaalde server. U kunt elke bestaande affiniteitsnaam kiezen, maar gebruik geen spaties of leestekens. Als u verschillende servers gebruikt, geeft u verschillende namen op, gescheiden door komma&#39;s.

  >[!IMPORTANT]
  >
  >Als de waarde die in dit veld wordt gedefinieerd, op geen enkele server bestaat, blijft de campagne met meerdere stappen in behandeling.


* **[!UICONTROL Save SQL queries in log]**: Schakel deze optie in om de SQL-query&#39;s van de workflmulti-step campagne nu op te slaan in de logboeken. Deze functionaliteit is gereserveerd voor geavanceerde gebruikers. De klasse is van toepassing op multi-step campagnes die gerichte activiteiten zoals **[!UICONTROL Build audience]** bevatten. Wanneer deze optie wordt toegelaten, worden de SQL vragen die naar het gegevensbestand tijdens multi-step campagneuitvoering worden verzonden getoond in de logboeken van de multi-step campagne, die u toestaan om hen te analyseren om vragen te optimaliseren of kwesties te diagnostiseren.

## Instellingen voor foutbeheer  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Instellingen voor foutbeheer"
>abstract="In deze sectie kunt u definiëren hoe fouten tijdens de uitvoering van de campagne in meerdere stappen moeten worden beheerd. U kunt ervoor kiezen het proces te pauzeren, een bepaald aantal fouten te negeren of de uitvoering van de campagne in meerdere stappen te stoppen."

* **[!UICONTROL Error management]**: in dit veld kunt u de acties definiëren die moeten worden uitgevoerd als een campagnemaak met meerdere stappen fouten bevat. Er zijn drie mogelijke opties:

   * **[!UICONTROL Suspend the process]**: De campagne met meerdere stappen wordt automatisch gepauzeerd en de status verandert in **[!UICONTROL Failed]** . Zodra het probleem is opgelost, hervat u de meerstapscampagne met de knoppen van **[!UICONTROL Resume]** .
   * **[!UICONTROL Ignore]**: De status van de taak die de fout heeft veroorzaakt, verandert in **[!UICONTROL Failed]** , maar de campagne met meerdere stappen behoudt de status **[!UICONTROL Started]** . <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Abort the process]**: De campagne met meerdere stappen wordt automatisch gestopt en de status verandert in **[!UICONTROL Failed]** . Zodra het probleem is opgelost, start u de campagne met meerdere stappen opnieuw met de knoppen van **[!UICONTROL Start]** .

* **[!UICONTROL Consecutive errors]**: Dit veld wordt beschikbaar wanneer de **[!UICONTROL Ignore]** -waarde wordt geselecteerd in het **[!UICONTROL In case of errors]** -veld. U kunt opgeven hoeveel fouten kunnen worden genegeerd voordat het proces wordt gestopt. Zodra dit aantal wordt bereikt, verandert de multi-step campagnestatus in **[!UICONTROL Failed]**. Als de waarde van dit veld 0 is, wordt de campagne met meerdere stappen nooit gestopt, ongeacht het aantal fouten.

## Initialisatiescript {#initialization-script}

Het **manuscript van de Initialisatie** laat u variabelen initialiseren of activiteiteneigenschappen wijzigen. Klik **geef code** knoop uit en typ het fragment van uit te voeren code. Het script wordt aangeroepen wanneer de campagne met meerdere stappen wordt uitgevoerd. Verwijs naar de sectie met betrekking tot [ gebeurtenisvariabelen ](event-variables.md).

