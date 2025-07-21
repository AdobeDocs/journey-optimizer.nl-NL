---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met campagnes
description: Meer informatie over campagnes in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: campagne, hoe, begin, optimaliseer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Aan de slag met campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Campagne"
>abstract="De campagnes beginnen standaard bij handmatige activering en eindigen direct nadat het bericht eenmaal is verzonden. U hebt de flexibiliteit om een specifieke datum en tijd voor het te verzenden bericht te plaatsen. Bovendien kunt u een einddatum voor terugkerende actiecampagnes specificeren. In de triggers van Actie kunt u de verzendfrequentie van berichten ook configureren om deze aan te passen aan uw voorkeuren."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Start campagne"
>abstract="Geef een datum en tijd op waarop het bericht moet worden verzonden."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Einde campagne"
>abstract="Geef op wanneer een terugkerende campagne moet stoppen met uitvoeren."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="actieftriggers voor campagne"
>abstract="Definieer de frequentie waarmee het campagnebericht moet worden verzonden."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="Besturingselement voor de rotatiesnelheid"
>abstract="Besturingselement voor de rotatiesnelheid"

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="Campagnes maken"
>abstract="Gebruik **Adobe Journey Optimizer** om eenmalige inhoud aan een specifiek publiek te leveren gebruikend diverse kanalen. Wanneer u reizen gebruikt, worden handelingen op volgorde uitgevoerd. Met campagnes, worden de acties uitgevoerd gelijktijdig, of onmiddellijk, of gebaseerd op een gespecificeerd programma."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Maak campagnes om eenmalige inhoud aan een specifiek publiek op verschillende kanalen te leveren. Voordat u uw campagne maakt, moet u ervoor zorgen dat u een kanaalconfiguratie hebt en een Adobe Experience Platform-publiek klaar voor gebruik."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Type campagne"
>abstract="**Geplande campagnes** worden uitgevoerd onmiddellijk of op een gespecificeerde datum en zijn bedoeld om berichten van het marketingtype te verzenden. **API-teweeggebrachte** campagnes worden uitgevoerd gebruikend een API vraag. Zij zijn gericht op het verzenden van ofwel marketingberichten (promotieberichten waarvoor toestemming van de gebruiker vereist is) ofwel transactieberichten (niet-commerciële berichten die ook in specifieke omstandigheden naar niet-geabonneerde profielen kunnen worden verzonden)."

Gebruik Journey Optimizer-campagnes om via verschillende kanalen eenmalige inhoud aan een specifiek publiek te leveren. Wanneer u reizen gebruikt, worden handelingen op volgorde uitgevoerd. Met campagnes, worden de acties uitgevoerd gelijktijdig, of onmiddellijk, of gebaseerd op een gespecificeerd programma.

![](assets/gs-campaigns.png)

U kunt verschillende typen campagnes maken in Journey Optimizer:

* **campagnes van de Actie**

  De campagnes van de actie (of Geplande campagnes) staan voor eenvoudige ad hoc partijmededelingen voor marketing gebruiksgevallen zoals promotieaanbiedingen, betrokkenheidscampagnes, aankondigingen, wettelijke berichten, of beleidsupdates toe.

* **API teweeggebrachte campagnes**

  API getriggerde campagnes staan toe of voor marketing mededelingen om aan een publiek op het juiste ogenblik te bereiken, of voor transactie/operationele berichten aan een individu zoals een wachtwoordteruggestelde, waar de behoefte personalisatie kan impliceren door niet alleen profielattributen maar ook de contextgegevens in real time in de trekker te gebruiken die een nuttige lading van de WEERSTAPI is.

<!--* **Orchestrated campaigns**

    Campaign Orchestration in Adobe Journey Optimizer powers sophisticated, brand-initiated marketing campaigns across channels, helping you drive engagement, revenue, and customer loyalty at scale.

    While cross-channel marketing is essential, orchestrated campaigns make it seamless. With a visual, drag-and-drop interface, you can design and automate complex marketing workflows, from segmentation to message delivery, across multiple channels. Everything happens in one intuitive environment, built for speed, control, and efficiency.-->

## Voordat u begint {#campaign-prerequisites}

Controleer de volgende voorwaarden voordat u begint met het maken van uw eerste campagne in [!DNL Journey Optimizer] :

1. **u hebt juiste toestemmingen** nodig. Campagnes zijn alleen beschikbaar voor gebruikers met toegang tot een campagne-gerelateerde **[!UICONTROL Product profile]** , zoals Campagnebeheerder, Campagneontwikkelaar, Campagnebeheerder en/of Campagneviewer. Als u geen toegang hebt tot campagnes, moeten uw toestemmingen worden uitgebreid.

   +++Meer informatie over het toewijzen van een aan een campagne gerelateerde rol

   1. Als u een rol wilt toewijzen aan een gebruiker in het [!DNL Permissions] -product, navigeert u naar het tabblad **[!UICONTROL Roles]** en selecteert u een van de ingebouwde campagneonderdelen **[!UICONTROL Roles]** : Campagnebeheerder, campagnefiatteur, Campagnebeheerder of Campagneviewer.

   1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add user]**.

   1. Typ de naam of het e-mailadres van de gebruiker of selecteer de gebruiker in de lijst en klik op **[!UICONTROL Save]** .

      Als de gebruiker niet eerder werd gecreeerd, verwijs naar [ gebruikersdocumentatie ](https://experienceleague.adobe.com/nl/docs/experience-platform/access-control/ui/users) toevoegen.

   Uw gebruiker moet dan een e-mail ontvangen die aan uw instantie opnieuw richt.

   +++

1. **u hebt een publiek** nodig. De doelgroepen moeten beschikbaar zijn voordat ze de campagne kunnen opzetten. [ krijgt begonnen met publiek ](../audience/about-audiences.md).

1. **u hebt een kanaalconfiguratie** nodig. Als u een kanaal wilt kunnen selecteren, moet de corresponderende kanaalconfiguratie (d.w.z. vooraf ingesteld) zijn gemaakt en beschikbaar. [ leer hoe te de configuraties van het opstellingskanaal ](../configuration/channel-surfaces.md).

## Laten we dieper duiken

Nu u de campagnes in [!DNL Journey Optimizer] begrijpt, is het tijd om dieper in deze documentatiesecties te duiken om uw eerste campagnes te beginnen creëren.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="actieplannen" src="assets/do-not-localize/gs-action-campaign.png" width="50%"></a><br/><a href="create-campaign.md">Actiecampagnes</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png" width="50%"></a><br/><a href="api-triggered-campaigns.md">API-actiecampagnes</a></td>
</tr></table>

<!--
<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="action campaigns" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Action campaigns</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API triggered campaigns</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Orchestrated campaigns</a></td>
</tr></table>-->
