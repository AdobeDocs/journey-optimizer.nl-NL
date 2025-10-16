---
solution: Journey Optimizer
product: journey optimizer
title: Een door API geactiveerde campagne plannen
description: Leer hoe u een door API geactiveerde campagne kunt plannen.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, API-geactiveerd, REST, optimizer, berichten
exl-id: e04b0d38-6b3d-4086-a0f0-c1b8f6d9634f
source-git-commit: 93698c93f3750b4d7feff18509f8144a7c79f156
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# De door de API geactiveerde campagne plannen {#api-schedule}

Gebruik het tabblad **[!UICONTROL Schedule]** om het campagneschema te definiëren.

## Begin- en einddatum instellen

Door gebrek, beginnen API teweeggebrachte campagnes zodra zij worden teweeggebracht, en eindigen zodra het bericht is verzonden eens. Als u de campagne niet direct wilt uitvoeren nadat deze is geactiveerd, kunt u met de optie **[!UICONTROL Campaign start]** een datum en tijd opgeven waarop het bericht moet worden verzonden.

Met de optie **[!UICONTROL Campaign end]** kunt u opgeven wanneer een campagne moet stoppen met uitvoeren. Buiten de opgegeven datums wordt de campagne niet uitgevoerd.

![](assets/api-triggered-schedule.png)

>[!NOTE]
>
>Wanneer u campagnes in [!DNL Adobe Journey Optimizer] plant, moet u ervoor zorgen dat de begindatum/tijd wordt uitgelijnd op de gewenste eerste levering.

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

Zodra uw campagneconfiguratie en inhoud klaar zijn, kunt u het herzien en activeren. [Meer informatie](../campaigns/review-activate-api-triggered-campaign.md)
