---
title: Aanvullende informatie
description: Journey Optimizer Release-aantekeningen
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: tm+mt
source-wordcount: '2973'
ht-degree: 9%

---

# Aanvullende informatie {#release-notes}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen voor [!DNL Journey Optimizer]. U kunt ook de [meest recente documentatie-updates](documentation-updates.md) pagina voor meer wijzigingen.

!DNL Adobe Journey Optimizer] is standaard op [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} vandaag en ontvang de nieuwste productupdates, spannende artikelen, gebruiksscenario&#39;s, tips en nog veel meer die elk kwartaal rechtstreeks aan uw Postvak IN worden bezorgd.


## Release van maart 2022 {#march-2022-release}

### Verbeteringen

**Journeys**

* Als u wilt voorkomen dat het schema van het uniforme profiel onnodige velden bevat, is het schema voor de gebeurtenis Reisstap niet meer standaard ingeschakeld voor profielen. Indien nodig, kunt u het activeren. [Meer informatie](../reports/sharing-overview.md)
* Journey Optimizer stuurt nu nieuwe stapgebeurtenissen met betrekking tot exporttaken naar Adobe Experience Platform. Voorbeelden van query&#39;s zijn toegevoegd aan documentatie. [Meer informatie](../reports/query-examples.md)

**Beslissingsbeheer**

* U kunt nu opgeven of het aanbieden van een maximum wordt toegepast op alle gebruikers of op één specifiek profiel, en op alle plaatsen of per plaatsing. [Meer informatie](../offers/offer-library/add-constraints.md#capping)
* Met de Batch-beslissings-API kunnen organisaties de functionaliteit offer decisioning gebruiken voor alle profielen in een bepaald segment in één aanroep. De aanbiedingsinhoud voor elke profielen in het segment wordt geplaatst in een AEP dataset waar het voor de werkschema&#39;s van de douanepartij beschikbaar is. [Meer informatie](../offers/api-reference/batch-api/deliver-offers-batch.md)

**Beheer**

* U kunt nu de koppeling voor het afmelden van abonnementen in- of uitschakelen in de e-mailheader op het niveau van de berichtvoorinstelling en een aangepaste URL voor het afmelden van abonnementen instellen op berichtniveau. [Meer informatie](../configuration/message-presets.md#list-unsubscribe)
* De lijst van gewenste personen kan nu worden in- en uitgeschakeld via de [!DNL Journey Optimizer] interface over productie- en niet-productie-sandboxen. [Meer informatie](../reports/allow-list.md#enable-allow-list)

**Personalisatie**

* U kunt nu meer dan 40 personalisatie-expressies opslaan in de bibliotheek. [Meer informatie](../personalization/personalization-library.md)

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
<th><strong>Nieuwe Personalization-expressiebibliotheek</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer beschikt nu over een bibliotheek waarmee u toegang kunt krijgen tot vooraf gedefinieerde personalisatie-expressies. Deze expressies worden geconfigureerd door Admin-gebruikers.</p>
<p>Raadpleeg de <a href="../personalization/personalization-library.md">gedetailleerde documentatie</a> voor meer informatie.</p>
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
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
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
<p>In Journey Optimizer-berichtinhoud kunt u nu UTM-parameters aan uw koppelingen toevoegen: zij kunnen extra gegevens over die verbinding verstrekken, en u helpen identificeren waar en waarom een persoon op uw verbinding klikte.</p>
<p>Raadpleeg de <a href="../configuration/message-presets.md#configure-email-settings">gedetailleerde documentatie</a> voor meer informatie.</p-->
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Reizen**

* Om de prestaties te optimaliseren, zullen alle reizen in testwijze die niet voor een week zijn teweeggebracht nu op de status van het Ontwerp terugschakelen. [Meer informatie](../building-journeys/testing-the-journey.md#important_notes)
* De integratie tussen Journey Optimizer en Adobe Campaign Classic is geoptimaliseerd om de prestaties te verbeteren. De het maximum standaardconfiguratie is veranderd in 4000 vraag/5 minuten.	[Meer informatie](../action/acc-action.md#important-notes)

**Rapportage**

* De leveringen kunnen nu worden gefilterd op basis van hun status:
   * In de lijst Berichtenuitvoering kunt u nu proefdrukken uitsluiten van de lijst met leveringen.
   * In uw Live/Global-rapporten kunt u testgebeurtenissen uitsluiten.

* U kunt nu rapporten openen over de gegevens voor Tijdoptimalisatie verzenden: het aantal personen dat onmiddellijk berichten was en het aantal personen dat met optimalisatie van 1 uur, optimalisatie van 2 uur, enz. werd gecommuniceerd.

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

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
<p>Wanneer u een <strong>Voorwaarde</strong> tijdens een rit kunt u nu een profieluiteinde definiëren. Met dit nieuwe voorwaardetype kunt u een maximumaantal profielen instellen voor een reispad. Wanneer deze limiet is bereikt, hebben de invoerprofielen een ander pad. Dit staat u toe om het volume van uw leveringen (IP oprijplaat) te verhogen. U kunt bijvoorbeeld de levering in een domein opsplitsen door de uitvoering te splitsen: verzend 1000 berichten op dag 1, 2000 op dag 2, enz.</p>
<p>Raadpleeg voor meer informatie de <a href="../building-journeys/condition-activity.md#profile_cap">gedetailleerde documentatie</a> en aanverwante <a href="../building-journeys/ramp-up-deliveries-uc.md">voorbeeldgebruik</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reizen - Verbetering van het leessegment</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De <strong>Incrementeel lezen</strong> is toegevoegd aan terugkerende <strong>Segment lezen</strong> activiteiten. Met deze optie kunt u zich alleen richten op de personen die het segment hebben betreden sinds de laatste uitvoering van de reis. De eerste uitvoering richt altijd alle segmentleden.</p>
<p>Raadpleeg de <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Reizen**

* Journey Optimizer step-gebeurtenissen kunnen nu worden gekoppeld aan andere datasets in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html). De **profileID** in het ingebouwde schema voor de gebeurtenis van de Stap van de Reis, wordt nu gedefinieerd als identiteitsgebied. [Meer informatie](../reports/sharing-overview.md#integration-cja)

**offer decisioning**

* Wanneer u een aanbod, een fallback-aanbieding, een verzameling van aanbiedingen of een besluit van een aanbieding bijwerkt waarnaar direct of indirect wordt verwezen in een gepubliceerd bericht, worden de updates nu automatisch weerspiegeld in het bijbehorende bericht, zonder dat u het bericht opnieuw hoeft te publiceren. [Meer informatie](../offers/offers-e2e.md#insert-decision-in-email)

* Wanneer het simuleren welke aanbiedingen voor een bepaald testprofiel zullen worden geleverd, kunt u de standaardsimulatie montages nu wijzigen, en de code bekijken die aan uw simulaties beantwoordt die voor het oplossen van problemendoel kunnen worden gebruikt. [Meer informatie](../offers/offer-activities/simulation.md#define-simulation-settings)

**Beheer**

* Beheerders kunnen nu PTR-records bewerken met een CNAME-setsubdomein. [Meer informatie](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalisatie**

* **Toevoegen aan Favorieten** - Om de efficiëntie van het werken met personalisatie te verbeteren, hebben we het concept &#39;sparen-favorieten&#39; geïntroduceerd. Door verschillende kenmerken toe te voegen aan het menu Favorieten hebt u snel toegang tot de meest gebruikte items. [Meer informatie](../personalization/personalize.md#fav)

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
<p>U kunt nu simuleren welke aanbiedingen worden geleverd aan een testprofiel voor een bepaalde plaatsing in de gebruikersinterface van Journey Optimizer. Hierdoor kunt u uw besluitvormingslogica, inclusief geschiktheidsbeperkingen en classificatiealgoritmen, eenvoudig valideren voordat u ze in productie zet. Met deze functie kunnen niet-technische en technische gebruikers snel offer decisioning testen en mogelijke problemen oplossen.</p>
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

**Reizen**

* **Expression-editor** - Als energiegebruiker kunt u nu functies gebruiken om met kaarten te werken. Deze mogelijkheid kan worden benut met de abonnementenlijsten. Als voorbeeld, van een segment, kunt u een e-mailadres van een abonnementenlijst nu krijgen. [Meer informatie in dit voorbeeld](../building-journeys/message-to-subscribers-uc.md)

* **Toezicht** - De stapgebeurtenissen voor de live ritten en de testmodus zijn verbeterd. [Nieuwe velden](../reports/sharing-field-list.md#serviceevents) zijn toegevoegd met betrekking tot exporttaken voor profielen. Voor een betere gebruikerservaring zijn de velden voor stapgebeurtenissen nu ingedeeld in verschillende categorieën. Alle gebeurtenisvelden van vorige stappen zijn nog steeds beschikbaar in het dialoogvenster [stepEvents](../reports/sharing-legacy-fields.md) categorie.
* **Toegankelijkheid** - Er zijn verbeteringen aangebracht in de toegankelijkheid van reizen.
* **Verzamelingen** - Arrays met objecten die subobjecten bevatten, worden nu ondersteund. [Meer informatie](../building-journeys/collections.md)
* **Lijsten** - Lijstschermen zijn verbeterd voor reizen, gebeurtenissen, handelingen, gegevensbronnen.

**Rapportage**

* **Gegevensindeling in algemene weergave** - U kunt nu schakelen tussen getallen en percentages in het dialoogvenster **Globale weergave** van de **Uitvoering** tab. [Meer informatie](../reports/message-monitoring.md)


**Beheer**

* **Voorinstellingen voor berichten bewerken** - U kunt nu voorinstellingen voor berichten bewerken en de status van de berichten controleren. [Meer informatie](../configuration/message-presets.md#edit-message-preset)
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
<p>Raadpleeg de <a href="../reports/message-monitoring.md">gedetailleerde documentatie</a> voor meer informatie.</p>
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

**Reizen**

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

**Reizen**

* **Dynamische koppen** - U kunt nu dynamische gegevens doorgeven in HTTP-headerparameters. Deze parameters kunnen door de integratiesystemen worden gebruikt die de vraag van HTTP van de reisactie, bijvoorbeeld timestamp of het volgen identiteitskaart ontvangen. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)
* **Dynamische URL-paden** - U kunt nu dynamische URL-paden instellen voor aangepaste handelingen. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)
* De algemene vertragingssnelheid voor gelezen segmenten is veranderd van 17.000 in 20.000 berichten per seconde. [Meer informatie](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Gebruikersinterface**

* **Zoeken** - Op elke pagina, kunt u bedrijfsvoorwerpen en hulpartikelen van het Verenigde Experience Cloud onderzoeksgebied nu direct zoeken. [Meer informatie](../start/user-interface.md#unified-search)
* **Recenten** - De weergave van recente elementen van de startpagina van Adobe Journey Optimizer wordt nu uitgebreid naar extra zakelijke objecten. Met deze update, omvatten de kortere weg aan uw onlangs betreden Berichten, Reizen, Segmenten, Schema&#39;s, Datasets, Gegevensbronnen, Gebeurtenissen, Acties, Bronnen, en Doelen. [Meer informatie](../action/about-custom-action-configuration.md#passing-collection)

**Inhoud ontwerpen**

* **Achtergrond** - Achtergrondafbeeldingen worden nu ondersteund in live voorvertoning. [Meer informatie](../design/preview.md)
* **Een-klik-koppeling voor weigeren** - U kunt een nieuw type koppeling invoegen in uw e-mailinhoud: de **Uitschakelen** de verbinding staat gebruikers toe om van het ontvangen van uw mededelingen in slechts één klik af te zien, zonder opnieuw te worden gericht aan een het landen pagina om het uit kiezen te bevestigen. [Meer informatie](../messages/consent.md#one-click-opt-out-link)

**Personalisatie**

* **Expressieeditor** - U kunt nu eenvoudig een terugvalwaarde toevoegen bij het definiëren van een personalisatie: als het verpersoonlijkingsgebied voor een profiel leeg is, zal de reserve waarde tonen. [Meer informatie](../personalization/functions/helpers.md)

**E-mailconfiguratie**

* **Lijst van gewenste personen** - De lijst van gewenste personen kan nu worden in- en uitgeschakeld op een niet-productiesandbox via een API-aanroep. [Meer informatie](../reports/allow-list.md#enable-allow-list)
* **Navigatie** - De onderdrukkingslijst, die toegankelijk was onder de **Beheer > Kanalen > E-mailconfiguratie > Algemeen** is verplaatst naar het nieuwe **Onderdrukkingslijst** submenu, dat alle verwante mogelijkheden voor gemakkelijkere toegang verzamelt. [Meer informatie](../configuration/manage-suppression-list.md#access-suppression-list)

**Beslissingsbeheer**

* De manier waarop u weergaven toevoegt en configureert wanneer u een aanbod maakt, is bijgewerkt voor een betere gebruikerservaring. In het bijzonder wordt de bibliotheek met assets nu alleen weergegeven wanneer u content van het afbeeldingstype voor een weergave definieert. [Meer informatie](../offers/offer-library/creating-personalized-offers.md#representations)

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
<p>Raadpleeg de <a href="../reports/allow-list.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Reizen**

* De algemene vertragingssnelheid van alle gelezen segmenten die gelijktijdig in dezelfde sandbox worden uitgevoerd, is beperkt tot 17.000 berichten per seconde. [Meer informatie](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* De **Cacheduur** Het veld is verwijderd uit het configuratievenster van de gegevensbron. [Meer informatie](../datasource/about-data-sources.md)
* Voor externe gegevensbronnen, wordt een het maximum van 15 vraag per seconde nu automatisch bepaald. [Meer informatie](../configuration/external-systems.md#capping)
* Voor live reizen worden in het scherm met de reiseigenschappen nu de publicatiedatum en de naam van de gebruiker weergegeven die de reis heeft gepubliceerd. [Meer informatie](../building-journeys/journey-gs.md#change-properties)
* In het scherm van de reislijst, is het filter van het reistype toegevoegd. [Meer informatie](../start/user-interface.md#filter-lists)
* De **[!UICONTROL Throttling rate]** parameter is toegevoegd in de Gelezen segmentactiviteit. [Meer informatie](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Voorbeeld- en testberichten**

* Identiteit en naamruimte zijn nu zichtbaar in het dialoogvenster **[!UICONTROL Preview]** scherm. [Meer informatie](../design/preview.md#preview-your-messages)
* Het aantal teste-mails voor proefdrukken is nu beperkt tot tien.
* Toegestane tekens voor de **Voorvoegsel van onderwerpregel** op het gebied van proefdrukken is het aantal . [Meer informatie](../design/preview.md#send-proofs)

**Editor voor persoonlijke expressie**

* De naam van de vervolgkeuzelijst met hulplijnen is gewijzigd en de volgorde ervan is gewijzigd.

### Oplossingen

* Probleem verholpen waarbij dubbele berichten werden afgeleverd voor verzending via batchberichten.
* Gebeurtenissen worden nu overeenkomstig gegenereerd wanneer het verzenden van e-mail niet wordt uitgevoerd wanneer de periode voor opnieuw proberen is verstreken.
* Oplossing voor een probleem waarbij IP-informatie ontbrak in het scherm PTR-records.
* De lokalisatie in het aanbod van het spoor binnen de Redacteur van de Uitdrukking wordt nu uitgevoerd.
* Onjuiste spatiëring in pop-ups met gegevens gecorrigeerd.
* Probleem verholpen in de e-mailontwerper bij het uploaden van een HTML-bestand met een intern stijlblad met `background-image` eigenschap wordt niet ondersteund.
