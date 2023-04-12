---
title: Een melding in de app maken
description: Leer hoe u een bericht in de app maakt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, bericht, maken, starten
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 1af9a3adeb6727e965e61434b0ed2c41ff3d4911
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 2%

---

# Een bericht in de app maken {#create-in-app}

In-app berichten worden gemaakt in de context van een campagne.

Voer de onderstaande stappen uit om een bericht in de app te maken:

1. Toegang krijgen tot **[!UICONTROL Campaigns]** en klik vervolgens op **[!UICONTROL Create campaign]**.

1. In de **[!UICONTROL Properties]** selecteert u wanneer het uitvoeringstype van de campagne: Gepland of API-geactiveerd. Meer informatie over soorten campagnes in [deze pagina](../campaigns/create-campaign.md#campaigntype).

1. In de **[!UICONTROL Actions]** in, kiest u de **[!UICONTROL In-app message]** en de **[!UICONTROL App surface]** eerder geconfigureerd voor uw bericht in de app. Klik vervolgens op **[!UICONTROL Create]**.

   Meer informatie over configuratie in de app in [deze pagina](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Van de **[!UICONTROL Properties]** in, voert u de **[!UICONTROL Title]** en de **[!UICONTROL Description]** beschrijving.

1. Selecteer **[!UICONTROL Manage access]**. [Meer informatie](../administration/object-based-access.md).

1. Klik op de knop **[!UICONTROL Select audience]** om het publiek te bepalen om van de lijst van beschikbare segmenten van Adobe Experience Platform te richten. [Meer informatie](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

1. Klikken **[!UICONTROL Edit triggers]** om de gebeurtenis(sen) en criteria te kiezen die uw bericht activeren:

   1. Klikken **Voorwaarde toevoegen** als u wilt dat de trigger rekening houdt met meerdere gebeurtenissen of criteria.
   1. Selecteer hoe uw gebeurtenissen worden gekoppeld. Kies bijvoorbeeld **[!UICONTROL And]** als u **beide** triggers moeten waar zijn om een bericht weer te geven of **[!UICONTROL Or]** als u wilt dat het bericht wordt getoond als **ofwel** van de triggers zijn waar.
   1. Klikken **[!UICONTROL Make group]** om triggers samen te groeperen.

   ![](assets/in_app_create_3.png)

1. Kies de frequentie van de trigger wanneer het bericht in de app actief is. De volgende opties zijn beschikbaar:

   * **[!UICONTROL Everytime]**: Toon altijd het bericht wanneer de gebeurtenissen die in **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Once]**: Alleen dit bericht weergeven als de gebeurtenissen die voor de eerste keer zijn geselecteerd in het dialoogvenster **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Until click through]**: Dit bericht weergeven wanneer de gebeurtenissen zijn geselecteerd in het dialoogvenster **[!UICONTROL Mobile app trigger]** drop-down komt voor tot een interactie gebeurtenis door SDK met een actie van &quot;geklikt&quot;wordt verzonden.
   * **[!UICONTROL X number of times]**: Dit bericht X-tijd tonen.

1. Kies zo nodig welke **[!UICONTROL Day of the week]** of **[!UICONTROL Time of day]** Het bericht in de app wordt weergegeven.

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe u de **[!UICONTROL Schedule]** van uw campagne in [deze sectie](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. U kunt nu beginnen met het ontwerpen van uw inhoud met de **[!UICONTROL Edit content]** knop. [Meer informatie](design-in-app.md)

   ![](assets/in_app_create_4.png)


## Hoe kan ik-video{#video}

In de onderstaande video ziet u hoe u in-app-berichten kunt maken, configureren en publiceren in uw campagnes.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**Verwante onderwerpen:**

* [In-app-bericht ontwerpen](design-in-app.md)
* [Uw In-app-bericht testen en verzenden](send-in-app.md)
* [Rapport in app](../reports/campaign-global-report.md#inapp-report)
* [Configuratie in de app](inapp-configuration.md)