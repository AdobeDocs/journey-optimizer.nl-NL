---
title: Configuratie in de app
description: Leer hoe u uw omgeving configureert voor het verzenden van In-app-berichten met Journey Optimizer
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
keywords: in-app, bericht, configuratie, platform
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 3%

---

# In-app-kanaal configureren {#inapp-configuration}

Voordat u berichten in de app verzendt, moet u het kanaal in de app configureren [!DNL Adobe Experience Platform Data Collection].

1. Van uw [!DNL Adobe Experience Platform Data Collection] account, toegang krijgen tot **[!UICONTROL Datastream]** menu en klik op **[!UICONTROL New datastream]**. Raadpleeg voor meer informatie over het maken van gegevensstromen de [deze pagina](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. Selecteer [!DNL Adobe Experience Platform] service.

   [!DNL Edge Segmentation], [!DNL Offer Decisioning] en [!DNL Adobe Journey Optimizer] moet worden geselecteerd.

   ![](assets/inapp_config_6.png)

1. Ga vervolgens naar de **[!UICONTROL App surfaces]** en klik vervolgens op **[!UICONTROL Create App surface]**.

   ![](assets/inapp_config_1.png)

1. Voeg een naam toe aan uw **[!UICONTROL App surface]**.

1. Typ in de vervolgkeuzelijst Apple iOS uw **iOS-bundel-id**. Zie [Apple-documentatie](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) voor meer informatie over **Bundel-id**.

   ![](assets/inapp_config_2.png)

1. Typ in de vervolgkeuzelijst Android uw **Android-pakketnaam**. Zie [Android-documentatie](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) voor meer informatie over **Pakketnaam**.

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
   * Identificeren
   * Mobiele kern
   * Profiel

   Zie [deze pagina](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en#add-a-new-extension) voor de nadere regeling.

   ![](assets/inapp_config_5.png)

Het kanaal in de app is nu geconfigureerd. U kunt in-app-berichten naar uw gebruikers verzenden.

**Verwante onderwerpen:**

* [Een bericht in de app maken](create-in-app.md)
* [Een campagne maken](../campaigns/create-campaign.md)
* [In-app-bericht ontwerpen](design-in-app.md)
* [Rapport in app](inapp-report.md)
