---
title: Release-aantekeningen 2022
description: Opmerkingen bij de release van Journey Optimizer 2022
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: bfd12553c653a4d4caccc969cb51b1416c64ba65
workflow-type: tm+mt
source-wordcount: '1418'
ht-degree: 9%

---

# Aanvullende informatie 2022 {#release-notes-2022}

Deze pagina bevat alle functies en verbeteringen voor [!DNL Journey Optimizer] vrijgegeven in 2022.

De meest recente opmerkingen bij de release zijn beschikbaar [op deze pagina](release-notes.md).

elke kwart naar uw postvak.

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
<img src="assets/do-not-localize/frequency-rn.gif"/>
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
<img src="assets/do-not-localize/optimization.gif"/>
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
<img src="assets/do-not-localize/audit-rn.gif"/>
<p>Raadpleeg de <a href="../privacy/audit-logs.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Personalisatie**

* **Nieuwe hulpfunctie voor verborgen tekens** - de `mask` Met de hulpfunctie kunt u een deel van een tekenreeks vervangen door &quot;X&quot;-tekens. [Meer informatie](../personalization/functions/string.md#mask)

**Landingspagina’s**

* **Pagina&#39;s zonder formulier landen** - U kunt nu een bestemmingspagina maken en publiceren die geen formulier bevat en geen actie van bezoekers vereist.
* **Sjablonen voor bestemmingspagina** - U kunt een landingspagina nu opslaan als een sjabloon en deze opnieuw gebruiken bij het maken van andere bestemmingspagina&#39;s. [Meer informatie](../landing-pages/lp-templates.md)
* **Terug naar de primaire pagina** - U kunt nu een koppeling naar de primaire pagina toevoegen vanuit elke subpagina binnen dezelfde bestemmingspagina.
* **Aangepaste JavaScript-ondersteuning** - U kunt nu aangepaste JavaScript toevoegen aan uw bestemmingspagina-inhoud om geavanceerde stijlen uit te voeren of aangepaste gedragingen toe te voegen aan uw bestemmingspagina&#39;s.	[Meer informatie](../landing-pages/lp-custom-js.md)

**Journeys**

* **Segment lezen** - Eenmalig Leessegment-reizen gaan nu 30 dagen na de uitvoering van de reis over naar de voltooide status. Voor geplande Gelezen segmenten, is het 30 dagen na de uitvoering van het laatste voorkomen. [Meer informatie](../building-journeys/read-segment.md)
* **Expression-editor** - de [limiet](../building-journeys/functions/functionlimit.md) Er is een functie toegevoegd waarmee u het aantal items in een lijst kunt beperken. De [sorteren](../building-journeys/functions/functionsort.md) Met deze functie kunt u nu een lijstobject sorteren. De ondersteuning van listObject is ook toegevoegd aan de [ontkenning](../building-journeys/functions/functiondistinct.md) en [differentWithNull](../building-journeys/functions/functiondistinctwithnull.md) functies.

**Beheer**

* **Update voor gebruiksdashboard voor licenties** - Het gebruiksdashboard voor licenties is beschikbaar in het dialoogvenster [!DNL Adobe Journey Optimizer] de gebruikersinterface weerspiegelt nu de juiste waarde voor de **Gelicentieerd** Gemiddelde profielrijkheid. Deze metrische weergave wordt verlaagd, wat betekent dat de licentielimiet nu correct wordt gerapporteerd. [Meer informatie](../segment/license-usage.md)


## Release van april 2022 {#april-2022-release}

### Verbeteringen

**Landingspagina’s**

* **Nieuwe optie voor selectievakjes opt-in/opt-out** - U kunt nu één selectievakje voor aanmelding/opt-out invoegen op abonnementsbestemmingspagina&#39;s. Gebruikers moeten het selectievakje voor toestemming (opt-in) inschakelen en het selectievakje uitschakelen om hun toestemming (opt-out) te verwijderen. [Meer informatie](../landing-pages/design-lp.md#define-lp-specific-content)

* **Vooraf opgevulde landingspaginavelden** - Het is nu mogelijk om gebruikers de mogelijkheid te geven om de landingspagina-velden vooraf te vullen met profielinformatie. [Meer informatie](../landing-pages/create-lp.md#configure-primary-page)

**Beslissingsbeheer**

* **API voor besluitvorming op Edge** - De Edge-API voor besluitvorming kan persoonlijke aanbiedingen die in de Offer decisioning worden beheerd, leveren en renderen. U kunt uw aanbiedingen en andere verwante objecten maken met de gebruikersinterface (UI) of API&#39;s van de Offer decisioning. [Meer informatie](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Beheer**

* **PTR-verzendduur** - De effectieve duur van PTR-bewerkingen is nu een paar uur. [Meer informatie](../configuration/ptr-records.md#processing)

**E-mailontwerp**

* **20 nieuwe e-mailsjablonen** zijn nu beschikbaar om uw e-mailinhoud te ontwerpen in Journey Optimizer.

**Gebruikersinterface**

* **Contextafhankelijke Help in de gebruikersinterface van Journey Optimizer** - Er zijn contextafhankelijke Help-koppelingen toegevoegd aan meerdere pagina&#39;s in Journey Optimizer. Klik, indien beschikbaar, op het pictogram &quot;i&quot; om een snelle beschrijving van de huidige functionaliteit en artikelen die betrekking hebben op toegang, weer te geven.

**Integratie met Adobe Campaign Standard**

Als Adobe Campaign Standard-klant kunt u nu e-mails, pushberichten en SMS verzenden via Journey Optimizer. Gebruik de nieuwe ingebouwde acties om de mogelijkheden van het Overseinen van de Campaign Standard Transactie in Journey Optimizer te gebruiken.  [Meer informatie](../action/acs-action.md)

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
* Met de Batch-beslissings-API kunnen organisaties de functionaliteit offer decisioning gebruiken voor alle profielen in een bepaald segment in één aanroep. De aanbiedingsinhoud voor elke profielen in het segment wordt geplaatst in een AEP dataset waar het voor de werkschema&#39;s van de douanepartij beschikbaar is. [Meer informatie](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Beheer**

* U kunt nu de koppeling voor het afmelden van abonnementen in- of uitschakelen in de e-mailheader op het niveau van de berichtvoorinstelling en een aangepaste URL voor het afmelden van abonnementen instellen op berichtniveau. [Meer informatie](../configuration/message-presets.md#list-unsubscribe)
* De lijst van gewenste personen kan nu worden in- en uitgeschakeld via de [!DNL Journey Optimizer] interface over productie- en niet-productie-sandboxen. [Meer informatie](../configuration/allow-list.md#enable-allow-list)

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
<th><strong>Nieuwe bibliotheek voor persoonlijke expressie</strong><br/></th>
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
