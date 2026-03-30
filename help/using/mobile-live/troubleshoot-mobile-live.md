---
solution: Journey Optimizer
product: journey optimizer
title: Live-activiteiten oplossen
description: Leer hoe te om Levende activiteiten in Journey Optimizer voor zowel eenheids als uitzendingsgebruiksgevallen problemen op te lossen, met inbegrip van profiel tokenkwesties, campagneconfiguratie, en leveringsmislukkingen
role: User
level: Intermediate
exl-id: f0f83bd2-7c2b-4d9b-b455-e1df12dfa175
source-git-commit: 016d905840a3ccc05ca1d2a934130b53c1108e7c
workflow-type: tm+mt
source-wordcount: '4503'
ht-degree: 0%

---

# Live-activiteiten oplossen {#troubleshoot-mobile-live}

Live-activiteiten in Adobe Journey Optimizer maken real-time, dynamische updates mogelijk op iOS-slotschermen en Dynamic Islands. Ze kunnen alleen worden geactiveerd en beheerd via door API&#39;s geactiveerde campagnes.

**gevaltypes van het Gebruik:**

* **Eenheid**: Individueel gericht, transactie (API-teweeggebrachte Transactionele campagnes)
* **Uitzending**: Publiek-gericht, massalevering (API-teweeggebrachte Marketing campagnes)

Een frequente uitdaging met Levende activiteiten is wanneer de API vraag om een Levende activiteit teweeg te brengen of bij te werken a **succesvolle reactie (200 O.K.)** terugkeert, maar de Levende activiteit ontbreekt om op het apparaat van de gebruiker te verschijnen of bij te werken. Deze verbinding tussen API bevestiging en daadwerkelijke apparatengedrag kan op veelvoudige punten in de leveringspijpleiding voorkomen. Deze gids verstrekt een systematische het oplossen van problemenbenadering om te identificeren waar de levering ontbreekt, die elk stadium van API verzoekbevestiging door apparatenteruggave onderzoekt.

## Vereisten

Zorg ervoor dat u beschikt over:

* 
  +++ Een Assurance-sessie instellen

  Opstelling een **zitting van Assurance** om de gebeurtenissen van SDK te vangen en de leveringspijpleiding te inspecteren. Assurance biedt zichtbaarheid in:

   * Edge Network-verzoeken en -antwoorden
   * Profielkwalificatiegebeurtenissen
   * Push token-registratie
   * Levende activiteiten

  Leer hoe te opstelling Assurance in de [ documentatie van Adobe Experience Platform Assurance ](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance).

  **Nota**: Voor Levende activiteit van iOS, zorg ervoor uw app op een fysiek apparaat van iOS (iOS 16.1 of later) of de Simulator van Xcode (iOS 16.1 of later) loopt.

  +++

* 
  +++ Gegevens over door API gestuurde campagnes verzamelen

  Navigeer naar de via API geactiveerde campagne in Journey Optimizer en zoek de volgende gegevens op:

   * Campagneraam
   * Campagne-id gevonden in de URL- of campagne-eigenschappen
   * Campagneversie indien van toepassing
   * Oppervlakteconfiguratie, iOS-toepassingsoppervlak gebruikt voor Live-activiteit

  +++

* 
  +++ Informatie over API-aanvragen verzamelen

  Sla tijdens het aanroepen van de API de Live-activiteit op:

   * payload van API-aanvragen, inclusief profiel-id&#39;s en Live-activiteitsgegevens
   * API-reactie inclusief statuscode, bericht-id, aanvraag-id
   * Tijdstempel van wanneer de API is aangeroepen
   * Gebruikte eindpunt, bijvoorbeeld `/campaign/{CAMPAIGN_ID}/execute`

  +++

* 
  +++ Het testprofiel identificeren

  Haal het volgende op uit uw API-verzoek:

   * Profielnaamruimte, bijvoorbeeld ECID, e-mail, klant-id
   * Profiel-id gebruikt in API-aanroep

  Controleer of u dit profiel in Adobe Experience Platform kunt opzoeken. Leer hoe te [ omhoog een profiel in de documentatie van Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide.html) kijken.

  +++

* 
  +++ Apparaat- en toepassingsgegevens

  Verzamel het volgende van uw testapparaat:

   * Apparaatmodel, bijvoorbeeld iPhone 14 Pro
   * iOS-versie
   * Id van toepassingspakket
   * APNs-pushtoken
   * De connectiviteitsstatus van het netwerk op het tijdstip van het testen

  +++

## Algemene scenario&#39;s

### Problemen met profiel- of pushtoken {#profile-issue}

[!BADGE  is op zowel eenheids als uitzendingsgebruiksgevallen ]{type=Positive} van toepassing

De API retourneert HTTP 200, maar de Live-activiteit wordt niet weergegeven. Vaak voorkomende oorzaken:

* Profiel bestaat niet in Adobe Experience Platform.
* Pushtoken voor live-activiteit is niet gesynchroniseerd met profiel.
* Pushdetails van Live-activiteit worden gesynchroniseerd maar bevatten een onjuiste configuratie, bijvoorbeeld onjuist `appId` of `attributeType` .

**Nota voor de gevallen van het uitzendingsgebruik**: Als sommige profielen in uw publiek tekenen missen, slechts zullen die profielen er niet in slagen om de Levende activiteit te ontvangen. Neem een monster van verschillende profielen van uw publiek om problemen met token te diagnosticeren. Dit is alleen van toepassing op externe start-gebeurtenissen, niet op update- of end-gebeurtenissen.

#### Voorcontroles

* iOS-toepassingsvereisten:
   * iOS 16.1+
   * `NSSupportsLiveActivities` ingesteld op `YES` in `Info.plist`
   * `ActivityAttributes` correct geïmplementeerd.
* Mobiele SDK-integratie:
   * Adobe Experience Platform Mobile SDK (messaging SDK 5.11.0+)
   * `Messaging.registerLiveActivities` geïmplementeerd en aangeroepen met pushtoken voor Live-activiteit.

#### Foutopsporingsstappen

1. 
   +++ Controleren of het profiel bestaat in Adobe Experience Platform

   1. In Journey Optimizer, navigeer aan **Klant** `>` **Profielen**.
   1. Zoeken met naamruimte en identiteitswaarde van API-verzoek.
   1. Als het profiel niet wordt gevonden, bestaat het profiel niet of wordt de opname niet voltooid. Maak het profiel of wacht op opname voordat u de Live-activiteit activeert.
   1. Als er een profiel wordt gevonden, gaat u verder naar stap 2 hieronder om te controleren of de pushtoken is gesynchroniseerd.

      +++

1. 
   +++ Controleren of push-token voor live-activiteit is gesynchroniseerd

   U kunt Assurance gebruiken om de tokenregistratie te verifiëren:

   1. In Assurance, van de **lijst van Gebeurtenissen**, filter of onderzoek naar gebeurtenissen `eventType = "liveActivity.pushToStart"`.
   1. Selecteer de **Gebeurtenis** en inspecteer de nuttige lading.
   1. Controleer of de waarden voor token, appId en attributeType aanwezig zijn.
   1. Bevestig of de gebeurtenis correct is verzonden.

   U kunt ook het Adobe Experience Platform-profiel inchecken.

   1. In Adobe Experience Platform, van uw **Profiel**, heb toegang tot **Gebeurtenissen** tabel.
   1. Zoeken naar `liveActivity.pushToStart` -gebeurtenissen.
   1. Controleer de even tijdstempel en lading.

   Als er geen gebeurtenissen worden gevonden, roept uw mobiele app `Messaging.registerLiveActivity` niet correct aan. U moet de SDK-integratie herstellen.

   +++

1. 
   +++ Tokendetails in profiel valideren

   1. Van uw **Profiel**, heb toegang tot **Attributen** tabel.
   1. Zoek `liveActivityPushNotificationDetails` .
   1. Verifieer de tokenconfiguratie:

      ```json
      {
        "liveActivityPushNotificationDetails": [
          {
            "appId": "com.example.myapp",
            "token": "abc123def456...",
            "platform": "apns",
            "denylisted": false,
            "attributeType": "OrderTrackingAttributes",
            "identity": {}
          }
        ]
      }
      ```

   **bevestigt elk gebied:**

   | Veld | Vereiste | Vaak probleem |
   |-|-|-|
   | `appId` | Moet exact overeenkomen met iOS-bundle-id | Verkeerde overeenkomst tussen dev/prod bundle IDs |
   | `attributeType` | Moet exact overeenkomen met SWIFT `ActivityAttributes` struct-naam (hoofdlettergevoelig) | Typo- of onjuiste structuurnaam |
   | `platform` | Moet `"apns"` of `"apnsSandbox"` zijn | Onjuiste platformwaarde |
   | `denylisted` | Moet zijn `false` | Token gemarkeerd als ongeldig of gebruiker uitgeschakeld |
   | `token` | Geldige APNs-pushtoken | Token verlopen of app opnieuw geïnstalleerd |

   Als een veld onjuist is: Werk de mobiele app bij, registreer u opnieuw met `Messaging.registerLiveActivities`, wacht 5-10 minuten en controleer het opnieuw.

   Als `liveActivityPushNotificationDetails` ontbreekt: het token is nog niet gesynchroniseerd. Wacht 5 tot 10 minuten nadat u de `liveActivity.pushToStart` -gebeurtenis in Assurance hebt gezien.

   +++

### Problemen met de configuratie en lading van campagnes {#payload-issues}

[!BADGE  is op zowel eenheids als uitzendingsgebruiksgevallen ]{type=Positive} van toepassing

Profiel bestaat met geldige tokens, maar Live-activiteit wordt niet weergegeven. Dit kan worden veroorzaakt door:

* Onjuiste oppervlak- of kanaalconfiguratie.
* Onjuiste API-laadstructuur.
* `content-state` en `attributes` komen niet overeen met iOS `ActivityAttributes` -implementatie.
* Stale `timestamp` (kritiek voor update/eind).

**Nota voor de gevallen van het uitzendingsgebruik**: De campagne moet **API-getriggerde Marketing** (niet Transactioneel) zijn. Bij Payload wordt `audience` gebruikt in plaats van individuele `profile` . Verwijs naar [ deze sectie ](#broadcast-config) voor uitzending-specifieke ladingsstructuur en naar [ documentatie van Adobe Developer ](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMAudienceMessageExecution) voor volledige API specificaties.

#### Voorcontroles

* De campagne is **API-teweeggebrachte Transactionele** (unitaire) of **API-teweeggebrachte Marketing** (uitzending) en **Hoge de optie van de Productie** moet **niet** worden toegelaten aangezien het met Levende activiteit onverenigbaar is.
* Zorg ervoor dat het profiel bestaat en de tekenen correct gebruikend het [ hierboven scenario ](#profile-issue) worden gesynchroniseerd.

#### Foutopsporingsstappen

1. 
   +++ Configuratie van campagneoppervlak verifiëren

   1. In Journey Optimizer, open uw **Campagne** en navigeer aan het **3} menu van Acties.**
   1. Controleer uw **Levende activiteitenconfiguratie**. Het oppervlak moet voor de iOS-toepassing worden geconfigureerd met een bundle-id die overeenkomt met de `appId` in het `liveActivityPushNotificationDetails` -profiel. Als uw profiel bijvoorbeeld `"appId": "com.example.myapp"` heeft, moet het oppervlak zich richten op dezelfde app.
   1. Controleer dat het **type van Activiteit** in uw campagneconfiguratie precies `attributeType` in uw profiel `liveActivityPushNotificationDetails` aanpast. Als uw profiel bijvoorbeeld `"attributeType": "FoodDeliveryLiveActivityAttributes"` heeft, moet de campagne hetzelfde type activiteit opgeven.

      +++

1. 
   +++Betalingsstructuur van API valideren

   Wanneer u de campagne uitvoert via de API, moet u ervoor zorgen dat de lading de juiste structuur volgt.

   **Eenheids lading:**

   ```json
   {
     "campaignId": "your-campaign-id",
     "recipients": [{
       "type": "aep",
       "userId": "user@example.com",
       "namespace": "email",
       "context": {
         "requestPayload": {
           "aps": {
             "content-available": 1,
             "timestamp": 1756984054,
             "event": "start",
             "attributes-type": "FoodDeliveryLiveActivityAttributes",
             "content-state": { ... },
             "attributes": { ... }
           }
         }
       }
     }]
   }
   ```

   **Gemeenschappelijke payload kwesties:**

   | Veld | Vereiste | Vaak probleem |
   |-|-|-|
   | `attributes-type` | Moet overeenkomen met type campagneactiviteit en profiel `attributeType` | Verkeerd of typefout |
   | `campaignId` | Moet overeenkomen met de geactiveerde campagne-id | Onjuiste of ontbrekende campagne-id |
   | `content-available` | Moet zijn `1` | Ontbrekende of onjuiste waarde |
   | `event` | Moet `"start"`, `"update"` of `"end"` zijn | Ongeldig gebeurtenistype |
   | `timestamp` | Moet altijd de huidige/laatste Unix-tijdperktijd in seconden zijn | Tijdstempel gebruiken in oude cache |
   | `userId` / `namespace` | Moet overeenkomen met een bestaand profiel in AEP | Profiel-id komt niet overeen |

   **Kritiek: Gebruik altijd recentste timestamp**

   * Het `timestamp` gebied moet **altijd** de **huidige Unix epoche tijd** (in seconden) zijn op het ogenblik elke API vraag wordt gemaakt.
   * Dit is op **van toepassing alle gebeurtenistypen**: `start`, `update`, en **vooral`end`**.
   * **Effect op updates/eindverzoeken**: Het gebruiken van een stapel of oude timestamp zal update en eindverzoeken veroorzaken om te ontbreken of door het apparaat worden genegeerd.
   * **NIET** hergebruik timestamps van vorige verzoeken of gebruik caching waarden.
   * Genereer een nieuwe tijdstempel voor elke API-aanroep.

   **Facultatieve gebieden (alle gebeurtenistypen):**

   * `requestId`: Unieke id voor reeksspatiëring (aanbevolen).
   * `alert`: Object met `title` en `body` voor melding (handig om de aandacht op updates te vestigen).

   **Ongeveer `dismissal-date`:**

   * Optioneel veld met Unix epoche-tijd (seconden).
   * **slechts relevant wanneer`event: "end"`**.
   * Hiermee geeft u aan wanneer de actieve activiteit automatisch van het apparaat moet worden verwijderd.
   * Als deze optie niet wordt opgegeven bij de eindgebeurtenis, blijft Live-activiteit zichtbaar totdat de gebruiker deze verlaat.
   * Moet een toekomstig tijdstempel zijn (later dan `timestamp`).

     +++

1. 
   +++ Betalingsbelasting uitlijnen met iOS-implementatie

   Zorg ervoor dat de payload van uw API overeenkomt met de implementatie van uw iOS-app. `ActivityAttributes` Het Adobe SDK `LiveActivityAttributes` -protocol breidt iOS `ActivityAttributes` uit en vereist een `liveActivityData` -eigenschap.

   **bevestigt de afbeelding:**

   1. Uw `ActivityAttributes` moet het Adobe `LiveActivityAttributes` -protocol implementeren. Voorbeeld:

      ```swift
      struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
       public struct ContentState: Codable, Hashable {
           var orderStatus: String
           var estimatedDeliveryTime: String
       }
      
       // Adobe SDK requirement
       var liveActivityData: LiveActivityData
      
       // Your custom attributes
       var restaurantName: String
      }
      ```

      **Nota** dat het `liveActivityData` gebied door Adobe SDK wordt vereist en in alle implementaties moet worden omvat.

   1. Uw API-lading moet de iOS-structuur weerspiegelen:

      ```json
      {
        "aps": {
           "event": "start",
           "timestamp": 1756984054,
           "attributes-type": "FoodDeliveryLiveActivityAttributes",
           "content-state": {
           "orderStatus": "Preparing",
           "estimatedDeliveryTime": "20 mins"
        },
        "attributes": {
          "liveActivityData": {
            "liveActivityID": "order-12345"
          },
          "restaurantName": "Pizza Palace"
        }
        }
      }
      ```

   **checklist van de Bevestiging:**

   * Neem alle `ContentState` -velden op in `content-state` (vereist voor alle gebeurtenistypen).
   * Neem alle `LiveActivityAttributes` -velden op in `attributes` (alleen startgebeurtenissen), inclusief:
      * `liveActivityData` (vereist; bevat doorgaans `liveActivityID` of een vergelijkbare id)
      * Alle aangepaste velden uit uw structuur
   * Namen van velden exact overeenkomen (hoofdlettergevoelig).
   * Datatypen afstemmen (String, Int, Bool, geneste objecten).
   * Geneste objectstructuur behouden.

   **Gemeenschappelijke fouten:**

   | Probleem | Gevolgen | Repareren |
   |-------|--------|-----|
   | Ontbrekende `liveActivityData` kenmerken | Live-activiteit wordt niet gestart | Object `liveActivityData` altijd opnemen in gebeurtenis start |
   | Vereist veld ontbreekt in startgebeurtenis | Live-activiteit wordt niet gestart | Alle velden uit iOS-structuur toevoegen |
   | Onjuiste veldnaam (typefout/hoofdletter) | Veld genegeerd of parseerfout | IOS-veldnamen exact afstemmen |
   | Onjuist gegevenstype | Parseringsfout | Overeenkomstige iOS-gegevenstypen |
   | Ontbrekend genest object | Onvolledige gegevens | Alle geneste structuren opnemen |
   | `attributes` opnemen in update/end | Onnodig, maar meestal genegeerd | Alleen `attributes` instart-gebeurtenis opnemen |
   | Tijdstempel schalen bij bijwerken/beëindigen | Bijwerken/beëindigen genegeerd door apparaat | Altijd nieuwe tijdstempel genereren |

   Voor meer voorbeelden, verwijs naar [ creeer Actieve activiteitenpagina ](create-mobile-live.md).

   +++

1. 
   +++ Testen met Assurance

   Verifieer de uitvoering van de API en de levering van de lading met Assurance:

   1. Open je Assurance-sessie.
   1. Voer de API-aanroep uit om de Live-activiteit te activeren.
   1. In de **Lijst van de Gebeurtenis**, controleer voor:
      * Gebeurtenissen tijdens de uitvoering van de campagne.
      * Gebeurtenissen voor de levering van live-activiteiten.
      * Gebeurtenissen van de Payload-validatie.
   1. Controleren van de te controleren gebeurtenislading:
      * De lading is correct verwerkt.
      * Er zijn geen validatiefouten opgetreden.
      * Live activiteit is naar APNs verzonden.

      +++

### Leveringsfouten en foutenanalyse

[!BADGE  is op zowel eenheids als uitzendingsgebruiksgevallen ]{type=Positive} van toepassing

In dit scenario zijn alle vorige controles geslaagd:

* Het profiel bestaat met [ geldige Actieve tokens van de activiteitenduw ](#profile-issue)
* De campagne wordt correct [ gevormd met juiste nuttige lading ](#payload-issues)
* [ tokens van de Update worden gesynchroniseerd ](#token-not-synced) (voor update/eindgebeurtenissen, unitaire gebruikscase slechts)

De Live-activiteit wordt echter nog steeds niet weergegeven, bijgewerkt of beëindigd zoals u had verwacht. Het probleem kan zich voordoen op het niveau van het Adobe-leveringssysteem of bij de APNs (push notification service provider).

**Nota voor de gevallen van het uitzendingsgebruik**: De rapporten tonen metriek over alle publieksleden. Sommige profielen kunnen slagen terwijl andere ontbreken.

**pre-controles**

* **Vorige Gevalideerde Scenario&#39;s:**
   * Profiel bestaat met juist `liveActivityPushNotificationDetails`
   * Het campagneoppervlak en het type activiteit zijn correct
   * API-payload is geldig met huidige tijdstempel
   * Tkens voor updates worden gesynchroniseerd (voor update-/eindgebeurtenissen)

* **Bevestigde Vraag van API:**

   * De API-aanroep retourneerde HTTP 200 (geslaagd)
   * Campagne-id en de gegevens van de ontvanger zijn juist

#### Foutopsporingsstappen

1. 
   +++ Campagnerapporten controleren

   1. Navigeer aan uw **Levende activiteitenCampagne**.
   1. Klik de **knoop van Rapporten**.
   1. Selecteer **Mening al tijdrapport**.
   1. Bekijk de volgende secties:

      1. Controleer de **Verzendende Statistieken** metriek om leveringssucces te begrijpen:

         | Metrisch | Wat het betekent | Wat moet u zoeken? |
         |-|-|-|
         | Gericht | Aantal profielen dat is gekwalificeerd voor het publiek | Neem uw testprofiel op |
         | Verzenden | Totaal aantal geprobeerd pushmeldingen | Moet overeenkomen met uw API-aanroepen |
         | Afgeleverd | Aangeleverd aan apparaten | Vergelijk met Verzenden om succespercentage te zien |
         | Fouten verzenden | Push-berichten die niet zijn verzonden | Hoge getallen |
         | Uitsluitingen verzenden | Profielen die door Adobe Journey Optimizer zijn uitgesloten | Controleren of uw profiel is uitgesloten |

      1. Als verzend fouten > 0, controleer de **Lijst van de Redenen van de Fout** voor specifieke foutencodes en berichten:

         | Algemene fout | Betekenis | Resolutie |
         |-|-|-|
         | Ongeldig token | Push-token is ongeldig of verlopen | Tokens voor live-activiteiten opnieuw registreren vanaf apparaat |
         | Token niet gevonden | Geen geldig token gekoppeld aan profiel | Controleren of `liveActivityPushNotificationDetails` bestaat |
         | APN&#39;s afgewezen | Apple Push Notification service heeft pushmelding afgewezen | APNs-certificaat, bundle ID, omgeving controleren |
         | Time-out netwerk | Kan APNs niet bereiken | Voorbijgaande kwestie; probeer de API vraag opnieuw |

      1. Als **uitsluitingen** > 0 verzendt, controleer de **Uitgesloten lijst van Redenen**:

         | Algemene uitsluiting | Betekenis | Resolutie |
         |-|-|-|
         | Profiel is uitgeschakeld | Gebruiker heeft geen meldingen ontvangen | Status van profieltoestemming controleren |
         | Token gevoegd op lijst van gewenste personen | Token gemarkeerd als ongeldig | Token opnieuw registreren of de status van de lijst van gewezen personen controleren |
         | Profiel komt niet in aanmerking | Profiel voldoet niet aan campagnecriteria | De publieksregels van de campagne bekijken |

   Leer meer in de [ Levende pagina van het activiteitencampagnerapport ](../reports/campaign-global-report-cja-activity.md).

   +++

1. 
   +++ Feedbackgebeurtenissen voor berichten in profiel controleren

   1. Navigeer aan **Klant** > **Profielen** in Journey Optimizer.
   1. Zoek naar en open het profiel.
   1. Selecteer de **Gebeurtenissen** tabel.
   1. Filter of zoek naar gebeurtenissen met `eventType = "message.feedback"` .
   1. Zoek naar feedbackgebeurtenissen die overeenkomen met het type `liveActivityID` en `event` van uw Live-activiteit.
   1. Bekijk de volgende belangrijke velden:

      | Veld | Mogelijke waarden | Wat het betekent |
      |-|-|-|
      | `feedbackStatus` | `sent`, `error`, `denylist` | Resultaat van levering door serviceprovider |
      | `serviceProvider` | `apns/apnsSandbox` | Moet APN&#39;s zijn voor iOS Live-activiteiten |
      | `errorCode` | Numerieke code of `null` | APNs-specifieke foutcode indien mislukt |
      | `errorMessage` | Foutbeschrijving of `null` | Foutbericht voor leesbare tekst |

   1. **als `feedbackStatus: "error"`:**
      * Controleer `errorCode` en `errorMessage` op specifieke APNs fouten
      * Veelvoorkomende APNs-fouten zijn verlopen token, ongeldig certificaat, onjuiste bundel-id

   1. **als geen terugkoppel gebeurtenis vond:**
      * Het pushbericht is mogelijk niet geprobeerd
      * Controleer of het profiel is uitgesloten in campagnerapporten, zoals beschreven in stap 1 hierboven.

      +++

1. 
   +++ Levering van live-activiteiten aan APN&#39;s in Assurance controleren

   1. Open uw Assurance-sessie. Deze moet actief zijn tijdens de API-aanroep.
   1. Voer de API-aanroep uit (start, update of end).
   1. In de **Lijst van de Gebeurtenis**, zoek de Actieve gebeurtenissen van de activiteitenlevering.
   1. Zoeken naar gebeurtenissen die te maken hebben met APNs-push.
   1. Controleren op de volgende indicatoren:
      * **duw verzoek aan APNs**: Bevestigt Adobe verzendt de duw naar de servers van Apple
      * **APNs reactie**: Toont of APNs of de duw goedkeurde verworpen
      * **Status van de Levering**: De aanwijzing van het succes of van de mislukking
   1. Als er problemen worden gevonden, raadpleegt u de volgende algemene APNs-leveringsproblemen:

      | Probleem | Symptoom in Assurance | Resolutie |
      |-|-|-|
      | APNs-certificaat verlopen | Verificatiefout | Nieuw APN-certificaat vernieuwen en uploaden |
      | Verkeerde omgeving (dev vs prod) | Fout door token | Zorg ervoor dat het certificaat overeenkomt met het type App-build |
      | Bundel-id komt niet overeen | Ongeldige bundle-id | Identieke overeenkomende certificaatbundel-id verifiëren |
      | Token is verlopen | InvalidToken-fout van APNs | Tokens voor live-activiteiten opnieuw registreren |
      | Snelheidbeperking | Te veel verzoeken | API-aanroepfrequentie verminderen |

      +++

1. 
   +++ Ga door met aanvullende diagnostische controles

   1. Controleer de levenscyclusgegevens van de actieve activiteit in het campagnerapport.

      In het campagnerapport, herzie de **Levende sectie van de activiteitenlevenscyclus**:

      | Metrisch | Te controleren wat |
      |-|-|
      | Extern starten | Het aantal API-gestuurde start moet worden weergegeven |
      | Updates | Aantal updategebeurtenissen weergeven |
      | Eindigt | Aantal eindgebeurtenissen weergeven |
      | Aantal totalen | Totaal gebeurtenisvolume van Live-activiteit |

      Als deze cijfers nul zijn of niet overeenkomen met uw API-aanroepen, is er een leveringsprobleem tussen Adobe en APNs.

   1. Als Adobe een geslaagde levering weergeeft, maar het apparaat de Live-activiteit niet weergeeft:

      * Controleer iOS-apparaatlogboeken op fouten met Live-activiteit.
      * Controleer of de app op de voor- of achtergrond staat (niet is afgesloten).
      * Bevestig apparaat heeft netwerkconnectiviteit.
      * Test op meerdere apparaten om apparaatspecifieke problemen uit te sluiten.
      * Controleer of iOS-versie 16.1 of hoger is.

      +++

1. 
   +++ Doorverwijzing naar Adobe-ondersteuning

   Als u alle stappen hebt uitgevoerd en het probleem niet is opgelost, neemt u contact op met de klantenservice van Adobe via:

   **Vereiste informatie:**

   * Campagne-id en naam
   * Profielnaamruimte en -id
      * `liveActivityID` van API-payload
   * Tijdstempels van API-aanroepen
   * Screenshots van:
      * Campagnerapporten (verzenden van statistieken, oorzaken van fouten, uitgesloten redenen)
      * Profielgebeurtenissen (`liveActivity.updateToken`, `message.feedback`)
      * Assurance-sessie met leveringsgebeurtenissen
   * Volledige lading voor API-verzoek
   * APNs-certificaatdetails (vervaldatum, omgeving, bundel-id)

     +++

## Uniespecifieke scenario&#39;s

### Token voor update van actieve activiteiten is niet gesynchroniseerd{#token-not-synced}

De Live-activiteit wordt op het apparaat gestart, maar volgende `update` - of `end` API-aanroepen (die HTTP 200 retourneren) kunnen de Live-activiteit niet bijwerken of sluiten. Dit komt voor wanneer het **Levende teken van de activiteitenupdate** niet behoorlijk aan het systeem van Adobe wordt gesynchroniseerd.

**Begrijpend updatetokens**

Wanneer een Live-activiteit op een apparaat start, genereert iOS een unieke updatetoken voor die specifieke Live-activiteit-instantie. Dit token is vereist voor:

* Updates van de Live-activiteit verzenden
* Live activiteiten extern beëindigen

Elke instantie van Live-activiteit heeft een eigen unieke update-token. Adobe heeft dit token nodig om update- en end-gebeurtenissen te leveren.

**Verwacht gedrag**

Update- en end-gebeurtenissen werken alleen als het volgende plaatsvindt:

1. Live-activiteit wordt op het apparaat gestart.
1. Apparaat genereert een updatetoken voor die Live-activiteit-instantie.
1. Mobile SDK legt de updatetoken vast en stuurt deze naar Adobe.
1. Het updatetoken wordt gesynchroniseerd en opgeslagen in het Adobe-systeem.
1. Volgende API-aanroepen voor bijwerken/beëindigen gebruiken dit token voor levering.

**pre-controles:**

* **Toestemming van de Gebruiker**: De eerste keer een Levende activiteit begint op een apparaat, toont iOS een systeemherinnering: &quot;Toestaan [ Naam van de App ] om Actieve activiteitenupdates te verstrekken?&quot; De gebruiker **moet &quot;toestaan&quot;tikken** voor updatetokens om worden geproduceerd en worden gesynchroniseerd. Als de gebruiker op &quot;Niet toestaan&quot; tikt, worden geen updatetokens gemaakt en mislukken de update-/eindaanvragen. Dit is een eenmalige machtiging per app.
* **Bevestiging van het Profiel en van de Campagne**: Volledige [ Scenario 1 ](#profile-issue) en [ Scenario 2 ](#payload-issues) controles om profiel, tekenen, en campagneconfiguratie te verzekeren zijn correct.

#### Foutopsporingsstappen

1. 
   +++ Synchronisatie van updatetoken verifiëren in Assurance

   1. Open je Assurance-sessie.
   1. Zorg ervoor dat de sessie actief was toen de Live-activiteit op het apparaat werd gestart.
   1. Filter of zoek naar gebeurtenissen met `eventType = "liveActivity.updateToken"` .
   1. Selecteer de gebeurtenis en controleer de lading:

      * Controleer of het veld `token` een geldige token-tekenreeks voor updates bevat.
      * Controleer of de `liveActivityID` overeenkomt met uw Live activity-instantie.
      * Bevestig dat de `activityType` overeenkomen met uw `attributes-type` .

   1. Als de gebeurtenis niet wordt gevonden:

      * Het updatetoken is niet gegenereerd of vastgelegd door de SDK.
      * Controleer of de gebruiker Live-activiteitmachtigingen heeft verleend.
      * Controleer of Live-activiteit correct op het apparaat is gestart.
      * Controleer of de mobiele SDK correct is geïntegreerd om updatetokens vast te leggen.

   1. Ga door met Stap 2 als een gebeurtenis wordt gevonden.

      +++

2. 
   +++ Update-token verifiëren bij profielgebeurtenissen

   1. Navigeer aan **Klant** > **Profielen** in Journey Optimizer.
   1. Zoek naar en open het profiel.
   1. Selecteer de **Gebeurtenissen** tabel.
   1. Zoek naar `liveActivity.updateToken` -gebeurtenissen.
   1. Controleer de gebeurtenisdetails:

      * Controleer of de tijdstempel recent is (komt overeen met het moment dat Live-activiteit is gestart).
      * Bevestig dat `token` en `liveActivityID` aanwezig zijn.
      * Controleer of `activityType` juist is.

   1. Als de gebeurtenis niet wordt gevonden in profiel:

      * Het is mogelijk dat de update-token-gebeurtenis nog niet aan het profiel is toegevoegd.
      * Wacht 5-10 minuten en controleer het opnieuw.
      * Als er na 15 minuten nog steeds een fout optreedt bij het opnemen van de gebeurtenis.

   1. Als er een gebeurtenis wordt gevonden, is het updatetoken gesynchroniseerd. U kunt doorgaan naar stap 3.

      +++

3. 
   +++ Live activity-leveringsgebeurtenissen in Assurance controleren

   1. Voer in uw Assurance-sessie een update uit of sluit een API-aanroep af.
   1. In de **Lijst van de Gebeurtenis**, zoek de Actieve gebeurtenissen van de activiteitenlevering (APNs duw gebeurtenissen).
   1. Controleren op gebeurtenissen die aangeven:
      * Pushmelding verzonden naar APNs.
      * Reactie van APNs (succes of fout).
      * Bevestiging van levering.
   1. Als APNs leveringsgebeurtenis aanwezig is: De pushmelding is verzonden. Als het apparaat nog steeds niet wordt bijgewerkt, bevindt het probleem zich mogelijk aan de apparaatzijde (toepassing die de push niet afhandelt, netwerkproblemen enzovoort).
   1. Als APNs-gebeurtenis voor levering ontbreekt: Het updatetoken wordt mogelijk niet correct opgeslagen of gekoppeld aan het profiel in het Adobe-systeem.
   1. Als er foutgebeurtenissen aanwezig zijn: controleer de foutdetails om specifieke mislukkingsredenen (ongeldige token, APNs afgewezen, enz.).

      +++

## Uitzendspecifieke scenario&#39;s

### Configuratie van de campagne voor uitzending en problemen met de lading{#broadcast-config}

Deze sectie behandelt het oplossen van problemenscenario&#39;s specifiek om Live activiteiten uit te zenden, die verschillende het zuiveren benaderingen dan eenheidscampagnes vereisen.

Als profielen geldige tokens hebben maar de Live-activiteit niet wordt weergegeven, bijgewerkt of zich niet naar behoren gedraagt voor publieksleden, is de uitgave doorgaans het resultaat van een van de volgende:

* De campagne is niet geconfigureerd als API-getriggerde marketing.
* De API-payload gebruikt een onjuiste uitzendstructuur (ontbreekt `audience` of `input-push-channel` ).
* De velden `content-state` en `attributes` komen niet overeen met de iOS `ActivityAttributes` -implementatie.
* `input-push-channel` is niet correct gemaakt op de Apple Developer Portal.

Dit scenario voor het oplossen van problemen is van toepassing op alle gebeurtenissen Live-activiteit in uitzendingscampagnes: `start`, `update` en `end` .

**pre-controles:**

* **Type van Campagne**:
   * Verifieer dat de campagne als API-teweeggebrachte Marketing (die voor uitzending/op publiek-gebaseerde campagnes wordt vereist) wordt gecreeerd.
   * Bevestig dat een publiek in de campagneconfiguratie wordt bepaald.
* **Profiel en Symbolische Bevestiging**: Steek veelvoudige profielen van het publiek om te verifiëren zij geldig `liveActivityPushNotificationDetails` hebben. Voor gedetailleerde bevestigingsstappen, volg [ Scenario 1 ](#profile-issue).

#### Foutopsporingsstappen

1. 
   +++ Configuratie voor publiek campagne controleren

   1. Open uw **API teweeggebrachte de Marketing Campagne van de Marketing** in Journey Optimizer.
   1. Navigeer aan de **sectie van het publiek** en verifieer:
      * Er is een publiek geselecteerd voor de campagne.
      * De gebruikers-id komt overeen met de id die wordt gebruikt in uw API-payload.
      * Het publiek bevat de verwachte profielen.
   1. Navigeer aan de **sectie van Acties**.
   1. Controleer de **Levende activiteitenconfiguratie**:
      * De configuratie moet worden ingesteld voor de iOS-toepassing met de juiste bundle-id.
      * Het type Activiteit moet overeenkomen met `attributes-type` in uw API-payload. Als uw lading bijvoorbeeld `"attributes-type": "AirplaneTrackingAttributes"` bevat, moet de campagne dit zelfde type van Activiteit specificeren.

      +++

1. 
   +++ Payloadstructuur van uitzendings-API valideren

   De structuur van de uitzendingslading verschilt van eenheidscampagnes. Verifieer dat uw lading het correcte uitzendingsformaat volgt.

   **Vereiste gebieden voor uitzending:**

   ```json
   {
     "campaignId": "878a11d4-b519-47bd-8313-fecfee19857b",
     "audience": {
       "id": "8c3dbdea-2957-401f-acf0-3966fba1601e"
     },
     "context": {
       "requestPayload": {
         "aps": {
           "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
           "content-available": 1,
           "timestamp": 1771829292,
           "event": "update",
           "attributes-type": "AirplaneTrackingAttributes",
           "content-state": { ... },
           "attributes": { ... }
         }
       }
     }
   }
   ```

   **Gemeenschappelijke payload kwesties:**

   | Veld | Vereiste | Vaak probleem |
   |-|-|-|
   | `campaignId` | Moet overeenkomen met de geactiveerde marketingcampagne-id | Onjuiste campagne-id of Transactionele campagne gebruiken |
   | `audience.id` | Moet overeenkomen met een bestaand publiek in AEP | Onjuiste publiek-id of publiek bestaat niet |
   | `input-push-channel` | Vereist voor uitzending - Unieke id voor deze uitgezonden instantie | Ontbreekt of komt niet overeen met `channelID` in `liveActivityData` |
   | `timestamp` | Moet altijd de huidige/laatste Unix-tijdperktijd in seconden zijn | Tijdstempel gebruiken in oude cache |
   | `event` | Moet `"start"`, `"update"` of `"end"` zijn | Ongeldig gebeurtenistype |
   | `attributes-type` | Moet overeenkomen met het type campagneactiviteit | Verkeerd of typefout |
   | `content-available` | Moet zijn `1` | Ontbrekende of onjuiste waarde |

   **Kritieke uitzending-specifieke gebieden:**

   * **`input-push-channel`** :
      * Vereist voor alle uitzendingen Live activiteiten.
      * Fungeert als een unieke id voor deze specifieke uitzendingsinstantie.
      * Alle profielen in het publiek ontvangen Live-activiteiten die aan dit kanaal zijn gekoppeld.
      * Moet overeenkomen met `channelID` in `liveActivityData.channelID` (zie Stap 3).
      * Moet door de client worden gemaakt voor de `appID` op de Apple Developer Portal.
      * Alleen kanalen die voor de specifieke `appID` zijn gemaakt, kunnen worden gebruikt voor het uitzenden van Live-activiteiten op die app.

   * **`audience.id`**:
      * Moet verwijzen naar een geldig publiekssegment dat in Adobe Experience Platform is gemaakt.
      * Alle profielen in dit publiek zijn gericht op Live-activiteit.
      * Het publiek moet worden geactiveerd en profielen met geldige waarden bevatten `liveActivityPushNotificationDetails` .

   **altijd gebruik recentste timestamp:**

   * Het veld `timestamp` moet voor elke API-aanroep altijd de huidige Unix-epoche-tijd (in seconden) zijn.
   * Deze vereiste geldt voor alle gebeurtenistypen: `start` , `update` en `end` .
   * **Kritiek voor updates/eind**: Het gebruiken van stapeltimestamps veroorzaakt update en eindverzoeken om te ontbreken.
   * Genereer een nieuwe tijdstempel voor elke API-oproep voor uitzending.

   **Facultatieve gebieden:**

   * `dismissal-date`: Unix tijdperk voor automatisch ontslag (alleen relevant voor `end` -gebeurtenissen)
   * `alert`: Object met `title` en `body` voor melding

   Verwijs naar de [ documentatie van API van het Overseinen van Adobe Journey Optimizer ](https://developer.adobe.com/journey-optimizer-apis/references/messaging) voor volledige API specificaties.

   +++

1. 
   +++ Inhoudsstatus, kenmerken en invoerpushkanaal uitlijnen met iOS-implementatie

   Zorg ervoor dat de payload-velden overeenkomen met de `ActivityAttributes` -implementatie van uw iOS-app en dat de `input-push-channel` overeenkomt met de `channelID` in `liveActivityData` .

   1. Bekijk de definitie van iOS ActivityAttributes.

   Uw aangepaste `ActivityAttributes` struct moet het Adobe `LiveActivityAttributes` -protocol implementeren:

   ```swift
   struct AirplaneTrackingAttributes: LiveActivityAttributes {
    public struct ContentState: Codable, Hashable {
        var journeyProgress: Int
    }
   
    // Adobe SDK requirement
    var liveActivityData: LiveActivityData
   
    // Your custom attributes
    var arrivalAirport: String
    var departureAirport: String
    var arrivalTerminal: String
   }
   ```

   1. Wijs iOS-velden toe aan de uitzending van de API.

   Neem voor alle gebeurtenissen zowel `attributes` als `content-state` op:

   ```json
         {
         "aps": {
          "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
          "event": "start",
          "timestamp": 1771829292,
          "attributes-type": "AirplaneTrackingAttributes",
          "content-state": {
            "journeyProgress": 0
          },
          "attributes": {
            "arrivalAirport": "DEL",
            "departureAirport": "MUM",
            "arrivalTerminal": "T1",
            "liveActivityData": {
              "channelID": "FEt0NgvLEfEAAOqA6AXdIQ=="
            }
          }
         }
         }
   ```

   **Kritiek: `input-push-channel` moet`channelID`** aanpassen

   * De `input-push-channel` -waarde in de hoofdmap van `aps` moet exact overeenkomen met de `channelID` in `liveActivityData` .
   * In het bovenstaande voorbeeld zijn beide waarden `"FEt0NgvLEfEAAOqA6AXdIQ=="` .
   * Deze overeenkomst koppelt de uitzendingsinstantie aan de Levende activiteitengegevens.
   * Bij een onjuiste overeenkomst treden leveringsfouten op.

   **Zeer belangrijke bevestigingspunten:**

   * Neem alle `ContentState` -velden op in `content-state` voor alle gebeurtenistypen.
   * Neem alleen voor startgebeurtenissen alle aangepaste `LiveActivityAttributes` velden in `attributes` op.
   * Voor start-gebeurtenissen moet `liveActivityData.channelID` overeenkomen met `input-push-channel` .
   * Veldnamen zijn hoofdlettergevoelig en moeten exact overeenkomen.
   * De gegevenstypen moeten overeenkomen (String, Int, Bool, geneste objecten, enz.).
   * Voor update-/end-gebeurtenissen gebruikt u dezelfde `input-push-channel` als de oorspronkelijke start-gebeurtenis.

   **Gemeenschappelijke fouten:**

   | Probleem | Gevolgen | Repareren |
   |-|-|-|
   | Ontbrekend `input-push-channel` | Uitzenden werkt niet | Unieke kanaal-id toevoegen voor elke uitzending |
   | `input-push-channel` komt niet overeen met `channelID` | Live-activiteit wordt niet gestart | Zorg ervoor dat beide waarden identiek zijn |
   | Verschil `input-push-channel` voor bijwerken/beëindigen | Update/end bereikt de Live-activiteiten niet | Dezelfde kanaal-id gebruiken gedurende de hele levenscyclus |
   | Ontbrekend `liveActivityData.channelID` | Live-activiteiten zijn niet gekoppeld aan uitzenden | `channelID` opnemen in kenmerken voor startgebeurtenis |
   | Vereist veld ontbreekt in startgebeurtenis | Live-activiteit wordt niet gestart | Alle velden uit iOS-structuur toevoegen |
   | Onjuiste veldnaam (typefout/hoofdletter) | Veld genegeerd of parseerfout | IOS-veldnamen exact afstemmen |
   | Tijdstempel schalen bij bijwerken/beëindigen | Bijwerken/beëindigen genegeerd door apparaten | Altijd nieuwe tijdstempel genereren |

   +++

1. 
   +++ Testen met Assurance

   Verifieer de uitvoering van de API en de levering van de lading met Assurance:

   1. Open uw Assurance-sessie op een testapparaat dat deel uitmaakt van het publiek.
   1. Voer de uitzending API vraag uit.
   1. In de **Lijst van de Gebeurtenis**, zoek:
      * Gebeurtenissen tijdens de uitvoering van de campagne.
      * Gebeurtenissen voor de levering van live-activiteiten.
      * Foutgebeurtenissen die mislukte payload-validatie aangeven.
   1. Inspecteer gebeurtenisladingen om te bevestigen:
      * De lading is correct verwerkt.
      * De lus `input-push-channel` is aanwezig.
      * Er zijn geen validatiefouten opgetreden.
      * Live-activiteiten zijn naar APN&#39;s verzonden voor publieksleden.

      +++

### Profiel niet in publieksopname of opname van een vergelijkbaar publiek

In dit scenario worden de campagne en de lading correct gevormd, maar de specifieke profielen ontvangen niet de Levende activiteit. Dit gebeurt gewoonlijk wanneer:

* Het profiel is geen lid van het publiek dat aan de campagne is gekoppeld.
* Het publiek is een batchpubliek en bevat een verouderde momentopname van profielgegevens.
* De tokens voor live-activiteiten van het profiel zijn onlangs toegevoegd, maar zijn nog niet weerspiegeld in de opname van het publiek.

Dit het oplossen van problemenscenario is specifiek op uitzendingscampagnes gebruikend op publiek-gebaseerd richten van toepassing.

**Begrijpend publieksevaluatie**

Adobe Experience Platform gebruikt verschillende methoden voor publieksevaluatie die bepalen wanneer profielupdates in het publiek worden weerspiegeld:

| Methode | Evaluatiefrequentie | Gegevensversheid | Best voor |
|-|-|-|--|
| Batch | Eenmaal daags (gepland) | Mag maximaal 24 uur houdbaar zijn | Groot publiek, niet-tijdgevoelig |
| Streaming | In real time (op profielveranderingen) | Bijna real-time voor bijgewerkte profielen | Tijdgevoelig, vereist profielupdates |

**pre-controles:**

* **Campagne en Bevestiging van de Lading**:
   * Voltooi de controles in [ dit scenario ](#broadcast-config) om de campagne en de lading te verzekeren correct zijn.
   * Controleer of de `audience.id` in de API-payload overeenkomt met de configuratie van de campagne.
* **Profiel bestaat**: Bevestig dat het profiel in AEP met geldig `liveActivityPushNotificationDetails` bestaat.

#### Foutopsporingsstappen

1. 
   +++ Controleren of het profiel in het publiek aanwezig is

   Bevestig eerst of het profiel dat de Live-activiteit moet ontvangen, daadwerkelijk deel uitmaakt van het publiek.

   1. Navigeer aan **Soorten publiek** in Adobe Experience Platform.
   1. Zoek naar en open het publiek gebruikend `audience.id` van uw campagne.
   1. Klik **doorbladeren** of **profielen van de Steekproef** om publieksleden te bekijken.
   1. Zoek naar uw testprofiel gebruikend namespace en identiteitswaarde.
   1. **als het profiel niet in het publiek wordt gevonden:**
      * Het profiel voldoet niet aan de publiekscriteria of segmentregels.
      * Bekijk de publieksdefinitie om inzicht te krijgen in de lidmaatschapsvereisten.
      * Werk de profielgegevens of publieksdefinitie bij om het profiel op te nemen.
      * Wacht op publieksevaluatie om te voltooien (zie Stap 2).
   1. **als het profiel in het publiek wordt gevonden:** ga aan Stap 2 te werk om gegevensversheid te controleren.

      +++

2. 
   +++ Type en planning van publieksevaluatie controleren

   Identificeer of het publiek batch- of streaming evaluatie gebruikt, aangezien dit gegevensversheid bepaalt.

   1. Op de **pagina van de Details van het publiek**, controleer de **methode van de Evaluatie**:
      * **Partij**: Evalueerde eens per dag op een programma.
      * **Streaming**: die in real time wordt geëvalueerd wanneer de profielupdates voorkomen.
      * **Edge**: Evaluated bij randplaatsen in real time.

   Volg de aangewezen die het oplossen van problemenstappen op de evaluatiemethode worden gebaseerd:

   **als het publiek de evaluatie van de Partij gebruikt:**

   1. **begrijp de beperkingen van het partijpubliek:**
      * Het batchpubliek wordt eenmaal per dag geëvalueerd (doorgaans &#39;s nachts).
      * De momentopname van het publiek kan tot 24 uur oud zijn.
      * Als een profiel onlangs geregistreerde Levende activiteitentekenen, kunnen die tokens niet in de huidige momentopname zijn.
      * Updates voor profielen worden pas in de volgende batchevaluatie weergegeven.

   1. **Controle toen laatste evaluatie voorkwam:**
      * In de publieksdetails, zoek **Laatste evaluatie** timestamp.
      * Als het profiel `liveActivityPushNotificationDetails` na deze tijdstempel is bijgewerkt, heeft het publiek vaste gegevens.

   1. **los stale gegevens op:**
      1. **Optie 1: Wacht op geplande partijevaluatie**
         * De volgende batchevaluatie bevat de bijgewerkte profielgegevens.
         * Dit gebeurt automatisch eenmaal per dag.
         * Het beste voor niet-dringende scenario&#39;s.

      1. **Optie 2: Trigger op bestelling publieksevaluatie**
         1. Navigeer aan **Soorten publiek** in AEP.
         1. Selecteer uw publiek.
         1. Klik **evalueer nu** of **activeer op bestelling**.
         1. Wacht tot de evaluatie is voltooid (dit kan enkele minuten tot uren duren, afhankelijk van de grootte van het publiek).
         1. Controleer of het profiel nu bijgewerkte gegevens bevat in de momentopname van het publiek.
         1. Probeer de API-aanroep van de uitzending opnieuw.

   **als het publiek het Streamen evaluatie gebruikt:**

   1. **Begrijp het stromen publieksgedrag:**
      * Streaming publiek wordt in realtime geëvalueerd wanneer profielupdates plaatsvinden.
      * **Nieuwe profielen**: Kwalificeer kort na verwezenlijking als zij segmentcriteria voldoen.
      * **Bijgewerkte profielen**: Kwalificeer of diskwalificeer kort na wordt bijgewerkt.
      * **Bestaande ongewijzigde profielen**: Zijn niet hergeëvalueerd tenzij een update voorkomt.

   1. **identificeer de kwestie:**
      * Als een profiel al bestaat en aan de segmentcriteria voldoet, maar er vindt geen update voor dat profiel plaats, wordt het mogelijk niet toegevoegd aan een nieuw gemaakt streaming publiek.
      * Het profiel moet een update (elke wijziging in kenmerken) ontvangen om herevaluatie te starten.

   1. **los de kwestie op:**
      * **voor nieuwe profielen**: Zij kwalificeren automatisch als de criteria worden voldaan aan. Geen actie nodig.
      * **voor bestaande profielen zonder recente updates:**
         * Een kleine update van het profiel uitvoeren (bijvoorbeeld een tijdstempelveld bijwerken).
         * Dit activeert het stromen evaluatie en voegt het profiel aan het publiek toe.
         * Alternatief: gebruik een batchpubliek of een randpubliek voor bestaande profielen.

      +++
