---
solution: Journey Optimizer
product: journey optimizer
title: Opmerkingen bij de vorige release (2021)
description: Opmerkingen bij de release van Journey Optimizer 2021
exl-id: 0e43be98-f471-4860-be84-8f99ab93e983
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '2067'
ht-degree: 9%

---

# Aanvullende informatie 2021 {#release-notes-2021}

Deze pagina bevat alle functies en verbeteringen voor [!DNL Journey Optimizer] vrijgegeven in 2021.


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
<p>Adobe Journey Optimizer ondersteunt nu CNAME's. Een CNAME, of Canonical Name verslag, is een verslag dat aan een ander domeinadres eerder dan een IP adres richt. De subdomeindelegatie van CNAME laat u toe om subdomain tot stand te brengen en CNAMEs te gebruiken om aan Adobe-specifieke verslagen te richten. Met behulp van deze configuratie delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS in de omgeving voor het verzenden, renderen en volgen van e-mails.</p>
<p>Deze methode wordt aanbevolen als het beleid van uw organisatie de methode voor volledige subdomeindelegatie beperkt.</p>
<p>Meer informatie over subdomeindelegatie van CNAME in het deelvenster <a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">gedetailleerde documentatie</a>.</p>
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
<p>U kunt de inhoud van uw aanbiedingen nu aanpassen met Adobe Experience Platform-profielkenmerken en -segmenten en dezelfde expressie-editorcomponent gebruiken die in de gehele gebruikersinterface van Journey Optimizer wordt gebruikt. </p>
<p>Raadpleeg de <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


Zie ook [Opmerkingen bij de release Adobe Experience Platform oktober](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html){target=&quot;_blank&quot;} voor meer wijzigingen.

### Verbeteringen

**Journeys**

* **Expression-editor** - Als energiegebruiker kunt u nu functies gebruiken om met kaarten te werken. Deze mogelijkheid kan worden benut met de abonnementenlijsten. Als voorbeeld, van een segment, kunt u een e-mailadres van een abonnementenlijst nu krijgen. [Meer informatie in dit voorbeeld](../building-journeys/message-to-subscribers-uc.md)

* **Toezicht** - De stapgebeurtenissen voor de live ritten en de testmodus zijn verbeterd. [Nieuwe velden](../reports/sharing-field-list.md#serviceevents) zijn toegevoegd met betrekking tot exporttaken voor profielen. Voor een betere gebruikerservaring zijn de velden voor stapgebeurtenissen nu ingedeeld in verschillende categorieën. Alle gebeurtenisvelden van vorige stappen zijn nog steeds beschikbaar in het dialoogvenster [stepEvents](../reports/sharing-legacy-fields.md) categorie.
* **Toegankelijkheid** - Er zijn verbeteringen aangebracht in de toegankelijkheid van reizen.
* **Verzamelingen** - Arrays met objecten die subobjecten bevatten, worden nu ondersteund. [Meer informatie](../building-journeys/collections.md)
* **Lijsten** - Lijstschermen zijn verbeterd voor reizen, gebeurtenissen, handelingen, gegevensbronnen.

**Rapportage**

* **Gegevensindeling in algemene weergave** - U kunt nu schakelen tussen getallen en percentages in het dialoogvenster **Globale weergave** van de **Uitvoering** tab.


**Beheer**

* **Voorinstellingen voor berichten bewerken** - U kunt nu voorinstellingen voor berichten bewerken en de status van de berichten controleren. [Meer informatie](../configuration/channel-surfaces.md#edit-channel-surface)
* **PTR-records bewerken** - U kunt nu PTR-records bewerken en de updatestatus ervan controleren. [Meer informatie](../configuration/ptr-records.md#edit-ptr-record)

**Personalisatie**

* **Nieuwe hulpfunctie voor datumnotatie** - U kunt nu opgeven hoe een datumtekenreeks moet worden weergegeven. [Meer informatie](../personalization/functions/dates.md#format-date)


**Beslissingsbeheer**

* **Evaluatiereeks** - Met de nieuwe en verbeterde workflow voor het maken van beslissingen kunt u niet alleen naadloos tussen beslissingsobjecten navigeren, maar hebt u ook de volledige controle over de manier waarop de verzameling van aanbiedingen door de beslissingsengine wordt geëvalueerd. Dit omvat welke verzamelingen samen of afzonderlijk worden geëvalueerd en in welke volgorde de verzamelingen moeten worden geëvalueerd. [Meer informatie](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Oplossingen

* Probleem verholpen waardoor de lijst met reizen, de berichtenlijst en de e-mailontwerper niet konden worden weergegeven als de browsertaal niet Engels was.
* Probleem verholpen met een syntaxisfout die optrad bij het toevoegen van personalisatie met een expressie in de e-mailontwerper: tekens zijn verkeerd beschermd.
* Probleem verholpen dat tot een fout van 404 leidde bij het navigeren in het dialoogvenster **Beheer** -menu.
* Probleem verholpen waarbij andere live reizen werden geïnitieerd tijdens het testen van een reis met behulp van een zakelijke gebeurtenis.


## Release september 2021 {#september-2021-release}

### Nieuwe functies

<table>
<thead>
<tr>

<th><strong>Rapportage - Beter inzicht voor doelgroep</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Nieuwe metriek zijn beschikbaar in rapportering: Gericht en Uitgesloten voor e-mail- en pushberichten zijn zichtbaar in zowel live- als algemene rapporten. </br> Om toegang te hebben tot de recentste metriek, gelieve te merken op dat u de verschillende rapporteringsdashboards voor elk kanaal en rapporttype zult moeten terugstellen. Raadpleeg voor meer informatie over het aanpassen van het dashboard de <a href="../reports/live-report.md">gedetailleerde documentatie.</a></p>
<p>Een nieuwe kolom in de lijst van de berichtuitvoering toont het aantal gerichte profielen voor elke berichtuitvoering. </p>
<p>Raadpleeg de <a href="../reports/global-report.md">gedetailleerde documentatie</a> voor meer informatie.</p>
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
<p>Raadpleeg voor meer informatie over verzamelingen de <a href="../building-journeys/collections.md">gedetailleerde documentatie</a>. </p>
<p>Het filter en de kruisfuncties zijn toegevoegd aan de lijst met functies die beschikbaar zijn in de geavanceerde expressie-editor. Dit biedt meer mogelijkheden voor het filteren en vergelijken van verzamelingen.</p>
<p>Raadpleeg de documentatie bij de <a href="../building-journeys/functions/functionfilter.md">filter</a> en <a href="../building-journeys/functions/functionintersect.md">doorsnijden</a> functies.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Journeys**

* Systeem produceerde schema&#39;s en datasets die tijdens levering voor stapgebeurtenissen zijn gecreeerd zijn nu op read-only wijze, beschermend tegen om het even welke onbedoelde wijzigingen in kritieke schema&#39;s. [Meer informatie](../reports/sharing-overview.md)
* De **Wachten** activiteit met een label dat op het canvas wordt weergegeven. Het etiket wordt ook gebruikt in rapportering en testwijzelogboeken om duidelijk te identificeren wat u doet. [Meer informatie](../building-journeys/about-journey-activities.md#best-practices)
* Vind uw gebeurtenissen en acties sneller door elementen in te filteren **Gebeurtenissen** en **Handeling** rubrieken die zoekactie gebruiken. Orchestratie-activiteiten worden niet meer gefilterd. [Meer informatie](../building-journeys/using-the-journey-designer.md)
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
<p>Verzend automatisch uw pushbericht of e-mail op het beste moment voor elke klant die u met Adobe Journey Optimizer werkt. De Optimalisering van de Send-Time, aangedreven door de diensten AI van Adobe, voorspelt de beste tijd om een e-mail of duw bericht te verzenden om overeenkomst te maximaliseren die op historische open wordt gebaseerd en tarieven uit de doos te klikken.</p>
<p>Deze functie is momenteel in bètaversie beschikbaar voor bètaklanten. Neem contact op met de klantenservice van Adobe om deel te nemen aan het bètaprogramma.</p>
<p>Raadpleeg de <a href="../building-journeys/journeys-message.md#send-time-optimization">gedetailleerde documentatie</a> voor meer informatie.</p>
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

**Journeys**

* **Dynamische koppen** - U kunt nu dynamische gegevens doorgeven in HTTP-headerparameters. Deze parameters kunnen door de integratiesystemen worden gebruikt die de vraag van HTTP van de reisactie, bijvoorbeeld timestamp of het volgen identiteitskaart ontvangen. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)
* **Dynamische URL-paden** - U kunt nu dynamische URL-paden instellen voor aangepaste handelingen. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)
* De algemene vertragingssnelheid voor gelezen segmenten is veranderd van 17.000 in 20.000 berichten per seconde. [Meer informatie](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Gebruikersinterface**

* **Zoeken** - Op elke pagina, kunt u bedrijfsvoorwerpen en hulpartikelen van het Verenigde Experience Cloud onderzoeksgebied nu direct zoeken. [Meer informatie](../start/user-interface.md#unified-search)
* **Recenten** - De weergave van recente elementen van de startpagina van Adobe Journey Optimizer wordt nu uitgebreid naar extra zakelijke objecten. Met deze update, omvatten de kortere weg aan uw onlangs betreden Berichten, Reizen, Segmenten, Schema&#39;s, Datasets, Gegevensbronnen, Gebeurtenissen, Acties, Bronnen, en Doelen. [Meer informatie](../action/about-custom-action-configuration.md#passing-collection)

**Inhoud ontwerpen**

* **Achtergrond** - Achtergrondafbeeldingen worden nu ondersteund in live voorvertoning. [Meer informatie](../email/preview.md)
* **Een-klik-koppeling voor weigeren** - U kunt een nieuw type koppeling invoegen in uw e-mailinhoud: de **Uitschakelen** de verbinding staat gebruikers toe om van het ontvangen van uw mededelingen in slechts één klik af te zien, zonder opnieuw te worden gericht aan een het landen pagina om het uit kiezen te bevestigen. [Meer informatie](../privacy/opt-out.md#one-click-opt-out-link)

**Personalisatie**

* **Expression-editor** - U kunt nu eenvoudig een terugvalwaarde toevoegen bij het definiëren van een personalisatie: als het verpersoonlijkingsgebied voor een profiel leeg is, zal de reserve waarde tonen. [Meer informatie](../personalization/functions/helpers.md)

**E-mailconfiguratie**

* **Lijst van gewenste personen** - De lijst van gewenste personen kan nu worden in- en uitgeschakeld op een niet-productiesandbox via een API-aanroep. [Meer informatie](../configuration/allow-list.md#enable-allow-list)
* **Navigatie** - De onderdrukkingslijst, die toegankelijk was onder de **Beheer > Kanalen > E-mailconfiguratie > Algemeen** is verplaatst naar het nieuwe **Onderdrukkingslijst** submenu, dat alle verwante mogelijkheden voor gemakkelijkere toegang verzamelt. [Meer informatie](../configuration/manage-suppression-list.md#access-suppression-list)

**Beslissingsbeheer**

* De manier waarop u weergaven toevoegt en configureert wanneer u een aanbod maakt, is bijgewerkt voor een betere gebruikerservaring. In het bijzonder wordt de bibliotheek met assets nu alleen weergegeven wanneer u content van het afbeeldingstype voor een weergave definieert. [Meer informatie](../offers/offer-library/creating-personalized-offers.md#representations)

### Oplossingen

* Probleem met toegankelijkheid in navigatie op het tabblad Bericht verholpen.
* Probleem met lokalisatie in de labels van de e-mailontwerper is opgelost.
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

**Journeys**

* De algemene vertragingssnelheid van alle gelezen segmenten die gelijktijdig in dezelfde sandbox worden uitgevoerd, is beperkt tot 17.000 berichten per seconde. [Meer informatie](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* De **Cacheduur** Het veld is verwijderd uit het configuratievenster van de gegevensbron. [Meer informatie](../datasource/about-data-sources.md)
* Voor externe gegevensbronnen, wordt een het maximum van 15 vraag per seconde nu automatisch bepaald. [Meer informatie](../configuration/external-systems.md#capping)
* Voor live reizen worden in het scherm met de reiseigenschappen nu de publicatiedatum en de naam van de gebruiker weergegeven die de reis heeft gepubliceerd. [Meer informatie](../building-journeys/journey-gs.md#change-properties)
* In het scherm van de reislijst, is het filter van het reistype toegevoegd. [Meer informatie](../start/user-interface.md#filter-lists)
* De **[!UICONTROL Throttling rate]** parameter is toegevoegd in de Gelezen segmentactiviteit. [Meer informatie](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Voorvertonen en testen**

* Identiteit en naamruimte zijn nu zichtbaar in het dialoogvenster **[!UICONTROL Preview]** scherm. [Meer informatie](../email/preview.md#preview-your-messages)
* Het aantal teste-mails voor proefdrukken is nu beperkt tot tien.
* Toegestane tekens voor de **Voorvoegsel van onderwerpregel** op het gebied van proefdrukken is het aantal . [Meer informatie](../email/preview.md#send-proofs)

**Editor voor persoonlijke expressie**

* De naam van de vervolgkeuzelijst met hulplijnen is gewijzigd en de volgorde ervan is gewijzigd.

### Oplossingen

* Probleem verholpen waarbij dubbele berichten werden afgeleverd voor verzending via batchberichten.
* Gebeurtenissen worden nu overeenkomstig gegenereerd wanneer het verzenden van e-mail niet wordt uitgevoerd wanneer de periode voor opnieuw proberen is verstreken.
* Oplossing voor een probleem waarbij IP-informatie ontbrak in het scherm PTR-records.
* De lokalisatie in het aanbod van het spoor in de Expression Editor is nu geïmplementeerd.
* Onjuiste spatiëring in pop-ups met gegevens gecorrigeerd.
* Probleem verholpen in de e-mailontwerper bij het uploaden van een HTML-bestand met een intern stijlblad met `background-image` eigenschap wordt niet ondersteund.
