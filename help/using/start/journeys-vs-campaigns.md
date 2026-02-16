---
solution: Journey Optimizer
product: journey optimizer
title: Reizen en campagnes - Kies de juiste aanpak
description: Vergelijk de Reizen, de Campagnes van de Actie, API-teweeggebrachte Campagnes, en Geordende Campagnes om de juiste benadering voor uw marketing behoeften in Adobe Journey Optimizer te kiezen.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
keywords: reis, campagne, georkestreerd, vergelijking, keuze, beslissing, workflow, realtime, batch, orchestratie, meerdere stappen, gepland, API-geactiveerd, gebeurtenisgestuurd
hide: true
hidefromtoc: true
exl-id: 8b4d010e-4278-49fd-a7d3-dcc706829577
source-git-commit: 4cf2b850561ef99dc8dc8300c41eeedd0cecfe32
workflow-type: tm+mt
source-wordcount: '1602'
ht-degree: 1%

---

# Reizen en campagnes: kies de juiste aanpak {#journeys-vs-campaigns}

[!DNL Adobe Journey Optimizer] biedt vier belangrijkste manieren aan om uw klanten te bereiken en in dienst te nemen: **Reizen**, **Campagnes van de Actie**, **API-teweeggebrachte Campagnes**, en **Geordende Campagnes**. Het schoppen van juiste hangt van af of u 1 :1 organisatie in real time, geplande uitzendingen, gebeurtenis-gedreven berichten, of complexe partijwerkschema&#39;s nodig hebt.

Deze gids helpt u kiezen gebaseerd op uitvoeringsstijl, gegevensbehoeften, en gebruik geval-met een snelle vergelijking, beslissingsboom, en concrete voorbeelden.

## Snelle vergelijkingsoverzicht {#quick-overview}

| Benadering | Best voor | Uitvoerstijl |
|----------|----------|-----------------|
| **Reizen** | De multi-stap, real-time klantenervaringen met voorwaardelijke logica | 1 :1 orkest - elk profiel in hun eigen tempo |
| **Campagnes van de Actie** | Geplande of terugkerende uitzendingen aan publiek | Batchuitvoering - publiek samen verwerkt tijdens verzending |
| **API-teweeggebrachte Campagnes** | Gebeurtenisgestuurde of transactionele berichten van externe systemen | Uitvoering op aanvraag - geactiveerd door API-aanroep met payload |
| **Geordende Campagnes** | Complexe batchworkflows met segmentatie van meerdere entiteiten | Batchcanvas - alle profielen samen verwerkt |

>[!TIP]
>
>**Snelle regel van duim:** heb elke klant nodig om bij hun eigen tempo met logica in real time te bewegen? De Reizen van het gebruik **&#x200B;**. Eén bericht verzenden naar een publiek volgens een planning? De Campagnes van de Actie van het gebruik **&#x200B;**. Triggerend vanaf een extern systeem via API? Gebruik **API-teweeggebrachte Campagnes**. Gegevens van meerdere entiteiten, exacte aantallen of een batchcanvas nodig? Het gebruik **Orchestrated Campaigns**.

## Gedetailleerde vergelijking {#detailed-comparison}

Gebruik deze uitgebreide tabel om de belangrijkste verschillen te begrijpen:

| Functie | Journeys | Handelingscampagnes | API-geactiveerde campagnes | Geordende campagnes |
|---------|----------|------------------|------------------------|----------------------|
| **Primair doel** | Multistep 1 :1 organisatie met klantencontext in real time | Eenmalige of terugkerende berichtlevering aan het publiek | Transactionele of gebeurtenisgestuurde berichten die door externe systemen worden geïnitieerd | Meerdere batchcampagnes met complexe segmentatieworkflows |
| **het type van Canvas** | 1 :1 canvas - elk profiel reist bij hun eigen tempo | Geen canvas - uitvoering van één handeling | Geen canvas - uitvoering van één handeling | Batchcanvas - alle profielen samen verwerkt |
| **stroom van de Uitvoering** | Opeenvolgende handelingen, profiel behoudt status gedurende de hele reis | Gelijktijdige uitvoering voor het gehele publiek | Directe uitvoering per API-aanroep | Workflow met meerdere stappen met activiteiten en overgangen |
| **mechanisme van de Ingang** | Gebeurtenissen, publiek, kwalificaties, bedrijfsevenementen | Handmatige activering en planning | API-aanroep van extern systeem | Geplande uitvoering van batchworkflow |
| **Model van Gegevens** | Realtime profiel + gebeurtenisgegevens | Profielgegevens van Experience Platform-publiek | API-laadgegevens met optioneel profiel opzoeken | Relationele gegevens over meerdere entiteiten (profielen, producten, winkels, boekingen) |
| **Segmentatie** | Vooraf gebouwd publiek + real-time voorwaarden | Vooraf gebouwd publiek uit Experience Platform | Payload-gestuurde doelen (geen gepland publiek) | Op verzoek samengesteld publiek met exacte aantallen binnen canvas |
| **verwerking van het Profiel** | Individueel, real-time (wanneer gebeurtenissen voorkomen) | Batch, allemaal tegelijk | Per API-aanroep, door de lading aangedreven | Batch, allemaal samen met ondersteuning voor meerdere entiteiten |
| **Personalization** | Contextafhankelijke gegevens in realtime + profielkenmerken | Profielkenmerken | Payloadgegevens + optionele profielkenmerken | Gegevens van meerdere entiteiten voor precisie gericht |
| **Complexiteit** | Meerdere stappen met vertakkingen, wachttijden, omstandigheden | Eén handeling of eenvoudige workflow | Eén handeling met ladingstoewijzing | Workflows met meerdere stappen voor batchverwerking met segmentatie, verrijking, splitsingen |
| **Best voor** | Levenscyclusritten van klanten, aan boord gaan, het verlaten van het karretje | Promotiecampagnes, nieuwsbrieven, aankondigingen | Bevestigingen bestellen, waarschuwingen verzenden, opnieuw instellen wachtwoord | Complexe seizoenscampagnes, multi-step promoties, productlanceringen |
| **Timing** | Doorlopend, altijd actief na publicatie | Geplande begin-/einddatums | Op aanvraag, gebeurtenisgestuurd via API | Batchuitvoering volgens schema |
| **het beheer van de Staat** | Houdt klantenstaat voor acties in real time | Statenloze executie | Uitvoering zonder status per oproep | Batchverwerking met werktafels |
| **Gebruik wanneer** | Meerdere aanraakpunten vereist met realtime beslissingslogica | Eenvoudig bericht voor een publiek op een bepaald moment | Extern systeem moet onmiddellijk een bericht activeren | De behoefte aan complexe segmentatie, multi-entiteitsgegevens, of nauwkeurige pre-send tellingen |
| **Unieke mogelijkheden** | Reacties in realtime, wachtactiviteiten, profielgebaseerde plaatsing | Planning, publiek richten, tariefcontrole | API-taaktoewijzing, systeem-naar-systeem activeren | Relationele gegevenssets, segmentatie van meerdere entiteiten, exacte aantallen, verzenden op meerdere niveaus |

## Beslissingsgids {#decision-guide}

Volg deze beslisboom om de juiste benadering te kiezen. Veel merken gebruiken meer dan één type; kies de beste pasvorm voor elk gebruiksgeval.

### Stap 1: Wat is uw uitvoeringsvereiste?

**Echte-tijd, individuele reacties op klantengedrag?**
→ **de Reizen van het Gebruik**
* Profielen moeten in hun eigen tempo worden verplaatst
* Voorwaardelijke logica gebaseerd op gedrag
* De context in real time is kritiek

**Eenvoudige berichtlevering aan een publiek in een gepland tijd?**
→ **de Campagnes van de Actie van het Gebruik**
* Alle profielen ontvangen tegelijkertijd een bericht
* Gepland of terugkerend verzendt
* Geen complexe meerstapslogica nodig

**Onmiddellijk bericht dat door een extern systeem wordt teweeggebracht?**
→ **Gebruik API-teweeggebrachte Campagnes**
* Op aanvraag geactiveerd via API-aanroep
* Personalisatie met betalingsgestuurde personalisatie
* Geen complexe meerstapslogica nodig

**Complexe partijwerkschema met geavanceerde segmentatie?**
→ **Gebruik Geordende Campagnes**
* Gegevens van meerdere entiteiten nodig (producten, winkels, boekingen)
* Exacte aantallen vóór verzending vereisen
* Meerfasebatchverwerking met splitsingen en verrijking

### Stap 2: Valideer uw keuze

| Uw behoeften | Aanbevolen aanpak | Waarom |
|-----------|---------------------|-----|
| Welkom nieuwe klanten met meerdere stappen aan boord | Journeys | Real-time invoer, meerdere aanraakpunten, voorwaardelijke paden |
| Maandelijkse nieuwsbrief naar abonnees sturen | Handelingscampagnes | Eenvoudig gepland bericht voor publiek |
| Afmelden starten met herinneringsreeks | Journeys | Realtime trigger, wachttijden, voorwaardelijke follow-up |
| Aankondiging van promoties aan alle klanten | Handelingscampagnes | Eenmalig bericht, directe levering |
| Inactieve gebruikers opnieuw inschakelen op basis van gedrag | Journeys | Geïnactiveerd door kwalificatie van het publiek, gepersonaliseerd pad |
| Flash-verkoop geactiveerd door een bedrijfsgebeurtenis | Reizen (Business Event) | Realtime trigger die meerdere klanten beïnvloedt |
| Seizoensgebonden promotie met integratie van productcatalogus | Geordende campagnes | Gegevens over meerdere entiteiten, complexe segmentatie, exacte aantallen |
| API-geactiveerd transactiebericht | API-geactiveerde campagnes | Externe systeemtrigger, directe levering |
| Verzenden op meerdere niveaus per boeking | Geordende campagnes | Relaties tussen meerdere entiteiten, één bericht per boeking |

## Belangrijkste uitleg {#key-distinctions}

### Reizen: 1 :1 Real-time orchestratie

**wat het uniek maakt:**
* Elk profiel behoudt de afzonderlijke status en context
* Profielen worden in hun eigen tempo ingevoerd en uitgevoerd
* Besluitvorming in realtime op basis van gedrag en gebeurtenissen
* Wacht activiteiten creeer gepersonaliseerde timing
* Voorwaardelijke vertakking creëert unieke paden per profiel

**Stroom van het Voorbeeld:**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Elke klant ervaart zijn eigen reistijdlijn op basis van zijn acties.

[Meer informatie over reizen](../building-journeys/journey.md)

### Campagnes: eenvoudige batch- of geactiveerde levering

**wat het uniek maakt:**
* Alle profielen tegelijkertijd en op identieke wijze verwerkt
* Uitvoering zonder status - geen context gehandhaafd
* Eenvoudige planning of API-activering
* Ideaal voor omroepcommunicatie

**Stroom van het Voorbeeld:**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Iedereen krijgt de zelfde boodschap tezelfdertijd.

**Types:**
* **Campagnes van de Actie**: Geplande levering aan publiek (éénmalig of terugkomend)
* **API-teweeggebrachte Campagnes**: Op bestelling levering teweeggebracht door een API vraag met ladingsgegevens

[Meer informatie over campagnes](../campaigns/get-started-with-campaigns.md)

### Geordende campagnes: workflows voor het canvas in batches

**wat het uniek maakt:**
* Het canvas van de partij met activiteiten en overgangen (gelijkend op reiscanvas maar partijgeoriënteerd)
* Ondersteuning voor relationele gegevens van meerdere entiteiten (profielen + producten + winkels + boekingen)
* Op aanvraag publiek opbouwen binnen het canvas
* Exacte aantallen vóór verzending (zichtbaarheid vóór verzending)
* Verzending op meerdere niveaus (één bericht per entiteit, bijvoorbeeld per boeking)
* Alle profielen samen verwerkt in batch

**Stroom van het Voorbeeld:**

```
Query customers → Filter by purchase history → Split by region → 
Enrich with product data → Build segments → Send personalized offers → All in one batch execution
```

Combineert werkstroomcomplexiteit met het uitvoeren van batchcampagnes.

[Meer informatie over geordende campagnes](../orchestrated/gs-orchestrated-campaigns.md)

## Voorbeelden van hoofdletters gebruiken {#use-cases}

### Gebruiksgevallen voor reizen

* **terugwinning van het verlaten van de kunst**: teweeggebracht door wagentje voegt gebeurtenis toe, wacht op controle, verzendt herinneringen als geen aankoop
* **Klant aan boord nemen**: De multi-stap welkome reeks met gepersonaliseerde inhoud die op profielgegevens wordt gebaseerd
* **Loyalty rijverbetering**: teweeggebracht wanneer de klant nieuwe rij bereikt, verzend felicitaties en voordelen
* **campagnes van de Verjaardag**: Ingang die op geboortedatum wordt gebaseerd, gepersonaliseerde aanbiedingen
* **re-engagement**: teweeggebracht door publiekskwalificatie (inactiviteit), progressieve outreach

### Gebruiksgevallen voor campagne (activering en activering van API)

**Campagnes van de Actie:**
* **Maandelijkse nieuwsbrieven**: Geplande partijlevering aan abonneesegment
* **Bevorderingsaankondigingen**: Tijd-gevoelige aanbiedingen aan doelpubliek
* **de lanceringen van het Product**: Gecoördineerde aankondiging aan alle klanten
* **seizoensgebonden groeten**: De berichten van de vakantie op specifieke data

**API-teweeggebrachte Campagnes:**
* **Bevestigingen van de Orde**: teweeggebracht door e-commercesysteem na aankoop
* **Verzendingsberichten**: Teweeggebracht door logistiek systeem
* **de alarm van de Rekening**: teweeggebracht door het systeem van de fraudeopsporing
* **Terugstellen van het Wachtwoord**: teweeggebracht door gebruikersactie in toepassing

### Gebruiksgevallen van geordende campagne

* **seizoensgebonden bevordering met catalogusintegratie**: De het productcatalogus van de vraag, identificeert in aanmerking komende klanten, segment door voorkeur, verzend gepersonaliseerde productaanbevelingen
* **opslag-specifieke campagnes**: De klanten van het doel dichtbij specifieke opslagplaatsen met de gegevens van de opslagvoorraad
* **Multi-booking mededelingen**: Verzend één bericht per het boeken (hotelreserveringen, vluchtboekingen)
* **Complexe segmentorkest**: Bouw publiek stap voor stap met verrijking van veelvoudige gegevensbronnen
* **pre-verzendt bevestiging**: Krijg nauwkeurige tellingen van ontvangers alvorens belangrijke campagnes te lanceren

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
| Direct mail | ✅ | ✅ | ❌ | ✅ |

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

Ja. Vele organisaties gebruiken alle vier benaderingen voor verschillende scenario&#39;s:

* **Reizen** voor gedrag, in real time overeenkomst
* **Campagnes van de Actie** voor geplande uitzendingsmededelingen
* **API-teweeggebrachte Campagnes** voor transactionele berichten
* **Geordende Campagnes** voor complexe, gegevens-intensieve partijcampagnes

Gebruik het juiste gereedschap voor elk gebruiksgeval in plaats van voor alles één aanpak te forceren.

+++

+++ Kan ik een campagne omzetten in een reis of andersom?

Nee, u moet de ervaring opnieuw opbouwen in de juiste indeling. U kunt inhoud, soorten publiek en logische concepten echter opnieuw gebruiken.

+++

+++ Welke benadering is gemakkelijker te bouwen?

De Campagnes van de actie zijn typisch het eenvoudigste (enig bericht aan publiek), gevolgd door API-teweeggebrachte Campagnes, Reizen (complexer met multi-step logica), en Geordende Campagnes (het complexst toe te schrijven aan canvaswerkschema en multi-entiteitsmogelijkheden).

+++

+++ Welke schaal is beter voor grote doelgroepen?

Alle vier kunnen goed schalen; de juiste keuze hangt af van uw patroon:

* **lees de Reizen van het publiek** en **Campagnes van de Actie** worden geoptimaliseerd voor grote partijpubliek (één bericht of stroom aan vele profielen tegelijkertijd).
* **Orchestrated Campaigns** excel bij complexe segmentatie met grote datasets en multi-entiteitsgegevens.
* **Eenheid (gebeurtenis-gebaseerde) de procesprofielen van de Schavens** individueel aangezien de gebeurtenissen voorkomen, zodat hangt de schaal van gebeurtenisvolume en productie af.

+++

+++ Kan ik hetzelfde publiek gebruiken voor reizen en campagnes?

Ja. Soorten publiek die zijn gemaakt in [!DNL Adobe Experience Platform] , kunnen worden gebruikt in Journalen, Handelingcampagnes en Geordende campagnes (waarbij de logica van het publiek ook op aanvraag kan worden opgebouwd in het canvas). API-getriggerde campagnes worden aangedreven door de lading en gebruiken niet op dezelfde manier vooraf gebouwde soorten publiek.

+++

## Volgende stappen {#next-steps}

Klaar om te beginnen met bouwen? Bekijk de gedetailleerde documentatie voor uw gekozen aanpak:

* **[wordt begonnen met Reizen](../building-journeys/journey.md)** - de types van Reis, ontwerper, en werkschema
* **[worden begonnen met Campagnes](../campaigns/get-started-with-campaigns.md)** - actie en API-teweeggebrachte campagnes
* **[wordt begonnen met Geordende Campagnes](../orchestrated/gs-orchestrated-campaigns.md)** - de werkschema&#39;s van het canvas van de partij

>[!MORELIKETHIS]
>
>* [&#x200B; de types van Reis vergelijking &#x200B;](../building-journeys/journey.md#journey-types-comparison)
>* [&#x200B; de types van Campagne vergelijking &#x200B;](../campaigns/get-started-with-campaigns.md#campaign-types)
>* [&#x200B; Veelgestelde vragen van de Reis &#x200B;](../building-journeys/journey-faq.md)
>* [&#x200B; Orchestrated FAQ van Campagnes &#x200B;](../orchestrated/orchestrated-campaigns-faq.md)
>* [&#x200B; Beste praktijken &#x200B;](best-practices.md) - gebruiksgevallen in real time en het schrapen met gidsen
