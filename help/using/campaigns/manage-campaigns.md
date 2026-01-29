---
solution: Journey Optimizer
product: journey optimizer
title: Campagnes openen en beheren
description: Leer hoe u uw campagnes in Journey Optimizer kunt openen en beheren.
feature: Campaigns
topic: Content Management
role: User
mini-toc-levels: 1
level: Beginner
keywords: campagnes, status, planning, toegang, optimaliseren beheren
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 478bd6df8a82c9e37ec9319dedb27d99c021ee99
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Campagnes openen en beheren {#manage-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Geordende inventarisatie van campagnes"
>abstract="In dit scherm, kunt u tot de volledige lijst van Geordende campagnes toegang hebben, hun huidige status, laatste/volgende uitvoeringsdata controleren, en een nieuwe Geordende campagne creëren."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Actie"
>abstract="In deze secties worden alle acties weergegeven die in de geordende campagne worden gebruikt."

Leer hoe u uw campagnes in Adobe Journey Optimizer kunt openen, organiseren en beheren. Deze handleiding omvat alles, van het zoeken naar campagnes tot het begrijpen van statussen, het uitvoeren van algemene bewerkingen en het onderhouden van uw campagnewerkruimte.

>[!BEGINSHADEBOX]

**sprong direct aan wat u nodig hebt:**

* **creeer een nieuwe campagne** - [ kies uw campagnetype ](get-started-with-campaigns.md#campaign-types) | [ creeer de campagne van de Actie ](create-campaign.md) | [ creeer API-teweeggebrachte campagne ](api-triggered-campaigns.md) | [ creeer Geordende campagne ](../orchestrated/gs-orchestrated-campaigns.md)
* **vind bestaande campagnes** - [ Onderzoek en filter ](#access)
* **campagneprestaties van de Mening** - [ de rapporten van de Campagne ](../reports/campaign-global-report-cja.md)
* **campagnes van het Programma** - [ Gebruik de kalender ](#calendar)
* **beheer conflicten** - [ de beheershandleiding van het Conflict ](../conflict-prioritization/gs-conflict-prioritization.md)

>[!ENDSHADEBOX]

## Campagnes openen en doorbladeren {#access}

Campagnes zijn toegankelijk via het menu **[!UICONTROL Campaigns]** . Gebruik de lusjes om campagnes door type te doorbladeren: **actie** campagnes, **API-teweeggebrachte** campagnes, en **Geordende** campagnes. Leer meer over de [ types van campagnes ](get-started-with-campaigns.md#campaign-types). Welke typen beschikbaar zijn, is afhankelijk van uw licentieovereenkomst en uw machtigingen.

>[!BEGINTABS]

>[!TAB  campagnes van de Actie ]

Selecteer het tabblad **[!UICONTROL Action]** voor toegang tot de lijst met actiecampagnes.

Standaard worden in de lijst alle campagnes met de statussen **[!UICONTROL Draft]** , **[!UICONTROL Scheduled]** en **[!UICONTROL Live]** weergegeven. Om gestopt, voltooide, en gearchiveerde campagnes te tonen, moet u de filter ontruimen.

![](assets/create-campaign-list.png)

>[!TAB  API teweeggebrachte campagnes ]

Selecteer het tabblad **[!UICONTROL API triggered]** voor toegang tot de lijst met API-geactiveerde campagnes.

Standaard worden in de lijst alle campagnes met de statussen **[!UICONTROL Draft]** , **[!UICONTROL Scheduled]** en **[!UICONTROL Live]** weergegeven. Om gestopt, voltooide, en gearchiveerde campagnes te tonen, moet u de filter ontruimen.

![](assets/api-triggered-list.png)

>[!TAB  Geordende campagnes ]

Selecteer het tabblad **[!UICONTROL Orchestration]** voor toegang tot de lijst met geordende campagnes.

![ beeld dat de Geordende campagneinventaris ](assets/inventory.png){zoomable="yes"} toont

Elk Geordende campagne in de lijst toont informatie zoals de huidige [ status van de campagne ](#statuses), het bijbehorende kanaal en de markeringen, of de laatste tijd het werd gewijzigd. U kunt de getoonde kolommen aanpassen door ![ te klikken vormt lay-outknoop ](assets/do-not-localize/inventory-configure-layout.svg).

>[!ENDTABS]

### Zoeken en filteren {#search-filter}

Bovendien zijn er een zoekbalk en filters beschikbaar waarmee u gemakkelijk in de lijst kunt zoeken. U kunt bijvoorbeeld campagnes filteren om alleen de campagnes weer te geven die aan een bepaald kanaal of een bepaalde tag zijn gekoppeld, of de campagnes die tijdens een bepaald datumbereik zijn gemaakt.

## Campagne {#operations}

Het ![ beeld dat de Meer knopen van acties ](assets/do-not-localize/rule-builder-icon-more.svg) in de campagneinventaris toont staat u toe om diverse verrichtingen uit te voeren.

![ beeld dat de campagneinventaris ](assets/inventory-actions.png) toont

### Beschikbare acties

**voor alle campagneretypen:**

* **[!UICONTROL View all time report]** / **[!UICONTROL View last 24 hours report]** - Gebruik rapporten om de impact en prestaties van uw campagnes te meten en te visualiseren. [ leer meer over campagnerapporten → ](../reports/campaign-global-report-cja.md)
* **[!UICONTROL Edit tags]** - Bewerk de tags die aan de campagne zijn gekoppeld. [ leren hoe te om markeringen te gebruiken → ](../start/search-filter-categorize.md#add-tags)
* **[!UICONTROL Duplicate]** - Gebruik deze optie om een campagne te dupliceren, bijvoorbeeld om een geordende campagne uit te voeren die is gestopt. [ leer meer over het dupliceren → ](#duplicate-a-campaign)
* **[!UICONTROL Delete]** - Gebruik deze optie om een campagne te verwijderen. [ Leer meer over het schrappen → ](#delete-a-campaign)
* **[!UICONTROL Archive]** - Archiveer de campagne. Alle gearchiveerde campagnes worden 30 dagen na de laatste gewijzigde datum gewist. Deze actie is beschikbaar voor alle campagnes behalve **[!UICONTROL Draft]** campagnes. [ Leer meer over het archiveren → ](#archive-a-campaign)

**voor Actie en API teweeggebrachte slechts campagnes:**

* **[!UICONTROL Add to package]** - Voeg de campagne toe aan een pakket om deze naar een andere sandbox te exporteren. [ leer hoe te om voorwerpen uit te voeren → ](../configuration/copy-objects-to-sandbox.md)
* **[!UICONTROL Open draft version]** - Als een nieuwe versie van de campagne is gemaakt en nog niet is geactiveerd, kunt u de conceptversie van de campagne openen met deze actie.

**slechts voor Geordende campagnes:**

* **[!UICONTROL Back to draft]** - Publiceer een campagne ongedaan en herstel de status van de campagne om fouten te herstellen. Deze actie is beschikbaar wanneer een geplande campagne nog niet is begonnen, of wanneer een live campagne een fout ontdekt alvorens om het even welke uitvoeringen worden voltooid. [ Leer meer over het terugkeren van campagnes → ](../orchestrated/start-monitor-campaigns.md#back-to-draft)

## Inzicht in campagestatus {#statuses}

Elke campagne beweegt zich door een levenscyclus die door zijn status in de interface wordt weerspiegeld. Als u deze statussen begrijpt, weet u beter welke handelingen beschikbaar zijn en wat u daarna moet doen.

| Status | Actiecampagnes | API-gestuurde campagnes | Geordende campagnes | Wat het betekent | Volgende handelingen |
|--------|:----------------:|:-----------------------:|:----------------------:|---------------|--------------|
| **[!UICONTROL Draft]** | ✅ | ✅ | ✅ | Wordt bewerkt, niet geactiveerd | Ga het uitgeven of [ activeer campagne ](review-activate-campaign.md) verder |
| **[!UICONTROL Scheduled]** | ✅ | ✅ | ✅ | Gevormd voor specifieke begindatum | Wacht op lancering, [ wijzigt indien nodig ](#modify), of [ mening in kalender ](#calendar) |
| **[!UICONTROL Live]** | ✅ | ✅ | ✅ | Geactiveerd en actief | [ prestaties van de Monitor ](../reports/campaign-global-report-cja.md), [ creeer nieuwe versie ](#modify) indien nodig. Voor Geordende campagnes: [ keer terug naar ontwerp ](../orchestrated/start-monitor-campaigns.md#back-to-draft) voor geplande campagnes nog niet begonnen of campagnes met uitvoeringsfouten alvorens om het even welke berichten worden verzonden |
| **[!UICONTROL In review]** | ✅ | ✅ | — | Ter goedkeuring ingediend | Wacht op [ goedkeuring ](../test-approve/gs-approval.md) of wijzig |
| **[!UICONTROL Stopped]** | ✅ | ✅ | ✅ | Handmatig gestopt. Kan niet opnieuw activeren | [ Dupliceren aan hergebruik ](#duplicate-a-campaign) |
| **[!UICONTROL Completed]** | ✅ | ✅ | ✅ | Uitvoering voltooid (automatisch toegewezen 3 dagen na activering of op einddatum voor terugkerend) | [ rapporten van de Mening ](../reports/campaign-global-report-cja.md), [ archief ](#archive-a-campaign), of [ dupliceert ](#duplicate-a-campaign) |
| **[!UICONTROL Failed]** | ✅ | ✅ | — | Uitvoering mislukt | De logboeken van de controle, bevestigen kwesties, [ dupliceren om ](#duplicate-a-campaign) opnieuw te proberen |
| **[!UICONTROL Archived]** | ✅ | ✅ | ✅ | Gearchiveerd (automatisch verwijderd na 30 dagen) | [ wint het gebruiken van filter ](#access) terug indien nodig |
| **[!UICONTROL Closed]** | — | — | ✅ | Recurrecampagne gesloten, geen nieuwe ingangen toegestaan (blijft tot alle activiteiten voltooien) | Wacht op voltooiing |
| **[!UICONTROL Publishing]** | — | — | ✅ | Wordt gepubliceerd | Wacht tot publicatie is voltooid |

>[!NOTE]
>
>Voor actie- en API-getriggerde campagnes geeft het pictogram &#39;Concepten openen&#39; naast de status **[!UICONTROL Live]** of **[!UICONTROL Scheduled]** aan dat een nieuwe versie is gemaakt en nog niet is geactiveerd.

### Foutindicatoren

Als er een fout optreedt in een van uw campagnes, verschijnt er een waarschuwingspictogram naast de status van de campagne. Klik erop om informatie over de waarschuwing weer te geven. Deze waarschuwingen kunnen zich in verschillende situaties voordoen, bijvoorbeeld wanneer het campagnebericht niet is gepubliceerd of wanneer de gekozen configuratie onjuist is.

![](assets/campaign-alerts.png)

>[!NOTE]
>
>Assets/Images zijn maximaal 2 jaar (730 dagen) sinds de eerste publicatie ervan in een fragment/inline-bericht toegankelijk in de geleverde inhoud. Na deze vervaldatum (op een willekeurig tijdstip na 730 dagen) moet de publicatie opnieuw worden gepubliceerd om deze twee jaar toegankelijk te houden. Bij elke herpublicatie die binnen 730 dagen na de eerste publicatie wordt uitgevoerd, wordt het vervallen van de middelen/afbeeldingen niet tot de volgende 730 dagen verlengd.

## Campagne-kalender {#calendar}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_view"
>title="Lijst- en kalenderweergaven van campagnes"
>abstract="Naast de lijst met campagnes biedt [!DNL Journey Optimizer] een kalenderweergave van uw campagnes en een duidelijke visuele weergave van hun programma&#39;s. Met deze knoppen kunt u op elk gewenst moment schakelen tussen de lijst- en de kalenderweergave."

Naast de lijst met campagnes biedt [!DNL Journey Optimizer] een kalenderweergave van uw campagnes en een duidelijke visuele weergave van hun programma&#39;s.

### De werking van de kalender

Hoe campagnes worden vertegenwoordigd:

* Standaard worden in het kalenderraster alle live en geplande campagnes voor de geselecteerde week weergegeven. Aanvullende filteropties kunnen voltooide, gestopt en voltooide activeringen of activeringen van een bepaald type of kanaal weergeven.
* Conceptcampagnes worden niet weergegeven.
* Campagnes die meerdere dagen beslaan, worden boven in het kalenderraster weergegeven.
* Als er geen begintijd is opgegeven, wordt de dichtstbijzijnde handmatige activeringstijd gebruikt om deze in de kalender te plaatsen.
* Campagnes worden getoond als timespans van 1 uur, maar dit weerspiegelt geen daadwerkelijke verzend of voltooiingstijd.

### Navigeren door de kalender

1. Klik het ![ kalender ](assets/do-not-localize/Smock_Calendar_18_N.svg) pictogram om tot uw kalender van Campagnes toegang te hebben.

1. Gebruik de pijlknoppen of de datumkiezer boven de kalender om tussen weken te gaan.

   In de kalender worden alle campagnes weergegeven die voor de huidige week zijn gepland.

   ![ kalendermening die levende campagnes tonen ](assets/campaigns-timeline.png)

1. Klik het ![ tandwiel ](assets/do-not-localize/Smock_Gears_18_N.png) pictogram om de vertoning van punten van een knevel te voorzien die veelvoudige dagen of weken overspannen.

   ![ kalendermening die levende campagnes tonen ](assets/campaign-long-term.png)

1. Klik ![ toevoegen kalender ](assets/do-not-localize/Smock_CalendarAdd_18_N.svg) pictogram om tot drie externe kalenders te beheren en toe te voegen.

   ![ kalendermening die externe kalenders tonen ](assets/campaign-external-calendar.png)

1. Sleep de CSV-bestanden met namen van gebeurtenissen, begindatums en einddatums.

   Geüploade gebeurtenissen worden voor alle gebruikers in uw organisatie weergegeven en worden zowel op de kalenders Reis als Campagne weergegeven.

   +++De CSV-indeling moet als volgt zijn:

   | Kolom1 | Kolom2 | Kolom3 |
   |-|-|-|
   | Gebeurtenisnaam | Begindatum in mm/dd/jj-formaat | Einddatum in mm/dd/yformaat |

   +++

1. Indien nodig, kunt u toegevoegde externe kalenders verbergen, verbergen of verwijderen.

   ![ kalendermening die externe kalenders tonen ](assets/campaign-manage-calendar.png)

1. Voor meer informatie over een campagne klikt u op het visuele blok om de details ervan te openen. Er wordt een informatievenster geopend met verschillende informatie over de campagne, zoals het type, de toegang tot de rapporten of de tags die zijn toegewezen.

   ![ campagnemijst met de informatieruit geopend ](assets/campaign-rail.png)

## Herhaalde handelingscampagnes wijzigen en stoppen {#modify}

### Een handelingscampagne wijzigen {#modify-an-action-campaign}

Voer de volgende stappen uit om een nieuwe versie van een terugkerende campagne te wijzigen en te maken:

1. Open de campagne en klik op de knop **[!UICONTROL Modify campaign]** .

1. Er wordt een nieuwe versie van de campagne gemaakt. U kunt de live versie controleren door op **[!UICONTROL Open live version]** te klikken.

   ![](assets/create-campaign-draft.png)

   In de lijst met campagnes worden geactiveerde campagnes met een conceptversie in uitvoering weergegeven met een specifiek pictogram in de kolom **[!UICONTROL Status]** . Klik op dit pictogram om de conceptversie van de campagne te openen.

   ![](assets/create-campaign-edit-list.png)

1. Zodra uw veranderingen klaar zijn, kunt u de nieuwe versie van de campagne (zie [ Overzicht activeren en een campagne ](review-activate-campaign.md) activeren).

   >[!IMPORTANT]
   >
   >Als u het concept activeert, wordt de live versie van de campagne vervangen.

**Verwante onderwerpen:**
* [Campagneigenschappen](campaign-properties.md)
* [Campagne](campaign-action.md)
* [Campagneinhoud](campaign-content.md)
* [Campagnepubliek](campaign-audience.md)
* [Campagne](campaign-schedule.md)

### Een actiecampagne stoppen {#stop}

Als u een terugkerende campagne wilt stoppen, opent u deze en klikt u op de knop **[!UICONTROL Stop campaign]** .

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Als een campagne wordt gestopt, wordt het verzenden niet gestopt, maar wordt het geplande verzenden gestopt of het volgende verzenden als het verzenden al aan de gang is.

## Een campagne archiveren {#archive-a-campaign}

Met de tijd groeit de lijst met campagnes en wordt het uiteindelijk moeilijker om door voltooide en stopgezette campagnes te bladeren.

Om dit te voorkomen, kunt u voltooide en gestopt campagnes archiveren die u niet meer nodig hebt. Klik hiertoe op de knop voor ovaal en selecteer **[!UICONTROL Archive]** .

![](assets/create-campaign-archive.png)

Gearchiveerde campagnes kunnen vervolgens worden opgehaald met het speciale filter in de lijst.

## Een campagne verwijderen {#delete-a-campaign}

Om een campagne te schrappen, gebruik het ellips ![ beeld dat de Meer actieknoop ](assets/do-not-localize/rule-builder-icon-more.svg) toont en **[!UICONTROL Delete]** selecteert.

![](assets/delete-a-campaign.png){width="70%" align="left"}

>[!IMPORTANT]
>
>Deze optie is alleen beschikbaar voor **[!UICONTROL Draft]** -campagnes.

## Een campagne dupliceren {#duplicate-a-campaign}

Om een campagne te dupliceren, bijvoorbeeld als het is tegengehouden, gebruik het ellips ![ beeld dat de Meer actieknoop ](assets/do-not-localize/rule-builder-icon-more.svg) toont en **[!UICONTROL Duplicate]** selecteert.

Voer de naam van de campagne in en bevestig deze.

De campagne wordt gemaakt en toegevoegd aan de lijst met campagnes.

## Aanvullende bronnen

* **Begonnen het worden** - [ begonnen met campagnes ](get-started-with-campaigns.md) | [ creeer uw eerste campagne van de Actie ](create-campaign.md) | [ API-teweeggebrachte campagnegids ](api-triggered-campaigns.md) | [ Geordende campagnegids ](../orchestrated/gs-orchestrated-campaigns.md)

* **configuratie van de Campagne** - [ eigenschappen van de Campagne ](campaign-properties.md) | [ acties en kanalen van de Campagne ](campaign-action.md) | [ het inhoudsontwerp van de Campagne ](campaign-content.md) | [ de publieksselectie van de campagne ](campaign-audience.md) | [ Campagne die ](campaign-schedule.md) plant

* **Geavanceerde eigenschappen** - [ de werkschema&#39;s van de Goedkeuring ](../test-approve/gs-approval.md) | [ Conflict beheer &amp; prioritering ](../conflict-prioritization/gs-conflict-prioritization.md) | [ Het in kaart brengen van de Frequentie door kanaal ](../conflict-prioritization/channel-capping.md) | [ Prioriteitsscores ](../conflict-prioritization/priority-scores.md) | [ campagnes van de Uitvoer aan andere zandbakken ](../configuration/copy-objects-to-sandbox.md)

* **Controle &amp; optimalisering** - [ de rapporten van de Campagne (CJA) ](../reports/campaign-global-report-cja.md) | [ Het alarm van de opstelling ](../reports/alerts.md)

* **Organisatie** - [ Werk met markeringen ](../start/search-filter-categorize.md) | [ leiden toestemmingen ](../administration/ootb-product-profiles.md)
