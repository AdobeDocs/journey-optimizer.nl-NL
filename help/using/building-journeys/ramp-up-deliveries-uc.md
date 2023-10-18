---
solution: Journey Optimizer
product: journey optimizer
title: Een overzicht van uw leveringen maken
description: Leer hoe u uw leveringen kunt opvoeren
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: leverbaarheid, transport, gebruiksscenario, e-mail, reputatie
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 3%

---

# Gebruik hoofdletters/kleine letters: maak uw leveringen groter{#use-case-ramp-up-your-deliveries}

Als u onlangs naar een andere e-maildienstverlener, IP adres, of e-maildomein of subdomain bent verplaatst, moet u uw reputatie als afzender vestigen. Anders, zouden uw leveringen kunnen worden geblokkeerd of aan de spamomslag van de brievenbus van ontvangers worden verplaatst. Leer hoe u uw e-mailreputatie met IP-opwarming in de [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target="_blank"}.

Om uw IP op te warmen, kunt u geleidelijk het aantal van uw leveringen opvoeren. Meer informatie over [leverbaarheid optimaliseren in Journey Optimizer](../reports/deliverability.md).

Het doel van deze gebruikszaak is een reis te maken om uw e-mailleveringen op te voeren. Om deze reis te vormen, volg deze stappen:

1. Een journey maken. [Meer informatie](journey-gs.md).

1. Voeg een **[!UICONTROL Condition]** activiteit van de reis. [Meer informatie](condition-activity.md).

1. In de **[!UICONTROL Condition]** de montages van de activiteit, plaatsen het maximumaantal ontvangers voor uw levering:

   1. In de **[!UICONTROL Condition]** activiteitinstellingen, stelt de **[!UICONTROL Type]** veld naar **[!UICONTROL Profile cap]**. [Meer informatie](condition-activity.md#profile_cap).

   1. Stel de **[!UICONTROL Limit]** tot het maximumaantal ontvangers voor deze levering.

   ![](assets/profile-cap-condition.png)

   U kunt deze limiet geleidelijk verhogen tot het totale aantal abonnees.

1. Een **[!UICONTROL Email]** actieactiviteit op het nominale pad na de **[!UICONTROL Condition]** activiteit.

   ![](assets/ramp-up-deliveries-message.png)

   Wanneer de reis loopt, wordt het bericht verzonden de het ingaan profielen, tot het maximumaantal profielen dat u hebt gespecificeerd. Wanneer deze limiet is bereikt, nemen de ingevoerde profielen het alternatieve pad aan.

1. Voltooi de reis met de activiteiten van uw keuze.

Nadat uw IP omhoog heeft verwarmd, kunt u deze voorwaarde verwijderen.
