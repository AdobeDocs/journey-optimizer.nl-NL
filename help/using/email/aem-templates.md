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
badge: label="Beta" type="Informative"
exl-id: e4935129-c1cb-41b1-b84d-cd419053c303
source-git-commit: dd463d36550b53faaffca90691550278498c862a
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 1%

---

# Werken met Adobe Experience Manager-sjablonen {#aem-templates}

>[!AVAILABILITY]
>
>Integratie met Adobe Experience Manager is momenteel alleen beschikbaar als een bètaversie om gebruikers te selecteren.
> Als bètagebruiker kunt u [dit formulier](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} om feedback te delen.

Met Adobe Journey Optimizer kunt u op maat gemaakte berichten maken via Adobe Experience Manager-sites. Begin door uw sjablonen te ontwerpen met gebruik van Adobe Experience Manager-inhoudsbronnen en verzend deze vervolgens naar Adobe Journey Optimizer. Als deze sjablonen eenmaal zijn gedeeld, zijn ze toegankelijk in de Adobe Journey Optimizer e-mailontwerper, waardoor het maken en verzenden van berichten naar het gewenste publiek eenvoudiger wordt.

## Vereisten {#prerequisites}

Voordat u begint met het gebruik van deze functie, moet u zich aan de volgende vereisten houden:

* **Experience Manager-instellingen**

  Deze mogelijkheid is beschikbaar bij [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/overview/introduction.html){target="_blank"}.

  Als deel van het bètaprogramma, wordt de configuratie van de Cloud Service uitgevoerd door Adobe in Adobe Experience Manager om met Adobe Journey Optimizer te verbinden.

* **Toestemmingen**

  Als u inhoudssjablonen wilt maken, bewerken en verwijderen in Adobe Journey Optimizer, moet u beschikken over de **[!DNL Manage Library Items]** bevoegdheid opgenomen in de **[!DNL Content Library Manager]** productprofiel. [Meer informatie](../administration/ootb-product-profiles.md#content-library-manager)

## Afvoerkanalen en beperkingen{#aem-templates-limitations}

Om het gebruik van Adobe Experience Manager met Adobe Journey Optimizer verder te optimaliseren, is het belangrijk dat u rekening houdt met de volgende aanvullende instructies en beperkingen:

* De correcte syntaxis van Journey Optimizer wordt vereist voor verpersoonlijking in het malplaatje van de Experience Manager om efficiënt te zijn. [Meer informatie](../personalization/personalization-syntax.md)

* Bulksjabloonexport wordt momenteel niet ondersteund, sjablonen moeten afzonderlijk worden geëxporteerd.

* Synchronisatie tussen Experience Manager en Journey Optimizer is momenteel niet beschikbaar. Als er wijzigingen worden aangebracht in een Experience Manager-sjabloon nadat deze naar Journey Optimizer is verzonden, moet de gebruiker de sjabloon opnieuw exporteren en opnieuw naar Journey Optimizer verzenden.

## Een sjabloon naar Journey Optimizer verzenden{#aem-templates-send}

Voer de volgende stappen uit om een Adobe Experience Manager-sjabloon naar Adobe Journey Optimizer te exporteren:

1. Selecteer op uw Adobe Experience Manager-homepage de optie **[!UICONTROL Outbound Marketing]**.

   ![](assets/aem-outbound-menu.png)

1. Vanuit uw inhoudsbibliotheek kunt u eerder geconfigureerde sjablonen gebruiken of een geheel nieuwe sjabloon maken. [Meer informatie](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/managing-pages.html#creating-a-new-page)

1. Door Journey Optimizer-verpersoonlijkingssyntaxis in uw sjabloon op te nemen, kunt u de aanpassingsmogelijkheden van de toepassing verbeteren. [Meer informatie](../personalization/personalization-syntax.md)

   ![](assets/aem_ajo_4.png)

1. Selecteer de sjabloon die u naar Journey Optimizer wilt exporteren en klik op **[!UICONTROL Send to]** in het geavanceerde menu.

   ![](assets/aem-advanced-menu.png)

1. Voer de **[!UICONTROL Name]** van de inhoudssjabloon en selecteer het doel **[!UICONTROL Sandbox]**.

   ![](assets/aem-send-template-settings.png)

1. Nadat u op de knop **[!UICONTROL Send]** -knop, wordt het exportproces gestart. Wanneer het exporteren is voltooid, wordt in de gebruikersinterface het volgende bericht weergegeven: &quot;Sjabloon &quot;XX&quot; is naar AJO verzonden.&quot;

De sjabloon wordt toegevoegd aan Adobe Journey Optimizer-inhoudssjablonen van de geselecteerde sandbox.

## Een Adobe Experience Manager-sjabloon gebruiken en aanpassen{#aem-templates-perso}

Zodra het malplaatje van de Experience Manager in Journey Optimizer als inhoudsmalplaatje beschikbaar is, kunt u de noodzakelijke inhoud voor e-mail identificeren en opnemen, met inbegrip van verpersoonlijking.

1. In Journey Optimizer, vanaf de **[!UICONTROL Content template]** toegang tot uw geïmporteerde sjabloon.

   ![](assets/aem_ajo_1.png)

1. Klik op de knop **[!UICONTROL Alert]** kunt u snel controleren of er belangrijke instellingen ontbreken. Dit zal helpen ervoor zorgen dat uw berichten behoorlijk worden gevormd en om het even welke potentiële fouten of kwesties verhinderen.

   ![](assets/aem_ajo_2.png)

1. In de **[!UICONTROL Template properties]** venster, klikt u op **[!UICONTROL Manage access]** gebruiken om aangepaste of basislabels voor gegevensgebruik toe te wijzen aan uw sjabloon. [Leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC)](../administration/object-based-access.md)

1. Om uw malplaatje van de Experience Manager verder aan te passen en douaneprijdbaarheid aan uw inhoud toe te voegen, klik **[!UICONTROL Edit content]**. Zo kunt u gemakkelijk wijzigingen aanbrengen en de sjabloon aan uw specifieke behoeften aanpassen. [Meer informatie](get-started-email-design.md)

   >[!WARNING]
   >
   > Als u de sjabloon wilt bewerken en aanpassen, kunt u alleen de compatibiliteitsmodus gebruiken.

1. Wanneer uw inhoudssjabloon gereed is, [testen en valideren](../content-management/content-templates.md#test-template).

1. Nadat u de inhoud hebt gedefinieerd, kunt u deze gebruiken bij het maken van een nieuwe e-mail door in de **[!UICONTROL Saved templates]** verzameling. Selecteer vervolgens **[!UICONTROL Use this template]**.

   ![](assets/aem_ajo_3.png)

1. U kunt de inhoud nu bewerken en aanpassen. Raadpleeg deze voor meer informatie over het samenstellen van uw e-mailinhoud [page](content-from-scratch.md).

   ![](assets/aem_ajo_5.png)

1. Als u gepersonaliseerde inhoud aan uw malplaatje van de Experience Manager hebt toegevoegd, klik **[!UICONTROL Simulate Content]** aan voorproef hoe het in het bericht zal verschijnen gebruikend testprofielen.

[Meer informatie over voorvertoningen en testprofielen](../email/preview.md)

   ![](assets/aem_ajo_6.png)

1. Wanneer u de voorvertoning van het bericht weergeeft, worden alle gepersonaliseerde elementen automatisch vervangen door de bijbehorende gegevens uit het geselecteerde testprofiel.

   Indien nodig kunnen aanvullende testprofielen via de **[!UICONTROL Manage test profiles]** knop.

   ![](assets/aem_ajo_7.png)

Wanneer uw e-mail klaar is, voltooi de configuratie van uw [reis](../building-journeys/journey-gs.md) of [campagne](../campaigns/create-campaign.md)en activeer deze om het bericht te verzenden.
