---
title: Aanvullende informatie
description: Journey Optimizer Release-aantekeningen
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7c02f27f0160aea2c2f55c7dc5a8e7c3de3ac159
workflow-type: tm+mt
source-wordcount: '1526'
ht-degree: 11%

---

# Aanvullende informatie {#release-notes}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen voor [!DNL Journey Optimizer]. U kunt ook de nieuwste [Documentatie-updates](documentation-updates.md) raadplegen.



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
<p>Nieuwe metriek zijn beschikbaar in rapportering: Gericht en Uitgesloten voor e-mail- en pushberichten zijn zichtbaar in zowel live- als algemene rapporten. </br> Om toegang te hebben tot de recentste metriek, gelieve te merken op dat u de verschillende rapporteringsdashboards voor elk kanaal en rapporttype zult moeten terugstellen. Raadpleeg de <a href="reports/live-report.md">gedetailleerde documentatie voor meer informatie over het aanpassen van het dashboard.</a></p>
<p>Een nieuwe kolom in de lijst van de berichtuitvoering toont het aantal gerichte profielen voor elke berichtuitvoering. </p>
<p>Raadpleeg de <a href="message-monitoring.md">gedetailleerde documentatie</a> voor meer informatie.</p>
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
<p>Raadpleeg de <a href="building-journeys/collections.md">gedetailleerde documentatie</a> voor meer informatie over verzamelingen. </p>
<p>Het filter en de kruisfuncties zijn toegevoegd aan de lijst met functies die beschikbaar zijn in de geavanceerde expressie-editor. Dit biedt meer mogelijkheden voor het filteren en vergelijken van verzamelingen.</p>
<p>Raadpleeg de documentatie over de <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionfilter.html">filter</a> en <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionintersect.html">intersect</a> functies.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decision Management - Personalize your offers</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now personalize content added to your offers' representations using the expression editor.</p>
<p>For more information, refer to the <a href="offers/offer-library/creating-personalized-offers.md#content">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### Verbeteringen

**Journeys**

* Systeem produceerde schema&#39;s en datasets die tijdens levering voor stapgebeurtenissen zijn gecreeerd zijn nu op read-only wijze, beschermend tegen om het even welke onbedoelde wijzigingen in kritieke schema&#39;s. [Meer informatie](reports/sharing-overview.md)
* Geef de activiteit **wait** een duidelijk label met een label dat op het canvas wordt weergegeven. Het etiket wordt ook gebruikt in rapportering en testwijzelogboeken om duidelijk te identificeren wat u doet. [Meer informatie](building-journeys/about-journey-activities.md#best-practices)
* Vind uw gebeurtenissen en acties sneller door elementen in **Gebeurtenissen** en **Actie** categorieën te filtreren gebruikend onderzoek. Orchestratie-activiteiten worden niet meer gefilterd. [Meer informatie](building-journeys/using-the-journey-designer.md)
* Wanneer u een gebeurtenis-id-voorwaarde definieert in een op regels gebaseerde of zakelijke gebeurtenis, is de operator &quot;contains&quot; nu beschikbaar voor tekenreekstypen velden. [Meer informatie](event/about-creating.md)

**E-mailconfiguratie**

* Wanneer een IP-pool is gekoppeld aan een berichtvoorinstelling, kunt u deze nu bewerken, waarbij de update asynchroon is. U kunt elke IP status van de poolupdate ook controleren. [Meer informatie](configuration/ip-pools.md#edit-ip-pool)

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
<p>Raadpleeg de <a href="building-journeys/journeys-message.md#send-time-optimization">gedetailleerde documentatie</a> voor meer informatie.</p>
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
<p>Raadpleeg de <a href="event/experience-event-schema.md#leverage_schema_relationships">gedetailleerde documentatie</a> voor meer informatie.</p>
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
<p>Raadpleeg de <a href="personalization/personalization-syntax.md#perso-urls">gedetailleerde documentatie</a> voor meer informatie.</p>
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
<p>Raadpleeg de <a href="configuration/retries.md#retry-duration">gedetailleerde documentatie</a> voor meer informatie.</p>
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
<p>Raadpleeg de <a href="configuration/manage-suppression-list.md#add-addresses-and-domains">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Customer Alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now subscribe to event-based alerts regarding Adobe Journey Optimizer activities. The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.
</p>
<p>For more information, refer to the <a href="https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html">Adobe Experience Platform documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### Verbeteringen

**Reizen**

* **Dynamische headers**  - U kunt nu dynamische gegevens doorgeven in HTTP-headerparameters. Deze parameters kunnen door de integratiesystemen worden gebruikt die de vraag van HTTP van de reisactie, bijvoorbeeld timestamp of het volgen identiteitskaart ontvangen. [Meer informatie](action/about-custom-action-configuration.md#url-configuration)
* **Dynamische URL-paden**  - U kunt nu dynamische URL-paden instellen voor aangepaste handelingen. [Meer informatie](action/about-custom-action-configuration.md#url-configuration)
* De algemene vertragingssnelheid voor gelezen segmenten is veranderd van 17.000 in 20.000 berichten per seconde. [Meer informatie](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Gebruikersinterface**

* **Zoeken**  - Op elke pagina, kunt u bedrijfsvoorwerpen en hulpartikelen van het Verenigde Experience Cloud onderzoeksgebied nu direct zoeken. [Meer informatie](user-interface.md#unified-search)
* **Recenten**  - De weergave van elementen uit de beginpagina van Adobe Journey Optimizer wordt nu uitgebreid naar extra zakelijke objecten. Met deze update, omvatten de kortere weg aan uw onlangs betreden Berichten, Reizen, Segmenten, Schema&#39;s, Datasets, Gegevensbronnen, Gebeurtenissen, Acties, Bronnen, en Doelen. [Meer informatie](action/about-custom-action-configuration.md#passing-collection)

**Inhoud ontwerpen**

* **Achtergrond**  - Achtergrondafbeeldingen worden nu ondersteund in live voorvertoning. [Meer informatie](preview.md)
* **Een-klik-optie-uit verbinding**  - U kunt een nieuw type verbinding in uw e-mailinhoud opnemen: Met de  **Opt-** outlink kunnen gebruikers zich niet meer abonneren op het ontvangen van uw communicatie met slechts één klik, zonder dat ze opnieuw hoeven te worden omgeleid naar een bestemmingspagina om te bevestigen dat ze de communicatie willen verlaten. [Meer informatie](message-tracking.md#one-click-opt-out-link)

**Personalisatie**

* **De Redacteur**  van de uitdrukking - u kunt nu gemakkelijk een reserve waarde toevoegen wanneer het bepalen van verpersoonlijking: als het verpersoonlijkingsgebied voor een profiel leeg is, zal de reserve waarde tonen. [Meer informatie](personalization/functions/helpers.md)

**E-mailconfiguratie**

* **Lijst van gewenste personen**  - De lijst van gewenste personen kan nu op een niet-productiesandbox door een API vraag worden toegelaten en worden onbruikbaar gemaakt. [Meer informatie](allow-list.md#enable-allow-list)
* **Navigatie**  - De suppressielijst, die toegankelijk was via  **Beheer > Kanalen > E-mailconfiguratie >** Algemeen menu, is verplaatst naar het nieuwe  **keuzemenu** Onderdrukking, dat alle verwante mogelijkheden voor gemakkelijkere toegang verzamelt. [Meer informatie](configuration/manage-suppression-list.md#access-suppression-list)

**Beslissingsbeheer**

* De manier waarop u weergaven toevoegt en configureert wanneer u een aanbod maakt, is bijgewerkt voor een betere gebruikerservaring. In het bijzonder wordt de bibliotheek met assets nu alleen weergegeven wanneer u content van het afbeeldingstype voor een weergave definieert. [Meer informatie](offers/offer-library/creating-personalized-offers.md#representations)

### Oplossingen

* Probleem met toegankelijkheid in navigatie op het tabblad Bericht verholpen.
* Probleem met lokalisatie in de labels van de e-mailontwerper is opgelost.
* Probleem verholpen wanneer u meerdere knooppunten op een pad selecteert en op Verwijderen klikt in het deelvenster Eigenschappen.
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
<p>Raadpleeg de <a href="event/experience-event-schema.md#leverage_schema_relationships">gedetailleerde documentatie</a> voor meer informatie.</p>
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
<p>Raadpleeg de <a href="allow-list.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Reizen**

* De algemene vertragingssnelheid van alle gelezen segmenten die gelijktijdig in dezelfde sandbox worden uitgevoerd, is beperkt tot 17.000 berichten per seconde. [Meer informatie](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Het veld **Cacheduur** is verwijderd uit het configuratievenster van de gegevensbron. [Meer informatie](datasource/about-data-sources.md)
* Voor externe gegevensbronnen, wordt een het maximum van 15 vraag per seconde nu automatisch bepaald. [Meer informatie](configuration/external-systems.md#capping)
* Voor live reizen worden in het scherm met de reiseigenschappen nu de publicatiedatum en de naam van de gebruiker weergegeven die de reis heeft gepubliceerd. [Meer informatie](building-journeys/journey-gs.md#change-properties)
* In het scherm van de reislijst, is het filter van het reistype toegevoegd. [Meer informatie](user-interface.md#section_lgm_hpz_pgb)
* De parameter **[!UICONTROL Throttling rate]** is toegevoegd in de Gelezen segmentactiviteit. [Meer informatie](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Voorbeeld- en testberichten**

* Identiteit en naamruimte zijn nu zichtbaar in het scherm **[!UICONTROL Preview]**. [Meer informatie](preview.md#preview-your-messages)
* Het aantal teste-mails voor proefdrukken is nu beperkt tot tien.
* De tekens die zijn toegestaan voor het **voorvoegsel van de onderwerpregel** in proefdrukken zijn nu beperkt. [Meer informatie](preview.md#send-proofs)

**Editor voor persoonlijke expressie**

* De naam van de vervolgkeuzelijst met hulplijnen is gewijzigd en de volgorde ervan is gewijzigd.

### Oplossingen

* Probleem verholpen waarbij dubbele berichten werden afgeleverd voor verzending via batchberichten.
* Gebeurtenissen worden nu overeenkomstig gegenereerd wanneer het verzenden van e-mail niet wordt uitgevoerd wanneer de periode voor opnieuw proberen is verstreken.
* Oplossing voor een probleem waarbij IP-informatie ontbrak in het scherm PTR-records.
* De lokalisatie in het aanbod van het spoor binnen de Redacteur van de Uitdrukking wordt nu uitgevoerd.
* Onjuiste spatiëring in pop-ups met gegevens gecorrigeerd.
* Probleem verholpen in de e-mailontwerper tijdens het uploaden van een HTML-bestand waarbij intern stijlblad met de eigenschap `background-image` niet werd ondersteund.
