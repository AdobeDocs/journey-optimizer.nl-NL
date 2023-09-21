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
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '519'
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

## Toegang en beheer IP-opwarmingsplannen {#manage-ip-warmup-plans}

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]**. Alle IP warmup die plannen tot nu toe worden gecreeerd worden getoond.

   ![](assets/ip-warmup-filter-list.png)

1. U kunt filteren op de status. De verschillende statussen zijn:

   * **Niet gestart**: er is geen run uitgevoerd
   * **In uitvoering**: zodra een run is gestart <!--or is done?-->
   * **Gepauzeerd**
   * **Voltooid**: alle uitvoeringen in het plan zijn uitgevoerd

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

>[!CAUTION]
>
>Om IP warmup plannen tot stand te brengen, uit te geven en te schrappen, moet u hebben **[!UICONTROL Deliverability Consultant]** toestemming.
<!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

Wanneer een of meer live campagnes met de **[!UICONTROL IP warmup plan activation]** toegelaten optie wordt geactiveerd, kunt u hen met een IP warmlopingsplan associëren.

>[!CAUTION]
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

### Upload een IP warmup plan opnieuw {#re-upload-plan}

U kunt een ander IP warmlopingsplan opnieuw uploaden gebruikend de overeenkomstige knoop.

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>De IP details van het warmup plan zullen veranderen zoals per het onlangs geupload dossier. De volledige looppas en de geactiveerde looppas worden niet beïnvloed.

### Het bestand met het abonnement uploaden {#upload-plan}

Hieronder is een voorbeeld van een dossier dat een IP warmlopingsplan bevat.

![](assets/ip-warmup-sample-file.png)

Elke fase komt overeen met een periode die bestaat uit meerdere uitvoeringen, waaraan u één campagne toewijst.

Voor elke run hebt u een bepaald aantal ontvangers en u zult een datum definiëren waarop deze run wordt uitgevoerd.

U kunt zoveel kolommen hebben als u wilt voor de domeinen u aan wilt leveren. In dit voorbeeld hebt u drie kolommen: Gmail, Adobe en andere. Dit houdt in dat

Het idee is meer looppas in de eerste fasen te hebben en het aantal gerichte adressen geleidelijk te verhogen terwijl het verminderen van het aantal looppas.
