---
solution: Journey Optimizer
product: journey optimizer
title: Bladeren en uw reizen filteren
description: Bladeren en filteren in Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: reis, eerste, begin, snel-begin, publiek, gebeurtenis, actie
exl-id: 770bdbf2-560d-4127-bdb9-1f82495a566f
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '1142'
ht-degree: 2%

---

# Bladeren en uw reizen filteren {#browse-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_view"
>title="Reislijst en kalenderweergaven"
>abstract="Naast de lijst met ritten geeft [!DNL Journey Optimizer] een kalenderweergave van uw reizen, met een duidelijke visuele weergave van hun dienstregelingen. Met deze knoppen kunt u op elk gewenst moment schakelen tussen de lijst- en de kalenderweergave."

## Reisdashboard {#dashboard-jo}

Klik in de menusectie JOURNEY MANAGEMENT op **[!UICONTROL Journeys]** . Er zijn twee tabbladen beschikbaar: **[!UICONTROL Overview]** en **[!UICONTROL Browse]** .

### Overzicht van reizen

Op het tabblad **[!UICONTROL Overview]** wordt een dashboard weergegeven met de belangrijkste maatstaven voor uw reizen.

![ dashboard van de Reis die het Overzicht tabel ](assets/journeys-dashboard.png) benadrukt

* **verwerkte Profielen**: totaal aantal profielen die in de laatste 24 uren worden verwerkt
* **Levende reizen**: totaal aantal levende reizen met verkeer over de laatste 24 uren. De actieve reizen omvatten **Eenheids reizen** (gebeurtenis-gebaseerd) en **ritten van de Partij** (gelezen publiek).
* **tarief van de Fout**: verhouding van alle profielen in fout vergeleken met het totale aantal profielen die over de laatste 24 uren inging.
* **verwerpt tarief**: verhouding van alle verworpen profielen vergeleken met het totale aantal profielen die de afgelopen 24 uren inging. Een weggegooid profiel vertegenwoordigt iemand die niet in aanmerking komt om de reis, bijvoorbeeld, wegens onjuiste namespace of toegangsregels binnen te gaan.

>[!NOTE]
>
>Dit dashboard houdt rekening met de reizen met verkeer in de afgelopen 24 uur. Alleen de reizen waartoe u toegang hebt, worden weergegeven. De metriek worden verfrist om de 30 minuten en slechts wanneer de nieuwe gegevens beschikbaar zijn.

### Reizigerslijst

Op het tabblad **[!UICONTROL Browse]** wordt de lijst met bestaande reizen weergegeven. U kunt reizen zoeken, filters gebruiken en basishandelingen op elk element uitvoeren. U kunt bijvoorbeeld een item dupliceren of verwijderen.

![ reis dashboard die het Browse lusje benadrukt ](assets/journeys-browse.png)

### Reizigerskalender {#calendar}

Naast de lijst met ritten geeft [!DNL Journey Optimizer] een kalenderweergave van uw reizen, met een duidelijke visuele weergave van hun dienstregelingen.

>[!AVAILABILITY]
>
>De kalenderweergave is momenteel alleen beschikbaar voor een set organisaties (beperkte beschikbaarheid). Om toegang te verzoeken, gebruik [ deze vorm ](https://forms.cloud.microsoft/r/FC49afuJVi){target="_blank"}.
>
>Deze functie is actief ontwikkeld. We verwelkomen uw invoer en verzoeken met de knop **[!UICONTROL Beta Feedback]** in het bovenste menu.

Om tot de kalendermening toegang te hebben, open de reislijst en klik het ![ pictogram van de Kalender ](assets/do-not-localize/timeline-icon.svg) pictogram.

In de kalender worden alle reizen weergegeven die voor de huidige week zijn gepland. Gebruik de pijlknoppen boven de kalender om tussen weken te navigeren.

![ kalendermening die levende reizen tonen ](assets/timeline-journeys.png)

Hoe reizen worden vertegenwoordigd:

* Standaard worden in het rooster alle actieve en geplande reizen voor de geselecteerde week weergegeven. Extra filteropties kunnen voltooide, gestopt en voltooide activeringen of activeringen tonen.
* Conceptreizen en ritten in testmodus worden niet weergegeven.
* Reizen die meerdere dagen beslaan, worden boven in het kalenderraster weergegeven.
* Als er geen begintijd is opgegeven, wordt de dichtstbijzijnde handmatige activeringstijd gebruikt om deze in de kalender te plaatsen.
* De reizen worden getoond als timespans van 1 uur, maar dit weerspiegelt geen daadwerkelijke verzend of voltooiingstijd.

Voor meer details op een reis, klik zijn visueel blok om zijn details te openen en te onderzoeken.

In de reislijst, worden alle reisversies getoond met het versieaantal. Wanneer u een reis zoekt, verschijnen de nieuwste versies bij de eerste keer dat de toepassing wordt geopend boven aan de lijst. Vervolgens kunt u de gewenste sortering definiëren en wordt deze door de toepassing als gebruikervoorkeur behouden. De versie van de reis wordt ook weergegeven boven aan de interface van de reiseditie, boven het canvas. Leer meer over [ beheer van de reisversie ](publishing-the-journey.md#journey-versions-journey-versions).



## Uw reizen filteren {#journey-filter}

Gebruik in de lijst met reizen verschillende filters om de lijst met reizen te verfijnen.

![ het Scherm dat een steekproef van reis toont filtrerend met twee geselecteerde types van reizen ](assets/filter-journeys.png)

U kunt reizen volgens hun [ status ](#journey-statuses) filtreren, [ type ](#journey-types), [ versie ](publishing-the-journey.md#journey-versions-journey-versions), en toegewezen [ markeringen ](../start/search-filter-categorize.md#tags) van **[!UICONTROL Status and version filters]**.

Gebruik **[!UICONTROL Creation filters]** om ritten te filteren op basis van de aanmaakdatum of de gebruiker die ze heeft gemaakt.

Geef ritten weer die een specifieke gebeurtenis, veldgroep of handeling van de **[!UICONTROL Activity filters]** en **[!UICONTROL Data filters]** gebruiken.

Gebruik **[!UICONTROL Publication filters]** om een publicatiedatum of een gebruiker te selecteren. U kunt bijvoorbeeld kiezen of u de nieuwste versies wilt weergeven van live reizen die gisteren zijn gepubliceerd.

Selecteer **[!UICONTROL Custom]** in de vervolgkeuzelijst **[!UICONTROL Published]** als u reizen wilt filteren op basis van een specifiek datumbereik.

Daarnaast wordt in het configuratievenster Gebeurtenis, Gegevensbron en Handeling in het veld **[!UICONTROL Used in]** het aantal ritten weergegeven dat die specifieke gebeurtenis, veldgroep of handeling gebruikt. U kunt klikken op de knop **[!UICONTROL View journeys]** om de lijst met corresponderende journey’s weer te geven.

![](assets/journey3bis.png)

## Soorten reizen {#journey-types}

Het soort reis hangt af van de activiteiten die in die reis worden gebruikt. Het kan zijn:

* **[!UICONTROL Unitary event]** - Eenheidsuitzettingen worden gekoppeld aan een specifiek profiel. Gebeurtenissen hebben betrekking op het gedrag van een persoon of iets dat met een persoon verband houdt (een persoon bereikte bijvoorbeeld 10.000 loyaliteitspunten). [Meer informatie](../event/about-events.md).
* **[!UICONTROL Business event]**. De reis van bedrijfsgebeurtenissen begint met een niet-profielgerelateerde gebeurtenis. De gebeurtenisconfiguratie wordt uitgevoerd door een technische gebruiker en kan niet worden uitgegeven. [Meer informatie](../event/about-events.md).
* **[!UICONTROL Audience Qualification]** - De reizen van de Kwalificatie van het publiek luisteren naar de ingangen en de uitgangen van profielen in het publiek van Adobe Experience Platform om individuen te maken ingaan of zich op een reis voortbewegen. [Meer informatie](audience-qualification-events.md).
* **[!UICONTROL Read audience]** - Bij Lezen kijkreizen nemen alle personen in het publiek de reis in en ontvangen ze de berichten die in uw reis zijn opgenomen.  [Meer informatie](read-audience.md).


Leer meer over reistypes en bijbehorend ingangsbeheer op [ deze pagina ](entry-management.md).

## Reisstatussen {#journey-statuses}

De reisstatus hangt af van de levenscyclus. Het kan zijn:

* **Gesloten**: de reis is gesloten gebruikend **dicht aan nieuwe ingangen** knoop. De reis houdt in dat nieuwe individuen de reis kunnen betreden. Personen die al onderweg zijn, kunnen de reis normaal afmaken.
* **Ontwerp**: de reis is in zijn eerste stadium. Het is nog niet gepubliceerd.
* **Ontwerp (Test)**: de testwijze is geactiveerd gebruikend de **wijze van de Test** knoop.
* **Voltooid**: De reis schakelt automatisch aan deze status na de globale onderbreking 91 dag [&#128279;](journey-properties.md#global_timeout). Profielen die al op reis zijn, worden normaal afgehandeld. Nieuwe profielen kunnen niet langer de reis betreden.
* **Levend**: de reis is gepubliceerd gebruikend **publiceer** knoop.
* **Gestopt**: de reis is uitgezet gebruikend de **3&rbrace; knoop van het Einde &lbrace;.** Alle individuen sluiten onmiddellijk de reis.

>[!NOTE]
>
>* De publicatielevenscyclus van de Reis omvat ook een reeks tussenliggende statussen die niet beschikbaar zijn voor filtering: &quot;Publishing&quot; (tussen &quot;Draft&quot; en &quot;Live&quot;), &quot;Activating test mode&quot; of &quot;Deactivating test mode&quot; (tussen &quot;Draft&quot; en &quot;Draft (test)&quot;) en &quot;Stopping&quot; (tussen &quot;Live&quot; en &quot;Gestopt&quot;). Wanneer een reis in een tussenstadium is, is het read-only.
>
>* Als u aan a **levende** reis moet wijzigen, [ creeer een nieuwe versie ](#journey-versions) van uw reis.


## Een reis dupliceren {#duplicate-a-journey}

U kunt een bestaande reis van **dupliceren doorbladert** tabel. Alle objecten en instellingen worden gedupliceerd naar de reiskopie.

Volg onderstaande stappen om dit te doen:

1. Navigeer aan de reis u wilt kopiëren, **klikken Meer acties** pictogram (de drie punten naast de reisnaam).
1. Selecteer **Dupliceren**.

   ![ Dupliceer een reis ](assets/duplicate-jo.png)

1. Voer de naam van de reis in en bevestig deze. U kunt de naam ook wijzigen in het scherm met de reiseigenschappen. Standaard wordt de naam als volgt ingesteld: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. De nieuwe reis wordt gecreeerd en beschikbaar in de reislijst.
