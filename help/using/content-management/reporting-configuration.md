---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer-rapportage voor experimenten configureren
description: Meer informatie over het instellen van een rapportgegevensbron
feature: Experimentation, Reporting
topic: Administration
role: Admin
level: Intermediate
keywords: configuratie, experimenteren, rapporteren, optimaliseren
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 1%

---

# Rapportage voor experimenten configureren {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Gegevenssets instellen voor rapportage"
>abstract="De rapporteringsconfiguratie staat u toe om extra metriek terug te winnen die in uw campagnerapporten zal worden gebruikt. Het moet door een technische gebruiker worden uitgevoerd."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Een gegevensset selecteren"
>abstract="U kunt een gebeurtenis-type dataset slechts selecteren, die minstens één van de gesteunde gebiedsgroepen moet bevatten: de Details van de Toepassing, de Details van de Handel, de Details van het Web,."

De rapporterende gegevensbronconfiguratie staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw rapporten zal worden gebruikt.

<!--The reporting data source configuration allows you to retrieve additional metrics that will be used in the **[!UICONTROL Objectives]** tab of your campaign reports.-->

>[!NOTE]
>
>De rapportconfiguratie moet door een technische gebruiker worden uitgevoerd. <!--Rights?-->

Voor deze configuratie, moet u één of meerdere datasets toevoegen die de extra elementen bevatten die u voor uw rapporten wilt gebruiken. Volg de stappen om dit te doen [onder](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## Vereisten


Alvorens een dataset aan de rapporteringsconfiguratie toe te voegen, moet u die dataset tot stand brengen. Meer informatie in het dialoogvenster [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#create){target="_blank"}.

* U kunt alleen gebeurtenistypen toevoegen.

* Deze gegevensbestanden moeten de `Experience Event - Proposition Interactions` [veldgroep](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target="_blank"}.

* Deze gegevensreeksen kunnen ook een van de volgende elementen bevatten: [veldgroepen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target="_blank"}: `Application Details`, `Commerce Details`, `Web Details`.

  >[!NOTE]
  >
  >Andere veldgroepen kunnen ook worden opgenomen, maar momenteel worden alleen de bovenstaande veldgroepen ondersteund in Journey Optimizer-rapportage.

  Als u bijvoorbeeld wilt weten wat het effect is van een e-mailcampagne op handelsgegevens zoals aankopen of bestellingen, moet u een dataset van de ervaringsgebeurtenis maken met de `Commerce Details` veldgroep.

  Op dezelfde manier, als u over mobiele interactie wilt rapporteren, moet u een dataset van de ervaringsgebeurtenis met creëren `Application Details` veldgroep.

  <!--The metrics corresponding to each field group are listed [here](#objective-list).-->

* U kunt deze gebiedsgroepen aan één of verscheidene schema&#39;s toevoegen die in één of verscheidene datasets zullen worden gebruikt.

>[!NOTE]
>
>Meer informatie over XDM-schema&#39;s en veldgroepen in de [Documentatie over XDM System-overzicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}.

<!--
## Objectives corresponding to each field group {#objective-list}

The table below shows which metrics will be added to the **[!UICONTROL Objectives]** tab of your campaign reports for each field group.

| Field group | Objectives |
|--- |--- |
| Commerce Details | Price Total<br>Payment Amount<br>(Unique) Checkouts<br>(Unique) Product List Adds<br>(Unique) Product List Opens<br>(Unique) Product List Removal<br>(Unique) Product List Views<br>(Unique) Product Views<br>(Unique) Purchases<br>(Unique) Save For Laters<br>Product Price Total<br>Product Quantity |
| Application Details | (Unique) App Launches<br>First App Launches<br>(Unique) App Installs<br>(Unique) App Upgrades |
| Web Details | (Unique) Page Views |
-->

## Gegevenssets toevoegen {#add-datasets}

1. Van de **[!UICONTROL ADMINISTRATION]** menu, selecteert u **[!UICONTROL Configurations]**. In de  **[!UICONTROL Reporting]** sectie, klikken **[!UICONTROL Manage]**.

   ![](assets/reporting-config-menu.png)

   De lijst met gegevenssets die al zijn toegevoegd, wordt weergegeven.

1. Klik op het tabblad **[!UICONTROL Dataset]** op **[!UICONTROL Add dataset]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Als u **[!UICONTROL System dataset]** tab, slechts worden de datasets die door het systeem worden gecreeerd getoond. U kunt geen andere datasets toevoegen.

1. Van de **[!UICONTROL Dataset]** drop-down lijst, selecteer de dataset die u voor uw rapporten wilt gebruiken.

   >[!CAUTION]
   >
   >U kunt slechts een gebeurtenis-type dataset selecteren, die minstens één van gesteund moet bevatten [veldgroepen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target="_blank"}: **Toepassingsdetails**, **Commerce-gegevens**, **Webdetails**. Als u een dataset selecteert die die criteria niet aanpast, zult u uw veranderingen niet kunnen bewaren.

   ![](assets/reporting-config-datasets.png)

   Meer informatie over gegevenssets in het dialoogvenster [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target="_blank"}.

1. Van de **[!UICONTROL Profile ID]** drop-down lijst, selecteer de attributen van het gegevenssetgebied die zullen worden gebruikt om elk profiel in uw rapporten te identificeren.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Alleen beschikbare id&#39;s voor rapportage worden weergegeven.

1. De **[!UICONTROL Use Primary ID namespace]** is standaard ingeschakeld. Als de optie **[!UICONTROL Profile ID]** is **[!UICONTROL Identity Map]** kunt u deze optie uitschakelen en een andere naamruimte kiezen in de vervolgkeuzelijst die wordt weergegeven.

   ![](assets/reporting-config-namespace.png)

   Meer informatie over naamruimten in het dialoogvenster [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=nl){target="_blank"}.

1. Sparen uw veranderingen om de geselecteerde dataset aan de rapportconfiguratielijst toe te voegen.

   >[!CAUTION]
   >
   >Als u een dataset selecteerde die geen gebeurtenis-type is, zult u niet kunnen te werk gaan.

Voor webkanalen en in-app-kanalen moet u ervoor zorgen dat de [gegevensset](../data/get-started-datasets.md) gevormd voor gegevensinzameling wordt ook toegevoegd aan deze rapporteringsconfiguratie. Anders worden web- en In-app-gegevens niet weergegeven in de rapporten over het experimenteren met inhoud.

* Meer informatie over vereisten voor het experimenteren met inhoud voor webkanalen in [deze sectie](../web/web-prerequisites.md#experiment-prerequisites).

* Meer informatie over de kanaalconfiguratie in de app in [deze sectie](../in-app/inapp-configuration.md).

<!--
When building your campaign reports, you can now see the metrics corresponding to the field groups used in the datasets you added. Go to the **[!UICONTROL Objectives]** tab and select the metrics of your choice to better fine-tune your reports. [Learn more](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>If you add several datasets, all data from all datasets will be available for reporting.


## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
