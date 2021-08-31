---
title: Aanvullende informatie
description: Journey Optimizer Release-aantekeningen
source-git-commit: 1c299ec022a3985c2e9b164bc57d36948f0941d5
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 10%

---


# Release-opmerkingen {#release-notes}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen voor [!DNL Journey Optimizer]. U kunt ook de nieuwste [Documentatie-updates](documentation-updates.md) raadplegen.


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
<p>Raadpleeg voor meer informatie de <a href="building-journeys/journeys-message.md#send-time-optimization">gedetailleerde documentatie</a>.</p>
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
<p>Raadpleeg voor meer informatie de <a href="event/experience-event-schema.md#leverage_schema_relationships">gedetailleerde documentatie</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Personalized URLs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized URLs take recipients to specific pages of a website, or to a personalized microsite, depending on the profile attributes. In Adobe Journey Optimizer, you can now add personalization to URLs in your message content. URL personalization can be applied to text and images, and use profile data or contextual data.</p>
<p>For more information, refer to the <a href="documentation-updates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

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
<p>Raadpleeg voor meer informatie de <a href="configuration/retries.md#retry-duration">gedetailleerde documentatie</a>.</p>
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
<p>Raadpleeg voor meer informatie de <a href="configuration/manage-suppression-list.md#add-addresses-and-domains">gedetailleerde documentatie</a>.</p>
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

**Journeys**

* **Dynamische headers**  - U kunt nu dynamische gegevens doorgeven in HTTP-headerparameters. Deze parameters kunnen door de integratiesystemen worden gebruikt die de vraag van HTTP van de reisactie, bijvoorbeeld timestamp of het volgen identiteitskaart ontvangen. [Meer informatie](action/about-custom-action-configuration.md#url-configuration)
* **Dynamische URL-paden**  - U kunt nu dynamische URL-paden instellen voor aangepaste handelingen. [Meer informatie](action/about-custom-action-configuration.md#url-configuration)
* De algemene vertragingssnelheid voor gelezen segmenten is veranderd van 17.000 in 20.000 berichten per seconde. [Meer informatie](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Gebruikersinterface**

* **Zoeken**  - Op elke pagina, kunt u bedrijfsvoorwerpen en hulpartikelen van het Verenigde Experience Cloud onderzoeksgebied nu direct zoeken. [Meer informatie](user-interface.md#unified-search)
* **Recenten**  - De weergave van elementen uit de beginpagina van Adobe Journey Optimizer wordt nu uitgebreid naar extra zakelijke objecten. Met deze update, omvatten de kortere weg aan uw onlangs betreden Berichten, Reizen, Segmenten, Schema&#39;s, Datasets, Gegevensbronnen, Gebeurtenissen, Acties, Bronnen, en Doelen. [Meer informatie](action/about-custom-action-configuration.md#passing-collection)

**Inhoud ontwerpen**

* **Achtergrond**  - Achtergrondafbeeldingen worden nu ondersteund in live voorvertoning. [Meer informatie](preview.md)
* **Een-klik-optie-uit verbinding**  - U kunt een nieuw type verbinding in uw e-mailinhoud opnemen: Met de  **Opt-** outlink kunnen gebruikers zich niet meer abonneren op het ontvangen van uw communicatie met slechts één klik, zonder dat ze opnieuw hoeven te worden omgeleid naar een bestemmingspagina om te bevestigen dat ze de communicatie willen verlaten. [Meer informatie](message-tracking.md#one-click-opt-out-link)

<!--**Personalization**

* **Expression Editor** - You can now easily add a fall-back value when defining personalization: when personalization field is empty for a profile, the fall-back value will display. [Learn more](documentation-updates.md)-->

**E-mailconfiguratie**

* **Lijst van gewenste personen**  - De lijst van gewenste personen kan nu op een niet-productiesandbox door een API vraag worden toegelaten en worden onbruikbaar gemaakt. [Meer informatie](allow-list.md#enable-allow-list)
* **Navigatie**  - De suppressielijst, die toegankelijk was via  **Beheer > Kanalen > E-mailconfiguratie >** Algemeen menu, is verplaatst naar het nieuwe  **keuzemenu** Onderdrukking, dat alle verwante mogelijkheden voor gemakkelijkere toegang verzamelt. [Meer informatie](configuration/manage-suppression-list.md#access-suppression-list)
<!--* **Suppression list** - Adding email addresses and domains into the suppression list is now available from the user interface, either one by one, either in bulk mode through a CSV file upload. [Learn more](configuration/manage-suppression-list.md#add-addresses-and-domains)-->

### Oplossingen

* Probleem met toegankelijkheid in navigatie op het tabblad Bericht verholpen.
* Probleem met lokalisatie in de labels van de e-mailontwerper is opgelost.
* Probleem verholpen wanneer u meerdere knooppunten op een pad selecteert en op Verwijderen klikt in het deelvenster Eigenschappen.
* Probleem verholpen waarbij geen nieuwe koptekst kon worden toegevoegd aan een actie die tijdens een rit werd gebruikt.
* U kunt nu nagaan waarom het maken van een berichtvoorinstelling is mislukt door een explicietere waarschuwing in de gebruikersinterface.


## Release juli 2021 {#july-2021-release}

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
<p>Raadpleeg voor meer informatie de <a href="event/experience-event-schema.md#leverage_schema_relationships">gedetailleerde documentatie</a>.</p>
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
<p>Raadpleeg voor meer informatie de <a href="allow-list.md">gedetailleerde documentatie</a>.</p>
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

