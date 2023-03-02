---
solution: Journey Optimizer
product: journey optimizer
title: Werken met AEM sjablonen
description: Leer hoe u sjablonen maakt in AEM en exporteert naar Journey Optimizer
hide: true
hidefromtoc: true
feature: Overview
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informatief"
source-git-commit: a162f70dceb3bef635085840fc304e0da2c33eed
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 1%

---

# Werken met Adobe Experience Manager-sjablonen {#aem-templates}

>[!AVAILABILITY]
>
>Integratie met Adobe Experience Manager is momenteel alleen beschikbaar als bètaversie om gebruikers te selecteren.
> Als bètagebruiker kunt u [dit formulier](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} om feedback te delen.

Met Adobe Journey Optimizer kunt u op maat gemaakte berichten maken via Adobe Experience Manager-sites. Begin door uw sjablonen te ontwerpen met gebruik van Adobe Experience Manager-inhoudsbronnen en verzend deze vervolgens naar Adobe Journey Optimizer. Als deze sjablonen eenmaal zijn gedeeld, zijn ze toegankelijk in de Adobe Journey Optimizer e-mailontwerper, waardoor het maken en verzenden van berichten naar het gewenste publiek eenvoudiger wordt.

## Vereisten {#prerequisites}

Voordat u begint met het gebruik van deze functie, moet u zich aan de volgende vereisten houden:

* **Experience Manager-instellingen**

   Deze mogelijkheid is beschikbaar vanaf Adobe Experience Manager 6.5.14. U moet verbinding maken met Adobe Experience Manager Sites in uw Managed Services Author-omgeving.

   Als onderdeel van het bètaprogramma werd de configuratie van de Cloud Service uitgevoerd door Adobe in Adobe Experience Manager om verbinding te maken met Adobe Journey Optimizer.

* **Toestemmingen**

   Als u inhoudssjablonen wilt maken, bewerken en verwijderen in Adobe Journey Optimizer, moet u beschikken over de **[!DNL Manage Library Items]** bevoegdheid opgenomen in de **[!DNL Content Library Manager]** productprofiel. [Meer informatie](../administration/ootb-product-profiles.md#content-library-manager)


## Afvoerkanalen en beperkingen{#aem-templates-limitations}

Om het gebruik van Adobe Experience Manager met Adobe Journey Optimizer verder te optimaliseren, is het belangrijk dat u rekening houdt met de volgende aanvullende instructies en beperkingen:

* Het malplaatje van de Experience Manager moet geen verpersoonlijking bevatten. Personalisatie mag alleen in Journey Optimizer worden uitgevoerd.

* Bulksjabloonexport wordt momenteel niet ondersteund, sjablonen moeten afzonderlijk worden geëxporteerd.

* Synchronisatie tussen Experience Manager en Journey Optimizer is momenteel niet beschikbaar. Als er wijzigingen worden aangebracht in een Experience Manager-sjabloon nadat deze naar Journey Optimizer is verzonden, moet de gebruiker de sjabloon opnieuw exporteren en opnieuw naar Journey Optimizer verzenden.

## Een sjabloon naar Journey Optimizer verzenden{#aem-templates-send}

Voer de volgende stappen uit om een Adobe Experience Manager-sjabloon naar Adobe Journey Optimizer te exporteren:

1. Selecteer op je Adobe Experience Manager-homepage de optie **[!UICONTROL Outbound Marketing]**.

   ![](assets/aem-outbound-menu.png)

1. Open uw inhoudsbibliotheek en selecteer de sjabloon die u naar Journey Optimizer wilt exporteren.

   U kunt ook een geheel nieuwe pagina maken. [Meer informatie](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/managing-pages.html?lang=en#creating-a-new-page)

   ![](assets/aem-send-template.png)

1. Nadat u de sjabloon hebt geselecteerd, selecteert u **[!UICONTROL Send to]** in het geavanceerde menu.

   ![](assets/aem-advanced-menu.png)

1. Voer de **[!UICONTROL Name]** van de inhoudssjabloon en selecteer het doel **[!UICONTROL Sandbox]**.

   ![](assets/aem-send-template-settings.png)

1. Nadat u op de knop **[!UICONTROL Send]** -knop, wordt het exportproces gestart. Wanneer het exporteren is voltooid, wordt het volgende bericht weergegeven in de gebruikersinterface: &quot;Template &quot;XX&quot; is naar AJO verzonden.&quot;

De sjabloon wordt toegevoegd aan Adobe Journey Optimizer-inhoudssjablonen van de geselecteerde sandbox.

## Een Adobe Experience Manager-sjabloon gebruiken en aanpassen{#aem-templates-perso}

Zodra het malplaatje van de Experience Manager in Journey Optimizer als inhoudsmalplaatje beschikbaar is, kunt u de noodzakelijke inhoud voor e-mail identificeren en opnemen, met inbegrip van verpersoonlijking.

1. In Journey Optimizer, vanaf de **[!UICONTROL Content template]** toegang tot uw geïmporteerde sjabloon.

   ![](assets/aem_ajo_1.png)

1. Klik op de knop **[!UICONTROL Alert]** kunt u snel controleren of er belangrijke instellingen ontbreken. Dit zal helpen ervoor zorgen dat uw berichten behoorlijk worden gevormd en om het even welke potentiële fouten of kwesties verhinderen.

   ![](assets/aem_ajo_2.png)

1. In de **[!UICONTROL Template properties]** venster, klikt u op de knop **[!UICONTROL Manage access]** gebruiken om aangepaste of basislabels voor gegevensgebruik toe te wijzen aan uw sjabloon. [Leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC)](../administration/object-based-access.md)

1. Om uw AEM sjabloon verder aan te passen en aangepaste personalisatie aan uw inhoud toe te voegen, klikt u op **[!UICONTROL Edit content]**. Zo kunt u gemakkelijk wijzigingen aanbrengen en de sjabloon aan uw specifieke behoeften aanpassen. [Meer informatie](get-started-email-design.md)

   >[!NOTE]
   >
   > Als u de sjabloon wilt bewerken en aanpassen, kunt u alleen de compatibiliteitsmodus gebruiken.

1. Wanneer uw inhoudssjabloon gereed is, [testen en valideren](content-templates.md#test-template).

1. Nadat u de inhoud hebt gedefinieerd, kunt u deze gebruiken bij het maken van een nieuwe e-mail door in de **[!UICONTROL Saved templates]** verzameling. Selecteer vervolgens **[!UICONTROL Use this template]**.

   Leer hoe u e-mailinhoud kunt bewerken en aanpassen in [deze sectie](content-from-scratch.md).

   ![](assets/aem_ajo_3.png)

Wanneer uw e-mail klaar is, voltooi de configuratie van uw [reis](../building-journeys/journey-gs.md) of [campagne](../campaigns/create-campaign.md)en activeer deze om het bericht te verzenden.
