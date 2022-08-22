---
title: Rapportageconfiguratie
description: Meer informatie over het instellen van een rapportgegevensbron
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 11f7ce37dc1a99de4ed29fa7793f126e259f518d
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 3%

---

# Rapportageconfiguratie {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Gegevenssets instellen voor rapportage"
>abstract="De rapporteringsconfiguratie staat u toe om een verbinding aan een systeem te bepalen om extra douaneinformatie terug te winnen die in uw rapporten moet worden gebruikt. Het moet door een technische gebruiker worden uitgevoerd."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Een gegevensset selecteren"
>abstract="U kunt alleen een gebeurtenistype-gegevensset selecteren die ten minste een van de ondersteunde veldgroepen moet bevatten: ExperienceEvent-web, ExperienceEvent-application, ExperienceEvent-commerce."

De rapporterende gegevensbronconfiguratie staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw rapporten zal worden gebruikt.

>[!NOTE]
>
>De gegevensbronconfiguratie moet door een technische gebruiker worden uitgevoerd. <!--Rights?-->

Voor deze configuratie, moet u één of meerdere datasets toevoegen die de attributen bevatten die u voor uw rapporten wilt gebruiken. Volg de onderstaande stappen om dit te doen.

>[!CAUTION]
>
>Alvorens een dataset aan de rapporteringsconfiguratie toe te voegen, moet u het creëren. Meer informatie in het dialoogvenster [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}.
>
>U kunt gebeurtenis-type datasets slechts toevoegen, die minstens één van gesteunde moet bevatten [veldgroepen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **ExperienceEvent-web**, **ExperienceEvent-application**, **ExperienceEvent-commerce**.

<!--
➡️ [Discover this feature in video](#video)
-->

Als u bijvoorbeeld wilt weten wat het effect is van een e-mailcampagne op handelsgegevens zoals aankopen of bestellingen, moet u een dataset van de ervaringsgebeurtenis maken met de **ExperienceEvent-commerce** veldgroep. Op dezelfde manier, als u over mobiele interactie wilt rapporteren, moet u een dataset van de ervaringsgebeurtenis met creëren **ExperienceEvent-application** veldgroep. <!--If you want to report on web interactions then you need to include the web field group.--> U kunt deze gebiedsgroepen aan één of verscheidene schema&#39;s toevoegen die in één dataset of in verschillende datasets zullen worden gebruikt.

>[!NOTE]
>
>Meer informatie over XDM-schema&#39;s en veldgroepen in de [Documentatie over XDM System-overzicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target=&quot;_blank&quot;}.

1. Van de **[!UICONTROL ADMINISTRATION]** menu, selecteert u **[!UICONTROL Configurations]**. In de  **[!UICONTROL Reporting]** sectie, klikt u op **[!UICONTROL Manage]**.

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
   >U kunt slechts een gebeurtenis-type dataset selecteren, die minstens één van gesteund moet bevatten [veldgroepen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **ExperienceEvent-web**, **ExperienceEvent-application**, **ExperienceEvent-commerce**. Als u een dataset selecteert die die criteria niet aanpast, zult u uw veranderingen niet kunnen bewaren.

   ![](assets/reporting-config-datasets.png)

   Meer informatie over gegevenssets in het dialoogvenster [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}.

1. Van de **[!UICONTROL Profile ID]** drop-down lijst, selecteer de attributen van het gegevenssetgebied die zullen worden gebruikt om elk profiel in uw rapporten te identificeren.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Alleen beschikbare id&#39;s voor rapportage worden weergegeven.

1. De **[!UICONTROL Use Primary ID namespace]** is standaard ingeschakeld. Als de optie **[!UICONTROL Profile ID]** is **[!UICONTROL Identity Map]** kunt u deze optie uitschakelen en een andere naamruimte kiezen in de vervolgkeuzelijst die wordt weergegeven.

   ![](assets/reporting-config-namespace.png)

   Meer informatie over naamruimten in het dialoogvenster [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html){target=&quot;_blank&quot;}.

1. Sparen uw veranderingen om de geselecteerde dataset aan de rapportconfiguratielijst toe te voegen.

   >[!CAUTION]
   >
   >Als u een dataset selecteerde die geen gebeurtenis-type is, zult u niet kunnen te werk gaan.

Wanneer het bouwen van de rapporten van uw leveringen, kunt u gegevens van deze dataset nu gebruiken om extra douaneinformatie terug te winnen en beter uw rapporten te verfijnen. [Meer informatie](campaign-global-report.md#objectives-global)

>[!NOTE]
>
>Als u verscheidene datasets toevoegt, zullen alle gegevens van alle datasets voor rapportering beschikbaar zijn.


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
