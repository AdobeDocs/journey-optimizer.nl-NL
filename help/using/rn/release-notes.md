---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 20f5dc6eab5695b485f4569ad098922a130d4b56
workflow-type: tm+mt
source-wordcount: '2143'
ht-degree: 5%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** levert onophoudelijk nieuwe eigenschappen, verhogingen aan bestaande eigenschappen, en insectenmoeilijke situaties. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen. [!DNL Adobe Journey Optimizer] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.


## Opmerkingen bij de vervroegde release juni 25 {#25-6-rn}


**de vroege versienota&#39;s hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. Koppelingen, schermen en bijgewerkte documentatie worden gepubliceerd op de releasedatum.

**de datum van de Versie**: 17-18 juni, 2025

Zie ook [ de Nota&#39;s van de preVersie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

### Nieuwe functies {#25-06-features}

De nieuwe mogelijkheden die met deze release worden geleverd, worden hieronder beschreven.


<table>
<thead>
<tr>
<th><strong>RCS-berichten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Het Rich Communication Services (RCS) overseinen wordt nu gesteund in Journey Optimizer, toelatend de volgende verbeterde overseinenmogelijkheden afhankelijk van leverancier en dragersteun:</p>
<ul>
<li>Branded en de geverifieerde steun van de afzender: verzend berichten gebruikend geverifieerde bedrijfsprofielen met branding elementen (embleem, afzendernaam, enz.).</li>
<li>Inzichten van de levering van berichten: Ontvang gedetailleerde leveringsrapporten met inbegrip van updates van de berichtstatus (b.v., verzonden, geleverd, gelezen).</li>
<li>Koppelingentracering: sluit URL's in RCS-berichten in en traceer deze voor betrokkenheidsanalyses.</li>
<li>Terugvallen op SMS: Automatische fallback aan SMS wanneer het apparaat van het profiel geen RCS steunt of tijdelijk onbereikbaar via RCS is.</li>
<li>Basisberichtcompositie: Verstuur op tekst gebaseerde RCS-berichten met optionele media en rijke elementen, afhankelijk van de providerondersteuning.</li>
</ul>
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formuliervelden in ervaringsinhoud op basis van code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu specifieke bewerkbare velden definiëren in JSON- of HTML-inhoudssjablonen, waarmee niet-technische gebruikers inhoud eenvoudig kunnen bewerken in een formulierweergave in de op code gebaseerde ervaring in het maken van kanalen zonder dat ze code hoeven te bewerken.<br /> meer dan dat, wanneer het bepalen van de code-gebaseerde malplaatjes van de ervaringsinhoud kunt u besluitvormingsbeleid in het malplaatje nu opnemen, die herbruikbaarheid en gebruiksgemak verhogen.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aangepaste delegatiemethode voor subdomeinen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Naast de volledige delegatie en de methode CNAME, is een nieuwe subdomain configuratiemethode nu beschikbaar: de de delegatiemethode van de Douane, die u toelaat om volledig het controleren en het handhaven van alle aspecten van DNS te bezitten die voor het leveren, het teruggeven en het volgen van berichten worden vereist.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Inhoudsbesnoeiingsactiviteit tijdens reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu persoonlijke aanbiedingen opnemen in uw reizen door middel van een speciale activiteit voor het bepalen van inhoud in het reiscanvas en deze gebruiken in reisactiviteiten, waaronder voorwaarden en aangepaste acties.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid) en wordt globaal geïmplementeerd in een toekomstige release.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reizen op reis</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Reis Dry run is een speciale publicatiemodus in Adobe Journey Optimizer die reisartsen in staat stelt een reis te testen met behulp van echte productiegegevens zonder contact op te nemen met echte klanten of profielinformatie bij te werken. Deze functie helpt reisartsen vertrouwen te winnen in hun reisontwerp en doelgroep voordat ze het live publiceren.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid) en wordt globaal geïmplementeerd in een toekomstige release.</p>
</td>
</tr>
</tbody>
</table>

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
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid) en wordt globaal geïmplementeerd in een toekomstige release.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Schaal de winnaar van uw proefversie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Schaal de winnaar van de proefversie kunt u de winnende variatie van een experiment automatisch of handmatig voor alle gebruikers uitrollen. Deze functie zorgt ervoor dat u, zodra een topuitvoerder is geïdentificeerd, het bereik en de effectiviteit ervan kunt maximaliseren zonder voortdurend handmatig toezicht.</p>
<p>Raadpleeg de <a href="../content-management/content-experiment.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 2 juni 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflict en prioriteit</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer is het beheren van het volume en de timing van campagnes en reizen van essentieel belang om te voorkomen dat klanten met te veel interacties worden overspoeld. Journey Optimizer biedt nu diverse hulpmiddelen voor conflictbeheer en prioritering - voorheen alleen beschikbaar voor organisaties met beperkte toegang (LA) - die nu algemeen beschikbaar zijn (GA).</p>
<p>Eerder uitgebracht in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's. Met deze algemene release zijn de volgende verbeteringen aangebracht:</p>
<ul>
<li>Uitgebreide ondersteuning: de tools voor conflictbeheer ondersteunen nu niet alleen publiekstrajecten, maar ook eenheidsreizen en kwalificatiereizen voor het publiek.</li>
<li>Verbeterd het Oplossen van problemen: Twee nieuwe gebieden van de stapgebeurtenis zijn nu beschikbaar in de Dienst van de Vraag, toelatend u om te analyseren waarom een profiel van een reis of een campagne werd verworpen.</li>
<li>Verbeterde rapportage: in rapporten wordt nu aangegeven welke specifieke regel een profiel van een reis of campagne heeft uitgesloten, waardoor meer transparantie en activeerbare inzichten worden geboden.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Raadpleeg de <a href="../conflict-prioritization/gs-conflict-prioritization.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 3 juni 2025</p>
</td>
</tr>
</tbody>
</table>


### Verbeteringen {#25-06-improv}

De verbeteringen die bij deze release worden geleverd, worden hieronder weergegeven.

* **de regelreeksen van het Kanaal**

   * **venster van de Duur van de Douane** voor het in kaart brengen - een nieuw **gebied van de Telling van de Herhaling** is nu beschikbaar in het scherm van de reeksen van de kanaalregel, toestaand u om frequentie het in kaart brengen regels over veelvoudige dagen, weken, of maanden, afhankelijk van de gespecificeerde duur toe te passen.

   * **Uurduur** - u kunt het bedekken op een uurbasis voor de reeksen van de kanaalregel nu toepassen.

* **op code-gebaseerde ervaringen**

   * Het toevoegen van een besluitvormingsbeleid is nu beschikbaar in code-gebaseerde malplaatjes van de ervaringsinhoud.

   * Van het op code-gebaseerde de ervaringstraject of scherm van de campagneuitgave, kunt u direct een besluitvormingsbeleid toevoegen, zonder de verpersoonlijkingsredacteur te openen.

* **de Steun van CSS van de Douane in E-mail Designer**

  Met Journey Optimizer kunt u nu aangepaste CSS rechtstreeks in de e-mailtoepassing toevoegen aan uw e-mailinhoud.

* **Nieuwe van labels voorzien navigatie voor campagnes**

  Een nieuw navigatiepatroon maakt snellere toegang tot het ontwerpen van inhoud mogelijk en ondersteunt verdere uitbreiding van instellingen in alle campagnes.

* **Beslissing** - de datum van de Beschikbaarheid: 3 Juni, 2025

  Decisioning-objecten kunnen nu worden gekopieerd tussen sandboxen, waardoor test- en implementatieworkflows worden gestroomlijnd. [Meer informatie](../configuration/copy-objects-to-sandbox.md#decisioning)

* **de kenmerksteun van het Punt van het Besluit voor beslissingsregels** - de datum van de Beschikbaarheid: 4 juni, 2025

  U kunt nu kenmerken van beslissingspunten gebruiken om beslissingsregels te maken. [Meer informatie](../experience-decisioning/rules.md#create)

* **Interactieve update van API van de Uitvoering van het Bericht** - de datum van de Beschikbaarheid: 6 juni, 2025

  De Interactieve API van de Uitvoering van het Bericht staat u nu toe om het programma van aanstaande campagneuitvoering te schrappen. [Meer informatie](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}

## Release-aantekeningen mei &#39;25 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### Nieuwe functies {#25-05-features}

De nieuwe mogelijkheden die met deze release worden geleverd, worden hieronder beschreven.

<table>
<thead>
<tr>
<th><strong>Kalenderweergave voor campagne- en reisvoorraad</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In de lijsten met reizen en campagnes is nu een kalenderweergave beschikbaar. Hiermee kunt u alle reizen en campagnes in de respectieve lijsten visualiseren.</p>
<p>Deze wijziging is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Om toegang te verzoeken, gebruik <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank"> deze vorm </a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Voor meer informatie, verwijs naar deze secties: <a href="../building-journeys/journey-ui.md"> doorblader en filter uw reizen </a>, <a href="../campaigns/modify-stop-campaign.md"> campagnes van de Toegang </a>.</p>
<p>Beschikbaarheidsdatum: 28 mei 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integratie van Adobe Experience Manager Content-fragmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dankzij de integratie van Adobe Experience Manager en Adobe Journey Optimizer kunt u nu moeiteloos Adobe Experience Manager Content Fragments gebruiken in uw Journey Optimizer-inhoud. Dankzij deze naadloze verbinding is het gemakkelijker om uw AEM-inhoud rechtstreeks in Journey Optimizer te openen en te gebruiken.</p>
<p>Voorheen beschikbaar voor een beperkt aantal organisaties (LA), is deze mogelijkheid nu GA met de volgende verbetering: u kunt nu plaatsaanduidingen definiëren en aanpassingswaarden toewijzen binnen de fragmenthandtekening met de modus Editor.</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>Raadpleeg de <a href="../integrations/aem-fragments.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 23 mei 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager Dynamic Media-integratie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dynamische media-elementen zijn nu rechtstreeks beschikbaar en toegankelijk in Journey Optimizer. Dankzij deze integratie kunt u:</p>
<ul>
<li>Middelen centraal beheren met realtime updates.</li>
<li>Wijzig uw activa montages zoals breedte en hoogte onmiddellijk.</li>
<li>Pas de Dynamische malplaatjes van Media aan door uw inhoud bij te werken en verpersoonlijkingsgebieden toe te voegen.</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p>Raadpleeg de <a href="../integrations/aem-dynamic.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 23 mei 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aanvullende ID voor door gebeurtenissen veroorzaakte reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu ritten activeren met een profiel-id en een andere id, zoals een bestellings-id, een abonnement-id of een recept-id, zodat hetzelfde profiel zich meerdere keren tegelijk in dezelfde reis kan bevinden. Dit laat scenario's zoals het beheren van veelvoudige orden of abonnementen parallel toe, met elke instantie die zijn eigen weg door de reis volgt.</p>
<p>Raadpleeg de <a href="../building-journeys/supplemental-identifier.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p>Beschikbaarheidsdatum: 23 mei 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Inhoudsvariaties simuleren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>Eerder uitgebracht in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's. Met deze algemene beschikbaarheidsrelease biedt deze functie nu ondersteuning voor meertalige content en content-experimenten, waarmee u variaties kunt testen in verschillende talen en behandelingen. Bovendien worden nu contextafhankelijke kenmerken ondersteund (naast profielkenmerken), zodat inhoud nog dynamischer en situationeler kan worden getest.</p>
<img src="assets/do-not-localize/variants.gif">
<p>Raadpleeg de <a href="../test-approve/simulate-sample-input.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 23 mei 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Leespublieksschema synchroniseren met batchsegmentatietaak</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt dagelijkse reislooppas nu teweegbrengen na partijsegmentatie voltooiing. Deze optie is nu beschikbaar voor dagelijkse reizen naar alle klanten. Het staat u toe om voor een tijdvenster van maximaal 6 uren te bepalen te wachten op publieksgegevens van de banen van de partijsegmentatie, die ervoor zorgen reizen met de meest bijgewerkte gegevens lopen of als niet klaar overgeslagen worden.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>Raadpleeg de <a href="../building-journeys/read-audience.md#schedule">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 20 mei 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aangepaste SMS-provider</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer staat u nu toe om extra leveranciers van SMS voorbij de standaardopties te vormen: Sinch, Infobip, en Twilio. Met de aangepaste configuratie van de SMS-provider kunt u rechtstreeks externe providers integreren, geavanceerde aanpassingen van de payload gebruiken voor dynamisch berichten en de voorkeuren voor machtigingen beheren (opt-in/opt-out) om naleving te garanderen.</p>
<p>Raadpleeg de <a href="../sms/sms-configuration-custom.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p>Beschikbaarheidsdatum: 20 mei 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Thema's in de Designer-e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu snel vooraf goedgekeurde thema's toepassen om de consistentie van uw merk in alle e-mails te garanderen, het aanmaakproces van uw campagne te versnellen en onafhankelijk e-mails van hoge kwaliteit te produceren en de afhankelijkheid van ontwerpteams te verminderen.</p>
<p>Deze mogelijkheid is momenteel beschikbaar in bètaversie en alleen voor bètaklanten. Neem contact op met uw Adobe-vertegenwoordiger als u wilt deelnemen aan het bètaprogramma.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Raadpleeg de <a href="../email/apply-email-themes.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 14 mei 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Beslissing - nieuwe AI-formulebuilder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu specifieke rangschikkingsformules voor besluiten maken door criteria te definiëren en te combineren vanuit een nieuwe, verbeterde interface. In plaats van alleen te vertrouwen op een statische aanbiedingsprioriteit, kunt u aangepaste rangschikkingsformules definiëren die AI-modelscores combineren, prioriteiten, profielkenmerken bieden, kenmerken aanbieden en contextuele signalen via een geleide interface.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Raadpleeg de <a href="../experience-decisioning/exd-ranking-formulas.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 14 mei 2025</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#25-05-improv}

De verbeteringen die bij deze release worden geleverd, worden hieronder weergegeven.


* **Nieuwe campagnevoorwerpen steunen voor zandbakexemplaar** - de datum van de Beschikbaarheid: 15 mei, 2025

  Wanneer het kopiëren van campagnes over veelvoudige zandbakken gebruikend de pakketuitvoer en de invoermogelijkheden, worden de volgende gebiedsdelen nu ook gekopieerd: kanaalconfiguraties, experimenteervarianten en montages, besluitvormingsbeleid en punten. [Meer informatie](../configuration/copy-objects-to-sandbox.md)

* **Omslagen voor het landen van pagina&#39;s** - de datum van Beschikbaarheid: 9 mei, 2025

  Om uw openingspagina&#39;s gemakkelijk te beheren, kunt u omslagen nu gebruiken om hen effectiever in een gestructureerde hiërarchie te organiseren. [Meer informatie](../landing-pages/manage-lp.md)

* **Directe Post: SSH Zeer belangrijke steun voor verbindingen SFTP** - de datum van de Beschikbaarheid: 5 Mei, 2025

  In het Directe dossier dat van de Post configuratie verplettert, naast bestaande SFTP met wachtwoordauthentificatietype, kunt u uw direct-maildossier naar een server van SFTP met SSH zeer belangrijke authentificatie nu uitvoeren. [Meer informatie](../direct-mail/direct-mail-configuration.md)

* **pills activering voor verpersoonlijking** - de datum van de Beschikbaarheid: 5 Mei, 2025

  Er is een nieuwe knop &#39;Pills&#39; toegevoegd aan de personalisatie-editor. Wanneer deze optie is ingeschakeld, worden profielen en contextafhankelijke kenmerken weergegeven als vullingen, waardoor de leesbaarheid van de code wordt verbeterd. [Meer informatie](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Deze mogelijkheid zal de komende 30 dagen geleidelijk aan in alle omgevingen worden benut.

* **&#39;Omleiden naar URL&#39;-ondersteuning in webkanaal** - Beschikbaarheidsdatum: 20 mei 2025

  Met het Journey Optimizer-webkanaal kunt u bezoekers nu omleiden naar een andere bestaande URL in plaats van een nieuwe variant in de visuele editor te ontwerpen. Dit vermogen kan worden gebruikt om experimenten uit te voeren die twee volledig verschillende pagina&#39;s vergelijken in plaats van enkel een paar elementen binnen een pagina te veranderen. [Meer informatie](../web/create-web.md#web-redirect-to-url)

* **Omslagen voor malplaatjes en fragmenten** - de datum van de Beschikbaarheid: 20 mei, 2025

  Met mappen kunt u uw objecten gemakkelijker en effectiever ordenen in een gestructureerde hiërarchie. Eerder beschikbaar voor een reeks organisaties (LA), zijn de omslagen nu beschikbaar aan alle gebruikers (GA) om hun inhoudsmalplaatjes en fragmenten te beheren. Lees meer in de [ malplaatjes van de Inhoud ](../content-management/access-content-templates.md#folders) en [ Fragmenten ](../content-management/manage-fragments.md#folders) secties.

* **klik het volgen in e-mailmalplaatjes** - de datum van de Beschikbaarheid: 20 mei, 2025

  Klik op bijhouden op `<area>` -elementen in afbeeldingen met hyperlinks in e-mailinhoud worden nu standaard ondersteund in [!DNL Journey Optimizer] . Op deze manier zorgt u ervoor dat gebieden met afbeeldingskaarten dezelfde tekstomloop, tekstspatiëringsgegevens en toegevoegde parameters krijgen als standaardhyperlinks. [ Leer meer bij bericht het volgen ](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Rechterspoor in campagnemelijst** - Beschikbaarheidsdatum: 20 mei, 2025

  Als u in de lijst met campagnes een campagne selecteert, wordt nu een venster geopend waarin de details worden weergegeven.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.-->

<!--* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->

