---
title: Een melding in de app maken
description: Leer hoe u een bericht in de app maakt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, bericht, maken, starten
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# Een bericht in de app maken {#create-in-app}

In-app berichten worden gemaakt in de context van een campagne.

>[!BEGINTABS]

>[!TAB Een bericht in de app toevoegen aan een reis]

>[!AVAILABILITY]
>
>De activiteit in de app is momenteel beschikbaar als een bètaversie om alleen gebruikers te selecteren. Neem contact op met de klantenservice van Adobe om deel te nemen aan het bètaprogramma.

1. Open uw reis en sleep vervolgens een **[!UICONTROL In-app]** van de **[!UICONTROL Actions]** in het palet.

   Wanneer een profiel het einde van de rit bereikt, verlopen alle berichten in de app die aan hen worden weergegeven, automatisch. Daarom wordt er automatisch een wachtbewerking toegevoegd na uw activiteiten in de app om de juiste timing te garanderen.

   ![](assets/in_app_journey_1.png)

1. Voer een **[!UICONTROL Label]** en **[!UICONTROL Description]** voor uw bericht.

1. Kies de optie [In-app oppervlak](inapp-configuration.md) te gebruiken.

   ![](assets/in_app_journey_2.png)

1. U kunt nu beginnen met het ontwerpen van uw inhoud met de **[!UICONTROL Edit content]** knop. [Meer informatie](design-in-app.md)

1. Klikken **[!UICONTROL Edit trigger]** om de trigger te configureren.

   ![](assets/in_app_journey_4.png)

1. Kies de frequentie van de trigger wanneer het bericht in de app actief is:

   * **[!UICONTROL Show every time]**: Toon altijd het bericht wanneer de gebeurtenissen die in **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Show once]**: Alleen dit bericht weergeven als de gebeurtenissen die voor de eerste keer zijn geselecteerd in het dialoogvenster **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Show until click through]**: Dit bericht weergeven wanneer de gebeurtenissen zijn geselecteerd in het dialoogvenster **[!UICONTROL Mobile app trigger]** drop-down komt voor tot een interactie gebeurtenis door SDK met een actie van &quot;geklikt&quot;wordt verzonden.

1. Van de **[!UICONTROL Mobile app trigger]** -dropdown(s), kies de gebeurtenis(sen) en de criteria die uw bericht zullen activeren:

   1. Selecteer in de linkervervolgkeuzelijst de gebeurtenis die nodig is om het bericht te activeren.
   1. Selecteer in de rechtervervolgkeuzelijst de vereiste validatie voor de geselecteerde gebeurtenis.
   1. Klik op de knop **[!UICONTROL Add]** als u wilt dat de trigger rekening houdt met meerdere gebeurtenissen of criteria. Herhaal vervolgens de bovenstaande stappen.
   1. Selecteer hoe uw gebeurtenissen worden gekoppeld. Kies bijvoorbeeld **[!UICONTROL And]** als u **beide** triggers moeten waar zijn om een bericht weer te geven of **[!UICONTROL Or]** als u wilt dat het bericht wordt getoond als **ofwel** van de triggers zijn waar.
   1. Klikken **[!UICONTROL Save]** wanneer uw triggers zijn geconfigureerd.

   ![](assets/in_app_journey_3.png)

1. Indien nodig voltooit u de reisflow door extra handelingen of gebeurtenissen te slepen en neer te zetten. [Meer informatie](../building-journeys/about-journey-activities.md)

1. Zodra uw bericht in de app klaar is, voltooit u de configuratie en publiceert u uw reis om het te activeren.

Voor meer informatie over hoe te om een reis te vormen, verwijs naar [deze pagina](../building-journeys/journey-gs.md).

>[!TAB Een bericht in de app toevoegen aan een campagne]

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

>[!ENDTABS]

## Hoe kan ik-video{#video}

In de onderstaande video ziet u hoe u in-app-berichten kunt maken, configureren en publiceren in uw campagnes.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**Verwante onderwerpen:**

* [In-app-bericht ontwerpen](design-in-app.md)
* [Uw In-app-bericht testen en verzenden](send-in-app.md)
* [Rapport in app](../reports/campaign-global-report.md#inapp-report)
* [Configuratie in de app](inapp-configuration.md)