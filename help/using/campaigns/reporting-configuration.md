---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer-rapportage voor experimenten configureren
description: Meer informatie over het instellen van een rapportgegevensbron
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 2%

---

# Rapportage voor experimenten configureren {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Gegevenssets instellen voor rapportage"
>abstract="De rapporteringsconfiguratie staat u toe om extra metriek terug te winnen die in het lusje van Doelstellingen van uw campagnerapporten zal worden gebruikt. Het moet door een technische gebruiker worden uitgevoerd."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Een gegevensset selecteren"
>abstract="U kunt alleen een gebeurtenistype-gegevensset selecteren, die minstens een van de ondersteunde veldgroepen moet bevatten: Application Details, Commerce Details, Web Details."

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

De rapportgegevensbronconfiguratie staat u toe om extra metriek terug te winnen die in zal worden gebruikt **[!UICONTROL Objectives]** van uw campagnerapporten. [Meer informatie](content-experiment.md#objectives-global)

>[!NOTE]
>
>De rapportconfiguratie moet door een technische gebruiker worden uitgevoerd. <!--Rights?-->

Voor deze configuratie, moet u één of meerdere datasets toevoegen die de extra elementen bevatten die u voor uw rapporten wilt gebruiken. Volg de stappen om dit te doen [onder](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## Vereisten


Alvorens een dataset aan de rapporteringsconfiguratie toe te voegen, moet u die dataset tot stand brengen. Meer informatie in het dialoogvenster [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}.

* U kunt alleen gegevenssets van het gebeurtenistype toevoegen.

* Deze gegevensbestanden moeten ten minste een van de volgende elementen bevatten [veldgroepen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **Toepassingsdetails**, **Handelsgegevens**, **Webdetails**.

   >[!NOTE]
   >
   >Momenteel worden alleen deze veldgroepen ondersteund.

   Als u bijvoorbeeld wilt weten wat het effect is van een e-mailcampagne op handelsgegevens zoals aankopen of bestellingen, moet u een dataset van de ervaringsgebeurtenis maken met de **Handelsgegevens** veldgroep.

   Op dezelfde manier, als u over mobiele interactie wilt rapporteren, moet u een dataset van de ervaringsgebeurtenis met creëren **Toepassingsdetails** veldgroep.

   De cijfers voor elke veldgroep worden weergegeven [hier](#objective-list).

* U kunt deze gebiedsgroepen aan één of verscheidene schema&#39;s toevoegen die in één of verscheidene datasets zullen worden gebruikt.

>[!NOTE]
>
>Meer informatie over XDM-schema&#39;s en veldgroepen in de [Documentatie over XDM System-overzicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target=&quot;_blank&quot;}.

## Doelstellingen voor elke veldgroep {#objective-list}

In de onderstaande tabel wordt aangegeven welke maatstaven worden toegevoegd aan de **[!UICONTROL Objectives]** tabblad van uw campagnerapporten voor elke veldgroep.

| Veldgroep | Doelstellingen |
|--- |--- |
| Handelsgegevens | Prijs totaal<br>Betalingsbedrag<br>(Uniek) Afhandelingen<br>(Unieke) Toegevoegde productlijst<br>(Uniek) Productlijst wordt geopend<br>(Unieke) productlijst verwijderen<br>(Unieke) productenlijstweergaven<br>(Unieke) productweergaven<br>(Unieke) aankopen<br>(Uniek) Opslaan voor later<br>Totaal productprijs<br>Aantal producten |
| Toepassingsdetails | (Uniek) App Launches<br>First App Launches<br>(Uniek) App-installaties<br>(Unieke) App-upgrades |
| Webdetails | (Unieke) paginaweergaven |

## Gegevenssets toevoegen {#add-datasets}

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
   >U kunt slechts een gebeurtenis-type dataset selecteren, die minstens één van gesteund moet bevatten [veldgroepen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **Toepassingsdetails**, **Handelsgegevens**, **Webdetails**. Als u een dataset selecteert die die criteria niet aanpast, zult u uw veranderingen niet kunnen bewaren.

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

Wanneer het bouwen van uw campagnerapporten, kunt u de metriek nu zien die aan de gebiedsgroepen beantwoordt die in de datasets worden gebruikt u toevoegde. Ga naar de **[!UICONTROL Objectives]** en selecteert u de gewenste maatstaven voor een betere afstemming van uw rapporten. [Meer informatie](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>Als u verscheidene datasets toevoegt, zullen alle gegevens van alle datasets voor rapportering beschikbaar zijn.

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
