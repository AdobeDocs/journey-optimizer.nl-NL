---
solution: Journey Optimizer
product: journey optimizer
title: Opmerkingen bij de release 2026
description: Opmerkingen bij de release van Journey Optimizer 2026
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 65ca94cf-8e17-4a25-90f3-238083f81477
source-git-commit: 559feb1d45abb287d5f4b0e2abae8f2ec663713b
workflow-type: tm+mt
source-wordcount: '2525'
ht-degree: 8%

---

# Aanvullende informatie 2026 {#release-notes-2026}

Deze pagina bevat een overzicht van alle functies en verbeteringen die [!DNL Journey Optimizer] in 2026 heeft uitgebracht.



## Opmerkingen bij de release van februari &#39;26 {#feb-26-01-rn}

### Nieuwe functies {#feb-26-01-features}


<table>
<thead>
<tr>
<th><strong>Reisarbitrage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt <strong> rangschikkende formules </strong> nu gebruiken om de score van de reisprioriteit automatisch op te voeren die op de attributen van het klantenprofiel en contextafhankelijke factoren wordt gebaseerd, die klanten verzekeren de meest relevante reizen ingaan.</p>
<p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p>Raadpleeg de <a href="../conflict-prioritization/journey-ranking-formulas.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 24 februari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actie tijdens reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer steunt een nieuwe generische <strong> activiteit van de Actie </strong> die u toelaat om zowel enige acties als multi-action binnenkomende actiegroepen te vormen, die voor gestroomlijnde actieconfiguratie binnen het wegcanvas toestaan. Met deze nieuwe functie kunt u met name:</p>
<ul>
<li>Een vereenvoudigde native actieconfiguratie binnen het reiscanvas.</li>
<li>De capaciteit om multi-actie binnenkomende actiegroepen te creëren.</li>
<li>De mogelijkheid om optimalisatie toe te voegen aan ingebouwde kanaalacties.</li>
<li>De mogelijkheid om zowel experimentele als meertalige opties aan een actie toe te voegen.</li>
</ul>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p>Raadpleeg de <a href="../building-journeys/journey-action.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 20 februari 2026</p>
<p><strong> Nota:</strong> Alle inheemse kanalen zijn nu toegankelijk door de de reisactiviteit van de Actie. Oudere native kanaalactiviteiten worden vervangen door de release van maart. Bestaande reizen die oudere handelingen bevatten, blijven functioneren zoals ze zijn: er is geen migratie vereist.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Golf die uitgaande berichten verzendt</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu berichten van Journey Optimizer-campagnes of reizen plannen die in gecontroleerde batches in de loop van de tijd worden geleverd.</p>
<p>Wave-verzending biedt de volgende voordelen:</p>
<ul>
<li>Betere leverbaarheid - Spread verzendt in tijd om te helpen een sterke sender reputatie handhaven en het risico verminderen om als spam worden gemarkeerd.</li>
<li>Controle van de lading - vermijd overweldigende stroomafwaartse systemen (b.v. callcenters, landende pagina's) door te beperken hoeveel berichten tegelijk uitgaan.</li>
<li>Gebruiksscenario's met veel volume en veel tijd - Geschikt voor grote doelgroepen of wanneer u de timing moet bepalen (bijvoorbeeld capaciteit van het callcenter, opwaardering of tijdgebonden aanbiedingen).</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p>In <strong> campagnes </strong>, is dit vermogen beschikbaar aan alle milieu's (Algemene Beschikbaarheid). Raadpleeg de <a href="../campaigns/send-using-waves.md">gedetailleerde documentatie</a> voor meer informatie.</p>

<p>In <strong> reizen </strong>, is dit vermogen slechts beschikbaar voor een reeks organisaties (Beperkte Beschikbaarheid) - om toegang te krijgen, uw vertegenwoordiger van Adobe te contacteren. Raadpleeg de <a href="../building-journeys/send-using-waves.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 19 februari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Subdomeinen migreren naar aangepaste delegatie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt subdomeinen nu migreren gebruikend de de delegatiemodus van de NAAM aan douanedelegatie direct van de interface, zodat kunt u strikter veiligheidsbeleid in overeenstemming met de richtlijnen van uw bedrijf ontmoeten zonder kanaalconfiguraties opnieuw te creëren.</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p>Raadpleeg de <a href="../configuration/custom-subdomain-migration.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 19 februari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web-push-berichtkanaal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer steunt nu <strong> Pushberichten van het Web </strong>, die het duw kanaal voorbij mobiel uitbreiden. U kunt naadloos berichten aan zowel <strong> mobiele als Desktopbrowsers leveren </strong>, toelatend u om klanten op hun apparaten direct te bereiken zonder een app te vereisen. Dankzij deze verbetering kunt u gebruikers in real-time en op maat gesneden berichten laten zien, zodat u dezelfde ontwerpworkflows kunt gebruiken en de functies kunt kiezen die al beschikbaar zijn voor mobiele push.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Eerder in Beta is deze mogelijkheid beschikbaar voor alle omgevingen (algemene beschikbaarheid).</p>
<p>Raadpleeg de <a href="../push/push-configuration-web.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 13 februari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Beslissingsactiviteit inhoud</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Een nieuwe <strong> activiteit van het besluit van de Inhoud </strong> is nu beschikbaar in het wegcanvas voor het integreren van gepersonaliseerde aanbiedingen direct in uw klantenreizen. Deze activiteit laat u toe om op besluit-gebaseerde inhoud te leveren en die aanbiedingen door uw reis-in voorwaarden voor het creëren van op geschiktheid-gebaseerde vertakking, in douaneacties voor het overgaan van aanbiedingsgegevens aan externe systemen, en in andere activiteiten voor de bouw van volledig gepersonaliseerde klantenervaringen van verwijzingen te voorzien.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Raadpleeg de <a href="../building-journeys/content-decision.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 10 februari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Self-service migratie-API's</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Het hulpmiddel van de migratie APIs is nu beschikbaar om <strong> het beheer van het Besluit </strong> entiteiten aan <strong> Beslissing </strong> programmatically te migreren, kenmerkend:</p>
<ul>
<li>Flexibele migratieruimten (sandbox-, bied- of beslissingsniveau)</li>
<li>Geautomatiseerde afhankelijkheidsanalyse en -validatie</li>
<li>Ondersteuning voor terugdraaien van voltooide migraties</li>
<li>Gedetailleerde migratierapporten met objecttoewijzingen</li>
</ul>
<p>Raadpleeg de <a href="../experience-decisioning/decisioning-migration-api.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 3 februari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aangepaste actiecontrole</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verbeter insight dieper in de gezondheid en prestaties van uw eindpunten van de douaneactie met een nieuw controledashboard en verrijkte gegevens van de reisstap. Spoor succesvolle vraag, fouten, productie, reactietijden, en rij wacht tijden om snel te begrijpen wanneer, waar, en waarom anomalieën voorkomen.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p>Raadpleeg de <a href="../action/reporting.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 3 februari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ondersteuning voor besluitvorming in SMS-kanaal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt de inhoud van uw SMS-berichten nu personaliseren en optimaliseren met Beslissing. Gebruik Prioritaire scores, Formulas of AI-modellen om de beste inhoud weer te geven aan uw klanten.</p>
<p>Raadpleeg de <a href="../experience-decisioning/create-decision.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 2 februari 2026</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#feb-26-01-improv}

De verbeteringen die bij deze release worden geleverd, worden hieronder weergegeven.

#### Configuratie

* **het gebeurtenisgebruik van de Ervaring in reisuitdrukkingen** - Beginnend 1 April, 2026, zal het gebruik van de attributen van de ervaringsgebeurtenis in reisuitdrukkingen niet meer gesteund worden voor organisaties die dit vermogen in de laatste 90 dagen niet hebben gebruikt. Deze mogelijkheid is al sinds 8 juli 2025 niet meer beschikbaar voor nieuwe klantenorganisaties. Voor alternatieven, zie [&#x200B; de gebeurtenisraadpleging van de Ervaring in reizen &#x200B;](../building-journeys/exp-event-lookup.md).

#### Contentmanagement

<!--
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors</strong> section defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity. [Read more](../content-management/brands.md)
-->

* **thema&#39;s van het Gebruik om beelden in e-mailmalplaatjes** om te zetten - wanneer het omzetten van een beeld in een e-mailmalplaatje in Journey Optimizer, kunt u een thema nu gebruiken als input zodat geproduceerde HTML uw merkparameters volgt. Stijlen zoals achtergrondkleur, knopkleur, lettertypen, regelafstand, marges en opvulling worden automatisch toegepast, waardoor het handmatig ontwerpen minder wordt en een sjabloon ontstaat die klaar is voor gebruik met minimale bewerkingen. [Meer informatie](../content-management/image-to-html.md)

  Beschikbaarheidsdatum: 17 februari 2026.

<!--* **Text mode for fragments** - You can now create and manage text versions of your fragments, supporting workflows that rely on plain text content and providing the same flexibility as in email content. [Read more](../content-management/create-fragments.md)-->

#### Email Designer

* **Inspringing van de Tekst** - u kunt klantgerichte linkerinspringing op de eerste lijn van paragrafen in tekstcomponenten direct van het eigenschappenpaneel nu toepassen. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. --> dit verbetert leesbaarheid voor lange-vorminhoud zoals redacteurs en artikelen. [Meer informatie](../email/get-started-email-style.md)

  Beschikbaarheidsdatum: 18 februari 2026.

#### Beslissing

* **Edge binnenkomende steun voor het gebruiken van de gegevens van Adobe Experience Platform in Beslissing** - het gebruiken van de gegevens van Adobe Experience Platform in Beslissing steunt nu rand binnenkomende gebruiksgevallen, naast e-mail en douaneacties in reizen. [Meer informatie](../experience-decisioning/aep-data-exd.md)

  Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

* **Beslissende voorproef in op code-gebaseerd kanaal van de Ervaring** - u kunt besluitvormingspunten nu voorproef wanneer het vormen van Beslissing met het op code-Gebaseerde kanaal van de Ervaring. Voorvertoning is rechtstreeks beschikbaar in de ontwerpinterface voordat u live gaat. [Meer informatie](../code-based/test-code-based.md#preview-code-based)

  Beschikbaarheidsdatum: 18 februari 2026

<!--THIS WAS FINALLY NOT RELEASED IN FEBRUARY

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach fragments to decision items which can be leveraged in code-based experience campaigns through decision policies. [Read more](../experience-decisioning/fragments-decision-policies.md)

  Previously released in Limited Availability, this capability is now available to all environments (General Availability).

  Availability date: February 12, 2026.-->

#### Personalisatie

* **hulp van Metagegevens van de Uitvoering** - de `executionMetadata` hulpfunctie is nu beschikbaar aan alle klanten van Journey Optimizer. Gebruik dit schema om contextuele informatie dynamisch toe te voegen aan elke native handeling en deze vast te leggen in een gegevensset voor export naar externe systemen. [Meer informatie](../personalization/functions/helpers.md#execution-metadata)

  Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu&#39;s (Algemene Beschikbaarheid).

  Beschikbaarheidsdatum: 20 februari 2026.

#### Sms

* **Webhooks van SMS** - Webhooks worden nu gesteund over alle leveranciers van SMS. U kunt elke WebHaak vormen die op zijn voorgenomen doel wordt gebaseerd: Binnenkomende webhooks om inkomende berichten en Terugkoppeling webhooks te vangen om leveringsontvangstbewijzen, statusupdates, en andere bericht-gerelateerde gebeurtenissen te ontvangen. [Meer informatie](../sms/sms-webhook.md)

  Beschikbaarheidsdatum: 2 februari 2026.



## Opmerkingen bij de release van januari &#39;26 {#jan-26-rn}

<!--**Release date**: January 27-28, 2026-->

### Nieuwe functies {#jan-26-01-features}


<table>
<thead>
<tr>
<th><strong>Ondersteuning voor beslissingen in het pushkanaal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt de inhoud van uw <strong> Push berichten </strong> met <strong> Beslissing </strong> nu personaliseren en optimaliseren. Gebruik Prioritaire scores, Formulas of AI-modellen om de beste inhoud weer te geven aan uw klanten.</p>
<p>Voor het bepalen van de ervaring met pushmeldingen is een specifieke versie van de Mobile SDK vereist. Alvorens deze eigenschap uit te voeren, controleer de <a href="https://developer.adobe.com/client-sdks/home/release-notes/" target="_blank"> versienota's </a> om de vereiste versie te identificeren en u te verzekeren dienovereenkomstig hebt bevorderd. U kunt alle beschikbare versies van SDK voor uw platform in <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" target="_blank"> ook bekijken deze sectie </a>.</p>
<p>Raadpleeg de <a href="../experience-decisioning/create-decision.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 30 januari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Directe post voor reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eerder beperkt tot Campagnes, <strong> is het kanaal van 0&rbrace; Directe Post &lbrace;nu beschikbaar op het wegcanvas, toelatend u om Directe Post in uw reizen op te nemen. </strong> De directe Post kan nu in zowel <strong> partij en 1:1 reisscenario's </strong>, met steun voor de configuratie van de dossierextractie en op tijd-gebaseerde frequentiemontages worden gebruikt.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p><img src="assets/do-not-localize/dm-journey.gif"/></p>
<p>Raadpleeg de <a href="../direct-mail/get-started-direct-mail.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 29 januari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Quiet uren (op tijd gebaseerde uitsluitingen)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong> Stil uren </strong> laat u op tijd-gebaseerde uitsluitingen voor E-mail, SMS, Duw, en kanalen WhatsApp bepalen. Zij zorgen ervoor dat geen berichten tijdens specifieke periodes worden verzonden, die u helpen klantenvoorkeur en nalevingsvereisten respecteren. U kunt stille uren door <strong> regelreeksen </strong> toepassen, die aan individuele acties in campagnes of reizen voor nauwkeurige controle kunnen worden toegewezen.</p>
<p>Eerder uitgebracht in Beperkte Beschikbaarheid, is deze eigenschap nu beschikbaar aan alle milieu's. Met deze algemene beschikbaarheidsrelease biedt deze functie nu de mogelijkheid voor de klant om een campagneactie in de wachtrij te plaatsen tot de voltooiing van Quiet Hours en de mogelijkheid om een voorvertoning van de geactiveerde Quiet Hours-regel weer te geven.</p>
<p><img src="assets/do-not-localize/quiet-hour-ga.gif"/></p>
<p>Raadpleeg de <a href="../conflict-prioritization/quiet-hours.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 29 januari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Bericht exporteren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Een nieuw <strong> vermogen van de Uitvoer van het 0&rbrace; Bericht is nu beschikbaar voor e-mail en de kanalen van SMS. </strong> Met deze functie kunt u automatisch verzonden berichtinhoud exporteren naar een speciale Experience Platform-gegevensset, zodat u:</p>
<ul>
<li>Voldoen aan wettelijke nalevingsvereisten (zoals HIPAA)</li>
<li>Berichten archiveren voor juridische claims en vragen over klantenservice</li>
<li>Kopieën behouden van persoonlijke inhoud die naar individuen is verzonden</li>
</ul>
<p>De verslagen worden bewaard in de Dataset van de Uitvoer van het Bericht van AJO voor 7 kalenderdagen vanaf opneming. Tijdens deze bewaarperiode kunt u ze naar uw eigen opslagruimte exporteren via Experience Platform-bestemmingen. De eigenschap wordt toegelaten op het niveau van de kanaalconfiguratie, die u <strong> korrelige controle </strong> geven waarover de berichten worden uitgevoerd.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor het e-mail- en sms-kanaal, voor organisaties die de add-on service Message Export hebben aangeschaft. Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>Raadpleeg de <a href="../configuration/message-export.md#message-export">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 28 januari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct mail kanaal in georkestreerde campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail kanaal is nu beschikbaar in georkestreerde campagnes. De <strong> Directe postactiviteit </strong> vergemakkelijkt direct mail die binnen uw Geordende campagne, voor zowel eenmalige als terugkomende berichten verzendt. Het dient om het proces te automatiseren om het <strong> extractiedossier </strong> te produceren dat door directe postleveranciers wordt vereist. U kunt kanaalactiviteiten in het Geordende campagnecanvas combineren om kanaalcampagnes tot stand te brengen die acties kunnen teweegbrengen die op klantengedrag en gegevens worden gebaseerd.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>Raadpleeg de <a href="../orchestrated/activities/channels.md#channel">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 28 januari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - Een reis maken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent biedt nu creatieve mogelijkheden aan, toelatend de gebruikers van Journey Optimizer om marketing reizen door a <strong> natuurlijke taalinterface </strong> te bouwen en te vormen. Met deze nieuwe vaardigheden, kunnen de artsen reizen snel tot stand brengen door hun vereisten in <strong> gespreksherinneringen </strong> eenvoudig te beschrijven. Deze innovatie stroomlijnt het proces van het creëren van de reis, waardoor de marketeers zich op strategie eerder dan technische configuratie kunnen concentreren.</p>
<p>Raadpleeg de <a href="../start/ai-features.md#journey-agent">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 12 januari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>OphaalAPI voor handelingencampagne</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Een nieuwe Journey Optimizer API is nu beschikbaar, toelatend u om programmatically <strong> op campagne betrekking hebbende gegevens </strong> zoals details, versies, en configuraties terug te winnen en te inspecteren.</p>
<p>Raadpleeg de <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 24 november 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Designer-thema's e-mailen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt <strong> vooraf goedgekeurde thema's </strong> nu snel toepassen om <strong> merkconsistentie </strong> over alle e-mails te verzekeren, uw proces van de campagneverwezenlijking te versnellen, en onafhankelijk e-mails van hoge kwaliteit te produceren terwijl het verminderen van afhankelijkheid van ontwerpteams.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Eerder in bètaversie is deze mogelijkheid nu beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p>Raadpleeg de <a href="../email/apply-email-themes.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 5 november 2025</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#jan-26-01-improv}

#### AI

* **AI de Controles van de Kwaliteit van de Inhoud van de Inhoud &lbrace;** - Naast merkgroepering, kunt u algemene <strong> inhoudskwaliteit </strong> nu evalueren om potentiële kwesties met <strong> leesbaarheid </strong>, samenhang, en doeltreffendheid, onafhankelijk van uw merkrichtlijnen te ontdekken. Deze geautomatiseerde controles helpen onduidelijk overseinen, inconsistente toon, of structurele hiaten identificeren. [Meer informatie](../content-management/brands-score.md#validate-quality).

  [&#x200B; ontdekt deze eigenschap in video &#x200B;](https://video.tv.adobe.com/v/3470544/?learn=on).

#### Journeys

* **combineer inheemse en het berichtacties van Adobe Campaign** - Journey Optimizer laat u nu <strong> Adobe Campaign v7/v8 </strong> berichtacties met <strong> inheemse kanaalacties </strong> in de zelfde reis combineren. [Meer informatie](../building-journeys/using-adobe-campaign-v7-v8.md)

  Beschikbaarheidsdatum: 27 januari 2026.

* **de antwoordlading van de actiefout van de Actie van de Douane** - u kunt een facultatieve <strong> nuttige lading van de foutenreactie </strong> voor douaneacties nu bepalen. Wanneer een vraag ontbreekt, wordt de foutenlading blootgesteld in de reiscontext (onder de knoop van errorResponse van de actie) en is beschikbaar in de <strong> onderbreking/foutentak </strong>, naast `jo_status_code`, om rijkere fallback logica en het zuiveren te steunen. [Meer informatie](../action/about-custom-action-configuration.md#define-the-message-parameters)

  Beschikbaarheidsdatum: 27 januari 2026.

* **de bevestiging van de grootte van de ladingsgrootte van de Reis in reizen** - Journey Optimizer bevestigt nu <strong> ladingsgrootte </strong> helpen optimale prestaties en systeemstabiliteit verzekeren. Wanneer het bouwen van of het publiceren van reizen, ontvangt u duidelijke <strong> waarschuwingen en fouten </strong> als de grootte van de nuttige lading de geadviseerde grenzen, samen met actioneerbare begeleiding benadert om uw reisconfiguratie te optimaliseren. Deze proactieve validatie helpt u potentiële problemen vroegtijdig te identificeren en de reisprestaties te handhaven. [Meer informatie](../start/guardrails.md#journey-payload-size)

  Beschikbaarheidsdatum: 27 januari 2026.


* **het alarm van de Reis** - Nieuw <strong> pre-gevormde alarm </strong> is beschikbaar voor reizen.
   * <strong> Profiel verwerpt Tarief dat </strong> wordt overschreden - Verhouding van profielteruggooi naar ingegaan profielen over de laatste 5 minuten overschrijdt drempel
   * <strong> het Tarief van de Fout van de Actie van de Douane overtrok </strong> - Verhouding van de fouten van de douaneactie aan succesvolle vraag van HTTP over de laatste 5 minuten overschrijdt drempel
   * <strong> het Tarief van de Fout van het Profiel overtrok </strong> - Verhouding van profielen-in-fout aan ingegaan profielen over de laatste 5 minuten overschrijdt drempel

  Raadpleeg de [gedetailleerde documentatie](../reports/alerts.md) voor meer informatie.

  Beschikbaarheidsdatum: 14 oktober 2025.

#### Geordende campagnes

* **de overerving van het het gebruiksetiket van gegevens voor publiek** - de Etiketten die in Adobe Experience Platform worden toegepast dragen nu automatisch over wanneer het bewaren van <strong> publiek </strong> in georkestreerde campagnes, die handmatige <strong> DULE etiketteren </strong> verminderen. [Meer informatie](../orchestrated/activities/save-audience.md)

* **vooraf bepaalde filters met parameters** - u kunt <strong> vooraf bepaalde filters </strong> met <strong> parameters </strong> in georkestreerde campagnes voor herbruikbare, editable regels nu tot stand brengen. [Meer informatie](../orchestrated/predefined-filters.md)

* **Uitgezochte attributen en de waarden van de exemplaardistributie** - u kunt <strong> waarden </strong> van de <strong> distributie van waarden </strong> mening in georkestreerde campagnes nu selecteren of kopiëren. [Meer informatie](../orchestrated/build-query.md)

* **bevestiging van het Bericht alvorens** te verzenden - A <strong> bevestigingsstap </strong> wordt nu toegelaten door gebrek alvorens georkestreerde campagnes te verzenden om toevallig te verminderen verzendt. [Meer informatie](../orchestrated/activities/channels.md#confirm-message-sending)

* **vooraf bepaalde het opnieuw richten filters** - om het gemakkelijkere opnieuw richten voor de geordende gevallen van het campagnegebruik te steunen, introduceert deze versie nieuwe <strong> campagne terugkoppelt filters </strong>. Deze filters laten u rechtstreeks doelpubliek richten dat op <strong> wordt gebaseerd berichtovereenkomst </strong>, zoals verzonden, geopend slechts, geopend of geklikt, of geopend en geklikt, en de specifieke campagne of in-overgangscampagne selecteren u wilt opnieuw richten. [Meer informatie](../orchestrated/retarget.md)

* **de controlesteun van het Tarief** - Geordende campagnes steunen nu <strong> tariefcontrole </strong> om u te helpen leveringen plaatsen en zich met <strong> volumebeperkingen </strong> richten. [Meer informatie](../orchestrated/activities/channels.md#rate-control)

* **knoop van het Begin** - Geordende campagnes omvatten nu a <strong> herstart knoop </strong> zodat kunt u snel <strong> looppas </strong> herlanceren wanneer nodig alvorens de campagne te publiceren. [Meer informatie](../orchestrated/start-monitor-campaigns.md)

* **gebruiker-geproduceerde meta-gegevenssteun** - de <strong> executeMetadata helperfunctie </strong> is nu beschikbaar in de verpersoonlijkingsredacteur voor Geordende campagnes, toelatend u om contextafhankelijke informatie aan om het even welke inheemse actie vast te maken en het op te slaan in een dataset voor de uitvoer naar externe systemen. [Meer informatie](../personalization/functions/helpers.md#execution-metadata)

  Beschikbaarheidsdatum: 27 januari 2026.

* **Keer levende campagnes aan ontwerp status** terug - u kunt levende georkestreerde campagnes aan ontwerp status nu terugkeren wanneer zij uitvoeringsfouten ontmoeten of wanneer u geplande campagnes moet wijzigen alvorens zij beginnen uit te voeren. Deze optie is beschikbaar tot het eerste bericht wordt verzonden. [Meer informatie](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### Campagnes

* **Campagne van het Programma die de Zone van de Tijd van het Profiel** gebruikt - het plannen van de Campagne kan de 2&rbrace; tijdzone van elk profiel <strong> nu gebruiken om berichten bij de voorgenomen lokale tijd te leveren. </strong> [Meer informatie](../campaigns/campaign-schedule.md)

  **Nota**: Deze verbetering is slechts beschikbaar voor een reeks organisaties (Beperkte Beschikbaarheid).

  Beschikbaarheidsdatum: 27 januari 2026.

#### Machtigingen

* **verhindert zelfgoedkeuring voor reizen en campagnes** - voegde een optie toe wanneer het creëren van of het plaatsen van <strong> Beleid van de Goedkeuring </strong> om reis of campagnescheppers te verhinderen van <strong> goedkeurend hun eigen voorwerpen </strong>. [Meer informatie](../test-approve/approval-policies.md)

  Beschikbaarheidsdatum: 27 januari 2026.
