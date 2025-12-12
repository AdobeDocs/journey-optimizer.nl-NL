---
title: Aan de slag voor ontwikkelaars
description: Als ontwikkelaar leert u hoe u met Journey Optimizer kunt werken
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: ed3246d0bd552fee9c4df01babe18a5c1acd3b5f
workflow-type: tm+mt
source-wordcount: '1886'
ht-degree: 0%

---

# Aan de slag voor ontwikkelaars {#get-started-developers}

Als a **Ontwikkelaar**, bent u verantwoordelijk voor het uitvoeren van en het integreren van [!DNL Adobe Journey Optimizer] in uw toepassingen en systemen. U kunt beginnen met [!DNL Adobe Journey Optimizer] te werken zodra de [ Beheerder van het Systeem ](administrator.md) en de [ Ingenieur van Gegevens ](data-engineer.md) u toegang hebben verleend en uw milieu hebben voorbereid.

## Uw rol in het ecosysteem van Journey Optimizer

Terwijl andere teamleden Journey Optimizer configureren via de gebruikersinterface, richt u zich op:

* **Uitvoerend SDKs** in mobiele en Webtoepassingen
* **Verzendende gebeurtenissen** van uw toepassingen om reizen teweeg te brengen
* **bouw API eindpunten** die Journey Optimizer via douaneacties kan roepen
* **Integrerend** Journey Optimizer met uw bestaande systemen en infrastructuur
* **het Testen en het zuiveren** uw implementaties

Uw [ Ingenieur van Gegevens ](data-engineer.md) zal gegevensschema&#39;s, gebeurtenisconfiguraties, en gegevensbronnen behandelen. Uw [ Beheerder ](administrator.md) zal opstellingstoestemmingen en kanaalconfiguraties. [ Marketers ](marketer.md) zullen de reizen en de inhoud ontwerpen die uw implementaties gebruiken.

In deze handleiding worden de belangrijkste stappen besproken die nodig zijn om u op weg te helpen met Journey Optimizer. Of u nu mobiele apps, webervaringen of API-integratie ontwikkelt, volg de onderstaande secties om uw implementatie in te stellen.

## Vereisten {#prerequisites}

Voordat u met de implementatie begint, moet u controleren of:

| Categorie | Vereisten |
|----------|-------------|
| **Technische vaardigheden** | * Ervaring met JavaScript (voor het Web SDK) of Swift/Kotlin (voor Mobiele SDK) <br>* Begrip van RESTful APIs en JSON <br>* Familiariteit met asynchrone programmering en gebeurtenis-gedreven architectuur <br>* Kennis van de de toepassingsarchitectuur van uw organisatie |
| **Toegang en hulpmiddelen** | * Toegang tot [ Adobe Developer Console ](https://developer.adobe.com){target="_blank"} voor API geloofsbrieven <br>* het milieu van de Ontwikkeling met toegang tot codebase van uw toepassing <br>* het Testen hulpmiddelen zoals Postman voor API het testen <br>* Browser ontwikkelaarshulpmiddelen of mobiele het zuiveren hulpmiddelen |
| **van andere teamleden** | * De toegang van het milieu die door uw [ wordt verleend beheerder ](administrator.md)<br>* XDM schema&#39;s en gebeurtenisdefinities van uw [ Ingenieur van Gegevens ](data-engineer.md)<br>* Vereisten en gebruiksgevallen van uw [ Marketers ](marketer.md) |

## De technische basis begrijpen {#technical-foundation}

Voordat u de implementatie ingaat, moet u zich vertrouwd maken met de belangrijkste technische concepten:

1. **de integratie van Adobe Experience Platform**: Journey Optimizer wordt gebouwd native op Adobe Experience Platform. Kennis van de onderliggende architectuur helpt u effectievere implementaties te maken. Leer meer over [ hoe Journey Optimizer ](../understanding-ajo.md) werkt.

1. **XDM gegevensmodellen**: Journey Optimizer gebruikt het Model van Gegevens van de Ervaring (XDM) om gebeurtenis en profielgegevens te structureren. Als ontwikkelaar, zult u moeten begrijpen hoe te om gegevens te verzenden die aan de schema&#39;s in overeenstemming zijn die door uw [ Ingenieur van Gegevens ](data-engineer.md) worden gevormd. Leer over [ schema&#39;s XDM ](../../data/get-started-schemas.md).

1. **Authentificatie en veiligheid**: Alle implementaties vereisen juiste authentificatie. Begrijp hoe te opstellingsauthentificatie voor SDKs en APIs. Leer over [ API authentificatie ](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Integratie van mobiele apps instellen {#mobile-integration}

### Adobe Experience Platform Mobile SDK configureren

Als u pushberichten, in-app berichten en andere mobiele mogelijkheden wilt inschakelen, integreert u de Adobe Experience Platform Mobile SDK in uw mobiele toepassingen.

1. **installeer en vorm Mobiele SDK**: Volg de [ Mobiele documentatie van SDK van Adobe Experience Platform ](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"} om met de integratie van SDK begonnen te worden.

1. **creeer een mobiel bezit**: Opstelling een mobiel bezit in [!DNL Adobe Experience Platform Data Collection]. Leer hoe te [ tot stand brengen en een mobiel bezit ](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"} vormen.

1. **vorm dupberichten**:
   * Voor **iOS apps**: Registreer uw app met APNs (de dienst van het Bericht van de Duw van Apple). Leer meer in [ documentatie van Apple ](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Voor **Android apps**: De Overseinen van de Wolk van de opstelling van de Vuurstand voor uw Android app. Leer meer in [ documentatie van Google ](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Test uw mobiele integratie**: Gebruik [ mobiel op het instappen snel beginwerkschema ](../../push/mobile-onboarding-wf.md) om uw mobiele opstelling snel te vormen en te testen.

De gedetailleerde stappen om dupberichten te vormen zijn beschikbaar op [ deze pagina ](../../push/push-configuration.md).

### Op code gebaseerde ervaringen implementeren (Mobile SDK)

Voor systeemeigen mobiele app-personalisatie met gebruik van op code gebaseerde ervaringen:

* Volg [ dit leerprogramma ](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} voor de Mobiele implementatie van SDK
* De steekproefimplementaties van het overzicht voor [ iOS ](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} en [ Android ](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Webervaringen implementeren {#web-implementation}

### Adobe Experience Platform Web SDK instellen

Voor web-based implementaties, is het Web SDK uw belangrijkste integratiepunt:

1. **installeer het Web SDK**: Volg de [ de implementatiegids van SDK van het Web ](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"} aan opstelling SDK op uw website.

1. **vorm gegevensstromen**: creeer en vorm een gegevensstroom in [!DNL Adobe Experience Platform Data Collection] met toegelaten Journey Optimizer. Leer meer in de [ documentatie van gegevensstromen ](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target="_blank"}.

1. **laat Web pushberichten** (facultatief) toe: Vorm het [ pushNotifications bezit ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} in uw configuratie van SDK van het Web en gebruik het [ sendPushSubscription bevel ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} om dupabonnementen te registreren.

### Implementeer op code gebaseerde ervaringen (Web SDK)

Met codegebaseerde ervaringen kunt u elk digitaal aanraakpunt aanpassen:

1. **kies uw implementatiemethode**: Cliënt-kant, server-kant, of hybride. Herzie [ implementatiemonsters ](../../code-based/code-based-implementation-samples.md) voor elke benadering.

1. **bepaalt oppervlakten**: Identificeer de plaatsen in uw toepassing waar u gepersonaliseerde inhoud wilt leveren. Leer over [ oppervlakteconfiguratie ](../../code-based/code-based-surface.md).

1. **voert inhoud uit die** teruggeeft: Gebruik SDK van het Web om verpersoonlijkingsinhoud te halen en toe te passen. Zie [ code-gebaseerde implementatieleerprogramma&#39;s ](../../code-based/code-based-decisioning-implementations.md).

1. **verzendt vertoning en interactiegebeurtenissen**: Spoor wanneer de inhoud wordt getoond en wanneer de gebruikers met het voor analyse en optimalisering in wisselwerking staan.

Onderzoek [ steekproefimplementaties op GitHub ](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} om code-gebaseerde ervaringen in actie te zien.

Leer meer over [ begonnen worden met code-gebaseerde ervaringen ](../../code-based/get-started-code-based.md).

## Gebeurtenisstreaming implementeren {#event-streaming}

### Gebeurtenissen verzenden om reizen te activeren

Als ontwikkelaar, zult u de code uitvoeren om gebeurtenissen te verzenden die reizen teweegbrengen. Uw [ Ingenieur van Gegevens ](data-engineer.md) zal de gebeurtenisschema&#39;s en definities in Journey Optimizer vormen.

1. **begrijp de gebeurtenislading**: Het werk met uw Ingenieur van Gegevens om het gebeurtenisschema en de vereiste loonlaststructuur te krijgen. De nuttige lading moet met het XDM schema in overeenstemming zijn zij hebben gevormd. Leer over [ vereisten van het gebeurtenisschema ](../../event/experience-event-schema.md).

1. **voer gebeurtenis het stromen uit**: Verzend gebeurtenissen naar Adobe Experience Platform gebruikend [ Streaming Ingestie APIs ](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=nl){target="_blank"}. Leer de [ stappen om gebeurtenissen ](../../event/additional-steps-to-send-events-to-journey.md) te verzenden.

1. **de gebeurtenistypen van de Handle**:
   * **Eenheid gebeurtenissen**: Voer gebeurtenis uit die voor persoon-specifieke acties (b.v., knoop klikt, aankoopvoltooiing) verzendt
   * **Bedrijfs gebeurtenissen**: Verzend zaken-verwante gebeurtenissen (b.v., inventarisupdates, prijsveranderingen)

1. **de gebeurtenislevering van de Test**: Verifieer dat de gebeurtenissen behoorlijk ontvangen zijn en reizen zoals verwacht teweegbrengen. Leer over [ gebeurtenis het oplossen van problemen ](../../building-journeys/troubleshooting-inbound.md).

**implementatie van het Voorbeeld** voor het verzenden van een gebeurtenis via API:

```javascript
POST https://{DATACOLLECTION_ENDPOINT}/collection/{DATASTREAM_ID}
Content-Type: application/json

{
  "header": {
    "datasetId": "{DATASET_ID}",
    "imsOrgId": "{ORG_ID}",
    "source": {
      "name": "Web SDK"
    }
  },
  "body": {
    "xdmMeta": {
      "schemaRef": {
        "id": "{SCHEMA_ID}"
      }
    },
    "xdmEntity": {
      "_id": "unique-event-id",
      "eventType": "purchase",
      "timestamp": "2024-01-01T12:00:00Z",
      // ... your event data
    }
  }
}
```

Leer meer over [ het werken met reisgebeurtenissen ](../../event/about-events.md).

## Eindpunten van aangepaste handelingen ontwikkelen {#custom-actions}

Met aangepaste handelingen kunnen reizen uw API&#39;s bellen. Als ontwikkelaar gaat u de API-eindpunten maken die door aangepaste handelingen worden aangeroepen:

1. **bouwt uw API eindpunt**: Creeer RESTful API eindpunten die Journey Optimizer tijdens reisuitvoering zal roepen. Uw eindpunt moet:
   * JSON-payloads accepteren
   * Verzoeken verifiëren (OAuth, API-sleutel of JWT)
   * Verzoeken om verwerking binnen passende tijdslimieten
   * Reacties retourneren in de verwachte indeling

1. **Begrijp de mogelijkheden van de douaneactie**: De acties van de douane kunnen met derdesystemen zoals Epsilon, Slack, Vuurbasis, of uw eigen diensten verbinden. Leer meer over [ douaneacties ](../../action/action.md).

1. **Werk met actieconfiguraties**: Uw [ Beheerder ](administrator.md) of [ Ingenieur van Gegevens ](data-engineer.md) zal de douaneactie in Journey Optimizer vormen, bepalend het API eindpunt URL, authentificatiemethode, en parameters. U geeft hen uw API-specificatie. Leer over [ configuratie van de douaneactie ](../../action/about-custom-action-configuration.md).

1. **de actiefgegevens van de Terugkeer**: Ontwerp uw API om gegevens terug te keren die in verdere reisstappen kunnen worden gebruikt. Leer over [ actiereacties ](../../action/action-response.md).

1. **voert het beperken van** uit: Zorg uw eindpunten het verwachte volume kunnen behandelen. Journey Optimizer past een limiet van 5000 aanroepen per seconde toe, maar uw systeem moet veerkrachtig zijn. Leer over [ het in kaart brengen en het vertragen ](../../configuration/external-systems.md).

**het gebruiksgeval van het Voorbeeld**: [ schrijvend reisgebeurtenissen aan Experience Platform ](../../building-journeys/custom-action-aep.md) gebruikend douaneacties.

## Werken met Journey Optimizer API&#39;s {#apis}

Journey Optimizer biedt uitgebreide REST API&#39;s voor programmatische toegang:

1. **Begrijp API mogelijkheden**: Journey Optimizer APIs staat u toe om, diverse middelen programmatically tot stand te brengen te lezen bij te werken en te schrappen. Leer over [ Journey Optimizer APIs ](../../configuration/ajo-apis.md).

1. **Authentificatie**: Volg [ dit leerprogramma ](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} aan opstelling API authentificatie gebruikend Adobe Developer Console.

1. **onderzoek API verwijzingen**: Doorblader de volledige API documentatie en probeer direct APIs in de [ verwijzing van Adobe Journey Optimizer API ](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

1. **API-teweeggebrachte campagnes**: Bouw transactioneel overseinen met API-teweeggebrachte campagnes. Voor high-volume scenario&#39;s (tot 5000 TPS), onderzoek [ Hoge wijze van de Output ](../../campaigns/api-triggered-high-throughput.md) (vereist vergunning toe:voegen-op).

1. **Beheer APIs van het Besluit**: Gebruik gespecialiseerde APIs voor aanbiedingsbeheer en besluitvorming. Leer meer in de [ gids van het Beheer API van het Besluit ](../../offers/api-reference/getting-started.md).

## Testen en fouten opsporen {#testing}

1. **zuivert de implementatie van SDK**: Gebruik Adobe Experience Platform Assurance om de gebeurtenissen van SDK te inspecteren, gegevensinzameling te bevestigen, en integratiekwesties in real time problemen op te lossen. [ leer meer over Assurance ](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html){target="_blank"}.

1. **de gebeurtenislevering van de Test**: Verifieer dat de gebeurtenissen van uw toepassing correct door Adobe Experience Platform worden ontvangen en reizen zoals verwacht teweegbrengen. De opname van gebeurtenissen controleren en de ladingsstructuur valideren.

1. **bevestigt API integraties**: Test uw eindpunten van de douaneactie om ervoor te zorgen zij verzoeken van Journey Optimizer correct behandelen, binnen onderbrekingsgrenzen antwoorden, en terugkeer verwachte gegevensformaten.

1. **de testwijze van het Gebruik met testprofielen**: Het werk met uw [ Ingenieur van Gegevens ](data-engineer.md) om toegang tot testprofielen te krijgen, dan uw implementatie te bevestigen gebruikend de wijze van de reistest. Leer hoe te [ reizen ](../../building-journeys/testing-the-journey.md) testen.

1. **Logboeken van SDK van de Monitor**: Laat toe zuivert het registreren in uw implementatie van SDK om kwesties tijdens ontwikkeling problemen op te lossen:
   * **Mobiele SDK**: Laat het registreren toe om de gebeurtenissen van SDK en API vraag te zien
   * **SDK van het Web**: De browser van het gebruik console om de activiteit van SDK te controleren

1. **verifieer gegevensstroomconfiguratie**: Zorg ervoor uw gegevensstroom correct wordt gevormd om gegevens naar Journey Optimizer te verzenden. Controleer of gebeurtenissen door de gegevensstroom naar de juiste doelen lopen.

1. **de reisgegevens van de Vraag voor analyse**: SQL vragen van het gebruik op het meer van Gegevens om de gebeurtenissen van de reisstap te analyseren, kwesties te zuiveren, en de prestaties van de douaneactie te controleren. Onderzoek [ vraagvoorbeelden voor reisanalyse ](../../reports/query-examples.md) met inbegrip van:
   * Opsporing voor het in- en uitschakelen van profielen en redenen voor verwijderen
   * Eigen maatstaven voor de prestaties van handelingen (latentie, doorvoer, fouten)
   * Gebeurtenislevering en foutpatronen
   * Frames voor reisexemplaar

## Geavanceerde ontwikkelaarsonderwerpen {#advanced-topics}

### Werken met contextuele gegevens en verrijking

* **Interactief over series**: De syntaxis van Handlebars van het gebruik om dynamische lijsten van gebeurtenissen, de reacties van de douaneactie, en datasetraadplegingen in berichten te tonen. Leer over [ herhalend contextafhankelijke gegevens ](../../personalization/iterate-contextual-data.md).
* **de raadpleging van de Dataset**: Voer datasetraadplegingen uit om reisgegevens van de datasets van Adobe Experience Platform te verrijken. Werk met uw Ingenieur van Gegevens op configuratie. Leer over [ datasetraadpleging ](../../building-journeys/dataset-lookup.md).

### Werken met instemming en bestuur

Implementeer het beleid voor gegevensbeheer en instemming in uw integratie:

* **het bestuur van Gegevens**: Pas het beleid van het gegevensgebruik op douaneacties toe. Leer meer over [ gegevensbeheer ](../../action/action-privacy.md).
* **Toegangsbeheer**: De voorkeur van de de klantentoestemming van de handvatklant in uw implementaties. Leer over [ toestemming ](../../action/consent.md).

### Optimalisatie en aanbevolen procedures

* **Afschilderen en throttling**: Begrijp tariefgrenzen en voer aangewezen throttling uit. Leer over [ externe systemen ](../../configuration/external-systems.md).
* **optimalisering van de Reis**: Volg beste praktijken voor [ reis optimalisering ](../../building-journeys/optimize.md).
* **de behandeling van de Fout**: Voer robuuste fout behandeling uit. Herzie [ foutencodes ](../../building-journeys/error-codes-reference.md) en [ het oplossen van problemengidsen ](../../building-journeys/troubleshooting.md).

## Aanvullende bronnen {#additional-resources}

* **Developer Console**: Heb toegang tot [ Adobe Developer Console ](https://developer.adobe.com){target="_blank"} om integratie tot stand te brengen en API geloofsbrieven te beheren.
* **code van de Steekproef**: Onderzoek [ steekproefimplementaties op GitHub ](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **video&#39;s van het Leerprogramma**: Leer door hands-on leerprogramma&#39;s op [ Experience League ](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html){target="_blank"}.
* **de gemeenschap van de Ontwikkelaar**: Verbind met andere ontwikkelaars en krijg steun in de de communautaire forums van Adobe.

## Samenwerken in verschillende rollen {#next-steps}

Uw implementatiewerk doorsnijdt met andere teamleden:

>[!BEGINTABS]

>[!TAB  Werk met de Ingenieurs van Gegevens ]

Werk met [ Ingenieurs van Gegevens ](data-engineer.md) op gegevens en gebeurtenisconfiguraties samen:

* Krijg de schema&#39;s XDM en gebeurtenisstructuren u moet uitvoeren
* Begrijp welke gebeurtenissen u moet verzenden en hun vereist ladingsformaat
* Uitlijnen op vereisten voor gegevensverzameling en kwaliteitsnormen voor gegevens
* Gebeurtenislevering en gegevensinvoer tegelijk testen

>[!TAB  Werk met Beheerders ]

Werk met [ Beheerders ](administrator.md) op toegang en configuraties samen:

* API-specificaties opgeven voor aangepaste handelingen die ze zullen configureren
* Vereiste machtigingen en API-referenties aanvragen
* Coördinaat op de eisen van de kanaalconfiguratie (b.v., dupcertificaten)
* Uitlijnen op testomgevingen en sandboxstrategie

>[!TAB  Werk met Marketers ]

Werk met [ Marketers ](marketer.md) op reisvereisten en het testen samen:

* Begrijp welke gebruikersinteractie gebeurtenissen zou moeten teweegbrengen
* Tracking implementeren voor de prestaties van inhoud en de betrokkenheid van gebruikers
* Het testen van reizen met uw geïmplementeerde functies ondersteunen
* Problemen met berichtlevering of personalisatie oplossen

>[!ENDTABS]

## Bijwerken

Houd up-to-date met de nieuwste Journey Optimizer-mogelijkheden en technische wijzigingen:

* **[de Nota&#39;s van de Versie](../../rn/release-notes.md)**: De nieuwe eigenschappen van het overzicht, API veranderingen, de updates van SDK, en insectenmoeilijke situaties die elke maand worden vrijgegeven
* **[Updates van de Documentatie](../../rn/documentation-updates.md)**: De recente veranderingen van het spoor in technische documentatie met inbegrip van nieuwe implementatiegidsen en codevoorbeelden
* **[Berichten van het Product](../../rn/releases.md#staying-informed)**: Leer hoe te aan e-mail en in-productalarm voor updates van Journey Optimizer, met inbegrip van nieuwe versies van SDK, API veranderingen, het breken veranderingen, en kritieke veiligheidsupdates in te schrijven

## Starten met implementeren

Klaar om te beginnen met bouwen? Kies het eerste implementatiegebied in de bovenstaande secties:

1. **Mobiele toepassing?** Begin met [ Mobiele integratie van SDK ](#mobile-integration)
2. **Website?** Begin met [ de opstelling van SDK van het Web ](#web-implementation)
3. **API-integratie?** sprong aan [ Werkend met APIs ](#apis)
4. **Aangepast systeem?** Controle uit [ de acties van de Douane ](#custom-actions)

Elke sectie bevat koppelingen naar gedetailleerde technische documentatie, codevoorbeelden en zelfstudies om uw implementatie te begeleiden.
