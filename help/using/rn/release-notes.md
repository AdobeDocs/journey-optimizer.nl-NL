---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: e8edafaff94ae9498f3d0eb3d696b38cd25e4c0a
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 0%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** levert onophoudelijk nieuwe eigenschappen, verhogingen aan bestaande eigenschappen, en insectenmoeilijke situaties. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen. [!DNL Adobe Journey Optimizer] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.


## Opmerkingen bij de pre-release augustus &#39;25 {#25-8-rn}

**de Nota&#39;s van de pre hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. Koppelingen, schermen en bijgewerkte documentatie worden gepubliceerd op de releasedatum.

Zie ook [ de pre-versienota&#39;s van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

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
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
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
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
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

<table>
<thead>
<tr>
<th><strong>Adobe Experience Platform-gegevens gebruiken voor personalisatie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gebruik gegevens van [!DNL Adobe Experience Platform] in de verpersoonlijkingsredacteur om uw inhoud en besluitvormingsattributen aan te passen. Met name, staat dit u toe om de definitie van uw attributen tot extra gegevens in datasets voor bulkupdates uit te breiden die periodiek veranderen zonder het moeten manueel de attributen één voor één bijwerken.</p>
<p>Eerder uitgebracht in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's. Met deze algemene release zijn de volgende verbeteringen aangebracht:</p>
<ul>
<li>Ondersteuning van binnenkomende kanalen;</li>
<li>De hulpfunctie "datasetLookup" kan nu worden gebruikt binnen expressies en visuele fragmenten om inhoud te personaliseren met behulp van gegevens uit Adobe Experience Platform-gegevenssets,</li>
<li>Een optie in de dataset staat u nu toe om datasets voor raadpleging toe te laten verpersoonlijking, zonder het moeten een API vraag uitvoeren.</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

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

<table>
<thead>
<tr>
<th><strong>Reispad optimaliseren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer biedt u nu de mogelijkheid om uw reizen te optimaliseren door gebruik te maken van AI- en experimentatiekaders en tegelijk een naadloze bruikbaarheid en differentiatie tussen conditie en optimalisatiefuncties te garanderen.</p>
<p>U kunt paden optimaliseren om te zoeken naar, te experimenteren met of gebruik te maken van AI voor het bepalen van de volgorde van communicatie, de tijd tussen de verschillende kanalen, combinaties van kanalen en alles wat u kunt dromen op het canvas van de reis.</p>
<p>Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
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
<p>Journey Optimizer steunt een nieuwe generische activiteit van de Actie die u toelaat om zowel enige acties als multi-actie binnenkomende actiegroepen te vormen, die voor gestroomlijnde actieconfiguratie binnen het reiscanvas toestaan. Met deze nieuwe functie kunt u met name:</p>
<ul>
<li>Een vereenvoudigde native actieconfiguratie binnen het reiscanvas.</li>
<li>De capaciteit om multi-actie binnenkomende knopen te creëren.</li>
<li>De mogelijkheid om optimalisatie toe te voegen aan ingebouwde kanaalacties.</li>
<li>De mogelijkheid om experimenten en meertalige opties toe te voegen aan elke actie.</li>
</ul>
<p>Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
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
<p>Met Journey Optimizer kunt u nu aangepaste formulieren maken en deze gebruiken in bestemmingspagina's om profielkenmerken vast te leggen in de gegevensset die voor elk formulier is gedefinieerd.</p>
<p>Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p><!--This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.--></p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Optimalisatie in campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer stelt u nu in staat met de gereedschappen gepersonaliseerde en geoptimaliseerde inhoud te leveren aan het publiek van uw campagnes, zodat u experimenten met inhoud kunt uitvoeren, doelgerichte regels kunt maken en geavanceerde combinaties van beide kunt gebruiken om de doeltreffendheid van uw campagnes te maximaliseren.</p>
<p>Met Optimalisatie kunt u:</p>
<ul>
<li>Test veelvoudige inhoudsvariaties om het meest efficiënte overseinen te identificeren.</li>
<li>Aangepaste inhoud leveren op basis van gebruikerskenmerken en contextuele gegevens.</li>
<li>Combineer gerichte acties en experimenten voor geavanceerde campagnestrategieën.</li>
<li>Filter gebruikers uit die niet voldoen aan variantcriteria.</li>
<li>Zorg voor terugvalmechanismen om de betrokkenheid van de gebruiker te behouden.</li>
</ul>
<P>Wanneer de campagne live is, worden profielen beoordeeld aan de hand van de gedefinieerde criteria en op basis van overeenkomstige criteria, worden ze geleverd met de juiste ervaring of inhoud van de campagne.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Releasedatum: 8 augustus 2025</p>
<p>Voor meer informatie, verwijs naar de <a href="../campaigns/campaigns-message-optimization.md"> gedetailleerde documentatie </a></p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#Aug-25-8-improv}

De verbeteringen die bij deze release worden geleverd, worden hieronder weergegeven.

* **Beheer**

   * **de configuratiecontrolealarm van het Kanaal** - u kunt nu intekenen om systeemalarm, of door e-mail of in het het kennisgevingscentrum van Journey Optimizer te ontvangen, voor het geval dat een fout van de kanaalconfiguratie gebeurt of als een DNS verslag mist.

* **Campagnes**

   * **controle van het Tarief in uitgaande campagnes** - u kunt throttling tariefcontrole voor uitgaande campagnes (E-mail, SMS, Push berichten) nu toelaten, toestaand u om overbelasting op stroomafwaartse systemen, zoals het landen van pagina&#39;s of de platforms van de klantenzorg te verhinderen.

   * **campagne die van de Actie** plant - de campagne dagelijks, wekelijkse en maandelijkse planners zijn bijgewerkt voor betere granulariteit. U kunt nu bijvoorbeeld het aantal weken/maanden tussen de schema&#39;s instellen, bepalen op welke dag de uitvoering moet plaatsvinden en besluiten te stoppen na een bepaald aantal exemplaren of op een bepaalde datum.

   * **Geplande transactionele actiecampagnes** - Geplande transactionele actiecampagnes zijn nu beschikbaar voor het verzenden van partij, op publiek-gebaseerde transactionele mededelingen via E-mail, SMS, en de kanalen van de Duw.

* **Kanaal - duw**

   * **de vervaldatum van het pushbericht** - u kunt nu een vervaldatum voor elk Push- bericht specificeren, dat tijd-gevoelige berichten (zoals de Zwarte Verkoop van Vrijdag) verhindert na een bepaalde datum worden verzonden, zo vermijdt leverend slechte ervaring aan uw klanten.

* **Kanaal - E-mail**

   * **de gehechtheid van PDF aan e-mail** - u kunt statische dossiers van PDF aan e-mailberichten nu vastmaken die met Journey Optimizer worden verzonden. Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

* **Kanaal - SMS**

   * **Fuzzy Opt-out** - wanneer toegelaten, ontdekt de **Fuzzy Opt-out** optie binnenkomende berichten die dicht op bepaalde opt-out sleutelwoorden (b.v., &quot;CANCIL&quot;) lijken en verzendt automatisch een bevestigingsantwoord om de unsubscribe intent van de gebruiker te verifiëren. Als de gebruiker via de gedefinieerde prompt bevestigt, wordt het abonnement opgezegd.

     Merk op dat **Vage Opt-uit** slechts met Sinch en Infobip beschikbaar is.

   * **verifieer de Verbinding van SMS** - U kunt uw geloofsbrieven van SMS API binnen Adobe Journey Optimizer nu gemakkelijk testen en verifiëren door een steekproefbericht naar een aangewezen apparaat te verzenden.

* **Configuratie**

   * **Dynamische domeinsteun** - Journey Optimizer steunt nu verpersoonlijking in het volgen van URLs voor vooraf bepaalde die domeinen op het niveau van de kanaalconfiguratie worden vermeld.

   * **de kenmerkensteun van de Douane met één-Klik unsubscribe URL** - met Journey Optimizer, als u toestemming buiten Adobe beheert, kunt u een extern douaneeindpunt plaatsen door uw eigen te bepalen unsubscribe verbinding in de e-mailconfiguratie. Wanneer uw ontvangers op de koppeling voor afmelden klikken, voegt Journey Optimizer enkele standaardprofielspecifieke parameters toe aan de gebeurtenis voor het bijwerken van de toestemming.

     Als u uw koppeling voor het opzeggen van uw abonnement met één klik verder wilt aanpassen, kunt u nu aangepaste kenmerken definiëren die aan de gebeurtenis voor toestemming worden toegevoegd.

* **Beslissing**

   * **de fragmenten van de Band aan besluitvormingspunten** - Journey Optimizer verstrekt nu de capaciteit om fragmenten aan besluitvormingspunten vast te maken die in code-gebaseerde ervaringscampagnes door besluitvormingsbeleid kunnen worden leveraged.

* **Reizen**

   * **de bulkverrichtingen van de Reis** - van de lijst van uw reizen, kunt u veelvoudige punten nu selecteren. Als deze optie is geselecteerd, kunt u maximaal tien reizen per keer pauzeren of hervatten.

   * **Redirect (302) Steun in de Acties van de Douane** - de acties van de Douane kunnen HTTP 302 nu behandelen herleidt op een per-verzoekbasis. Hierdoor kunnen reizen worden geïntegreerd met API&#39;s die aanvragen doorsturen naar gelokaliseerde of regiospecifieke URL&#39;s. Omleidingen worden automatisch gevolgd, zodat de juiste inhoud zonder extra configuratie wordt geleverd.

* **Datasets**

   * **Ervaring die Bewaarplaats van Objecten bepaalt - de Gepersonaliseerde Punten van de Aanbieding** - de ingebouwde de uitvoerdataset vangt nu alle aanbiedingsattributen en levenscyclusstatus, toelatend volledige verpersoonlijking en rapportering.

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


