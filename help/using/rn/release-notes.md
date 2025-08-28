---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ff3511e55eb56d8d5448df6d5de92dfd29ea8718
workflow-type: tm+mt
source-wordcount: '1702'
ht-degree: 2%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** levert onophoudelijk nieuwe eigenschappen, verhogingen aan bestaande eigenschappen, en insectenmoeilijke situaties. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen. [!DNL Adobe Journey Optimizer] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=nl-NL){target="_blank"}.


## Opmerkingen bij de release van augustus &#39;25 {#25-8-rn}

**de datum van de Versie**: 19 augustus, 2025

### Nieuwe functies {#Aug-25-8-features}

De nieuwe mogelijkheden die met deze release worden geleverd, worden hieronder beschreven.

<table>
<thead>
<tr>
<th><strong>Reizen onderbreken en hervatten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu uw reizen pauzeren en hervatten. Deze mogelijkheid geeft reisartsen meer controle en flexibiliteit door het tijdelijk stilleggen van de actieve reizen toe te staan zonder de ervaring van de klant te verstoren. Wanneer gepauzeerd, worden geen mededelingen verzonden, en de profielen blijven in een geschorste staat tot de reis wordt hervat.</p>
<p>U kunt slechts één reis pauzeren en hervatten, of bulkpauze uitvoeren en verrichtingen aan een groep reizen hervatten.</p>
<p>Bovendien kunt u algemene filters toepassen op gepauzeerde reizen om profielen uit te sluiten op basis van hun kenmerken.</p>
<p><img src="assets/do-not-localize/PauseResume.gif"/></p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p>Voor meer informatie, verwijs naar de <a href="../building-journeys/journey-pause.md"> gedetailleerde documentatie </a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Kalenderweergave</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In de lijsten met reizen en campagnes is nu een kalenderweergave beschikbaar. Hiermee kunt u alle reizen en campagnes in de respectieve lijsten visualiseren.</p>
<p>Eerder beschikbaar in Beperkte Beschikbaarheid, is deze eigenschap nu beschikbaar aan alle milieu's. Met deze algemene beschikbaarheidsrelease omvat deze functie:</p>
<ul>
<li>Ontwerpverbeteringen voor de navigatie in datums</li>
<li>de mogelijkheid om ontwerpcampagnes te bekijken als u een begin- en einddatum hebt ingesteld,</li>
<li>Een nieuwe instelling voor het verbergen en weergeven van kalenderitems die lange tijd worden uitgevoerd.</li>
</ul>
<p><img src="assets/do-not-localize/calendar.gif"/></p>
<p>Voor meer informatie, verwijs naar de <a href="../building-journeys/journey-ui.md#calendar"> gedetailleerde documentatie </a></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from [!DNL Adobe Experience Platform] in the personalization editor to personalize your content and decision attributes. In particular, this allows you to extend the definition of your attributes to additional data in datasets for bulk updates that change periodically without having to manually update the attributes one at a time.</p>
<p>With this release, the following enhancements have been introduced:</p>
<ul>
<li>Support of inbound channels,</li>
<li>The "datasetLookup" helper function can now be used within expression and visual fragments to personalize content using data from Adobe Experience Platform datasets,</li>
<li>An option in the dataset now allows you to enable datasets for lookup personalization, without having to perform an API call.</li>
</ul>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p>For more information, refer to the <a href="../personalization/aep-data-perso.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Journey path optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use the new Optimize node to target specific audiences or run A/B tests to determine the best path to meet your business-centric KPIs.</p>
<p>This tool allows you to test and vary, and customize communications, sequencing, and timing to best reach your customers.</p>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>For more information, refer to the <a href="../building-journeys/optimize.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Actie tijdens reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer steunt een nieuwe generische activiteit van de Actie die u toelaat om zowel enige acties als multi-actie binnenkomende actiegroepen te vormen, die voor gestroomlijnde actieconfiguratie binnen het reiscanvas toestaan. Met deze nieuwe functie kunt u met name:</p>
<ul>
<li>Een vereenvoudigde native actieconfiguratie binnen het reiscanvas.</li>
<li>De capaciteit om multi-actie binnenkomende actiegroepen te creëren.</li>
<li>De mogelijkheid om optimalisatie toe te voegen aan ingebouwde kanaalacties.</li>
<li>De mogelijkheid om experimenten en meertalige opties toe te voegen aan elke actie.</li>
</ul>
<p>Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Voor meer informatie, verwijs naar de <a href="../building-journeys/journey-action.md"> gedetailleerde documentatie </a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>PDF-bijlagen bij e-mailberichten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu een statisch PDF-bestand toevoegen aan een e-mailbericht dat met Journey Optimizer is verzonden.</p>
<ul>
<li>U kunt maximaal zes berichten verzenden met een PDF-bijlage per profiel per jaar.</li>
<li>De maximaal toegestane bestandsgrootte voor elke bijlage is 5 MB.</li>
<li>Voor elke extra grootte of elk extra volume kunt u een invoegtoepassing voor een bijlagepakket aanschaffen. Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.</li>
</ul>
<p>Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Voor meer informatie, verwijs naar de <a href="../email/pdf-attachments.md"> gedetailleerde documentatie </a></p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Optimalisatie in campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer stelt u nu in staat met de gereedschappen gepersonaliseerde en geoptimaliseerde inhoud aan uw publiek te leveren, zodat u contentexperimenten kunt uitvoeren, doelgerichte regelgeving kunt maken en geavanceerde combinaties van beide kunt gebruiken om de doeltreffendheid van uw campagnes en reizen te maximaliseren.</p>
<p>Met Optimalisatie kunt u:</p>
<ul>
<li>Test veelvoudige inhoudsvariaties om het meest efficiënte overseinen te identificeren.</li>
<li>Aangepaste inhoud leveren op basis van gebruikerskenmerken en contextuele gegevens.</li>
<li>Combineer gerichte toepassingen en experimenten voor geavanceerde strategieën.</li>
<li>Filter gebruikers uit die niet voldoen aan variantcriteria.</li>
<li>Zorg voor terugvalmechanismen om de betrokkenheid van de gebruiker te behouden.</li>
</ul>
<P>Zodra de reis of de campagne live is, worden profielen beoordeeld aan de hand van de vastgestelde criteria en op basis van passende criteria, worden zij geleverd met de juiste ervaring of inhoud.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Alleen al op 8 augustus is deze capaciteit tijdens campagnes beschikbaar op reizen die beginnen op 22 augustus.</p>
<p>Voor meer informatie, verwijs naar de <a href="../campaigns/campaigns-message-optimization.md"> gedetailleerde documentatie </a></p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#Aug-25-8-improv}

De verbeteringen die bij deze release worden geleverd, worden hieronder weergegeven.

* **Beheer**

   * **de configuratiecontrole van het Kanaal alarm** - u kunt nu intekenen om systeemalarm, of door e-mail of in het het kennisgevingscentrum van Journey Optimizer te ontvangen, voor het geval <!--a channel configuration failure happens or if --> een DNS verslag mist. [Meer informatie](../reports/alerts.md#alert-dns-record-missing)

* **AI Medewerker**

   * **Inhoudsgeneratie in veelvoudige talen** - de Inhoud kan nu in Frans, Spaans, Duits, Italiaans, Japans, Zweeds, Nederlands, en Noors worden geproduceerd. [Meer informatie](../content-management/generative-uc.md#languages)

     Beschikbaarheidsdatum: 25 augustus


* **Campagnes**

   * **controle van het Tarief in uitgaande campagnes** - u kunt tariefcontrole voor uitgaande campagnes (E-mail, SMS, Push berichten) nu toelaten, toestaand u om overbelasting op stroomafwaartse systemen, zoals het landen van pagina&#39;s of de platforms van de klantenzorg te verhinderen. [Meer informatie](../campaigns/campaign-schedule.md#rate-control)

   * **campagne die van de Actie** plant - de campagne dagelijks, wekelijkse, en maandelijkse planners zijn bijgewerkt om meer gedetailleerde controle over terugkomende programma&#39;s te verstrekken:

      * **Wekelijkse herhaling**: U kunt nu verkiezen om de campagne elke week of elke twee weken te herhalen, en de dag(en) van de week te selecteren waarop het zou moeten lopen.

      * **Maandelijkse herhaling**: U kunt nu verkiezen om de campagne elke maand of om de andere maand te herhalen, en de dag van de maand te selecteren waarop het zou moeten lopen.

      * **Dagelijkse, wekelijkse, of maandelijkse programma&#39;s**: U kunt specificeren als het terugkomende programma op een specifieke datum of na een bepaald aantal voorkomen zou moeten ophouden.

   * **Geplande transactionele actiecampagnes** - Geplande transactionele actiecampagnes zijn nu beschikbaar voor het verzenden van partij, op publiek-gebaseerde transactionele mededelingen via E-mail, SMS, en de kanalen van de Duw.

* **Kanaal - de kaarten van de Inhoud**

   * **de lay-outmalplaatjes van de kaart van de Inhoud** - Het kanaal van de kaart van de Inhoud verstrekt nu OTB berichtlay-outs die uw auteurservaring zullen stroomlijnen. Deze release bevat sjablonen voor de lay-out Kleine afbeelding, Grote afbeelding en Alleen afbeelding. [Meer informatie](../content-card/design-content-card.md)

* **Kanaal - duw**

   * **de vervaldatum van het pushbericht** - u kunt nu een vervaldatum voor elk Push- bericht specificeren, dat tijd-gevoelige berichten (zoals de Zwarte Verkoop van Vrijdag) verhindert na een bepaalde datum worden verzonden, zo vermijdt leverend slechte ervaring aan uw klanten.

* **Kanaal - SMS**

   * **Fuzzy Opt-out** - wanneer toegelaten, ontdekt de **Fuzzy Opt-out** optie binnenkomende berichten die dicht op bepaalde opt-out sleutelwoorden (b.v., &quot;CANCIL&quot;) lijken en verzendt automatisch een bevestigingsantwoord om de unsubscribe intent van de gebruiker te verifiëren. Als de gebruiker via de gedefinieerde prompt bevestigt, wordt het abonnement opgezegd. [Meer informatie](../sms/sms-configuration-sinch.md)

     >[!NOTE]
     >
     >**Fuzzy Opt-out** is slechts beschikbaar met Sinch en Infobip.

   * **verifieer de Verbinding van SMS** - U kunt uw geloofsbrieven van SMS API binnen Adobe Journey Optimizer nu gemakkelijk testen en verifiëren door een steekproefbericht naar een aangewezen apparaat te verzenden. [Meer informatie](../sms/sms-configuration-sinch.md)

* **Configuratie**

  &lt;!—* **Dynamische domeinsteun** - Journey Optimizer steunt nu volledige/basisURL verpersoonlijking voor vooraf bepaalde die domeinen door Adobe worden goedgekeurd. Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid voor een set klanten. [ las meer ](../personalization/personalization-build-expressions.md#where)-Update op Augustus 21: Het wachten op eng. om te bevestigen wanneer opgesteld op prod.—>

   * **de kenmerkensteun van de Douane met één-Klik unsubscribe URL** - met Journey Optimizer, als u toestemming buiten Adobe beheert, kunt u een extern douaneeindpunt plaatsen door uw eigen te bepalen unsubscribe verbinding in de e-mailconfiguratie. Wanneer uw ontvangers op de koppeling voor afmelden klikken, voegt Journey Optimizer enkele standaardprofielspecifieke parameters toe aan de gebeurtenis voor het bijwerken van de toestemming.

     Als u uw koppeling voor het opzeggen van uw abonnement met één klik verder wilt aanpassen, kunt u nu aangepaste kenmerken definiëren die ook aan de gebeurtenis voor toestemming worden toegevoegd. [Meer informatie](../email/list-unsubscribe.md#custom-attributes)

* **Datasets**

   * **Ervaring die Bewaarplaats van Objecten bepaalt - de Gepersonaliseerde Punten van de Aanbieding** - de ingebouwde de uitvoerdataset vangt nu alle aanbiedingsattributen en levenscyclusstatus, toelatend volledige verpersoonlijking en rapportering. [Meer informatie](../data/export-datasets.md)

   * Introduceerde versiecontrole via het veld `etag` om de consistentie te verbeteren en wijzigingen bij te houden om items betrouwbaarder aan te bieden.

* **Beslissing**

   * **de fragmenten van de Band aan besluitvormingspunten** - Journey Optimizer verstrekt nu de capaciteit om fragmenten aan besluitvormingspunten vast te maken die in code-gebaseerde ervaringscampagnes door besluitvormingsbeleid kunnen worden leveraged. Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid voor een set klanten. [Meer informatie](../experience-decisioning/create-decision.md#fragments)

* **Reizen**

   * **de bulkverrichtingen van de Reis** - van de lijst van uw reizen, kunt u veelvoudige punten nu selecteren. Als deze optie is geselecteerd, kunt u maximaal tien reizen per keer pauzeren of hervatten.

   * **Redirect (302) Steun in de Acties van de Douane** - de acties van de Douane kunnen HTTP 302 nu behandelen herleidt op een per-verzoekbasis. Hierdoor kunnen reizen worden geïntegreerd met API&#39;s die aanvragen doorsturen naar gelokaliseerde of regiospecifieke URL&#39;s. Omleidingen worden automatisch gevolgd, zodat de juiste inhoud zonder extra configuratie wordt geleverd.

   * **Veelvoudige binnenkomende acties in reizen** - om uw reisorchestratie te vereenvoudigen, kunt u verscheidene binnenkomende acties in één enkele reis nu bepalen. Deze functie was eerder beschikbaar in campagnes en stelt u in staat om meerdere op code gebaseerde ervaringen, In-app-berichten, Content Cards of webhandelingen tegelijk naar verschillende locaties te verzenden, waarbij elke actie een specifieke inhoud bevat. [Meer informatie](../building-journeys/journey-action.md#multi-action)

## Campagneorganisatie

**de datum van de Beschikbaarheid**: 4 augustus, 2025

Journey Optimizer omvat nu **Organiseren van de Campagne**, een nieuw vermogen doelgericht-gebouwd voor merk-in werking gestelde, partijcampagnes. Deze release introduceert een campagneorchestration canvas en verbeterde gegevensmodellering, die samenwerken om marketers gepersonaliseerde cross-channel campagnes te laten plannen, richten en leveren.

>[!IMPORTANT]
>
>Om tot Campagneorganisatie toegang te hebben, moet uw vergunning of de **Journey Optimizer - Campagnes &amp; Reizen** of **Journey Optimizer - het pakket van Campagnes** omvatten. Neem contact op met uw Adobe-vertegenwoordiger om uw licentie te bevestigen en indien nodig bij te werken.

![ de Orchestratie GIF van de Campagne ](assets/do-not-localize/release.gif)

Het omvat [ Relationele Schema&#39;s &amp; Datasets ](#oc-relational) en [ het Canvas van de Campagne ](#oc-canvas). Samen ontsluiten deze twee innovaties een nieuwe norm voor het organiseren van batchcampagnes in Journey Optimizer. De belangrijkste mogelijkheden worden hieronder vermeld.

### Belangrijkste mogelijkheden {#oc-capabilities}

* **multi-step werkschema&#39;s**

  Maak geavanceerde multi-kanaals batchcampagnes met de nieuwe, speciaal gebouwde campagnecorchestratiekanvas.

* **Op bestelling publiek**

  Segmentpubliek op aanvraag voor onmiddellijke activering.

* **Meerentiteitssegmentatie**

  Bouw publiek gebruikend bedrijfscontext (niet-personendimensies) zoals product, opslag, vernieuwingen, reserveringen, en meer.

* **pre-send zicht**

  Het publiek en de campagnes vóór het starten en tijdens het uitvoeren van campagnes evalueren, verfijnen en optimaliseren

### Campagnecanvas {#oc-canvas}

Een gloednieuwe visuele orchestration interface speciaal gebouwd voor batchcampagnes. Met dit canvas kunt u:

* Visuele planning van multi-step, multi-channel campagnestromen

* Ondersteuning voor publiek op aanvraag die is opgebouwd op basis van relationele query&#39;s

* Geavanceerde publiekssplitsing, wachttijden en voorwaardelijke logica

* Nauwkeurige pre-send tellingen na het toepassen van bedrijfsregels en filters

### Relationele schema&#39;s en gegevenssets {#oc-relational}

Adobe Journey Optimizer ondersteunt nu relationele entiteiten (bijvoorbeeld producten, winkels, boekingen, contracten) die zijn gekoppeld aan profielen van personen. Dit maakt segmentatie en personalisatie over multidimensionale gegevensstructuren mogelijk, waardoor gebruiksgevallen zoals:

* Eén bericht per boeking, abonnement of contract

* Segmentatie op basis van gerelateerde entiteitskenmerken (bijvoorbeeld productcategorie of locatie van winkel)

* Verbeterde adresseerbaarheid (verzend bijvoorbeeld alle bekende contacten die verbonden zijn met een entiteit)

### Waarom het belangrijk is

Deze release geeft marketeers volledige controle over merkgebaseerde batchmarketing op basis van het publiek, waarbij flexibele gegevensmodellering wordt gecombineerd met een doelgerichte orkest-ervaring. Het is speciaal ontworpen voor batchcampagneorchestratie vanuit realtime reizen en biedt geavanceerde personalisatie en schaalbaarheid.

### Meer informatie

Leer meer in de [ documentatie van het Organiseren van de Campagne ](../orchestrated/gs-orchestrated-campaigns.md).


