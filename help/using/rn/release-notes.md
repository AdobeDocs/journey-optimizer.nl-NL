---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 029f91599f0be6d30d1e7d73cac7390a6fb05f1f
workflow-type: tm+mt
source-wordcount: '1461'
ht-degree: 4%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** levert onophoudelijk nieuwe eigenschappen, verhogingen aan bestaande eigenschappen, en insectenmoeilijke situaties. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] volgt een doorlopend leveringsmodel, dat Adobe in staat stelt voortdurend nieuwe functies, verbeteringen en correcties te leveren. Deze benadering maakt een schaalbare, gefaseerde implementatie van mogelijkheden mogelijk om prestaties en stabiliteit in alle omgevingen te garanderen.

Vanwege dit model worden releaseopmerkingen bijgewerkt tussen maandelijkse releases. Voor volledige details over de de versiecyclus en beschikbaarheidsfasen, zie [&#x200B; de versiecyclus van Journey Optimizer &#x200B;](releases.md).

[!DNL Adobe Journey Optimizer] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [&#x200B; de Nota&#39;s van de Versie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

## Opmerkingen voorafgaand aan de release van februari &#39;26 {#feb-26-01-rn}

**de pre-versienota&#39;s hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. Koppelingen, schermen en bijgewerkte documentatie worden gepubliceerd in de releaseopmerkingen op de releasedatum.

Zie ook [&#x200B; de pre-versienota&#39;s van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**de datum van de Versie**: 17-18 februari, 2026

### Nieuwe functies {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>Golf die uitgaande berichten verzendt</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu uitgaande berichten van Journey Optimizer-campagnes plannen of reizen die in gecontroleerde batches in de loop van de tijd worden geleverd.</p>
<p>Wave-verzending biedt de volgende voordelen:</p>
<ul>
<li>Betere leverbaarheid - Spread verzendt in tijd om te helpen een sterke sender reputatie handhaven en het risico verminderen om als spam worden gemarkeerd.</li>
<li>Controle van de lading - vermijd overweldigende stroomafwaartse systemen (b.v. callcenters, landende pagina's) door te beperken hoeveel berichten tegelijk uitgaan.</li>
<li>Gebruiksscenario's met veel volume en veel tijd - Geschikt voor grote doelgroepen of wanneer u de timing moet bepalen (bijvoorbeeld capaciteit van het callcenter, opwaardering of tijdgebonden aanbiedingen).</li>
</ul>
<p>In campagnes, is dit vermogen beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p>Bij reizen is deze mogelijkheid alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
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
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reisarbitrage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt <strong> rangschikkende formules </strong> <!--and <strong>AI models</strong> --> nu gebruiken om de scores van de reisprioriteit automatisch op te voeren die op de attributen van het klantenprofiel en contextafhankelijke factoren worden gebaseerd, die klanten verzekeren gaan de meest relevante reizen in.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Kanaalinhoud maken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aangedreven door <strong> Adobe Experience Platform Agent Orchestrator </strong>, <strong> Journey Agent </strong> is beschikbaar in Journey Optimizer en laat u toe om reizen door een natuurlijke taalinterface te analyseren. U kunt kanaal-specifieke inhoud nu ook direct in Journey Agent produceren en beheren, creërend inhoud voor kanalen zoals e-mail en duw, het toepassen van en het voorvertonen van malplaatjes, het verfijnen van toon en stijl door herinneringen, en het openen van inhoud in <strong> Inhoud Designer </strong> voor in-context het uitgeven.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide real-time updates and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Bewaking van AI-modellen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Journey Optimizer kunt u nu de gezondheid, de trainingsstatus en de prestaties van uw beslissingsAI-modellen controleren. Dit staat u toe om opleidingssucces te verifiëren, mislukkingen problemen op te lossen, en invloed op uw resultaten te begrijpen om de beste aanbiedingen voor elke klant te selecteren gebruikend AI. Merk op dat dit vermogen voor <strong> Beslissing </strong> slechts (niet voor de modellen van het Beheer van erfenisBesluit) beschikbaar is.</p>
<p>Dit vermogen is momenteel beschikbaar voor <strong> gepersonaliseerde optimalisering </strong> slechts modellen (niet auto-optimalisering).</p>
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
<li>De mogelijkheid om zowel experimenteeropties als meertalige&gt; opties aan een actie toe te voegen.</li>
</ul>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
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
<p>Beschikbaarheidsdatum: 11 februari 2026</p>
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
<p>Versterking dieper insight in de gezondheid en de prestaties van uw <strong> eindpunten van de douaneactie </strong> met een nieuw <strong> controledashboard </strong> en verrijkte <strong> gegevens van de de gebeurtenisstap van de reisstap </strong>. Spoor succesvolle vraag, fouten, productie, reactietijden, en rij wacht tijden om snel te begrijpen wanneer, waar, en waarom anomalieën voorkomen.</p>
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
<p>U kunt de inhoud van uw <strong> berichten van SMS </strong> met <strong> Beslissing </strong> nu personaliseren en optimaliseren. De Scores van de Prioriteit van het gebruik <strong>, </strong> Formulas <strong>, of </strong> AI Modellen <strong> om de beste inhoud aan uw klanten te tonen.</strong></p>
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


#### Inhoudssjablonen

* **thema&#39;s van het Gebruik om beelden in e-mailmalplaatjes** om te zetten - wanneer het omzetten van een beeld in een e-mailmalplaatje in Journey Optimizer, kunt u een thema nu gebruiken als input zodat geproduceerde HTML uw merkparameters volgt. Stijlen zoals achtergrondkleur, knopkleur, lettertypen, regelafstand, marges en opvulling worden automatisch toegepast, waardoor het handmatig ontwerpen minder wordt en een sjabloon ontstaat die klaar is voor gebruik met minimale bewerkingen. [Meer informatie](../content-management/image-to-html.md)

  Beschikbaarheidsdatum: 13 februari 2026.


#### Email Designer

* **de brandjes van de Update met nieuw kleurenlusje** - de hulp van de Merk zorgt ervoor uw merk constant over alle touchpoints wordt voorgesteld. De nieuwe sectie van Kleuren bepaalt de normen voor het kleurensysteem van uw merk, die hoe de kleuren worden geselecteerd, georganiseerd, en toegepast over ervaringen schetst. Het zorgt voor consistent gebruik van primaire, secundaire, accenten en neutrale kleuren ter ondersteuning van een consistente, toegankelijke en herkenbare merkidentiteit.


#### AI

* **Integratie van de modellen van douaneFirefly en derdebeeldgeneratie** - laat naadloze integratie van standaard en douanemodellen van Firefly, samen met goedgekeurde derdebeeldmodellen (b.v., NanoBanana) toe, om grotere flexibiliteit, controle, en merkgroepering te verstrekken wanneer het produceren van beelden. Op deze manier kunt u het beste model voor elk geval van gebruik selecteren: standaard Firefly voor algemene behoeften, aangepaste Firefly voor on-brand-productie of goedgekeurde modellen van derden voor gespecialiseerde of experimentele scenario&#39;s.


#### Ervaar beslissingsvermogen

* **Edge binnenkomende steun voor het gebruiken van de gegevens van Adobe Experience Platform in Beslissing** - het gebruiken van de gegevens van Adobe Experience Platform in Beslissing steunt nu rand binnenkomende gebruiksgevallen, naast e-mail en douaneacties in reizen.

  **Nota**: Dit vermogen is slechts beschikbaar voor een reeks organisaties (<strong> Beperkte Beschikbaarheid </strong>). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

* **de Voorproef van het Beslissen van de Ervaring in op code-gebaseerd kanaal van de Ervaring** - u kunt de punten van de voorproef bij het vormen van Ervaring Beslissing met het op code-Gebaseerde kanaal van de Ervaring nu vormen. Voorvertoning is rechtstreeks beschikbaar in de ontwerpinterface voordat u live gaat.


* **de fragmenten van de Band aan besluitvormingspunten** - Journey Optimizer verstrekt nu de capaciteit om fragmenten aan besluitvormingspunten vast te maken die in code-gebaseerde ervaringscampagnes door besluitvormingsbeleid kunnen worden leveraged. [Meer informatie](../experience-decisioning/fragments-decision-policies.md)

  **Nota**: Eerder vrijgegeven in Beperkte Beschikbaarheid, is dit vermogen nu beschikbaar aan alle milieu&#39;s (Algemene Beschikbaarheid).

  Beschikbaarheidsdatum: 12 februari 2026.


#### Sms

* **Webhooks van SMS** - <strong> Webhooks </strong> worden nu gesteund over alle leveranciers van SMS. U kunt elke webhaak vormen die op zijn voorgenomen doel wordt gebaseerd: <strong> Binnenkomende webhooks </strong> om inkomende berichten en <strong> Terugkoppeling webhooks </strong> te vangen om leveringsontvangstbewijzen, statusupdates, en andere op bericht betrekking hebbende gebeurtenissen te ontvangen. [Meer informatie](../sms/sms-webhook.md)

  Beschikbaarheidsdatum: 2 februari 2026.