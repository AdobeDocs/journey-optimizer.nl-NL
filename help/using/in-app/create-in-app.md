---
title: Een melding in de app maken
description: Leer hoe u een bericht in de app maakt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---


# Een bericht in de app maken {#create-in-app}

## Een campagne en een bericht in de app maken{#create-in-app-in-a-campaign}

Voer de onderstaande stappen uit om een bericht in de app te maken:

1. Toegang krijgen tot **[!UICONTROL Campaigns]** en klik vervolgens op **[!UICONTROL Create campaign]**.

1. In de **[!UICONTROL Properties]** , geeft u op wanneer u de campagne wilt uitvoeren.

1. In de **[!UICONTROL Actions]** in, kiest u de **[!UICONTROL In-app message]** en de **[!UICONTROL App surface]** eerder geconfigureerd voor uw bericht in de app. Klik vervolgens op **[!UICONTROL Create]**.

   [Meer informatie over configuratie in de app](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Van de **[!UICONTROL Properties]** sectie, uw campagne bewerken **[!UICONTROL Title]** en **[!UICONTROL Description]**.

1. Als u aangepaste of basislabels voor gegevensgebruik wilt toewijzen aan de landingspagina, selecteert u **[!UICONTROL Manage access]**. [Meer informatie](../administration/object-based-access.md).

1. Klik op de knop **[!UICONTROL Select audience]** om het publiek te bepalen om van de lijst van beschikbare segmenten van Adobe Experience Platform te richten. [Meer informatie](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

1. Kies de frequentie van de trigger wanneer het bericht in de app actief is:

   * **[!UICONTROL Show every time]**
   * **[!UICONTROL Show once]**
   * **[!UICONTROL Show until click through]**

1. Kies de gebeurtenis die het bericht activeert in het menu **[!UICONTROL Mobile app trigger]**
vervolgkeuzelijst.

   Als u een trigger kiest, kiest u welke actie van de gebruiker het bericht in de app weergeeft.

   ![](assets/in_app_create_3.png)

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe u de **[!UICONTROL Schedule]** van uw campagne in [deze sectie](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. U kunt nu beginnen met het ontwerpen van uw inhoud met de **[!UICONTROL Edit content]** knop.

   ![](assets/in_app_create_4.png)

## Uw In-app-berichten verzenden{#in-app-send}

### Voorvertonen op apparaat {#preview-device}

U kunt een voorvertoning van de melding in de app weergeven op een bepaald apparaat.

1. Klik op **[!UICONTROL Preview on device]**.

   ![](assets/in_app_create_6.png)

1. Van de **[!UICONTROL Connect to device]** venster, klikt u op **[!UICONTROL Start]**.

1. Typ in het dialoogvenster **[!UICONTROL Base URL]** van uw toepassing en klik op **[!UICONTROL Next]**.

   ![](assets/in_app_create_7.png)

1. Scan de QR-code met het apparaat en voer de weergegeven pincode in.

Het bericht in de app kan nu rechtstreeks op het apparaat worden geactiveerd, zodat u een voorbeeld van het bericht kunt bekijken en het op een echt apparaat kunt bekijken.

### Uw In-app-melding controleren en activeren{#in-app-review}

Nadat u het bericht in de app hebt gemaakt en de inhoud ervan hebt gedefinieerd en gepersonaliseerd, kunt u het bericht controleren en activeren.

Volg onderstaande stappen om dit te doen:

1. Gebruik de **[!UICONTROL Review to activate]** om een overzicht van uw bericht weer te geven.

   In het overzicht kunt u uw campagne desgewenst wijzigen en controleren of een parameter onjuist is of ontbreekt.

   ![](assets/in_app_create_5.png)

1. Controleer of uw campagne correct is geconfigureerd en klik vervolgens op **[!UICONTROL Activate]**.

Uw campagne is nu geactiveerd. Het bericht In-App dat in de campagne wordt gevormd wordt verzonden onmiddellijk, of op de gespecificeerde datum.

Zodra verzonden, kunt u het effect van uw in-app berichten binnen het rapport van de Campagne meten. Raadpleeg [deze sectie](inapp-report.md) voor meer informatie over rapporten.

**Verwante onderwerpen:**

* [In-app-bericht ontwerpen](design-in-app.md)
* [Rapport in app](inapp-report.md)
* [Configuratie in de app](inapp-configuration.md)
