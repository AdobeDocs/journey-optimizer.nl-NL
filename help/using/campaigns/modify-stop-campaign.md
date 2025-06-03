---
solution: Journey Optimizer
product: journey optimizer
title: Een campagne wijzigen of stoppen
description: Leer hoe u live campagnes in Journey Optimizer kunt wijzigen, stoppen of dupliceren
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: campagnes, status, planning, toegang, optimaliseren beheren
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 1ad534b7877f0ac6c1f50e29f41af708e83b34c9
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Campagnes beheren {#modify-stop-campaign}

Nadat een campagne is geactiveerd, kunt u deze op elk gewenst moment wijzigen of stoppen. Deze bewerkingen zijn alleen beschikbaar voor campagnes met een terugkerende uitvoering.

Daarnaast kunt u live campagnes (die één keer of met een terugkerende uitvoering worden uitgevoerd) dupliceren om nieuwe campagnes te maken en voltooide of gestopt campagnes archiveren.

## Campagnes openen {#access}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_view"
>title="Lijst- en kalenderweergaven van campagnes"
>abstract="Naast de lijst met campagnes biedt [!DNL Journey Optimizer] een kalenderweergave van uw campagnes en een duidelijke visuele weergave van hun programma&#39;s. Met deze knoppen kunt u op elk gewenst moment schakelen tussen de lijst- en de kalenderweergave."

Campagnes zijn toegankelijk via het menu **[!UICONTROL Campaigns]** .

Standaard worden in de lijst alle campagnes met de statussen **[!UICONTROL Draft]** , **[!UICONTROL Scheduled]** en **[!UICONTROL Live]** weergegeven. Om gestopt, voltooide, en gearchiveerde campagnes te tonen, moet u de filter ontruimen.

![](assets/create-campaign-list.png)

U kunt de lijst ook filteren op basis van het type en het kanaal van de campagne of de tags die aan de campagnes zijn toegewezen tijdens het maken van de campagnes. [ Leer hoe te om markeringen aan een campagne toe te wijzen ](create-campaign.md#create)

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
* **[!UICONTROL Activating]**: De campagne wordt geactiveerd.
* **[!UICONTROL Processing]** *(e-mailcampagnes slechts)*: De publieksuitvoer is volledig, wordt de campagne gepubliceerd.
* **[!UICONTROL Live]**: De campagne is geactiveerd.
* **[!UICONTROL Scheduled]**: De campagne is geconfigureerd om te worden geactiveerd op een specifieke startdatum.
* **[!UICONTROL Stopped]**: de campagne is handmatig gestopt. U kunt het niet meer activeren of opnieuw gebruiken. [ Leer hoe te om een campagne ](modify-stop-campaign.md#stop) tegen te houden
* **[!UICONTROL Completed]**: de campagne is voltooid. Deze status wordt automatisch toegewezen 3 dagen nadat een campagne is geactiveerd, of op de einddatum van de campagne als de campagne een terugkerende uitvoering heeft.
* **[!UICONTROL Archived]**: De campagne is gearchiveerd. [ Leer hoe te om campagnes te archiveren ](modify-stop-campaign.md#archive)

>[!NOTE]
>
>Het pictogram &#39;Conceptversie openen&#39; naast de status **[!UICONTROL Live]** of **[!UICONTROL Scheduled]** geeft aan dat een nieuwe versie van de campagne is gemaakt en nog niet is geactiveerd. [Meer informatie](modify-stop-campaign.md#modify).

Als er een fout optreedt in een van uw campagnes, verschijnt er een waarschuwingspictogram naast de status van de campagne. Klik erop om informatie over de waarschuwing weer te geven. Deze waarschuwingen kunnen zich in verschillende situaties voordoen, bijvoorbeeld wanneer het campagnebericht niet is gepubliceerd of wanneer de gekozen configuratie onjuist is.

![](assets/campaign-alerts.png)

## Een terugkerende campagne wijzigen {#modify}

Voer de volgende stappen uit om een terugkerende campagne te wijzigen en een nieuwe versie ervan te maken:

1. Open de campagne en klik op de knop **[!UICONTROL Modify campaign]** .

1. Er wordt een nieuwe versie van de campagne gemaakt. U kunt de live versie controleren door op **[!UICONTROL Open live version]** te klikken.

   ![](assets/create-campaign-draft.png)

   In de lijst met campagnes worden geactiveerde campagnes met een conceptversie in uitvoering weergegeven met een specifiek pictogram in de kolom **[!UICONTROL Status]** . Klik op dit pictogram om de conceptversie van de campagne te openen.

   ![](assets/create-campaign-edit-list.png)

1. Zodra uw veranderingen klaar zijn, kunt u de nieuwe versie van de campagne (zie [ Overzicht activeren en een campagne ](create-campaign.md#review-activate) activeren).

   >[!IMPORTANT]
   >
   >Als u het concept activeert, wordt de live versie van de campagne vervangen.

## Een terugkerende campagne stoppen {#stop}

Als u een terugkerende campagne wilt stoppen, opent u deze en klikt u op de knop **[!UICONTROL Stop campaign]** .

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Als een campagne wordt gestopt, wordt het verzenden niet gestopt, maar wordt een geplande verzending gestopt of de volgende keren als het verzenden al bezig is.

<!-- inbound campaign (inapp): can stop and resume -->

## Een campagne dupliceren {#duplicate}

U kunt een live campagne dupliceren om een nieuwe te maken. U doet dit door de campagne te openen en vervolgens op **[!UICONTROL Duplicate]** te klikken.

![](assets/create-campaign-duplicate.png)

## Een campagne archiveren {#archive}

Met de tijd groeit de lijst met campagnes en wordt het uiteindelijk moeilijker om door voltooide en stopgezette campagnes te bladeren.

Om dit te voorkomen, kunt u voltooide en gestopt campagnes archiveren die u niet meer nodig hebt. Klik hiertoe op de knop voor ovaal en selecteer **[!UICONTROL Archive]** .

![](assets/create-campaign-archive.png)

Gearchiveerde campagnes kunnen vervolgens worden opgehaald met het speciale filter in de lijst. [ Leer hoe te om tot campagnes toegang te hebben ](get-started-with-campaigns.md#access)
