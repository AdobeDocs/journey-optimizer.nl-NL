---
title: Aan de slag met campagnes
description: Meer informatie over campagnes in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6177a33edeb3b8381c3eb5609762b4d974dc93e3
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 2%

---


# Aan de slag met campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Met campagnes, kunt u eenmalig inhoud aan een specifiek segment over veelvoudige kanalen leveren. Voordat u een nieuwe campagne maakt, moet u een berichtvoorinstelling en een Adobe Experience Platform-segment klaar voor gebruik hebben."

## Informatie over campagnes {#about}

Met campagnes kunt u eenmalige inhoud leveren aan een specifiek segment met behulp van meerdere kanalen. In tegenstelling tot reizen, waar acties worden ontworpen om in opeenvolging te worden uitgevoerd, voeren de campagnes acties gelijktijdig, of onmiddellijk, of op een gespecificeerd programma uit.

U kunt twee typen campagnes maken:

* **Geplande campagnes** voor eenvoudige ad-hoc partijmededelingen voor marketing gebruiksgevallen zoals promotieaanbiedingen, betrokkenheidscampagnes, aankondigingen, wettelijke berichten, of beleidsupdates toestaan.
* **API-gestuurde campagnes** eenvoudige transactie-/operationele berichten mogelijk maken met REST API&#39;s (opnieuw instellen van wachtwoorden, annuleren van kaarten, enz.), waarbij de behoefte kan bestaan uit personalisatie met behulp van profielkenmerken en contextafhankelijke gegevens van lading.

Leer hoe u met campagnes kunt werken:
* [Een campagne maken](create-campaign.md)
* [API-gestuurde campagnes maken](api-triggered-campaigns.md)
* [Een campagne wijzigen of stoppen](modify-stop-campaign.md)
* [Campagne live-rapport](campaign-live-report.md)
* [Globaal verslag campagne voeren](campaign-global-report.md)

## Campagnes openen {#access}

Campagnes zijn toegankelijk vanuit de **[!UICONTROL Campaigns]** -menu.

Standaard worden in de lijst alle campagnes met de **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]**, en **[!UICONTROL Live]** statussen. Om gestopt, voltooide en gearchiveerde campagnes te tonen, moet u de filter ontruimen.

![](assets/create-campaign-list.png)

## Campagnestatus {#statuses}

Campagnes kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: De campagne wordt bewerkt en is niet geactiveerd.
* **[!UICONTROL Activating]**: De campagne wordt geactiveerd.
* **[!UICONTROL Live]**: De campagne is geactiveerd.
* **[!UICONTROL Scheduled]**: De campagne is geconfigureerd om te worden geactiveerd op een specifieke startdatum.
* **[!UICONTROL Stopped]**: De campagne is handmatig gestopt. U kunt het niet meer activeren of opnieuw gebruiken (zie [Een campagne stoppen](modify-stop-campaign.md#stop))
* **[!UICONTROL Completed]**: De campagne is voltooid.
* **[!UICONTROL Archived]**: De campagne is gearchiveerd.

>[!NOTE]
>
>Het pictogram Conceptversie openen naast een **[!UICONTROL Live]** of **[!UICONTROL Scheduled]** status geeft aan dat er een nieuwe versie van de campagne is gemaakt en nog niet is geactiveerd (zie [Een campagne wijzigen](modify-stop-campaign.md#modify)).
