---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met meertalige inhoud
description: Meer informatie over meertalige inhoud in Journey Optimizer
feature: Multilingual
topic: Content Management
role: User
level: Beginner
keywords: aan de slag, starten, inhoud, experimenteren
hide: true
hidefromtoc: true
source-git-commit: 3b1acd7ada0637ce22e360e6e1bb35921dde2315
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 1%

---

# Meertalige inhoud maken {#multilingual-automated}

Met de meertalige functie kunt u moeiteloos inhoud in meerdere talen maken in één campagne. Met deze functie kunt u schakelen tussen talen tijdens het bewerken van uw campagne, het hele bewerkingsproces stroomlijnen en uw mogelijkheden verbeteren om meertalige inhoud efficiënt te beheren.

## Landinstelling maken {#create-locale}

Wanneer het vormen van uw taalmontages, zoals die in [Taalinstellingen maken](#language-settings) als een specifieke landinstelling niet beschikbaar is voor meertalige inhoud, hebt u de flexibiliteit om zoveel nieuwe landinstellingen te maken als nodig is met de **[!UICONTROL Translation]** -menu.

1. Van de **[!UICONTROL Administration]** menu, toegang **[!UICONTROL Channel]**.

   Via het menu voor vertalingen hebt u toegang tot de lijst met geactiveerde landinstellingen.

1. Klik op het tabblad **[!UICONTROL Locale dictionary]** op **[!UICONTROL Add locale]**.

   ![](assets/locale_1.png)

1. Selecteer uw landinstellingscode in het menu **[!UICONTROL Language]** en de bijbehorende **[!UICONTROL Region]**.

1. Klikken **[!UICONTROL Save]** om uw landinstelling te maken.

   ![](assets/locale_2.png)

## Vertaalproject maken {#translation-project}

1. Van de **[!UICONTROL Translation projects]** menu onder **[!UICONTROL Content management]**, klikt u op **[!UICONTROL Create project]**.

1. Type-in a **[!UICONTROL Name]** en **[!UICONTROL Description]**.

1. Selecteer **[!UICONTROL Source locale]**.

1. Kies of uw vertalingen na goedkeuring automatisch worden gepubliceerd en of u de revisieworkflow wilt inschakelen.

1. Klikken **[!UICONTROL Add locale]** om het menu te openen en de talen voor uw vertaalproject te definiëren.

   Indien een **[!UICONTROL Locale]** ontbreekt, kunt u het handmatig maken via de **[!UICONTROL Translation]** of door API. Zie [Een nieuwe landinstelling maken](#create-locale).

1. Selecteer in de lijst uw **[!UICONTROL Target locale(s)]** en kies welke **[!UICONTROL Translation provider]** wilt u gebruiken voor elke landinstelling.

1. Klikken **[!UICONTROL Add a locale]** wanneer u klaar bent met het koppelen van uw doellandinstelling aan de juiste vertaalprovider.

1. Klikken **[!UICONTROL Save]** wanneer uw vertaalproject wordt gevormd.

1. In het menu Geavanceerd van het vertaalproject kunt u kiezen of u het project wilt bewerken, deactiveren of verwijderen.

## Taalinstellingen maken {#language-settings}

In deze sectie kunt u de primaire taal en de bijbehorende landinstellingen instellen voor het beheer van meertalige inhoud. U kunt ook het kenmerk kiezen dat u wilt gebruiken om informatie met betrekking tot de profieltaal op te zoeken

1. Van de **[!UICONTROL Administration]** menu, toegang **[!UICONTROL Channel]**.

1. In de **[!UICONTROL Language settings]** menu, klikt u op **[!UICONTROL Create language settings]**.

1. Typ de naam van uw **[!UICONTROL Language settings]**.

1. Kies de optie **[!UICONTROL Translation project]**.

1. Van de **[!UICONTROL Translation project]** veld, klikken **[!UICONTROL Edit]** en kies uw eerder gemaakte **[!UICONTROL Translation project]**.

   Uw eerder geconfigureerde landinstellingen worden automatisch geïmporteerd. Als u uw **[!UICONTROL Translation project]**, klikt u op **[!UICONTROL Refresh]** om deze wijzigingen in uw **[!UICONTROL Language settings]**.

1. Van de **[!UICONTROL Sending preference]** selecteert u het kenmerk dat u wilt opzoeken om informatie over profieltalen te zoeken.

1. Klikken **[!UICONTROL Edit]** naast uw **[!UICONTROL Locale]** om het verder aan te passen en toe te voegen **[!UICONTROL Profile preferences]**.

1. Klikken **[!UICONTROL Submit]** om uw **[!UICONTROL Language settings]**.

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Een meertalige campagne maken {#create-multilingual-campaign}

1. Begin met het maken en configureren van uw campagne volgens uw vereisten. [Meer informatie](../campaigns/create-campaign.md)

1. Ga naar de **[!UICONTROL Actions]** en selecteert u **[!UICONTROL Edit content]**.

1. Maak of importeer de originele inhoud en pas deze indien nodig aan.

1. Wanneer de primaire inhoud is gemaakt, klikt u op **[!UICONTROL Save]** en ga terug naar het scherm van de campagneconfiguratie.

1. Klikken **[!UICONTROL Add languages]** en selecteer uw eerder gemaakte **[!UICONTROL Language settings]**. [Meer informatie](#create-language-settings)

1. Open de geavanceerde instellingen van de **[!UICONTROL Locales]** en selecteert u **[!UICONTROL Copy primary to all locales]**.

1. Nu de primaire inhoud wordt gedupliceerd door de geselecteerde inhoud  **[!UICONTROL Locales]**, elke landinstelling openen en klikken **[!UICONTROL Edit email body]** om uw inhoud te vertalen.

1. U kunt ervoor kiezen om landinstellingen uit te schakelen of in te schakelen met de **[!UICONTROL More action]** van uw geselecteerde landinstelling.

1. Als u de meertalige configuratie wilt deactiveren, klikt u op **[!UICONTROL Add languages]** en selecteer de taal die u als lokale taal wilt behouden.

1. Klikken **[!UICONTROL Review to activate]** om een overzicht van de campagne weer te geven.

   In het overzicht kunt u uw campagne desgewenst wijzigen en controleren of een parameter onjuist is of ontbreekt.

1. Blader door uw meertalige inhoud om de rendering in elke taal te bekijken.

1. Controleer of uw campagne correct is geconfigureerd en klik vervolgens op **[!UICONTROL Activate]**.

Uw campagne is nu geactiveerd. Het bericht dat in de campagne wordt gevormd wordt verzonden onmiddellijk, of op de gespecificeerde datum. Houd er rekening mee dat uw campagne niet kan worden gewijzigd zodra deze actief is. Als u inhoud opnieuw wilt gebruiken, kunt u uw campagne dupliceren.

Nadat u de campagne hebt verzonden, kunt u de impact van de campagnes meten in de campagnerapporten.

## Meertalig campagnerapport {#multilingual-campaign-report}

Algemene rapporten, toegankelijk via de **Alle tijd** weergegeven, gebeurtenissen die ten minste twee uur geleden hebben plaatsgevonden en gebeurtenissen gedurende een geselecteerde tijdsperiode bedekken. Het algemene rapport van de campagne kan direct van uw Campagne met worden betreden **[!UICONTROL View report]** knop.

Voor meer informatie over gegevens beschikbaar in het rapport Campagne, verwijs naar [deze pagina](../reports/campaign-global-report.md).

+++ Meer informatie over de verschillende meetgegevens en widgets die beschikbaar zijn voor uw meertalige inhoud.

![](assets/report_multilingual.png)

De **[!UICONTROL Email sending statistics by languages]** widget geeft aan hoe succesvol uw levering is, afhankelijk van uw **[!UICONTROL Locales]**:

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

De **[!UICONTROL Email tracking statistics by languages]** widget bevat de beschikbare gegevens voor de activiteit van de ontvanger voor uw levering afhankelijk van uw **[!UICONTROL Locales]**:

* **[!UICONTROL Unsubscribes]**: Het aantal klikken op de koppeling voor het opzeggen van abonnementen.

* **[!UICONTROL Opens]**: Het aantal keren dat het bericht is geopend.

* **[!UICONTROL Clicks]**: Het aantal keren dat er op de inhoud is geklikt.
+++


<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.


-->
