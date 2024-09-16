---
title: Configuratie van inhoudskaarten
description: Voorwaarden voor het kanaal van inhoudskaarten
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Beperkte beschikbaarheid" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 8a902298bbbac5689b4f84266dd9c9027e45fad5
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---

# Voorwaarden voor inhoudskaarten {#content-card-configuration-prereq}

>[!BEGINSHADEBOX]

**Lijst van inhoud**

* [Aan de slag met inhoudskaarten](get-started-content-card.md)
* **de kaartevoorwaarden van 0} Inhoud**
* [Het kanaal voor inhoudskaarten in Journey Optimizer configureren](content-card-configuration.md)
* [Inhoudskaarten maken](create-content-card.md)
* [Inhoudskaarten ontwerpen](design-content-card.md)
* [Rapport voor inhoudskaarten](content-card-report.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Inhoudskaarten zijn momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.

Adobe Journey Optimizer kan alleen inhoudskaarten correct weergeven als u de volgende Adobe Experience Platform-instellingen configureert:

* **de Inzameling van Gegevens van Adobe Experience Platform**

  [ creeer een datastream ](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) en [ voeg de dienst van het Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep) toe. Schakel de opties **[!UICONTROL Edge Segmentation]** en **[!UICONTROL Adobe Journey Optimizer]** in. Dit zorgt ervoor dat Journey Optimizer-gebeurtenissen worden afgehandeld door de Adobe Experience Platform-Edge Network. Zie de [ documentatie van gegevensstromen ](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) voor meer informatie over hoe te om een gegevensstroom te vormen.

* **Adobe Experience Platform**

  Verzeker het standaardsamenvoegbeleid **actief-op-Edge Beleid van de Fusie** toegelaten onder **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** menu van het Experience Platform heeft. [ leer meer ](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure) {target="_blank"}

  >[!NOTE]
  >
  >Wanneer u een aangepast **[!UICONTROL Dataset preference]** samenvoegbeleid gebruikt, moet u de **[!UICONTROL Journey Inbound]** -gegevensset toevoegen binnen het opgegeven samenvoegbeleid.

* **Adobe Experience Platform Mobile of het Web SDK van het Platform**

  Voor mobiele en Webtoepassingen, om wijzigingen aan uw Web-pagina&#39;s of mobiele apps toe te voegen, moet u of [ SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/overview) op uw website of [ Mobiele SDK van Adobe Experience Platform ](https://developer.adobe.com/client-sdks/home/) op uw mobiele apps uitvoeren.

* **Journey Optimizer**

  Creeer de kaartconfiguratie van de a [ Inhoud ](#content-card-configuration).

* **Problemen oplossen**

  Gebruik de **mening van 0} Edge Delivery {binnen** Verzekering van Adobe Experience Platform **om mobiele ervaringen problemen op te lossen.** Het kan verzoeken inspecteren, randvraag verifiëren, en profielgegevens onderzoeken. [Meer informatie](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery)

* **de Experimenten van de Inhoud**

  Verzeker de dataset die in uw app [ wordt gebruikt datastream ](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank) ook in uw inhoudexperiment meldend configuratie is. Toepassingsgegevens worden niet weergegeven in rapporten als de gegevenssets niet overeenkomen.

  Leer hoe te om datasets voor inhoudexperiment toe te voegen dat in [ meldt deze sectie ](../content-management/reporting-configuration.md).
