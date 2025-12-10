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
source-git-commit: 05e300476ee77c7ac449f3cbb1ecb506e94c3da0
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 2%

---

# IP-warmtecampagnes maken {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Activeer de IP optie van het warmlopingsplan"
>abstract="Wanneer u deze optie selecteert, kan de campagne in een IP warmlopingsplan worden gebruikt. Het campagneschema zal dan door het IP warmup plan worden aangedreven het met wordt geassocieerd."

Alvorens het IP warmup plan zelf in [!DNL Journey Optimizer] tot stand te brengen, moet u eerst één of meerdere campagnes tot stand brengen specifiek voor gebruik in een IP warmup plan <!--through a dedicated option--> worden ontworpen.

Om een IP warmup campagne tot stand te brengen, volg de hieronder stappen.

1. Creeer een e-mailkanaal [&#x200B; configuratie &#x200B;](channel-surfaces.md) voor het domein en IPs dat u voor uw warmlopingsplan hebt geïdentificeerd.

   Werk samen met uw leverancier om het domein en IPs te identificeren dat moet worden gebruikt. Leer hoe te om hen in een e-mailconfiguratie in [&#x200B; te selecteren deze sectie &#x200B;](../email/email-settings.md#ip-pools).

   >[!CAUTION]
   >
   >Bewerk niet de configuratie van het e-mailkanaal nadat het IP warmup plan [&#x200B; &#x200B;](ip-warmup-execution.md) is begonnen.

1. Creeer een geplande marketing [&#x200B; campagne &#x200B;](../campaigns/create-campaign.md) en selecteer de [&#x200B; E-mail &#x200B;](../email/create-email.md#create-email) actie.

   <!--Select the Marketing category. The IP warmup plan activation option is only available for  marketing-type campaigns.-->

1. Selecteer de configuratie die u voor IP warmte-up creeerde.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same configuration as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Klik op **[!UICONTROL Create]**.

1. Selecteer in de sectie **[!UICONTROL Schedule]** de optie **[!UICONTROL IP warmup plan activation]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   Het campagne [&#x200B; programma &#x200B;](../campaigns/campaign-schedule.md) zal door het IP warmup plan worden gedreven het zal worden geassocieerd met, betekenend dat het programma niet meer in de campagne zelf wordt bepaald.

1. Voltooi de stappen om een e-mailcampagne tot stand te brengen, zoals het bepalen van de campagneeigenschappen, [&#x200B; publiek &#x200B;](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?-->, en [&#x200B; inhoud &#x200B;](../email/get-started-email-design.md#key-steps).

   >[!IMPORTANT]
   >
   >Het publiek dat in een IP warmup campagne wordt toegestaan moet [&#x200B; op segment-gebaseerd &#x200B;](../audience/creating-a-segment-definition.md) zijn en tot stand gebracht gebruikend het [&#x200B; standaardsamenvoegingsbeleid &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/overview#default-merge-policy){target="_blank"}.
   >
   >CSV uploadt publiek wordt niet gesteund voor IP warmup campagnes en zal in een fout bij campagneactivering resulteren.

   Voor meer informatie over hoe te om een campagne te vormen, verwijs naar [&#x200B; deze pagina &#x200B;](../campaigns/get-started-with-campaigns.md).

1. [&#x200B; activeer &#x200B;](../campaigns/review-activate-campaign.md) de campagne. De status verandert in **[!UICONTROL Live]** .

   >[!NOTE]
   >
   >[&#x200B; Bedrijfs regels &#x200B;](../conflict-prioritization/rule-sets.md#rule-sets) zouden niet op IP warmup plannen moeten worden gebruikt. De toepassing van deze regels kan het bereiken van het gewenste aantal doelprofielen voor campagnes belemmeren.

   Voor een levende campagne met IP geactiveerd warmup plan, is de **[!UICONTROL Delete]** knoop beschikbaar tot het met een IP warmup plan wordt geassocieerd. Als de campagne eenmaal in een abonnement is gebruikt, kan deze niet meer worden verwijderd.

1. De campagne wordt weergegeven in de lijst **[!UICONTROL Campaigns]** . Om alle IP warmup campagnes gemakkelijk terug te winnen die op de huidige zandbak worden gecreeerd, kunt u op de **[!UICONTROL IP warmup]** campagneoptie filtreren.

   ![](assets/ip-warmup-campaign-filter.png)

Zodra levend, is de campagne klaar voor gebruik in een IP warmup plan. [Meer informatie](ip-warmup-plan.md)

Een IP warmup campagne kan slechts in één IP warmup plan worden gebruikt. Nochtans, kan de zelfde campagne in één of meerdere fasen van het zelfde IP warmup plan worden gebruikt. [Meer informatie](ip-warmup-plan.md#ip-warmup-plan-tab)

>[!NOTE]
>
>Wanneer een levende campagne in een IP warmup plan wordt gebruikt, nadat het plan [&#x200B; zoals voltooid &#x200B;](ip-warmup-execution.md#mark-as-completed) duidelijk is, verandert het statuut van die campagne in **[!UICONTROL Stopped]**.

