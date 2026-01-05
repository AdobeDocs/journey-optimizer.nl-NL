---
solution: Journey Optimizer
product: Journey Optimizer
title: Testen, valideren en goedkeuren
description: Ontdek alle test- en goedkeuringsmogelijkheden in Journey Optimizer. Geef een voorvertoning weer van de inhoud, simuleer reizen, test e-mails, voer experimenten uit, detecteer conflicten en stel goedkeuringswerkstromen in voordat u de toepassing start.
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: testen, valideren, goedkeuren, goedkeuring, kwaliteitsborging, qa, testprofielen, personalisatie, rendering, spam-check, content-experiment, a/b-test, conflictdetectie, zaadlijst, proefdrukken, sample-data, goedkeuringswerkstroom, e-mail-test, validatie-workflow
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: f774ce00cea82eca84410bd76f482e53d3c60bf6
workflow-type: tm+mt
source-wordcount: '3103'
ht-degree: 0%

---

# Testen, valideren en goedkeuren{#section-overview}

In deze sectie worden alle test- en goedkeuringsmogelijkheden in Journey Optimizer besproken. U zult hulpmiddelen vinden om inhoud met testprofielen voor te vertonen, reislogica te bevestigen, e-mailteruggeven en spamscores te controleren, A/B experimenten in werking te stellen, conflicten te ontdekken, en de werkschema&#39;s van de opstellingsgoedkeuring te plaatsen.

Deze landingspagina helpt u de juiste testende benadering te kiezen die wordt gebaseerd op wat u bouwt (campagnes versus reizen), begeleidt u door geadviseerde testende werkschema&#39;s, en verleent snelle toegang tot alle test en goedkeuringsmiddelen. Het begin met [&#x200B; kiest uw het testen benadering &#x200B;](#choose-your-testing-approach) hieronder om te identificeren welke hulpmiddelen op uw gebruiksgeval van toepassing zijn.

## Overzicht van de testmogelijkheden

**het Testen beschikbare types:**

* Inhoud het testen: Voorproef en bevestigt berichtinhoud alvorens → [&#x200B; het Testen campagnes &#x200B;](#testing-campaigns), [&#x200B; het Testen van verpersoonlijking &#x200B;](#testing-personalization) te verzenden
* Logische het testen van de reis: Simuleer klantenvooruitgang door wegwegen → [&#x200B; het Testen reizen &#x200B;](#testing-journeys)
* Technische het testen: Bevestig het teruggeven, leverbaarheid, en authentificatie → [&#x200B; Technische bevestiging &#x200B;](#2-technical-validation)
* Het testen van prestaties: Vergelijk inhoudsvariaties gebruikend experimenten A/B → [&#x200B; experimenten van de Inhoud &#x200B;](#content-experiments--ab-testing)
* Conflict het testen: Detecteer campagne en reis overlapt → [&#x200B; de opsporing van het Conflict &#x200B;](#conflict-detection)
* Goedkeuring het testen: Gestructureerde overzichtswerkschema&#39;s alvorens activering → [&#x200B; de werkschema&#39;s van de Goedkeuring &#x200B;](#approval-workflows-for-journeys-and-campaigns)

**Zeer belangrijke mogelijkheden door context:**

| Capaciteit | Van toepassing op | Kanaalbeperkingen | Vereisten | Primair doel | Documentatie |
|------------|-----------|---------------------|--------------|-----------------|---------------|
| [Testprofielen](../using/content-management/test-profiles.md) | Campagnes, reizen | Alle kanalen | Testprofielen gemaakt | Voorvertoning van gepersonaliseerde inhoud weergeven | [&#x200B; Gids &#x200B;](#testing-campaigns) |
| [&#x200B; de inputgegevens van de Steekproef &#x200B;](../using/test-approve/simulate-sample-input.md) | Campagnes, reizen | E-mail, SMS, Push, Web, Code-based, In-app, Content cards | CSV/JSON-bestand | Meerdere varianten voor personalisatie testen | [&#x200B; Gids &#x200B;](#simulate-content-variations) |
| [&#x200B; wijze van de Test &#x200B;](../using/building-journeys/testing-the-journey.md) | Alleen reizen | N.v.t. | Conceptreis, naamruimte geconfigureerd | Profielvoortgang simuleren | [&#x200B; Kaart &#x200B;](#test-your-journey) |
| [&#x200B; Droog looppas &#x200B;](../using/building-journeys/journey-dry-run.md) | Alleen reizen | N.v.t. | Reis gemaakt | Uitvoeringspaden analyseren | [&#x200B; Kaart &#x200B;](#journey-dry-run) |
| [E-mailweergave](../using/content-management/rendering.md) | Campagnes, reizen | Alleen e-mail | Litmus-integratie | Weergave op clients controleren | [&#x200B; Werkschema &#x200B;](#2-technical-validation) |
| [&#x200B; Spam score &#x200B;](../using/content-management/spam-report.md) | Campagnes, reizen | Alleen e-mail | Geen | Geldigheidsvalidering | [&#x200B; Werkschema &#x200B;](#2-technical-validation) |
| [&#x200B; Zaadlijsten &#x200B;](../using/configuration/seed-lists.md) | Campagnes, reizen | Alleen e-mail | Zaadlijst geconfigureerd | Toezicht op belanghebbenden | [&#x200B; Kaart &#x200B;](#seed-lists-for-stakeholder-monitoring) |
| [&#x200B; experimenten van de Inhoud &#x200B;](../using/content-management/get-started-experiment.md) | Alleen campagnes | Alle kanalen | Geen | A/B- en meervoudig bewapende bandtests | [&#x200B; Kaart &#x200B;](#content-experiments--ab-testing) |
| [&#x200B; de opsporing van het Conflict &#x200B;](../using/conflict-prioritization/conflicts.md) | Campagnes, reizen (beperkt) | Alle kanalen | Geen | Overseinen door klant voorkomen | [&#x200B; Kaart &#x200B;](#conflict-detection) |
| [&#x200B; de werkschema&#39;s van de Goedkeuring &#x200B;](../using/test-approve/gs-approval.md) | Campagnes, reizen | Alle kanalen | Goedkeuringsbeleid gemaakt | Gestructureerd revisieproces | [&#x200B; Kaart &#x200B;](#approval-workflows-for-journeys-and-campaigns) |
| [&#x200B; de playground van Personalization &#x200B;](../using/personalization/personalize.md#playground) | Alles | Alle kanalen | Geen | Cursussyntaxis voor aanpassen en testen | [&#x200B; Kaart &#x200B;](#personalization-playground) |

**Gemeenschappelijke het testen werkschema&#39;s:**

1. Pre-ontwikkeling: Gebruik [&#x200B; verpersoonlijkings playground &#x200B;](#testing-personalization) om syntaxis te leren
2. Tijdens ontwikkeling: De voorproef met [&#x200B; testprofielen &#x200B;](#testing-campaigns), bevestigt met [&#x200B; gegevens van de steekproefinput &#x200B;](#simulate-content-variations)
3. Pre-lancering: Looppas [&#x200B; technische tests &#x200B;](#2-technical-validation) (teruggeven, spam), controleer [&#x200B; conflicten &#x200B;](#conflict-detection), voorlegt voor [&#x200B; goedkeuring &#x200B;](#approval-workflows-for-journeys-and-campaigns)
4. Post-lancering: De monitor met levende rapporten (zie [&#x200B; Controle &amp; het Oplossen van problemen &#x200B;](#monitoring--troubleshooting)), herhaling gebaseerd op resultaten


## Waarom het testen en goedkeuren belangrijk is

Testen en goedkeuringen dienen als essentiële kwaliteitspoorten die uw merkreputatie beschermen en het succes van de campagne garanderen. Dit is de reden waarom ze belangrijk zijn:

* **de fouten van de Vangst alvorens zij klanten** bereiken - identificeer gebroken verbindingen, onjuiste verpersoonlijking, teruggevende kwesties, en logische onvolkomenheden in een gecontroleerd milieu waar de moeilijke situaties snel en risico-vrij zijn.

* **verbeter leverability** - de spamscores van de Test, bevestigt e-mailauthentificatie, en controleert het teruggeven over e-mailcliënten om inbox plaatsing en betrokkenheidstarieven te maximaliseren.

* **verzeker merkconsistentie** - de inhoud van de voorproef met verschillende testprofielen om te verifiëren dat de verpersoonlijkingsvertoningen correct voor diverse klantensegmenten en handhaaft merknormen.

* **bevestigt complexe reizen** - Simuleer multi-step wegstromen om te bevestigen dat de trekkers correct branden, de voorwaarden evalueren behoorlijk, en de klanten ontvangen de juiste berichten op het juiste ogenblik.

* **Vestig verantwoordingsplicht** - voer formele goedkeuringswerkschema&#39;s uit die van de belanghebbende ondertekening vereisen, creërend duidelijke eigendom en verminderend onbevoegde of premature campagnelanceringen.

* **sparen tijd en middelen** - ontdek kwesties vroeg in de ontwikkelingscyclus wanneer de moeilijke situaties goedkoper en sneller zijn, verhinderend dure post-lanceringscorrecties of de escalaties van de klantendienst.

## Belangrijke terminologie

**[de profielen van de Test](../using/content-management/test-profiles.md)** = Synthetische klantenprofielen (niet echte klanten) die aan voorproef gepersonaliseerde inhoud worden gebruikt. Gemarkeerd in Real-Time Customer Profile Service. Vereist voor testmodus en voorvertoning van inhoud. [&#x200B; Leer hoe te om testprofielen tot stand te brengen &#x200B;](../using/audience/creating-test-profiles.md)

**[de wijze van de Test](../using/building-journeys/testing-the-journey.md)** = de simulatie van de Reis eigenschap die testprofielen door reiswegen verzendt. Beperkingen: alleen conceptreizen; vereist naamruimte, alleen testprofielen. [&#x200B; Zie de documentatie van de testwijze &#x200B;](../using/building-journeys/testing-the-journey.md)

**[Droog looppas](../using/building-journeys/journey-dry-run.md)** = het analysehulpmiddel van de de uitvoeringsanalyse van de Weg dat wegen zonder berichten te verzenden of API vraag te maken traceert. Hoofdlettergebruik: logica valideren zonder bronnen te verbruiken. [&#x200B; Leer over droge looppas &#x200B;](../using/building-journeys/journey-dry-run.md)

**[de inputgegevens van de Steekproef](../using/test-approve/simulate-sample-input.md)** = CSV of JSON dossiers die profielkenmerkwaarden voor het testen van verpersoonlijking bevatten. Ondersteunt maximaal 30 varianten. U kunt ook testprofielen maken. [&#x200B; hoe te om inhoudvariaties &#x200B;](../using/test-approve/simulate-sample-input.md) te simuleren

**[zaadlijsten](../using/configuration/seed-lists.md)** = E-mailadressen van interne belanghebbenden automatisch inbegrepen in daadwerkelijke leveringen (niet test verzendt). Alleen e-mailkanaal. Gebruik hoofdletters/kleine letters: kwaliteitsbewaking en naleving. [&#x200B; vorm zaadlijsten &#x200B;](../using/configuration/seed-lists.md)

**[experimenten van de inhoud](../using/content-management/get-started-experiment.md)** = het testen A/B of multi-gewapende bandit experimenten die inhoudsvariaties vergelijken. Alleen campagnes, niet beschikbaar op reizen. [&#x200B; worden begonnen met experimenten &#x200B;](../using/content-management/get-started-experiment.md) | [&#x200B; creeer experimenten &#x200B;](../using/content-management/content-experiment.md)

**[Proofs](../using/content-management/proofs.md)** = de e-mailleveringen van de Test die naar specifieke e-mailadressen worden verzonden gebruikend de gegevens van het testprofiel. Verschil van zaadlijsten (proefdrukken zijn handtest verzendt, zaadlijsten zijn automatische exemplaren van de belanghebbende). [&#x200B; verzendt proeven &#x200B;](../using/content-management/proofs.md)

**[de opsporing van het Conflict](../using/conflict-prioritization/conflicts.md)** = Hulpmiddel dat overlappende campagnes en reizen identificeert gericht op het zelfde publiek. Beperkte reisondersteuning: alleen eenheids-, Audience Qualification- en Read Audience-typen. [&#x200B; Leer over conflictbeheer &#x200B;](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[de werkschema&#39;s van de Goedkeuring](../using/test-approve/gs-approval.md)** = het multi-step controleproces dat de goedkeuring van de belanghebbende vereist alvorens activering. Vereist configuratie goedkeuringsbeleid. [&#x200B; goedkeuringen van de opstelling &#x200B;](../using/test-approve/gs-approval.md) | [&#x200B; creeer beleid &#x200B;](../using/test-approve/approval-policies.md)

**[teruggevend tests](../using/content-management/rendering.md)** = De vertoningsbevestiging van de e-mail over e-mailcliënten (Gmail, Vooruitzichten, de Post van Apple) en apparaten. Vereist Litmus-integratie. [&#x200B; e-mailteruggeven van de Test &#x200B;](../using/content-management/rendering.md)

**[de playground van Personalization](../using/personalization/personalize.md#playground)** = Interactief het leren milieu om met verpersoonlijkingssyntaxis en testuitdrukkingen met steekproefgegevens te experimenteren. Geen live datasets vereist. [&#x200B; heb toegang tot playground &#x200B;](../using/personalization/personalize.md#playground)

## Beslissingsstructuur voor selectie van testmethoden

Gebruik deze beslissingsboom om snel de juiste testhulpmiddelen voor uw specifiek scenario te identificeren. Beantwoord elke vraag op basis van uw context (wat u bouwt, wat u moet valideren en welk kanaal u gebruikt) om rechtstreeks naar de relevante mogelijkheden en documentatie te navigeren.

+++ **Vraag 1: Wat test u?**

* Campagne → [&#x200B; het Testen campagnes &#x200B;](#testing-campaigns)
* Reis → [&#x200B; het Testen reizen &#x200B;](#testing-journeys)
* De uitdrukkingen van Personalization → [&#x200B; playground van Personalization &#x200B;](#testing-personalization)
+++

+++**Vraag 2: Welk aspect vereist bevestiging?**

* Inhoud en verpersoonlijking → [&#x200B; de profielen van de Test &#x200B;](#testing-campaigns) of [&#x200B; gegevens van de steekproefinput &#x200B;](#simulate-content-variations)
* E-mailvertoning → [&#x200B; e-mail teruggevende tests &#x200B;](#2-technical-validation)
* Leverbaarheid → [&#x200B; Spam scorecontroles &#x200B;](#2-technical-validation)
* De logica van de reis en stroom → [&#x200B; wijze van de Test &#x200B;](#testing-journeys) of [&#x200B; droge looppas &#x200B;](#journey-dry-run)
* De vergelijking van prestaties → [&#x200B; experiment van de Inhoud &#x200B;](#content-experiments--ab-testing) (campagnes slechts)
* De conflicten van de timing → [&#x200B; opsporing van het Conflict &#x200B;](#conflict-detection)
* De revisie van de belanghebbende → [&#x200B; werkschema van de Goedkeuring &#x200B;](#approval-workflows-for-journeys-and-campaigns)
+++

+++**Vraag 3: Welk kanaal?**

* E-mail → Alle beschikbare testende methodes (zie [&#x200B; het Testen campagnes &#x200B;](#testing-campaigns))
* SMS, Duw → [&#x200B; Inhoud het testen &#x200B;](#testing-campaigns), [&#x200B; gegevens van de steekproefinput &#x200B;](#simulate-content-variations), [&#x200B; goedkeuringswerkschema&#39;s &#x200B;](#approval-workflows-for-journeys-and-campaigns)
* Web, in-app, op code-Gebaseerde → [&#x200B; Inhoud het testen &#x200B;](#testing-campaigns), [&#x200B; gegevens van de steekproefinput &#x200B;](#simulate-content-variations), [&#x200B; goedkeuringswerkschema&#39;s &#x200B;](#approval-workflows-for-journeys-and-campaigns)
* Meerdere kanalen → test elk kanaal afzonderlijk
+++

+++**Vraag 4: Wanneer in het werkschema?**

* Alvorens te bouwen → [&#x200B; de playground van Personalization &#x200B;](#personalization-playground) voor het leren
* Tijdens het bouwen → [&#x200B; de profielen van de Test &#x200B;](#testing-campaigns) en [&#x200B; gegevens van de steekproefinput &#x200B;](#simulate-content-variations) voor bevestiging
* Vóór lancering → [&#x200B; het Teruggeven tests &#x200B;](#2-technical-validation), [&#x200B; spamcontroles &#x200B;](#email-spam-report), [&#x200B; conflictopsporing &#x200B;](#conflict-detection), [&#x200B; goedkeuringen &#x200B;](#approval-workflows-for-journeys-and-campaigns)
* Na lancering → [&#x200B; Levende rapporten &#x200B;](../using/building-journeys/report-journey.md) en [&#x200B; controle &#x200B;](#monitoring--troubleshooting)
+++


## Kies uw testbenadering

De juiste testbenadering hangt af van wat u bouwt en wat u moet bevestigen. Gebruik deze gids om de meest relevante testhulpmiddelen voor uw scenario te identificeren.

### Testcampagnes

**voor alle campagnes:**

* De voorproef en test inhoud gebruikend [&#x200B; testprofielen &#x200B;](../using/content-management/test-profiles.md) of [&#x200B; gegevens van de steekproefinput &#x200B;](../using/test-approve/simulate-sample-input.md)
* Controle [&#x200B; e-mailteruggeven &#x200B;](../using/content-management/rendering.md) over apparaten en cliënten (e-mailkanaal slechts)
* De controles van de de spamscore van de looppas [&#x200B; (e-mailkanaal slechts)](../using/content-management/spam-report.md)
* Herzie [&#x200B; conflicten &#x200B;](../using/conflict-prioritization/conflicts.md) met andere campagnes en reizen
* Opstelling [&#x200B; zaadlijsten &#x200B;](../using/configuration/seed-lists.md) voor belanghebbende controle (e-mailkanaal slechts)
* Verzenden voor [&#x200B; goedkeuring &#x200B;](../using/test-approve/gs-approval.md) alvorens activering

**voor het testen A/B en optimalisering:**

* Creeer [&#x200B; inhoudexperimenten &#x200B;](../using/content-management/get-started-experiment.md) om veelvoudige behandelingen te testen en prestaties te meten

**voor API-teweeggebrachte campagnes:**

* Gebruik [&#x200B; de Simulatie API van de Campagne &#x200B;](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} om proefdrukbanen programmatically teweeg te brengen

### Reizen testen

**voor alle reizen:**

* Het gebruik [&#x200B; testwijze &#x200B;](../using/building-journeys/testing-the-journey.md) om profielvooruitgang (ontwerp reizen slechts, vereist namespace) of [&#x200B; droge looppas &#x200B;](../using/building-journeys/journey-dry-run.md) te simuleren om uitvoeringswegen te analyseren zonder berichten te verzenden
* Test individuele berichten gebruikend [&#x200B; voorproef en proeven &#x200B;](../using/content-management/preview-test.md)
* Controle [&#x200B; conflicten &#x200B;](../using/conflict-prioritization/conflicts.md) met andere reizen en campagnes
* Verzenden voor [&#x200B; goedkeuring &#x200B;](../using/test-approve/gs-approval.md) alvorens te publiceren

**voor complexe reizen:**

* De testwijze van het gebruik en droge looppas samen om vertakkende logica en uitvoeringspaden grondig te bevestigen
* Verschillende invoervoorwaarden en profielkenmerken systematisch testen

**Nota:** de opsporing van het Conflict en het aftappen van de reis zijn beschikbaar voor unitary, de Kwalificatie van het Publiek, en slechts de reizen van het Publiek lezen.

### Aanpassing testen

**alvorens inhoud te bouwen:**

* Experimenteer in [&#x200B; verpersoonlijkings playground &#x200B;](../using/personalization/personalize.md#playground) om syntaxis en testuitdrukkingen met steekproefgegevens te leren

**tijdens inhoudsverwezenlijking:**

* De voorproef met [&#x200B; testprofielen &#x200B;](../using/content-management/test-profiles.md) om verpersoonlijkingsteruggeven correct te bevestigen
* Testen veelvoudige scenario&#39;s gebruikend [&#x200B; gegevens van de steekproefinput &#x200B;](../using/test-approve/simulate-sample-input.md) van Csv/JSON- dossiers (steunen tot 30 varianten)

## Best practices testen

Volg de onderstaande aanbevolen procedures om de doeltreffendheid van uw testactiviteiten te maximaliseren:

1. **Test vroeg en vaak** - wacht niet tot een campagne volledig wordt gebouwd. Test inhoud, personalisatie en logica in toenemende mate tijdens uw ontwikkeling.

1. **Gebruik realistische testprofielen** - [&#x200B; creeer testprofielen &#x200B;](../using/audience/creating-test-profiles.md) die nauwkeurig uw doelpubliekssegmenten, met inbegrip van randgevallen en verschillende verpersoonlijkingsscenario&#39;s vertegenwoordigen.

1. **Test over apparaten en cliënten** - verifieer [&#x200B; e-mailteruggevende &#x200B;](../using/content-management/rendering.md) op populaire e-mailcliënten (Gmail, Vooruitzichten, de Post van Apple) en apparaten (Desktop, mobiel, tablet) om verenigbare vertoning (e-mailkanaal slechts) te verzekeren.

1. **bevestigt volledig verpersoonlijking** - test met veelvoudige [&#x200B; testprofielen &#x200B;](../using/content-management/test-profiles.md) die verschillende attributenwaarden hebben om verpersoonlijkingstokens te bevestigen teruggeven correct en het werk van terugvalwaarden. Gebruik [&#x200B; verpersoonlijkingspeler &#x200B;](../using/personalization/personalize.md#playground) om met verpersoonlijkingsuitdrukkingen en testcode met steekproefgegevens te experimenteren alvorens hen op uw campagnes toe te passen.

1. **de inhoudsvariaties van de Test met steekproefgegevens** - Gebruik [&#x200B; gegevens van de steekproefinput &#x200B;](../using/test-approve/simulate-sample-input.md) van CSV of JSON dossiers om tot 30 verpersoonlijkingsscenario&#39;s te testen zonder talrijke testprofielen te creëren, die tijd terwijl het verzekeren van uitvoerige dekking besparen. Ondersteunt kanalen voor e-mail, SMS, push, web, op code gebaseerde ervaring, in-app en inhoudskaarten.

1. **zaadlijsten van het Gebruik voor belanghebbende controle** - vorm [&#x200B; zaadlijsten &#x200B;](../using/configuration/seed-lists.md) om automatisch interne belanghebbenden te omvatten die exemplaren van alle leveringen in uitvoeringstijd voor kwaliteit controle en nalevingscontrole (e-mailkanaal slechts) zullen ontvangen.

1. **Simuleer reiswegen** - voor complexe reizen met veelvoudige takken, gebruik [&#x200B; testwijze &#x200B;](../using/building-journeys/testing-the-journey.md) om verschillende ingangsvoorwaarden en profielattributen te testen om alle mogelijke wegen te bevestigen. Beschikbaar voor conceptreizen die een naamruimte gebruiken.

1. **de leverbaarheidsindicatoren van de Controle** - het spamscores van het Overzicht [&#x200B; &#x200B;](../using/content-management/spam-report.md), authentificatiestatus, en de metriek van de e-mailgezondheid alvorens groot verzendt (e-mailkanaal slechts).

1. **de testresultaten van het Document** - houd verslagen van testresultaten, gevonden kwesties, en resoluties om toekomstige testprocessen te verbeteren en lessen met uw team te delen.

1. **verbind vroege belanghebbenden** - Deel voorproeven en testresultaten met belanghebbenden vóór [&#x200B; formele goedkeuring &#x200B;](../using/test-approve/gs-approval.md) om te verzamelen terugkoppel en richt verwachtingen.

## Aanbevolen testworkflow

Volg deze systematische aanpak om te zorgen voor grondige tests en probleemloze goedkeuringen:

### &#x200B;1. Ontwikkeling van inhoud en voorvertoning

Begin door uw inhoud te creëren en voorproefmogelijkheden te gebruiken om eerste ontwerp en verpersoonlijking te verifiëren:

* Ontwerp uw [&#x200B; e-mail &#x200B;](../using/email/create-email.md), [&#x200B; SMS &#x200B;](../using/sms/create-sms.md), [&#x200B; duw bericht &#x200B;](../using/push/create-push.md), of andere kanaalinhoud

* Gebruik de **[Simuleer inhoud](../using/content-management/preview-test.md)** eigenschap aan voorproef met testprofielen

* De tokens van de controle [&#x200B; van de 1&rbrace; verpersoonlijking &lbrace;, dynamische inhoud, en terugvalwaarden](../using/personalization/personalization-syntax.md)

* Experimenteer met verpersoonlijkingsuitdrukkingen in **[verpersoonlijkings playground](../using/personalization/personalize.md#playground)** om uw code met steekproefgegevens te testen en te raffineren alvorens op levende inhoud van toepassing te zijn

* Test veelvoudige variaties gebruikend **[gegevens van de steekproefinput](../using/test-approve/simulate-sample-input.md)** van Csv/JSON- dossiers om verpersoonlijking over diverse profielscenario&#39;s te bevestigen

* Verifieer [&#x200B; teruggevend &#x200B;](../using/content-management/rendering.md) over verschillende het schermgrootte en e-mailcliënten

### &#x200B;2. Technische validatie

Valideer technische aspecten die gevolgen hebben voor de leverbaarheid en functionaliteit:

* Voer [&#x200B; controles van de spamscore &#x200B;](../using/content-management/spam-report.md) in werking om potentiële leveringskwesties te identificeren

* Koppelingen testen om te controleren of ze niet worden verbroken en correct worden bijgehouden

* Bevestig [&#x200B; e-mailauthentificatie &#x200B;](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC) configuratie

* HTML-rendering controleren en controleren op problemen met CSS-compatibiliteit

* Test [&#x200B; ontvankelijk ontwerp &#x200B;](../using/email/content-from-scratch.md) op mobiele en Desktopapparaten

* Controle voor [&#x200B; potentiële conflicten &#x200B;](../using/conflict-prioritization/conflicts.md) met andere campagnes en reizen om de vermoeidheid en de timingskwesties van het klantenbericht te verhinderen

### &#x200B;3. Reistesten (alleen ritten)

Als u een reis test, bevestig de orkestlogica:

* Activeer **[wijze van de Test](../using/building-journeys/testing-the-journey.md)** om profielvooruitgang door de reis te simuleren

* Test verschillende [&#x200B; ingangsvoorwaarden &#x200B;](../using/building-journeys/entry-management.md) en publiekskwalificaties

* Verifieer [&#x200B; activiteiten &#x200B;](../using/building-journeys/wait-activity.md) wachten, [&#x200B; voorwaarden &#x200B;](../using/building-journeys/condition-activity.md), en vertakkend logisch werk correct

* Gebruik **[Droog looppas](../using/building-journeys/journey-dry-run.md)** voor complexe reizen om uitvoeringspaden te analyseren zonder berichten te verzenden

* Controle dat [&#x200B; gebeurtenissen &#x200B;](../using/event/about-events.md) correct teweegbrengen en [&#x200B; douaneacties &#x200B;](../using/action/about-custom-action-configuration.md) uitvoeren zoals verwacht

### &#x200B;4. Goedkeuringsaanvraag

Nadat het testen is voltooid en de problemen zijn opgelost:

* Verzend de campagne of de reis voor goedkeuring volgens het 0&rbrace; goedkeuringsbeleid van uw organisatie [&#128279;](../using/test-approve/approval-policies.md)

* Omvat testresultaten en documentatie met het [&#x200B; goedkeuringsverzoek &#x200B;](../using/test-approve/request-approval.md)

* Adres om het even welke terugkoppel of veranderingsverzoeken van [&#x200B; fiatteurs &#x200B;](../using/test-approve/review-approve-request.md)

* Breng de noodzakelijke herzieningen aan en test of de wijzigingen significant zijn

### &#x200B;5. Verificatie voorafgaand aan de lancering

Voordat u uw campagne of reis activeert:

* Voer een definitieve overzicht van alle montages, publiek, en [&#x200B; programma&#39;s &#x200B;](../using/building-journeys/journey-properties.md) uit

* Controleren of alle goedkeuringen zijn geïnstalleerd en gedocumenteerd

* Bevestig verzendt tijden en [&#x200B; tijdstreken &#x200B;](../using/building-journeys/timezone-management.md) correct zijn

* Laat [&#x200B; controle en alarm &#x200B;](../using/reports/alerts.md) toe om prestaties na lancering te volgen

### &#x200B;6. Monitor en herhaling

Ga na het opstarten door met de bewaking om eventuele problemen vroeg op te vangen:

* De opstelling [&#x200B; systeemalarm &#x200B;](../using/reports/alerts.md) voor reisfouten, hoge stuittarieven, of lage overeenkomst

* Herzie [&#x200B; levende rapporten &#x200B;](../using/building-journeys/report-journey.md) om prestaties tegen verwachtingen te volgen

* Ben bereid om [&#x200B; reizen te pauzeren of te wijzigen &#x200B;](../using/building-journeys/journey-pause.md) als de kritieke kwesties zich voordoen

* Geleerde documentlessen voor het verbeteren van toekomstige testprocessen

## Testen in actie: gebruik hoofdletters/kleine letters

Zie hoe testconcepten op real-world scenario&#39;s van toepassing zijn:

| Gebruiksscenario | Wat leert u? | Focus van belangrijkste tests |
|----------|-------------------|-------------------|
| **[verzend multi-kanaalberichten](../using/building-journeys/journeys-uc.md)** | Test een reis die het publiek Read, reactiegebeurtenissen, en e-mail/dupberichten combineert. Valideer de volledige stroom van publiek richtend aan berichtlevering. | Coördinatie van meerdere kanalen, reactiegebeurtenissen, end-to-end-stroomvalidatie, test- en publicatiestappen |
| **[verzend een bericht aan abonnees](../using/building-journeys/message-to-subscribers-uc.md)** | Test reizen die abonnementenlijsten met dynamische e-mailadressering als doel hebben. Bevestig verpersoonlijkingsuitdrukkingen voor correcte abonnee richtend. | Personalization-expressies, dynamische adressering, abonnementenlijst gericht |
| **[verzendt tijd-gebonden berichten](../using/building-journeys/weekday-email-uc.md)** | Testritten onder tijdsvoorwaarden om te controleren of berichten op bepaalde dagen worden verzonden. Valideer wachtactiviteiten en planningslogica. | Op tijd gebaseerde voorwaarden, activiteiten wachten, validatie plannen |
| **[Onderzoek meer gevallen van het reisgebruik](../using/building-journeys/jo-use-cases.md)** | Toegang tot uitgebreide verzameling praktische voorbeelden met betrekking tot ervaringsgebeurtenissen, multi-channel berichten en externe systeemintegratie. | Verschillende scenario&#39;s, geavanceerde patronen, integratietests |

## Inhoud testen en goedkeuren

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=nl-NL)

Inhoud voorvertonen, testen en valideren

Leer hoe u persoonlijke inhoud kunt voorvertonen, testen en valideren met testprofielen, e-mailrenderingtests, spamscore-evaluaties en meer.

[Voorvertoning weergeven en inhoud testen](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=nl-NL)

Goedkeuringswerkstromen voor reizen en campagnes

Begrijp hoe u goedkeuringsprocedures instelt, beheert en uitvoert om kwaliteitscontrole voor reizen en campagnes te waarborgen.

[Meer informatie over goedkeuringswerkstromen](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=nl-NL)

Uw reis testen

Valideer uw reis voordat u deze publiceert door deze te testen met specifieke profielen om ervoor te zorgen dat gebeurtenissen, voorwaarden en acties naar behoren werken. Beschikbaar voor conceptreizen die een naamruimte gebruiken.

[Uw reis testen](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=nl-NL)

Reizen op reis

Voer een droge looppas uit om de uitvoeringspad van uw reis te simuleren en te bevestigen, die potentiële kwesties identificeren alvorens live te gaan.

[Meer informatie over Journey Dry run](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=nl-NL)

Bewaking en probleemoplossing

Toegang tot uitgebreide bronnen voor probleemoplossing, systeemwaarschuwingen en foutcodes om problemen met de uitvoering en prestaties van de reis op te lossen.

[Bewaking en probleemoplossing weergeven](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg?lang=nl-NL)

Personalization Playground

Experimenteer met personalisatie-expressies in een veilige omgeving. Test de code met voorbeeldgegevens en geef een voorvertoning van de resultaten weer voordat u deze toepast op uw campagnes en reizen.

[Meer informatie over de Personalization Playground](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

Inhoud-experimenten en A/B-tests

Optimaliseer uw campagnes door veelvoudige inhoudvariaties te testen en prestaties te meten om de best-presterende behandelingen te identificeren. Alleen beschikbaar voor campagnes (ondersteunt A/B- en multigewapende bandiproeven).

[Meer informatie over contentexperimenten](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=nl-NL)

Zaadlijsten voor toezicht door belanghebbenden

Neem automatisch interne adressen van belanghebbenden op in leveringen om de feitelijke berichten te controleren die naar klanten worden verzonden voor kwaliteitsborging en naleving. Alleen beschikbaar voor e-mailkanalen.

[Zaadlijsten configureren](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=nl-NL)

Conflictdetectie

Identificeer potentiële overlappingen tussen campagnes en reizen om overweldigende klanten met teveel gelijktijdige mededelingen te verhinderen. Beschikbaar voor campagnes en unitaire reizen, de Kwalificatie van het Publiek, en gelezen de reizen van het Publiek.

[Conflicten detecteren](../using/conflict-prioritization/conflicts.md)
:::

::::

## Aanvullende bronnen

### Essentiële instructies voor het testen en valideren

* [&#x200B; Simuleer de Variaties van de Inhoud &#x200B;](../using/test-approve/simulate-sample-input.md) - Test tot 30 verpersoonlijkingsscenario&#39;s gebruikend CSV of JSON dossiers. Ideaal voor het testen van meertalige inhoud zonder meerdere testprofielen te maken. Ondersteunt e-mail-, sms-, push-, web-, op code gebaseerde, in-app- en inhoudskaarten.

* [&#x200B; Creërend de Profielen van de Test &#x200B;](../using/audience/creating-test-profiles.md) - creeer en beheer testprofielen om klantenscenario&#39;s te simuleren. Leer hoe u profielen markeert voor testen, kenmerken instelt en testsegmenten ordent.

* [&#x200B; E-mailSpam Rapport &#x200B;](../using/content-management/spam-report.md) - de spamscores van de Controle alvorens te verzenden om leverability en inbox plaatsing te verbeteren. Aanbevelingen voor optimalisatie van inhoud.

* [&#x200B; Veelgestelde vragen van de Reis &#x200B;](../using/building-journeys/journey-faq.md) - Snelle verwijzing voor gemeenschappelijke vragen over reis het testen, uitvoering, en het oplossen van problemen.

### Afhankelijkheden en relaties

Begrijp hoe testmogelijkheden met elkaar en met uw bredere Journey Optimizer-workflows verbinden. Deze sectie brengt eerste vereisten, stroomopwaarts/stroomafwaartse gebiedsdelen, en gemeenschappelijke vermogenscombinaties in kaart.

+++**Vereisten (die vóór het testen worden vereist)**

* Testprofielen moeten worden gemaakt voordat de testmodus of de voorvertoning van de inhoud wordt gebruikt
* Goedkeuringsbeleid moet zijn geconfigureerd voordat het ter goedkeuring wordt ingediend
* Er moeten zaadlijsten worden gemaakt voordat u deze kunt toevoegen aan campagnes/reizen
* Noodintegratie vereist voor tests voor het renderen van e-mail
* De reis moet in ontwerpstatus zijn om testwijze te gebruiken
* De reis moet namespace hebben die wordt gevormd om testwijze te gebruiken

+++

+++**wat het testen afhangt van (stroomopwaarts)**

* Inhoud maken: campagnes of reizen nodig om te testen
* Testprofielen: vereist voor testmodus en voorvertoning van inhoud
* Goedkeuringsbeleid: vereist voor goedkeuringswerkstromen
* Configuratie: kanaalconfiguraties, e-mailverificatie, domeininstellingen

+++

+++**wat van het testen (stroomafwaarts) afhangt**

* Activering campagne/reis: kan niet activeren zonder fouten op te lossen
* Publiceren: goedkeuring is mogelijk vereist voor publicatie
* Live bewaking: monitoring en rapportage na de introductie
* Optimalisatie: gebruik testresultaten om toekomstige campagnes te verfijnen

+++

+++**Verwante mogelijkheden**

* Testen + Goedkeuringswerkstromen = Kwaliteitsborgingsproces
* Testen + Conflictdetectie = Voorkomen van over-messaging voor klanten
* Testen + experimenten met inhoud = optimalisatie van prestaties
* Testen + Rapportage = Continuverbeteringscyclus
* Testprofielen + Personalization = validatie van inhoud
* Droge run + testmodus = Uitgebreide reisvalidatie

+++

+++**Gemeenschappelijke vermogenscombinaties**

* Inhoud testen: testprofielen + invoervoorbeeldgegevens + Personalization-afspeellocatie
* E-mailvalidatie: tests renderen + spamscores + testprofielen + proefdrukken
* Reisvalidatie: testmodus + droge run + testprofielen
* Controlelijst vóór de introductie: alle technische tests + conflictdetectie + goedkeuringswerkstromen

+++

### Algemene vragen

+++**Q: Welke het testen wordt vereist alvorens een campagne te lanceren?**

**Minimum:** de voorproef van de inhoud met testprofielen + Spam score controle (e-mail)
**geadviseerd:** + E-mail teruggevend + de opsporing van het Conflict + het werkschema van de Goedkeuring
**Beste praktijken:** + het testen van de inputgegevens van de Steekproef + Zaadlijsten + A/B experiment (als het optimaliseren)

+++

+++**Q: Hoe test ik verpersoonlijking zonder vele testprofielen te creëren?**

**Primaire oplossing:** 2&rbrace; gegevens van de steekproefinput van het Gebruik &lbrack; met CSV/JSON- dossiers (steunen tot 30 varianten)
[&#128279;](../using/test-approve/simulate-sample-input.md) Alternatief:**creeer 3-5 representatieve** testprofielen  die zeer belangrijke segmenten behandelen
&rbrack;(../using/audience/creating-test-profiles.md) Lerend hulpmiddel:**Experimenteer eerst in** verpersoonlijkings playground [&#128279;](../using/personalization/personalize.md#playground)

+++

+++**Q: Wat is het verschil tussen testwijze en droge looppas voor reizen?**

**de wijze van de Test:** verzendt testprofielen door reis, brengt daadwerkelijke acties teweeg, produceert testberichten. Vereist conceptreis + naamruimte.
**Droog looppas:** vindt uitvoeringswegen zonder om het even wat te verzenden. Werkt met elke reisstatus. Geen berichten verzonden, geen acties uitgevoerd.
**Gebruik samen:** wijze van de Test voor bericht het testen + Dry looppas voor logische bevestiging = uitvoerige dekking.

+++

+++**Q: Kan ik reizen in productie/levende status testen?**

**wijze van de Test:** Nr - ontwerp slechts reizen
**Droog looppas:** ja - de werken op om het even welke reisstatus
**Voorproef van de Inhoud:** ja - voorproef individuele berichten op om het even welk ogenblik
**Oplossing:** Dupliceer levende reis aan ontwerp voor volledige testwijzebevestiging

+++

+++**Q: Welke testende mogelijkheden vereisen externe integratie?**

**E-mail die teruggeeft:** vereist de integratie van de Mus (afzonderlijke vergunning)
**Alle anderen:** Ingebouwd aan Journey Optimizer, geen extra vereiste integratie
**Nota:** de profielen van de Test vereisen de dienst van het Profiel van de Klant in real time (inbegrepen)

+++

+++**Q: Hoe test ik API-teweeggebrachte campagnes?**

**Optie 1:** Gebruik [&#x200B; Simulatie API van de Campagne &#x200B;](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} voor programmatic het testen
**Optie 2:** inhoud van de voorproef met testprofielen in UI
**Optie 3:** verzend proef om e-mailadressen te testen
**Beste praktijken:** combineer alle drie voor uitvoerige bevestiging

+++


### Verwante onderwerpen

* [&#x200B; het Beheer van de Inhoud &#x200B;](content-management-landing-page.md) - Leer hoe te, voorproef, en beheer inhoud gebruikend malplaatjes, fragmenten, en e-mail Designer. Aanbevolen werkwijzen voor het maken van basisinhoud voor consistente branding.

* [&#x200B; Rapportering &amp; Analytics &#x200B;](reporting-landing-page.md) - analyseer campagne en reisprestaties met uitvoerige rapporten, dashboards, en metriek. Maak gegevensgestuurde besluiten om klantenervaringen te optimaliseren.

* [&#x200B; Configuratie van de Reis &#x200B;](configure-journeys-landing-page.md) - vorm gegevensbronnen, gebeurtenissen, en douaneacties om verfijnde reisorchestratie toe te laten. De technische grondslagen leggen voor het creëren van reizen.

* [&#x200B; Beheer van de Campagne &#x200B;](../using/campaigns/get-started-with-campaigns.md) - onderzoek verschillende campagneretypes en leer hoe te, partij en in real time campagnes voor maximumeffect tot stand brengen te plannen en te optimaliseren.
