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
source-git-commit: a7da542320a38dbc739ec42ee4926fce1dea1df0
workflow-type: tm+mt
source-wordcount: '2363'
ht-degree: 0%

---


# Veelgestelde vragen {#faq-journeys}

Hieronder vindt u Veelgestelde vragen over Adobe Journey Optimizer-reizen.

Wilt u meer details? Gebruik terugkoppelen opties bij de bodem van deze pagina om uw vraag op te roepen, of met [&#x200B; gemeenschap van Adobe Journey Optimizer &#x200B;](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"} te verbinden.

## Algemene beginselen

+++ Wat is een reis in Adobe Journey Optimizer?

Een reis is een multi-step organisatie die u toestaat om klantenervaringen in real time over veelvoudige kanalen te ontwerpen en uit te voeren. De reizen combineren gebeurtenissen, orkestactiviteiten, acties, en berichten om gepersonaliseerde, contextuele ervaringen tot stand te brengen die op klantengedrag en bedrijfsgebeurtenissen worden gebaseerd.

Leer meer over [&#x200B; reizen &#x200B;](journey.md).

+++

+++ Wat zijn de verschillende soorten reizen?

Adobe Journey Optimizer ondersteunt drie soorten reizen:

* **Eenheidstreizen**: teweeggebracht individueel door een gebeurtenis (b.v., een aankoop, app login). Profielen voeren de reis een voor een in wanneer de gebeurtenis plaatsvindt.
* **lees de reizen van het Publiek**: Begin met een publiek van Adobe Experience Platform en verzend berichten in partij aan alle profielen in dat publiek.
* **de dienstreizen van de Bedrijfs gebeurtenis**: teweeggebracht door bedrijfsgebeurtenissen (b.v., voorraadupdates, weeralarm) die veelvoudige profielen gelijktijdig beïnvloeden.

Leer meer over [&#x200B; reistypes &#x200B;](entry-management.md#types-of-journeys).

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

Leer meer over [&#x200B; reisactiviteiten &#x200B;](about-journey-activities.md).

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

Volg de [&#x200B; geleidelijke gids &#x200B;](journey-gs.md).

+++

+++ Welke voorwaarden zijn er nodig om een reis te kunnen maken?

Vereisten zijn afhankelijk van het type reis:

* **gebeurtenis-teweeggebrachte reizen**: Vorm gebeurtenissen om te bepalen wanneer de profielen de reis zouden moeten ingaan
* **op publiek-gebaseerde reizen**: Creeer publiek in Adobe Experience Platform
* **de verrijking van Gegevens**: De bronnen van opstellingsgegevens om extra informatie terug te winnen
* **de Integraties van de Derde**: Vorm douaneacties als het gebruiken van externe systemen

Leer meer over [&#x200B; reisconfiguratie &#x200B;](../configuration/about-data-sources-events-actions.md).

+++

+++ Kan ik gegevens van externe systemen gebruiken tijdens mijn reis?

Ja. U kunt **externe gegevensbronnen** vormen om informatie van derde API diensten terug te winnen en het in uw reisvoorwaarden, verpersoonlijking, of acties te gebruiken. Dit staat u toe om de klantenervaring met gegevens in real time van uw CRM, loyaliteitssystemen, weerdiensten, of andere externe platforms te verrijken.

Leer meer over [&#x200B; externe gegevensbronnen &#x200B;](../datasource/external-data-sources.md).

+++

+++ Hoe voeg ik voorwaarden toe aan mijn reis?

U kunt voorwaarden toevoegen gebruikend de **activiteit van de Voorwaarde** van het orkest palet. Voorwaarden bieden de volgende mogelijkheden:

* Eenvoudige of geavanceerde voorwaarden maken met de expressie-editor
* Splits de reis in veelvoudige wegen die op profielattributen, publiekslidmaatschap, gebeurtenissen, of contextafhankelijke gegevens worden gebaseerd
* Tijdlijnpaden definiëren voor profielen die niet binnen een opgegeven tijd aan de voorwaarde voldoen

Leer meer over [&#x200B; voorwaarden &#x200B;](condition-activity.md).

+++

+++ Kan ik berichten naar profielen verzenden tijdens een reis?

Ja. Journey Optimizer omvat **ingebouwde kanaalacties** die u toestaan om berichten door e-mail, dupberichten, SMS/MMS/RCS, in-app berichten, Webervaringen, code-gebaseerde ervaringen, direct mail, inhoudskaarten, WhatsApp, en LIJN te verzenden. U kunt berichtinhoud rechtstreeks in Journey Optimizer ontwerpen en deze toevoegen als actieactiviteiten tijdens uw reis.

Leer meer over [&#x200B; berichten in reizen &#x200B;](journeys-message.md).

+++

+++ Hoe wacht ik op een specifieke tijd of een bepaalde gebeurtenis op een reis?

Gebruik **wacht activiteit** om de reis voor een gespecificeerde duur of tot een specifieke datum/tijd te pauzeren. Wachten-activiteiten zijn handig voor:

* Verzenden van vervolgberichten na een vertraging (bijvoorbeeld 3 dagen na aankoop)
* Wachten op kantooruren voordat actie wordt ondernomen
* Druppingscampagnes maken met getimede intervallen
* Combineren met voorwaarden om time-outscenario&#39;s te maken

Leer meer over [&#x200B; wachten activiteiten &#x200B;](wait-activity.md).

+++

+++ Kan ik profielgegevens bijwerken binnen een reis?

Ja. Gebruik de **activiteit van het Profiel van de Update** om profielattributen in Adobe Experience Platform te wijzigen die op reisgebeurtenissen of voorwaarden wordt gebaseerd. Dit is nuttig voor het bijwerken van loyaliteitspunten, het registreren van reis mijlpalen, het veranderen van voorkeursinstellingen, of het volgen van de scores van de klantenovereenkomst.

Leer meer over [&#x200B; profielupdates &#x200B;](update-profiles.md).

+++

## Testen en publiceren

+++ Hoe kan ik mijn reis testen voordat ik het publiceert?

Journey Optimizer biedt twee testmethoden:

* **wijze van de Test**: Simuleer individuele profielen die door de reis stap voor stap bewegen, toestaand u om logica, voorwaarden, en acties te verifiëren alvorens te leven.
* **Droog looppaswijze**: Voer uw reis uit gebruikend echte productiegegevens zonder daadwerkelijke klanten te contacteren of profielinformatie bij te werken. Dit geeft u vertrouwen in doelgerichtheid en reisontwerp.

**Beste praktijken**: Test altijd reizen alvorens te publiceren om ervoor te zorgen zij werken zoals verwacht en om om het even welke kwesties vroegtijdig te identificeren.

Leer meer over [&#x200B; testwijze &#x200B;](testing-the-journey.md) en [&#x200B; droge looppas &#x200B;](journey-dry-run.md).

+++

+++ Wat gebeurt er als ik een reis publiceer?

Wanneer u een reis publiceert:

* De reis wordt **actief** en klaar om nieuwe profielen goed te keuren
* Profielen kunnen worden ingevoerd op basis van de entry-criteria (gebeurtenis of publiek)
* Berichten en acties worden uitgevoerd voor profielen die door de reis bewegen
* U kunt een gepubliceerde reis niet rechtstreeks bewerken (u moet een nieuwe versie maken)

Leer meer over [&#x200B; het publiceren reizen &#x200B;](publishing-the-journey.md).

+++

+++ Kan ik een reis wijzigen die al gepubliceerd is?

U kunt een live reis niet rechtstreeks bewerken. Wijzigingen aanbrengen:

1. **creeer een nieuwe versie**: Dupliceer de gepubliceerde reis om een ontwerp versie te creëren
2. **maak uw veranderingen**: Bewerk de ontwerp versie zoals nodig
3. **Test de nieuwe versie**: De testwijze van het gebruik om veranderingen te bevestigen
4. **publiceer de nieuwe versie**: Dit sluit automatisch de vorige versie en activeert nieuwe

Profielen die al onderweg zijn, voltooien de oorspronkelijke versie, terwijl nieuwe profielen de nieuwe versie invoeren.

Leer meer over [&#x200B; reisversies &#x200B;](journey-ui.md#journey-versions).

+++

+++ Hoe stop ik een reis?

U kunt de uitvoering van de reis op verschillende manieren beheren:

* **dicht bij nieuwe ingangen**: De nieuwe profielen van het einde van het ingaan terwijl het toestaan van bestaande profielen om hun reis te voltooien
* **Einde onmiddellijk**: Eind de reis en ga alle profielen weg momenteel in het
* **Pauze**: Tijdelijk de reis tegenhouden en het later hervatten (beschikbaar voor specifieke vervoerstypes)

Leer meer over [&#x200B; beëindigende reizen &#x200B;](end-journey.md).

+++

## Uitvoering van en toezicht op reizen

+++ Hoe kan ik de voortgang van een reis bijhouden?

U kunt de uitvoering van de reis controleren met:

* **Reis Levend Rapport**: De metriek en KPIs van de mening in real time voor uw reis
* **Reis Al Rapport van de Tijd**: Analyseer reisprestaties gebruikend Customer Journey Analytics
* **Gebeurtenissen van de Stap van de Reis**: Toegang gedetailleerde uitvoeringsgegevens voor douane het melden
* **Dashboard van de Looppas van de Droog van de Reis**: De resultaten van de testuitvoering van het overzicht alvorens live te gaan

Leer meer over [&#x200B; reis rapporterend &#x200B;](report-journey.md).

+++

+++ Waarom kwam er geen profiel op mijn reis?

De profielen met algemene redenen mogen geen reis maken:

* **Gebeurtenis niet ontvangen**: De het teweegbrengen gebeurtenis werd niet verzonden of behoorlijk gevormd
* **niet voldaan aan de criteria van het publiek**: Het profiel kwalificeert niet voor het ingangspubliek
* **Regels van de Wedertoetreding**: Het profiel voltooide onlangs de reis en re-entry wordt geblokkeerd
* **niet gepubliceerde Reis**: De reis is in ontwerpstatus
* **Ongeldige namespace**: De reis namespace past niet de profielidentiteit aan
* **Reis gesloten**: De reis keurt nieuwe ingangen niet meer goed

Leer meer over [&#x200B; ingangsbeheer &#x200B;](entry-management.md).

+++

+++ Wat zijn trapsgewijze gebeurtenissen en hoe kan ik ze gebruiken?

De gebeurtenissen van de wegstap zijn automatisch geproduceerde datasets die gedetailleerde informatie over elke stap vangen een profiel in een reis neemt. Deze omvatten entry- en exit-gebeurtenissen, uitgevoerde handelingen (verzonden berichten, aangeroepen aangepaste handelingen), overgangen (verplaatsen tussen activiteiten) en fouten en time-outs.

**gevallen van het Gebruik**:

* Aangepaste rapporten samenstellen in Customer Journey Analytics- of BI-gereedschappen
* Problemen met het uitvoeren van foutopsporing
* Gedetailleerd profielgedrag bijhouden
* Geavanceerde analysemodellen en attributiemodellen maken

Leer meer over [&#x200B; gebeurtenissen van de reisstap &#x200B;](../reports/sharing-overview.md).

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

Leer meer over [&#x200B; het oplossen van problemenreizen &#x200B;](troubleshooting.md).

+++

+++ Wat gebeurt er als een actie mislukt op een reis?

Wanneer een actie ontbreekt (b.v., de onderbrekingen van de API vraag, fout van de berichtlevering), gaat de reis door gebrek tenzij anders gevormd verder. U kunt voorwaardenactiviteiten bepalen om mislukkingsscenario&#39;s te behandelen, en de fouten worden het programma geopend reisrapporten en stapgebeurtenissen voor controle.

**Beste praktijken**: Plaats aangewezen onderbrekingswaarden voor externe acties en bepaal alternatieve wegen voor kritieke mislukkingsscenario&#39;s.

Leer meer over [&#x200B; actierespons &#x200B;](../action/action-response.md).

+++

## Geavanceerde concepten

+++ Wat is een naamruimte voor reizen en waarom is dat belangrijk?

A **namespace** is een identiteitstype (b.v., e-mail, ECID, telefoonaantal) dat bepaalt hoe de profielen in de reis worden geïdentificeerd. De naamruimte definieert welke id wordt gebruikt om profielen aan te passen, moet consistent zijn voor gebeurtenissen, publiek en profielgegevens en heeft invloed op het invoeren van de reis en het gedrag van de nieuwe gebruiker.

**Beste praktijken**: Kies een namespace die betrouwbaar uw klanten over alle aanrakingspunten identificeert.

Leer meer over [&#x200B; identiteitsnaamruimten &#x200B;](../audience/get-started-identity.md).

+++

+++ Kunnen de profielen de zelfde reis veelvoudige tijden ingaan?

Ja, afhankelijk van de **re-entry montages**:

* **staat re-ingang** toe: De profielen kunnen de reis veelvoudige tijden na het voltooien ingaan
* **re-ingang wacht periode**: Bepaal een minimumtijd tussen reisingangen (b.v., 7 dagen)
* **de terugkeer van de Kracht op gebeurtenis**: Trigger een nieuwe reisinstantie zelfs als het profiel reeds in de reis is

**Beste praktijken**: Gebruik re-entry regels om berichtvermoeidheid te verhinderen en aangewezen het passen te verzekeren.

Leer meer over [&#x200B; ingangsbeheer &#x200B;](entry-management.md).

+++

+++ Wat is een optimalisatie tijdens het verzenden?

**Send-Time Optimalisering (STO)** gebruikt AI om de beste tijd te voorspellen om een bericht naar elk individueel profiel te verzenden, maximaliserend open tarieven en overeenkomst. De STO analyseert historische betrokkenheidspatronen om te bepalen wanneer elke ontvanger het meest waarschijnlijk met uw bericht in wisselwerking zal staan.

**Voordelen**:

* Verbeterde open en kliksnelheden
* Betere klantervaring door optimaal getimed berichten
* Verlaagde afmeldingsrechten

Leer meer over [&#x200B; verzenden-tijd optimalisering &#x200B;](send-time-optimization.md).

+++

+++ Wat zijn regels voor het afdekken van reizen?

**Kaart van de Reis** staat u toe om het aantal tijden te beperken een profiel reizen binnen een gespecificeerde tijdspanne kan ingaan, die berichtmoeheid verhinderen en optimale klantenervaring verzekeren. U kunt maximale gegevens per profiel instellen voor reizen of specifieke reizen, tijdvensters definiëren (dagelijks, wekelijks, maandelijks) en reizen prioriteren wanneer meerdere reizen met hetzelfde profiel concurreren.

Leer meer over [&#x200B; aftappen van de reis &#x200B;](../conflict-prioritization/journey-capping.md).

+++

+++ Kan ik mijn reis integreren met externe systemen?

Ja. Het gebruik **douaneacties** om derde APIs (CRM, marketing automatisering, loyaliteitssystemen) te roepen, gegevens naar externe systemen te verzenden, informatie in real time voor besluit terug te winnen, en werkschema&#39;s in externe platforms teweeg te brengen.

Aangepaste acties ondersteunen verificatie (API-sleutel, OAuth 2.0), aanpassing van de payload voor aanvragen/antwoorden, foutafhandeling en time-outs en dynamische parameters vanuit de reiscontext.

Leer meer over [&#x200B; douaneacties &#x200B;](using-custom-actions.md).

+++

+++ Hoe kan ik Adobe Campaign gebruiken voor reizen?

Journey Optimizer integreert native met Adobe Campaign om zijn geavanceerde mogelijkheden te benutten:

* **Adobe Campaign Standard**: De acties van Campaign Standard van het gebruik om transactionele berichten te verzenden
* **Adobe Campaign v7/v8**: De werkschema&#39;s van de Campagne van de Trigger en gebruiks de leveringsinfrastructuur van de Campagne

**Beste praktijken**: Gebruik deze integratie als u bestaande malplaatjes van de Campagne, gegevensmodellen hebt, of campagne-specifieke eigenschappen vereist.

Leer meer over [&#x200B; integratie van de Campagne &#x200B;](ajo-ac.md).

+++

+++ Wat is de pompactiviteit?

De **activiteit van de Jump** staat u toe om profielen van één reis aan een andere over te brengen, toelatend herbruikbare wegpatronen, reis orchestratie over veelvoudige reizen, vereenvoudigd reisonderhoud, en progressieve betrokkenheidsstrategieën.

Wanneer een profiel een sprongactiviteit bereikt, sluiten zij de huidige reis en gaan de doelreis bij zijn uitgangspunt in.

Leer meer over [&#x200B; de activiteit van de Sprong &#x200B;](jump.md).

+++

## Best practices en beperkingen

+++ Wat zijn de belangrijkste beperkingen die ik zou moeten kennen?

Belangrijke instructies zijn:

* **de ingewikkeldheid van de Reis**: Maximale activiteiten, wegen, en het nestelen niveaus
* **Output**: Het bericht die tarieven en API vraaggrenzen verzendt
* **tijd-aan-levende**: Maximale reisduur (b.v., 91 dagen voor unitaire reizen)
* **grootte van de Publiek**: Beperkingen op gelezen grootte van de publiekspartij
* **Complexiteit van de Uitdrukking**: De grenzen van het karakter in voorwaarden en verpersoonlijking

Volledige van de mening [&#x200B; begeleiding en beperkingen &#x200B;](../start/guardrails.md).

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

Leer meer over [&#x200B; beste praktijken van het reisontwerp &#x200B;](using-the-journey-designer.md).

+++

+++ Hoeveel activiteiten kan ik toevoegen aan een reis?

Hoewel er geen strikte beperking is op het aantal activiteiten, kunnen zeer complexe reizen (50+ activiteiten) moeilijk worden om te onderhouden en problemen op te lossen. Grote reizen met veel vertakkingen en omstandigheden kunnen gevolgen hebben voor de verwerkingstijd en de leesbaarheid.

**Beste praktijken**: Als uw reis te complex wordt, overweeg het breken in veelvoudige reizen gebruikend de activiteit van de Reliëf, creërend herbruikbare sub-reizen, of vereenvoudigend logica met efficiëntere voorwaarden.

Leer meer over [&#x200B; reisontwerp &#x200B;](using-the-journey-designer.md).

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

Leer meer over [&#x200B; reis optimalisering &#x200B;](../start/guardrails.md).

+++

## Aanvullende bronnen

Raadpleeg de volgende bronnen voor meer informatie en updates:

* [Aan de slag met reizen](journey.md)
* [Uw eerste journey maken](journey-gs.md)
* [Problemen met hulplijnen oplossen](troubleshooting.md)
* [Gebruiksgevallen voor reizen](jo-use-cases.md)
* [&#x200B; de Beschrijving van het Product van Journey Optimizer &#x200B;](https://helpx.adobe.com/nl/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
