---
solution: Journey Optimizer
product: journey optimizer
title: Campagnes openen en beheren
description: Leer hoe u uw campagnes in Journey Optimizer kunt openen en beheren.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: campagnes, status, planning, toegang, optimaliseren beheren
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Campagnes openen en beheren {#modify-stop-campaign}

## Campagnes openen {#access}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_view"
>title="Lijst- en kalenderweergaven van campagnes"
>abstract="Naast de lijst met campagnes biedt [!DNL Journey Optimizer] een kalenderweergave van uw campagnes en een duidelijke visuele weergave van hun programma&#39;s. Met deze knoppen kunt u op elk gewenst moment schakelen tussen de lijst- en de kalenderweergave."

Campagnes zijn toegankelijk via het menu **[!UICONTROL Campaigns]** .

>[!BEGINTABS]

>[!TAB  campagnes van de Actie ]

Selecteer het tabblad **[!UICONTROL Action]** voor toegang tot de lijst met actiecampagnes.

Standaard worden in de lijst alle campagnes met de statussen **[!UICONTROL Draft]** , **[!UICONTROL Scheduled]** en **[!UICONTROL Live]** weergegeven. Om gestopt, voltooide, en gearchiveerde campagnes te tonen, moet u de filter ontruimen.

![](assets/create-campaign-list.png)

>[!TAB  API teweeggebrachte campagnes ]

Selecteer het tabblad **[!UICONTROL API triggered]** voor toegang tot de lijst met API-geactiveerde campagnes.

Standaard worden in de lijst alle campagnes met de statussen **[!UICONTROL Draft]** , **[!UICONTROL Scheduled]** en **[!UICONTROL Live]** weergegeven. Om gestopt, voltooide, en gearchiveerde campagnes te tonen, moet u de filter ontruimen.

![](assets/api-triggered-list.png)

>[!ENDTABS]

U kunt de lijst ook filteren op basis van het type en het kanaal van de campagne of de tags die aan de campagnes zijn toegewezen tijdens het maken van de campagnes.

## Campagne-kalender {#calendar}

Naast de lijst met campagnes biedt [!DNL Journey Optimizer] een kalenderweergave van uw campagnes en een duidelijke visuele weergave van hun programma&#39;s.

>[!AVAILABILITY]
>
>De kalenderweergave is momenteel alleen beschikbaar voor een set organisaties (beperkte beschikbaarheid). Om toegang te verzoeken, gebruik [ deze vorm ](https://forms.cloud.microsoft/r/FC49afuJVi){target=”_blank”}.
>
>Deze functie is actief ontwikkeld. We verwelkomen uw invoer en verzoeken met de knop **[!UICONTROL Beta Feedback]** in het bovenste menu.

In de kalender worden alle campagnes weergegeven die voor de huidige week zijn gepland. Gebruik de pijlknoppen boven de kalender om tussen weken te navigeren.

![ kalendermening die levende campagnes tonen ](assets/campaigns-timeline.png)

Hoe campagnes worden vertegenwoordigd:

* Standaard worden in het kalenderraster alle live en geplande campagnes voor de geselecteerde week weergegeven. Aanvullende filteropties kunnen voltooide, gestopt en voltooide activeringen of activeringen van een bepaald type of kanaal weergeven.
* Conceptcampagnes worden niet weergegeven.
* Campagnes die meerdere dagen beslaan, worden boven in het kalenderraster weergegeven.
* Als er geen begintijd is opgegeven, wordt de dichtstbijzijnde handmatige activeringstijd gebruikt om deze in de kalender te plaatsen.
* Campagnes worden getoond als timespans van 1 uur, maar dit weerspiegelt geen daadwerkelijke verzend of voltooiingstijd.

Voor meer informatie over een campagne klikt u op het visuele blok om de details ervan te openen.

Als u details voor een specifieke campagne wilt weergeven, selecteert u deze in de lijst. Er wordt een informatievenster geopend met verschillende informatie over de campagne, zoals het type, de toegang tot de rapporten of de tags die zijn toegewezen.

![ campagnemijst met de informatieruit geopend ](assets/campaign-rail.png)

## Statistieken en waarschuwingen voor campagnes {#statuses}

Campagnes kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: De campagne wordt bewerkt en is niet geactiveerd.
* **[!UICONTROL Scheduled]**: De campagne is geconfigureerd om te worden geactiveerd op een specifieke startdatum.
* **[!UICONTROL Live]**: De campagne is geactiveerd.
* **[!UICONTROL In review]**: De campagne is ter goedkeuring voorgelegd om te worden gepubliceerd. [ leer hoe te met goedkeuringen ](../test-approve/gs-approval.md) werken
* **[!UICONTROL Stopped]**: de campagne is handmatig gestopt. U kunt het niet meer activeren of opnieuw gebruiken. [ Leer hoe te om een campagne ](modify-stop-campaign.md#stop) tegen te houden
* **[!UICONTROL Completed]**: de campagne is voltooid. Deze status wordt automatisch toegewezen 3 dagen nadat een campagne is geactiveerd, of op de einddatum van de campagne als de campagne een terugkerende uitvoering heeft.
* **[!UICONTROL Failed]**: De uitvoering van de campagne is mislukt. Controleer de logboeken om de kwestie te identificeren.
* **[!UICONTROL Archived]**: De campagne is gearchiveerd. [ Leer hoe te om campagnes te archiveren ](modify-stop-campaign.md#archive)

>[!NOTE]
>
>Het pictogram &#39;Conceptversie openen&#39; naast de status **[!UICONTROL Live]** of **[!UICONTROL Scheduled]** geeft aan dat een nieuwe versie van de campagne is gemaakt en nog niet is geactiveerd. [Meer informatie](modify-stop-campaign.md#modify).

Als er een fout optreedt in een van uw campagnes, verschijnt er een waarschuwingspictogram naast de status van de campagne. Klik erop om informatie over de waarschuwing weer te geven. Deze waarschuwingen kunnen zich in verschillende situaties voordoen, bijvoorbeeld wanneer het campagnebericht niet is gepubliceerd of wanneer de gekozen configuratie onjuist is.

![](assets/campaign-alerts.png)

## Herhaalde handelingscampagnes wijzigen en stoppen {#modify}

### Een handelingscampagne wijzigen

Ga als volgt te werk om een terugkerende actiecampagne te wijzigen en een nieuwe versie te maken:

1. Open de actiecampagne en klik op de knop **[!UICONTROL Modify campaign]** .

1. Er wordt een nieuwe versie van de campagne gemaakt. U kunt de live versie controleren door op **[!UICONTROL Open live version]** te klikken.

   ![](assets/create-campaign-draft.png)

   In de lijst met campagnes worden geactiveerde campagnes met een conceptversie in uitvoering weergegeven met een specifiek pictogram in de kolom **[!UICONTROL Status]** . Klik op dit pictogram om de conceptversie van de campagne te openen.

   ![](assets/create-campaign-edit-list.png)

1. Zodra uw veranderingen klaar zijn, kunt u de nieuwe versie van de campagne (zie [ Overzicht activeren en een campagne ](create-campaign.md#review-activate) activeren).

   >[!IMPORTANT]
   >
   >Als u het concept activeert, wordt de live versie van de campagne vervangen.

### Een actiecampagne stoppen {#stop}

Als u een terugkerende campagne wilt stoppen, opent u deze en klikt u op de knop **[!UICONTROL Stop campaign]** .

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Als een campagne wordt gestopt, wordt het verzenden niet gestopt, maar wordt een geplande verzending gestopt of de volgende keren als het verzenden al bezig is.

## Een campagne dupliceren {#duplicate}

U kunt een campagne dupliceren om een nieuwe te maken. U doet dit door de campagne te openen en vervolgens op **[!UICONTROL Duplicate]** te klikken.

![](assets/create-campaign-duplicate.png)

## Een campagne archiveren {#archive}

Met de tijd groeit de lijst met campagnes en wordt het uiteindelijk moeilijker om door voltooide en stopgezette campagnes te bladeren.

Om dit te voorkomen, kunt u voltooide en gestopt campagnes archiveren die u niet meer nodig hebt. Klik hiertoe op de knop voor ovaal en selecteer **[!UICONTROL Archive]** .

![](assets/create-campaign-archive.png)

Gearchiveerde campagnes kunnen vervolgens worden opgehaald met het speciale filter in de lijst.
