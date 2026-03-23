---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 18bb9845554b4610c0d07ac7ec2a711e2230a01d
workflow-type: tm+mt
source-wordcount: '2989'
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

## Opmerkingen voorafgaand aan de release van 26 maart {#march-26-rn}

**de pre-versienota&#39;s hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. Koppelingen, schermen en bijgewerkte documentatie worden gepubliceerd in de releaseopmerkingen op de releasedatum.

Zie ook [&#x200B; de pre-versienota&#39;s van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**de datum van de Versie**: Maart 24-25, 2026

### Nieuwe functies {#march-26-features}



<table>
<thead>
<tr>
<th><strong>Transactieberichten in geordende campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De geordende Campagnes steunen nu <strong> transactioneel overseinen </strong>, toelatend u om real time, gebeurtenis-gedreven berichten-zulke zoals ordesbevestigingen, het boeken berichten, en rekening updates-direct binnen uw campagnewerkschema teweeg te brengen.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestroomlijnde campagnes activeren met behulp van API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu een geordende campagne activeren via API. Vorm de doelcampagne als "teweeggebracht door een signaal"en publiceer het. Gebruik vervolgens een API-aanroep om de campagne te starten. De API-aanroep kan parameters bevatten die beschikbaar zijn als variabelen in de getriggerde campagne.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Testactiviteit in geordende campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Een nieuwe <strong> activiteit van de Test </strong> is nu beschikbaar in Geordende Campagnes. Deze activiteit leidt werkschemauitvoering aan verschillende takken die op bepaalde voorwaarden worden gebaseerd, toelatend u om campagnelogica en configuraties te bevestigen alvorens levende leveringen te activeren.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Codering van URL-parameters</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>URL-parameters in het bijhouden van koppelingen en bestemmingspagina's kunnen nu worden gecodeerd, zodat een extra beveiligingslaag voor vertrouwelijke parametergegevens beschikbaar is.</p>
<ul>
<li>Registreer en beheer encryptiesleutels in een specifiek <strong> register van het Beleid </strong>.</li>
<li>Gebruik de nieuwe encryptiehelper in uitdrukkingen om gevoelige gegevens in het volgen van verbindingen en het landen pagina URLs voor de vraagparameters te coderen u bij teruggevende tijd wilt beschermen.</li>
</ul>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reispad optimaliseren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gebruik de nieuwe Optimize knoop om specifieke doelgroepen te richten of A/B tests in werking te stellen om de beste weg te bepalen om aan uw zaken-centric KPIs te voldoen.
Dit hulpmiddel staat u toe om te testen en te variëren, en mededelingen, het rangschikken, en timing aan te passen om uw klanten het best te bereiken.
</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid). <a href="../building-journeys/optimize.md">Meer informatie</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ondersteuning voor opzoeken van gegevenssets tijdens reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Een nieuwe activiteit in reizen, de raadpleging van de Dataset, staat u toe om gegevens van de gegevensreeksen van het verslag van Adobe Experience Platform dynamisch terug te winnen tijdens runtime. Door gebruik te maken van deze mogelijkheid hebt u toegang tot gegevens die mogelijk niet in het profiel of de lading van de gebeurtenis zijn opgeslagen, zodat uw klanteninteractie zowel relevant als tijdig is. Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid). Raadpleeg de <a href="../building-journeys/dataset-lookup.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Acties voor native kanaal zijn afgekeurd</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Na de Algemene Beschikbaarheid van de <strong> activiteit van de Actie </strong> in Februari 2026, de activiteiten van het erfenisinheemse kanaal (E-mail, Duw, SMS, In-app, Web, op code-gebaseerde ervaring, en de Kaart van de Inhoud) in het reiscanvas worden nu afgekeurd.</p>
<p>U gebruikt nu één enkele <strong> activiteit van de Actie </strong> om alle kanaalacties te vormen, die de behoefte aan afzonderlijke kanaal-specifieke knopen vervangen.</p>
Bestaande reizen die gebruikmaken van activiteiten van het oude kanaal zullen blijven functioneren zonder dat wijzigingen of migratie vereist zijn.
<p>Raadpleeg de <a href="../building-journeys/journey-action.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ondersteuning voor besluitvorming in e-mailkanaal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt <strong> Beslissing </strong> nu gebruiken om de inhoud van uw e-mailberichten te personaliseren en te optimaliseren. Gebruik Prioriteitsscores, Formulas of AI-modellen om de meest relevante aanbiedingen en inhoud aan elke ontvanger weer te geven.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid). Met deze algemene beschikbaarheidsrelease worden spiegelpagina's nu ondersteund.</p>
<p>Raadpleeg de <a href="../experience-decisioning/create-decision-policy.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Afbeeldingen converteren naar sjablonen voor e-mailinhoud</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt afbeeldingen nu rechtstreeks in Journey Optimizer converteren naar sjablonen voor e-mailinhoud. Gebruik een door AI aangedreven analyse om automatisch gestructureerde HTML-sjablonen te genereren op basis van visuele referenties, waardoor de ontwerptijd voor e-mail aanzienlijk korter wordt.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid). <a href="../content-management/image-to-html.md">Meer informatie</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Inbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong> Inbox </strong> is een mobiele functionaliteit, beschikbaar met de Kaarten van de Inhoud, die klanten toelaat om een gecentraliseerde plaats binnen hun app of website tot stand te brengen om berichten te tonen die naar hun gebruikers worden verzonden. Dit breidt de levensduur van marketing mededelingen uit door ervoor te zorgen dat de berichten toegankelijk blijven zelfs nadat zij worden verworpen.</p>
<p>Beschikbaarheidsdatum: 31 maart 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Geavanceerde HTML-editor voor e-mailsjablonen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met de geavanceerde HTML-modus voor sjablonen voor e-mailinhoud kunt u de HTML-bron van uw inhoud bewerken in de e-mail Designer, geavanceerde expressies (zoals voorwaarden) toevoegen aan de bron en schakelen tussen de HTML-weergave en de Desktop-weergave zonder dat uw wijzigingen verloren gaan.</p>
<p>Deze mogelijkheid is alleen beschikbaar in inhoudssjablonen voor het e-mailkanaal. Deze bevindt zich momenteel in beperkte beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>Raadpleeg de <a href="../content-management/email-template-expert-mode.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 10 maart 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integratie van aangepaste Firefly-modellen en modellen voor het genereren van images van derden</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Zorgt voor een naadloze integratie van standaard- en aangepaste Firefly-modellen in combinatie met goedgekeurde externe afbeeldingsmodellen voor meer flexibiliteit, controle en uitlijning van merken bij het genereren van afbeeldingen.</p>
<p>Kies het juiste model voor uw behoeften:</p>
<ul><li> <strong> Adobe model </strong> (aangedreven door Firefly Image Model 4) voor directe beeldgeneratie zonder extra opstelling</li><li> <strong> model van de Partner </strong> (aangedreven door Gemini 2.5 Flits) voor gespecialiseerde mogelijkheden</li><li><strong> de modellen van de Douane </strong> (merkspecifieke modellen die op uw eigen activa worden opgeleid) voor de generatie van het merk die precies op uw merkidentiteit, stijl, en visuele richtlijnen richt.</li></ul>
<p>Raadpleeg de <a href="../content-management/generative-models.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 2 maart 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Live-activiteiten voor iOS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Breng real-time ervaringen rechtstreeks naar het slot van Screens en Dynamic Island van uw klanten met iOS Live Activity in Adobe Journey Optimizer. Lever live updates, van bestelling volgen en vliegstatus tot aftellingen van gebeurtenissen, live scores en voortgang van de levering, zonder dat gebruikers uw app hoeven te openen. Houd je publiek op de hoogte en betrokken op precies het juiste moment, waar ze zijn.</p>
<p>Eerder in bèta is deze mogelijkheid nu beschikbaar voor alle omgevingen (algemene beschikbaarheid).</p>
<p>Raadpleeg de <a href="../mobile-live/get-started-mobile-live.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 3 maart 2026</p>
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
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p>Raadpleeg de <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 4 maart 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Controle AI-model</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Journey Optimizer kunt u nu de gezondheid, de trainingsstatus en de prestaties van uw beslissingsAI-modellen controleren. Dit staat u toe om opleidingssucces te verifiëren, mislukkingen problemen op te lossen, en invloed op uw resultaten te begrijpen om de beste aanbiedingen voor elke klant te selecteren gebruikend AI. Merk op dat dit vermogen voor <strong> Beslissing </strong> slechts (niet voor de modellen van het Beheer van erfenisBesluit) beschikbaar is.</p>
<p>Dit vermogen is momenteel beschikbaar voor <strong> gepersonaliseerde optimalisering </strong> slechts modellen (niet auto-optimalisering).</p>
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>Raadpleeg de <a href="../experience-decisioning/ranking/ai-model-observability.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 9 maart 2026</p>
</td>
</tr>
</tbody>
</table>


### Verbeteringen {#march-26-improv}

De verbeteringen die bij deze release worden geleverd, worden hieronder weergegeven.


#### Rapportage

* **sluit beide klikken voor e-mail en SMS het melden** uit - E-mail en SMS het melden filtreert nu automatisch uit beide klikken van klikmetriek, die nauwkeurigere betrokkenheidsgegevens verstrekken en geautomatiseerd verkeer verhinderen uw prestatiescijfers te verhogen.

* **Send-Time Optimalisering: de bijgewerkte controleplaats en het nieuwe hefboomrapport** - de controles van de Optimalisering van de Send-Time (STO) zijn herplaatst aan het de configuratiemenu van de Actie. Bovendien is er nu een nieuw liftrapport beschikbaar in Dagrapporten om de impact van STO op de maatstaven van de prestaties van uw campagne te meten.

#### Email Designer

* **E-mail Designer die in Verenigde Shell** wordt getoond - E-mail Designer wordt nu getoond binnen de Verenigde ervaring van Shell, die een verenigbare navigatie en kopbalervaring verstrekt die met andere toepassingen van Adobe richt.

* **de wijzesteun van de Tekst in fragmenten** - om op tekst-gebaseerde e-mailwerkschema&#39;s te steunen, kunt u tekstversies van uw visuele fragmenten voor optimaal gebruik in de gewone tekstversie van e-mails nu tot stand brengen en beheren die dat fragment omvatten.

  **Voorzichtigheid:** wanneer het gebruiken van een fragment dat vóór de huidige versie werd gecreeerd, kan de versie van de fragmenttekst verkeerd worden teruggegeven-zowel in E-mail Designer als in definitieve e-mail die aan uw ontvangers wordt geleverd. Voor de beste resultaten met oudere fragmenten kunt u elk fragment bewerken, opslaan en opnieuw publiceren.

#### Beslissing

* **de veranderingsvoer van de fragmentverwijzing van de Uitdrukking in Edge Decisioning** - Deze verhoging staat veranderingen in fragmentverwijzingen toe om automatisch in alle punten worden weerspiegeld die fragmenten van verwijzingen voorzien, zonder om het even wat te verfrissen manueel (het herpubliceren van de campagne of het besluitvormingsbeleid).

* **Facultatieve fragmenten in besluitvormingspunten** - wanneer het gebruiken van fragmenten in besluitvormingspunten, kunt u een fragment facultatief nu maken zodat als het tijdelijk op Edge niet beschikbaar is, het wordt overgeslagen en de reis of de campagne blijft teruggeven in plaats van het ontbreken.

#### Configuratie

* **Omslagen voor reizen en campagnes** - u kunt uw reizen en campagnes in omslagen nu organiseren, toelatend gestructureerde navigatie en gemakkelijker beheer voor teams die met grote volumes van inhoud werken. Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

* **de Secundaire de Naam van Dataset van de Gebeurtenis van de Terugkoppeling van AJO Secundaire Ontvanger** anders - de `AJO Email BCC Feedback Event` Dataset is anders genoemd aan `AJO Secondary Recipient Feedback Event` Dataset. Het effect varieert afhankelijk van uw situatie:

   * **Bestaande gebruikers**: Slechts wordt de vertoningsnaam bijgewerkt. De onderliggende tabelnaam blijft ongewijzigd.
   * **Nieuwe gebruikers en zandbakken**: Zowel wijzen de vertoningsnaam als de lijstnaam op de nieuwe naam.
   * **Bestaande gebruikers met nieuwe zandbakken**: Zowel worden de vertoningsnaam als de lijstnaam bijgewerkt aan de nieuwe naam.

  Beschikbaarheidsdatum: 2 maart 2026

#### Geordende campagnes

* **Globale variabelen in Geordende Campagnes** - Geordende Campagnes steunen nu globale variabelen die eens kunnen worden bepaald en over alle activiteiten binnen een werkschema worden hergebruikt, die configuratie vereenvoudigen en consistentie in dynamische waarden, uitdrukkingen, en inhoudsprijdmaking verzekeren.

* **vereenvoudiging van de dimensie van het Doel in Geordende Campagnes** - u kunt of automatisch het recht selecteren en de secundaire dimensies in Geordende campagnes voor nauwkeurige, efficiënte publieksactivering nu selecteren of automatisch aftrekken.

#### Journeys

* **Golf die berichten in reizen** verzendt - u kunt berichten van de reizen van Journey Optimizer nu plannen die in gecontroleerde partijen in tijd moeten worden geleverd. [Meer informatie](../building-journeys/send-using-waves.md)

  Eerder vrijgegeven in Beperkte Beschikbaarheid voor gebruik in reizen, is deze capaciteit nu beschikbaar aan alle milieu&#39;s (Algemene Beschikbaarheid).

  Beschikbaarheidsdatum: 16 maart 2026

* **Pauzeer en hervat details in reis technische details** - de reis **technische details** omvatten nu extra pauze en hervat informatie: de datum en de tijd van de laatste pauze en hervat, de vertoningsnaam en interne herkenningsteken van de gebruiker die elke actie, en een volledige reeks gepauzeerde reismontages zoals pauze gedrag, maximumpauzeduur, en auto-hervat staat uitvoerde. [Meer informatie](../building-journeys/journey-properties.md)

  Beschikbaarheidsdatum: 2 maart 2026


## Opmerkingen bij de release van februari &#39;26 {#feb-26-01-rn}

De [&#x200B; Nieuwe mogelijkheden &#x200B;](#feb-26-01-features) en [&#x200B; secties van Verbeteringen &#x200B;](#feb-26-01-improv) behandelen reeds beschikbare mogelijkheden. <!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in February.-->

<!--**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

<!--**Release date**: February 17-18, 2026-->

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


* **de fragmenten van de Band aan besluitvormingspunten** - Journey Optimizer verstrekt nu de capaciteit om fragmenten aan besluitvormingspunten vast te maken die in code-gebaseerde ervaringscampagnes door besluitvormingsbeleid kunnen worden leveraged. [Meer informatie](../experience-decisioning/fragments-decision-policies.md)

  Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu&#39;s (Algemene Beschikbaarheid).

  Beschikbaarheidsdatum: 12 februari 2026.

#### Personalisatie

* **hulp van Metagegevens van de Uitvoering** - de `executionMetadata` hulpfunctie is nu beschikbaar aan alle klanten van Journey Optimizer. Gebruik dit schema om contextuele informatie dynamisch toe te voegen aan elke native handeling en deze vast te leggen in een gegevensset voor export naar externe systemen. [Meer informatie](../personalization/functions/helpers.md#execution-metadata)

  Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu&#39;s (Algemene Beschikbaarheid).

  Beschikbaarheidsdatum: 20 februari 2026.

#### Sms

* **Webhooks van SMS** - Webhooks worden nu gesteund over alle leveranciers van SMS. U kunt elke WebHaak vormen die op zijn voorgenomen doel wordt gebaseerd: Binnenkomende webhooks om inkomende berichten en Terugkoppeling webhooks te vangen om leveringsontvangstbewijzen, statusupdates, en andere bericht-gerelateerde gebeurtenissen te ontvangen. [Meer informatie](../sms/sms-webhook.md)

  Beschikbaarheidsdatum: 2 februari 2026.

<!--## Coming soon {#coming-soon}

The features and improvements below are planned for release later in February. Release dates and scope may change without prior notice.

### Improvements {#coming-soon-improv}

* **Decisioning preview in Code-based Experience channel** - You can now preview decision items when configuring Decisioning with the Code-based Experience channel. Preview is available directly in the authoring interface before going live.

  Availability date: February 18, 2026
-->

