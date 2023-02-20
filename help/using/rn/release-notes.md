---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Aanvullende informatie voor Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d160baac2eb454cfd10097e29147562f83c1cd50
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 5%

---

# Aanvullende informatie {#release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen.

Opmerkingen bij vorige release zijn beschikbaar in [deze pagina](release-notes-2022.md). U kunt ook de [meest recente documentatie-updates](documentation-updates.md) pagina voor meer wijzigingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} vandaag, en ontvang de recentste productupdates, opwindende verhalen, gebruiksgevallen, uiteinden en meer die direct aan uw Postbus worden geleverd elk kwartaal.


## Opmerkingen bij de release Vroege februari 2023 {#feb-2023}

Deze rubriek bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd. Gedetailleerde documentatie is beschikbaar op de releasedatum.

Beschikbaarheid: **22 februari 2023**

### Verbeteringen {#feb-2023-improvements}

**Journeys**

* De **Wachttijd bij terugkeer** het veld is toegevoegd aan de eigenschappen van de reis . In dit veld kunt u de tijd definiëren die u moet wachten voordat een profiel de reis weer in één keer kan betreden (te beginnen met een gebeurtenis of een segmentkwalificatie). Hierdoor wordt voorkomen dat ritten meerdere keren ten onrechte worden geactiveerd voor dezelfde gebeurtenis. Het veld wordt standaard ingesteld op 5 minuten.

* Er zijn verbeteringen aangebracht voor **begin- en einddatum van de reis**. Als u geen begindatum hebt opgegeven, wordt deze nu automatisch toegevoegd op het moment van publicatie. Voor **Segment lezen** voor reizen kunt u nu een einddatum toevoegen. Hiermee kunnen profielen automatisch worden afgesloten wanneer de datum wordt bereikt.

* Het canvas Journey is verbeterd voor een eenvoudigere en verbeterde gebruikerservaring. Aan het einde van elk pad op het canvas zijn de lege plaatsaanduidingen verwijderd. U kunt nu gewoon uw activiteiten toevoegen door deze naar een willekeurige locatie tussen knooppunten te slepen.

* Tijdslimiet en foutenbeheer zijn verbeterd op het gebied van reizen. Time-out- en foutpaden worden nu altijd toegevoegd op het canvas. Er is een nieuwe werkbalkknop beschikbaar om deze paden weer te geven/te verbergen.

* Er is een nieuw type systeemwaarschuwing ingevoerd. U kunt nu een melding krijgen wanneer een aangepaste handeling mislukt.


**Beheer**

* **Lijst van gewenste personen** - U kunt de lijst van gewenste personen nu downloaden als een CSV-bestand.

* **E-mailoppervlak** - Er is een extra controle toegevoegd aan de instellingen voor het e-mailoppervlak: als de MX-record voor het subdomein dat wordt gebruikt in het dialoogvenster **Reageren op (e-mailadres)** of in de **BCC-e-mailadres** is niet behoorlijk gevormd, kan de e-mailoppervlakte niet meer worden gecreeerd. U moet het gevormd hebben of een andere gebruiken.

* **E-mailoppervlak** - In het gedeelte URL-volgparameters van de instellingen van het e-mailoppervlak, de limiet voor elke **Waarde** Het veld is bijgewerkt van 255 tekens naar 5 kB ten behoeve van compatibiliteit met Adobe Analytics-tracking.

**Beslissingsbeheer**

* **Plaatsen** - Er zijn aanvullende parameters toegevoegd aan het scherm voor het maken van plaatsingen. Hiermee kunt u bepalen of een aanbieding op meerdere plaatsen kan worden gedupliceerd en kunt u opgeven of de inhoud en metagegevens van de aanbieding moeten worden opgenomen in de API-reactie.

* **URL-personalisatie** - Wanneer u URL&#39;s als inhoud toevoegt aan de representaties van uw aanbiedingen, kunt u deze URL&#39;s nu aanpassen met de Expressieeditor.



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

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

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

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**Personalisatie**

* Er zijn nieuwe hulpfuncties beschikbaar: formatCurrency, charCodeAt, stringToDate, toString, formatNumber en toHexString. Bovendien accepteert de functie toDateTimeOnly nu tekenreekstypen, datumvelden, lange en int-veldtypen. [Meer informatie](../personalization/functions/functions.md)
