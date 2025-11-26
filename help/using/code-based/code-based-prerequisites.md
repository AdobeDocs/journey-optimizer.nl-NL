---
title: Voorwaarden voor op code gebaseerde ervaring
description: Volg de voorwaarden op deze pagina als u toepassingen en webpagina's wilt bewerken met de functie die is gebaseerd op Journey Optimizer-code
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: 3d5ed7c5efd76616c8dbc89078f7368eedc5f1af
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 1%

---

# Voorwaarden voor op code gebaseerde ervaring {#code-based-prerequisites}

Als u code-gebaseerde ervaringsacties in [!DNL Journey Optimizer] wilt kunnen gebruiken en code inhoud lading kunt leveren die door uw toepassingen kan worden gebruikt, volg hieronder de eerste vereisten:

* Als u wijzigingen wilt toevoegen aan uw toepassingen, moet u een specifieke implementatie hebben. [Meer informatie](#implementation-prerequisites)

* Voor de op code-gebaseerde ervaringen die correct moeten worden geleverd, zorg ervoor u de montages van Adobe Experience Platform bepaalt die [ hier ](#delivery-prerequisites) worden gedetailleerd.

* Om gegevens toe te laten om in uw code-gebaseerde ervaringsrapporten te tonen, zorg ervoor u deze [ het melden eerste vereisten ](#reporting-prerequisites) volgt.

* Wanneer het creëren van a [ code-Gebaseerde configuratie van het ervaringskanaal ](code-based-configuration.md), zorg ervoor u een koord/weg of een oppervlakte URI ingaat die in uw eigen implementatie wordt verklaard. Dit zorgt ervoor dat de inhoud wordt geleverd op de gewenste locatie binnen de opgegeven app of pagina. Anders kunnen de wijzigingen niet worden uitgevoerd. [Meer informatie](code-based-surface.md)

>[!NOTE]
>
>Wanneer u pseudoniem-profielen (ongeautoriseerde bezoekers) aanwijst met uw op code gebaseerde ervaringen, kunt u overwegen een Time-To-Live (TTL) in te stellen voor automatische profielverwijdering om uw aanspreekbare aantal en de bijbehorende kosten te beheren. [Meer informatie](#profile-management-guardrail)

## Voorwaarden voor implementatie {#implementation-prerequisites}

De op code-gebaseerde ervaring steunt om het even welk type van klantenimplementatie zoals aangetoond in de opties hieronder. U kunt een client-side, server-side of een hybride implementatiemethode voor uw eigenschappen gebruiken:

* Cliënt-kant slechts - om wijzigingen aan uw Web-pagina&#39;s of mobiele apps toe te voegen, moet u of het [ Web SDK van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"} op uw website of [ Adobe Experience Platform Mobile SDK ](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} op uw mobiele apps uitvoeren.

* Hybride wijze - u kunt de [ Server API van AEP Edge Network gebruiken API ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} om voor verpersoonlijkingsserver-kant te verzoeken; de reactie wordt verstrekt aan SDK van het Web van Adobe Experience Platform om de wijzigingen cliënt-kant terug te geven. Leer meer in de Adobe Experience Platform [ API documentatie van de Server van Edge Network ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}. U kunt meer over de hybride wijze te weten komen en sommige implementatiemonsters in [ controleren dit blogpost ](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Server-kant - u kunt de [ Server API van AEP Edge Network gebruiken API ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} om voor verpersoonlijkingsserver-kant te verzoeken. Uw ontwikkelingsteam moet de reactie behandelen en de wijzigingen cliënt-kant in uw app implementatie teruggeven.

U kunt steekproeven voor elk van de implementatiemethode hierboven in [ deze sectie ](code-based-implementation-samples.md) vinden.

## Leveringsvoorwaarden {#delivery-prerequisites}

De op code gebaseerde ervaringen kunnen alleen correct worden geleverd als de volgende instellingen zijn gedefinieerd:

* In de [ Gegevensverzameling van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target="_blank"}, zorg ervoor u een gegevensstroom hebt die zoals onder de **[!UICONTROL Adobe Experience Platform]** dienst wordt bepaald u de **[!UICONTROL Adobe Journey Optimizer]** toegelaten optie hebt.

  Dit zorgt ervoor dat de binnenkomende gebeurtenissen van Journey Optimizer correct worden afgehandeld door de Adobe Experience Platform Edge. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* In [ Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"}, zorg ervoor u één toegelaten fusiebeleid met de **[!UICONTROL Active-On-Edge Merge Policy]** optie hebt. Selecteer hiertoe een beleid in het menu **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Dit samenvoegbeleid wordt door [!DNL Journey Optimizer] binnenkomende kanalen gebruikt om binnenkomende campagnes op de rand correct te activeren en te publiceren. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* Om de levering van het Webervaringen van Journey Optimizer problemen op te lossen, kunt u de **Edge Delivery** mening binnen **Adobe Experience Platform Assurance** gebruiken. Deze plugin laat u toe om verzoekvraag in detail te inspecteren, te verifiëren of de verwachte randvraag zoals voorzien voorkomt, en profielgegevens, met inbegrip van identiteitskaarten, segmentlidmaatschap, en toestemmingsmontages te onderzoeken. Daarnaast kunt u de activiteiten bekijken waarvoor het verzoek is gekwalificeerd en vaststellen voor welke activiteiten het niet heeft uitgevoerd.

  Het gebruiken van de **insteekmodule van Edge Delivery** helpt u de inzichten verkrijgen nodig om uw binnenkomende implementaties effectief te begrijpen en problemen op te lossen.

  [ leer meer over de mening van Edge Delivery ](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

## Voorwaarden voor rapportage {#reporting-prerequisites}

Om rapportering voor het op code-gebaseerde kanaal toe te laten, moet u ervoor zorgen de [ dataset ](../data/get-started-datasets.md) in uw app implementatie [ wordt gebruikt datastream ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} is ook inbegrepen in uw rapporteringsconfiguratie die.

Met andere woorden, als u bij het configureren van rapporten een gegevensset toevoegt die niet aanwezig is in uw toepassingsgegevensstroom, worden toepassingsgegevens niet weergegeven in uw rapporten.

Leer hoe te om datasets voor het melden in [ toe te voegen deze sectie ](../reports/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>De dataset wordt gebruikt read-only door het [!DNL Journey Optimizer] rapporteringssysteem en beïnvloedt gegevensinzameling of gegevensopname niet.

## Handleiding voor profielbeheer {#profile-management-guardrail}

In [!DNL Journey Optimizer] kunnen op code gebaseerde ervaringen betrekking hebben op pseudoniem-profielen. Dit zijn profielen die nog niet zijn geverifieerd of bekend zijn omdat ze nog niet eerder op andere kanalen zijn gebruikt. Dit is bijvoorbeeld het geval wanneer u zich richt op alle bezoekers of doelgroepen op basis van tijdelijke id&#39;s zoals ECID.

Hierdoor neemt het totale aantal aanspreekbare profielen toe. Dit kan kosten met zich meebrengen als het contractueel aantal aangeschafte profielen wordt overschreden. De metriek van de vergunning voor elk pakket is vermeld op de [ pagina van de Beschrijving van het Product van Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. U kunt het aantal in dienst komende profielen in het [ dashboard van het vergunningsgebruik ](../audience/license-usage.md) controleren.

Adobe raadt u aan om een time-to-live (TTL) in te stellen om pseudoniem-profielen automatisch te verwijderen uit het realtime-klantprofiel als deze niet zijn gezien of gebruikt binnen een bepaald tijdvenster.

>[!NOTE]
>
>Leer hoe te om gegevensvervalsing voor pseudoniem profielen in de [ documentatie van Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"} te vormen.

Adobe raadt aan de TTL-waarde in te stellen op 14 dagen om deze aan te passen aan de huidige Edge-profielTTL.
