---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Opmerkingen bij de vervroegde release van Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '1999'
ht-degree: 2%

---

# Vroege aanvullende informatie {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle veranderingen worden geconsolideerd aan het eind van elke maand in de [ versienota&#39;s ](release-notes.md).

**de vroege versienota&#39;s hieronder zijn onderhevig aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in de [ versienota&#39;s ](release-notes.md), bij de versiedatum.

## Opmerkingen bij de vervroegde release van oktober 2024 {#e-2024}

**de datum van de Versie**: 29-30 van oktober, 2024

### Nieuwe mogelijkheden {#e-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden beschreven.

<table>
<thead>
<tr>
<th><strong>E-mailinhoud vergrendelen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Journey Optimizer kunt u nu inhoud in e-mailsjablonen vergrendelen door de volledige sjabloon of specifieke structuren en onderdelen te vergrendelen. Hierdoor kunt u onbedoelde bewerkingen of verwijderingen voorkomen, waardoor u meer controle hebt over de aanpassing van de sjabloon en de efficiëntie en betrouwbaarheid van uw e-mailcampagnes verbetert.</p>
<!--p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Goedkeuringen tijdens reizen en campagnes (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met het goedkeuringsbeleid kunt u nu een goedkeuringsproces in Journey Optimizer instellen dat marketingteams in staat stelt ervoor te zorgen dat campagnes en reizen worden gecontroleerd en ondertekend door de relevante belanghebbenden voordat ze live gaan.</p>
<p>Eerder beschikbaar voor een reeks organisaties (LA), is het goedkeuringsbeleid nu beschikbaar aan alle gebruikers (GA).</p>
<p>Raadpleeg de <a href="../test-approve/gs-approval.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Aanpassing e-mailconfiguratie (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt dynamische subdomeinen en gepersonaliseerde kopbalparameters nu bepalen wanneer het creëren van configuraties van het e-mailkanaal, voor verhoogde flexibiliteit en controle over uw e-mailmontages.</p><p>Door een gepersonaliseerde configuratie in een campagne of een rit te gebruiken, kunt u een voorvertoning van uw e-mailinhoud weergeven om te controleren op mogelijke fouten met de dynamische instellingen die u hebt gedefinieerd.</p>
<p>Eerder beschikbaar voor een reeks organisaties (LA), is de aanpassing van de e-mailconfiguratie nu beschikbaar aan alle gebruikers (GA).</p>
<p>Raadpleeg de <a href="../email/surface-personalization.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Uw inhoud testen met behulp van voorbeeldinvoergegevens (Bèta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Reis Optimizer kunt u nu verschillende varianten van uw e-mailinhoud testen door hiervan een voorvertoning weer te geven en proefdrukken te verzenden met behulp van voorbeeldinvoergegevens die zijn geüpload uit een CSV-bestand of handmatig zijn toegevoegd. Alle profielkenmerken die in je content worden gebruikt voor personalisatie worden automatisch gedetecteerd door het systeem en kunnen worden gebruikt voor je testen om meerdere varianten te maken.</p>
<p>Deze mogelijkheid is momenteel beschikbaar als bètaversie.</p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Conflict- en prioriteitsbeheer (beperkte beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer is het beheren van het volume en de timing van campagnes en trajecten essentieel om te voorkomen dat klanten met te veel interacties worden overspoeld. Journey Optimizer biedt nu verschillende tools voor conflictbeheer en prioritering.</p><p><ul><li><b> de frequentielimiteren van de Reis </b>: U kunt regelreeksen nu tot stand brengen om op uw reizen van toepassing te zijn, toestaand u om het aantal reizen voor een profiel per dag, week, of maand te beperken, evenals het aantal gelijktijdige lopende reizen te controleren.</li>
<li><b> Prioriteitsscore </b>: U kunt een prioritaire score aan een campagne of een reis nu toewijzen, die zich van 0 tot 100 uitstrekken. Een hoger getal geeft een hogere prioriteit aan. Als twee campagnes of trajecten dezelfde kanaalconfiguratie gebruiken, selecteert Journey Optimizer de catalogus met de hoogste prioriteit. Als de campagnes dezelfde score hebben, wordt de campagne gekozen die het laatst is gewijzigd.</li>
<li><b></b></li>
<li><b></b> You can create a rule to suppress entry into a lower priority journey when a customer qualifies for an upcoming journey of higher priority.</li></ul></p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>Conflict and priority management capabilities are available in Limited Availability to a select group of customers. Please note that these features will be gradually rolled out to more users in the future. Reach out to your account team if interested in being added to the waitlist for these features.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Niet-visuele bewerkingsmodus voor webontwerper</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als alternatief voor de Journey Optimizer-webontwerper kunt u nu wijzigingen aan uw website toevoegen met een niet-visuele editor. Hiermee kunt u uw wijzigingen handmatig invoeren zonder dat u de pagina's hoeft te openen in de visuele editor.
Deze niet-visuele bewerkingsmodus is handig als u geen browserextensies zoals de Adobe Experience Cloud Visual Helper kunt installeren, die nodig is om uw pagina's in de webontwerper te laden.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Inhoud experimenteren in trajecten (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer is al beschikbaar in campagnes en ondersteunt nu experimenten in trajecten. Experimenten zijn gerandomiseerde onderzoeken, wat in de context van online testen betekent dat u sommige willekeurig geselecteerde gebruikers blootstelt aan een bepaalde variatie van een bericht, en een andere willekeurig geselecteerde groep gebruikers aan een andere variatie of behandeling. Na de belichting kun je de resultaten meten waarin je geïnteresseerd bent, zoals het openen van e-mails, abonnementen of aankopen.</p>
<p>Previously available for a set of organizations (LA), experiments in journeys are now available to all users (GA).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Beslissing (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Beslissingen, voorheen beschikbaar voor een reeks organisaties (LA) en bekend onder de naam Experience Decisioning, zijn nu beschikbaar voor alle gebruikers (GA). Het vereenvoudigt personalisatie door een gecentraliseerde catalogus van marketingaanbiedingen aan te bieden die bekend staan als 'beslissingsitems' en een geavanceerde beslissingsengine. Deze motor hanteert regels en rangschikkingscriteria om de meest relevante beslissingsposten te selecteren en aan elke persoon voor te stellen. Deze beslissingsitems worden naadloos geïntegreerd in een breed scala aan binnenkomende oppervlakken via het op code gebaseerde ervaringskanaal.</p>

<p>Voorlopig is het niet mogelijk om een beslissing te nemen voor klanten die de Adobe-add-on voor het gezondheidsschild en privacy- en beveiligingsschild hebben aangeschaft.</p>

<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Regelsets (beperkte beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to your messages or journeys through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p><p>It also allows you to limit the number of journeys per day, week, or month, as well as control the number of concurrent journeys running simultaneously.</p>
<p>Rule sets are available in Limited Availability to a select group of customers. Please note that these features will be gradually rolled out to more users in the future. Reach out to your account team if interested in being added to the waitlist for this feature.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns (General availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Je kunt nu moeiteloos content creëren in meerdere talen binnen één campagne of traject. Met deze functie kun je schakelen tussen talen tijdens het bewerken van je campagne of je traject, het hele bewerkingsproces stroomlijnen en je vermogen verbeteren om meertalige content efficiënt te beheren.</p>
<p>Dankzij de algemene beschikbaarheid is meertalige content nu toegankelijk voor alle kanalen. </p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integratie met Movable Ink en Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Je kunt nu Movable Ink Da Vinci en Adobe Journey Optimizer integreren. Met deze nieuwe integratie kunt u: </p>
<p><ul><li>Profiteer van krachtige mogelijkheden in het Da Vinci-product van Movable Ink om e-mailvariaties voor batchcampagnes samen te stellen en te personaliseren</li>
<li>Snellere workflows voor Journey Optimizer-klanten met Da Vinci voor authoring en AJO voor optimalisatie en aanlevering</li>
<li>Optimaliseer Da Vinci-modellen met Adobe data.</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Bijgewerkte rapportage-ervaring (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Beschikbaar vanaf 16 okt. 2024</p>
<p>De Journey Optimizer-rapportage is nu algemeen beschikbaar (GA) en wordt geleverd met een verbeterde interoperabiliteit met de mogelijkheden van de Customer Journey Analytics, standaardisering van de rapportage op beide platforms en verbetering van de consistentie en betrouwbaarheid van de gegevens. Deze naadloze integratie tussen Journey Optimizer en Customer Journey Analytics biedt een duidelijker beeld van prestatiemetrieken, waardoor gebruikers beter geïnformeerde beslissingen kunnen nemen.</p>
<p>Met algemene beschikbaarheid worden vier nieuwe functies geïntroduceerd: de mogelijkheid om eenvoudige metrics te maken, doelgroepen te maken en te publiceren, ad-hocvragen te stellen met Insight Builder en rapporten te plannen die automatisch naar belangrijke ontvangers worden gemaild.</p>
<p>Raadpleeg de <a href="../reports/report-cja-manage.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Belangrijk:De huidige ervaring met rapportage wordt met ingang van januari 2025 buiten gebruik gesteld. Na deze datum wordt de nieuwe rapportervaring de standaard. We raden u aan vertrouwd te raken met de nieuwe functies en functies om een soepele overgang te waarborgen. <a href="../reports/report-gs-cja.md"> Leer hoe te om met Journey Optimizer te worden begonnen nieuwe Rapporterende interface </a></p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ervaringen op basis van code bij reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Beschikbaar sinds 1 okt. 2024</p>
<p>Met het op code-gebaseerde ervaringskanaal, staat Adobe Journey Optimizer u toe om geavanceerde verpersoonlijking en het testen voor om het even welk van uw binnenkomende eigenschappen te doen, toelatend naadloze levering van op maat gemaakte ervaringen over diverse aanraakpunten zoals Web apps, mobiele apps, Desktop apps, videoconsoles, TV aangesloten apparaten, slimme TVs, kiosks, ATMs, IoT apparaten, en meer. Het op code-gebaseerde ervaringskanaal is nu beschikbaar in het reiscanvas.</p>
<p>Raadpleeg de <a href="../code-based/create-code-based.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Webervaringen tijdens reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Beschikbaar sinds 1 okt. 2024</p>
<p>Met het kanaal van het Web, staat Adobe Journey Optimizer u toe om de Webervaring te personaliseren u aan uw klanten door binnenkomende Webreizen levert. Het webkanaal is nu beschikbaar op het reiscanvas.</p>
<p>Raadpleeg de <a href="../web/create-web.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### Verbeteringen {#e-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Sms-kanaal**

>[!AVAILABILITY]
>
>De volgende verbeteringen zijn alleen beschikbaar bij Sinch- en Infobip-providers.

Sms-verbeteringen zijn geïntroduceerd om je berichtvoorzieningen te verbeteren:

* Je kunt unieke trefwoorden definiëren en beheren voor je SMS-campagnes en -trajecten, waardoor je gepersonaliseerdere en efficiëntere communicatie kunt realiseren.

* U kunt een standaard SMS-bericht maken en leveren wanneer een trefwoord niet wordt herkend.

* U kunt nu een SMS API-kanaalconfiguratie bewerken of verwijderen.

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!—* **Max. aantal Levende transporten** - Journey Optimizer heeft nu een grip van 500 levende reizen op productiemandboxen, in plaats van 100. Het aantal live trajecten is zichtbaar in het canvas van het traject. <!-- DOCAC-10977-->

**Datasets**

* **tijd-aan-levende guardrail** - Beginnend November 1, 2024, zal een tijd-aan-levende (TTL) guardrail aan systeem-geproduceerde datasets van Journey Optimizer in nieuwe zandbakken en nieuwe organen als volgt worden uitgerold:

   * 90 dagen voor gegevens in de profielenopslag
   * 13 months for data in the data lake

  This change will be rolled out to existing customer sandboxes subsequently in a second phase.

  Additionally, starting November 1st, streaming segmentation will no longer support the use of send and open events from tracking and feedback datasets. This change will apply to all customer sandboxes and orgs at that time. [Meer informatie](../data/datasets-ttl.md)

* **** [Meer informatie](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Meldend**

* **Beslissing die** meldt is nu beschikbaar, die essentiële inzichten aanbieden in hoe uw bezoekers met uw ervaringen interactie aangaan.

**het bestuur van Gegevens &amp; toestemmingsbeleid** - de datum van de Beschikbaarheid: 7 okt, 2024

* **handhaving van het beleid van het beheer van gegevens** vindt nu over alle kanalen in Journey Optimizer plaats. Voor klanten die beleid in Adobe Experience Platform hebben gemaakt, worden deze toegepast op marketingacties als onderdeel van de kanaalconfiguratie-instellingen. Als je content maakt met een configuratie, controleert het systeem alle personalisatievelden op eventuele schendingen van data-governance. Als er een schending wordt gevonden, is het niet mogelijk een traject of campagne te publiceren. [Meer informatie](../action/action-privacy.md)

* **het toestemmingsbeleid van de Douane** is nu op alle kanalen van Journey Optimizer van toepassing. Bij handhaving voordat een bericht wordt verzonden of een binnenkomende ervaring wordt geleverd, controleert het systeem of de gebruiker toestemming heeft gegeven om personalisatievelden te gebruiken in de inhoud die ze zullen ontvangen. Als er geen toestemming wordt gegeven, wordt de ervaring niet weergegeven. [Meer informatie](../action/consent.md)

  >[!NOTE]
  >
  >Het toestemmingsbeleid is momenteel slechts beschikbaar voor organisaties die het 3} toe:voegen-op dienstenaanbod van het Schild van de Adobe **of van de Privacy en van de Veiligheid 2} hebben gekocht**.****

**Doelgroepen** - de datum van de Beschikbaarheid: 8 okt, 2024

* Bij het targeten van een CSV-bestandspubliek, kun je nu kenmerken uit het bestand gebruiken in de personalisatie-editor en in trajecten en campagneregelbuilder. [Meer informatie](../audience/about-audiences.md)

* The use of audiences and attributes from custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.

****

* Content templates are now available. You can speed up authoring your code-based experiences starting from a content template built by your developers. Using a content template will allow the marketer to just modify some values or fields, instead of composing the whole HTML or JSON content payload.

****

[ Adobe Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) de gebruikers kunnen douanemodellen nu kiezen om op te optimaliseren wanneer vestiging een model van AI in Beslissing (vroeger genoemd geworden Beslissing van de Ervaring). Zo kunt u bijvoorbeeld een aangepaste tabel voor aankopen optimaliseren in plaats van gedefinieerde beperkingen zoals click-through rate.&quot;
