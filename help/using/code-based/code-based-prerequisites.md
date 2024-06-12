---
title: Garanties en voorwaarden voor ervaring op basis van code
description: Volg de voorwaarden op deze pagina als u toepassingen en webpagina's wilt bewerken met de functie die is gebaseerd op Journey Optimizer-code
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: 07c453366280b21f5546322430a90752fd996099
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Guardrails en voorwaarden {#web-prerequisites}

Code-gebaseerde ervaringsacties kunnen gebruiken in [!DNL Journey Optimizer] en leveren van code inhoud lading die door uw toepassingen kan worden gebruikt, volg de hieronder eerste vereisten:

* Als u wijzigingen wilt toevoegen aan uw toepassingen, moet u een specifieke implementatie hebben. [Meer informatie](#implementation-prerequisites)

* Zorg ervoor dat u de Adobe Experience Platform-instellingen gedetailleerd definieert voor een correcte weergave van de op code gebaseerde ervaringen [hier](#delivery-prerequisites).

>[!CAUTION]
>
>* Het op code gebaseerde ervaringskanaal is niet beschikbaar voor organisaties die de Adobe hebben aangeschaft **Gezondheidsschild** en **Privacy- en beveiligingsschild** add-on aanbiedingen.
>
>* U kunt alleen op code gebaseerde ervaringen maken in **campagnes**. [Meer informatie](../campaigns/create-campaign.md#configure).

## Voorwaarden voor implementatie {#implementation-prerequisites}

De op code-gebaseerde ervaring steunt om het even welk type van klantenimplementatie zoals aangetoond in de opties hieronder. U kunt een client-side, server-side of een hybride implementatiemethode voor uw eigenschappen gebruiken:

* Alleen client - Als u wijzigingen wilt toevoegen aan uw webpagina&#39;s of mobiele apps, moet u ofwel de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"} op uw website of [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} op uw mobiele apps.

* Hybride modus - U kunt de opdracht [AEP Edge Network Server-API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} om voor verpersoonlijkingsserver-kant te verzoeken; de reactie wordt verstrekt aan het Web SDK van Adobe Experience Platform om de wijzigingen cliënt-kant terug te geven. Meer informatie in de Adobe Experience Platform [API-documentatie voor Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}. U kunt meer informatie vinden over de hybride modus en een aantal implementatiemonsters controleren in [dit blogbericht](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Server-kant - U kunt de [AEP Edge Network Server-API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} aan verzoek om verpersoonlijkingsserver-kant. Uw ontwikkelingsteam moet de reactie behandelen en de wijzigingen cliënt-kant in uw app implementatie teruggeven.

U kunt steekproeven voor elk van de implementatie hierboven methode vinden in [deze sectie](code-based-implementation-samples.md).

## Leveringsvoorwaarden {#delivery-prerequisites}

De op code gebaseerde ervaringen kunnen alleen correct worden geleverd als de volgende instellingen zijn gedefinieerd:

* In de [Adobe Experience Platform-gegevensverzameling](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target="_blank"}moet u ervoor zorgen dat er een gegevensstroom is gedefinieerd, zoals onder de **[!UICONTROL Adobe Experience Platform]** de dienst u hebt **[!UICONTROL Adobe Journey Optimizer]** optie ingeschakeld.

  Dit zorgt ervoor dat de inkomende Journey Optimizer-gebeurtenissen correct worden afgehandeld door de Adobe Experience Platform Edge. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* In [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"}, zorg ervoor dat u één samenvoegbeleid hebt met de **[!UICONTROL Active-On-Edge Merge Policy]** optie ingeschakeld. Selecteer hiertoe een beleid in het dialoogvenster **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Menu Experience Platform. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Dit samenvoegbeleid wordt gebruikt door [!DNL Journey Optimizer] binnenkomende kanalen om binnenkomende campagnes op de rand correct te activeren en te publiceren. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* Als u de levering van Journey Optimizer-webervaringen wilt oplossen, kunt u de opdracht **Edge Delivery** bekijken binnen **Adobe Experience Platform Assurance**. Deze plugin laat u toe om verzoekvraag in detail te inspecteren, te verifiëren of de verwachte randvraag zoals voorzien voorkomt, en profielgegevens, met inbegrip van identiteitskaarten, segmentlidmaatschap, en toestemmingsmontages te onderzoeken. Daarnaast kunt u de activiteiten bekijken waarvoor het verzoek is gekwalificeerd en vaststellen voor welke activiteiten het niet heeft uitgevoerd.

  Met de **Edge Delivery** Met insteekmodule krijgt u de inzichten die u nodig hebt om uw binnenkomende implementaties effectief te begrijpen en problemen op te lossen.

  [Meer informatie over de Edge Delivery-weergave](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery)

## Voorwaarden voor het testen van inhoud {#experiment-prerequisites}

Als u inhoudsexperimenten wilt inschakelen voor het op code gebaseerde kanaal, moet u ervoor zorgen dat de [gegevensset](../data/get-started-datasets.md) gebruikt in uw app-implementatie [datastream](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} is ook inbegrepen in uw rapporteringsconfiguratie.

Met andere woorden, als u experimentele rapportage configureert en u een gegevensset toevoegt die niet aanwezig is in uw toepassingsgegevensstroom, worden toepassingsgegevens niet weergegeven in de rapporten over het experimenteren met inhoud.

Leer hoe u gegevenssets voor het experimenteren met inhoud toevoegt aan de rapportering in [deze sectie](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>De dataset wordt gebruikt read-only door [!DNL Journey Optimizer] rapportagesysteem en heeft geen invloed op gegevensverzameling of gegevensinvoer.
