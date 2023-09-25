---
solution: Journey Optimizer
product: journey optimizer
title: Creeer een IP warmlopingsplan
description: Leer hoe te om een IP warmup plan tot stand te brengen
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, groep, subdomeinen, leverbaarheid
hide: true
hidefromtoc: true
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 1%

---

# Creeer een IP warmlopingsplan {#ip-warmup}

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Ga aan de slag met IP-opwarming](ip-warmup-gs.md)
* [IP-warmtecampagnes maken](ip-warmup-campaign.md)
* **[Creeer een IP warmlopingsplan](ip-warmup-plan.md)**
* [Voer het IP-opwarmingsplan uit](ip-warmup-running.md)

>[!ENDSHADEBOX]

Nadat u een of meer [IP-opwarmingscampagnes](ip-warmup-campaign.md) met een specifieke toegelaten oppervlakte en de overeenkomstige toegelaten optie, kunt u beginnen tot uw IP warmup plan te leiden.

## Vul het IP warmup malplaatje in {#upload-plan}

Alvorens een IP warmup plan in de interface van Journey Optimizer te kunnen tot stand brengen, moet u een malplaatje in het formaat van Excel met alle gegevens invullen die uw plan zullen voeren.

>[!CAUTION]
>
>Werk met uw leverancier consultant om ervoor te zorgen dat uw IP-bestand met opwarmingsplannen correct is ingesteld.

Hieronder is een voorbeeld van een dossier dat een IP warmlopingsplan bevat.

![](assets/ip-warmup-sample-file.png)

### Het lusje van het Plan van de Warmup

IP de warmte-up is een activiteit die in het geleidelijk verhogen van het volume van e-mails bestaat die van uw IPs en domein aan de belangrijkste dienstverleners van Internet (ISPs) gaan om uw reputatie als wettige afzender te vestigen.

Deze activiteit wordt vaak uitgevoerd met de hulp van een leveringsconsultant of deskundige die een weloverwogen plan voorbereidt dat op het industrieterrein, gebruikscase, regio, ISPs en diverse andere factoren wordt gebaseerd.

* In dit voorbeeld is een plan opgesteld dat zich over 17 dagen uitstrekt en een doelvolume van xxx profielen bereikt.

* Dit plan wordt uitgevoerd in zes fasen.

* U kunt zoveel kolommen hebben als u wilt voor de domeinen u aan wilt leveren. In dit voorbeeld, is het plan verdeeld in vier kolommen die aan de domeingroepen beantwoorden in uw plan te gebruiken: Gmail, Adobe, Yahoo en anderen.

Het idee is meer looppas in de eerste fasen te hebben en het aantal gerichte adressen geleidelijk te verhogen terwijl het verminderen van het aantal looppas.

De lijst van uit-van-de-doos domeinen is als volgt:

* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigvijver
* Oranje
* Softbank
* Docomo
* United Internet
* Microsoft
* KDDI
* Italia Online
* La Poste
* Apple

### Tabblad Aangepaste domeingroep

U kunt ook meer kolommen toevoegen met uw aangepaste domeingroepen.

Gebruik de **[!UICONTROL Custom Domain Group]** om een nieuw domein te definiëren en voor elk domein kunt u alle subdomeinen toevoegen waarop het betrekking heeft.<!--TBC-->

## Toegang en beheer IP-opwarmingsplannen {#manage-ip-warmup-plans}

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]**. Alle IP warmup die plannen tot nu toe worden gecreeerd worden getoond.

   ![](assets/ip-warmup-filter-list.png)

1. U kunt filteren op de status. De verschillende statussen zijn:

   * **Niet gestart**: er is nog geen uitvoering geactiveerd. [Meer informatie](ip-warmup-running.md#define-runs)
   * **Wordt uitgevoerd/Live**: het plan neemt deze status in zodra de eerste run in de eerste fase met succes is geactiveerd. [Meer informatie](ip-warmup-running.md#define-runs)
   * **Voltooid**: het plan is gemarkeerd als voltooid. Deze optie is alleen beschikbaar als alle runnen in het abonnement zijn opgenomen **[!UICONTROL Succeeded]** of **[!UICONTROL Draft]** status (geen run kan worden uitgevoerd) **[!UICONTROL Live]**). [Meer informatie](ip-warmup-running.md#define-runs#mark-as-completed)
   * **Gepauzeerd**<!--: to check (user action)-->

1. Om een IP warmup plan te schrappen, selecteer **[!UICONTROL Delete]** naast een lijstitem en het verwijderen bevestigen.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >Het geselecteerde IP warmup plan zal permanent worden geschrapt.

## Creeer een IP warmlopingsplan {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Specificeer uw IP warmtekrachtplan"
>abstract="Download het malplaatje CSV en vul het met gegevens voor IP warmup fasen en doelaantal profielen."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Een marketingoppervlak selecteren"
>abstract="U moet de zelfde oppervlakte selecteren zoals die in de campagne wordt geselecteerd u met uw IP warmup plan wilt associëren."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="Kanaaloppervlakken instellen"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="IP-warmtecampagnes maken"

Wanneer een of meer live campagnes met de **[!UICONTROL IP warmup plan activation]** toegelaten optie wordt geactiveerd, kunt u hen met een IP warmlopingsplan associëren.

>[!CAUTION]
>
>Om IP warmup plannen tot stand te brengen, uit te geven en te schrappen, moet u hebben **[!UICONTROL Deliverability Consultant]** toestemming. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->
>
>Werk samen met uw leverancier om ervoor te zorgen dat uw IP het malplaatje van het warmlopingsplan correct opstelling is. <!--TBC-->

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]** en klik vervolgens op **[!UICONTROL Create IP warmup plan]**.

   ![](assets/ip-warmup-create-plan.png)

1. Vul de IP details van het warmlopingsplan in: geef het een naam en een beschrijving.

   ![](assets/ip-warmup-plan-details.png)

1. Selecteer een [oppervlak](channel-surfaces.md). Alleen marketingoppervlakken zijn beschikbaar voor selectie. [Meer informatie over e-mailtypen](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >U moet de zelfde oppervlakte selecteren zoals die in de campagne wordt geselecteerd u met uw IP warmup plan wilt associëren. [Leer hoe te om een IP warmup campagne te creëren](#create-ip-warmup-campaign)

1. Upload het dossier van Excel dat uw IP warmup plan bevat<!--which formats are allowed?-->. U kunt de sjabloon gebruiken die door het leveringsteam wordt aangeboden.<!--TBC?--> [Meer informatie](#upload-plan)
   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. Klik op **[!UICONTROL Create]**. Het aantal fasen dat is gedefinieerd in het bestand dat u hebt geüpload, wordt automatisch weergegeven voor elke fase. [Meer informatie](#upload-plan)

   ![](assets/ip-warmup-plan-phases.png)

## Upload een IP warmup plan opnieuw {#re-upload-plan}

U kunt een ander IP warmlopingsplan opnieuw uploaden gebruikend de overeenkomstige knoop.

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>De IP details van het warmup plan zullen veranderen zoals per het onlangs geupload dossier. De volledige looppas en de geactiveerde looppas worden niet beïnvloed.