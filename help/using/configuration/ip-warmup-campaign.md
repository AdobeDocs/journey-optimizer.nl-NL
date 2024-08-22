---
solution: Journey Optimizer
product: journey optimizer
title: IP-warmtecampagnes maken
description: Leer hoe te om een IP warmup campagne te creëren
feature: Campaigns, IP Warmup Plans
topic: Administration
role: Admin
level: Intermediate
keywords: IP, pools, leverbaarheid
exl-id: a9995ca1-d7eb-4f8d-a9d9-fe56198ac325
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 2%

---

# IP-warmtecampagnes maken {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Activeer de IP optie van het warmlopingsplan"
>abstract="Wanneer u deze optie selecteert, kan de campagne in een IP warmlopingsplan worden gebruikt. Het campagneschema zal dan door het IP warmup plan worden aangedreven het met wordt geassocieerd."

Alvorens het IP warmup plan zelf in [!DNL Journey Optimizer] tot stand te brengen, moet u eerst één of meerdere campagnes tot stand brengen specifiek voor gebruik in een IP warmup plan <!--through a dedicated option--> worden ontworpen.

Om een IP warmup campagne tot stand te brengen, volg de hieronder stappen.

1. Creeer een [ e-mail ](../email/email-settings.md) kanaal [ configuratie ](channel-surfaces.md) voor het domein en IPs die u voor uw warmlopingsplan hebt geïdentificeerd.

   >[!NOTE]
   >
   >Leer hoe te om het domein en IPs te selecteren in een e-mailconfiguratie in [ deze sectie ](../email/email-settings.md#subdomains-and-ip-pools) te gebruiken.
   >
   >* Het werk met uw leverbaarheidsconsultant om het domein en IPs te identificeren dat voor uw IP warmup plan moet worden gebruikt.<!--TBC-->

1. Creeer een geplande marketing [ campagne ](../campaigns/create-campaign.md) en selecteer de [ E-mail ](../email/create-email.md#create-email-journey-campaign) actie.

   <!--Select the Marketing category. The IP warmup plan activation option is only available for  marketing-type campaigns.-->

1. Selecteer de configuratie die u voor IP warmte-up creeerde.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same configuration as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Klik op **[!UICONTROL Create]**.

1. Selecteer in de sectie **[!UICONTROL Schedule]** de optie **[!UICONTROL IP warmup plan activation]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   Het campagne [ programma ](../campaigns/create-campaign.md#schedule) zal door het IP warmup plan worden gedreven het zal worden geassocieerd met, betekenend dat het programma niet meer in de campagne zelf wordt bepaald.

1. Voltooi de stappen om een e-mailcampagne tot stand te brengen, zoals het bepalen van de campagneeigenschappen, [ publiek ](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?-->, en [ inhoud ](../email/get-started-email-design.md#key-steps).

   Merk op dat u een op regel-gebaseerd publiek voor uw IP warmup campagne moet selecteren. [Meer informatie](../audience/creating-a-segment-definition.md)

   Voor meer informatie over hoe te om een campagne te vormen, verwijs naar [ deze pagina ](../campaigns/get-started-with-campaigns.md).

1. [ activeer ](../campaigns/review-activate-campaign.md) de campagne. De status verandert in **[!UICONTROL Live]** .

   Merk op dat de bedrijfsregels niet op IP warmup plan zouden moeten worden gebruikt. De toepassing van deze regels kan het bereiken van het gewenste aantal doelprofielen voor campagnes belemmeren.

   Voor een levende campagne met IP geactiveerd warmup plan, is de **[!UICONTROL Delete]** knoop beschikbaar tot het met een IP warmup plan wordt geassocieerd. Als de campagne eenmaal in een abonnement is gebruikt, kan deze niet meer worden verwijderd.

1. De campagne wordt weergegeven in de lijst **[!UICONTROL Campaigns]** . Om alle IP warmup campagnes gemakkelijk terug te winnen die op de huidige zandbak worden gecreeerd, kunt u op de **[!UICONTROL IP warmup]** campagneoptie filtreren.

   ![](assets/ip-warmup-campaign-filter.png)

Zodra levend, is de campagne klaar voor gebruik in een IP warmup plan. [Meer informatie](ip-warmup-plan.md)

Een IP warmup campagne kan slechts in één IP warmup plan worden gebruikt. Nochtans, kan de zelfde campagne in één of meerdere fasen van het zelfde IP warmup plan worden gebruikt. [Meer informatie](ip-warmup-plan.md#define-phases)

>[!NOTE]
>
>Wanneer een levende campagne in een IP warmup plan wordt gebruikt, nadat het plan [ zoals voltooid ](ip-warmup-execution.md#mark-as-completed) duidelijk is, verandert het statuut van die campagne in **[!UICONTROL Stopped]**.

