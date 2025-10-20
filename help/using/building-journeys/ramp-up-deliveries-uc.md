---
solution: Journey Optimizer
product: journey optimizer
title: Een overzicht van uw leveringen maken
description: Leer hoe u uw leveringen kunt opvoeren
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
hide: true
hidefromtoc: true
keywords: leverbaarheid, transport, gebruiksscenario, e-mail, reputatie
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 2%

---

# Gebruik hoofdletters/kleine letters: maak uw leveringen groter{#use-case-ramp-up-your-deliveries}

Als u onlangs naar een andere e-maildienstverlener, IP adres, of e-maildomein of subdomain bent verplaatst, moet u uw reputatie als afzender vestigen. Anders, zouden uw leveringen kunnen worden geblokkeerd of aan de spamomslag van de brievenbus van ontvangers worden verplaatst. Leer hoe te om uw e-mailreputatie met IP opwarmen in de [&#x200B; Gids van de Beste praktijken van de Levering te verhogen &#x200B;](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target="_blank"}.

Om uw IP op te warmen, kunt u geleidelijk het aantal van uw leveringen opvoeren. Lees meer over [&#x200B; optimaliserend leverbaarheid in Journey Optimizer &#x200B;](../reports/deliverability.md).

Het doel van deze gebruikszaak is een reis te maken om uw e-mailleveringen op te voeren. Om deze reis te vormen, volg deze stappen:

1. Maak een reis. [Meer informatie](journey-gs.md).

1. Voeg een **[!UICONTROL Condition]** activiteit aan de reis toe. [Meer informatie](condition-activity.md).

1. Stel in de activiteitsinstellingen van **[!UICONTROL Condition]** het maximumaantal ontvangers in voor uw levering:

   1. Stel in de activiteitsinstellingen van **[!UICONTROL Condition]** het veld **[!UICONTROL Type]** in op **[!UICONTROL Profile cap]** . [Meer informatie](condition-activity.md#profile_cap).

   1. Stel het veld **[!UICONTROL Limit]** in op het maximum aantal ontvangers voor deze levering.

   ![](assets/profile-cap-condition.png)

   U kunt deze limiet geleidelijk verhogen tot het totale aantal abonnees.

1. Voeg een handeling **[!UICONTROL Email]** toe aan het nominale pad na de handeling **[!UICONTROL Condition]** .

   ![](assets/ramp-up-deliveries-message.png)

   Wanneer de reis loopt, wordt het bericht verzonden de het ingaan profielen, tot het maximumaantal profielen dat u hebt gespecificeerd. Wanneer deze limiet is bereikt, nemen de ingevoerde profielen het alternatieve pad aan.

1. Voltooi de reis met de activiteiten van uw keuze.

Nadat uw IP omhoog heeft verwarmd, kunt u deze voorwaarde verwijderen.
