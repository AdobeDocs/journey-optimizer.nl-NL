---
title: Een melding in de app maken
description: Leer hoe u een bericht in de app maakt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, bericht, maken, starten
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 2%

---

# Een bericht in de app maken {#create-in-app}

<!--
>[!BEGINTABS]

>[!TAB Add an In-app message to a journey]

>[!AVAILABILITY]
>
>The In-app activity is currently available as a beta to select users only. To join the beta program, contact Adobe Customer Care.

1. Open your journey, then drag and drop an **[!UICONTROL In-app]** activity from the **[!UICONTROL Actions]** section of the palette.

    When a profile reaches the end of their journey, any in-app messages displayed to them will automatically expire. For that reason, a Wait activity is automatically added after your In-app activity to ensure proper timing.

    ![](assets/in_app_journey_1.png)

1. Enter a **[!UICONTROL Label]** and **[!UICONTROL Description]** for your message.

1. Choose the [In-app surface](inapp-configuration.md) to use.

    ![](assets/in_app_journey_2.png)

1. You can now start designing your content with the **[!UICONTROL Edit content]** button. [Learn more](design-in-app.md)

1. Click **[!UICONTROL Edit trigger]** to configure your Trigger. 

    ![](assets/in_app_journey_4.png)

1. Choose the frequency of your trigger when your In-app message is active:

    * **[!UICONTROL Show every time]**: Always show the message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show once]**: Only show this message the first time the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show until click through]**: Show this message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur until an interact event is sent by the SDK with an action of "clicked".

1. From the **[!UICONTROL Mobile app trigger]** dropdown(s), choose the event(s) and criteria that will trigger your message:

    1. From the left drop-down, select the event required to trigger the message.
    1. From the right drop-down, select the validation required on the selected event.
    1. Click the **[!UICONTROL Add]** button if you want the trigger to consider multiple events or criteria. Then, repeat the steps above.
    1. Select how your events are linked, e.g. choose **[!UICONTROL And]** if you want **both** triggers to be true in order for a message to be shown or choose **[!UICONTROL Or]** if you want the message to be shown if **either** of the triggers are true.
    1. Click **[!UICONTROL Save]** when your Triggers have been configured.

    ![](assets/in_app_journey_3.png)
    
1. If necessary, complete your journey flow by dragging and dropping additional actions or events. [Learn more](../building-journeys/about-journey-activities.md)

1. Once your In-app message is ready, finalize the configuration and publish your journey to activate it.

For more information on how to configure a journey, refer to [this page](../building-journeys/journey-gs.md).

>[!TAB Add an In-app message to a campaign]
-->

1. Toegang krijgen tot de **[!UICONTROL Campaigns]** en klik vervolgens op **[!UICONTROL Create campaign]**.

1. In de **[!UICONTROL Properties]** , selecteert u wanneer het type uitvoering van de campagne: Gepland of API-geactiveerd. Meer informatie over campagneretypen in [deze pagina](../campaigns/create-campaign.md#campaigntype).

1. In de **[!UICONTROL Actions]** in, kiest u **[!UICONTROL In-app message]** en de **[!UICONTROL App surface]** eerder geconfigureerd voor uw bericht in de app. Klik vervolgens op **[!UICONTROL Create]**.

   Meer informatie over configuratie in de app in [deze pagina](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Van de **[!UICONTROL Properties]** in, voert u de **[!UICONTROL Title]** en de **[!UICONTROL Description]** beschrijving.

1. Als u aangepaste of basislabels voor gegevensgebruik wilt toewijzen aan het bericht in de app, selecteert u **[!UICONTROL Manage access]**. [Meer informatie](../administration/object-based-access.md).

1. Klik op de knop **[!UICONTROL Select audience]** om het publiek te bepalen om van de lijst van beschikbare publiek van Adobe Experience Platform te richten. [Meer informatie](../audience/about-audiences.md).

   ![](assets/in_app_create_2.png)

1. In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde publiek te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

1. Klikken **[!UICONTROL Create experiment]** om uw inhoud te configureren experimenteert u en maakt u behandelingen om de prestaties te meten en de beste optie voor uw doelgroep te identificeren. [Meer informatie](../campaigns/content-experiment.md)

1. Klikken **[!UICONTROL Edit triggers]** om de gebeurtenis(sen) en criteria te kiezen die uw bericht activeren. Met regelbuilders kunnen gebruikers criteria en waarden opgeven die, wanneer ze voldoen, een set handelingen activeren, zoals het verzenden van een bericht in de app.

   1. Klik op de vervolgkeuzelijst Gebeurtenis om de trigger zo nodig te wijzigen.

   1. Klikken **[!UICONTROL Add condition]** als u wilt dat de trigger rekening houdt met meerdere gebeurtenissen of criteria.

   1. Kies de optie **[!UICONTROL Or]** voorwaarde als u meer wilt toevoegen **[!UICONTROL Triggers]** om uw regel verder uit te breiden.

      ![](assets/in_app_create_3.png)

   1. Kies de optie **[!UICONTROL And]** voorwaarde als u wilt toevoegen **[!UICONTROL Traits]** en perfectioneer uw regel beter.

      +++Zie beschikbare Traits.

      | Pakket | Eigenschappen  | Definitie |
      |---|---|---|
      | Apparaatinfo | Naam vervoerder | Wordt geactiveerd wanneer aan een van de naam van de vervoerder uit de lijst wordt voldaan. |
      | Apparaatinfo | Apparaatnaam | Wordt geactiveerd wanneer aan een van de apparaatnamen wordt voldaan. |
      | Apparaatinfo | Landinstelling | Wordt geactiveerd wanneer aan een van de talen in de lijst wordt voldaan. |
      | Apparaatinfo | Besturingssysteemversie | Wordt geactiveerd wanneer aan een van de opgegeven versies van het besturingssysteem wordt voldaan. |
      | Apparaatinfo | Vorige OS-versie | Wordt geactiveerd wanneer aan een van de opgegeven versies van het vorige besturingssysteem wordt voldaan. |
      | Apparaatinfo | Uitvoeren, modus | Wordt geactiveerd als de uitvoeringsmodus een toepassing of een uitbreiding is. |
      | Levenscyclus toepassing | Toepassings-id | Wordt geactiveerd wanneer aan de opgegeven toepassings-id wordt voldaan. |
      | Levenscyclus toepassing | Dag van de week | Wordt geactiveerd wanneer de opgegeven dag van de week is bereikt. |
      | Levenscyclus toepassing | Dag sinds eerste gebruik | Wordt geactiveerd wanneer het opgegeven aantal dagen sinds het eerste gebruik is bereikt. |
      | Levenscyclus toepassing | Dag sinds laatste gebruik | Wordt geactiveerd wanneer het opgegeven aantal dagen sinds laatste gebruik is bereikt. |
      | Levenscyclus toepassing | Dag sinds upgrade | Wordt geactiveerd wanneer het opgegeven aantal dagen sinds de laatste upgrade is bereikt. |
      | Levenscyclus toepassing | Datum van installatie | Wordt geactiveerd wanneer de opgegeven installatiedatum is bereikt. |
      | Levenscyclus toepassing | Lanceringen | Wordt geactiveerd wanneer aan het opgegeven aantal Launches wordt voldaan. |
      | Levenscyclus toepassing | Tijd van dag | Wordt geactiveerd wanneer de opgegeven tijd van de dag is bereikt. |
      | Plaatsen | Huidige POI | Wordt geactiveerd door de SDK Plaatsen wanneer uw klant het opgegeven Point of Interest (POI) invoert. |
      | Plaatsen | Laatste ingevoerde POI | Wordt geactiveerd door de SDK van Plaatsen, afhankelijk van uw klant die het laatst Point of Interest (POI) heeft ingevoerd. |
      | Plaatsen | Laatst afgesloten POI | Wordt geactiveerd door de SDK van Plaatsen, afhankelijk van het punt van interesse dat de klant het laatst heeft verlaten (POI). |

+++

      ![](assets/in_app_create_8.png)

   1. Klikken **[!UICONTROL Make group]** om triggers samen te groeperen.

1. Kies de frequentie van de trigger wanneer het bericht in de app actief is. De volgende opties zijn beschikbaar:

   * **[!UICONTROL Everytime]**: Toon altijd het bericht wanneer de gebeurtenissen die in **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Once]**: Alleen dit bericht weergeven als de in het dialoogvenster **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Until click through]**: Dit bericht weergeven wanneer de gebeurtenissen zijn geselecteerd in het dialoogvenster **[!UICONTROL Mobile app trigger]** drop-down komt voor tot een interactie gebeurtenis door SDK met een actie van &quot;geklikt&quot;wordt verzonden.
   * **[!UICONTROL X number of times]**: Dit bericht wordt X-tijd weergegeven.

1. Kies zo nodig welke **[!UICONTROL Day of the week]** of **[!UICONTROL Time of day]** Het bericht in de app wordt weergegeven.

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe u de **[!UICONTROL Schedule]** van uw campagne in [deze sectie](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. U kunt nu beginnen met het ontwerpen van uw inhoud met de **[!UICONTROL Edit content]** knop. [Meer informatie](design-in-app.md)

   ![](assets/in_app_create_4.png)

<!--
>[!ENDTABS]
-->

## Instructievideo&#39;s{#video}

* In de onderstaande video ziet u hoe u in-app-berichten kunt maken, configureren en publiceren in uw campagnes.

  +++Zie video
  >[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)
+++

* In de onderstaande video ziet u hoe u experimenten met inhoud kunt configureren en analyseren op berichten in de A/B-test.

  +++Zie video
  >[!VIDEO](https://video.tv.adobe.com/v/3419898)
+++


**Verwante onderwerpen:**

* [In-app-bericht ontwerpen](design-in-app.md)
* [Uw In-app-bericht testen en verzenden](send-in-app.md)
* [Rapport in app](../reports/campaign-global-report.md#inapp-report)
* [Configuratie in de app](inapp-configuration.md)