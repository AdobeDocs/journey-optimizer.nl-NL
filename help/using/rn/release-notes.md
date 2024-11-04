---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 018ff365780c5064afd94c8f842ca0498fe06065
workflow-type: tm+mt
source-wordcount: '1960'
ht-degree: 6%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** levert onophoudelijk nieuwe eigenschappen, verhogingen aan bestaande eigenschappen, en insectenmoeilijke situaties. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen. [!DNL Adobe Journey Optimizer] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html) {target="_blank"}.

## Release oktober 1924 {#24-10-rn}

**de datum van de Versie**: Oktober 29-30, 2024

### Nieuwe functies {#24-10-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden beschreven:

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
<p>Raadpleeg de <a href="../content-management/content-locking.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
<p>Beschikbaar sinds 24 okt. 2024</p>
</td>
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
<p>Met het op code-gebaseerde ervaringskanaal, staat Adobe Journey Optimizer u toe om geavanceerde verpersoonlijking en het testen voor om het even welk van uw binnenkomende eigenschappen te doen, toelatend naadloze levering van op maat gemaakte ervaringen over diverse aanraakpunten zoals Web apps, mobiele apps, Desktop apps, videoconsoles, TV aangesloten apparaten, slimme TVs, kiosks, ATMs, IoT apparaten, en meer. Het op code-gebaseerde ervaringskanaal is nu beschikbaar in het reiscanvas.</p>
<p>Raadpleeg de <a href="../code-based/create-code-based.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>Beschikbaar sinds 1 okt. 2024</p>
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
<p>Met het kanaal van het Web, staat Adobe Journey Optimizer u toe om de Webervaring te personaliseren u aan uw klanten door binnenkomende Webreizen levert. Het webkanaal is nu beschikbaar op het reiscanvas.</p>
<p>Raadpleeg de <a href="../web/create-web.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>Beschikbaar sinds 1 okt. 2024</p>
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
<p>In Journey Optimizer is het beheren van het volume en de timing van campagnes en reizen van essentieel belang om te voorkomen dat klanten met te veel interacties worden overspoeld. Journey Optimizer biedt nu verschillende tools voor conflictbeheer en prioritering. <p>Raadpleeg de <a href="../conflict-prioritization/gs-conflict-prioritization.md">gedetailleerde documentatie</a> voor meer informatie.</p></p><p><ul><li><b> frequentie het in kaart brengen van de Reis </b>: U kunt regelreeksen nu tot stand brengen om op uw reizen van toepassing te zijn, toestaand u om het aantal reizen voor een profiel per dag, week, of maand te beperken, evenals het aantal gezamenlijke reizen die gelijktijdig lopen te controleren.</li>
<li><b> Prioriteitsscore </b>: U kunt een prioritaire score aan een campagne of een reis nu toewijzen, die zich van 0 tot 100 uitstrekken. Een hoger getal geeft een hogere prioriteit aan. Wanneer twee campagnes of reisacties de zelfde kanaalconfiguratie gebruiken, zal Journey Optimizer één met de hoogste prioritaire score selecteren. Als de campagnes dezelfde score hebben, wordt de campagne gekozen die het minst recent is gewijzigd.</li>
<li><b> de potentiële conflicten van de Mening </b>: Een nieuwe "potentiële conflicten van de Mening"knoop in reizen en campagnes staat u nu toe om overlapping met andere reizen of campagnes zoals de begindatum, het gerichte publiek, of de geselecteerde kanaalconfiguratie te identificeren.</li>
<li><b> Arbitrage van de Reis </b>: Dit nieuwe vermogen laat u toe om aan de belangrijkste reizen voor uw klanten voorrang te geven. U kunt een regel tot stand brengen om ingang in een lagere prioritaire reis te onderdrukken wanneer een klant voor een aanstaande reis van hogere prioriteit kwalificeert.</li>
<li><b> het in kaart brengen van de Frequentie door communicatie type: </b> met regelreeksen, kunt u korrelige regels door communicatietype (b.v., Verkoop, Bevordering) nu plaatsen om het overbelasten van klanten met gelijkaardige berichten te verhinderen. U kunt de frequentie in meerdere kanalen bepalen, waarbij al te gevraagde profielen automatisch worden uitgesloten voor een betere ervaring met klanten.</li></ul>

<img src="assets/do-not-localize/gif-conflict.gif">

<p>Conflict- en prioriteitsbeheermogelijkheden zijn beschikbaar in Beperkte beschikbaarheid voor een geselecteerde groep klanten. Houd er rekening mee dat deze functies in de toekomst geleidelijk aan voor meer gebruikers beschikbaar zullen zijn. Neem contact op met uw accountteam als u interesse hebt in het toevoegen van deze functies aan de wachtlijst.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Integratie van Movable Ink en Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu Movable Ink Da Vinci en Adobe Journey Optimizer integreren. Met deze nieuwe integratie kunt u: </p>
<p><ul><li>Gebruik krachtige mogelijkheden in het Da Vinci-product van Movable Ink om e-mailvariaties voor batchcampagnes samen te stellen en aan te passen</li>
<li>Snellere workflows voor praktijkgebruikers voor Journey Optimizer-klanten die Da Vinci gebruiken voor ontwerpen en Adobe Journey Optimizer voor optimalisatie en levering</li>
<li>Optimaliseer Da Vinci modellen met Adobe gegevens.</li></ul></p>
<p>Voor meer informatie, verwijs naar de <a href="https://movableink.com/adobe-and-movable-ink"> Movable documentatie van Da Vinci van de Inkt </a>.</p>
</tr>
</tbody>
</table>

Eerder beschikbaar voor een reeks organisaties (LA), zijn de volgende mogelijkheden nu beschikbaar aan alle gebruikers (GA):

<table>
<thead>
<tr>
<th><strong>Aanpassing e-mailconfiguratie (algemene beschikbaarheid) </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Voor meer flexibiliteit en meer controle over de e-mailinstellingen kunt u dynamische subdomeinen en gepersonaliseerde headerparameters definiëren wanneer u configuraties met e-mailkanalen maakt.
</p>
<p>Raadpleeg de <a href="../email/surface-personalization.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>Beschikbaar sinds 23 oktober 2024</p>
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
<p>Raadpleeg de <a href="../test-approve/gs-approval.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/approval.gif"/>
<p>Beschikbaar sinds 22 okt. 2024</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Inhoud experimenteren op reizen (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer is al beschikbaar in campagnes en ondersteunt nu experimenten op reizen. Experimenten zijn gerandomiseerde onderzoeken, die in de context van online tests betekenen dat u sommige willekeurig geselecteerde gebruikers aan een bepaalde variatie van een bericht blootstelt, en een andere willekeurig geselecteerde reeks gebruikers aan één of andere andere variatie of behandeling. Na blootstelling, kunt u de resultaatmetriek meten u in geinteresseerd bent, zoals opent van e-mail, abonnementen, of aankopen.</p>
<p>Raadpleeg de <a href="../content-management/content-experiment.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Decisioning (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning, previously available for a set of organizations (LA) and known as Experience Decisioning, is now available to all users (GA), including organizations that have purchased the Adobe Healthcare Shield or Privacy and Security Shield add-on offerings.</p><p>Decisioning simplifies personalization by offering a centralized catalog of marketing offers known as 'decision items' and a sophisticated decision engine. This engine leverages rules and ranking criteria to select and present the most relevant decision items to each individual. These decision items are seamlessly integrated into a wide range of inbound surfaces through the code-based experience channel.</p>
<p>For more information, refer to the <a href="../experience-decisioning/gs-experience-decisioning.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Meertalige berichten tijdens reizen en campagnes (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu moeiteloos inhoud in meerdere talen maken in één campagne of reis. Met deze functie kunt u schakelen tussen talen wanneer u uw campagne of reis bewerkt, het hele bewerkingsproces stroomlijnt en uw mogelijkheden voor efficiënt beheer van meertalige inhoud verbetert.</p>
<p>Raadpleeg de <a href="../content-management/multilingual-gs.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/multilingual.gif">
</td>
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
<p>De Journey Optimizer-rapportage is nu algemeen beschikbaar (GA) en wordt geleverd met een verbeterde interoperabiliteit met de mogelijkheden van de Customer Journey Analytics, standaardisering van de rapportage op beide platforms en verbetering van de consistentie en betrouwbaarheid van de gegevens. Deze naadloze integratie tussen Journey Optimizer en Customer Journey Analytics biedt een duidelijker beeld van prestatiesmetriek, toelatend gebruikers om geïnformeerde besluiten te nemen.</p>
<p>Met Algemene Beschikbaarheid, worden vier nieuwe eigenschappen geïntroduceerd: de capaciteit om eenvoudige metriek tot stand te brengen, te creëren en publiek te publiceren, ad-hocvragen te stellen gebruikend de Bouwer van het Inzicht, en planningsrapporten om automatisch aan zeer belangrijke ontvangers worden gemaild.</p>
<p>Raadpleeg de <a href="../reports/report-cja-manage.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Belangrijk: de huidige ervaring met rapportage wordt met ingang van januari 2025 opgeheven. Na deze datum wordt de nieuwe ervaring met rapportage de norm. We raden u aan bekend te maken met de nieuwe functies en functies om een soepele overgang te garanderen. <a href="../reports/report-gs-cja.md"> Leer hoe te om met Journey Optimizer te worden begonnen de nieuwe Rapporterende interface </a></p>
<p>Beschikbaar vanaf 16 oktober 2024</p>
</tr>
</tbody>
</table>

<!--The following capabilities are available to all customers in public beta:-->

<table>
<thead>
<tr>
<th><strong>Inhoud testen met behulp van voorbeeldinvoergegevens (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Reisoptimalisator kunt u nu verschillende varianten van uw inhoud testen door deze voor te vertonen en e-mailproefdrukken te verzenden met voorbeeldinvoergegevens die zijn geüpload uit een bestand of handmatig zijn toegevoegd. Alle profielkenmerken die in de inhoud worden gebruikt voor personalisatie worden automatisch gedetecteerd door het systeem en kunnen worden gebruikt voor uw tests om meerdere varianten te maken.</p>
<p>Deze mogelijkheid is momenteel beschikbaar voor alle klanten als een openbare bètaversie, voor de communicatiekanalen E-mail, SMS en Push.</p>
<p>Raadpleeg de <a href="../test-approve/simulate-sample-input.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/gif-simulate.gif">
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from Adobe Experience Platform in the personalization editor to personalize your content. To do this, datasets needed for lookup personalization must first be enabled through an API call. Once done, you can use their data to personalize your content into [!DNL Journey Optimizer].</p>
<p>This capability is currently available to all customers as a public beta.</p>
<p>For more information, refer to the <a href="../personalization/lookup-aep-data.md"</a>.</p>
</td>
</tr>
</tbody>
</table>-->

### Verbeteringen {#24-10-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Sms-kanaal**

* U kunt nu een SMS API-kanaalconfiguratie bewerken of verwijderen. [Meer informatie](../sms/sms-configuration.md)

* De volgende verhogingen zijn geïntroduceerd om uw het overseinenmogelijkheden van SMS met Infobip en Sinch te verbeteren:

   * U kunt unieke trefwoorden voor uw SMS-campagnes en -reizen definiëren en beheren, zodat u meer gepersonaliseerde en efficiënte communicatie mogelijk maakt.

   * U kunt een standaard SMS-bericht maken en leveren wanneer een trefwoord niet wordt herkend.

  Leer meer over deze verbeteringen in de de configuratiedocumentatie van SMS voor [ Infobip ](../sms/sms-configuration-infobip.md) en [ Sinch ](../sms/sms-configuration-sinch.md).


<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!—* **Max. aantal Levende reizen** - Journey Optimizer heeft nu een grip van 500 levende reizen op productiestanddozen, in plaats van 100. Het aantal rechtstreekse reizen is zichtbaar in het canvas van de reis. <!-- DOCAC-10977-->

**het kanaal van het Web**

* **niet-visuele het uitgeven wijze voor de Webontwerper** - als alternatief voor de het Webontwerper van Journey Optimizer, kunt u wijzigingen aan uw website nu toevoegen gebruikend een niet-visuele redacteur. U kunt de wijzigingen handmatig invoeren zonder de pagina&#39;s in de visuele editor te openen. Deze niet-visuele bewerkingsmodus is handig als u geen browserextensies kunt installeren, zoals de Adobe Experience Cloud Visual Helper, die nodig is om uw pagina&#39;s in de webontwerper te laden. [Meer informatie](../web/web-non-visual-editor.md)


**Datasets**

* **verzend en open gebeurtenissen** - Beginnend 1 November, 2024, zal het stromen segmentatie niet meer het gebruik van verzenden en open gebeurtenissen van Journey Optimizer het volgen en terugkoppelen datasets steunen. Deze wijziging is van toepassing op alle sandboxen en organisaties van klanten. [Meer informatie](../data/datasets-ttl.md#segmentation-update)

* **Tijd-aan-levende Dataset (TTL)** - Beginnend in Februari 2025, zal een tijd-aan-levende (TTL) guardrail aan systeem-geproduceerde datasets van Journey Optimizer in nieuwe zandbakken en nieuwe organismen als volgt worden uitgerold:

   * 90 dagen voor gegevens in de profielopslag
   * 13 maanden voor gegevens in het data Lake

  Deze wijziging wordt in een volgende fase doorgevoerd in bestaande sandboxen voor klanten. [Meer informatie](../data/datasets-ttl.md#ttl)

* **Parameters in douaneacties** - de datum van de Beschikbaarheid: 3 okt, 2024 - ONGELDIGE en facultatieve parameters worden nu gesteund in douaneacties. [Meer informatie](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Meldend**

* **Beslissing die** meldt is nu beschikbaar, die essentiële inzichten aanbieden in hoe uw bezoekers met uw ervaringen in wisselwerking staan. [Meer informatie](../reports/campaign-global-report-cja-code.md#decisioning-kpis)

**het bestuur van Gegevens &amp; het beleid van de Toestemming** - de datum van Beschikbaarheid: 7 okt, 2024

* **de handhaving van het beleid van het beheer van 0} Gegevens {vindt nu over alle kanalen in Journey Optimizer plaats.** Voor klanten die beleid in Adobe Experience Platform hebben gecreeerd, worden deze toegepast op marketing acties als deel van de opstelling van kanaalconfiguraties. Als u inhoud maakt met een configuratie, controleert het systeem alle personalisatievelden op overtredingen van het gegevensbeheer. Als er een overtreding wordt gevonden, is het niet mogelijk een reis of campagne te publiceren. [Meer informatie](../action/action-privacy.md)

* **het toestemmingsbeleid van de Douane** is nu op alle kanalen van Journey Optimizer van toepassing. Bij handhaving voordat een bericht wordt verzonden of een binnenkomende ervaring wordt opgeleverd, controleert het systeem of de gebruiker toestemming heeft gegeven om verpersoonlijkingsvelden te gebruiken in de inhoud die hij of zij zal ontvangen. Als er geen toestemming wordt gegeven, wordt de ervaring niet weergegeven. [Meer informatie](../action/consent.md)

  >[!NOTE]
  >
  >Het toestemmingsbeleid is momenteel slechts beschikbaar voor organisaties die het Adobe **het Schild van de Gezondheidszorg** of **Privacy en het 3} toe:voegen-op dienstenaanbod van het Schild van de Veiligheid hebben gekocht.**

**Soorten publiek** - Beschikbaarheidsdatum: 8 okt, 2024

* Wanneer het richten van een Csv- dossierpubliek, kunt u attributen van het dossier in de verpersoonlijkingsredacteur en in reizen en campagneregelbouwer nu gebruiken. [Meer informatie](../audience/about-audiences.md)

* Het gebruik van soorten publiek en kenmerken van aangepaste upload (CSV-bestand) is nu beschikbaar voor gebruik met het Healthcare Shield of Privacy and Security Shield.

**Configuratie** - de datum van de Beschikbaarheid: 23 okt, 2024

* Wanneer u een gepersonaliseerde configuratie gebruikt in een campagne of een rit, kunt u nu een voorbeeld van uw e-mailinhoud bekijken om te controleren op mogelijke fouten met de dynamische instellingen die u hebt gedefinieerd. [Meer informatie](../email/surface-personalization.md#check-configuration)

**op code-Gebaseerd kanaal**

* Inhoudssjablonen zijn nu beschikbaar. U kunt het ontwerpen versnellen van uw op code-gebaseerde ervaringen die van een inhoudsmalplaatje beginnen door uw ontwikkelaars wordt gebouwd. Als u een inhoudssjabloon gebruikt, kan de markeerteken alleen enkele waarden of velden wijzigen in plaats van de gehele HTML- of JSON-inhoudslading samen te stellen. [Meer informatie](../content-management/content-templates.md)

**Beslissing**

* [ Adobe Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) de gebruikers kunnen douanemodellen nu kiezen om te optimaliseren wanneer vestiging een AI model in Beslissing (vroeger genoemd geworden Ervaring die Beslissing) wordt bekend. Zo kunt u bijvoorbeeld een aangepaste tabel &quot;aankopen&quot; optimaliseren in plaats van gedefinieerde beperkingen, zoals een doorklikfrequentie. [Meer informatie](../experience-decisioning/ranking.md)

* Wanneer het toevoegen van een besluitvormingsbeleid aan een code-gebaseerde campagne met Beslissing, kunt u één enkele besluitvormingspunten, naast selectiestrategieën nu manueel selecteren. Bovendien kunt u nu meerdere fallback-voorstellen selecteren. Dit garandeert dat er een aantal teruggestuurde besluiten zijn. [Meer informatie](../experience-decisioning/create-decision.md)
