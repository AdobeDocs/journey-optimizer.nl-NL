---
solution: Journey Optimizer
product: journey optimizer
title: Reizen en campagnes - Kies de juiste aanpak
description: Vergelijk reizen, campagnes en georkestreerde campagnes om de juiste aanpak te kiezen voor uw marketingbehoeften in Adobe Journey Optimizer
feature: Journeys, Campaigns, Get Started, Overview
role: User
level: Beginner
keywords: reis, campagne, georkestreerd, vergelijking, keuze, beslissing, workflow, realtime, batch, orchestratie, meerdere stappen, gepland, API-geactiveerd, gebeurtenisgestuurd
hide: true
hidefromtoc: true
source-git-commit: 3fd971c719bfd667fe5b237c8f03a5915422c1e7
workflow-type: tm+mt
source-wordcount: '1334'
ht-degree: 1%

---


# Reizen en campagnes: kies de juiste aanpak {#journeys-vs-campaigns}

Adobe Journey Optimizer biedt drie krachtige benaderingen om uw klanten te bereiken en erbij te betrekken. Begrijpen wanneer elk moet worden gebruikt is essentieel voor het opbouwen van effectieve marketingervaringen.

Deze gids helpt u tussen **Transparanten**, **Campagnes** (Actie &amp; API-teweeggebracht) kiezen, en **Orchestrated Campagnes** gebaseerd op uw specifieke marketing behoeften.

## Snelle vergelijkingsoverzicht {#quick-overview}

| Benadering | Best voor | Uitvoerstijl |
|----------|----------|-----------------|
| **Reizen** | De multi-stap, real-time klantenervaringen met voorwaardelijke logica | 1 :1 orkest - elk profiel in hun eigen tempo |
| **Campagnes (Actie &amp; API)** | Eenvoudige, geplande of getriggerde berichtlevering | Batch of API geactiveerd - alle profielen tegelijk |
| **Geordende Campagnes** | Complexe batchworkflows met segmentatie van meerdere entiteiten | Batchcanvas - alle profielen samen verwerkt |

## Gedetailleerde vergelijking {#detailed-comparison}

Gebruik deze uitgebreide tabel om de belangrijkste verschillen te begrijpen:

| Functie | Journeys | Campagnes (actie en API-activering) | Geordende campagnes |
|---------|----------|-----------------------------------|----------------------|
| **Primair doel** | Multistep 1 :1 organisatie met klantencontext in real time | Eenmalige of terugkerende berichtlevering aan het publiek | Meerdere batchcampagnes met complexe segmentatieworkflows |
| **het type van Canvas** | 1 :1 canvas - elk profiel reist bij hun eigen tempo | Geen canvas - uitvoering van één handeling | Batchcanvas - alle profielen samen verwerkt |
| **stroom van de Uitvoering** | Opeenvolgende handelingen, profiel behoudt status gedurende de hele reis | Gelijktijdige uitvoering voor het gehele publiek | Workflow met meerdere stappen met activiteiten en overgangen |
| **mechanisme van de Ingang** | Gebeurtenissen, publiek, kwalificaties, bedrijfsevenementen | Handmatige activering, geplande activering of API-trigger | Geplande uitvoering van batchworkflow |
| **Model van Gegevens** | Realtime profiel + gebeurtenisgegevens | Profielgegevens + API-lading | Relationele gegevens over meerdere entiteiten (profielen, producten, winkels, boekingen) |
| **Segmentatie** | Vooraf gebouwd publiek + real-time voorwaarden | Vooraf gebouwd publiek uit Experience Platform | Op verzoek samengesteld publiek met exacte aantallen binnen canvas |
| **verwerking van het Profiel** | Individueel, real-time (wanneer gebeurtenissen voorkomen) | Batch, allemaal tegelijk | Batch, allemaal samen met ondersteuning voor meerdere entiteiten |
| **Personalization** | Contextafhankelijke gegevens in realtime + profielkenmerken | Profielkenmerken + API-laadgegevens | Gegevens van meerdere entiteiten voor precisie gericht |
| **Complexiteit** | Meerdere stappen met vertakkingen, wachttijden, omstandigheden | Eén handeling of eenvoudige workflow | Workflows met meerdere stappen voor batchverwerking met segmentatie, verrijking, splitsingen |
| **Best voor** | Levenscyclusritten van klanten, aan boord gaan, het verlaten van het karretje | Promotiecampagnes, nieuwsbrieven, aankondigingen, transactieberichten | Complexe seizoenscampagnes, multi-step promoties, productlanceringen |
| **Timing** | Doorlopend, altijd actief na publicatie | Geplande begin-/einddatums of API-geactiveerd | Batchuitvoering volgens schema |
| **het beheer van de Staat** | Houdt klantenstaat voor acties in real time | Statenloze executie | Batchverwerking met werktafels |
| **Gebruik wanneer** | Meerdere aanraakpunten vereist met realtime beslissingslogica | Eenvoudig bericht voor publiek op specifiek tijdstip | De behoefte aan complexe segmentatie, multi-entiteitsgegevens, of nauwkeurige pre-send tellingen |
| **Unieke mogelijkheden** | Reacties in realtime, wachtactiviteiten, profielgebaseerde plaatsing | Eenvoudige planning, API-activering, snelheidsbeheer | Relationele gegevenssets, segmentatie van meerdere entiteiten, exacte aantallen, verzenden op meerdere niveaus |

## Beslissingsgids {#decision-guide}

Volg deze beslisboom om de juiste benadering te kiezen:

### Stap 1: Wat is uw uitvoeringsvereiste?

**Echte-tijd, individuele reacties op klantengedrag?**
→ **de Reizen van het Gebruik**
- Profielen moeten in hun eigen tempo worden verplaatst
- Voorwaardelijke logica gebaseerd op gedrag
- De context in real time is kritiek

**Eenvoudige berichtlevering aan een publiek?**
→ **Actie van het Gebruik of API-teweeggebrachte Campagnes**
- Alle profielen ontvangen tegelijkertijd een bericht
- Gepland of geactiveerd via API
- Geen complexe meerstapslogica nodig

**Complexe partijwerkschema met geavanceerde segmentatie?**
→ **Gebruik Geordende Campagnes**
- Gegevens van meerdere entiteiten nodig (producten, winkels, boekingen)
- Exacte aantallen vóór verzending vereisen
- Meerfasebatchverwerking met splitsingen en verrijking

### Stap 2: Valideer uw keuze

| Uw behoeften | Aanbevolen aanpak | Waarom |
|-----------|---------------------|-----|
| Welkom nieuwe klanten met meerdere stappen aan boord | Journeys | Real-time invoer, meerdere aanraakpunten, voorwaardelijke paden |
| Maandelijkse nieuwsbrief naar abonnees sturen | Handelscampagne | Eenvoudig gepland bericht voor publiek |
| Afmelden starten met herinneringsreeks | Journeys | Realtime trigger, wachttijden, voorwaardelijke follow-up |
| Aankondiging van promoties aan alle klanten | Handelscampagne | Eenmalig bericht, directe levering |
| Inactieve gebruikers opnieuw inschakelen op basis van gedrag | Journeys | Geïnactiveerd door kwalificatie van het publiek, gepersonaliseerd pad |
| Flash-verkoop geactiveerd door een bedrijfsgebeurtenis | Reizen (Business Event) | Realtime trigger die meerdere klanten beïnvloedt |
| Seizoensgebonden promotie met integratie van productcatalogus | Geordende campagne | Gegevens over meerdere entiteiten, complexe segmentatie, exacte aantallen |
| API-geactiveerd transactiebericht | API-activering | Externe systeemtrigger, directe levering |
| Verzenden op meerdere niveaus per boeking | Geordende campagne | Relaties tussen meerdere entiteiten, één bericht per boeking |

## Belangrijkste uitleg {#key-distinctions}

### Reizen: 1 :1 Real-time orchestratie

**wat het uniek maakt:**
- Elk profiel behoudt de afzonderlijke status en context
- Profielen worden in hun eigen tempo ingevoerd en uitgevoerd
- Besluitvorming in realtime op basis van gedrag en gebeurtenissen
- Wacht activiteiten creeer gepersonaliseerde timing
- Voorwaardelijke vertakking creëert unieke paden per profiel

**Stroom van het Voorbeeld:**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Elke klant ervaart zijn eigen reistijdlijn op basis van zijn acties.

[Meer informatie over reizen](../building-journeys/journey.md)

### Campagnes: eenvoudige batch- of geactiveerde levering

**wat het uniek maakt:**
- Alle profielen tegelijkertijd en op identieke wijze verwerkt
- Uitvoering zonder status - geen context gehandhaafd
- Eenvoudige planning of API-activering
- Ideaal voor omroepcommunicatie

**Stroom van het Voorbeeld:**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Iedereen krijgt de zelfde boodschap tezelfdertijd.

**Types:**
- **Campagnes van de Actie**: Geplande levering (éénmalig of terugkomend)
- **API-teweeggebrachte Campagnes**: Teweeggebracht via API vraag van externe systemen

[Meer informatie over campagnes](../campaigns/get-started-with-campaigns.md)

### Geordende campagnes: workflows voor het canvas in batches

**wat het uniek maakt:**
- Het canvas van de partij met activiteiten en overgangen (gelijkend op reiscanvas maar partijgeoriënteerd)
- Ondersteuning voor relationele gegevens van meerdere entiteiten (profielen + producten + winkels + boekingen)
- Op aanvraag publiek opbouwen binnen het canvas
- Exacte aantallen vóór verzending (zichtbaarheid vóór verzending)
- Verzending op meerdere niveaus (één bericht per entiteit, bijvoorbeeld per boeking)
- Alle profielen samen verwerkt in batch

**Stroom van het Voorbeeld:**

```
Query customers → Filter by purchase history → Split by region → 
Enrich with product data → Build segments → Send personalized offers → All in one batch execution
```

Combineert werkstroomcomplexiteit met het uitvoeren van batchcampagnes.

[Meer informatie over geordende campagnes](../orchestrated/gs-orchestrated-campaigns.md)

## Voorbeelden van hoofdletters gebruiken {#use-cases}

### Gebruiksgevallen voor reizen

- **terugwinning van het verlaten van de kunst**: teweeggebracht door wagentje voegt gebeurtenis toe, wacht op controle, verzendt herinneringen als geen aankoop
- **Klant aan boord nemen**: De multi-stap welkome reeks met gepersonaliseerde inhoud die op profielgegevens wordt gebaseerd
- **Loyalty rijverbetering**: teweeggebracht wanneer de klant nieuwe rij bereikt, verzend felicitaties en voordelen
- **campagnes van de Verjaardag**: Ingang die op geboortedatum wordt gebaseerd, gepersonaliseerde aanbiedingen
- **re-engagement**: teweeggebracht door publiekskwalificatie (inactiviteit), progressieve outreach

### Gebruiksgevallen voor campagne (activering en activering van API)

**Campagnes van de Actie:**
- **Maandelijkse nieuwsbrieven**: Geplande partijlevering aan abonneesegment
- **Bevorderingsaankondigingen**: Tijd-gevoelige aanbiedingen aan doelpubliek
- **de lanceringen van het Product**: Gecoördineerde aankondiging aan alle klanten
- **seizoensgebonden groeten**: De berichten van de vakantie op specifieke data

**API-teweeggebrachte Campagnes:**
- **Bevestigingen van de Orde**: teweeggebracht door e-commercesysteem na aankoop
- **Verzendingsberichten**: Teweeggebracht door logistiek systeem
- **de alarm van de Rekening**: teweeggebracht door het systeem van de fraudeopsporing
- **Terugstellen van het Wachtwoord**: teweeggebracht door gebruikersactie in toepassing

### Gebruiksgevallen van geordende campagne

- **seizoensgebonden bevordering met catalogusintegratie**: De het productcatalogus van de vraag, identificeert in aanmerking komende klanten, segment door voorkeur, verzend gepersonaliseerde productaanbevelingen
- **opslag-specifieke campagnes**: De klanten van het doel dichtbij specifieke opslagplaatsen met de gegevens van de opslagvoorraad
- **Multi-booking mededelingen**: Verzend één bericht per het boeken (hotelreserveringen, vluchtboekingen)
- **Complexe segmentorkest**: Bouw publiek stap voor stap met verrijking van veelvoudige gegevensbronnen
- **pre-verzendt bevestiging**: Krijg nauwkeurige tellingen van ontvangers alvorens belangrijke campagnes te lanceren

## Beschikbaarheid van functies {#feature-availability}

### Kanalen

| Kanaal | Journeys | Handelingscampagnes | API-geactiveerde campagnes | Geordende campagnes |
|---------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Email | ✅ | ✅ | ✅ | ✅ |
| Push | ✅ | ✅ | ✅ | ✅ |
| Sms | ✅ | ✅ | ✅ | ✅ |
| In-app | ✅ | ✅ | ✅ | ❌ |
| Web | ✅ | ✅ | ❌ | ❌ |
| Op code gebaseerd | ✅ | ✅ | ❌ | ❌ |
| Inhoudskaarten | ✅ | ✅ | ❌ | ❌ |
| Direct mail | ✅ | ✅ | ❌ | ❌ |

### Geavanceerde mogelijkheden

| Capaciteit | Journeys | Handelingscampagnes | API-geactiveerde campagnes | Geordende campagnes |
|-----------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Workflows met meerdere stappen | ✅ | ❌ | ❌ | ✅ |
| Real-time triggers | ✅ | ❌ | ✅ | ❌ |
| Wachten op activiteiten | ✅ | ❌ | ❌ | ✅ |
| Voorwaardelijke vertakking | ✅ | ❌ | ❌ | ✅ |
| Geplande uitvoering | ✅ | ✅ | ✅ | ✅ |
| API-activering | ❌ | ❌ | ✅ | ❌ |
| Gegevens over meerdere entiteiten | ❌ | ❌ | ❌ | ✅ |
| Exacte aantallen vóór verzending | ❌ | ❌ | ❌ | ✅ |
| Segmentatie op aanvraag | ❌ | ❌ | ❌ | ✅ |
| Optimalisatie bij verzending | ✅ | ✅ | ✅ | ✅ |
| A/B-tests | ✅ | ✅ | ❌ | ❌ |
| Goedkeuringswerkstromen | ✅ | ✅ | ✅ | ❌ |

## Algemene vragen {#common-questions}

+++ Kan ik reizen en campagnes combineren in mijn marketingstrategie?

Absoluut! De meeste organisaties gebruiken alle drie benaderingen voor verschillende scenario&#39;s:
- Reizen voor gedragsbetrokkenheid, realtime betrokkenheid
- Actie-campagnes voor geplande uitzendingen
- API-getriggerde campagnes voor transactieberichten
- Geordende campagnes voor complexe, gegevensintensieve batchcampagnes

+++

+++ Kan ik een campagne omzetten in een reis of andersom?

Nee, u moet de ervaring opnieuw opbouwen in de juiste indeling. U kunt inhoud, soorten publiek en logische concepten echter opnieuw gebruiken.

+++

+++ Welke benadering is gemakkelijker te bouwen?

De Campagnes van de actie zijn typisch het eenvoudigste (enig bericht aan publiek), gevolgd door API-teweeggebrachte Campagnes, Reizen (complexer met multi-step logica), en Geordende Campagnes (het complexst toe te schrijven aan canvaswerkschema en multi-entiteitsmogelijkheden).

+++

+++ Welke schaal is beter voor grote doelgroepen?

Alle drie kunnen goed schalen, maar:
- **gelezen de Reizen van het publiek** en **Campagnes van de Actie** worden geoptimaliseerd voor grote partijpubliek
- **Orchestrated Campaigns** excel bij complexe segmentatie met grote datasets
- **de procesprofielen van de Eenheid van de Reizen** individueel, zodat hangt de schaal van gebeurtenisvolume af

+++

+++ Kan ik hetzelfde publiek gebruiken voor reizen en campagnes?

Ja, in Adobe Experience Platform gecreëerd publiek kan in alle drie benaderingen worden gebruikt.

+++

## Volgende stappen {#next-steps}

Klaar om te beginnen met bouwen? Bekijk de gedetailleerde documentatie voor uw gekozen aanpak:

- **[wordt begonnen met Reizen](../building-journeys/journey.md)** - leer over reistypes, ontwerper, en werkschema
- **[worden begonnen met Campagnes](../campaigns/get-started-with-campaigns.md)** - onderzoek Actie en API-teweeggebrachte campagnes
- **[worden begonnen met Geordende Campagnes](../orchestrated/gs-orchestrated-campaigns.md)** - ontdekt de werkschema&#39;s van het partijcanvas

**heb meer hulp nodig bepalend?**
- [Vergelijking van reistypes](../building-journeys/journey.md#journey-types-comparison)
- [Vergelijking van campagne-typen](../campaigns/get-started-with-campaigns.md#campaign-types)
- [Veelgestelde vragen over reizen](../building-journeys/journey-faq.md)
- [Veelgestelde vragen over geordende campagnes](../orchestrated/orchestrated-campaigns-faq.md)

