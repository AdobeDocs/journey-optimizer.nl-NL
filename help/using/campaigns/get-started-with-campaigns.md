---
title: Aan de slag met campagnes
description: Meer informatie over campagnes in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 8d8586a6c70b6fc01dbd1c2a8833079f422c93f7
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---

# Aan de slag met campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Met campagnes, kunt u eenmalig inhoud aan een specifiek segment over veelvoudige kanalen leveren. Voordat u een nieuwe campagne maakt, moet u ervoor zorgen dat u een kanaaloppervlak (d.w.z. een voorinstelling voor berichten) en een Adobe Experience Platform-segment gebruiksklaar hebt."

## Informatie over campagnes {#about}

Met campagnes kunt u eenmalige inhoud leveren aan een specifiek segment met behulp van meerdere kanalen. In tegenstelling tot reizen, waar acties worden ontworpen om in opeenvolging te worden uitgevoerd, voeren de campagnes acties gelijktijdig, of onmiddellijk, of op een gespecificeerd programma uit.

Op deze manier kunt u eenvoudige ad-hocbatchberichten verzenden voor marketingdoeleinden, zoals promotieaanbiedingen, betrokkenheidscampagnes, aankondigingen, juridische kennisgevingen of beleidsupdates.

➡️ [Ontdek deze functie in video](#video)

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

## Vereisten {#campaign-prerequisites}

Campagne is alleen beschikbaar voor gebruikers met toegang tot een campagne in verband met **[!UICONTROL Product profile]** zoals Campagnebeheerder, Campagneontwikkelaar, Campagnebeheerder en/of Campagneviewer.

Om de overeenkomstige **[!UICONTROL Product profile]** aan uw gebruikers:

1. Van de [!DNL Admin console], selecteert u de [!DNL Adobe Experience Platform] product.

1. Van de **[!UICONTROL Product profile]** selecteert u een van de ingebouwde campagnes die betrekking hebben op **[!UICONTROL Product profile]**: Campagnebeheerder, campagnefiatteur, campagnebeheerder of campagneviewer.

   Meer informatie over campagne **[!UICONTROL Product profiles]** en **[!UICONTROL Permissions]**, verwijzen naar [page](../administration/ootb-product-profiles.md).

   ![](assets/do-not-localize/admin_1.png)

1. Klikken **[!UICONTROL Add user]** om aan uw gebruiker toe te wijzen selecteerde **[!UICONTROL Product profile]**.

   ![](assets/do-not-localize/admin_2.png)

1. Typ de naam, de groep of het e-mailadres van uw gebruiker en klik op **[!UICONTROL Save]**.

De gebruiker heeft nu toegang tot **[!UICONTROL Campaigns]**.

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
* **[!UICONTROL Completed]**: De campagne is voltooid. Deze status wordt automatisch toegewezen 3 dagen nadat een campagne is geactiveerd, of op de einddatum van de campagne als de campagne een terugkerende uitvoering heeft.
* **[!UICONTROL Archived]**: De campagne is gearchiveerd.

>[!NOTE]
>
>Het pictogram Conceptversie openen naast een **[!UICONTROL Live]** of **[!UICONTROL Scheduled]** status geeft aan dat er een nieuwe versie van de campagne is gemaakt en nog niet is geactiveerd (zie [Een campagne wijzigen](modify-stop-campaign.md#modify)).

## Hoe kan ik-video {#video}

Leer hoe u uw eerste campagne kunt maken.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
