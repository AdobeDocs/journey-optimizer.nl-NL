---
title: Configuratie van inhoudskaarten
description: Voorwaarden voor het kanaal van inhoudskaarten
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: 1f9841ddd039a7591f396e38d8a93ed840d6879e
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 2%

---

# Voorwaarden voor inhoudskaarten {#content-card-configuration-prereq}

Adobe Journey Optimizer kan alleen inhoudskaarten correct weergeven als u de volgende Adobe Experience Platform-instellingen configureert:

* **de Inzameling van Gegevens van Adobe Experience Platform**

  [&#x200B; creeer een datastream &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure){target="_blank"} en [&#x200B; voeg de dienst van Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep){target="_blank"} toe. Schakel de opties **[!UICONTROL Edge Segmentation]** en **[!UICONTROL Adobe Journey Optimizer]** in. Dit zorgt ervoor dat Journey Optimizer-gebeurtenissen worden afgehandeld door de Adobe Experience Platform Edge Network.
Voeg de **Gebeurtenis van de Ervaring toe - de 1&rbrace; gebiedsgroep van de Interactie van de Positie &lbrace;aan uw dataset om deze gegevens in uw rapporten te omvatten.** [&#x200B; leer meer over gegevensstromen &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure){target="_blank"}

* **Adobe Experience Platform**

  Verzeker het standaardsamenvoegbeleid **actief-op-Edge Beleid van de Fusie** toegelaten onder **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu heeft. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  >[!NOTE]
  >
  >Wanneer u een aangepast **[!UICONTROL Dataset preference]** samenvoegbeleid gebruikt, moet u de **[!UICONTROL Journey Inbound]** -gegevensset toevoegen binnen het opgegeven samenvoegbeleid.

* **Adobe Experience Platform Mobile of het Web SDK van het Platform**

  Voor mobiele en Webtoepassingen, om wijzigingen aan uw Web-pagina&#39;s of mobiele apps toe te voegen, moet u of het [&#x200B; Web SDK van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/overview){target="_blank"} op uw website of [&#x200B; Adobe Experience Platform Mobiele SDK &#x200B;](https://developer.adobe.com/client-sdks/home/){target="_blank"} op uw mobiele apps uitvoeren.

* **Journey Optimizer**

  Creeer de kaartconfiguratie van de a [&#x200B; Inhoud &#x200B;](#content-card-configuration).

* **Problemen oplossen**

  Gebruik de **mening van 0&rbrace; Edge Delivery &lbrace;binnen** Adobe Experience Platform Assurance **om mobiele ervaringen problemen op te lossen.** Het kan verzoeken inspecteren, randvraag verifiëren, en profielgegevens onderzoeken. [Meer informatie](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

* **de Experimenten van de Inhoud**

  Verzeker de dataset die in uw app [&#x200B; wordt gebruikt datastream &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank){target="_blank"} ook in uw inhoudexperiment meldend configuratie is. Toepassingsgegevens worden niet weergegeven in rapporten als de gegevenssets niet overeenkomen.

  Leer hoe te om datasets voor inhoudexperiment toe te voegen dat in [&#x200B; meldt deze sectie &#x200B;](../reports/reporting-configuration.md).

>[!CAUTION]
>
>Wanneer u pseudoniem-profielen (ongeautoriseerde bezoekers) aanwijst met uw inhoudskaarten, kunt u een Time-to-Live (TTL) instellen voor automatische profielverwijdering om uw aanspreekbare aantal profielen en de bijbehorende kosten te beheren. [Meer informatie](../start/guardrails.md#profile-management-inbound)