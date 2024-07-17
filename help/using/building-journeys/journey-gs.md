---
solution: Journey Optimizer
product: journey optimizer
title: Uw eerste journey maken
description: Belangrijke stappen om uw eerste journey met Adobe Journey Optimizer te maken
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: reis, eerste, begin, snel-begin, publiek, gebeurtenis, actie
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: a7234350c0ca66d033bbbd77c1b14063147468cf
workflow-type: tm+mt
source-wordcount: '1215'
ht-degree: 7%

---

# Uw eerste journey maken{#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Reizen maken"
>abstract="Het gebruik **Adobe Journey Optimizer** om in real time het gebruikscase van het orkestgebruik te bouwen gebruikend contextafhankelijke gegevens die in gebeurtenissen of gegevensbronnen worden opgeslagen."


## Vereisten{#start-prerequisites}

Voor het verzenden van berichten met ritten zijn de volgende configuraties vereist:

1. **vorm een gebeurtenis**: als u uw reizen wilt teweegbrengen tijdelijk wanneer een gebeurtenis wordt ontvangen, moet u een gebeurtenis vormen. U bepaalt de verwachte informatie en hoe te om het te verwerken. Deze stap wordt uitgevoerd door a **technische gebruiker**. [Meer informatie](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **creeer een publiek**: uw reis kan aan het publiek van Adobe Experience Platform ook luisteren om berichten in partij naar een gespecificeerde reeks profielen te verzenden. Hiervoor moet u een publiek maken. [Meer informatie](../audience/about-audiences.md).

   ![](assets/segment2.png)

1. **vorm de gegevensbron**: u kunt een verbinding aan een systeem bepalen om extra informatie terug te winnen die in uw reizen, bijvoorbeeld in uw voorwaarden zal worden gebruikt. Tijdens de provisioning wordt ook een ingebouwde Adobe Experience Platform-databron geconfigureerd. Deze stap is niet vereist als u alleen data gebruikt van de gebeurtenissen in uw journey. Deze stap wordt uitgevoerd door a **technische gebruiker**. [Meer informatie](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **vorm een actie**: Als u een derdesysteem gebruikt om uw berichten te verzenden, kunt u een douaneactie tot stand brengen. Leer meer in deze [ sectie ](../action/action.md). Deze stap wordt uitgevoerd door a **technische gebruiker**. Als u de ingebouwde berichtmogelijkheden van Journey Optimizer gebruikt, hoeft u alleen maar een kanaalactie aan uw reis toe te voegen en uw inhoud te ontwerpen.

   ![](assets/custom2.png)

## Toegang tot reizen {#journey-access}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Journeys"
>abstract="Ontwerpen van klantritten om persoonlijke, contextuele ervaringen te bieden. Met Journey Optimizer kunt u in real-time gebruikmaken van het orkestgebruik en contextuele gegevens opslaan in gebeurtenissen of gegevensbronnen. Het **Overzicht** lusje toont een dashboard met zeer belangrijke metriek met betrekking tot uw reizen. Het **doorbladert** lusje toont de lijst van bestaande reizen."

### Belangrijkste metriek en reislijst {#access-metrics}

Klik in de menusectie JOURNEY MANAGEMENT op **[!UICONTROL Journeys]** . Er zijn twee tabbladen beschikbaar:

**Overzicht**: dit lusje toont een dashboard met zeer belangrijke metriek met betrekking tot uw reizen:

* **verwerkte Profielen**: totaal aantal profielen die in de laatste 24 uren worden verwerkt
* **Levende reizen**: totaal aantal levende reizen met verkeer over de laatste 24 uren. De actieve reizen omvatten **Eenheids reizen** (gebeurtenis-gebaseerd) en **ritten van de Partij** (gelezen publiek).
* **tarief van de Fout**: verhouding van alle profielen in fout vergeleken met het totale aantal profielen die over de laatste 24 uren inging.
* **verwerpt tarief**: verhouding van alle verworpen profielen vergeleken met het totale aantal profielen die de afgelopen 24 uren inging. Een weggegooid profiel vertegenwoordigt iemand die niet in aanmerking komt om de reis binnen te gaan, bijvoorbeeld vanwege een onjuiste naamruimte of vanwege regels voor opnieuw betreden.

>[!NOTE]
>
>Dit dashboard houdt rekening met de reizen met verkeer in de afgelopen 24 uur. Alleen de reizen waartoe u toegang hebt, worden weergegeven. De metriek worden verfrist om de 30 minuten en slechts wanneer de nieuwe gegevens beschikbaar zijn.

![](assets/journeys-dashboard.png)

**doorbladert**: dit lusje toont de lijst van bestaande reizen. U kunt reizen zoeken, filters gebruiken en basishandelingen op elk element uitvoeren. U kunt bijvoorbeeld een item dupliceren of verwijderen. Raadpleeg [deze sectie](../start/user-interface.md#filter-lists) voor meer informatie.

![](assets/journeys-browse.png)

### Reizen filteren {#filter}

In de lijst met reizen kunt u verschillende filters gebruiken om de lijst met reizen te verfijnen, zodat u deze beter leesbaar kunt maken.

![](assets/filter-journeys.png)

Hier zijn de diverse het filtreren verrichtingen die u kunt uitvoeren:

De ritten van de filter op hun status, type, versie en toegewezen markeringen van **[!UICONTROL Status and version filters]**.

Het type kan zijn: **[!UICONTROL Unitary event]**, **[!UICONTROL Audience qualification]**, **[!UICONTROL Read audience]** of **[!UICONTROL Business event]** .

De status kan zijn:

* **Gesloten**: de reis is gesloten gebruikend **dicht aan nieuwe ingangen** knoop. De reis houdt in dat nieuwe individuen de reis kunnen betreden. Personen die al onderweg zijn, kunnen de reis normaal afmaken.
* **Ontwerp**: de reis is in zijn eerste stadium. Het is nog niet gepubliceerd.
* **Ontwerp (Test)**: de testwijze is geactiveerd gebruikend de **wijze van de Test** knoop.
* **Voltooid**: De reis schakelt automatisch aan deze status na de globale onderbreking 91 dag [ ](journey-properties.md#global_timeout). Profielen die al op reis zijn, worden normaal afgehandeld. Nieuwe profielen kunnen niet langer de reis betreden.
* **Levend**: de reis is gepubliceerd gebruikend de **Publish** knoop.
* **Gestopt**: de reis is uitgezet gebruikend de **3} knoop van het Einde {.** Alle individuen sluiten onmiddellijk de reis.

>[!NOTE]
>
>De publicatielevenscyclus van de Reis omvat ook een reeks tussenliggende statussen die niet beschikbaar zijn voor filtering: &quot;Publishing&quot; (tussen &quot;Draft&quot; en &quot;Live&quot;), &quot;Activating test mode&quot; of &quot;Deactivating test mode&quot; (tussen &quot;Draft&quot; en &quot;Draft (test)&quot;) en &quot;Stopping&quot; (tussen &quot;Live&quot; en &quot;Gestopt&quot;). Wanneer een reis in een tussenstadium is, is het read-only.

Gebruik **[!UICONTROL Creation filters]** om ritten te filteren op basis van de aanmaakdatum of de gebruiker die ze heeft gemaakt.

Geef ritten weer die een specifieke gebeurtenis, veldgroep of handeling van de **[!UICONTROL Activity filters]** en **[!UICONTROL Data filters]** gebruiken.

Gebruik **[!UICONTROL Publication filters]** om een publicatiedatum of een gebruiker te selecteren. U kunt bijvoorbeeld kiezen of u de nieuwste versies wilt weergeven van live reizen die gisteren zijn gepubliceerd.

Selecteer **[!UICONTROL Custom]** in de vervolgkeuzelijst **[!UICONTROL Published]** als u reizen wilt filteren op basis van een specifiek datumbereik.

Daarnaast wordt in het configuratievenster Gebeurtenis, Gegevensbron en Handeling in het veld **[!UICONTROL Used in]** het aantal ritten weergegeven dat die specifieke gebeurtenis, veldgroep of handeling gebruikt. U kunt klikken op de knop **[!UICONTROL View journeys]** om de lijst met corresponderende journey’s weer te geven.

![](assets/journey3bis.png)

## Uw reis maken {#jo-build}

Ontwerpreizen om persoonlijke contextafhankelijke ervaringen te bieden. Met [!DNL Journey Optimizer] kunt u in real-time gebruikmaken van het orkestgebruik en contextuele gegevens opslaan in gebeurtenissen of gegevensbronnen. Ontwerp multistep geavanceerde scenario&#39;s aangedreven door de volgende mogelijkheden:

* Verzend in real time **unitaire levering** teweeggebracht wanneer een gebeurtenis wordt ontvangen, of **in partij** gebruikend het publiek van Adobe Experience Platform.

* Gebruik **contextafhankelijke gegevens** van gebeurtenissen, informatie van Adobe Experience Platform, of gegevens van de diensten van derdeAPI.

* Gebruik **ingebouwde kanaalacties** (E-mail, SMS, Duw, InApp) om berichten te verzenden die in [!DNL Journey Optimizer] worden ontworpen of **douaneacties** tot stand te brengen als u een derdesysteem gebruikt om uw berichten te verzenden.

* Met de **reisontwerper**, bouwt uw multi-step gebruiksgevallen: sleep en laat gemakkelijk een ingangsgebeurtenis of een gelezen publieksactiviteit vallen, voeg voorwaarden toe en verzend gepersonaliseerde berichten.

➡️ [ ontdekt deze eigenschap in video ](journey.md#video)

De stappen om berichten door reizen te verzenden zijn hieronder vermeld:

1. Van **doorbladert** lusje, klik **[!UICONTROL Create Journey]** om een nieuwe reis tot stand te brengen.

1. Bewerk de eigenschappen van de journey in het configuratievenster dat aan de rechterkant wordt weergegeven. Leer hoe te om de eigenschappen van uw reis in dit [ te plaatsen deze pagina ](journey-properties.md).

   ![](assets/jo-properties.png)

1. Begin door een gebeurtenis te slepen en te laten vallen of a **las de activiteit van het publiek** van het palet in het canvas. Meer over reisontwerp leren, verwijs naar [ deze sectie ](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Sleep de volgende stappen die het individu zal volgen en zet ze neer. U kunt bijvoorbeeld een voorwaarde toevoegen, gevolgd door een kanaalactie. Meer over activiteiten leren, verwijs naar [ deze sectie ](using-the-journey-designer.md).

1. Test uw reis met testprofielen. Leer meer in deze [ sectie ](testing-the-journey.md)

1. Publish je reis om het te activeren. Leer meer in deze [ sectie ](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Bewaak uw reis gebruikend de specifieke rapporteringshulpmiddelen om de doeltreffendheid van uw reis te meten. Leer meer in deze [ sectie ](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)


## Een reis dupliceren {#duplicate-a-journey}

U kunt een bestaande reis van **dupliceren doorbladert** tabel. Alle objecten en instellingen worden gedupliceerd naar de reiskopie.

Volg onderstaande stappen om dit te doen:

1. Navigeer aan de reis u wilt kopiëren, **klikken Meer acties** pictogram (de drie punten naast de reisnaam).
1. Selecteer **Dupliceren**.

   ![ Dupliceer een reis ](assets/duplicate-jo.png)

1. Voer de naam van de reis in en bevestig deze. U kunt de naam ook wijzigen in het scherm met de reiseigenschappen. Standaard wordt de naam als volgt ingesteld: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. De nieuwe reis wordt gecreeerd en beschikbaar in de reislijst.
