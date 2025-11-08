---
solution: Journey Optimizer
product: journey optimizer
title: Opmerkingen bij de vorige release (2021)
description: Opmerkingen bij de release van Journey Optimizer 2021
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hidefromtoc: true
hide: true
exl-id: 0e43be98-f471-4860-be84-8f99ab93e983
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '2032'
ht-degree: 8%

---

# Aanvullende informatie 2021 {#release-notes-2021}

Deze pagina bevat een overzicht van alle functies en verbeteringen die [!DNL Journey Optimizer] in 2021 heeft uitgebracht.

## Release november 2021 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>CNAME-subdomeindelegatie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ondersteunt nu CNAME's. Een CNAME, of Canonical Name verslag, is een verslag dat aan een ander domeinadres eerder dan een IP adres richt. De subdomeindelegatie van CNAME laat u toe om subdomain tot stand te brengen en CNAMEs te gebruiken om aan Adobe-specifieke verslagen te richten. Met behulp van deze configuratie delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS om een omgeving in te stellen voor het verzenden, renderen en volgen van e-mails.</p>
<p>Deze methode wordt aanbevolen als het beleid van uw organisatie de methode voor volledige subdomeindelegatie beperkt.</p>
<p>Leer meer over subdomain delegatie CNAME in de <a href="../configuration/delegate-subdomain.md#cname-subdomain-setup"> gedetailleerde documentatie </a>.</p>
</td>
</tr>
</tbody>
</table>


## Release oktober 2021 {#oct-2021-release}

### Nieuwe functies

<table>
<thead>
<tr>
<th><strong>Beslissingsbeheer - Simulaties aanbieden</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu simuleren welke aanbiedingen worden geleverd aan een testprofiel voor een bepaalde plaatsing in de gebruikersinterface van Journey Optimizer. Hierdoor kunt u uw besluitvormingslogica, inclusief geschiktheidsbeperkingen en classificatiealgoritmen, eenvoudig valideren voordat u ze in productie zet. Dit vermogen staat niet-technische en technische gebruikers toe om besluitvormingsbeheer snel te testen en potentiële problemen op te lossen.</p>
<p>Raadpleeg de <a href="../offers/offer-activities/simulation.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Beslissingsbeheer - Je voorstellen aanpassen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt de inhoud van uw aanbiedingen nu personaliseren met Adobe Experience Platform-profielkenmerken en -soorten publiek, met dezelfde expressie-editorcomponent die in de hele gebruikersinterface van Journey Optimizer wordt gevonden. </p>
<p>Raadpleeg de <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


Zie ook [&#x200B; de Nota&#39;s van de Versie van Adobe Experience Platform Oktober &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=nl-NL){target="_blank"} voor meer veranderingen.

### Verbeteringen

**Reizen**

* **de redacteur van de Uitdrukking** - als machtsgebruiker, kunt u functies nu gebruiken om met kaarten te werken. Deze mogelijkheid kan worden benut met de abonnementenlijsten. Als voorbeeld kunt u vanuit een publiek nu een e-mailadres ophalen uit een abonnementenlijst. [&#x200B; leer meer in deze steekproef &#x200B;](../building-journeys/message-to-subscribers-uc.md)

* **Controle** - De gebeurtenissen van de Stap voor levende reizen en testwijze zijn verbeterd. [&#x200B; de Nieuwe gebieden &#x200B;](../reports/sharing-field-list.md#servicevents-field) zijn toegevoegd met betrekking tot de banen van de profieluitvoer. Voor een betere gebruikerservaring zijn de velden voor stapgebeurtenissen nu ingedeeld in verschillende categorieën. Alle vorige gebieden van stapgebeurtenissen zijn nog beschikbaar in de [&#x200B; stepEvents &#x200B;](../reports/sharing-legacy-fields.md) categorie.
* **Toegankelijkheid** - de verhogingen van de Toegankelijkheid zijn uitgevoerd in reizen.
* **Inzamelingen** - de series van voorwerpen die subvoorwerpen bevatten worden nu gesteund. [Meer informatie](../building-journeys/collections.md)
* **Lijsten** - de schermen van lijsten zijn verbeterd voor reizen, gebeurtenissen, acties, gegevensbronnen.

**Meldend**

* **formaat van Gegevens in Globale mening** - u kunt nu tussen aantallen en percentages in de **Globale mening** van de **Uitvoering** tabel van een knevel voorzien.


**Beheer**

* **geeft berichtvoorinstellingen** uit - u kunt berichtvoorinstellingen nu uitgeven en hun updatestatus controleren. [Meer informatie](../configuration/channel-surfaces.md#edit-channel-surface)
* **geeft PTR verslagen** uit - u kunt PTR verslagen nu uitgeven en hun updatestatus controleren. [Meer informatie](../configuration/ptr-records.md#edit-ptr-record)

**Personalization**

* **Nieuwe hulpfunctie voor datum het formatteren** - u kunt nu specificeren hoe een datumkoord zou moeten worden vertegenwoordigd. [Meer informatie](../personalization/functions/dates.md#format-date)


**Beheer van het Besluit**

* **het rangschikken van de Evaluatie** - de nieuwe en betere stroom van de besluitvormingsverwezenlijking laat u toe om niet alleen tussen besluitvormingsvoorwerpen foutloos te navigeren, maar geeft u ook een volledige controle van hoe de aanbiedingsinzamelingen door de besluitvormingsmotor worden geëvalueerd. Dit omvat welke verzamelingen samen of afzonderlijk worden geëvalueerd en in welke volgorde de verzamelingen moeten worden geëvalueerd. [Meer informatie](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Oplossingen

* Probleem verholpen waardoor de lijst met reizen, de berichtenlijst en de e-maillijst van Designer niet konden worden weergegeven als de browsertaal niet Engels was.
* Probleem verholpen met een syntaxisfout die optrad bij het toevoegen van personalisatie met een expressie in de e-mailtoepassing: tekens zijn ten onrechte beschermd.
* Vaste een kwestie die tot een fout 404 leidde toen het navigeren in het **1&rbrace; menu van het Beleid.**
* Probleem verholpen waarbij andere live reizen werden geïnitieerd tijdens het testen van een reis met behulp van een zakelijke gebeurtenis.


## Release september 2021 {#september-2021-release}

### Nieuwe functies

<table>
<thead>
<tr>

<th><strong>Rapportage - Betere insight voor doelgroep</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Er zijn nieuwe meetgegevens beschikbaar in rapportage: Gericht en Uitgesloten voor e-mail- en pushberichten zijn zowel in live als in global-rapporten zichtbaar. </br> Als u toegang wilt hebben tot de meest recente metriek, moet u de verschillende rapportdashboards voor elk kanaal en rapporttype opnieuw instellen. Voor meer informatie over dashboardaanpassing, verwijs naar de <a href="../reports/live-report.md"> gedetailleerde documentatie.</a></p>
<p>Een nieuwe kolom in de lijst van de berichtuitvoering toont het aantal gerichte profielen voor elke berichtuitvoering. </p>
<p>Raadpleeg de <a href="../reports/report-gs-cja.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Gegevenslijsten dynamisch doorgeven met behulp van aangepaste handelingen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu verzamelingen of een lijst met gegevens in de aangepaste handelingsparameters doorgeven die tijdens runtime dynamisch worden gevuld. Er worden twee soorten verzamelingen ondersteund: eenvoudige verzamelingen en objectverzamelingen. Eerder gemaakte aangepaste handelingen blijven werken. </p>
<p>Voor meer informatie over inzamelingen, verwijs naar de <a href="../building-journeys/collections.md"> gedetailleerde documentatie </a>. </p>
<p>Het filter en de kruisfuncties zijn toegevoegd aan de lijst met functies die beschikbaar zijn in de geavanceerde expressie-editor. Dit biedt meer mogelijkheden voor het filteren en vergelijken van verzamelingen.</p>
<p>Raadpleeg de documentatie over de <a href="../building-journeys/functions/list-functions.md#filter"> filter </a> en <a href="../building-journeys/functions/list-functions.md#intersect"> snijdt </a> functies.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Reizen**

* Systeem produceerde schema&#39;s en datasets die tijdens levering voor stapgebeurtenissen zijn gecreeerd zijn nu op read-only wijze, beschermend tegen om het even welke onbedoelde wijzigingen in kritieke schema&#39;s. [Meer informatie](../reports/sharing-overview.md)
* Cleanly etiketteer **&#x200B;**&#x200B;activiteit met een etiket wachten dat in het canvas zal worden getoond. Het etiket wordt ook gebruikt in rapportering en testwijzelogboeken om duidelijk te identificeren wat u doet. [Meer informatie](../building-journeys/about-journey-activities.md#best-practices)
* Vind uw gebeurtenissen en acties sneller door elementen in de **Gebeurtenissen** en **categorieën van de Actie** te filtreren gebruikend onderzoek. Orchestratie-activiteiten worden niet meer gefilterd. [Meer informatie](../building-journeys/using-the-journey-designer.md)
* Wanneer u een gebeurtenis-id-voorwaarde definieert in een op regels gebaseerde of zakelijke gebeurtenis, is de operator &quot;contains&quot; nu beschikbaar voor tekenreekstypen velden. [Meer informatie](../event/about-creating.md)

**E-mailconfiguratie**

* Wanneer een IP-pool is gekoppeld aan een berichtvoorinstelling, kunt u deze nu bewerken, waarbij de update asynchroon is. U kunt elke IP status van de poolupdate ook controleren. [Meer informatie](../configuration/ip-pools.md#edit-ip-pool)


## Release van augustus 2021 {#august-2021-release}

### Nieuwe functies

<table>
<thead>
<tr>

<th><strong>Verzend berichten op het beste ogenblik - Send-Time Optimalisering</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Verzend automatisch uw pushbericht of e-mail op het beste moment voor elke klant die u met Adobe Journey Optimizer werkt. Optimalisatie voor Send-Time, aangedreven door Adobe AI-services, voorspelt de beste tijd om een e-mail- of pushbericht te verzenden om de betrokkenheid te maximaliseren op basis van een open historie en het klikken op snelheden buiten het vak.</p>
<p>Deze functie is momenteel in bètaversie beschikbaar voor bètaklanten. Neem contact op met de klantenservice van Adobe om deel te nemen aan het bètaprogramma.</p>
<p>Raadpleeg de <a href="../building-journeys/send-time-optimization.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Relaties tussen schema's van de hefboomwerking in bedrijfsgebeurtenissen - het beheer van de opzoeklijst</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt hefboomwerkingsverhoudingen tussen schema's nu wanneer het vormen van een bedrijfsgebeurtenissen. Dit komt naast de capaciteit aan hefboomwerkings gebieden van verbonden lijsten wanneer het vormen van een eenheidsgebeurtenis, wanneer het gebruiken van voorwaarden in een reis, in berichtverpersoonlijking, en in de verpersoonlijking van de douaneactie.</p>
<p>Raadpleeg de <a href="../event/experience-event-schema.md#leverage_schema_relationships">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Persoonlijke URL's</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Persoonlijke URL's sturen ontvangers naar specifieke pagina's van een website of naar een gepersonaliseerde microsite, afhankelijk van de profielkenmerken. In Adobe Journey Optimizer kunt u nu personalisatie toevoegen aan URL's in de inhoud van uw bericht. U kunt URL-aanpassing toepassen op tekst en afbeeldingen en profielgegevens of contextafhankelijke gegevens gebruiken.</p>
<p>Raadpleeg de <a href="../personalization/personalization-syntax.md#perso-urls">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Zorg ervoor dat je e-mailberichten naar je gebruikers gaan - Opnieuw e-mailen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt de periode voor het opnieuw proberen nu op een vooraf ingestelde basis bepalen om ervoor te zorgen dat de pogingen voor het opnieuw proberen niet meer worden uitgevoerd wanneer niet meer nodig is. U kunt bijvoorbeeld de periode voor het opnieuw proberen instellen op 24 uur voor een bericht voor het opnieuw instellen van een wachtwoord dat een koppeling bevat die slechts een dag geldig is. Opnieuw proberen is alleen van toepassing op het e-mailkanaal.</p>
<p>Raadpleeg de <a href="../configuration/retries.md#retry-duration">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adressen definiëren om uit te sluiten van verzending - Onderdrukkingslijst</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Het toevoegen van e-mailadressen en domeinen aan de suppressielijst is nu beschikbaar bij de gebruikersinterface, één voor één, of in bulkwijze door een Csv- dossier te uploaden.</p>
<p>Raadpleeg de <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


### Verbeteringen

**Reizen**

* **Dynamische kopballen** - u kunt dynamische gegevens in HTTP- kopbalparameters nu overgaan. Deze parameters kunnen door de integratiesystemen worden gebruikt die de vraag van HTTP van de reisactie, bijvoorbeeld timestamp of het volgen identiteitskaart ontvangen. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)
* **Dynamische wegen URL** - u kunt de wegen van opstellings dynamische URL voor douaneacties nu. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)
* De totale snelheid voor leessoorten is gewijzigd van 17.000 naar 20.000 berichten per seconde. [Meer informatie](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**Gebruikersinterface**

* **Onderzoek** - op elke pagina, kunt u bedrijfsvoorwerpen en hulpartikelen van het Verenigde het onderzoeksgebied van Experience Cloud nu direct zoeken. [Meer informatie](../start/user-interface.md#unified-search)
* **Recenten** - de vertoning van recente elementen van de homepage van Adobe Journey Optimizer wordt nu uitgebreid tot extra bedrijfsvoorwerpen. Met deze update, omvatten de kortere weg aan uw onlangs betreden Berichten, Reizen, Soorten, Schema&#39;s, Datasets, Gegevensbronnen, Gebeurtenissen, Acties, Bronnen, en Doelen. [Meer informatie](../action/about-custom-action-configuration.md#passing-collection)

**Ontwerp van de Inhoud**

* **Achtergrond** - de beelden van de Achtergrond worden nu gesteund in levende voorproef. [Meer informatie](../content-management/preview-test.md)
  <!--* **One-click opt-out link** - You can insert a new type of link into your email content: the **Opt-out** link allows users to unsubscribe from receiving your communications in just one click, without being redirected to a landing page to confirm opting out. [Learn more](../privacy/opt-out.md#opt-out-personalization)-->

**Personalization**

* **de redacteur van de Uitdrukking** - u kunt nu gemakkelijk een daling-achterwaarde toevoegen wanneer het bepalen van verpersoonlijking: wanneer het verpersoonlijkingsgebied voor een profiel leeg is, zal de daling-achterwaarde tonen. [Meer informatie](../personalization/functions/helpers.md)

**E-mailconfiguratie**

* **Lijst van gewenste personen** - de lijst van gewenste personen kan nu worden toegelaten en op een niet productiesandbox door een API vraag worden onbruikbaar gemaakt. [Meer informatie](../configuration/allow-list.md#enable-allow-list)
* **Navigatie** - de suppressielijst, die onder het **Beleid > Kanalen > E-mail montages > Algemeen** menu toegankelijk was, is verplaatst naar het nieuwe **lijst van de Onderdrukking** submenu, dat alle verwante mogelijkheden voor gemakkelijkere toegang verzamelt. [Meer informatie](../configuration/manage-suppression-list.md#access-suppression-list)

**het beheer van het Besluit**

* De manier waarop u weergaven toevoegt en configureert wanneer u een aanbod maakt, is bijgewerkt voor een betere gebruikerservaring. Met name wordt de bibliotheek met middelen nu alleen weergegeven wanneer u inhoud van het afbeeldingstype definieert voor een representatie. [Meer informatie](../offers/offer-library/creating-personalized-offers.md#representations)

### Oplossingen

* Probleem met toegankelijkheid in navigatie op het tabblad Bericht verholpen.
* Probleem met lokalisatie in de Designer-labels voor e-mail opgelost.
* Probleem verholpen bij het selecteren van meerdere knooppunten in een rit en klikken op Verwijderen in het eigenschappenvenster.
* Probleem verholpen waarbij geen nieuwe koptekst kon worden toegevoegd aan een actie die tijdens een rit werd gebruikt.
* U kunt nu nagaan waarom het maken van een berichtvoorinstelling is mislukt door een explicietere waarschuwing in de gebruikersinterface.


## Release van juli 2021 {#july-2021-release}

### Nieuwe functies

<table>
<thead>
<tr>
<th><strong>Metagegevens in uw berichten gebruiken - tabelbeheer opzoeken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verrijk je ervaringen met referentiegegevens die je in Journey Optimizer hebt geladen. Voorbeelden zijn het opzoeken van metagegevens over een reserverings-id in een ervaringsgebeurtenis of het opzoeken van productinformatie van een sku in een ervaringsgebeurtenis voor gebruik op het canvas. </p>
<p>U kunt hefboomwerkingsverhoudingen tussen schema's nu om één dataset als raadplegingslijst voor een andere te gebruiken. U kunt dan hefboomwerking alle gebieden van de verbonden lijsten wanneer het vormen van een eenheidsgebeurtenis, wanneer het gebruiken van voorwaarden in een reis, in berichtverpersoonlijking, en in de verpersoonlijking van de douaneactie.</p>
<p>Raadpleeg de <a href="../event/experience-event-schema.md#leverage_schema_relationships">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Lijst van gewenste personen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu een specifieke verzendende-veilige lijst op het zandbakniveau bepalen, om een veilige milieu voor testend doel te hebben. Op een niet-productiegeval, waar de fouten kunnen voorkomen, verzekert de lijst van gewenste personen u geen risico om ongewenste berichten naar uw klanten te verzenden. Deze functie wordt ingeschakeld door gebruik te maken van onderdrukking-API's.</p>
<p>Raadpleeg de <a href="../configuration/allow-list.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Reizen**

* De algemene snelheid waarmee alle leessoorten die tegelijkertijd in dezelfde sandbox worden uitgevoerd, worden vertraagd, is beperkt tot 17.000 berichten per seconde. [Meer informatie](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Het **gebied van de duur van het Geheime voorgeheugen** is verwijderd uit de ruit van de gegevensbronconfiguratie. [Meer informatie](../datasource/about-data-sources.md)
* Voor externe gegevensbronnen, wordt een het maximum van 15 vraag per seconde nu automatisch bepaald. [Meer informatie](../configuration/external-systems.md#capping)
* Voor live reizen worden in het scherm met de reiseigenschappen nu de publicatiedatum en de naam van de gebruiker weergegeven die de reis heeft gepubliceerd. [Meer informatie](../building-journeys/journey-gs.md#change-properties)
* In het scherm van de reislijst, is het filter van het reistype toegevoegd. [Meer informatie](../start/user-interface.md#filter-lists)
* De parameter **[!UICONTROL Throttling rate]** is toegevoegd aan de publieksactiviteit Lezen. [Meer informatie](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**Voorproef en test**

* Identiteit en naamruimte zijn nu zichtbaar in het **[!UICONTROL Preview]** -scherm. [Meer informatie](../content-management/preview-test.md#preview-test)
* Het aantal teste-mails voor proefdrukken is nu beperkt tot tien.
* De karakters die voor het **worden toegestaan de lijnprefix van het Onderwerp** in proeven zijn nu beperkt. [Meer informatie](../content-management/preview-test.md#send-proofs)

**de uitdrukkingsredacteur van Personalization**

* De naam van de vervolgkeuzelijst met hulplijnen is gewijzigd en de volgorde ervan is gewijzigd.

### Oplossingen

* Probleem verholpen waarbij dubbele berichten werden afgeleverd voor verzending via batchberichten.
* Gebeurtenissen worden nu overeenkomstig gegenereerd wanneer het verzenden van e-mail niet wordt uitgevoerd wanneer de periode voor opnieuw proberen is verstreken.
* Oplossing voor een probleem waarbij IP-informatie ontbrak in het scherm PTR-records.
* De lokalisatie in het aanbod van het spoor in de Expression Editor is nu geïmplementeerd.
* Onjuiste spatiëring in pop-ups met gegevens gecorrigeerd.
* Probleem verholpen in de E-mail-Designer tijdens het uploaden van een HTML-bestand waarbij interne stijlpagina met de eigenschap `background-image` niet werd ondersteund.
