---
title: Een Web In-app-bericht maken in Journey Optimizer
description: Leer hoe u een Web In-app-bericht maakt in Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: in-app, bericht, maken, starten
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 1%

---


# Het webkanaal in de app configureren {#configure-in-app-web}

## Vereisten {#prerequisites}

* Zorg ervoor dat u de nieuwste versie gebruikt voor uw **Adobe Experience Platform Web SDK** extensie.

* Installeer de **Adobe Experience Platform Web SDK** in uw **Eigenschappen van tag** en de **Persoonlijke opslag** -optie.

  Deze configuratie is essentieel voor het opslaan van gebeurtenisgeschiedenissen op de cliënt, een voorwaarde voor het uitvoeren van de Regels van de Frequentie in de Bouwer van Regels. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## Verzonden gegevens naar platformregel configureren {#configure-sent-data-trigger}

1. Toegang tot uw **Adobe Experience Platform-gegevensverzameling** -instantie en navigeer naar **Eigenschappen van label** geconfigureerd met de **Adobe Experience Platform Web SDK** extensie.

1. Van de **Authoring** menu, selecteert u **Regels** dan **Nieuwe regel maken** of **Regel toevoegen**.

   ![](assets/configure_web_inapp_2.png)

1. In de **Gebeurtenissen** sectie, klikken **Toevoegen** en configureren als volgt:

   * **Extensie**: Core

   * **Type gebeurtenis**: Bibliotheek geladen (pagina boven).

   ![](assets/configure_web_inapp_3.png)

1. Klikken **Wijzigingen behouden** om de gebeurtenisconfiguratie op te slaan.

1. In de **Handelingen** sectie, klikken **Toevoegen** en configureren als volgt:

   * **Extensie**: Adobe Experience Platform Web SDK

   * **Type handeling**: De gebeurtenis Send

   ![](assets/configure_web_inapp_4.png)

1. In de **Personalisatie** deel van uw **Handeling** tekst, inschakelen **Besluiten over visuele personalisatie renderen** -optie.

   ![](assets/configure_web_inapp_5.png)

1. In de **Beslissingscontext** in, definieert u de **Sleutel** en **Waarde** paren die bepalen welke ervaring om te leveren.

   ![](assets/configure_web_inapp_6.png)

1. Sla uw **Handeling** configuratie door te klikken **Wijzigingen behouden**.

1. Ga naar de **Publicatiestroom** -menu. Een nieuwe **Bibliotheek** of selecteer een bestaande **Bibliotheek** en voeg uw nieuw gemaakte **Regel** aan de Commissie. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. Van uw **Bibliotheek**, selecteert u **Opslaan en samenstellen voor ontwikkeling**.

   ![](assets/configure_web_inapp_7.png)

## Handmatige regel configureren {#configure-manual-trigger}

1. Toegang tot uw **Adobe Experience Platform-gegevensverzameling** -instantie en navigeer naar **Eigenschappen van label** geconfigureerd met de **Adobe Experience Platform Web SDK** extensie.

1. Van de **Authoring** menu, selecteert u **Regels** dan **Nieuwe regel maken** of **Regel toevoegen**.

   ![](assets/configure_web_inapp_8.png)

1. In de **Gebeurtenissen** sectie, klikken **Toevoegen** en configureren als volgt:

   * **Extensie**: Core

   * **Type gebeurtenis**: Klikken

   ![](assets/configure_web_inapp_9.png)

1. In de **Configuratie klikken**, de **Kiezer** dat zal worden geëvalueerd .

   ![](assets/configure_web_inapp_10.png)

1. Klikken **Wijzigingen behouden** om de **Gebeurtenis** configuratie.

1. In de **Handelingen** sectie, klikken **Toevoegen** en configureren als volgt:

   * **Extensie**: Adobe Experience Platform Web SDK

   * **Type handeling**: Regels evalueren

   ![](assets/configure_web_inapp_11.png)

1. In de **Handeling linialen evalueren** deel van uw **Handeling** tekst, inschakelen **Besluiten over visuele personalisatie renderen** -optie.

   ![](assets/configure_web_inapp_13.png)

1. In de **Beslissingscontext** in, definieert u de **Sleutel** en **Waarde** paren die bepalen welke ervaring om te leveren.

1. Toegang krijgen tot de **Publicatiestroom** een nieuw menu maken **Bibliotheek** of selecteer een bestaande **Bibliotheek** en voeg uw nieuw gemaakte **Regel**. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. Van uw **Bibliotheek**, selecteert u **Opslaan en samenstellen voor ontwikkeling**.

   ![](assets/configure_web_inapp_14.png)

