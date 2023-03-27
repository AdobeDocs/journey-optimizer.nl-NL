---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Aanvullende informatie voor Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 4399d1665fd27fdd3b2cca6cfe448464c3c79f0c
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 7%

---

# Aanvullende informatie {#release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen.

Opmerkingen bij vorige release zijn beschikbaar in [deze pagina](release-notes-2022.md). U kunt ook de [meest recente documentatie-updates](documentation-updates.md) pagina voor meer wijzigingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} vandaag, en ontvang de recentste productupdates, opwindende verhalen, gebruiksgevallen, uiteinden en meer die direct aan uw Postbus worden geleverd elk kwartaal.


## Opmerkingen bij de release Vroege maart 2023 {#mar-2023}

Onderstaande informatie kan zonder voorafgaande kennisgeving worden gewijzigd tot de beschikbaarheidsdatum van de release. Bijgewerkte documentatie wordt gepubliceerd op de releasedatum en er worden directe koppelingen toegevoegd aan deze pagina.

**Beschikbaarheidsdatum**: 29 maart

### Nieuwe functies{#mar-2023-features}


<table>
<thead>
<tr>
<th><strong>Kanaal in de app (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu binnen een campagne persoonlijke In-app-berichten naar gebruikers van de app sturen. Met Journey Optimizer kunt u meldingen ontwerpen en de lay-out, weergave, tekst en knoppen van berichten aanpassen voor een naadloze ervaring.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Raadpleeg de <a href="../in-app/get-started-in-app.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SMS-klik bijhouden</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met SMS klikt het volgen, kunt u de prestaties van uw verkorte URLs controleren, identificeren wie op hen klikte, en deze gegevens gebruiken om die klanten met verdere campagnes opnieuw te richten.</p>
<!--p>For more information, refer to the <a href="../sms/create-sms.md#sms-content">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Tags gebruiken in uw reizen (bèta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als Journey Optimizer-expert kunt u uw zakelijke objecten nu organiseren met tags. Met tags kunt u objecten snel en eenvoudig classificeren om zoekopdrachten te verbeteren. Deze functie is momenteel beschikbaar in bèta en alleen voor reizen.</p>
<p>Raadpleeg de <a href="../building-journeys/tags.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


### Verbeteringen {#mar-2023-improvements}

**Journeys**

* De nieuwe **Throttling API** Hiermee kunt u een limiet instellen voor het aantal gebeurtenissen dat per seconde wordt verzonden, zodat overweldigende verkeersspikes op uw externe systemen of API worden voorkomen. Wanneer de ingestelde limiet is bereikt, worden alle volgende API-aanroepen zo snel mogelijk in de wachtrij geplaatst en verwerkt in de volgorde waarin ze zijn ontvangen. Houd er rekening mee dat deze functie slechts ondersteuning biedt voor één configuratie met vertraagde verwerking van al uw sandboxen.
* Het canvas Journey is verbeterd voor een eenvoudigere en verbeterde gebruikerservaring. Aan het einde van elk pad op het canvas zijn de lege plaatsaanduidingen verwijderd. U kunt nu gewoon uw activiteiten toevoegen door deze aan het einde van een pad te slepen. <!--[Learn more](../building-journeys/using-the-journey-designer.md)-->
* De standaardonderbreking en foutenduur in reiseigenschappen zijn veranderd van 5 aan 30 seconden. De standaardvertragingstarief in gelezen segmentactiviteiten is veranderd van 20.000 in 5.000 berichten per seconde.
* Er is een hulplijn toegevoegd aan de testmodus om alleen te luisteren naar gebeurtenissen die via de interface worden verzonden. Er wordt geen rekening gehouden met gebeurtenissen die via een extern gereedschap worden verzonden.
* Wanneer u een actie E-mail, SMS of Push toevoegt aan een reis, wordt het oppervlak standaard voorgevuld met het laatst gebruikte oppervlak voor dat kanaal.

<!-- * A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)-->

<!--
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**Beslissingsbeheer**

* Om mogelijke verwarring met de recente versie van tags in Adobe Experience Platform te voorkomen, zijn de namen van Beslissingsbeheertags gewijzigd in &quot;Verzamelingsaanduidingen&quot;.

   Hoewel de term &quot;tag&quot; niet meer wordt gebruikt in de gebruikersinterface van het besluitvormingsbeheer, wordt deze nog steeds gebruikt in back-endservices zoals API&#39;s en datasets.

* U kunt de teller van de aanbieding nu op een dagelijkse, wekelijkse of maandelijkse basis terugstellen. <!--[Learn more](../offers/offer-library/add-constraints.md#capping)-->

* U kunt ook kiezen naar welke Adobe Experience Platform-gebeurtenis moet worden gezocht om de offer decisioning te beperken. <!--[Learn more](../offers/offer-library/add-constraints.md#capping)-->

* Er zijn aanvullende parameters toegevoegd aan het scherm Plaatsingsontwerp. Hiermee kunt u bepalen of een aanbieding op meerdere plaatsen kan worden gedupliceerd en kunt u opgeven of de inhoud en metagegevens van de aanbieding moeten worden opgenomen in de API-reactie. <!--[Learn more](../offers/offer-library/creating-placements.md)-->

## Opmerkingen bij de release februari 2023 {#feb-2023}

### Nieuwe functies{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>Kanaal in app (bèta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu binnen een campagne persoonlijke In-app-berichten naar gebruikers van de app sturen. Met Journey Optimizer kunt u meldingen ontwerpen en de lay-out, weergave, tekst en knoppen van berichten aanpassen voor een naadloze ervaring.</p>
<p><strong>Waarschuwing</strong> - Deze functie is momenteel in bètaversie beschikbaar voor bètaklanten. Neem contact op met de klantenservice van Adobe om deel te nemen aan het bètaprogramma.</p>
<p>Raadpleeg de <a href="../in-app/get-started-in-app.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Optimizer-gegevenssets exporteren naar cloudopslagdoelen (bèta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu een live verbinding maken met opslaglocaties in de cloud om de inhoud van uw gegevenssets te exporteren. Beschikbare doelen zijn: Amazon S3 Cloud Storage, Azure Blob, Azure Data Lake Gen 2, Data Landing Zone, Google Cloud Storage, SFTP.</p>
<p><strong>Waarschuwing</strong> - Deze functie is momenteel in bèta beschikbaar voor alle Adobe Journey Optimizer-gebruikers. Werk samen met uw Adobe-medewerker om toegang te krijgen tot Doelen als u nog geen toegang hebt.</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>Raadpleeg de <a href="../data/export-datasets.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++
-->

### Verbeteringen {#feb-2023-improvements}

**Journeys**

* De **Wachttijd bij terugkeer** het veld is toegevoegd aan de eigenschappen van de reis . In dit veld kunt u de tijd definiëren die u moet wachten voordat een profiel de reis weer in één keer kan betreden (te beginnen met een gebeurtenis of een segmentkwalificatie). Hierdoor wordt voorkomen dat ritten meerdere keren ten onrechte worden geactiveerd voor dezelfde gebeurtenis. Het veld wordt standaard ingesteld op 5 minuten. [Meer informatie](../building-journeys/journey-gs.md#entrance)

* Er zijn verbeteringen aangebracht voor **begin- en einddatum van de reis**. Als u geen begindatum hebt opgegeven, wordt deze nu automatisch toegevoegd op het moment van publicatie. Voor **Segment lezen** voor reizen kunt u nu een einddatum toevoegen. Hiermee kunnen profielen automatisch worden afgesloten wanneer de datum wordt bereikt. [Meer informatie](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**Beheer**

* **Lijst van gewenste personen** - U kunt de lijst van gewenste personen nu downloaden als een CSV-bestand. [Meer informatie](../configuration/allow-list.md#download-allowed-list)

* **E-mailoppervlak** - Er is een extra controle toegevoegd aan de instellingen voor het e-mailoppervlak: als de MX-record voor het subdomein dat wordt gebruikt in het dialoogvenster **Reageren op (e-mailadres)** of in de **BCC-e-mailadres** is niet behoorlijk gevormd, kan de e-mailoppervlakte niet meer worden gecreeerd. U moet het gevormd hebben of een andere gebruiken. [Meer informatie](../email/email-settings.md#reply-to-email)

* **E-mailoppervlak** - In de **Parameters voor URL-tracking** sectie van de instellingen van het e-mailoppervlak, de limiet voor elke **Waarde** Het veld is bijgewerkt van 255 tekens naar 5 kB ten behoeve van compatibiliteit met Adobe Analytics-tracking. [Meer informatie](../email/email-settings.md#url-tracking)

**Beslissingsbeheer**

* **URL-personalisatie** - Wanneer u URL&#39;s als inhoud toevoegt aan de representaties van uw aanbiedingen, kunt u deze URL&#39;s nu aanpassen met de Expressieeditor. [Meer informatie](../offers/offer-library/add-representations.md)

## Release van januari 2023 {#jan-2023-release}

### Nieuwe functies{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>Gegevenshygiëne</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform biedt een reeks mogelijkheden voor gegevenshygiëne waarmee u uw opgeslagen gegevens kunt beheren via programmatische verwijderingen van consumentengegevens en gegevenssets. Deze mogelijkheid is nu beschikbaar voor Adobe Journey Optimizer. </p>
<p>U kunt uw gegevensopslag beheren om ervoor te zorgen dat de informatie wordt gebruikt zoals verwacht, wordt bijgewerkt wanneer onjuiste gegevens het bevestigen vereisen, en wordt geschrapt wanneer het organisatorische beleid het noodzakelijk acht.</p>
<p><strong>Waarschuwing</strong> - Gegevenshygiëne-mogelijkheden zijn momenteel alleen beschikbaar voor organisaties die de <strong>Gezondheidsschild</strong> en <strong>Privacy- en beveiligingsschild</strong> add-on aanbiedingen.</p><p>Raadpleeg de <a href="../privacy/data-hygiene.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>E-mailinhoudssjablonen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu zelfstandige inhoudssjablonen maken die u kunt gebruiken voor reizen en campagnes voor snel hergebruik.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Leer hoe u inhoudssjablonen kunt maken, bewerken en gebruiken in <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html">deze video</a>. Raadpleeg de <a href="../email/content-templates.md">gedetailleerde documentatie</a> voor meer informatie.
</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#jan-2023-improvements}

**Journeys**

* Bij het toevoegen van een **Segmentkwalificatie** of **Segment lezen** in een reis, wordt namespace nu vooraf gevuld, door gebrek, met het laatst gebruikte namespace. Zie de [Segmentkwalificatie](../building-journeys/segment-qualification-events.md#about-segment-qualification) en [Segment lezen](../building-journeys/read-segment.md#configuring-segment-trigger-activity) secties.

* Op het reiscanvas is er een nieuwe knop beschikbaar op de werkbalk waarmee u een schermafbeelding van uw reis kunt downloaden.

**Email Designer**

* U kunt de e-mailinhoud nu exporteren vanuit de **HTML exporteren** -menu. Geëxporteerde bestanden zijn beschikbaar in een ZIP-bestand (archiefbestand).

**Beheer**

* Een nieuwe subsectie bevat aanbevelingen voor het opbouwen van de **Reageren op (e-mail)** het adresseren en waarborgen van een adequaat antwoordbeheer. [Meer informatie](../email/email-settings.md#reply-to-email)

* Bij het maken of bewerken **IP-pools**, worden de bijbehorende PTR- verslagen nu getoond in de IP lijst en wanneer het hangen over de geselecteerde IP adressen. [Meer informatie](../configuration/ip-pools.md#create-ip-pool)

* Nadat een IP pool in een kanaaloppervlakte is geselecteerd, is PTR- verslaginformatie nu zichtbaar wanneer het bedekken over de IP adressen. [Meer informatie](../email/email-settings.md#subdomains-and-ip-pools)

* De gebruikersinterface voor bewerken [PTR-records](../configuration/ptr-records.md#edit-ptr-record) en [uitvoeringsvelden](../configuration/primary-email-addresses.md) is bijgewerkt.

* De gebruikersinterface voor het maken en bewerken van subdomeinen is verbeterd. [Meer informatie](../configuration/delegate-subdomain.md)

* De onderdrukkingslijst **Recente uploads** scherm is bijgewerkt. [Meer informatie](../configuration/manage-suppression-list.md#recent-uploads)

**Campagnes**

* Er wordt nu automatisch een voorbeeld van een cURL-aanvraag gegenereerd die uitvoering van door de API geïnitieerde campagnes toestaat, en beschikbaar gesteld in het campagnescherm. [Meer informatie](../campaigns/api-triggered-campaigns.md)


**Personalisatie**

* Er zijn nieuwe hulpfuncties beschikbaar: formatCurrency, charCodeAt, stringToDate, toString, formatNumber en toHexString. Bovendien accepteert de functie toDateTimeOnly nu tekenreekstypen, datumvelden, lange en int-veldtypen. [Meer informatie](../personalization/functions/functions.md)
