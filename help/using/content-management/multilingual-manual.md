---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met meertalige inhoud
description: Meer informatie over meertalige inhoud in Journey Optimizer
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: aan de slag, starten, inhoud, experimenteren
hide: true
hidefromtoc: true
exl-id: 6244d717-fbd6-468e-9164-60451d0d62f0
badge: label="Beta" type="Informative"
source-git-commit: feee761f9893633f88b0109b810ac55ae82dd9e0
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 1%

---

# Meertalige inhoud maken met handmatige vertaling {#multilingual-manual}

>[!BEGINSHADEBOX]

**Inhoudsopgave**

* [Aan de slag met meertalige inhoud](multilingual-gs.md)
* **[Meertalige inhoud maken met handmatige vertaling](multilingual-manual.md)**
* [Meertalige inhoud maken met automatische vertaling](multilingual-automated.md)
* [Meertalig campagnerapport](multilingual-report.md)

>[!ENDSHADEBOX]

Met de handmatige stroom kunt u uw inhoud moeiteloos rechtstreeks vertalen in uw campagne voor e-mail, pushmeldingen of SMS, zodat u nauwkeurige controle- en aanpassingsopties hebt voor uw meertalige berichten. Bovendien kunt u met de optie HTML importeren eenvoudig bestaande meertalige inhoud importeren.

Ga als volgt te werk om meertalige inhoud te maken met handmatige vertaling:

1. [Uw landinstelling maken](#create-locale).

1. [Taalinstellingen maken](#create-language-settings).

1. [Een meertalige campagne maken](#create-a-multilingual-campaign).

## Landinstelling maken {#create-locale}

Wanneer het vormen van uw taalmontages, zoals die in [Taalinstellingen maken](#language-settings) als een specifieke landinstelling niet beschikbaar is voor meertalige inhoud, hebt u de flexibiliteit om zoveel nieuwe landinstellingen te maken als nodig is met de **[!UICONTROL Translation]** -menu.

1. Van de **[!UICONTROL Administration]** menu, toegang **[!UICONTROL Channel]**.

   Via het menu voor vertalingen hebt u toegang tot de lijst met geactiveerde landinstellingen.

1. Klik op het tabblad **[!UICONTROL Locale dictionary]** op **[!UICONTROL Add locale]**.

   ![](assets/locale_1.png)

1. Selecteer uw landinstellingscode in het menu **[!UICONTROL Language]** en de bijbehorende **[!UICONTROL Region]**.

1. Klikken **[!UICONTROL Save]** om uw landinstelling te maken.

   ![](assets/locale_2.png)

## Taalinstellingen maken {#language-settings}

In deze sectie kunt u de primaire taal en de bijbehorende landinstellingen instellen voor het beheer van meertalige inhoud. U kunt ook het kenmerk kiezen dat u wilt gebruiken om informatie met betrekking tot de profieltaal op te zoeken

1. Van de **[!UICONTROL Administration]** menu, toegang **[!UICONTROL Channel]**.

1. In de **[!UICONTROL Language settings]** menu, klikt u op **[!UICONTROL Create language settings]**.

   ![](assets/multilingual-settings-1.png)

1. Typ de naam van uw **[!UICONTROL Language settings]**.

1. Selecteer de **[!UICONTROL Locales]** aan deze instellingen zijn gekoppeld. U kunt maximaal 50 landinstellingen toevoegen.

   Indien een **[!UICONTROL Locale]** ontbreekt, kunt u het handmatig maken via de **[!UICONTROL Translation]** of door API. Zie [Een nieuwe landinstelling maken](#create-locale).

   ![](assets/multilingual-settings-2.png)

1. Van de **[!UICONTROL Sending preference]** selecteert u het kenmerk dat u wilt opzoeken om informatie over profieltalen te zoeken.

   ![](assets/multilingual-settings-3.png)

1. Klikken **[!UICONTROL Edit]** naast uw **[!UICONTROL Locale]** om het verder aan te passen en toe te voegen **[!UICONTROL Profile preferences]**.

   ![](assets/multilingual-settings-4.png)

1. Andere selecteren **[!UICONTROL Locales]** van de voorkeurendrop-down van het Profiel en klik **[!UICONTROL Add profiles]**.

1. Open het geavanceerde menu van uw **[!UICONTROL Locale]** om uw **[!UICONTROL Primary locale]**, dat wil zeggen de standaardtaal als het profielkenmerk niet is opgegeven.

   U kunt ook de landinstelling verwijderen uit dit geavanceerde menu.

   ![](assets/multilingual-settings-5.png)

1. Klikken **[!UICONTROL Submit]** om uw **[!UICONTROL Language settings]**.

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Een meertalige campagne maken {#create-multilingual-campaign}

Nadat u meertalige inhoud hebt ingesteld, kunt u uw campagne plannen en de inhoud voor elk van uw geselecteerde landinstellingen aanpassen.

1. Begin met het maken en configureren van uw campagne voor e-mail-, sms- of pushmeldingen volgens uw vereisten. [Meer informatie](../campaigns/create-campaign.md)

1. Ga naar de **[!UICONTROL Actions]** en selecteert u **[!UICONTROL Edit content]**.

   ![](assets/multilingual-campaign-1.png)

1. Maak of importeer de originele inhoud en pas deze indien nodig aan.

1. Wanneer de primaire inhoud is gemaakt, klikt u op **[!UICONTROL Save]** en ga terug naar het scherm van de campagneconfiguratie.

   ![](assets/multilingual-campaign-2.png)

1. Klikken **[!UICONTROL Add languages]** en selecteer uw eerder gemaakte **[!UICONTROL Language settings]**. [Meer informatie](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. Open de geavanceerde instellingen van de **[!UICONTROL Locales]** en selecteert u **[!UICONTROL Copy primary to all locales]**.

   ![](assets/multilingual-campaign-4.png)

1. Nu de primaire inhoud wordt gedupliceerd door de geselecteerde inhoud  **[!UICONTROL Locales]**, elke landinstelling openen en klikken **[!UICONTROL Edit email body]** om uw inhoud te vertalen.

   ![](assets/multilingual-campaign-5.png)

1. U kunt ervoor kiezen om landinstellingen uit te schakelen of in te schakelen met de **[!UICONTROL More action]** van uw geselecteerde landinstelling.

   ![](assets/multilingual-campaign-6.png)

1. Als u de meertalige configuratie wilt deactiveren, klikt u op **[!UICONTROL Add languages]** en selecteer de taal die u als lokale taal wilt behouden.

   ![](assets/multilingual-campaign-7.png)

1. Klikken **[!UICONTROL Review to activate]** om een overzicht van de campagne weer te geven.

   In het overzicht kunt u uw campagne desgewenst wijzigen en controleren of een parameter onjuist is of ontbreekt.

1. Blader door uw meertalige inhoud om de rendering in elke taal te bekijken.

   ![](assets/multilingual-campaign-8.png)

1. Controleer of uw campagne correct is geconfigureerd en klik vervolgens op **[!UICONTROL Activate]**.

Uw campagne is nu geactiveerd. Het bericht dat in de campagne wordt gevormd wordt verzonden onmiddellijk, of op de gespecificeerde datum. Houd er rekening mee dat uw campagne niet kan worden gewijzigd zodra deze actief is. Als u inhoud opnieuw wilt gebruiken, kunt u uw campagne dupliceren.

Nadat u de campagne hebt verzonden, kunt u de impact van de campagnes meten in de campagnerapporten.

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

-->
