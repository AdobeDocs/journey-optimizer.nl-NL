---
solution: Journey Optimizer
product: journey optimizer
title: Gegevens verzenden naar AEP
description: Leer hoe u gegevens naar AEP kunt verzenden
feature: Journeys, Use Cases
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: reis, gebruiksgeval
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 2%

---

# Hoofdlettergebruik: een aangepaste handeling maken om gegevens naar Adobe Experience Platform te verzenden{#send-data-to-aep}

Als u onlangs naar een andere e-maildienstverlener, IP adres, of e-maildomein of subdomain bent verplaatst, moet u uw reputatie als afzender vestigen. Anders, zouden uw leveringen kunnen worden geblokkeerd of aan de spamomslag van de brievenbus van ontvangers worden verplaatst. Leer hoe u uw e-mailreputatie met IP-opwarming in de [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target="_blank"}.

Om uw IP op te warmen, kunt u geleidelijk het aantal van uw leveringen opvoeren. Meer informatie over [leverbaarheid optimaliseren in Journey Optimizer](../reports/deliverability.md).

Het doel van deze gebruikszaak is een reis te maken om uw e-mailleveringen op te voeren. Om deze reis te vormen, volg deze stappen:

1. Maak een reis. [Meer informatie](journey-gs.md).

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
