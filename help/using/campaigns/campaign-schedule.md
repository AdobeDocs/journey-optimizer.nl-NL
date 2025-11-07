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
source-git-commit: bc779f732b865d5c178141f0b660d5c75f95a237
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# De actiecampagne plannen {#action-campaign-schedule}

Gebruik het tabblad **[!UICONTROL Schedule]** om het campagneschema te definiëren.

## Begindatum van campagne instellen

Standaard worden actiecampagnes gestart als ze handmatig zijn geactiveerd en eindigen als het bericht eenmaal is verzonden.

Als u uw campagne niet meteen na activering wilt uitvoeren, kunt u in de sectie **[!UICONTROL Campaign start]** een datum en tijd opgeven waarop het bericht moet worden verzonden.

![](assets/campaign-start.png)

>[!NOTE]
>
>Wanneer u campagnes in [!DNL Adobe Journey Optimizer] plant, moet u ervoor zorgen dat de begindatum/tijd wordt uitgelijnd op de gewenste eerste levering. Voor terugkerende campagnes, als de aanvankelijke geplande tijd reeds is overgegaan, zullen de campagnes aan de volgende beschikbare tijdgroef volgens hun terugkeringsregels rollen.

## Een uitvoeringsfrequentie instellen

Voor **E-mail**, **SMS**, en **Push bericht** acties, kunt u een frequentie bepalen waarbij het bericht van de campagne zou moeten worden verzonden. Hiervoor gebruikt u de **[!UICONTROL Action triggers]** -opties in het scherm voor het maken van campagnes om op te geven of de campagne dagelijks, wekelijks of maandelijks moet worden uitgevoerd.

![](assets/campaign-frequency.png)

>[!NOTE]
>
>Voor **e-mail** acties, kunt u specifieke IP campagnes van de opwarmingsPlan tot stand brengen. Het campagneschema zal door het IP warmup plan worden gedreven het zal worden geassocieerd met, betekenend dat het programma niet meer in de campagne zelf wordt bepaald. [&#x200B; Leer hoe te om IP warmup campagnes &#x200B;](../configuration/ip-warmup-campaign.md) tot stand te brengen.

## Einddatum instellen

In de sectie **[!UICONTROL Campaign end]** kunt u opgeven wanneer een campagne moet stoppen met uitvoeren. Buiten de opgegeven datums wordt de campagne niet uitgevoerd.

![](assets/campaign-end.png)

## Snelheidbeheersing instellen

Met [!DNL Journey Optimizer] kunt u tariefcontrole inschakelen voor uitgaande acties (e-mail, SMS, pushberichten).

Deze functie is vooral handig om overbelasting op downstreamsystemen, zoals pagina&#39;s voor landingen of platforms voor klantenservice, te voorkomen. Bijvoorbeeld, kunt u een tariefgrens van 165 berichten per seconde plaatsen om constante levering zonder overweldigende stroomafwaartse systemen te verzekeren.

Als u de snelheidsregeling wilt instellen, schakelt u de optie **[!UICONTROL Throttle delivery]** in de **[!UICONTROL Delivery settings]** -sectie in en geeft u de gewenste **[!UICONTROL Delivery rate]** per seconde op.

* Minimaal ondersteunde leveringspercentage: 1 per seconde.
* Maximale ondersteunde leversnelheid: 2000 per seconde wanneer de optie &quot;Throttle delivery&quot; is ingeschakeld.

![](assets/throttling-rate-control.png)

>[!IMPORTANT]
>
>Bij het instellen van een leveringstarief is de maximale tijdlijn waarvoor het campagnepubliek kan worden uitgevoerd 12 uur. Als de leveringstarief aan een waarde wordt geplaatst die niet alle publiek toestaat om het bericht in het 12 uurstijdsbestek te worden verzonden, dan zouden de resterende profielen van de campagne worden uitgesloten. U kunt de telling van deze uitgesloten profielen in het campagnerapport zien.

## Volgende stappen {#next}

Zodra uw campagnemodel klaar is, kunt u de campagne beoordelen en activeren. [Meer informatie](review-activate-campaign.md)
