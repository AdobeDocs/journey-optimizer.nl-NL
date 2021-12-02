---
title: Profiel uiteinde
description: Profiel uiteinde
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
hide: true
hidefromtoc: true
source-git-commit: b5ce2ea81d4091b4fa9c09e83573f9043c5e55a8
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---


# Uw reputatie als afzender vaststellen

Als u onlangs naar een andere e-maildienstverlener, IP adres, of e-maildomein of subdomain bent verplaatst, moet u uw reputatie als afzender vestigen. Anders, zouden uw leveringen kunnen worden geblokkeerd of aan de spamomslag van de brievenbus van ontvangers worden verplaatst.

Om uw IP op te warmen, kunt u geleidelijk het aantal van uw leveringen opvoeren. Zie dit [use case](../building-journeys/ramp-up-deliveries-uc.md).

## Voorkeurstype voor hoofdletter van profiel {#profile_cap}

Andere voorwaardetypen worden gedetailleerd in dit [sectie](../building-journeys/condition-activity.md).

Gebruik dit voorwaardetype om een maximumaantal profielen voor een wegweg te plaatsen. Wanneer deze limiet is bereikt, hebben de invoerprofielen een ander pad.

U kunt dit voorwaardetype gebruiken om het volume van uw leveringen te verhogen. Zie dit [use case](../building-journeys/ramp-up-deliveries-uc.md).

De standaard-uiteinde is 1000. U kunt een geheel-getalwaarde van 1 tot 20.000 plaatsen.

De teller geldt alleen voor de geselecteerde reisversie. De teller wordt teruggesteld aan nul na één maand. Na het opnieuw instellen nemen de ingevoerde profielen het nominale pad opnieuw tot de tellerlimiet is bereikt.

Het nominale pad heeft altijd voorrang op het alternatieve pad, zelfs als u het alternatieve pad boven het nominale pad op het canvas verplaatst.

![](../assets/profile-cap-condition.png)

## Hoofdlettergebruik: opvoeren van uw leveringen

Als u onlangs naar een andere e-maildienstverlener, IP adres, of e-maildomein of subdomain bent verplaatst, moet u uw reputatie als afzender vestigen. Anders, zouden uw leveringen kunnen worden geblokkeerd of aan de spamomslag van de brievenbus van ontvangers worden verplaatst. Leer hoe u uw e-mailreputatie met IP-opwarming in de [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}.

Om uw IP op te warmen, kunt u geleidelijk het aantal van uw leveringen opvoeren. Meer informatie over [leverbaarheid optimaliseren in Journey Optimizer](../deliverability.md).

Het doel van deze gebruikszaak is een reis te maken om uw e-mailleveringen op te voeren. Om deze reis te vormen, volg deze stappen:

1. Een journey maken. [Meer informatie](../building-journeys/journey-gs.md).

1. Voeg een **[!UICONTROL Condition]** activiteit van de reis. [Meer informatie](../building-journeys/condition-activity.md).

1. In de **[!UICONTROL Condition]** de montages van de activiteit, plaatsen het maximumaantal ontvangers voor uw levering:

   1. In de **[!UICONTROL Condition]** activiteitinstellingen, stelt de **[!UICONTROL Type]** veld naar **[!UICONTROL Profile cap]**. [Meer informatie](profile-cap.md#profile_cap).

   1. Stel de **[!UICONTROL Limit]** tot het maximumaantal ontvangers voor deze levering.

   ![](../assets/profile-cap-condition.png)

   U kunt deze limiet geleidelijk verhogen tot het totale aantal abonnees.

1. Voeg een **[!UICONTROL Message]** activiteit aan de nominale weg na **[!UICONTROL Condition]** activiteit.

   ![](../assets/ramp-up-deliveries-message.png)

   Wanneer de reis loopt, wordt het bericht verzonden de het ingaan profielen, tot het maximumaantal profielen dat u hebt gespecificeerd. Wanneer deze limiet is bereikt, nemen de ingevoerde profielen het alternatieve pad aan.

1. Voltooi de reis met de activiteiten van uw keuze.

Nadat uw IP omhoog heeft verwarmd, kunt u deze voorwaarde verwijderen.

