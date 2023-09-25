---
solution: Journey Optimizer
product: journey optimizer
title: IP-warmtecampagnes maken
description: Leer hoe te om een IP warmup campagne te creëren
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: IP, pools, leverbaarheid
hide: true
hidefromtoc: true
source-git-commit: b3e5a825b881736516b3bcd1d368843c3a601100
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 2%

---

# IP-warmtecampagnes maken {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Activeer de IP optie van het warmlopingsplan"
>abstract="Wanneer u deze optie selecteert, kan de campagne in een IP warmlopingsplan worden gebruikt. Het campagneschema zal dan door het IP warmup plan worden aangedreven het met wordt geassocieerd."

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Ga aan de slag met IP-opwarming](ip-warmup-gs.md)
* **[IP-warmtecampagnes maken](ip-warmup-campaign.md)**
* [Creeer een IP warmlopingsplan](ip-warmup-plan.md)
* [Voer het IP warmlopingsplan uit](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Alvorens het IP warmup plan zelf in te creëren [!DNL Journey Optimizer], moet u eerst één of meerdere campagnes met de specifieke toegelaten optie tot stand brengen zodat zij in een IP warmup plan kunnen worden gebruikt.

Om een IP warmup campagne tot stand te brengen, volg de hieronder stappen.

1. Een [email](../email/email-settings.md) kanaal [oppervlak](channel-surfaces.md) voor het domein en IPs die u voor uw warmlopingsplan hebt geïdentificeerd.

   >[!NOTE]
   >
   >Leer hoe te om het domein en IPs te selecteren in een e-mailoppervlak in [deze sectie](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >Het werk met uw leverbaarheidsadviseur om het domein en IPs te identificeren dat voor uw IP warmup plan moet worden gebruikt.<!--TBC-->

1. Een [campagne](../campaigns/create-campaign.md) en selecteert u de [E-mail](../email/create-email.md#create-email-journey-campaign) handeling.

1. Selecteer de oppervlakte die u voor IP warmte-up creeerde.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Klik op **[!UICONTROL Create]**.

1. Selecteer in de sectie **[!UICONTROL Schedule]** de optie **[!UICONTROL IP warmup plan activation]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   De campagne [schema](../campaigns/create-campaign.md#schedule) zal door het IP warmup plan worden gedreven het zal worden geassocieerd met, betekenend dat het programma niet meer in de campagne zelf wordt bepaald.

1. Voer de stappen uit om een e-mailcampagne te maken, zoals het definiëren van de campagne-eigenschappen. [publiek](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?-->, en [content](../email/get-started-email-design.md#key-steps).

   >[!NOTE]
   >
   >Voor meer informatie over hoe te om een campagne te vormen, raadpleeg [deze pagina](../campaigns/get-started-with-campaigns.md).

1. [Activeren](../campaigns/review-activate-campaign.md) de campagne.

   >[!NOTE]
   >
   >Voor een levende campagne met IP warmup plan geactiveerd, **[!UICONTROL Delete]** de knoop is beschikbaar tot het met een IP warmup plan wordt geassocieerd. Als de campagne eenmaal in een abonnement is gebruikt, kan deze niet meer worden verwijderd.

1. De campagne wordt weergegeven in het dialoogvenster **[!UICONTROL Campaigns]** lijst. Om alle IP warmup campagnes gemakkelijk terug te winnen die op de huidige zandbak worden gecreeerd, kunt u op **[!UICONTROL IP warmup]** campagneoptie.

   ![](assets/ip-warmup-campaign-filter.png)

Zodra levend, is de campagne klaar voor gebruik in een IP warmup plan. [Meer informatie](ip-warmup-plan.md)

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->

