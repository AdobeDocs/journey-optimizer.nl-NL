---
solution: Journey Optimizer
product: journey optimizer
title: De actiecampagne plannen
description: Leer hoe u de campagne Handelingen kunt plannen.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: maken, optimaliseren, campagne, oppervlak, berichten
exl-id: b183eeb8-606f-444d-9302-274f159c3847
source-git-commit: 4417643cbf206b9ad112bae5c270cdfc746a9c5d
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# De actiecampagne plannen {#action-campaign-schedule}

Gebruik het tabblad **[!UICONTROL Schedule]** om het campagneschema te definiëren.

## Begin- en einddatum instellen

Standaard worden actiecampagnes gestart als ze handmatig zijn geactiveerd en eindigen als het bericht eenmaal is verzonden. Als u de campagne niet meteen na activering wilt uitvoeren, kunt u met de optie **[!UICONTROL Campaign start]** een datum en tijd opgeven waarop het bericht moet worden verzonden.

Met de optie **[!UICONTROL Campaign end]** kunt u opgeven wanneer een campagne moet stoppen met uitvoeren. Buiten de opgegeven datums wordt de campagne niet uitgevoerd.

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>Wanneer u campagnes in [!DNL Adobe Journey Optimizer] plant, moet u ervoor zorgen dat de begindatum/tijd wordt uitgelijnd op de gewenste eerste levering. Voor terugkerende campagnes, als de aanvankelijke geplande tijd reeds is overgegaan, zullen de campagnes aan de volgende beschikbare tijdgroef volgens hun terugkeringsregels rollen.

## Snelheidbeheersing instellen

Met [!DNL Journey Optimizer] kunt u tariefcontrole inschakelen voor uitgaande acties (e-mail, SMS, pushberichten).

Deze functie is vooral handig om overbelasting op downstreamsystemen, zoals pagina&#39;s voor landingen of platforms voor klantenservice, te voorkomen. Bijvoorbeeld, kunt u een tariefgrens van 165 berichten per seconde plaatsen om constante levering zonder overweldigende stroomafwaartse systemen te verzekeren.

Als u de snelheidsregeling wilt instellen, schakelt u de optie **[!UICONTROL Throttle delivery]** in de **[!UICONTROL Delivery settings]** -sectie in en geeft u de gewenste **[!UICONTROL Delivery rate]** per seconde op.

![](assets/throttling-rate-control.png)

## Een uitvoeringsfrequentie instellen

Voor acties voor e-mail-, sms- en pushmeldingen kunt u een frequentie definiëren waarmee het campagnebericht moet worden verzonden. Hiervoor gebruikt u de **[!UICONTROL Action triggers]** -opties in het scherm voor het maken van campagnes om op te geven of de campagne dagelijks, wekelijks of maandelijks moet worden uitgevoerd.

![](assets/action-triggers.png)

## IP-opwarmingsplannen instellen

Voor e-mailacties kunt u specifieke campagnes voor activering van het IP-warmteopruimingsplan maken. Het campagneschema zal door het IP warmup plan worden gedreven het zal worden geassocieerd met, betekenend dat het programma niet meer in de campagne zelf wordt bepaald. [ Leer hoe te om IP warmup campagnes ](../configuration/ip-warmup-campaign.md) tot stand te brengen.

## Volgende stappen {#next}

Zodra uw campagnemodel klaar is, kunt u de campagne beoordelen en activeren. [Meer informatie](review-activate-campaign.md)
