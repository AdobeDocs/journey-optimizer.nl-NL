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
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# De actiecampagne plannen {#action-campaign-schedule}

Gebruik het tabblad **[!UICONTROL Schedule]** om het campagneschema te definiëren.

Standaard worden actiecampagnes gestart als ze handmatig zijn geactiveerd en eindigen als het bericht eenmaal is verzonden. Als u de campagne niet meteen na activering wilt uitvoeren, kunt u met de optie **[!UICONTROL Campaign start]** een datum en tijd opgeven waarop het bericht moet worden verzonden.

Met de optie **[!UICONTROL Campaign end]** kunt u opgeven wanneer een campagne moet stoppen met uitvoeren. Buiten de opgegeven datums wordt de campagne niet uitgevoerd.

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>Wanneer u campagnes in [!DNL Adobe Journey Optimizer] plant, moet u ervoor zorgen dat de begindatum/tijd wordt uitgelijnd op de gewenste eerste levering. Voor terugkerende campagnes, als de aanvankelijke geplande tijd reeds is overgegaan, zullen de campagnes aan de volgende beschikbare tijdgroef volgens hun terugkeringsregels rollen.

Er zijn aanvullende planningsopties beschikbaar op basis van het campagnekanaal:

* **Frequentie** (E-mail, SMS, de Actie van de Duw)

  U kunt een frequentie bepalen waarmee het bericht van de campagne zou moeten worden verzonden. Hiervoor gebruikt u de **[!UICONTROL Action triggers]** -opties in het scherm voor het maken van campagnes om op te geven of de campagne dagelijks, wekelijks of maandelijks moet worden uitgevoerd.

* **IP de activering van het warmup plan** (E-mail)

  Voor e-mailcampagnes, kunt u specifieke IP campagnes van de opwarmingsplanactivering tot stand brengen. Het campagneschema zal door het IP warmup plan worden gedreven het zal worden geassocieerd met, betekenend dat het programma niet meer in de campagne zelf wordt bepaald. [ Leer hoe te om IP warmup campagnes ](../configuration/ip-warmup-campaign.md) tot stand te brengen.

## Volgende stappen {#next}

Zodra uw campagnemodel klaar is, kunt u de campagne beoordelen en activeren. [Meer informatie](review-activate-campaign.md)
