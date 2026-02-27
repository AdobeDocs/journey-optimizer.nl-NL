---
solution: Journey Optimizer
product: journey optimizer
title: Veelgestelde vragen
description: Veelgestelde vragen over actieve activiteiten
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e7e994ca-aa0c-4e86-8710-c87430b74188
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 0%

---

# Veelgestelde vragen {#mobile-live-faq}

## Algemene vragen

+++Wat is het verschil tussen een Levende activiteit en een Duw bericht?

Live-activiteit biedt permanente updates in real time op het Lock Screen en Dynamic Island zonder dat gebruikers hun apparaat hoeven te ontgrendelen. Pushmeldingen zijn tijdelijke waarschuwingen die verdwijnen als ze eenmaal zijn afgewezen. Live activiteiten blijven zichtbaar en kunnen meerdere keren worden bijgewerkt tot ze expliciet worden beëindigd.

+++

+++Hoeveel instanties van Live-activiteit kunnen tegelijkertijd actief zijn?

Een iOS-toepassing kan meerdere instanties van Live-activiteiten tegelijk uitvoeren, waaronder meerdere instanties die hetzelfde `ActivityAttributes` type gebruiken.

Ontwikkelaars kunnen geen limiet instellen voor het aantal Live-activiteitinstanties van een bepaald kenmerktype. U kunt zo veel starten als uw toepassingslogica vereist, bijvoorbeeld één voor doorlopende levering of rit. IOS past echter op systeemniveau een limiet toe op het aantal Live activity-instanties dat tegelijk actief of zichtbaar kan zijn.

In de praktijk:

* iOS biedt doorgaans ondersteuning voor maximaal vijf gelijktijdige exemplaren van Live-activiteit per app.

* Als u dit aantal overschrijdt, kan het systeem ophouden tonend sommige activiteiteninstanties of eindigen oudere degenen om middelen te besparen.

* Elke instantie van Live-activiteit heeft een unieke `Activity.id` , waarmee u deze afzonderlijk kunt bijwerken of beëindigen.

+++

+++Moeten gebruikers de app hebben geopend om Live activity updates te ontvangen?

Nee. Live activiteiten kunnen worden gestart, bijgewerkt en op afstand worden beëindigd, zelfs wanneer de app volledig is gesloten, een van de belangrijkste voordelen van de functie.

+++

+++Welke iOS-versies ondersteunen Live-activiteiten?

* iOS 16.1+: Basic Live activity support
* iOS 17.2+: Push-to-start-functionaliteit (extern starten zonder app te openen)
* iOS 18+: Ondersteuning voor kanalen voor uitzending van op het publiek gebaseerde Live-activiteiten
+++

+++Hoe lang kan een Live-activiteit actief blijven?

Apple beperkt Levende activiteit tot **8 uren van actieve updates**. Na dat, beëindigt het systeem automatisch de activiteit, hoewel het in een statische staat voor maximaal **12 extra uren** vóór verwijdering zichtbaar kan blijven. U kunt een live activiteit ook eerder beëindigen door een `dismissalDate` in te stellen of `activity.end()` expliciet aan te roepen in uw app.

+++

### Ontwikkelaarsvragen

+++Moet ik een aparte widgetextensie maken voor Live-activiteit?

Ja. Live-activiteit wordt weergegeven via WidgetKit, dus u moet een widgetextensie maken in uw Xcode-project en `ActivityConfiguration` implementeren.
[ leer meer over configuratie Widget ](mobile-live-configuration-sdk.md)

+++

+++Kan ik dezelfde `LiveActivityAttributes` -klasse gebruiken voor zowel lokale als externe Live-activiteiten?

Ja. Dezelfde kenmerkklasse werkt voor zowel lokaal opgestarte als extern opgestarte (push-to-start) Live-activiteit. U dient ervoor te zorgen dat u deze registreert bij `Messaging.registerLiveActivity()` .

+++

+++Wat gebeurt er als ik een update verzend voor een Live-activiteit die niet bestaat?

Als u een update- of eindgebeurtenis verzendt voor een niet-bestaande `liveActivityID` of `channelID` , mislukt de aanvraag zonder toezicht op het apparaat. Zorg altijd dat u bijhoudt welke Live-activiteitsinstanties actief zijn voor elke gebruiker.

+++

+++Kan ik Live-activiteit testen in de iOS Simulator?

Ja, u kunt plaatselijk-begonnen evenals ver-begonnen Levende activiteit in de Simulator van iOS testen.

* **Lokaal**: Dit omvat het creëren van, het bijwerken van, en het beëindigen van Levende activiteit direct van uw app gebruikend **ActivityKit APIs**.

* **Verre**: Om Levende functionaliteit van de Activiteiten ver te testen, integreer ons Overseinen SDK in uw app en gebruik verstrekte uitvoering APIs om verre begin, update en eind naar uw testapparaat of de Simulator van iOS te verzenden. Gelijkaardig aan hoe de pushberichten momenteel met de integratie van Adobe SDKs kunnen worden getest.

+++

+++Hoe kan ik updates verwerken wanneer de app op de achtergrond wordt uitgevoerd?

De SDK handelt dit automatisch af. Zodra de app is geregistreerd, ontvangt Live-activiteit updates, zelfs wanneer de app wordt beëindigd. Er zijn geen extra achtergrondmodi vereist.
+++

+++Wat is het verschil tussen `liveActivityID` en `channelID`?

* `liveActivityID`: wordt gebruikt voor individuele (eenheids) Levende activiteit gericht op specifieke gebruikers. Elke id vertegenwoordigt een unieke instantie van Live-activiteit.
* `channelID`: Wordt gebruikt voor het uitzenden van Live-activiteiten die naar het publiek worden verzonden. Alle gebruikers in het publiek ontvangen dezelfde updates op hetzelfde kanaal.
+++

+++Kan ik de weergave Dynamisch eiland los van het vergrendelingsscherm aanpassen?

Ja. `ActivityConfiguration` heeft afzonderlijke sluitingen voor de inhoud van het Scherm van het Slot en de Dynamische inhoud van de Eilanden (uitgevouwen, compacte, en minimale staten), elk ontwerp onafhankelijk.
+++

+++Moet ik pushtokens handmatig opslaan?

Nee. Wanneer u een Actieve Type van Activiteit bij `Messaging.registerLiveActivity()` registreert, verzamelt en beheert SDK automatisch duptokens voor u.
+++

+++Zijn er grenzen aan het op afstand starten van Live-activiteiten?

Ja. Externe start via `ActivityKit` zijn onderworpen aan door het systeem opgelegde beperkingen. Als u snel na elkaar probeert meerdere beginaanvragen te starten, kan iOS verdere start weigeren vanwege quota&#39;s voor Live-activiteit of budgetbeperkingen. Na ongeveer 5 opeenvolgende beginpogingen, beginnen de verdere verzoeken mislukt tot een korte afkoelingsperiode voorbijgaat.

+++

+++Wat is het budget voor updates met hoge prioriteit?

Apple geeft geen exact numeriek uiteinde op voor `(priority: 10)` Live-activiteiten-updates met hoge prioriteit. Het systeem handhaaft een dynamisch intern budget dat beperkt hoe vaak dergelijke updates kunnen worden verzonden. Als er te veel updates met hoge prioriteit worden uitgegeven in een korte periode, kan iOS de daaropvolgende updates vertragen of vertragen.

Vertraging minimaliseren:

* **prioritaire niveaus van het Saldo**: Combineer zowel standaard `(priority: 5)` als hoge `(priority: 10)` updates afhankelijk van belang.
* **Hoge prioriteit van het Gebruik spaarzaam**: Reserve hoge prioriteit voor tijd-kritieke updates, zoals leveringsvooruitgang, ordestatus, of levende sportscores.
* **de frequente updates van de Steun**: omvatten `NSSupportsLiveActivitiesFrequentUpdates` in uw app `Info.plist` en plaatsen het aan **JA** als u frequente updates nodig hebt.

+++

### Marktvragen

+++Kan ik inhoud van Live-activiteit voor elke gebruiker in een uitzendingscampagne personaliseren?

De campagnes van de uitzending verzenden de zelfde inhoud naar alle gebruikers in het publiek. Gebruik voor persoonlijke inhoud eenheidscampagnes (transactionele campagnes) die gericht zijn op individuele gebruikers.
+++

+++Hoe weet ik of mijn Live-activiteiten succesvol zijn uitgevoerd?

[ controleert uw campagneanalytica ](../reports/campaign-global-report-cja-activity.md) in Adobe Journey Optimizer. U kunt de leveringssnelheden, mislukkingen, en betrokkenheidsmetriek volgen. Overweeg ook aangepaste analytische gebeurtenissen in uw app te implementeren.
+++

+++Kan ik live-activiteiten vooraf plannen?

De API-aanroep activeert de Live-activiteit direct. U kunt uw API-aanroepen echter plannen via uw back-endsystemen of de mogelijkheden van de Journey Optimizer-organisatie gebruiken om deze op de juiste manier uit te voeren.
+++

+++Wat gebeurt er als ik een &quot;start&quot;-gebeurtenis verzend voor een Live-activiteit die al bestaat?

Bij het op afstand starten van Live-activiteiten via API&#39;s voor Adobe-uitvoering:

* U kunt een header `x-request-id` in uw aanvraag opnemen. In het ideale geval moet elke `liveActivityID` een-op-een relatie hebben met de bijbehorende `x-request-id` . Dit zorgt ervoor dat als er meerdere aanvragen worden ingediend met dezelfde combinatie `x-request-id` en `liveActivityID` , er slechts één instantie Live-activiteit wordt gestart op het apparaat en dubbele aanvragen worden genegeerd.

* Als de header `x-request-id` wordt weggelaten, wordt elke aanvraag afzonderlijk behandeld. Dit kan ertoe leiden dat meerdere instanties van Live-activiteit met dezelfde `liveActivityID` worden gemaakt. In dergelijke gevallen kunnen toekomstige updates mislukken of slechts op één van de actieve exemplaren van toepassing zijn.

* De waarde `x-request-id` mag niet opnieuw worden gebruikt in verschillende `liveActivityIDs` -API-aanvragen.

+++

+++Kan ik A/B verschillende ervaringen met Live-activiteit testen?

Ja. Maak meerdere campagnes met verschillende inhoudsstructuren en gebruik Adobe Journey Optimizer-experimentatiefuncties om te testen wat beter presteert. Zorg ervoor dat uw app alle variaties in de inhoudsstatus ondersteunt.

+++

+++Hoe vaak moet ik een Live-activiteit bijwerken?

Werk alleen bij wanneer belangrijke wijzigingen in de informatie worden aangebracht omdat updates te vaak worden uitgevoerd, de batterij kunnen leeglopen en de kwaliteit van de gebruikerservaring kan verminderen. Voor scenario&#39;s in real time, zoals levering het volgen, is elke 30-60 seconden typisch aanvaardbaar. Voor langzamere veranderende inhoud, zoals sportscores, dient u alleen de update voor belangrijke gebeurtenissen bij te werken.

+++

+++Kan ik gebruikers als doel instellen op basis van of ze Live-activiteit hebben ingeschakeld?

U zult met uw ontwikkelingsteam moeten samenwerken om deze voorkeur aan Adobe Experience Platform als gebruikersattribuut te volgen en over te gaan, dan die segment op dat attribuut wordt gebaseerd.

+++

### API-vragen

+++Wat is het verschil tussen `timestamp` en `dismissal-date`?

* `timestamp`: De huidige tijdperk waarin de gebeurtenis plaatsvindt, die voor alle gebeurtenissen is vereist.
* `dismissal-date`: Een toekomstige tijdperk waarin de Live-activiteit automatisch wordt beëindigd. Dit is alleen vereist voor &quot;end&quot;-gebeurtenissen.

+++

+++Moet ik alle `attributes` velden in elke updateaanroep verzenden?

Ja, op basis van uw `LiveActivityAttribute` -klasse.

* Alle velden van het kenmerkobject, inclusief `liveActivityData` , moeten bij elke oproep worden opgenomen, voor het starten, bijwerken of beëindigen.
* Alleen de `content-state` -velden geven aan wat er daadwerkelijk dynamisch verandert bij actieve activiteiten.
* Neem ook een waakzaam object op. Hierdoor wordt de push behandeld als een bericht dat zichtbaar is voor de gebruiker, en niet als een achtergrond met stilte. Alleen vereist voor &#39;start&#39;-gevallen en anderszins optioneel.

+++

+++In welke notatie moeten tijdstempels worden geplaatst?

De Tijd van het tijdperk van Unix van het gebruik in **seconden** niet milliseconden. Bijvoorbeeld: `1759937682`

+++

+++Kan ik dezelfde `requestId` gebruiken voor meerdere API-aanroepen?

Nee. Elke API-aanvraag moet een uniek bestand `requestId` hebben om te zorgen voor immuniteitsprestatie en correcte tracering. Gebruik UUID&#39;s of vergelijkbare unieke id&#39;s.

+++

+++Welke verificatie is vereist voor de Headless API?

Verwijs naar [ API teweeggebrachte Documentatie van Campagnes ](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) voor authentificatievereisten, met inbegrip van tokens OAuth en API sleutels.

+++

+++Wat gebeurt er als mijn API-aanroep mislukt?

Implementeer logica voor opnieuw proberen met exponentiële back-up. Controleer de API-reactie op foutcodes en berichten om problemen vast te stellen. Veelvoorkomende fouten zijn ongeldige campagne-id&#39;s, onjuist gevormde payloads of verificatieproblemen.

+++

+++Kan ik updates van Live-activiteit verzenden vanaf mijn eigen back-endservers?

Ja, dat is het bedoelde gedrag. Uw back-end roept de Adobe Journey Optimizer Headless API aan om Live activity-gebeurtenissen te activeren wanneer dit vereist is voor uw bedrijfslogica.

+++

+++Heb ik een andere campagne nodig voor begin, update, en eindgebeurtenissen?

Nee. U kunt dezelfde campagne gebruiken en het veld `event` in de payload wijzigen. Sommige organisaties geven echter de voorkeur aan aparte campagnes voor een betere analysetracering.

+++

### Problemen oplossen

+++Mijn Live-activiteiten worden gestart, maar niet bijgewerkt. Wat zou het probleem kunnen zijn?

Vaak voorkomende oorzaken:

* Niet-overeenkomende aanroepen `liveActivityID` of `channelID` tussen starten en bijwerken.
* `content-state` -velden komen niet overeen met uw `ContentState` struct.
* De Live-activiteit is al beëindigd.
* De connectiviteitskwesties van het netwerk op het apparaat.
* De tijdperktijd die als tijdstempel wordt gebruikt, is niet up-to-date.

+++

+++Het veld `attributes-type` wordt niet herkend. Wat moet ik controleren?

* Verzeker de klassennaam precies **** (case-sensitive) met uw Swift struct naam aanpast
* Controleren of de structuur correct is gedefinieerd en geregistreerd
* Controleren op typos in de JSON-payload
* Bevestig dat de versie van de app is geïnstalleerd met de implementatie van Live activiteit

+++

+++Gebruikers zien alleen de update van Live-activiteit en niet de waarschuwingsmelding. Is dit een bekend probleem?

Nee. Het veld `alert` is optioneel en kan door iOS onder bepaalde omstandigheden worden onderdrukt, bijvoorbeeld in de modus Niet storen. Live activiteit kan zonder toezicht worden bijgewerkt, wat vaak het bedoelde gedrag is. Het waarschuwingsveld is verplicht voor het verzenden van een externe start, anders behandelt appel het als een stille achtergrondmelding.

+++

+++Kan ik alle exemplaren van Live-activiteit voor een gebruiker verwijderen of wissen?

U moet een &quot;end&quot;-gebeurtenis verzenden voor elke actieve Live activity-instantie. Houd bij welke instanties van Live-activiteit actief zijn voor elke gebruiker in uw systeem, zodat u deze op de juiste wijze kunt opschonen.

+++

+++Mijn widget toont &quot;Geen gegevens&quot;, ook al heb ik een update verzonden. Wat zou het probleem kunnen zijn?

* Controleer of uw widgetimplementatie correct toegang heeft tot `context.state` en `context.attributes` .
* Controleer of standaardwaarden of foutstatussen in de widgetinterface worden verwerkt.
* Gebruik het `LiveActivityAssuranceDebuggable` protocol om het schema te zuiveren.
* Test met Adobe Assurance om te zien of er gegevens worden ontvangen.
+++
