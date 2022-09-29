---
title: Aan de slag met campagnes
description: Meer informatie over campagnes in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 5a33508759d527a76dd7119102358ae345107652
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 3%

---

# Aan de slag met campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Maak campagnes om eenmalige inhoud aan een specifiek segment over verschillende kanalen te leveren. Voordat u de campagne maakt, moet u controleren of u een kanaaloppervlak (d.w.z. een berichtvoorinstelling) en een Adobe Experience Platform-segment hebt die u kunt gebruiken."

Gebruik Journey Optimizer-campagnes om eenmalige inhoud via verschillende kanalen aan een specifiek segment te leveren. Wanneer u reizen gebruikt, worden handelingen op volgorde uitgevoerd. Met campagnes, worden de acties uitgevoerd gelijktijdig, of onmiddellijk, of gebaseerd op een gespecificeerd programma.

U kunt twee typen campagnes maken:

* **Geplande campagnes** voor eenvoudige ad-hoc partijmededelingen voor marketing gebruiksgevallen zoals promotieaanbiedingen, betrokkenheidscampagnes, aankondigingen, wettelijke berichten, of beleidsupdates toestaan.
* **API-gestuurde campagnes** eenvoudige transactie-/operationele berichten mogelijk maken met REST API&#39;s (opnieuw instellen van wachtwoorden, annuleren van kaarten, enz.), waarbij de behoefte kan bestaan uit personalisatie met behulp van profielkenmerken en contextafhankelijke gegevens van lading.

De belangrijkste stappen voor het opzetten van een campagne zijn:

![](assets/create-campaign-process.png)

➡️ [Ontdek deze functie in video](#video)

## Voordat u begint {#campaign-prerequisites}

Controleer de volgende voorwaarden voordat u begint met het maken van uw eerste campagne in Journey Optimizer:

1. **U hebt de juiste machtigingen nodig**. Campagnes zijn alleen beschikbaar voor gebruikers die toegang hebben tot een campagne **[!UICONTROL Product profile]** zoals Campagnebeheerder, Campagneontwikkelaar, Campagnebeheerder en/of Campagneviewer.

   Als u geen toegang hebt tot campagnes, moeten uw toestemmingen worden uitgebreid. Als u toegang hebt tot [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} voor uw organisatie voert u de onderstaande stappen uit. Als dat niet het geval is, neemt u contact op met uw Journey Optimizer-beheerder.

   +++Leer hoe u campagnemachtigingen toewijst

   Om de overeenkomstige **[!UICONTROL Product profile]** aan uw gebruikers:

   1. Van [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} selecteert u de optie [!DNL Adobe Experience Platform] product.

   1. Bladeren naar de **[!UICONTROL Product profile]** selecteert u een van de ingebouwde campagnes die betrekking hebben op **[!UICONTROL Product profile]**: Campagnebeheerder, campagnefiatteur, campagnebeheerder of campagneviewer.

      Meer informatie over de Journey Optimizer-campagne **[!UICONTROL Product profiles]** en **[!UICONTROL Permissions]**, [verwijzen naar deze pagina](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Klikken **[!UICONTROL Add user]** om aan uw gebruiker toe te wijzen selecteerde **[!UICONTROL Product profile]**.

      ![](assets/do-not-localize/admin_2.png)

   1. Typ de naam, de groep of het e-mailadres van uw gebruiker en klik op **[!UICONTROL Save]**.
   Uw gebruiker heeft nu toegang tot **[!UICONTROL Campaigns]**.

+++

1. **U hebt een publiek nodig**. De segmenten van het publiek moeten beschikbaar zijn alvorens de campagne te creëren. Meer informatie over publiek maken [op deze pagina](../segment/about-segments.md).
1. **U hebt een kanaaloppervlak nodig**. Als u een kanaal wilt selecteren, moet het bijbehorende kanaaloppervlak (dus de voorinstelling) zijn gemaakt en beschikbaar. Meer informatie over kanaaloppervlakken [op deze pagina](../configuration/channel-surfaces.md).

## Campagnes openen {#access}

Campagnes zijn toegankelijk vanuit de **[!UICONTROL Campaigns]** -menu.

Standaard worden in de lijst alle campagnes met de **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]**, en **[!UICONTROL Live]** statussen. Om gestopt, voltooide, en gearchiveerde campagnes te tonen, moet u de filter ontruimen.

![](assets/create-campaign-list.png)

## Campagnestatus {#statuses}

Campagnes kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: De campagne wordt bewerkt en is niet geactiveerd.
* **[!UICONTROL Activating]**: De campagne wordt geactiveerd.
* **[!UICONTROL Live]**: De campagne is geactiveerd.
* **[!UICONTROL Scheduled]**: De campagne is geconfigureerd om te worden geactiveerd op een specifieke startdatum.
* **[!UICONTROL Stopped]**: De campagne is handmatig gestopt. U kunt het niet meer activeren of opnieuw gebruiken. [Meer informatie](modify-stop-campaign.md#stop)
* **[!UICONTROL Completed]**: De campagne is voltooid. Deze status wordt automatisch toegewezen 3 dagen nadat een campagne is geactiveerd, of op de einddatum van de campagne als de campagne een terugkerende uitvoering heeft.
* **[!UICONTROL Archived]**: De campagne is gearchiveerd.

>[!NOTE]
>
>Het pictogram Conceptversie openen naast een **[!UICONTROL Live]** of **[!UICONTROL Scheduled]** status geeft aan dat een nieuwe versie van de campagne is gemaakt en nog niet is geactiveerd. [Meer informatie](modify-stop-campaign.md#modify).

## Hoe kan ik-video {#video}

Leer hoe u uw eerste campagne kunt maken.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
