---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 6304c4db02526ca6e774792474d3a495c7180f95
workflow-type: tm+mt
source-wordcount: '2245'
ht-degree: 7%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** levert onophoudelijk nieuwe mogelijkheden, verhogingen aan bestaande mogelijkheden, en insectenmoeilijke situaties. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] volgt een doorlopend leveringsmodel, dat Adobe in staat stelt voortdurend nieuwe mogelijkheden, verbeteringen en oplossingen te bieden. Deze benadering maakt een schaalbare, gefaseerde implementatie van mogelijkheden mogelijk om prestaties en stabiliteit in alle omgevingen te garanderen.

Vanwege dit model worden releaseopmerkingen bijgewerkt tussen maandelijkse releases. Voor volledige details over de de versiecyclus en beschikbaarheidsfasen, zie [&#x200B; de versiecyclus van Journey Optimizer &#x200B;](releases.md).

[!DNL Adobe Journey Optimizer] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [&#x200B; de Nota&#39;s van de Versie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

## Updates van april 26 {#april-26-rn}

### Nieuwe functies {#april-26-features}

<table>
<thead>
<tr>
<th><strong>Reispad experimenteren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gebruik nieuwe <strong> optimaliseer </strong> knoop om tests A/B of multi-gewapende bandit experimenten in werking te stellen om de beste weg te bepalen om uw zaken-centric KPIs te ontmoeten. Dit hulpmiddel staat u toe om te testen en te variëren, en mededelingen, het rangschikken, en timing aan te passen om uw klanten het best te bereiken.
</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p>Als deel van de Algemene Beschikbaarheid, introduceert deze versie <strong> experimenteertype </strong> selectie (A/B of multi-gewapende bandit) en <strong> schaal de winnaar </strong> voor unitaire reizen.</p>
<p><img src="assets/do-not-localize/optimize-experiment.gif"></p>
<p>Raadpleeg de <a href="../building-journeys/path-experimentation.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 7 april 2026</p>
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
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>Raadpleeg de <a href="../inbox/inbox-gs.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 7 april 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>E-mailtekst voor AI-invakken optimaliseren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer beschikt nu over een nieuwe functie die ervoor zorgt dat uw e-mails optimaal zijn gestructureerd voor inboxes met AI-functionaliteit zoals Apple Intelligence en Google Gemini in Gmail.</p>
<p>Aangezien AI-assistenten steeds meer bepalen hoe ontvangers lezen en handelen op e-mail, helpt deze functie u inhoud te schrijven die goed functioneert in de afhandeling van AI-taken, zoals samenvatten, verkleinen, prioriteren en uitpakken van intenties.</p>
<p><img src="assets/do-not-localize/text-optimizer.gif"></p>
<p>Voor meer informatie, verwijs naar <a href="../email/llm-email-optimizer.md"> e-mailtekst voor AI inboxes </a> optimaliseren.</p>
<p>Beschikbaarheidsdatum: 3 april 2026</p>
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
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>Raadpleeg de <a href="../experience-decisioning/create-decision-policy.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 6 april 2026</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#april-26-improv}

#### Padoptimalisatie voor reizen

* **Type van Experiment** - u kunt nu tussen A/B experiment (vaste spleet bij het begin) of Multi-gewapende bandit (automatische spleet met wekelijkse gewichtsupdates) kiezen wanneer het vormen van een wegexperiment. [Meer informatie](../building-journeys/path-experimentation.md)

  Beschikbaarheidsdatum: 7 april 2026

* **experimenteren van de Weg: Schaal de Winner** - u kunt de het winnen weg van een experiment aan uw volledig publiek nu automatisch of manueel uitrollen. Zodra een winnaar wordt bepaald, kunt u zijn bereik en doeltreffendheid vergroten zonder het experiment constant te controleren. [Meer informatie](../building-journeys/path-experimentation.md#scale-winner)

  Deze mogelijkheid is alleen beschikbaar voor eenheidstreizen (gebeurtenisgestuurde en bekwaamheidsbewijzen). Deze optie is niet beschikbaar voor ritten voor lezers.

  Beschikbaarheidsdatum: 7 april 2026

* **Voorwaarden** - [&#x200B; optimaliseer &#x200B;](../building-journeys/optimize.md) activiteit is het nieuwe voertuig voor het creëren van voorwaardelijke wegen in reizen. Het vervangt de vroegere **voorwaarde** activiteit, die uit UI is verwijderd. Alle voorwaardelijke logica wordt behouden en nu behandeld door **optimaliseert** de voorwaarden van de activiteit. [Meer informatie](../building-journeys/conditions.md)

  Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu&#39;s (Algemene Beschikbaarheid).

  Beschikbaarheidsdatum: 7 april 2026

<!--
* **Adobe Experience Manager Content Fragment context while authoring** - Your Content Fragment selection stays active as you move between text fields and content blocks, so you can add more fragment fields without reopening **Open AEM Content advisor** each time. [Read more](../integrations/aem-fragments.md)

  Availability date: April 1, 2026
-->

#### Adobe Experience Manager-integratie

* **de steun van de de fragmentvariatie van de Inhoud van Adobe Experience Manager** - u kunt **variaties van het Fragment van de Inhoud** (bijvoorbeeld taal of kanaalvarianten) selecteren wanneer het opnemen van de Fragmenten van de Inhoud van Adobe Experience Manager, met betere behandeling voor scène en meertalige scenario&#39;s. [Meer informatie](../integrations/aem-fragments.md#aem-variations)

  Beschikbaarheidsdatum: 3 april 2026


## Opmerkingen bij de release van maart 1926 {#march-26-rn}

De [&#x200B; Nieuwe mogelijkheden &#x200B;](#march-26-features) en [&#x200B; secties van Verbeteringen &#x200B;](#march-26-improv) behandelen reeds beschikbare mogelijkheden. De [&#x200B; komende spoedig &#x200B;](#coming-soon) sectie maakt een lijst van eigenschappen en verbeteringen die voor versie later in Maart worden gepland.

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

**de datum van de Versie**: Maart 24-25, 2026

### Nieuwe functies {#march-26-features}

<table>
<thead>
<tr>
<th><strong>URL-parametercodering</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>URL-parameters voor het bijhouden en landen van paginakoppelingen die aan uw e-mailberichten zijn toegevoegd, kunnen nu worden gecodeerd, zodat een extra beveiligingslaag voor vertrouwelijke parametergegevens beschikbaar is.</p>
<ul>
<li>Registreer en beheer encryptiesleutels in het specifieke <strong> register van het Beleid </strong>.</li>
<li>Gebruik de nieuwe hulpfunctie "Encrypt"in uitdrukkingen om gevoelige gegevens in URLs voor de vraagparameters te coderen u bij teruggevende tijd wilt beschermen.</li>
</ul>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p><img src="assets/do-not-localize/encrypt-helper.gif"></p>
<p>Raadpleeg de <a href="../personalization/url-parameter-encryption.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 31 maart 2026</p>
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
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p><img src="assets/do-not-localize/image-converter.gif"></p>
<p>Raadpleeg de <a href="../content-management/image-to-html.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 31 maart 2026</p>
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
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>Raadpleeg de <a href="../inbox/inbox-gs.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 31 maart 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aangepaste formulieren op de bestemmingspagina</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met [!DNL Journey Optimizer] kunt u profielkenmerken vastleggen via de bestemmingspagina's.</p>
<p>U kunt aangepaste formulieren maken, ontwerpen en beheren op basis van een specifieke gegevensset. U kunt deze formulieren vervolgens gebruiken in bestemmingspagina's om de profielkenmerken van uw keuze toe te voegen aan de gegevensset die voor elk formulier is gedefinieerd.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid voor klanten in de Verenigde Staten en Australië, is dit vermogen nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>Raadpleeg de <a href="../landing-pages/lp-forms.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 26 maart 2026.</p>
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
<p><img src="../orchestrated/assets/test-1.png"></p>
<p>Raadpleeg de <a href="../orchestrated/activities/test.md">gedetailleerde documentatie</a> voor meer informatie.</p>
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
<p>Een nieuwe <strong> opzoekactie van de Dataset </strong> activiteit in reizen laat u dynamisch gegevens van het recorddataset van Adobe Experience Platform bij runtime terugwinnen — die u toegang tot informatie geeft die geen deel van het profiel of gebeurtenislading uitmaakt, zodat blijven de klanteninteractie relevant en geschikt.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid aan een beperkte reeks organisaties, is de opzoekactiviteit van Dataset in reizen nu beschikbaar aan alle klanten die recht hebben op [dataset lookup] (../data/lookup-aep-data.md), terwijl het blijven in Beperkte Beschikbaarheid.</p>
<p><img src="../building-journeys/assets/aep-data-activity.png"></p>
<p>Raadpleeg de <a href="../building-journeys/dataset-lookup.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actie vervangt kanaalspecifieke reisactiviteiten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Na de Algemene Beschikbaarheid van de <strong> activiteit van de Actie </strong> in Februari 2026, de activiteiten van het erfenisinheemse kanaal (E-mail, Duw, SMS, In-app, Web, op code-gebaseerde ervaring, en de Kaart van de Inhoud) in het reiscanvas worden nu afgekeurd.</p>
<p>U moet nu de enige activiteit van de Actie gebruiken om alle kanaalacties te vormen, die de behoefte aan afzonderlijke kanaal-specifieke knopen vervangen.</p>
<p>Bestaande reizen die gebruikmaken van activiteiten van het oude kanaal blijven functioneren zonder dat er wijzigingen of migratie vereist zijn.</p>
<p><img src="assets/do-not-localize/action-activity.gif"></p>
<p>Raadpleeg de <a href="../building-journeys/journey-action.md">gedetailleerde documentatie</a> voor meer informatie.</p>
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
<p>Deze mogelijkheid is alleen beschikbaar in inhoudssjablonen voor het e-mailkanaal. Het is momenteel in Beperkte Beschikbaarheid — neem contact op met uw Adobe-vertegenwoordiger om toegang te krijgen.</p>
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
<p>Breng ervaringen in real time rechtstreeks aan het Slot van uw klanten Screens en Dynamic Island met <strong> Live Activiteit van iOS </strong> in Adobe Journey Optimizer. Lever live updates, van bestelling volgen en vliegstatus tot aftellingen van gebeurtenissen, live scores en voortgang van de levering, zonder dat gebruikers uw app hoeven te openen. Houd je publiek op de hoogte en betrokken op precies het juiste moment, waar ze zijn.</p>
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
<p>Raadpleeg de <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html" target="_blank">gedetailleerde documentatie</a> voor meer informatie.</p>
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

<table>
<thead>
<tr>
<th><strong>Trigger Orchestrated campagnes gebruikend een signaal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De geordende campagnes kunnen nu via een <strong> API signaal </strong> worden teweeggebracht. Om deze opstelling te vormen, vorm de doelcampagne zoals <strong> teweeggebracht door een signaal </strong>, publiceer het, dan brand het gebruikend een API vraag. Alle parameters die in de API-aanroep zijn opgenomen, zijn beschikbaar als variabelen binnen de actieve campagne. Merk op dat signaal-teweeggebrachte georkesterde campagnes <strong> partij </strong> campagnes blijven en van API-teweeggebrachte campagnes verschillend zijn.</p>
<p><img src="assets/do-not-localize/oc-triggered.gif"></p>
<p>Raadpleeg de <a href="../orchestrated/trigger-orchestrated-campaign.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Transactiecategorie in geordende campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Geordende campagnes, kunt u een kanaalactiviteit aan de <strong> Transactionele </strong> categorie nu plaatsen. Dit past transactiekanaalconfiguraties op die activiteit toe en is nuttig wanneer de bedrijfsregels niet zouden moeten van toepassing zijn of wanneer de opt-in van klanten niet wordt vereist.</p>
<p><img src="assets/do-not-localize/oc-transactional.gif"></p>
<p>Raadpleeg de <a href="../orchestrated/activities/channels.md#add">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Dit vermogen zal de komende dagen geleidelijk aan naar alle regio's worden uitgebreid.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#march-26-improv}

De verbeteringen die bij deze release worden geleverd, worden hieronder weergegeven.

#### Personalisatie

* **Volledige/basisURL verpersoonlijking** - u kunt bestemming URLs personaliseren gebruikend profielattributen (bijvoorbeeld, voor het domein of de weg). U kunt deze mogelijkheid inschakelen door Adobe uw lijst met toegestane domeinen te verschaffen. [Meer informatie](../personalization/personalization-build-expressions.md#where)

  Eerder vrijgegeven in Beperkte Beschikbaarheid voor gebruik in reizen, is deze capaciteit nu beschikbaar aan alle milieu&#39;s (Algemene Beschikbaarheid).

  Beschikbaarheidsdatum: 1 april 2026

#### Rapportage

* **Send-Time Optimalisering: de bijgewerkte controleplaats en het nieuwe hefboomrapport** - de controles van de Optimalisering van de Send-Time (STO) zijn herplaatst aan het de configuratiemenu van de Actie. Bovendien is er nu een nieuw liftrapport beschikbaar in Dagrapporten om de impact van STO op de maatstaven van de prestaties van uw campagne te meten. [Meer informatie](../reports/channel-report-cja.md#optimization-models)

  Beschikbaarheidsdatum: 27 maart 2026

<!--
* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.

#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
-->
<!--
#### Decisioning

* **Optional fragments in decision items** - When using fragments in decision items, you can now make a fragment optional so that if it is temporarily unavailable on Edge, it is skipped and the journey or campaign continues rendering instead of failing.
-->

#### Configuratie

<!--* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.-->

* **de vernieuwing van het domeincertificaat van AJO is mislukt** - u kunt nu intekenen om systeemalarm, of door e-mail of in het het berichtcentrum van Journey Optimizer te ontvangen, wanneer een domeincertificaat dat voor e-maillevering wordt gebruikt bijna verloopt of reeds is verlopen. [Meer informatie](../reports/alerts.md#alert-certificates-renewal-unsuccessful)

  Beschikbaarheidsdatum: 26 maart 2026

* **de Secundaire de Naam van Dataset van de Gebeurtenis van de Terugkoppeling van AJO Secundaire Ontvanger** anders - de `AJO Email BCC Feedback Event` Dataset is anders genoemd aan `AJO Secondary Recipient Feedback Event` Dataset. Het effect varieert afhankelijk van uw situatie:

   * **Bestaande gebruikers**: Slechts wordt de vertoningsnaam bijgewerkt. De onderliggende tabelnaam blijft ongewijzigd.
   * **Nieuwe gebruikers en zandbakken**: Zowel wijzen de vertoningsnaam als de lijstnaam op de nieuwe naam.
   * **Bestaande gebruikers met nieuwe zandbakken**: Zowel worden de vertoningsnaam als de lijstnaam bijgewerkt aan de nieuwe naam.

  Beschikbaarheidsdatum: 2 maart 2026


#### Journeys

* **actie van het Profiel van de Update: steun voor veelvoudige profielattributen** - de **actie van het Profiel van de Update** steunt nu het bijwerken van tot vijf profielattributen in één enkele knoop. Eerder kon elke actie slechts één kenmerk tegelijk bijwerken, waarbij meerdere knooppunten verschillende kenmerken moesten bijwerken. Gebruik de nieuwe **Update een andere gebied** knoop om extra gebied/waardeparen toe te voegen, die canvasingewikkeldheid verminderen en prestaties verbeteren. [Meer informatie](../building-journeys/update-profiles.md)

* **Golf die berichten in reizen** verzendt - u kunt berichten van de reizen van Journey Optimizer nu plannen die in gecontroleerde partijen in tijd moeten worden geleverd. [Meer informatie](../building-journeys/send-using-waves.md)

  Eerder vrijgegeven in Beperkte Beschikbaarheid voor gebruik in reizen, is deze capaciteit nu beschikbaar aan alle milieu&#39;s (Algemene Beschikbaarheid).

  Beschikbaarheidsdatum: 16 maart 2026

* **Pauzeer en hervat details in reis technische details** - de reis **technische details** omvatten nu extra pauze en hervat informatie: de datum en de tijd van de laatste pauze en hervat, de vertoningsnaam en interne herkenningsteken van de gebruiker die elke actie, en een volledige reeks gepauzeerde reismontages zoals pauze gedrag, maximumpauzeduur, en auto-hervat staat uitvoerde. [Meer informatie](../building-journeys/journey-properties.md)

  Beschikbaarheidsdatum: 2 maart 2026

#### Beslissing

* **Beslissende migratie — bied en contextattributen** aan - de migratie API entiteitafbeelding maakt nu een lijst van **aanbiedingsattributen** (`migratedofferattributes` op het Gepersonaliseerde schema van het aanbiedingspunt) en **contextattributen** (`migratedcontextattributes` op het schema van de migratiedataset). [Meer informatie](../experience-decisioning/decisioning-migration-api.md#entity-mapping)

  Beschikbaarheidsdatum: 31 maart 2026

<!--
## Coming soon {#coming-soon}

The features and improvements below are planned for release later in March/early April. Release dates and scope are **subject to change without prior notice**.


WAITING RELEASE DATE CONFIRMATION * **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.


WAITING RELEASE DATE CONFIRMATION
* **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->

