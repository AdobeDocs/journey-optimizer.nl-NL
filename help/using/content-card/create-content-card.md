---
title: Inhoudskaarten maken
description: Leer hoe u inhoudskaarten ontwerpt en de inhoud ervan bewerkt in Journey Optimizer
topic: Content Management
feature: Content Cards
role: User
level: Beginner
exl-id: a26bb3bd-d593-466b-9852-94e194d6d2b7
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '1319'
ht-degree: 1%

---

# Inhoudskaarten maken {#create-content-card}

>[!IMPORTANT]
>
>Standaard wordt de kaart verborgen met de knop Sluiten. Om meer functionaliteit toe te voegen, kunt u ontslagregels manueel bepalen of.

>[!BEGINTABS]

>[!TAB  voeg de kaarten van de Inhoud aan een reis ] toe

Voer de volgende stappen uit om een inhoudskaart toe te voegen aan een reis:

1. Open uw reis en sleep een **[!UICONTROL Card]** -activiteit vanuit de **[!UICONTROL Actions]** -sectie van het palet.

   ![](assets/content-card-jo-1.png)

1. Voer een **[!UICONTROL Label]** en **[!UICONTROL Description]** in voor uw bericht.

1. Kies uw [ de kaartconfiguratie van de Inhoud ](content-card-configuration.md) aan gebruik.

   ![](assets/content-card-jo-2.png)

1. U kunt nu beginnen met het ontwerpen van uw inhoud met de knop **[!UICONTROL Edit content]** . [Meer informatie](design-content-card.md)

1. Schakel de optie **[!UICONTROL Enable additional delivery rules]** in en selecteer **[!UICONTROL Edit rules]** om te bepalen wanneer uw bericht moet worden weergegeven, verwijderd of permanent verborgen.

   ![](assets/content-card-jo-3.png)

   1. Klik op **[!UICONTROL Add condition]** om uw gebeurtenis te selecteren.

      +++Zie beschikbare gebeurtenis.

      | Pakket | Trigger | Definitie |
      |---|---|---|
      | Gegevens verzenden naar platform | Gegevens verzonden naar platform | Wordt geactiveerd wanneer de mobiele app een Edge Experience-gebeurtenis uitgeeft om gegevens naar Adobe Experience Platform te verzenden. Gewoonlijk de API vraag [ sendEvent ](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) van de uitbreiding van AEP Edge. |
      | Core tracking | Handeling track | Teweeggebracht wanneer de erfenisfunctionaliteit die in mobiele code API [ wordt aangeboden trackAction ](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction) wordt geroepen. |
      | Core tracking | Status track | Teweeggebracht wanneer de erfenisfunctionaliteit die in mobiele code API [ wordt aangeboden trackState ](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate) wordt geroepen. |
      | Core tracking | PII verzamelen | Teweeggebracht wanneer de erfenisfunctionaliteit die in mobiele code API [ wordt aangeboden collectPII ](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii) wordt geroepen. |
      | Levenscyclus toepassing | Toepassing starten | Teweeggebracht bij elke looppas, met inbegrip van neerstortingen en installaties. Wordt ook geactiveerd op een hervat vanaf de achtergrond wanneer de time-out van de levenscyclussessie is overschreden. |
      | Levenscyclus toepassing | Toepassing installeren | Wordt geactiveerd bij de eerste run na installatie of herinstallatie. |
      | Levenscyclus toepassing | Toepassingsupdate | Teweeggebracht bij de eerste looppas na een verbetering of wanneer het versieaantal verandert. |
      | Levenscyclus toepassing | Toepassing sluiten | Wordt geactiveerd wanneer de toepassing wordt gesloten. |
      | Levenscyclus toepassing | Toepassing vastloopt | Wordt geactiveerd wanneer de toepassing geen achtergrond heeft voordat deze wordt gesloten. De gebeurtenis wordt verzonden wanneer de toepassing na de crash wordt gestart. Adobe Mobile-crashrapportage implementeert geen globale handler voor niet-afgevangen uitzonderingen. |

      +++

   1. Kies de voorwaarde **[!UICONTROL Or]** als u meer **[!UICONTROL Triggers]** wilt toevoegen om de lijn verder uit te breiden.

   1. Kies de voorwaarde **[!UICONTROL And]** als u **[!UICONTROL Traits]** wilt toevoegen en uw regel beter wilt perfectioneren.

      +++Zie de beschikbare traits.

      | Pakket | Treinen | Definitie |
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
      | Levenscyclus toepassing | Starten | Wordt geactiveerd wanneer aan het opgegeven aantal Launches wordt voldaan. |
      | Levenscyclus toepassing | Tijd van dag | Wordt geactiveerd wanneer de opgegeven tijd van de dag is bereikt. |

      +++

   1. Klik op **[!UICONTROL Make group]** om triggers samen te groeperen.

1. Indien nodig voltooit u de reisflow door extra handelingen of gebeurtenissen te slepen en neer te zetten. [Meer informatie](../building-journeys/about-journey-activities.md)

1. Zodra uw inhoudskaart klaar is, voltooi de configuratie en publiceer uw reis om het te activeren.

Voor meer informatie over hoe te om een reis te vormen, verwijs naar [ deze pagina ](../building-journeys/journey-gs.md).

>[!TAB  voeg de kaarten van de Inhoud aan een campagne ] toe

Volg de onderstaande stappen om uw inhoudskaarten te gaan maken via een campagne.

1. Maak een campagne. [Meer informatie](../campaigns/create-campaign.md)

1. Selecteer het type campagne dat u wilt uitvoeren

   * **[!UICONTROL Scheduled - Marketing]** : voer de campagne onmiddellijk uit of op een opgegeven datum. De geplande campagnes zijn gericht op het verzenden van **marketing** berichten. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

   * **[!UICONTROL API-triggered - Marketing/Transactional]** : voer de campagne uit met behulp van een API-aanroep. API-teweeggebrachte campagnes zijn gericht op het verzenden van of **marketing**, of **transactie** berichten, d.w.z. berichten die na een actie worden verzonden die door een individu wordt uitgevoerd: het terugstellen van het wachtwoord, het kartelaankoop enz. [ Leer hoe te om een campagne teweeg te brengen gebruikend APIs ](../campaigns/api-triggered-campaigns.md)

   ![](assets/content-card-create-1.png)

1. Geef in de sectie **[!UICONTROL Properties]** een naam en een beschrijving voor de campagne op.

1. In de **sectie van het publiek**, klik de **[!UICONTROL Select audience]** knoop om de lijst van beschikbare publiek van Adobe Experience Platform te tonen. [ leer meer over publiek ](../audience/about-audiences.md)

1. Kies in het veld **[!UICONTROL Identity namespace]** de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [ Leer meer over namespaces ](../event/about-creating.md#select-the-namespace)

1. Selecteer de handeling **[!UICONTROL Content card]** .

   ![](assets/content-card-create-2.png)

1. Selecteer of creeer een nieuwe [ de kaartconfiguratie van de Inhoud ](content-card-configuration.md).

1. Klik op **[!UICONTROL Create experiment]** om de inhoud van uw bericht te testen. Hierdoor kunt u meerdere variabelen van een levering testen op monsterpopulaties om te bepalen welke behandeling de grootste invloed heeft op het doelpubliek. [ Leer meer over inhoudexperiment ](../content-management/content-experiment.md).

1. Schakel de optie **[!UICONTROL Enable additional delivery rules]** in en selecteer **[!UICONTROL Edit rules]** om te bepalen wanneer uw bericht moet worden weergegeven, verwijderd of permanent verborgen.

   De regelbouwers van het gebruik om specifieke voorwaarden te plaatsen die deze acties teweegbrengen.

   1. Klik op **[!UICONTROL Add condition]** om uw gebeurtenis te selecteren.

      +++Zie beschikbare gebeurtenis.

      | Pakket | Trigger | Definitie |
      |---|---|---|
      | Gegevens verzenden naar platform | Gegevens verzonden naar platform | Wordt geactiveerd wanneer de mobiele app een Edge Experience-gebeurtenis uitgeeft om gegevens naar Adobe Experience Platform te verzenden. Gewoonlijk de API vraag [ sendEvent ](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) van de uitbreiding van AEP Edge. |
      | Core tracking | Handeling track | Teweeggebracht wanneer de erfenisfunctionaliteit die in mobiele code API [ wordt aangeboden trackAction ](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction) wordt geroepen. |
      | Core tracking | Status track | Teweeggebracht wanneer de erfenisfunctionaliteit die in mobiele code API [ wordt aangeboden trackState ](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate) wordt geroepen. |
      | Core tracking | PII verzamelen | Teweeggebracht wanneer de erfenisfunctionaliteit die in mobiele code API [ wordt aangeboden collectPII ](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii) wordt geroepen. |
      | Levenscyclus toepassing | Toepassing starten | Teweeggebracht bij elke looppas, met inbegrip van neerstortingen en installaties. Wordt ook geactiveerd op een hervat vanaf de achtergrond wanneer de time-out van de levenscyclussessie is overschreden. |
      | Levenscyclus toepassing | Toepassing installeren | Wordt geactiveerd bij de eerste run na installatie of herinstallatie. |
      | Levenscyclus toepassing | Toepassingsupdate | Teweeggebracht bij de eerste looppas na een verbetering of wanneer het versieaantal verandert. |
      | Levenscyclus toepassing | Toepassing sluiten | Wordt geactiveerd wanneer de toepassing wordt gesloten. |
      | Levenscyclus toepassing | Toepassing vastloopt | Wordt geactiveerd wanneer de toepassing geen achtergrond heeft voordat deze wordt gesloten. De gebeurtenis wordt verzonden wanneer de toepassing na de crash wordt gestart. Adobe Mobile-crashrapportage implementeert geen globale handler voor niet-afgevangen uitzonderingen. |

      +++

   1. Kies de voorwaarde **[!UICONTROL Or]** als u meer **[!UICONTROL Triggers]** wilt toevoegen om de lijn verder uit te breiden.

   1. Kies de voorwaarde **[!UICONTROL And]** als u **[!UICONTROL Traits]** wilt toevoegen en uw regel beter wilt perfectioneren.

      +++Zie de beschikbare traits.

      | Pakket | Treinen | Definitie |
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
      | Levenscyclus toepassing | Starten | Wordt geactiveerd wanneer aan het opgegeven aantal Launches wordt voldaan. |
      | Levenscyclus toepassing | Tijd van dag | Wordt geactiveerd wanneer de opgegeven tijd van de dag is bereikt. |

      +++

   1. Klik op **[!UICONTROL Make group]** om triggers samen te groeperen.

   ![](assets/content-card-rules.png)

1. U kunt uw campagne plannen aan een specifieke datum of reeks om met regelmatige intervallen opnieuw te komen. [Meer informatie](../campaigns/create-campaign.md#schedule)

1. U kunt nu beginnen met het ontwerpen van uw inhoud met de **[!UICONTROL Edit content]** . [Meer informatie](design-content-card.md)

   ![](assets/content-card-create-4.png)

>[!ENDTABS]
