---
title: In-app kanaalvereisten en configuratie
description: Leer hoe u uw omgeving configureert voor het verzenden van In-app-berichten met Journey Optimizer
role: Admin
feature: In App
level: Intermediate
keywords: in-app, bericht, configuratie, platform
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 1%

---

# Vereisten en configuratie {#inapp-configuration}

## Configuratiestappen {#inapp-steps}

In-app-berichten verzenden tijdens uw reizen en campagnes met [!DNL Journey Optimizer], moet u door de volgende configuratiestappen gaan.

1. Zorg ervoor dat u de juiste machtigingen hebt voor Journey Optimizer-campagnes voordat u begint, zelfs als u alleen in-app-berichten tijdens reizen wilt gebruiken. Campagnemachtigingen zijn nog steeds vereist. [Meer informatie](../campaigns/get-started-with-campaigns.md#campaign-prerequisites).
Er moet een specifieke machtiging worden verleend om toegang te krijgen tot **Toepassingsoppervlakken** in Adobe Experience Platform Data Collection. Meer informatie in [deze video](#video).
1. Adobe Journey Optimizer inschakelen in de gegevensstroom van de Adobe Experience Platform-gegevensverzameling en uw standaardsamenvoegbeleid in Adobe Experience Platform controleren, zoals wordt beschreven in het dialoogvenster [Leveringsvoorwaarden](#delivery-prerequisites) hieronder.
1. Creeer en vorm een oppervlakte van de App in de Inzameling van Gegevens van Adobe Experience Platform, zoals die in wordt gedetailleerd [deze sectie](#channel-prerequisites).
1. Als u inhoud experimenteert, zorg ervoor om de vereisten te volgen die in [deze sectie](#experiment-prerequisite).

Als u klaar bent, kunt u uw eerste In-app-bericht maken, configureren en verzenden. Leer hoe u dit kunt bereiken in [deze sectie](create-in-app.md).

## Leveringsvoorwaarden {#delivery-prerequisites}

Voor de correcte levering van de berichten in de app moeten de volgende instellingen worden gedefinieerd:

* In de [Adobe Experience Platform-gegevensverzameling](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target="_blank"}moet u ervoor zorgen dat er een gegevensstroom is gedefinieerd, zoals onder de **[!UICONTROL Adobe Experience Platform]** de Adobe Experience Platform Edge en **[!UICONTROL Adobe Journey Optimizer]** optie ingeschakeld.

  Dit zorgt ervoor dat de inkomende Journey Optimizer-gebeurtenissen correct worden afgehandeld door de Adobe Experience Platform Edge. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/inapp_config_6.png)

* In [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"}, zorg ervoor u het standaardfusiebeleid met hebt **[!UICONTROL Active-On-Edge Merge Policy]** optie ingeschakeld. Selecteer hiertoe een beleid in het dialoogvenster **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Menu Experience Platform. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Dit samenvoegbeleid wordt gebruikt door [!DNL Journey Optimizer] binnenkomende kanalen om binnenkomende campagnes op de rand correct te activeren en te publiceren. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target="_blank"}

  >[!NOTE]
  >
  >Wanneer u een aangepaste **[!UICONTROL Dataset preference]** samenvoegbeleid, zorg ervoor dat u het **[!UICONTROL Journey Inbound]** dataset binnen het gespecificeerde samenvoegbeleid.

  ![](assets/inapp_config_8.png)

* Als u problemen wilt oplossen met de levering van mobiele Journey Optimizer-ervaringen, kunt u de opdracht **Edge Delivery** bekijken binnen **Adobe Experience Platform Assurance**. Deze plugin laat u toe om verzoekvraag in detail te inspecteren, te verifiëren of de verwachte randvraag zoals voorzien voorkomt, en profielgegevens, met inbegrip van identiteitskaarten, segmentlidmaatschap, en toestemmingsmontages te onderzoeken. Daarnaast kunt u de activiteiten bekijken waarvoor het verzoek is gekwalificeerd en vaststellen voor welke activiteiten het niet heeft uitgevoerd.

  Met de **Edge Delivery** Met insteekmodule krijgt u de inzichten die u nodig hebt om uw binnenkomende implementaties effectief te begrijpen en problemen op te lossen.

  [Meer informatie over de Edge Delivery-weergave](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery)

## Voorwaarden voor kanaalconfiguratie {#channel-prerequisites}

1. Toegang krijgen tot de **[!UICONTROL App surfaces]** menu en klik op **[!UICONTROL Create App surface]**.

1. Voeg een naam toe aan uw **[!UICONTROL App surface]**.

   ![](assets/inapp_config_2b.png)

1. Van de **[!UICONTROL Apple iOS]** , configureert u uw mobiele toepassing voor Apple iOS.

+++ Meer informatie

   1. Typ uw **[!UICONTROL iOS Bundle ID]**. Zie [Apple-documentatie](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) voor meer informatie over **Bundel-id**.

   1. (optioneel) Kies de optie **[!UICONTROL Sandbox]** waar u pushmeldingen wilt verzenden. Merk op dat het kiezen van een specifieke zandbak de noodzakelijke toegangstoestemmingen vereist.

      Raadpleeg voor meer informatie over sandboxbeheer [deze pagina](../administration/sandboxes.md#assign-sandboxes).

   1. De optie **[!UICONTROL Push credentials]** om het .p8-bestand met de aautoets indien nodig te slepen en neer te zetten.

      U kunt ook de opdracht **[!UICONTROL Manually enter push credentials]** om de APNs AUth-toets rechtstreeks te kopiëren en plakken.

   1. Voer uw **[!UICONTROL Key ID]** en **[!UICONTROL Team ID]**.

      ![](assets/inapp_config_2.png)

+++

1. Van de **[!UICONTROL Android]** , configureert u uw mobiele toepassing voor Android.

+++ Meer informatie

   1. Typ uw **[!UICONTROL Android package name]**. Zie [Android-documentatie](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) voor meer informatie over **Pakketnaam**.

   1. (optioneel) Kies de optie **[!UICONTROL Sandbox]** waar u pushmeldingen wilt verzenden. Merk op dat het kiezen van een specifieke zandbak de noodzakelijke toegangstoestemmingen vereist.

      Raadpleeg voor meer informatie over sandboxbeheer [deze pagina](../administration/sandboxes.md#assign-sandboxes).

   1. De optie **[!UICONTROL Push credentials]** optie om uw .json dossier van de privé sleutel te slepen en te laten vallen indien nodig.

      U kunt ook de opdracht **[!UICONTROL Manually enter push credentials]** om de persoonlijke sleutel van FCM rechtstreeks te kopiëren en te plakken.

      ![](assets/inapp_config_7.png)

1. Klikken **[!UICONTROL Save]** wanneer u de configuratie van uw voltooide **[!UICONTROL App surface]**.

   ![](assets/inapp_config_3.png)

   Uw **[!UICONTROL App surface]** is nu beschikbaar wanneer u een nieuwe campagne maakt met een bericht in de app. [Meer informatie](create-in-app.md)

1. Nadat u het oppervlak van uw app hebt gemaakt, moet u nu een mobiele eigenschap maken.

   Zie [deze pagina](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) voor de nadere regeling.

   ![](assets/inapp_config_4.png)

1. Installeer de volgende extensies in het menu Extensies van de nieuwe eigenschap:

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP-betrouwbaarheid
   * Toestemming
   * Identiteit
   * Mobiele kern
   * Profiel

   Zie [deze pagina](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) voor de nadere regeling.

   ![](assets/inapp_config_5.png)

Het kanaal in de app is nu geconfigureerd. U kunt in-app-berichten naar uw gebruikers verzenden.

## Voorwaarden voor het testen van inhoud {#experiment-prerequisites}

Als u inhoudsexperimenten wilt inschakelen voor In-app-kanalen, moet u ervoor zorgen dat de [gegevensset](../data/get-started-datasets.md) gebruikt in uw In-app-implementatie [datastream](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} is ook inbegrepen in uw rapporteringsconfiguratie.

Met andere woorden, wanneer het vormen experimenteert rapportering, als u een dataset toevoegt die niet in uw Webgegevensstroom aanwezig is, zullen de Webgegevens niet in de rapporten van het inhoudexperiment tonen.

Leer hoe u gegevenssets voor het experimenteren met inhoud toevoegt aan de rapportering in [deze sectie](../content-management/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>De dataset wordt gebruikt read-only door [!DNL Journey Optimizer] rapportagesysteem en heeft geen invloed op gegevensverzameling of gegevensinvoer.

Als u **niet** met behulp van de volgende vooraf gedefinieerde [veldgroepen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target="_blank"} voor uw datasetschema: `AEP Web SDK ExperienceEvent` en `Consumer Experience Event` (zoals gedefinieerd in [deze pagina](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), moet u de volgende veldgroepen toevoegen: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details`, en `Web Details`. Deze zijn nodig voor de [!DNL Journey Optimizer] de inhoud experimenteert rapportering terwijl zij volgen welke experimenten en behandelingen elk profiel aan deelnemen.

>[!NOTE]
>
>Het toevoegen van deze veldgroepen heeft geen invloed op de normale gegevensverzameling. Het is alleen additief voor de pagina&#39;s waarop een experiment wordt uitgevoerd, waarbij alle andere tracking ongewijzigd blijft.

## Hoe kan ik-video{#video}

In de onderstaande video ziet u hoe u de **Toepassingsconfiguratie beheren** machtiging om het menu met toepassingsoppervlakken te openen.

>[!VIDEO](https://video.tv.adobe.com/v/3421607)


**Verwante onderwerpen:**

* [Een bericht in de app maken](create-in-app.md)
* [Een campagne maken](../campaigns/create-campaign.md)
* [In-app-bericht ontwerpen](design-in-app.md)
* [Rapport in app](../reports/campaign-global-report.md#inapp-report)

