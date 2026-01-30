---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 124ff40cf7cdc0dfdaf67924ff5fb558c96e2956
workflow-type: tm+mt
source-wordcount: '1722'
ht-degree: 6%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** levert onophoudelijk nieuwe eigenschappen, verhogingen aan bestaande eigenschappen, en insectenmoeilijke situaties. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] volgt een doorlopend leveringsmodel, dat Adobe in staat stelt voortdurend nieuwe functies, verbeteringen en correcties te leveren. Deze benadering maakt een schaalbare, gefaseerde implementatie van mogelijkheden mogelijk om prestaties en stabiliteit in alle omgevingen te garanderen.

Vanwege dit model worden releaseopmerkingen bijgewerkt tussen maandelijkse releases. Voor volledige details over de de versiecyclus en beschikbaarheidsfasen, zie [&#x200B; de versiecyclus van Journey Optimizer &#x200B;](releases.md).

[!DNL Adobe Journey Optimizer] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [&#x200B; de Nota&#39;s van de Versie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

## Opmerkingen bij de release van januari &#39;26 {#latest-rn}

<!--**Release date**: January 27-28, 2026-->

De [&#x200B; Eigenschappen &#x200B;](#jan-26-01-features) en [&#x200B; Verbeteringen &#x200B;](#jan-26-01-improv) secties behandelen reeds beschikbare mogelijkheden, terwijl [&#x200B; komende spoedig &#x200B;](#jan-26-01-coming-soon) punten die voor een recentere beschikbaarheidsdatum worden gepland.

<!-- **The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date. 

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Nieuwe functies {#jan-26-01-features}

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

#### Ervaar beslissingsvermogen

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

## Binnenkort beschikbaar {#jan-26-01-coming-soon}

In de komende dagen zijn de volgende mogelijkheden en verbeteringen gepland voor release. **de Informatie is onderworpen aan verandering**. De bijgewerkte verbindingen, de schermen, en de documentatie zullen worden gedeeld zodra deze updates in productie levend zijn.

### Functies

<table>
<thead>
<tr>
<th><strong>Self-service migratie-API's</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong> het tooling APIs van de Migratie </strong> is nu beschikbaar om besluitvormingsentiteiten programmatically te migreren aan Beslissing, kenmerkend:</p>
<ul>
<li>Flexibele migratieruimten (sandbox-, bied- of beslissingsniveau)</li>
<li>Geautomatiseerde afhankelijkheidsanalyse en -validatie</li>
<li>Ondersteuning voor terugdraaien van voltooide migraties</li>
<li>Gedetailleerde migratierapporten met objecttoewijzingen</li>
</ul>
<p>Beschikbaarheidsdatum: 30 januari 2026</p>
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
<p>U kunt de inhoud van uw <strong> Duw en SMS </strong> Berichten met <strong> Beslissing </strong> nu personaliseren en optimaliseren. Gebruik Prioritaire scores, Formulas of AI-modellen om de beste inhoud weer te geven aan uw klanten.</p>
<p>Beschikbaarheidsdatum: 9 februari 2026</p>
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
<p>Een nieuwe <strong> activiteit van het besluit van de Inhoud </strong> is nu beschikbaar in het wegcanvas voor het integreren <strong> gepersonaliseerde aanbiedingen </strong> direct in uw klantenreizen. Deze activiteit laat u toe om op besluit-gebaseerde inhoud te leveren en die aanbiedingen door uw reis te verwijzen - in voorwaarden om op geschiktheid-gebaseerde vertakking tot stand te brengen, in douaneacties voor het overgaan van aanbiedingsgegevens aan externe systemen, en in andere activiteiten om volledig gepersonaliseerde klantenervaringen op te bouwen.</p>
<p>Deze mogelijkheid is beschikbaar voor alle omgevingen (algemene beschikbaarheid).</p>
<p>Beschikbaarheidsdatum: 9 februari 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web Push-berichtkanaal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer steunt nu <strong> Push berichten van het Web </strong>, uitbreidend het duw kanaal voorbij mobiel. U kunt naadloos berichten aan zowel <strong> mobiele als Desktopbrowsers leveren </strong>, toelatend u om klanten op hun apparaten direct te bereiken zonder een app te vereisen. Dankzij deze verbetering kunt u gebruikers in real-time en op maat gesneden berichten laten zien, zodat u dezelfde ontwerpworkflows kunt gebruiken en de functies kunt kiezen die al beschikbaar zijn voor mobiele push.</p>
<!--p><img src="assets/do-not-localize/web-push.gif"/></p-->
<p>Eerder in Beta is deze mogelijkheid beschikbaar voor alle omgevingen (algemene beschikbaarheid).</p>
<p>Beschikbaarheidsdatum: 11 februari 2026</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen


* **maak fragmenten** vast - Journey Optimizer verstrekt nu de capaciteit om <strong> fragmenten </strong> aan <strong> besluitvormingspunten </strong> vast te maken die in code-gebaseerde ervaringscampagnes door besluitvormingsbeleid kunnen worden leveraged.

  Beschikbaarheidsdatum: 9 februari 2026.
