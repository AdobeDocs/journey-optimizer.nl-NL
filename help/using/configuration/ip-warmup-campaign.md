---
solution: Journey Optimizer
product: journey optimizer
title: IP-warmtecampagnes maken
description: Leer hoe te om een IP warmup campagne te creëren
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, groep, subdomeinen, leverbaarheid
hide: true
hidefromtoc: true
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 2%

---

# IP-warmtecampagnes maken {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Activeer de IP optie van het warmlopingsplan"
>abstract="Selecteer de optie voor activering van het IP-opwarmingsplan. Zodra de campagne levend is, kan het met een IP warmlopingsplan worden geassocieerd."

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Ga aan de slag met IP-opwarming](ip-warmup-gs.md)
* **[IP-warmtecampagnes maken](ip-warmup-campaign.md)**
* [Creeer een IP warmlopingsplan](ip-warmup-plan.md)
* [Voer het IP-opwarmingsplan uit](ip-warmup-running.md)

>[!ENDSHADEBOX]

U moet één of meerdere campagnes met een specifieke toegelaten optie tot stand brengen zodat zij in een IP warmup plan kunnen worden gebruikt.

Om een IP warmup campagne tot stand te brengen, volg de hieronder stappen.

1. Een [oppervlak](channel-surfaces.md) voor het domein en IPs die u voor uw warmlopingsplan hebt geïdentificeerd.<!--how do you identify these or who does it at the customer level?-->

1. Een [campagne](../campaigns/create-campaign.md) en selecteert u de [E-mail](../email/create-email.md#create-email-journey-campaign) handeling.

1. Selecteer de oppervlakte die u voor IP warmte-up creeerde.

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Klik op **[!UICONTROL Create]**.

1. Selecteer in de sectie **[!UICONTROL Schedule]** de optie **[!UICONTROL IP warmup plan activation]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   De campagne [schema](../campaigns/create-campaign.md#schedule) zal door het IP warmup plan worden gedreven het zal worden geassocieerd met, betekenend dat het programma niet meer in de campagne zelf wordt bepaald.

1. [Activeren](../campaigns/review-activate-campaign.md) de campagne. Zodra levend, is het klaar voor gebruik in een IP warmup plan.

>[!NOTE]
>
>Voor een levende campagne met IP warmup plan geactiveerd, **[!UICONTROL Delete]** de knoop is beschikbaar tot het met een IP warmup plan wordt geassocieerd.

Voor meer informatie over hoe te om een campagne te vormen, raadpleeg [deze pagina](../campaigns/get-started-with-campaigns.md).

