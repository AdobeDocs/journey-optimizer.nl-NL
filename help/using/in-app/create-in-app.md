---
title: Een melding in de app maken in Journey Optimizer
description: Leer hoe u een bericht in de app maakt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, bericht, maken, starten
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 94c4e0e53625fdf20f940e8bfd15d67dba1d0120
workflow-type: tm+mt
source-wordcount: '1847'
ht-degree: 1%

---

# Een bericht in de app maken {#create-in-app}

U kunt een bericht in de app toevoegen aan een campagne of een reis. Voer de onderstaande stappen uit om in beide contexten een bericht in de app te maken.

>[!BEGINTABS]

>[!TAB Een bericht in de app toevoegen aan een reis]

Ga als volgt te werk om een bericht in de app toe te voegen:

1. Open uw reis en sleep vervolgens een **[!UICONTROL In-app]** van de **[!UICONTROL Actions]** in het palet.

   Wanneer een profiel het einde van de rit bereikt, verlopen alle berichten in de app die aan hen worden weergegeven, automatisch. Daarom wordt er automatisch een wachtbewerking toegevoegd na uw activiteiten in de app om de juiste timing te garanderen.

   ![](assets/in_app_journey_1.png)

1. Voer een **[!UICONTROL Label]** en **[!UICONTROL Description]** voor uw bericht.

1. Kies de optie [In-app oppervlak](inapp-configuration.md) te gebruiken.

   ![](assets/in_app_journey_2.png)

1. U kunt nu beginnen met het ontwerpen van uw inhoud met de **[!UICONTROL Edit content]** knop. [Meer informatie](design-in-app.md)

1. Klikken **[!UICONTROL Edit triggers]** om de gebeurtenis(sen) en criteria te kiezen die uw bericht activeren. Met regelbuilders kunnen gebruikers criteria en waarden opgeven die, wanneer ze voldoen, een set handelingen activeren, zoals het verzenden van een bericht in de app.

   ![](assets/in_app_journey_4.png)

   1. Klik op de vervolgkeuzelijst Gebeurtenis om de trigger zo nodig te wijzigen.

      +++Zie beschikbare triggers.

      | Pakket | Trigger | Definitie |
      |---|---|---|
      | Gegevens verzenden naar platform | Gegevens verzonden naar platform | Wordt geactiveerd wanneer de mobiele app een Edge Experience-gebeurtenis uitgeeft om gegevens naar Adobe Experience Platform te verzenden. Meestal de API-aanroep [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) uit de extensie AEP Edge. |
      | Core tracking | Handeling track | Wordt geactiveerd wanneer de verouderde functionaliteit wordt aangeboden in de API voor mobiele code [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction) wordt aangeroepen. |
      | Core tracking | Status track | Wordt geactiveerd wanneer de verouderde functionaliteit wordt aangeboden in de API voor mobiele code [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate) wordt aangeroepen. |
      | Core tracking | PII verzamelen | Wordt geactiveerd wanneer de verouderde functionaliteit wordt aangeboden in de API voor mobiele code [collectionPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii) wordt aangeroepen. |
      | Levenscyclus toepassing | Toepassing starten | Teweeggebracht bij elke looppas, met inbegrip van neerstortingen en installaties. Wordt ook geactiveerd op een hervat vanaf de achtergrond wanneer de time-out van de levenscyclussessie is overschreden. |
      | Levenscyclus toepassing | Toepassing installeren | Wordt geactiveerd bij de eerste run na installatie of herinstallatie. |
      | Levenscyclus toepassing | Toepassingsupdate | Teweeggebracht bij de eerste looppas na een verbetering of wanneer het versieaantal verandert. |
      | Levenscyclus toepassing | Toepassing sluiten | Wordt geactiveerd wanneer de toepassing wordt gesloten. |
      | Levenscyclus toepassing | Toepassing vastloopt | Wordt geactiveerd wanneer de toepassing geen achtergrond heeft voordat deze wordt gesloten. De gebeurtenis wordt verzonden wanneer de toepassing na de crash wordt gestart. Adobe Mobiele crashrapportage implementeert geen algemene niet-afgevangen uitzonderingshandler. |
      | Plaatsen | POI invoeren | Wordt geactiveerd door de SDK van Plaatsen wanneer uw klant het Point of Interest (POI) invoert dat u hebt geconfigureerd. |
      | Plaatsen | POI afsluiten | Wordt geactiveerd door de SDK van Plaatsen wanneer uw klant het Point of Interest (POI) verlaat dat u hebt geconfigureerd. |

+++

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

      ![](assets/in_app_journey_3.png)

   1. Kies de frequentie van de trigger wanneer het bericht in de app actief is:

      * **[!UICONTROL Show every time]**: Toon altijd het bericht wanneer de gebeurtenissen die in **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
      * **[!UICONTROL Show once]**: Alleen dit bericht weergeven als de in het dialoogvenster **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
      * **[!UICONTROL Show until click through]**: Dit bericht weergeven wanneer de gebeurtenissen zijn geselecteerd in het dialoogvenster **[!UICONTROL Mobile app trigger]** drop-down komt voor tot een interactie gebeurtenis door SDK met een actie van &quot;geklikt&quot;wordt verzonden.

1. Indien nodig voltooit u de reisflow door extra handelingen of gebeurtenissen te slepen en neer te zetten. [Meer informatie](../building-journeys/about-journey-activities.md)

1. Zodra uw bericht in de app klaar is, voltooit u de configuratie en publiceert u uw reis om het te activeren.

Voor meer informatie over hoe te om een reis te vormen, raadpleeg [deze pagina](../building-journeys/journey-gs.md).

>[!TAB Een bericht in de app toevoegen aan een campagne]

Voer de volgende stappen uit om een bericht in de app toe te voegen aan een campagne:

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

      +++Zie beschikbare triggers.

      | Pakket | Trigger | Definitie |
      |---|---|---|
      | Gegevens verzenden naar platform | Gegevens verzonden naar platform | Wordt geactiveerd wanneer de mobiele app een Edge Experience-gebeurtenis uitgeeft om gegevens naar Adobe Experience Platform te verzenden. Meestal de API-aanroep [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) uit de extensie AEP Edge. |
      | Core tracking | Handeling track | Wordt geactiveerd wanneer de verouderde functionaliteit wordt aangeboden in de API voor mobiele code [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction) wordt aangeroepen. |
      | Core tracking | Status track | Wordt geactiveerd wanneer de verouderde functionaliteit wordt aangeboden in de API voor mobiele code [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate) wordt aangeroepen. |
      | Core tracking | PII verzamelen | Wordt geactiveerd wanneer de verouderde functionaliteit wordt aangeboden in de API voor mobiele code [collectionPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii) wordt aangeroepen. |
      | Levenscyclus toepassing | Toepassing starten | Teweeggebracht bij elke looppas, met inbegrip van neerstortingen en installaties. Wordt ook geactiveerd op een hervat vanaf de achtergrond wanneer de time-out van de levenscyclussessie is overschreden. |
      | Levenscyclus toepassing | Toepassing installeren | Wordt geactiveerd bij de eerste run na installatie of herinstallatie. |
      | Levenscyclus toepassing | Toepassingsupdate | Teweeggebracht bij de eerste looppas na een verbetering of wanneer het versieaantal verandert. |
      | Levenscyclus toepassing | Toepassing sluiten | Wordt geactiveerd wanneer de toepassing wordt gesloten. |
      | Levenscyclus toepassing | Toepassing vastloopt | Wordt geactiveerd wanneer de toepassing geen achtergrond heeft voordat deze wordt gesloten. De gebeurtenis wordt verzonden wanneer de toepassing na de crash wordt gestart. Adobe Mobiele crashrapportage implementeert geen algemene niet-afgevangen uitzonderingshandler. |
      | Plaatsen | POI invoeren | Wordt geactiveerd door de SDK van Plaatsen wanneer uw klant het Point of Interest (POI) invoert dat u hebt geconfigureerd. |
      | Plaatsen | POI afsluiten | Wordt geactiveerd door de SDK van Plaatsen wanneer uw klant het Point of Interest (POI) verlaat dat u hebt geconfigureerd. |

+++

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

>[!ENDTABS]

## Instructievideo&#39;s{#video}

* In de onderstaande video ziet u hoe u in-app-berichten kunt maken, configureren en publiceren in uw campagnes.

  +++Zie video

  >[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)

+++

* In de onderstaande video ziet u hoe u experimenten met inhoud kunt configureren en analyseren op In-app-berichten voor A/B-tests.

  +++Zie video

  >[!VIDEO](https://video.tv.adobe.com/v/3419898)

+++

* In de onderstaande video ziet u hoe u een bericht in de app maakt tijdens een reis en hoe u uw reis kunt testen en publiceren.

  +++Zie video

  >[!VIDEO](https://video.tv.adobe.com/v/3423077)

+++

**Verwante onderwerpen:**

* [In-app-bericht ontwerpen](design-in-app.md)
* [Uw In-app-bericht testen en verzenden](send-in-app.md)
* [Rapport in app](../reports/campaign-global-report.md#inapp-report)
* [Configuratie in de app](inapp-configuration.md)