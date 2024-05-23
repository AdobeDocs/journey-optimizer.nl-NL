---
solution: Journey Optimizer
product: journey optimizer
title: Opmerkingen bij de release 2022
description: Opmerkingen bij de release van Journey Optimizer 2022
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hidefromtoc: true
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: e34c39c02f71361277f28b1a116a54390875f93d
workflow-type: tm+mt
source-wordcount: '3598'
ht-degree: 7%

---

# Opmerkingen bij de release 2022 {#release-notes-2022}

Deze pagina bevat alle functies en verbeteringen voor [!DNL Journey Optimizer] vrijgegeven in 2022.



## Release oktober 2022 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### Verbeteringen {#oct-2022-improvements}

**Reizen**

* De **Herkomst forceren bij herhaling** Deze optie is toegevoegd aan parameters voor terugkerende publieksprogramma&#39;s. Met deze optie kunt u alle profielen die zich nog in de reis bevinden, automatisch laten afsluiten bij de volgende uitvoering. Wanneer de optie is gedeactiveerd, moeten profielen de reis beëindigen alvorens zij in een ander voorkomen kunnen opnieuw ingaan. [Meer informatie](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**Administratie**

* Er is een bericht toegevoegd aan de gebruikersinterface om te waarschuwen dat subdomein, landende paginasubdomain, PTR-record en IP-poolconfiguraties algemeen gelden voor alle sandboxen en dat elke wijziging aan een van deze configuraties dus ook van invloed is op de productiesandboxen.
* De stappen voor het uploaden van de suppressielijst als een CSV-bestand vanuit de gebruikersinterface zijn gewijzigd. [Meer informatie](../configuration/manage-suppression-list.md#download-suppression-list)

**Campagnes**

* U kunt voltooide en gestopt campagnes nu archiveren. [Meer informatie](../campaigns/modify-stop-campaign.md#archive)


## Release september 2022{#sept-2022-release}

### Nieuwe functies{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>Dynamische inhoud en nieuwe voorwaardelijke regelbuilder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu dynamische inhoud maken om de inhoud van uw berichten aan te passen op basis van voorwaardelijke regels.</p> 
<p>Voorwaardelijke regels worden gecreeerd gebruikend een visuele regelbouwer binnen de Redacteur van de Uitdrukking, waar u hen voor verder hergebruik over uw reizen en campagnes kunt opslaan.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>Raadpleeg de <a href="../personalization/get-started-dynamic-content.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API-gestuurde campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Naast bestaande geplande campagnes kunt u nu API-getriggerde campagnes maken in Journey Optimizer en deze aanroepen vanuit een extern systeem met behulp van API's.</p>
<p>Dit staat u toe om diverse operationele en transactionele overseinenbehoeften zoals wachtwoordterugstellen, het teken van OTP, onder andere te behandelen.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Raadpleeg de <a href="../campaigns/api-triggered-campaigns.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Toegangsbeheer voor gegevens</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Via op kenmerken gebaseerd toegangsbeheer kunnen beheerders de toegang tot specifieke objecten beheren op basis van bepaalde kenmerken. Deze kenmerken kunnen metagegevens zijn die aan een object worden toegevoegd, zoals labels. Met het oog op deze release kunnen beheerders ook gebruikersrollen definiëren die alleen toegang hebben tot specifieke velden en/of objecten, en gegevens die overeenkomen met die velden en/of objecten.</p>
<p> Het gebruik van op attributen-gebaseerde toegangsbeheer is momenteel beperkt tot geselecteerde klanten, en zal aan alle milieu's in een toekomstige versie worden opgesteld.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>Raadpleeg de <a href="../administration/object-based-access.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Beheer en privacy van gegevens</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met zijn beheerskader voor etikettering en handhaving van gegevensgebruik (DULE) kan Journey Optimizer nu het Adobe Experience Platform-beleid voor governance gebruiken om te voorkomen dat gevoelige velden via aangepaste acties naar systemen van derden worden geëxporteerd. Als het systeem een beperkt veld identificeert in de parameters voor aangepaste handelingen, wordt een fout weergegeven waardoor u de reis niet kunt publiceren.</p>
<p>Het gebruik van de Etikettering en de Handhaving van het Gebruik van Gegevens (DULE) is momenteel beperkt tot geselecteerde klanten, en zal aan alle milieu's in een toekomstige versie worden opgesteld.</p>
<p>Raadpleeg de <a href="../action/action-privacy.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Geautomatiseerde toestemmingshandhaving (toestemmingsbeleid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Adobe Experience Platform kunt u eenvoudig marketingbeleid toepassen en afdwingen om de voorkeuren voor toestemming van uw klanten te respecteren. Beleid voor instemming wordt gedefinieerd in Adobe Experience Platform. In Journey Optimizer kunt u dit beleid voor toestemming toepassen op aangepaste handelingen. U kunt bijvoorbeeld regels voor toestemming definiëren om klanten uit te sluiten die niet hebben ingestemd met het ontvangen van e-mail, push- of SMS-berichten.
<p>Automated Consent Enforcement is momenteel alleen beschikbaar voor organisaties die de Add-on-aanbieding Healthcare Shield hebben aangeschaft.</p>
<p>Raadpleeg de <a href="../action/consent.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Machtigingsbeheer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ondersteunt het definiëren van gebruikersrollen en toegangsbeleid voor het beheren van machtigingen voor functies en objecten. Doorheen <strong>Adobe Experience Cloud-machtigingen</strong>, kunt u rollen tot stand brengen en beheren, evenals de gewenste middeltoestemmingen voor deze rollen toewijzen. Met machtigingen kunt u ook de labels, sandboxen en gebruikers beheren die aan een specifieke rol zijn gekoppeld.</p>
<p> Het gebruik van toestemmingen is momenteel beperkt tot geselecteerde klanten, en zal aan alle milieu's in een toekomstige versie worden opgesteld.</p>
<p>Raadpleeg de <a href="../administration/attribute-based-access.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Waarschuwing en bewaking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als Journey Optimizer-gebruiker kunt u nu systeemwaarschuwingen openen via de gebruikersinterface om op de hoogte te worden gebracht wanneer reizen niet naar behoren werken. U kunt de beschikbare waarschuwingen weergeven en hierop een abonnement nemen. In de eerste waarschuwing die bij deze release beschikbaar is, wordt u gewaarschuwd als een activiteit van het leespubliek tijdens de gedefinieerde tijdsperiode geen profiel heeft verwerkt. Er zal meer komen nu deze workflow ontgrendeld is.</p>
<!--p>For more information, refer to the <a href="../reports/alerts.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Verbeteringen{#sept-2022-improvements}

**Reizen**

* De **Entiteitsgegevens** is nu beschikbaar als out-of-the-box dataset in Adobe Journey Optimizer. Deze raadplegingsdataset omvat meta- gegevens om het volgen te verrijken en datasetinformatie terug te koppelen. Dit zal u helpen uw rapporten en vragen met begrijpelijkere gegevens verbeteren. [Meer informatie](../data/datasets-query-examples.md#entity-dataset)
* Er is een nieuwe guardrail toegevoegd aan de unitaire reizen (te beginnen met een evenement of een kwalificatie van het publiek) om te voorkomen dat ritten meerdere keren ten onrechte worden gestart voor hetzelfde evenement. De terugkeer van het profiel wordt nu tijdelijk geblokkeerd door gebrek voor 5 minuten. [Meer informatie](../start/guardrails.md#events-g)

**Administratie**

* Wanneer u de lijst van gewenste personen activeert of deactiveert, wordt nu een nieuwe waarschuwing weergegeven waarin de effecten van elke actie worden beschreven. [Meer informatie](../configuration/allow-list.md#enable-allow-list)
* De gebruikersinterface voor het creëren van kanaaloppervlakten, het creëren van IP pools, het beheren van de suppressielijst en de lijst van gewenste personen, en het vormen van het kanaal van SMS is bijgewerkt.
* Wanneer u nu het eerste kanaaloppervlak voor een bepaald subdomein maakt, duurt de verwerkingstijd 10 minuten tot 10 dagen en slechts 3 uur voor volgende oppervlakken die dat subdomein gebruiken. [Meer informatie](../configuration/channel-surfaces.md#create-channel-surface)
* De gebruikersinterface voor het maken van voorinstellingen voor openingspagina&#39;s en het landen van subdomeinen van de pagina is bijgewerkt. [Meer informatie](../landing-pages/lp-subdomains.md)

**Controles van audits**

* Met Journey Optimizer kunt u acties identificeren die door gebruikers in het systeem worden uitgevoerd op verschillende services en mogelijkheden, zoals campagnes, reizen, berichten, landingspagina&#39;s, enz. De middelen van het logboek van de controle omvatten nu veranderingen op diverse andere acties, en worden automatisch geregistreerd aangezien de activiteit voorkomt. Meer informatie [op deze pagina](../privacy/audit-logs.md).

**Ondersteuning voor archivering**

* De nieuwe **Entiteitsgegevens** omvat een gebied van het Malplaatje dat u toelaat om het formaat en de structuur van de verzonden berichten op alle kanalen voor archiveringsdoel uit te voeren. [Meer informatie](../configuration/archiving-support.md)

**Openingspagina&#39;s**

* U kunt nu contextuele gegevens gebruiken die afkomstig zijn van een andere pagina binnen dezelfde landingspagina. Als u bijvoorbeeld een selectievakje koppelt aan een abonnementenlijst op de primaire landingspagina, kunt u die abonnementenlijst op de subpagina &quot;Bedankt&quot; gebruiken. [Meer informatie](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Overige wijzigingen{#sept-2022-other}

* Modus Reisexplosie is vervangen door Modus Snelle levering campagne. [Meer informatie](../push/create-push.md#rapid-delivery)
* Om de prestaties te verbeteren, kunnen de groepen van het de gebeurtenisgebied van de Ervaring niet meer worden gebruikt in reizen die met een Gelezen publiek, een kwalificatie van het Publiek of een bedrijfsgebeurtenisactiviteit beginnen. Deze wijziging geldt alleen voor nieuwe reizen. De bestaande zullen het huidige gedrag houden. [Meer informatie](../start/guardrails.md#expression-editor)
* De limiet van 1 uur voor geplande leestuchtritten is verwijderd. Deze reizen kunnen nu zonder vertraging worden uitgevoerd.




## Release van augustus 2022 {#aug-2022-release}

### Nieuwe functies

<table>
<thead>
<tr>
<th><strong>Campagnes maken en beheren in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gebruik Journey Optimizer-campagnes om via verschillende kanalen eenmalige inhoud aan een specifiek publiek te leveren. Wanneer u reizen gebruikt, worden handelingen op volgorde uitgevoerd. Met campagnes, worden de acties uitgevoerd gelijktijdig, of onmiddellijk, of gebaseerd op een gespecificeerd programma. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>Leer hoe u een campagne kunt maken in het dialoogvenster <a href="../campaigns/get-started-with-campaigns.md">gedetailleerde documentatie</a> en <a href="https://video.tv.adobe.com/v/346680">functievideo</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SMS verzenden naar uw gebruikers (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu SMS in Journey Optimizer maken, personaliseren en verzenden via integratie met <b>Sinch</b> of <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Leer hoe u in dit venster een SMS maakt en verzendt <a href="../sms/create-sms.md">gedetailleerde documentatie</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Verbeteringen

**Rapportage**

* De tabel en de grafiek van het beleid voor instemming zijn nu beschikbaar in algemene rapporten van Journey. Met deze widgets kunt u de uitgesloten profielen bijhouden in het beleid in uw aangepaste handelingen. [Meer informatie](../reports/journey-global-report.md#journey-global)

  Als u toegang wilt hebben tot de meest recente widgets, moet u de verschillende rapportdashboards opnieuw instellen. Raadpleeg voor meer informatie over het aanpassen van het dashboard [de gedetailleerde documentatie](../reports/global-report.md).

**Administratie**

* Het is nu mogelijk om het primaire telefoonnummer bij te werken dat voor het SMS-kanaal moet worden gebruikt. [Meer informatie](../configuration/primary-email-addresses.md)


## Release van juli 2022 {#july-2022-release}

### Nieuwe functies

<table>
<thead>
<tr>
<th><strong>Nieuwe in-line overseinenstroom</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer biedt een nieuwe stroom voor het schrijven van berichten in de pers. In-line berichten besparen gebruikers aanzienlijke tijd en stroomlijnen het workflowproces voor het maken en leveren van een e-mail, een pushmelding of een SMS in Journey Optimizer. Door Berichten als afzonderlijke stap te verwijderen en in plaats daarvan editable in-line als deel van een actie op het Canvas van de Reis te maken, zullen de gebruikers minder knopen moeten klikken en minder schermen navigeren om hun inhoud te ontwerpen en uit te geven.</p>
<img src="assets/do-not-localize/inline.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Op kenmerken gebaseerde toegangscontrole (beperkte beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt schemagebieden met etiketten nu identificeren die organisatorisch of gegevensgebruikswerkingsgebied bepalen. Beheerders kunnen de interface voor machtigingen gebruiken om toegangsbeleid te definiëren dat betrekking heeft op XDM-schemavelden en om de toegang die wordt verleend aan gebruikers of groepen gebruikers (interne, externe of externe gebruikers) beter te beheren, en om toegang tot specifieke typen gegevens (d.w.z. gevoelige persoonlijke gegevens/SPD) te beheren.</p>
<p>Het gebruik van op attributen-gebaseerde toegangsbeheer is momenteel beperkt tot geselecteerde gebruikers, en zal aan alle milieu's in een toekomstige versie worden opgesteld.</p>
<p>Raadpleeg de <a href="../administration/attribute-based-access.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Batchbeslissingstaken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt taken voor batchbepaling nu uitvoeren vanuit de gebruikersinterface, zodat ik geen ontwikkelaar nodig heb om taken voor batchverwerking uit te voeren en de tijd die nodig is voor marketing kan verminderen. Met deze nieuwe interface kunt u nieuwe taken maken en huidige en vroegere taken beheren.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Raadpleeg voor meer informatie de <a href="../offers/batch-delivery.md">gedetailleerde documentatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gebruik automatisch de best presterende aanbieding in uw besluiten (beperkte beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu gepersonaliseerde optimalisatiemodelsystemen gebruiken in besluitvormingsbeheer. Met dit nieuwe type model kunt u aanbiedingen optimaliseren en aanpassen op basis van publiek en prestaties.</p>
<p>Het gebruik van gepersonaliseerde optimalisatie-AI-modellen is momenteel beperkt tot geselecteerde gebruikers en wordt in een toekomstige release geïmplementeerd in alle omgevingen.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Raadpleeg de <a href="../offers/ranking/personalized-optimization-model.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Reizen**

* **Een reis beëindigen** - In het reiscanvas **Einde** activiteit is verwijderd uit het palet. Eindtags worden nu standaard aan het einde van elk pad toegevoegd en kunnen niet worden verwijderd. Dankzij deze verbetering kan beter worden aangegeven waar een klant de reis heeft verlaten, zonder dat de reisdeskundige enige actie hoeft te ondernemen. Zie de [documentatie](../building-journeys/end-journey.md) en [functievideo](https://video.tv.adobe.com/v/345376){target="_blank"}.


* De **Tijdzone van profiel** Deze optie is nu standaard uitgeschakeld in reiseigenschappen. [Meer informatie](../building-journeys/timezone-management.md#timezone-from-profiles)

**Berichten**

* Voorinstellingen voor berichten zijn nu **kanaaloppervlakken**. [Meer informatie](../configuration/channel-surfaces.md)

**Administratie**

* **PTR-recordeditie** - Wanneer u nu een PTR-record bijwerkt, duurt de verwerkingstijd maximaal 3 uur. [Meer informatie](../configuration/ptr-records.md#processing)

* **UI LIJST VAN GEWENSTE PERSONEN** - U kunt nu de Journey Optimizer-gebruikersinterface gebruiken om nieuwe e-mailadressen of domeinen aan de lijst van gewenste personen toe te voegen. [Meer informatie](../configuration/allow-list.md)

* **Update voor logica van lijst van gewenste personen** - De logica lijst van gewenste personen wordt nu toegepast zodra de functie is ingeschakeld, zelfs als de lijst leeg is. [Meer informatie](../configuration/allow-list.md#logic)

* **Parameters voor URL-tracking** - U kunt nu de Expressieeditor gebruiken om URL-volgparameters in uw e-mailoppervlakken (dus voorinstellingen) te configureren. [Meer informatie](../email/email-settings.md#url-tracking)

**Beslissingsbeheer**

* **Grootte publiek** - Er wordt nu een nieuwe Beoordelingscomponent voor de doelgrootte weergegeven in de gebruikersinterface wanneer u een beslissingsregel maakt, een publiek of een regel selecteert om een geschiktheid voor de aanbieding in te stellen of een publiek of regel toevoegt aan een beslissingsbereik.


## Release van juni 2022 {#june-2022-release}

### Nieuwe functies

<table>
<thead>
<tr>
<th><strong>SMS verzenden naar uw gebruikers (beperkte beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu SMS in Journey Optimizer maken, personaliseren en verzenden via integratie met <b>Sinch</b> of <b>Twilio</b>.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>Het SMS-kanaal is momenteel alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe.</p>
<p>Leer hoe u in dit venster een SMS maakt en verzendt <a href="../sms/create-sms.md">gedetailleerde documentatie</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Snellere afbeeldingen zoeken dankzij Adobe Stock-integratie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De integratie-insteekmodule Adobe Stock en Adobe Journey Optimizer Email Designer biedt klanten een eenvoudige manier om te navigeren in afbeeldingen en deze te licentiëren en op te slaan voor gebruik in het schrijven van berichten. </br> De nieuwe <b>Vergelijkbare stockfoto's zoeken</b> kunt u ook Stock-foto's zoeken die overeenkomen met de inhoud, kleur en compositie van de afbeeldingen. </p>
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>Raadpleeg de <a href="../content-management/stock.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>BCC via e-mail gebruiken op al uw e-mails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu de e-mailfunctie BCC (blinde koolstofkopie) gebruiken om e-mails op te slaan die door Adobe Journey Optimizer zijn verzonden. Schakel deze optie in uw e-mailvoorinstellingen in, zodat elke verzonden e-mail blind wordt gekopieerd naar uw BCC-adres.</p>
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
<p>Raadpleeg de <a href="../configuration/archiving-support.md#bcc-email">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on audiences and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Objecten kopiëren tussen sandboxen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt de ervaringen nu opnieuw maken van een Journey Optimizer-sandbox naar een andere sandbox, bijvoorbeeld van een niet-productiesandbox naar een productiesandbox. Deze nieuwe mogelijkheid kopieert een volledige Reis, inclusief alle objecten waarvan de Reis afhankelijk is om correct te worden uitgevoerd, van de ene omgeving naar de andere. Naast Reizen kunt u ook andere componenten kopiëren, zoals Aanbiedingen, Berichten, Schema's, Datasets, Gegevensbronnen, Gebeurtenissen en Handelingen.</p>
<p>Raadpleeg de <a href="../building-journeys/copy-to-sandbox.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>




### Verbeteringen

**Beslissingsbeheer**

* **Ondersteuning voor HTML- en JSON-bestanden** - U kunt nu externe HTML- en JSON-bestanden van de Adobe Experience Cloud Asset-bibliotheek naar de inhoud van de aanbiedingsweergave slepen. [Meer informatie](../offers/offer-library/add-representations.md#html-json)


**E-mail**

* **Opslaan als sjabloon** - U kunt nu e-mailinhoud opslaan als een sjabloon en deze opnieuw gebruiken wanneer u andere berichten maakt. [Meer informatie](../content-management/content-templates.md#save-as-template)


**Administratie**

* **Voorvertoning van URL-parameters bijhouden** - Als u een berichtvoorinstelling configureert en URL-trackingparameters definieert, wordt nu een dynamische voorvertoning van de resulterende URL weergegeven. [Meer informatie](../email/email-settings.md#url-tracking)

* **Vooraf ingestelde berichtversie** - Wanneer u nu een berichtvoorinstelling bijwerkt, kan de verwerkingstijd maximaal 3 uur duren. [Meer informatie](../configuration/channel-surfaces.md#edit-channel-surface)

* **IP-pooleditie** - Wanneer het bijwerken van een IP pool, kan de verwerkingstijd slechts tot 3 uren vergen. [Meer informatie](../configuration/ip-pools.md#edit-ip-pool)




## Release van mei 2022 {#may-2022-release}

### Nieuwe functies

<table>
<thead>
<tr>
<th><strong>Regels voor berichtfrequentie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu bedrijfsregels voor meerdere kanalen instellen die overgevraagde profielen automatisch uitsluiten van berichten en handelingen.</p>
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>Raadpleeg de <a href="../configuration/frequency-rules.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Beslissingsbeheer - Automatisch optimalisatiemodel met AI-classificatie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu getrainde modelsystemen gebruiken in Beslissingsbeheer. Deze nieuwe capaciteitranches kunnen worden weergegeven voor een bepaald profiel.</p>
<!--img src="assets/do-not-localize/optimization.gif"/-->
<p>Raadpleeg de <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer Audit Logs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu de acties controleren die gebruikers op Adobe Journey Optimizer-bronnen uitvoeren.</p>
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>Raadpleeg de <a href="../privacy/audit-logs.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Personalisatie**

* **Nieuwe hulpfunctie voor verborgen tekens** - de `mask` Met de hulpfunctie kunt u een deel van een tekenreeks vervangen door &quot;X&quot;-tekens. [Meer informatie](../personalization/functions/string.md#mask)

**Openingspagina&#39;s**

* **Pagina&#39;s zonder formulier landen** - U kunt nu een bestemmingspagina maken en publiceren die geen formulier bevat en geen actie van bezoekers vereist.
* **Sjablonen voor bestemmingspagina** - U kunt een landingspagina nu opslaan als een sjabloon en deze opnieuw gebruiken bij het maken van andere bestemmingspagina&#39;s. [Meer informatie](../landing-pages/lp-templates.md)
* **Terug naar de primaire pagina** - U kunt nu een koppeling naar de primaire pagina toevoegen vanuit elke subpagina binnen dezelfde bestemmingspagina.
* **Aangepaste JavaScript-ondersteuning** - U kunt nu aangepaste JavaScript toevoegen aan uw bestemmingspagina-inhoud om geavanceerde stijlen uit te voeren of aangepaste gedragingen toe te voegen aan uw bestemmingspagina&#39;s.    [Meer informatie](../landing-pages/lp-custom-js.md)

**Reizen**

* **Lees publiek** - Eenmalig Leespubliek wordt nu 30 dagen na de uitvoering van de reis de status Voltooid. Voor een gepland leespubliek duurt het 30 dagen na de uitvoering van het laatste exemplaar. [Meer informatie](../building-journeys/read-audience.md)
* **Expression-editor** - de [limiet](../building-journeys/functions/functionlimit.md) Er is een functie toegevoegd waarmee u het aantal items in een lijst kunt beperken. De [sorteren](../building-journeys/functions/functionsort.md) Met deze functie kunt u nu een lijstobject sorteren. De ondersteuning van listObject is ook toegevoegd aan de [onenigheid](../building-journeys/functions/functiondistinct.md) en [differentWithNull](../building-journeys/functions/functiondistinctwithnull.md) functies.

**Administratie**

* **Update van het gebruiksdashboard voor licenties** - Het gebruiksdashboard voor licenties is beschikbaar in het dialoogvenster [!DNL Adobe Journey Optimizer] de gebruikersinterface weerspiegelt nu de juiste waarde voor de **Gelicentieerd** Gemiddelde profielrijkheid. Deze metrische weergave wordt verlaagd, wat betekent dat de licentielimiet nu correct wordt gerapporteerd. [Meer informatie](../audience/license-usage.md)


## Release van april 2022 {#april-2022-release}

### Verbeteringen

**Openingspagina&#39;s**

* **Nieuwe optie voor selectievakjes opt-in/opt-out** - U kunt nu een enkel selectievakje voor aanmelding/opt-out invoegen op abonnementsbestemmingspagina&#39;s. Gebruikers moeten het selectievakje voor toestemming (opt-in) inschakelen en het selectievakje uitschakelen om hun toestemming (opt-out) te verwijderen. [Meer informatie](../landing-pages/design-lp.md#define-lp-specific-content)

* **Vooraf opgevulde landingspaginavelden** - Het is nu mogelijk om gebruikers de mogelijkheid te geven om de landingspagina-velden vooraf te vullen met profielinformatie. [Meer informatie](../landing-pages/create-lp.md#configure-primary-page)

**Beslissingsbeheer**

* **API voor besluitvorming op Edge** - Edge Decisioning API kan persoonlijke aanbiedingen leveren en weergeven die worden beheerd in besluitvormingsbeheer. U kunt uw aanbiedingen en andere gerelateerde objecten maken met behulp van de gebruikersinterface (UI) of API&#39;s voor besluitvormingsbeheer. [Meer informatie](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administratie**

* **PTR-verzendduur** - De effectieve duur van PTR-bewerkingen is nu een paar uur. [Meer informatie](../configuration/ptr-records.md#processing)

**E-mailontwerp**

* **20 nieuwe e-mailsjablonen** zijn nu beschikbaar om uw e-mailinhoud te ontwerpen in Journey Optimizer.

**Gebruikersinterface**

* **Contextafhankelijke Help in de gebruikersinterface van Journey Optimizer** - Er zijn contextafhankelijke Help-koppelingen toegevoegd aan meerdere pagina&#39;s in Journey Optimizer. Klik, indien beschikbaar, op het pictogram &quot;i&quot; om een snelle beschrijving van de huidige functionaliteit en artikelen die betrekking hebben op toegang, weer te geven.

**Integratie met Adobe Campaign Standard**

Als Adobe Campaign Standard-klant kunt u nu e-mails, pushberichten en SMS verzenden via Journey Optimizer. Gebruik de nieuwe ingebouwde acties om de Transactionele mogelijkheden van het Overseinen van het Campaign Standard in Journey Optimizer te gebruiken.  [Meer informatie](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Release van maart 2022 {#march-2022-release}

### Verbeteringen

**Reizen**

* Als u wilt voorkomen dat het schema van het uniforme profiel onnodige velden bevat, is het schema voor de gebeurtenis Reisstap niet meer standaard ingeschakeld voor profielen. Indien nodig, kunt u het activeren. [Meer informatie](../reports/sharing-overview.md)
* Journey Optimizer stuurt nu nieuwe stapgebeurtenissen met betrekking tot exporttaken naar Adobe Experience Platform. Voorbeelden van query&#39;s zijn toegevoegd aan documentatie. [Meer informatie](../reports/query-examples.md)

**Beslissingsbeheer**

* U kunt nu opgeven of het aanbieden van een maximum wordt toegepast op alle gebruikers of op één specifiek profiel, en op alle plaatsen of per plaatsing. [Meer informatie](../offers/offer-library/add-constraints.md#capping)
* Met de Batch-API kunnen organisaties de functionaliteit voor besluitvormingsbeheer gebruiken voor alle profielen in een bepaald publiek in één aanroep. De aanbiedingsinhoud voor elke profielen in het publiek wordt geplaatst in een AEP dataset waar het voor de werkschema&#39;s van de douanepartij beschikbaar is. [Meer informatie](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administratie**

* U kunt nu de koppeling voor het afmelden van abonnementen in- of uitschakelen in de e-mailheader op het niveau van de berichtvoorinstelling en een aangepaste URL voor het afmelden van abonnementen instellen op berichtniveau. [Meer informatie](../configuration/channel-surfaces.md#list-unsubscribe)
* De lijst van gewenste personen kan nu worden in- en uitgeschakeld via de [!DNL Journey Optimizer] interface over productie- en niet-productie-sandboxen. [Meer informatie](../configuration/allow-list.md#enable-allow-list)

**Personalisatie**

* U kunt nu meer dan 40 personalisatie-expressies opslaan in de bibliotheek. [Meer informatie](../personalization/use-expression-fragments.md)

## Release van februari 2022 {#feb-2022-release}

### Nieuwe functies

<table>
<thead>
<tr>
<th><strong>Landingspagina's abonnement</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu bestemmingspagina's in Journey Optimizer maken en ontwerpen en uw gebruikers naar onlineformulieren sturen waar zij zich kunnen aanmelden of weigeren uw communicatie te ontvangen, of u kunt zich abonneren op een specifieke service zoals een nieuwsbrief.</p>
<p>Raadpleeg voor meer informatie de <a href="../landing-pages/create-lp.md">gedetailleerde documentatie</a> en aanverwante <a href="../landing-pages/lp-use-cases.md">voorbeeldgebruik</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nieuwe bibliotheek voor persoonlijke expressie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer beschikt nu over een bibliotheek waarmee u toegang kunt krijgen tot vooraf gedefinieerde personalisatie-expressies. Deze expressies worden geconfigureerd door Admin-gebruikers.</p>
<p>Raadpleeg de <a href="../personalization/use-expression-fragments.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs' feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Geef informatie door om uw berichten bij te houden met parameters voor het bijhouden van UTM</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer-berichtinhoud kunt u nu UTM-parameters aan uw koppelingen toevoegen. Deze kunnen aanvullende gegevens over die koppeling verschaffen en u helpen te bepalen waar en waarom iemand op uw koppeling heeft geklikt.</p>
<p>Raadpleeg de <a href="../configuration/channel-surfaces.md#configure-email-settings">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Reizen**

* Om de prestaties te optimaliseren, zullen alle reizen in testwijze die niet voor een week zijn teweeggebracht nu op de status van het Ontwerp terugschakelen. [Meer informatie](../building-journeys/testing-the-journey.md#important_notes)
* De integratie tussen Journey Optimizer en Adobe Campaign v7/v8 is geoptimaliseerd om de prestaties te verbeteren. De het maximum standaardconfiguratie is veranderd in 4000 vraag/5 minuten. [Meer informatie](../action/acc-action.md#important-notes)

**Rapportage**

* De leveringen kunnen nu worden gefilterd op basis van hun status:
   * In de lijst Berichtenuitvoering kunt u nu proefdrukken uitsluiten van de lijst met leveringen.
   * In uw Live/Global-rapporten kunt u testgebeurtenissen uitsluiten.

* U hebt nu toegang tot rapporten over de optimalisatiegegevens van Verzendtijd: het aantal personen dat onmiddellijk berichten waren en het aantal personen dat via optimalisatie van 1 uur werd gemaild, 2 uur optimalisatie, enz.

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Beslissingsbeheer**

* De classificaties en de AI-classificatie worden nu gegroepeerd in één enkel tabblad.

## Release van januari 2022 {#january-2022-release}

### Nieuwe functies

<table>
<thead>
<tr>
<th><strong>Reizen - Optimaliseer uw IP helling met de GLB voorwaarden van het Profiel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Wanneer u een <strong>Voorwaarde</strong> tijdens een rit kunt u nu een profieluiteinde definiëren. Met dit nieuwe voorwaardetype kunt u een maximumaantal profielen instellen voor een reispad. Wanneer deze limiet is bereikt, hebben de invoerprofielen een ander pad. Dit staat u toe om het volume van uw leveringen (IP oprijplaat) te verhogen. U kunt bijvoorbeeld uw leveringen opvoeren op een domein door de uitvoering te splitsen: verzend 1000 berichten op dag 1, 2000 op dag 2, enz.</p>
<p>Raadpleeg de <a href="../building-journeys/condition-activity.md#profile_cap">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reizen - Verbetering van het publiek lezen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De <strong>Incrementeel lezen</strong> is toegevoegd aan terugkerende <strong>Lees publiek</strong> activiteiten. Met deze optie kunt u zich alleen richten op de personen die het publiek zijn binnengekomen sinds de laatste uitvoering van de reis. De eerste uitvoering richt zich altijd op alle publieksleden.</p>
<p>Raadpleeg de <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Reizen**

* Journey Optimizer step-gebeurtenissen kunnen nu worden gekoppeld aan andere datasets in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html). De **profileID** in het ingebouwde schema voor de gebeurtenis van de Stap van de Reis, wordt nu gedefinieerd als identiteitsgebied. [Meer informatie](../reports/sharing-overview.md#integration-cja)

**Beslissingsbeheer**

* Wanneer u een aanbod, een fallback-aanbieding, een verzameling van aanbiedingen of een besluit van een aanbieding bijwerkt waarnaar direct of indirect wordt verwezen in een gepubliceerd bericht, worden de updates nu automatisch weerspiegeld in het bijbehorende bericht, zonder dat u het bericht opnieuw hoeft te publiceren. [Meer informatie](../offers/offers-e2e.md#insert-decision-in-email)

* Wanneer het simuleren welke aanbiedingen voor een bepaald testprofiel zullen worden geleverd, kunt u de standaardsimulatie montages nu wijzigen, en de code bekijken die aan uw simulaties beantwoordt die voor het oplossen van problemendoel kunnen worden gebruikt. [Meer informatie](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administratie**

* Beheerders kunnen nu PTR-records bewerken met een CNAME-setsubdomein. [Meer informatie](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalisatie**

* **Toevoegen aan Favorieten** - Om de efficiëntie te verbeteren bij het werken met personalisatie hebben we het concept van het redden van favorieten geïntroduceerd. Door verschillende kenmerken toe te voegen aan het menu Favorieten hebt u snel toegang tot de meest gebruikte items. [Meer informatie](../personalization/personalize.md#fav)
