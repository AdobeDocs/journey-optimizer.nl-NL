---
title: Een melding in de app maken
description: Leer hoe u een bericht in de app maakt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, bericht, maken, starten
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: e35aeba17f45145cc7712740cbcf1f0e169760fc
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 3%

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

1. Selecteer **[!UICONTROL Manage access]**. [Meer informatie](../administration/object-based-access.md).

1. Klik op de knop **[!UICONTROL Select audience]** om het publiek te bepalen om van de lijst van beschikbare segmenten van Adobe Experience Platform te richten. [Meer informatie](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

1. Klikken **[!UICONTROL Edit triggers]** om de gebeurtenis(sen) en criteria te kiezen die uw bericht activeren:

   1. Klikken **[!UICONTROL Add]voorwaarde** als u wilt dat de trigger rekening houdt met meerdere gebeurtenissen of criteria.
   1. Selecteer hoe uw gebeurtenissen worden gekoppeld. Kies bijvoorbeeld **[!UICONTROL And]** als u **beide** triggers moeten waar zijn om een bericht weer te geven of **[!UICONTROL Or]** als u wilt dat het bericht wordt getoond als **ofwel** van de triggers zijn waar.
   1. Klikken **[!UICONTROL Make group]** om triggers samen te groeperen.

   ![](assets/in_app_create_3.png)

1. Kies de frequentie van de trigger wanneer het bericht in de app actief is:

   * **[!UICONTROL Everytime]**: Toon altijd het bericht wanneer de gebeurtenissen die in **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Once]**: Alleen dit bericht weergeven als de gebeurtenissen die voor de eerste keer zijn geselecteerd in het dialoogvenster **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Until click through]**: Dit bericht weergeven wanneer de gebeurtenissen zijn geselecteerd in het dialoogvenster **[!UICONTROL Mobile app trigger]** drop-down komt voor tot een interactie gebeurtenis door SDK met een actie van &quot;geklikt&quot;wordt verzonden.
   * **[!UICONTROL X number of times]**: Dit bericht X-tijd tonen.

1. Kies zo nodig welke **[!UICONTROL Day of the week]** of **[!UICONTROL Time of day]** Het bericht in de app wordt weergegeven.

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

Zodra verzonden, kunt u het effect van uw in-app berichten binnen de Campagne of de rapporten van de Reis meten. Raadpleeg [deze sectie](../reports/campaign-global-report.md#inapp-report) voor meer informatie over rapporten.

**Verwante onderwerpen:**

* [In-app-bericht ontwerpen](design-in-app.md)
* [Rapport in app](../reports/campaign-global-report.md#inapp-report)
* [Configuratie in de app](inapp-configuration.md)

## Hoe kan ik-video{#video}

In de onderstaande video ziet u hoe u in-app-berichten kunt maken, configureren en publiceren in uw campagnes.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)
