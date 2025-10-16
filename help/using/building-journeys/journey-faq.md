---
solution: Journey Optimizer
product: journey optimizer
title: Veelgestelde vragen over reizen
description: Veelgestelde vragen over Journey Optimizer-reizen
feature: Journeys, Get Started
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: reis, vragen, antwoorden, problemen oplossen, hulp, gids
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: 32848633cdfb5683b45286fcdd22711a82d591b5
workflow-type: tm+mt
source-wordcount: '4094'
ht-degree: 0%

---


# Veelgestelde vragen {#faq-journeys}

Hieronder vindt u Veelgestelde vragen over Adobe Journey Optimizer-reizen.

Wilt u meer details? Gebruik terugkoppelen opties bij de bodem van deze pagina om uw vraag op te roepen, of met [ gemeenschap van Adobe Journey Optimizer ](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"} te verbinden.

## Algemene beginselen

+++ Wat is een reis in Adobe Journey Optimizer?

Een reis is een multi-step organisatie die u toestaat om klantenervaringen in real time over veelvoudige kanalen te ontwerpen en uit te voeren. De reizen combineren gebeurtenissen, orkestactiviteiten, acties, en berichten om gepersonaliseerde, contextuele ervaringen tot stand te brengen die op klantengedrag en bedrijfsgebeurtenissen worden gebaseerd.

Leer meer over [ reizen ](journey.md).

+++

+++ Wat zijn de verschillende soorten reizen?

Adobe Journey Optimizer ondersteunt drie soorten reizen:

* **Eenheidstreizen**: teweeggebracht individueel door een gebeurtenis (b.v., een aankoop, app login). Profielen voeren de reis een voor een in wanneer de gebeurtenis plaatsvindt.
* **lees de reizen van het Publiek**: Begin met een publiek van Adobe Experience Platform en verzend berichten in partij aan alle profielen in dat publiek.
* **de dienstreizen van de Bedrijfs gebeurtenis**: teweeggebracht door bedrijfsgebeurtenissen (b.v., voorraadupdates, weeralarm) die veelvoudige profielen gelijktijdig beïnvloeden.

Leer meer over [ reistypes ](entry-management.md#types-of-journeys).

+++

+++ Wat is het verschil tussen een reis en een campagne?

**de Schavens** zijn multi-step organisaties die op gebeurtenissen of doelpubliek reageren, die voor complexe logica, voorwaarden, wachttijden, en veelvoudige aanrakingspunten over de klantenlevenscyclus toestaan.

**campagnes** zijn eenmalige of terugkomende mededelingen die naar een specifiek publiek worden verzonden, ideaal voor standalone berichten zoals promotionele aankondigingen of nieuwsbrieven.

**Beste praktijken**: De reizen van het gebruik voor aan de gang zijnde, multi-step overeenkomst, en campagnes voor gerichte, standalone mededelingen.

+++

+++ Wat zijn de belangrijkste onderdelen van een reis?

Een reis bestaat uit:

* **Gebeurtenissen**: De punten van de ingang die de reis (b.v., profielkwalificatie, bedrijfsgebeurtenissen) teweegbrengen
* **de activiteiten van het Orchestration**: De componenten van de logica zoals voorwaarden, wachten, lezen publiek, en eind
* **Acties**: Activiteiten die taken, zoals het verzenden van berichten, het bijwerken van profielen, of het roepen van externe APIs uitvoeren
* **Ingebouwde kanaalacties**: De inheemse overseinenmogelijkheden voor e-mail, SMS, duw, en andere kanalen
* **de acties van de Douane**: Integratie met derdesystemen

Leer meer over [ reisactiviteiten ](about-journey-activities.md).

+++

+++ Hoe kan ik kiezen tussen een eenheidsreis en een leestoegang?

Gebruik **unitaire reizen** wanneer:

* U moet op individuele klantenacties in real time (b.v., koopbevestiging, kartontroeping) reageren
* Elke klant moet in zijn eigen tempo verdergaan
* U wilt activeren op basis van specifieke gebeurtenissen

Het gebruik **leest publiekstrajecten** wanneer:

* U verzendt partijmededelingen naar een groep (b.v., maandelijkse nieuwsbrief, promotiecampagnes)
* Alle klanten zouden het bericht rond de zelfde tijd moeten ontvangen
* U richt een vooraf bepaald publiekssegment

+++

## Reizen bouwen

+++ Hoe begin ik mijn eerste reis te bouwen?

Voer de volgende belangrijke stappen uit:

1. **de eerste vereisten van de opstelling**: Vorm gebeurtenissen, gegevensbronnen, en acties zoals nodig
2. **creeer de reis**: Navigeer aan het menu van de Reizen en klik &quot;Create Reis&quot;
3. **bepaalt reis eigenschappen**: Plaats de reisnaam, beschrijving, namespace, en andere montages
4. **Ontwerp de reis**: De activiteiten van de belemmering en van de daling van het palet in het canvas
5. **Test de reis**: De testwijze van het gebruik om uw reislogica te bevestigen
6. **publiceer de reis**: Activeer de reis om het levend te maken

Volg de [ geleidelijke gids ](journey-gs.md).

+++

+++ Welke voorwaarden zijn er nodig om een reis te kunnen maken?

Vereisten zijn afhankelijk van het type reis:

* **gebeurtenis-teweeggebrachte reizen**: Vorm gebeurtenissen om te bepalen wanneer de profielen de reis zouden moeten ingaan
* **op publiek-gebaseerde reizen**: Creeer publiek in Adobe Experience Platform
* **de verrijking van Gegevens**: De bronnen van opstellingsgegevens om extra informatie terug te winnen
* **de Integraties van de Derde**: Vorm douaneacties als het gebruiken van externe systemen

Leer meer over [ reisconfiguratie ](../configuration/about-data-sources-events-actions.md).

+++

+++ Kan ik gegevens van externe systemen gebruiken tijdens mijn reis?

Ja. U kunt **externe gegevensbronnen** vormen om informatie van derde API diensten terug te winnen en het in uw reisvoorwaarden, verpersoonlijking, of acties te gebruiken. Dit staat u toe om de klantenervaring met gegevens in real time van uw CRM, loyaliteitssystemen, weerdiensten, of andere externe platforms te verrijken.

Leer meer over [ externe gegevensbronnen ](../datasource/external-data-sources.md).

+++

+++ Hoe voeg ik voorwaarden toe aan mijn reis?

U kunt voorwaarden toevoegen gebruikend de **activiteit van de Voorwaarde** van het orkest palet. Voorwaarden bieden de volgende mogelijkheden:

* Eenvoudige of geavanceerde voorwaarden maken met de expressie-editor
* Splits de reis in veelvoudige wegen die op profielattributen, publiekslidmaatschap, gebeurtenissen, of contextafhankelijke gegevens worden gebaseerd
* Tijdlijnpaden definiëren voor profielen die niet binnen een opgegeven tijd aan de voorwaarde voldoen

Leer meer over [ voorwaarden ](condition-activity.md).

+++

+++ Kan ik berichten naar profielen verzenden tijdens een reis?

Ja. Journey Optimizer omvat **ingebouwde kanaalacties** die u toestaan om berichten door e-mail, dupberichten, SMS/MMS/RCS, in-app berichten, Webervaringen, code-gebaseerde ervaringen, direct mail, inhoudskaarten, WhatsApp, en LIJN te verzenden. U kunt berichtinhoud rechtstreeks in Journey Optimizer ontwerpen en deze toevoegen als actieactiviteiten tijdens uw reis.

Leer meer over [ berichten in reizen ](journeys-message.md).

+++

+++ Hoe wacht ik op een specifieke tijd of een bepaalde gebeurtenis op een reis?

Gebruik **wacht activiteit** om de reis voor een gespecificeerde duur of tot een specifieke datum/tijd te pauzeren. Wachten-activiteiten zijn handig voor:

* Verzenden van vervolgberichten na een vertraging (bijvoorbeeld 3 dagen na aankoop)
* Wachten op kantooruren voordat actie wordt ondernomen
* Druppingscampagnes maken met getimede intervallen
* Combineren met voorwaarden om time-outscenario&#39;s te maken

Leer meer over [ wachten activiteiten ](wait-activity.md).

+++

+++ Kan ik profielgegevens bijwerken binnen een reis?

Ja. Gebruik de **activiteit van het Profiel van de Update** om profielattributen in Adobe Experience Platform te wijzigen die op reisgebeurtenissen of voorwaarden wordt gebaseerd. Dit is nuttig voor het bijwerken van loyaliteitspunten, het registreren van reis mijlpalen, het veranderen van voorkeursinstellingen, of het volgen van de scores van de klantenovereenkomst.

Leer meer over [ profielupdates ](update-profiles.md).

+++

+++ Hoe verstuur ik een e-mail meteen nadat iemand een aankoop heeft gedaan?

Creeer a **unitaire gebeurtenis-teweeggebrachte reis**:

1. Een &quot;Purchase&quot;-gebeurtenis configureren met de ordergegevens
2. De gebeurtenis toevoegen als uw toegangspunt voor de reis
3. Direct volgen met een e-mailactie
4. Ontwerp een bevestigingsbericht voor uw bestelling met persoonlijke bestelgegevens
5. De reis publiceren

De reis wordt automatisch geactiveerd wanneer een aankoopgebeurtenis wordt ontvangen en de bevestigingsmail in real-time wordt verzonden.

Leer meer over [ gebeurtenisconfiguratie ](../event/about-events.md) en [ e-mailacties ](journeys-message.md).

+++

+++ Kan ik een bericht opnieuw verzenden als iemand het niet opent of klikt?

Ja. Gebruik de activiteit van de a **voorwaarde** die met **wordt gecombineerd activiteiten** wacht:

1. Een wachttijdactiviteit toevoegen (bijvoorbeeld 3 dagen wachten)
2. Voeg een Activiteitencontrole van de Voorwaarde toe als e-mail werd geopend of geklikt
3. Twee paden maken:
   * **Indien geopend/geklikt**: Eind de reis of ga met volgende stappen verder
   * **Als niet geopend/geklikt**: verzend een herinnering e-mail met verschillende onderwerpregel

**Beste praktijken**: Beperk het aantal opnieuw beëindigt om verschijnende spammy (typisch 1-2 herinneringen maximum) te vermijden.

Leer meer over [ reactiegebeurtenissen ](reaction-events.md).

+++

+++ Hoe creëer ik een ritje voor het verlaten van een winkelwagen?

Maak een door een gebeurtenis geïnitieerde reis met logica voor wachten en voorwaarden:

1. **vorm een &quot;Verlaten Kar&quot;gebeurtenis**: teweeggebracht wanneer de punten worden toegevoegd maar de controle wordt niet voltooid binnen een timeframe
2. **voeg een Wacht activiteit** toe: Wacht 1-2 uren om de klantentijd te geven om natuurlijk te voltooien
3. **voeg een Voorwaarde** toe: Controle als de aankoop tijdens wachttijd werd voltooid
4. **als niet gekocht**: verzend een e-mail van de terugkeringsherinnering met de inhoud van het karretje
5. **Facultatief**: Voeg een andere wachttijd (24 uren) toe en verzend een tweede herinnering met een stimulans (b.v., 10% korting)

Leer meer over [ gevallen van het reisgebruik ](jo-use-cases.md).

+++

+++ Hoe kan ik klanten opsplitsen in verschillende paden op basis van hun aankoopgeschiedenis?

Gebruik de activiteit van de a **Voorwaarde** met het publiekslidmaatschap of profielattributen:

1. Voeg een Condition-activiteit toe aan uw reis
2. Meerdere paden maken op basis van criteria:
   * **Weg 1**: De klanten van de hoog-waarde (totale aankopen > $1000)
   * **Weg 2**: Regelmatige klanten (totale aankopen $100 -$1000)
   * **Weg 3**: Nieuwe klanten (totale aankopen &lt; $100)
3. Verschillende berichten of aanbiedingen toevoegen voor elk pad

Leer meer over [ voorwaarden ](condition-activity.md) en [ publiekskwalificatie ](audience-qualification-events.md).

+++

+++ Hoe kan ik verschillende tijdzones afhandelen op mijn reis?

Journey Optimizer biedt verschillende opties voor tijdzonebeheer:

* **timezone van het Profiel**: De berichten worden verzonden gebaseerd op timezone van elk individu die in hun profiel wordt opgeslagen
* **Vaste timezone**: Alle berichten gebruiken specifieke timezone u bepaalt
* **wacht tot specifieke tijd**: Gebruik de Wacht activiteit om berichten op een specifieke tijd in lokale timezone van de ontvanger (b.v., 10 AM) te verzenden

**Voorbeeld**: Om een e-mail van de &quot;Goede ochtend&quot;te verzenden bij 9 AM in de tijdzone van elke klant, gebruik een Wacht activiteit met &quot;wacht tot een vaste datum/tijd&quot;en laat de timezone optie toe.

Leer meer over [ timezone management ](timezone-management.md).

+++

+++ Hoe lang moet ik wachten tussen berichten op mijn reis?

**Beste praktijken voor wachttijden**:

* **Transactionele berichten** (ordesbevestigingen): Verzend onmiddellijk
* **Welkome reeksen**: 1-3 dagen tussen e-mails
* **Onderwijsinhoud**: 3-7 dagen tussen berichten
* **Bevorderingscampagnes**: Minstens 7 dagen tussen aanbiedingen
* **re-engagement**: 14-30 dagen voor inactieve gebruikers

**Factoren om te overwegen**:

* Industriestandaarden en verwachtingen van klanten
* Noodzaak en belang van berichten
* Uw algemene berichtfrequentie over alle kanalen
* Servicepatronen van de klant

**Uiteinde**: De regels van het afschilderen van het gebruik om het totale aantal berichten te beperken een klant over alle reizen ontvangt.

Leer meer over [ wachten activiteiten ](wait-activity.md) en [ reis het in kaart brengen ](../conflict-prioritization/journey-capping.md).

+++

## Testen en publiceren

+++ Hoe kan ik mijn reis testen voordat ik het publiceert?

Journey Optimizer biedt twee testmethoden:

* **wijze van de Test**: Simuleer individuele profielen die door de reis stap voor stap bewegen, toestaand u om logica, voorwaarden, en acties te verifiëren alvorens te leven.
* **Droog looppaswijze**: Voer uw reis uit gebruikend echte productiegegevens zonder daadwerkelijke klanten te contacteren of profielinformatie bij te werken. Dit geeft u vertrouwen in doelgerichtheid en reisontwerp.

**Beste praktijken**: Test altijd reizen alvorens te publiceren om ervoor te zorgen zij werken zoals verwacht en om om het even welke kwesties vroegtijdig te identificeren.

Leer meer over [ testwijze ](testing-the-journey.md) en [ droge looppas ](journey-dry-run.md).

+++

+++ Wat gebeurt er als ik een reis publiceer?

Wanneer u een reis publiceert:

* De reis wordt **actief** en klaar om nieuwe profielen goed te keuren
* Profielen kunnen worden ingevoerd op basis van de entry-criteria (gebeurtenis of publiek)
* Berichten en acties worden uitgevoerd voor profielen die door de reis bewegen
* U kunt een gepubliceerde reis niet rechtstreeks bewerken (u moet een nieuwe versie maken)

Leer meer over [ het publiceren reizen ](publishing-the-journey.md).

+++

+++ Kan ik een reis wijzigen die al gepubliceerd is?

U kunt een live reis niet rechtstreeks bewerken. Wijzigingen aanbrengen:

1. **creeer een nieuwe versie**: Dupliceer de gepubliceerde reis om een ontwerp versie te creëren
2. **maak uw veranderingen**: Bewerk de ontwerp versie zoals nodig
3. **Test de nieuwe versie**: De testwijze van het gebruik om veranderingen te bevestigen
4. **publiceer de nieuwe versie**: Dit sluit automatisch de vorige versie en activeert nieuwe

Profielen die al onderweg zijn, voltooien de oorspronkelijke versie, terwijl nieuwe profielen de nieuwe versie invoeren.

Leer meer over [ reisversies ](journey-ui.md#journey-versions).

+++

+++ Hoe stop ik een reis?

U kunt de uitvoering van de reis op verschillende manieren beheren:

* **dicht bij nieuwe ingangen**: De nieuwe profielen van het einde van het ingaan terwijl het toestaan van bestaande profielen om hun reis te voltooien
* **Einde onmiddellijk**: Eind de reis en ga alle profielen weg momenteel in het
* **Pauze**: Tijdelijk de reis tegenhouden en het later hervatten (beschikbaar voor specifieke vervoerstypes)

Leer meer over [ beëindigende reizen ](end-journey.md).

+++

+++ Wat is het verschil tussen &quot;Dicht bij nieuwe ingangen&quot; en &quot;Stop&quot;?

**dicht bij nieuwe ingangen**:

* Nieuwe profielen kunnen geen reis ingaan
* Profielen die al onderweg zijn, worden voortgezet en het pad ervan voltooid
* Gebruik dit als u een reis netjes wilt afwinden
* Voorbeeld: seizoenscampagne die is beëindigd, maar u wilt dat bestaande klanten hun ervaring voltooien

**Einde**:

* Hiermee wordt de reis voor alle profielen onmiddellijk beëindigd
* Alle profielen die momenteel op reis zijn, worden verlaten
* Gebruik dit voor dringende situaties of kritieke fouten
* Voorbeeld: productterugroeping die onmiddellijke stopzetting van promotieberichten vereist

Leer meer over [ opties van de de reispauze ](journey-pause.md).

+++

## Uitvoering van en toezicht op reizen

+++ Hoe kan ik de voortgang van een reis bijhouden?

U kunt de uitvoering van de reis controleren met:

* **Reis Levend Rapport**: De metriek en KPIs van de mening in real time voor uw reis
* **Reis Al Rapport van de Tijd**: Analyseer reisprestaties gebruikend Customer Journey Analytics
* **Gebeurtenissen van de Stap van de Reis**: Toegang gedetailleerde uitvoeringsgegevens voor douane het melden
* **Dashboard van de Looppas van de Droog van de Reis**: De resultaten van de testuitvoering van het overzicht alvorens live te gaan

Leer meer over [ reis rapporterend ](report-journey.md).

+++

+++ Waarom kwam er geen profiel op mijn reis?

De profielen met algemene redenen mogen geen reis maken:

* **Gebeurtenis niet ontvangen**: De het teweegbrengen gebeurtenis werd niet verzonden of behoorlijk gevormd
* **niet voldaan aan de criteria van het publiek**: Het profiel kwalificeert niet voor het ingangspubliek
* **Regels van de Wedertoetreding**: Het profiel voltooide onlangs de reis en re-entry wordt geblokkeerd
* **niet gepubliceerde Reis**: De reis is in ontwerpstatus
* **Ongeldige namespace**: De reis namespace past niet de profielidentiteit aan
* **Reis gesloten**: De reis keurt nieuwe ingangen niet meer goed

Leer meer over [ ingangsbeheer ](entry-management.md).

+++

+++ Wat zijn trapsgewijze gebeurtenissen en hoe kan ik ze gebruiken?

De gebeurtenissen van de wegstap zijn automatisch geproduceerde datasets die gedetailleerde informatie over elke stap vangen een profiel in een reis neemt. Deze omvatten entry- en exit-gebeurtenissen, uitgevoerde handelingen (verzonden berichten, aangeroepen aangepaste handelingen), overgangen (verplaatsen tussen activiteiten) en fouten en time-outs.

**gevallen van het Gebruik**:

* Aangepaste rapporten samenstellen in Customer Journey Analytics- of BI-gereedschappen
* Problemen met het uitvoeren van foutopsporing
* Gedetailleerd profielgedrag bijhouden
* Geavanceerde analysemodellen en attributiemodellen maken

Leer meer over [ gebeurtenissen van de reisstap ](../reports/sharing-overview.md).

+++

+++ Hoe kan ik een reis problemen oplossen die niet zoals verwacht werkt?

Journey Optimizer biedt verschillende bronnen voor probleemoplossing:

* **de indicatoren van de Fout**: Visuele alarm in de kwesties van de de hoogteconfiguratie van het wegcanvas
* **wijze van de Test**: Stap door de reis om te identificeren waar de problemen voorkomen
* **de rapporten van de Reis**: De metriek van de uitvoering van het overzicht om knelpunten of fouten te vinden
* **de stapgebeurtenissen van de Reis**: Analyseer gedetailleerde uitvoeringsgegevens om profielgedrag te begrijpen

**Gemeenschappelijke kwesties**:

* Onjuist geconfigureerde gebeurtenissen of soorten publiek
* Ontbrekende gegevensbronverbindingen
* Ongeldige expressies in voorwaarden of personalisatie
* Te korte time-outinstellingen

Leer meer over [ het oplossen van problemenreizen ](troubleshooting.md).

+++

+++ Wat gebeurt er als een actie mislukt op een reis?

Wanneer een actie ontbreekt (b.v., de onderbrekingen van de API vraag, fout van de berichtlevering), gaat de reis door gebrek tenzij anders gevormd verder. U kunt voorwaardenactiviteiten bepalen om mislukkingsscenario&#39;s te behandelen, en de fouten worden het programma geopend reisrapporten en stapgebeurtenissen voor controle.

**Beste praktijken**: Plaats aangewezen onderbrekingswaarden voor externe acties en bepaal alternatieve wegen voor kritieke mislukkingsscenario&#39;s.

Leer meer over [ actierespons ](../action/action-response.md).

+++

+++ Kan ik zien wie momenteel op reis is?

Ja. Gebruik het **Levende Rapport van de Reis** aan mening:

* Aantal profielen op reis
* Aantal profielen bij elke activiteit
* Profielen die in de laatste 24 uur zijn ingevoerd
* Metrische gegevens voor uitvoering in realtime

Om individuele profielen te zien, gebruik {de gebeurtenissen van de 0} reis stap **in Customer Journey Analytics of vraag direct de datasets van de step gebeurtenis.**

Leer meer over [ reis levende rapportering ](report-journey.md).

+++

+++ Waarom worden mijn berichten niet op mijn reis verstuurd?

**Gemeenschappelijke redenen en oplossingen**:

* **Goedkeuring kwesties**: De ontvangers hebben niet binnen verkiest om mededelingen te ontvangen
Oplossing: controleer toestemmingsbeleid en opt-in status

* **Lijst van de Onderdrukking**: De e-mailadressen zijn op de lijst van de onderdrukking
Oplossing: bekijk de onderdrukkingslijst voor stuitingen of klachten

* **Ongeldige contactinformatie**: Ontbrekende of misvormde e-mailadressen/telefoonaantallen
Oplossing: de kwaliteit van profielgegevens valideren

* **niet gepubliceerde Reis**: De reis is nog op ontwerpwijze
Oplossing: publiceer de reis om deze te activeren

* **niet goedgekeurd Bericht**: De inhoud van het bericht vereist goedkeuring alvorens te verzenden
Oplossing: ter goedkeuring indienen of de goedkeuringsstatus controleren

* **de configuratiekwestie van het Kanaal**: De configuratie E-mail/SMS is onjuist
Oplossing: controleer kanaalconfiguraties en verificatie

Leer meer over [ het oplossen van problemen ](troubleshooting.md) en [ toestemmingsbeheer ](../action/consent.md).

+++

+++ Hoe kan ik berichten personaliseren op mijn reis?

U kunt berichten personaliseren gebruikend de **verpersoonlijkingsredacteur**:

**Beschikbare verpersoonlijkingsgegevens**:

* **attributen van het Profiel**: Voornaam, achternaam, e-mail, douanegebieden
* **de gegevens van de Gebeurtenis**: De details van de aankoop, doorbladergedrag, app activiteit
* **Contextafhankelijke gegevens**: De variabelen van de reis, externe API gegevens
* **het lidmaatschap van de Publiek**: De kwalificaties van het segment
* **Berekende attributen**: Vooraf berekende waarden

**verpersoonlijking van het Voorbeeld**:

* &quot;Hallo {{profile.firstName}}, bedankt voor uw aankoop van {{event.productName}}&quot;
* &quot;Gebaseerd op uw loyaliteitsrij ({{profile.loyaltyTier}}), hier is een speciale aanbieding&quot;
* Dynamische inhoudsblokken die worden gewijzigd op basis van de voorkeuren van de klant

Leer meer over [ verpersoonlijking ](../personalization/personalize.md).

+++

+++ Kan ik verschillende berichten verzenden die op aangewezen kanaal worden gebaseerd?

Ja. Gebruik de activiteit van de a **Voorwaarde** om het aangewezen kanaal te controleren:

1. Een profiel voor voorwaardelijke controle toevoegen.preferredChannel
2. Maak afzonderlijke paden voor elk kanaal:
   * **E-mailweg**: Verzend e-mailbericht
   * **weg van SMS**: Verzend het bericht van SMS
   * **Push path**: Verzend pushmelding
3. Standaardpad toevoegen voor profielen zonder voorkeur

**Alternatieve benadering**: Gebruik **multi-kanaalacties** waar Journey Optimizer automatisch het beste kanaal selecteert dat op profielvoorkeur en beschikbaarheid wordt gebaseerd.

Leer meer over [ kanaalacties ](journeys-message.md).

+++

+++ Kan ik bepaalde klanten van mijn reis uitsluiten?

Ja, er zijn verschillende manieren om klanten uit te sluiten:

**bij reisingang**:

* Gebruik publieksdefinities met uitsluitingsregels
* Itemvoorwaarden toevoegen waarmee specifieke profielen worden uitgefilterd
* Naamruimtevereisten configureren

**binnen de reis**:

* Voeg een Condition-activiteit toe aan het begin van de rit om ongewenste profielen af te sluiten
* Controleren op uitsluitingskenmerken (bijvoorbeeld VIP-status, testaccounts)
* De kwalificatie van het publiek gebruiken om profielen te identificeren om uit te sluiten

**de uitsluitingsscenario&#39;s van het Voorbeeld**:

* Exclusief klanten die onlangs hebben aangeschaft
* VIP-klanten uitsluiten van standaardaanbiedingen
* Exclusief werknemers en testaccounts
* Klanten in specifieke regio&#39;s uitsluiten

Leer meer over [ ingangsbeheer ](entry-management.md) en [ voorwaarden ](condition-activity.md).

+++

## Geavanceerde concepten

+++ Wat is een naamruimte voor reizen en waarom is dat belangrijk?

A **namespace** is een identiteitstype (b.v., e-mail, ECID, telefoonaantal) dat bepaalt hoe de profielen in de reis worden geïdentificeerd. De naamruimte definieert welke id wordt gebruikt om profielen aan te passen, moet consistent zijn voor gebeurtenissen, publiek en profielgegevens en heeft invloed op het invoeren van de reis en het gedrag van de nieuwe gebruiker.

**Beste praktijken**: Kies een namespace die betrouwbaar uw klanten over alle aanrakingspunten identificeert.

Leer meer over [ identiteitsnaamruimten ](../audience/get-started-identity.md).

+++

+++ Kunnen de profielen de zelfde reis veelvoudige tijden ingaan?

Ja, afhankelijk van de **re-entry montages**:

* **staat re-ingang** toe: De profielen kunnen de reis veelvoudige tijden na het voltooien ingaan
* **re-ingang wacht periode**: Bepaal een minimumtijd tussen reisingangen (b.v., 7 dagen)
* **de terugkeer van de Kracht op gebeurtenis**: Trigger een nieuwe reisinstantie zelfs als het profiel reeds in de reis is

**Beste praktijken**: Gebruik re-entry regels om berichtvermoeidheid te verhinderen en aangewezen het passen te verzekeren.

Leer meer over [ ingangsbeheer ](entry-management.md).

+++

+++ Wat is een optimalisatie tijdens het verzenden?

**Send-Time Optimalisering (STO)** gebruikt AI om de beste tijd te voorspellen om een bericht naar elk individueel profiel te verzenden, maximaliserend open tarieven en overeenkomst. De STO analyseert historische betrokkenheidspatronen om te bepalen wanneer elke ontvanger het meest waarschijnlijk met uw bericht in wisselwerking zal staan.

**Voordelen**:

* Verbeterde open en kliksnelheden
* Betere klantervaring door optimaal getimed berichten
* Verlaagde afmeldingsrechten

Leer meer over [ verzenden-tijd optimalisering ](send-time-optimization.md).

+++

+++ Wat zijn regels voor het afdekken van reizen?

**Kaart van de Reis** staat u toe om het aantal tijden te beperken een profiel reizen binnen een gespecificeerde tijdspanne kan ingaan, die berichtmoeheid verhinderen en optimale klantenervaring verzekeren. U kunt maximale gegevens per profiel instellen voor reizen of specifieke reizen, tijdvensters definiëren (dagelijks, wekelijks, maandelijks) en reizen prioriteren wanneer meerdere reizen met hetzelfde profiel concurreren.

Leer meer over [ aftappen van de reis ](../conflict-prioritization/journey-capping.md).

+++

+++ Kan ik mijn reis integreren met externe systemen?

Ja. Het gebruik **douaneacties** om derde APIs (CRM, marketing automatisering, loyaliteitssystemen) te roepen, gegevens naar externe systemen te verzenden, informatie in real time voor besluit terug te winnen, en werkschema&#39;s in externe platforms teweeg te brengen.

Aangepaste acties ondersteunen verificatie (API-sleutel, OAuth 2.0), aanpassing van de payload voor aanvragen/antwoorden, foutafhandeling en time-outs en dynamische parameters vanuit de reiscontext.

Leer meer over [ douaneacties ](using-custom-actions.md).

+++

+++ Hoe kan ik Adobe Campaign gebruiken voor reizen?

Journey Optimizer integreert native met Adobe Campaign om zijn geavanceerde mogelijkheden te benutten:

* **Adobe Campaign Standard**: De acties van Campaign Standard van het gebruik om transactionele berichten te verzenden
* **Adobe Campaign v7/v8**: De werkschema&#39;s van de Campagne van de Trigger en gebruiks de leveringsinfrastructuur van de Campagne

**Beste praktijken**: Gebruik deze integratie als u bestaande malplaatjes van de Campagne, gegevensmodellen hebt, of campagne-specifieke eigenschappen vereist.

Leer meer over [ integratie van de Campagne ](ajo-ac.md).

+++

+++ Wat is de pompactiviteit?

De **activiteit van de Jump** staat u toe om profielen van één reis aan een andere over te brengen, toelatend herbruikbare wegpatronen, reis orchestratie over veelvoudige reizen, vereenvoudigd reisonderhoud, en progressieve betrokkenheidsstrategieën.

Wanneer een profiel een sprongactiviteit bereikt, sluiten zij de huidige reis en gaan de doelreis bij zijn uitgangspunt in.

Leer meer over [ de activiteit van de Sprong ](jump.md).

+++

+++ Hoe maak ik een welkomstreis?

Een typische welkomstserie omvat meerdere aanraakpunten over een aantal dagen:

**structuur van het Voorbeeld**:

1. **Ingang**: Publiek van nieuwe abonnees of gebeurtenis wanneer iemand omhoog ondertekent
2. **E-mail 1 - Onmiddellijk welkom**: Dank u en inleiding
3. **wacht**: 2 dagen
4. **E-mail 2 - Aan de slag**: Leerprogramma of productgids
5. **wacht**: 3 dagen
6. **Voorwaarde**: Heeft de klant een aankoop gedaan?
   * **ja**: Eind of beweeg aan klantenreis
   * **Nr**: Ga welkome reeksen voort
7. **E-mail 3 - Stimulerend**: Speciale eerste-tijd koperskorting
8. **wacht**: 5 dagen
9. **E-mail 4 - Betrokkenheid**: Beste verkopers of populaire inhoud

**Beste praktijken**:

* Houd het 3-5 e-mails gedurende 2-3 weken
* Elke e-mail moet een duidelijk doel hebben en call-to-action
* Open snelheden bewaken en timing/inhoud dienovereenkomstig aanpassen
* Klanten vroegtijdig afsluiten als ze hun producten converteren of sterk engageren

Leer meer over [ gevallen van het reisgebruik ](jo-use-cases.md).

+++

+++ Kan I A/B verschillende wegen in mijn reis testen?

Ja. Gebruik **optimaliseer activiteit** (beschikbaar in specifieke pakketten van Journey Optimizer) of creeer manueel testspleten:

**Gebruikend optimaliseer activiteit**:

* Verkeer automatisch splitsen tussen varianten
* Test verschillende berichten, aanbiedingen of volledige reispaden
* Hiermee worden de prestaties gemeten en wordt een winnaar gedeclareerd

**Hand het testen met Voorwaarde**:

* Een voorwaarde maken die profielen willekeurig splitst (bijvoorbeeld met een willekeurige numerieke functie)
* Verschillende ervaringen naar elke splitsing verzenden
* Resultaten meten aan de hand van reisrapporten

**wat u** kunt testen:

* Verschillende onderwerpregel voor e-mail
* Alternatieve berichtinhoud
* Verschillende wachttijden
* Verschillende aanbiedingen of stimulansen
* Volledig verschillende reispaden

Leer meer over [ activiteit ](optimize.md) optimaliseren en [ inhoudexperimenten ](../content-management/content-experiment.md).

+++

+++ Hoe activeer ik een reis als de voorraad laag is?

Creeer de reis van de a **bedrijfsgebeurtenis**:

1. **vorm een bedrijfsgebeurtenis**: Opstelling een gebeurtenis die door uw inventarissysteem wordt teweeggebracht wanneer de voorraad onder een drempel daalt
2. **Uitgezochte doelpubliek**: Kies profielen om (b.v., klanten op de hoogte te brengen die het product, abonnees bekeken hervoorraadalarm) bekeken
3. **voeg berichtactie** toe: Verzend bericht e-mail of duw
4. **personaliseer inhoud**: Omvat productdetails, huidig inventarisniveau, urgentieoverseinen

**Van het bedrijfs voorbeeld gebeurtenissen**:

* Lage voorraadwaarschuwing
* Prijsdalingsmelding
* Product terug in voorraad
* Aankondiging van Flash-verkoop
* Op weersomstandigheden gebaseerde promoties

Leer meer over [ bedrijfsgebeurtenissen ](general-events.md).

+++

+++ Kan ik een reis voor een bepaalde persoon pauzeren zonder de hele reis te stoppen?

Hoewel u een reis voor individuele profielen niet direct kunt pauzeren, kunt u gelijkaardige resultaten bereiken:

**Opties**:

* **toevoegt aan uitsluitingspubliek**: Creeer een publiek van profielen om een voorwaarde uit te sluiten en toe te voegen die dit publiek op strategische punten in de reis controleert
* **de profielattributen van de Update**: Plaats een &quot;pauze&quot;vlag op het profiel en de gebruiksvoorwaarden om acties voor gemarkeerde profielen over te slaan
* **Actie van de Douane**: Gebruik een extern systeem om gepauzeerde profielen te volgen en status via API vraag te controleren
* **Handmatige uitgang**: Voor dringende gevallen, kunt u testprofielen manueel verwijderen

**Nota**: De veranderingen van de reis beïnvloeden slechts nieuwe toetreders. Profielen die al op reis zijn volgen het originele pad, tenzij de reis volledig wordt gestopt.

+++

+++ Wat is het verschil tussen een Voorwaarde en een Wacht activiteit?

**de activiteit van de Voorwaarde**:

* **Doel**: Creeert verschillende wegen die op logica (als/toen) worden gebaseerd
* **Functie**: Evalueert dienovereenkomstig gegevens en routeprofielen
* **de gevallen van het Gebruik**: De klanten van het segment, controlestatus, tak die op gedrag wordt gebaseerd
* **Voorbeeld**: Als de klant VIP is, verzend premieaanbieding; anders verzend standaardaanbieding

**wacht activiteit**:

* **Doel**: Pauzeert de reis voor een periode
* **Functie**: houdt profielen op een specifiek punt alvorens verder te gaan
* **de gevallen van het Gebruik**: Het timing tussen berichten, die op bedrijfsuren wachten, die vertragingen creëren
* **Voorbeeld**: Wacht 3 dagen na welkome e-mail alvorens volgende bericht te verzenden

**zij werken samen**:

* Wacht op een periode, dan gebruik een Voorwaarde om te controleren of iets tijdens het wachten gebeurde
* Voorbeeld: wacht 7 dagen en controleer vervolgens of de klant een aankoop heeft gedaan

Leer meer over [ voorwaarden ](condition-activity.md) en [ wachten activiteiten ](wait-activity.md).

+++

## Best practices en beperkingen

+++ Wat zijn de belangrijkste beperkingen die ik zou moeten kennen?

Belangrijke instructies zijn:

* **de ingewikkeldheid van de Reis**: Maximale activiteiten, wegen, en het nestelen niveaus
* **Output**: Het bericht die tarieven en API vraaggrenzen verzendt
* **tijd-aan-levende**: Maximale reisduur (b.v., 91 dagen voor unitaire reizen)
* **grootte van de Publiek**: Beperkingen op gelezen grootte van de publiekspartij
* **Complexiteit van de Uitdrukking**: De grenzen van het karakter in voorwaarden en verpersoonlijking

Volledige van de mening [ begeleiding en beperkingen ](../start/guardrails.md).

+++

+++ Wat zijn de beste praktijken voor reisontwerp?

**Structuur en organisatie**:

* Reizen concentreren op specifieke gebruiksgevallen
* Beschrijvende naamgeving gebruiken voor activiteiten
* Notities en labels toevoegen voor complexe logica
* Groepeer gerelateerde reizen met tags

**Prestaties**:

* De wachttijden optimaliseren om service en volume in evenwicht te brengen
* Externe API-aanroepen beperken tot essentiële gebruiksgevallen
* Afdekkingsregels gebruiken om vermoeidheid van berichten te voorkomen
* Reismeetgegevens regelmatig controleren

**het Testen**:

* Reizen altijd testen voordat ze worden gepubliceerd
* Alle voorwaardelijke paden en scenario&#39;s testen
* Gebruik realistische testprofielen
* Verpersoonlijking en dynamische inhoud valideren

**Onderhoud**:

* Reisprestaties regelmatig evalueren
* Ongebruikte reizen archiveren of sluiten
* Logica en bedrijfsregels voor documentreizen
* Plan voor het versieren van reizen

Leer meer over [ beste praktijken van het reisontwerp ](using-the-journey-designer.md).

+++

+++ Hoeveel activiteiten kan ik toevoegen aan een reis?

Hoewel er geen strikte beperking is op het aantal activiteiten, kunnen zeer complexe reizen (50+ activiteiten) moeilijk worden om te onderhouden en problemen op te lossen. Grote reizen met veel vertakkingen en omstandigheden kunnen gevolgen hebben voor de verwerkingstijd en de leesbaarheid.

**Beste praktijken**: Als uw reis te complex wordt, overweeg het breken in veelvoudige reizen gebruikend de activiteit van de Reliëf, creërend herbruikbare sub-reizen, of vereenvoudigend logica met efficiëntere voorwaarden.

Leer meer over [ reisontwerp ](using-the-journey-designer.md).

+++

+++ Hoe kan ik ervoor zorgen dat mijn reis goed functioneert op schaal?

**overwegingen van het Ontwerp**:

* Gebruik op publiek-gebaseerde ingang voor partijmededelingen in plaats van individuele gebeurtenissen
* Voer aangewezen wachttijden uit om berichtvolume te verspreiden
* Gebruikmaken van plafondregels om overbelasting van het systeem te voorkomen
* Logica voor voorwaarden optimaliseren om de complexiteit van de verwerking te verminderen

**Controle**:

* Regelmatig de afmetingen van het traject volgen
* API-prestaties controleren voor aangepaste handelingen
* Foutsnelheden en time-outvoorvallen controleren
* Waarschuwingen instellen voor kritieke fouten tijdens de rit

**Optimalisering**:

* Gebruik de testmodus en droog run om de prestaties te valideren voordat u gaat publiceren
* Externe gegevensbronaanroepen beperken tot essentiële scenario&#39;s
* Veelgebruikte gegevens indien mogelijk in cache plaatsen
* Prestaties van berichtlevering bekijken en optimaliseren

Leer meer over [ reis optimalisering ](../start/guardrails.md).

+++

## Aanvullende bronnen

Raadpleeg de volgende bronnen voor meer informatie en updates:

* [Aan de slag met reizen](journey.md)
* [Uw eerste journey maken](journey-gs.md)
* [Problemen met hulplijnen oplossen](troubleshooting.md)
* [Gebruiksgevallen voor reizen](jo-use-cases.md)
* [ de Beschrijving van het Product van Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
