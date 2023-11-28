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
source-git-commit: b9630c922ff67b0a402af5f950ee4e5a442bb1b1
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 1%

---

# Campagnes beheren {#modify-stop-campaign}

Nadat een campagne is geactiveerd, kunt u deze op elk gewenst moment wijzigen of stoppen. Deze bewerkingen zijn alleen beschikbaar voor campagnes met een terugkerende uitvoering.

Daarnaast kunt u live campagnes (die één keer of met een terugkerende uitvoering worden uitgevoerd) dupliceren om nieuwe campagnes te maken en voltooide of gestopt campagnes archiveren.

## Campagnes openen {#access}

Campagnes zijn toegankelijk vanuit de **[!UICONTROL Campaigns]** -menu.

Standaard worden in de lijst alle campagnes met de **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]**, en **[!UICONTROL Live]** statussen. Om gestopt, voltooide, en gearchiveerde campagnes te tonen, moet u de filter ontruimen.

![](assets/create-campaign-list.png)

Bovendien kunt u de lijst filteren op basis van het type en het kanaal van de campagne of de tags die aan de campagnes zijn toegewezen tijdens het maken van de campagnes. [Leer hoe u tags kunt toewijzen aan een campagne](create-campaign.md#create)

## Statistieken en waarschuwingen voor campagnes {#statuses}

Campagnes kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: De campagne wordt bewerkt en is niet geactiveerd.
* **[!UICONTROL Activating]**: De campagne wordt geactiveerd.
* **[!UICONTROL Processing]** *(alleen e-mailcampagnes)*: De doelexport is voltooid, de campagne wordt gepubliceerd.
* **[!UICONTROL Live]**: De campagne is geactiveerd.
* **[!UICONTROL Scheduled]**: De campagne is geconfigureerd om te worden geactiveerd op een specifieke startdatum.
* **[!UICONTROL Stopped]**: De campagne is handmatig gestopt. U kunt het niet meer activeren of opnieuw gebruiken. [Leer hoe u een campagne kunt stoppen](modify-stop-campaign.md#stop)
* **[!UICONTROL Completed]**: De campagne is voltooid. Deze status wordt automatisch toegewezen 3 dagen nadat een campagne is geactiveerd, of op de einddatum van de campagne als de campagne een terugkerende uitvoering heeft.
* **[!UICONTROL Archived]**: De campagne is gearchiveerd. [Leer campagnes archiveren](modify-stop-campaign.md#archive)

>[!NOTE]
>
>Het pictogram Conceptversie openen naast een **[!UICONTROL Live]** of **[!UICONTROL Scheduled]** status geeft aan dat er een nieuwe versie van de campagne is gemaakt en nog niet is geactiveerd. [Meer informatie](modify-stop-campaign.md#modify).

Als er een fout optreedt in een van uw campagnes, verschijnt er een waarschuwingspictogram naast de status van de campagne. Klik erop om informatie over de waarschuwing weer te geven. Deze waarschuwingen kunnen zich in verschillende situaties voordoen, bijvoorbeeld wanneer het campagnebericht niet is gepubliceerd of wanneer het gekozen oppervlak onjuist is.

![](assets/campaign-alerts.png)

## Een terugkerende campagne wijzigen {#modify}

Voer de volgende stappen uit om een terugkerende campagne te wijzigen en een nieuwe versie ervan te maken:

1. Open de campagne en klik op **[!UICONTROL Modify campaign]** knop.

1. Er wordt een nieuwe versie van de campagne gemaakt. U kunt de live versie controleren door op **[!UICONTROL Open live version]**.

   ![](assets/create-campaign-draft.png)

   In de lijst met campagnes worden geactiveerde campagnes met een conceptversie in uitvoering weergegeven met een specifiek pictogram in het dialoogvenster **[!UICONTROL Status]** kolom. Klik op dit pictogram om de conceptversie van de campagne te openen.

   ![](assets/create-campaign-edit-list.png)

1. Als uw wijzigingen gereed zijn, kunt u de nieuwe versie van de campagne activeren (zie [Een campagne bekijken en activeren](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >Als u het concept activeert, wordt de live versie van de campagne vervangen.

## Een terugkerende campagne stoppen {#stop}

Als u een terugkerende campagne wilt stoppen, opent u deze en klikt u op de knop **[!UICONTROL Stop campaign]** knop.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Als een campagne wordt gestopt, wordt het verzenden niet gestopt, maar wordt het geplande verzenden gestopt of het volgende verzenden als het verzenden al bezig is.

<!-- inbound campaign (inapp): can stop and resume -->

## Een campagne dupliceren {#duplicate}

U kunt een live campagne dupliceren om een nieuwe te maken. Om dit te doen, open de campagne, dan klik **[!UICONTROL Duplicate]**.

![](assets/create-campaign-duplicate.png)

## Een campagne archiveren {#archive}

Met de tijd groeit de lijst met campagnes en wordt het uiteindelijk moeilijker om door voltooide en stopgezette campagnes te bladeren.

Om dit te voorkomen, kunt u voltooide en gestopt campagnes archiveren die u niet meer nodig hebt. Klik hiertoe op de knop voor ovaal en selecteer **[!UICONTROL Archive]**.

![](assets/create-campaign-archive.png)

Gearchiveerde campagnes kunnen vervolgens worden opgehaald met het speciale filter in de lijst. [Leer hoe u campagnes kunt openen](get-started-with-campaigns.md#access)
