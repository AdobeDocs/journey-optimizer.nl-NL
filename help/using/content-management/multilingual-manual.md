---
solution: Journey Optimizer
product: journey optimizer
title: Meertalige inhoud maken met handmatige vertaling
description: Leer hoe u meertalige content maakt met handmatige vertaling in Journey Optimizer
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: aan de slag, starten, inhoud, experimenteren
exl-id: 6244d717-fbd6-468e-9164-60451d0d62f0
badge: label="Beperkte beschikbaarheid" type="Informative"
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 1%

---

# Meertalige inhoud maken met handmatige vertaling {#multilingual-manual}

>[!AVAILABILITY]
>
>Meertalige inhoud is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.

Met de handmatige stroom kunt u uw inhoud moeiteloos rechtstreeks vertalen in uw campagne en reis via e-mail, pushberichten of SMS, zodat u nauwkeurige controle- en aanpassingsopties hebt voor uw meertalige berichten. Bovendien kunt u met de optie HTML importeren eenvoudig bestaande meertalige inhoud importeren.

Ga als volgt te werk om meertalige inhoud te maken met handmatige vertaling:

1. [ creeer uw scène ](#create-locale).

1. [ creeer taalmontages ](#create-language-settings).

1. [ creeer een meertalige inhoud ](#create-a-multilingual-campaign).

## Landinstelling maken {#create-locale}

Wanneer het vormen van uw taalmontages, zoals die in [ worden beschreven creeer uw taalmontages ](#language-settings) sectie, als een specifieke scène niet beschikbaar voor uw meertalige inhoud is, hebt u de flexibiliteit om zo vele nieuwe scènes tot stand te brengen zoals vereist gebruikend het **[!UICONTROL Translation]** menu.

1. Open **[!UICONTROL Translation]** via het menu **[!UICONTROL Content management]** .

1. Klik op het tabblad **[!UICONTROL Locale dictionary]** op **[!UICONTROL Add locale]**.

   ![](assets/locale_1.png)

1. Selecteer uw landinstellingscode in de lijst **[!UICONTROL Language]** en de bijbehorende **[!UICONTROL Region]** .

1. Klik op **[!UICONTROL Save]** om uw landinstelling te maken.

   ![](assets/locale_2.png)

## Taalinstellingen maken {#language-settings}

In deze sectie kunt u de primaire taal en de bijbehorende landinstellingen instellen voor het beheer van meertalige inhoud. U kunt ook het kenmerk kiezen dat u wilt gebruiken om informatie met betrekking tot de profieltaal op te zoeken

1. Open **[!UICONTROL Channel]** > **[!UICONTROL General settings]** in het menu **[!UICONTROL Administration]** .

1. Klik in het menu **[!UICONTROL Language settings]** op **[!UICONTROL Create language settings]** .

   ![](assets/language_settings_1.png)

1. Typ de naam van de **[!UICONTROL Language settings]** .

1. Selecteer de **[!UICONTROL Locales]** die aan deze instellingen is gekoppeld. U kunt maximaal 50 landinstellingen toevoegen.

   Als een **[!UICONTROL Locale]** ontbreekt, kunt u het manueel van tevoren van het **[!UICONTROL Translation]** menu of door API tot stand brengen. Verwijs naar [ creeer een nieuwe Scène ](#create-locale).

   ![](assets/multilingual-settings-2.png)

1. Selecteer in het menu **[!UICONTROL Sending preference]** het kenmerk dat u wilt opzoeken naar informatie over profieltalen.

   ![](assets/multilingual-settings-3.png)

1. Klik op **[!UICONTROL Edit]** naast de **[!UICONTROL Locale]** om deze verder aan te passen en toe te voegen **[!UICONTROL Profile preferences]** .

   ![](assets/multilingual-settings-4.png)

1. Selecteer andere **[!UICONTROL Locales]** in de vervolgkeuzelijst Profielvoorkeuren en klik op **[!UICONTROL Add profiles]** .

1. Open het geavanceerde menu van uw **[!UICONTROL Locale]** om uw **[!UICONTROL Primary locale]** te bepalen, d.w.z. de standaardtaal als het profielattribuut niet wordt gespecificeerd.

   U kunt ook de landinstelling verwijderen uit dit geavanceerde menu.

   ![](assets/multilingual-settings-5.png)

1. Klik op **[!UICONTROL Submit]** om een **[!UICONTROL Language settings]** -bestand te maken.

<!--
1. Access the **[!UICONTROL channel configurations]** menu and create a new channel configuration or select an existing one.


1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Meertalige inhoud maken {#create-multilingual-campaign}

Nadat u meertalige inhoud hebt ingesteld, kunt u uw campagne of reis plannen en de inhoud voor elk van uw geselecteerde landinstellingen aanpassen.

1. Begin door uw E-mail, SMS of Push bericht [ campagne ](../campaigns/create-campaign.md) te creëren en te vormen of [ reis ](../building-journeys/journeys-message.md) volgens uw vereisten.

   >[!AVAILABILITY]
   >
   >We raden aan slechts één vertaalproject per reis op te nemen.

1. Maak of importeer de originele inhoud en pas deze indien nodig aan.

1. Wanneer uw primaire inhoud is gemaakt, klikt u op **[!UICONTROL Save]** en gaat u terug naar het scherm met de campagneconfiguratie.

   ![](assets/multilingual-campaign-2.png)

1. Klik op **[!UICONTROL Add languages]** en selecteer de eerder gemaakte **[!UICONTROL Language settings]** . [Meer informatie](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. Open de geavanceerde instellingen van het menu **[!UICONTROL Locales]** en selecteer **[!UICONTROL Copy primary to all locales]** .

   ![](assets/multilingual-campaign-4.png)

1. Nadat de primaire inhoud in de geselecteerde **[!UICONTROL Locales]** is gedupliceerd, opent u elke landinstelling en klikt u op **[!UICONTROL Edit email body]** om de inhoud te vertalen.

   ![](assets/multilingual-campaign-5.png)

1. U kunt ervoor kiezen om landinstellingen uit te schakelen of in te schakelen via het menu **[!UICONTROL More action]** van de geselecteerde landinstelling.

   ![](assets/multilingual-campaign-6.png)

1. Als u de meertalige configuratie wilt deactiveren, klikt u op **[!UICONTROL Add languages]** en selecteert u de taal die u als lokale taal wilt behouden.

   ![](assets/multilingual-campaign-7.png)

1. Klik op **[!UICONTROL Review to activate]** om een overzicht van de campagne weer te geven.

   In het overzicht kunt u uw campagne desgewenst wijzigen en controleren of een parameter onjuist is of ontbreekt.

1. Blader door uw meertalige inhoud om de rendering in elke taal te bekijken.

   ![](assets/multilingual-campaign-8.png)

U kunt nu uw campagne of reis activeren. Als u eenmaal bent verzonden, kunt u de impact van uw meertalige reis of campagne in rapporten meten.

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

-->
