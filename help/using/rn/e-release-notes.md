---
solution: Journey Optimizer
product: journey optimizer
title: Pre-release notities voor Journey Optimizer
description: Adobe Journey Optimizer Pre-Release notities
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: b7e8f139508ca9418c1b8941bc7ccd84f7f0661c
workflow-type: tm+mt
source-wordcount: '2067'
ht-degree: 1%

---

# Pre-release notities {#e-release-notes}

[!DNL Adobe Journey Optimizer] Continu nieuwe functies, verbeteringen aan bestaande functies en bugfixes geleverd. Alle wijzigingen worden aan het einde van elke maand samengevoegd in de [release notes](release-notes.md).


## Voorafgaande notities januari &#39;26 {#jan-26-01-rn}

**De pre-release notities hieronder kunnen zonder voorafgaande kennisgeving worden gewijzigd tot de releasedatum**. Links, schermen en bijgewerkte documentatie worden op de releasedatum gepubliceerd in de release notes.

Zie ook [Adobe Experience Platform Pre-release notities](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Releasedatum**: 26 januari 2026

### Nieuwe mogelijkheden {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Actie-activiteit in reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ondersteunt een nieuwe generieke <strong>actieactiviteit</strong> waarmee je zowel single actions als <strong>multi-action inbound action groups</strong> kunt configureren, waardoor de configuratie binnen het journey canvas gestroomlijnd kan worden gestroomlijnd. In het bijzonder maakt deze nieuwe functie mogelijk:</p>
<ul>
<li>Een vereenvoudigde native actieconfiguratie binnen het reiscanvas.</li>
<li>De capaciteit om multi-action inbound action groepen te creëren.</li>
<li>De mogelijkheid om optimalisatie toe te voegen aan elke ingebouwde kanaalactie.</li>
<li>De mogelijkheid om zowel experimenteren als meertalige opties toe te voegen aan elke actie.</li>
</ul>
<p>Voorheen uitgebracht in Beperkte Beschikbaarheid, is deze mogelijkheid nu beschikbaar voor alle omgevingen (Algemene Beschikbaarheid).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aangepaste actiemonitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Krijg dieper inzicht in de gezondheid en prestaties van je aangepaste actie-endpoints met een nieuw <strong>monitoringsdashboard</strong> en verrijkte data over de reisstap-gebeurtenissen. Volg succesvolle oproepen, fouten, doorvoer, responstijden en wachttijden om snel te begrijpen wanneer, waar en waarom afwijkingen optreden.</p>
<p>Voorheen uitgebracht in Beperkte Beschikbaarheid, is deze mogelijkheid nu beschikbaar voor alle omgevingen (Algemene Beschikbaarheid).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Stille Uren / Tijdgebaseerde Uitsluitingen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Quiet hours stelt je in staat tijdsgebaseerde uitsluitingen te definiëren <strong></strong> voor e-mail, sms, Push- en WhatsApp-kanalen. Zij zorgen ervoor dat er geen berichten worden verzonden gedurende specifieke periodes, waardoor u de voorkeuren van klanten en compliance-eisen respecteert. Je kunt stille uren toepassen via <strong>regelsets</strong>, die aan individuele acties in campagnes of reizen kunnen worden toegewezen voor nauwkeurige controle.</p>
<p>Voorheen uitgebracht in beperkte beschikbaarheid, is deze functie nu beschikbaar voor alle omgevingen. Met deze General Availability-release bevat de functie nu de mogelijkheid voor klanten om een campagneactie in de wachtrij te zetten tot de Quiet Hours is voltooid, en de mogelijkheid om de geactiveerde Quiet Hours-regel te bekijken.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct Mail-kanaal in reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Voorheen beperkt tot Campagnes, is het <strong>Direct Mail-kanaal</strong> nu beschikbaar op het <strong>journey canvas</strong>, waarmee je Direct Mail in je reizen kunt integreren. Direct Mail kan nu worden gebruikt in zowel batch- als 1:1-reisscenario's, met ondersteuning voor bestandsextractieconfiguratie en tijdgebaseerde frequentie-instellingen.</p>
<p>Voorheen uitgebracht in Beperkte Beschikbaarheid, is deze mogelijkheid nu beschikbaar voor alle omgevingen (Algemene Beschikbaarheid).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web Pushmeldingenkanaal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ondersteunt <strong>nu Web Push-meldingen</strong>, waarmee het pushkanaal verder gaat dan mobiel. Je kunt meldingen naadloos naar zowel mobiele als desktopbrowsers sturen, waardoor je klanten direct op hun apparaten kunt bereiken zonder een app nodig te hebben. Deze verbetering stelt je in staat om gebruikers in realtime te betrekken met tijdige, gepersonaliseerde berichten, waarbij gebruikmaken van dezelfde authoring-workflows en targetingmogelijkheden die al beschikbaar zijn voor mobiele push.</p>
<p>Voorheen uitgebracht in Beperkte Beschikbaarheid, is deze mogelijkheid nu beschikbaar voor alle omgevingen (Algemene Beschikbaarheid).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met de nieuwe <strong>RCS Basic-add-on</strong> optie kun je nu basisberichten van Rich Communication Services (RCS) leveren in de Journey Optimizer, waardoor de volgende verbeterde berichtmogelijkheden mogelijk zijn, afhankelijk van ondersteuning van provider en provider:</p>
<ul>
<li>Branded and verified sender support: Stuur berichten met geverifieerde bedrijfsprofielen met brandingelementen (logo, afzendernaam, enz.).</li>
<li>Inzichten in berichtbezorging: Ontvang gedetailleerde leveringsrapporten inclusief berichtstatusupdates (bijv. verzonden, afgeleverd, gelezen).</li>
<li>Linktracking: Embed en volg URL's binnen RCS-berichten voor engagementanalyse.</li>
<li>Fallback naar SMS: Automatische terugval op SMS wanneer het apparaat van het profiel geen RCS ondersteunt of tijdelijk niet bereikbaar is via RCS.</li>
<li>Basisberichtcompositie: Stuur eenvoudige tekstgebaseerde RCS-berichten.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Beslissingsondersteuning in Push- en SMS-kanalen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Je kunt nu Decision-beleidsmaatregelen<strong> toevoegen </strong>aan push- en SMS-reizen en campagnes. Beslissingsbeleid zijn containers voor je aanbiedingen die gebruikmaken van de Decisioning-engine om dynamisch de beste content terug te geven voor elk publiekslid.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor een reeks organisaties (Beperkte Beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger om toegang te krijgen.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct mail-kanaal in georkestreerde campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail-kanaal is nu beschikbaar in georkestreerde campagnes. De <strong>Direct mail-activiteit</strong> faciliteert het verzenden van direct mail binnen je Orkestreerde campagne, zowel voor eenmalige als terugkerende berichten. Het dient om het proces van het genereren van het <strong>extractiebestand</strong> te automatiseren dat vereist is door direct mail-aanbieders. Je kunt kanaalactiviteiten combineren in het Orchestrated campaign canvas om cross-channel campagnes te creëren die acties kunnen triggeren op basis van klantgedrag en data.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aangepaste formulieren op landingspagina</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Journey Optimizer kun je nu profielattributen<strong> vastleggen </strong>via je landingspagina's. Maak, ontwerp en beheer <strong>aangepaste formulieren</strong> die zijn afgestemd op uw behoeften op basis van een specifieke dataset. Je kunt deze formulieren vervolgens gebruiken in landingspagina's om de profielattributen van jouw keuze toe te voegen aan de dataset die voor elk formulier is gedefinieerd.</p>
<p>Voorheen uitgebracht in Beperkte Beschikbaarheid, is deze mogelijkheid nu beschikbaar voor alle omgevingen (Algemene Beschikbaarheid).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nieuwe bronconnectoren voor loyaliteitsapps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nieuwe <strong>bronconnectoren</strong> zijn nu beschikbaar in Adobe Experience Platform voor de Talon.One, Capillary en Kobie loyaliteitsapps. Deze connectors stellen je in staat loyaliteitsgegevens naadloos te streamen naar Adobe Experience Platform en deze data te benutten in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Berichtexport</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Het is nu mogelijk om verzonden leveringen<strong> te </strong>exporteren naar een specifieke dataset, voor archivering en compliance. Deze capaciteit is niet alleen beschikbaar voor e-mail, maar ook voor andere kanalen zoals sms. De gegevensbewaring voor de berichtexportdataset is nu <strong>7 dagen</strong>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nieuwe API om actiecampagnes op te halen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Er is nu een nieuwe <strong>Journey Optimizer API</strong> beschikbaar, waarmee je programmatisch campagnegerelateerde gegevens zoals details, versies en configuraties kunt ophalen en inspecteren.</p>
<p>Raadpleeg de <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 24 november 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nieuwe reiswaarschuwingen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Drie nieuwe <strong>reismeldingen</strong> zijn nu beschikbaar om je te helpen de levenscyclusgebeurtenissen van de reis en de prestaties van aangepaste acties te monitoren en te volgen:</p>
<ul>
<li><strong>Journey Published</strong>: Ontvang meldingen wanneer een reis door een beoefenaar wordt gepubliceerd in het journey canvas.</li>
<li><strong>Reis Voltooid</strong>: Ontvang meldingen wanneer een reis is afgerond, met specifieke definities op basis van reistype (Lees Publiek of Gebeurtenis-getriggerd).</li>
<li><strong>Aangepaste actie-capping geactiveerd</strong>: Word geïnformeerd wanneer capping wordt geactiveerd op een aangepaste actie-endpoint.</li>
</ul>
<p>Deze meldingen kunnen op organisatieniveau of voor specifieke reizen worden geabonneerd.</p>
<p>Raadpleeg de <a href="../reports/alerts.md#journey-alerts">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 5 november 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Thema's in de E-mailontwerper</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Je kunt nu snel vooraf goedgekeurde thema's<strong> toepassen </strong>om merkconsistentie in alle e-mails te waarborgen, je campagnecreatieproces versnellen en onafhankelijk hoogwaardige e-mails produceren terwijl je de afhankelijkheid van ontwerpteams vermindert.</p>
<p>Voorheen uitgebracht in bètaversie, is deze functionaliteit nu beschikbaar voor een reeks organisaties (Beperkte Beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger om toegang te krijgen.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Raadpleeg de <a href="../email/apply-email-themes.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 5 november 2025</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#jan-26-01-improv}

Verbeteringen die met deze release komen, worden hieronder vermeld.

#### AI

* **AI Assistant Content Quality Checks** - Naast merkafstemming kun je nu de algehele <strong>contentkwaliteit</strong> evalueren om mogelijke problemen met leesbaarheid, samenhang en effectiviteit te ontdekken, onafhankelijk van je merkrichtlijnen. Deze geautomatiseerde controles helpen onduidelijke boodschappen, inconsistente toon of structurele gaten te identificeren.
* **Werk merken bij met nieuw kleurtabblad** - Merkrichtlijnen zorgen ervoor dat je merk consistent wordt gepresenteerd op alle contactpunten. De nieuwe <strong>Colors-sectie</strong> definieert de standaarden voor het kleursysteem van jouw merk, waarin wordt beschreven hoe kleuren worden geselecteerd, georganiseerd en toegepast op ervaringen. Het zorgt voor consistent gebruik van primaire, secundaire, accent- en neutrale kleuren om een samenhangende, toegankelijke en herkenbare merkidentiteit te ondersteunen.

#### Campagnes

* **Plan campagne met behulp van de Profieltijdzone** - Campagneplanning kan nu de <strong>tijdzone</strong> van elk profiel gebruiken om berichten op het beoogde lokale tijdstip te bezorgen.

  **Opmerking**: Deze verbetering is alleen beschikbaar voor een reeks organisaties (Beperkte beschikbaarheid).

#### Kanalen

* **SMS Webhooks: Fase II** - Beschrijving wordt verstrekt.

* **WhatsApp Resell Aanbod** - Beschrijving wordt verstrekt.

#### Email Designer

* **Correcties ter plaatse in de E-mailontwerper** - <strong>AI-gestuurde automatische inhoudssuggesties</strong> zijn nu beschikbaar in de E-mailontwerper wanneer overtredingen worden gedetecteerd tijdens inhoudsvalidatie. Als inhoud wordt gemarkeerd als niet in lijn met merkrichtlijnen of niet voldoet aan kwaliteitscriteria, genereert het systeem proactief gecorrigeerde alternatieven die kunnen worden beoordeeld en toegepast, wat de naleving verbetert en de productie versnelt.

#### Ervaringsbeslissingen

* **Reisarbitrage** - Je kunt nu formules en AI-modellen<strong> gebruiken </strong>om automatisch de prioriteitsscores van reizen te verhogen op basis van klantprofielkenmerken en contextuele factoren, zodat klanten de meest relevante reizen invullen.

* **EXD Sandbox-tooling documentatie - Update** - Beschrijving wordt verstrekt.

* **Selfservice migratietooling-API&#39;s** - Er is een nieuwe set <strong>migratietooling-API&#39;s</strong> beschikbaar om Offer management-entiteiten te migreren naar Experience Decisioning. De tools maken naadloze migratie tussen sandboxes mogelijk met afhankelijkheidsoplossing en rollback-mogelijkheden.

* **Koppel fragmenten aan beslissingsitems** - Journey Optimizer biedt nu de mogelijkheid om fragmenten<strong> aan beslissingsitems te koppelen</strong>, wat kan worden ingezet in code-gebaseerde ervaringscampagnes via besluitbeleid.

  **Opmerking**: Eerder uitgebracht in Beperkte Beschikbaarheid, is deze verbetering nu beschikbaar voor alle omgevingen (Algemene Beschikbaarheid).

#### Journeys

* **Maak gebruik van een failure response payload in journey Custom Actions** - Je kunt nu een optionele <strong>error response payload</strong> definiëren voor custom actions. Wanneer een aanroep mislukt, wordt de foutpayload blootgesteld in de reiscontext en is beschikbaar in de timeout/error-branch om rijkere fallback-logica en debugging te ondersteunen.

* **Combineer native en Adobe Campaign berichtacties** - Journey Optimizer laat je nu Adobe Campaign v7/v8 berichtacties combineren met native kanaalacties in dezelfde reis.

* **Validatie van** de payloadgrootte van reizen in reizen - Journey Optimizer biedt <strong>nu validatie</strong> van payloadgrootte om optimale prestaties en systeemstabiliteit te waarborgen. Bij het bouwen of publiceren van reizen ontvang je duidelijke waarschuwingen en fouten als de payloadgrootte de aanbevolen limieten nadert of overschrijdt, samen met bruikbare richtlijnen om je reisconfiguratie te optimaliseren. Deze proactieve validatie helpt je potentiële problemen vroeg te identificeren en de prestaties van je reis te behouden.

* **Meerdere inkomende acties in reizen** - Om je reisorkestratie te vereenvoudigen, kun je nu meerdere inkomende acties<strong> in één reis definiëren</strong>. Voorheen beschikbaar in campagnes, stelt deze mogelijkheid je in staat om meerdere code-gebaseerde ervaringen, in-app berichten, Content Cards of webacties tegelijk naar verschillende locaties te leveren, waarbij elke actie een specifieke inhoud bevat.

  **Opmerking**: Eerder uitgebracht in Beperkte Beschikbaarheid, is deze verbetering nu beschikbaar voor alle omgevingen (Algemene Beschikbaarheid).

#### Georkestreerde campagnes

* **Selecteer attributen en kopieer distributiewaarden** - Je kunt nu waarden direct selecteren of kopiëren vanuit de verdelingsweergave van waarden in georkestreerde campagnes.

* **Data usage label inheritance for audiences** - <strong>Data usage labels</strong> die in Adobe Experience Platform worden toegepast, worden nu automatisch overgenomen bij het opslaan van doelgroepen in georkestreerde campagnes, waardoor handmatige DULE tagging wordt verminderd.

* **Vooraf gedefinieerde retargetingfilters** - Om eenvoudiger retargeting<strong> te maken voor georkestreerde campagne-toepassingen, introduceert deze release nieuwe </strong>retargetingfilters. Deze filters stellen je in staat doelgroepen direct te targeten op basis van berichtenbetrokkenheid, zoals verzonden, alleen geopend, geopend of geklikt, of geopend en geklikt, en de specifieke campagne of campagne in transitie selecteren die je wilt hertargeten.

* **Vooraf gedefinieerde filters met parameters** - Je kunt nu filters maken <strong>met parameters</strong> in georkestreerde campagnes voor herbruikbare, bewerkbare regels.

* **Berichtbevestiging vóór verzending** - Een <strong>bevestigingsstap</strong> is nu standaard ingeschakeld voordat georkestreerde campagnes worden verzonden om per ongeluk verzendingen te verminderen.

* **Ondersteuning voor door gebruikers gegenereerde metadata** - De <strong>uitvoeringsMetadata-hulpfunctie</strong> is nu beschikbaar in de personalisatie-editor voor georkestreerde campagnes, waarmee je contextuele informatie aan elke native actie kunt koppelen en deze kunt opslaan in een dataset voor export naar externe systemen.

* **Herstartknop** - Georkestreerde campagnes bevatten nu een <strong>herstartknop</strong> zodat je runs snel opnieuw kunt starten wanneer dat nodig is voordat je de campagne publiceert.

* **Ondersteuning** voor tariefcontrole - Georkestreerde campagnes ondersteunen <strong>nu tariefcontrole</strong> om je te helpen de leveringen te tempoën te sturen en af te stemmen op volumebeperkingen.

#### Machtigingen

* **Voorkom zelfgoedkeuring voor reizen en campagnes** - Je kunt nu eisen dat makers hun eigen reizen of campagnes niet mogen goedkeuren, wat de scheiding van taken<strong> in goedkeuringsworkflows verbetert</strong>.

## Binnenkort beschikbaar {#jan-26-01-coming-soon}

In de komende dagen staan de volgende mogelijkheden en verbeteringen gepland voor release. **Informatie kan worden gewijzigd**. Bijgewerkte links, schermen en documentatie worden gedeeld zodra deze updates live in productie zijn.

<table>
<thead>
<tr>
<th><strong>Contentgeneratie binnen Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aangedreven door Adobe Experience Platform Agent Orchestrator, <strong>is Journey Agent</strong> beschikbaar in Journey Optimizer en stelt het je in staat reizen te analyseren via een natuurlijke taalinterface. Je kunt nu ook kanaalspecifieke content direct genereren en beheren in Journey Agent, content creëren voor kanalen zoals e-mail en push, templates toepassen en previewen, toon en stijl verfijnen via prompts, en content openen in Content Designer voor in-context bewerking.</p>
<p>Beschikbaarheidsdatum: 2 februari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Contentbeslissingsactiviteit</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Je kunt nu gepersonaliseerde aanbiedingen<strong> opnemen </strong>in je reizen via een speciale contentkeuzeactiviteit in het reiscanvas, en deze gebruiken in reisactiviteiten, waaronder voorwaarden en aangepaste acties.</p>
<p>Beschikbaarheidsdatum: 2 februari 2026</p>
</td>
</tr>
</tbody>
</table>
