---
solution: Journey Optimizer
product: journey optimizer
title: Release-aantekeningen 2024
description: Opmerkingen bij de release van Journey Optimizer 2024
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: bae533c5-1bfc-48bf-9f8d-1145383c040c
source-git-commit: d0fa6d9f3a5d61310e8d072513b199e513a66138
workflow-type: tm+mt
source-wordcount: '1582'
ht-degree: 7%

---

# Aanvullende informatie 2024 {#release-notes-2024}

Deze pagina bevat alle functies en verbeteringen voor [!DNL Journey Optimizer] vrijgegeven in 2024.


## Opmerkingen bij de release van april 2024 {#apr-2024}

**Releasedatum** 2 mei 2024

### Nieuwe functies {#apr-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden beschreven.

<table>
<thead>
<tr>
<th><strong>Multimedia Message Service (MMS) - alle providers</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met het Kanaal van SMS, kunt u uw mededeling nu verbeteren door de MMS-berichten (Multimedia Message Service) te verzenden, toelatend het delen van beelden, GIFFEN, of video's met uw klanten. In eerste instantie alleen beschikbaar bij Sinch, is MMS nu ook beschikbaar bij Infobip en Twilio.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verbeterde Journey Designer en live rapportering</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Deze release wordt geleverd met een verbeterde gebruikersinterface voor het canvas voor reizen en biedt een intuïtievere en efficiëntere gebruikerservaring. De activiteiten zijn duidelijker en geven meer informatie over het reiscanvas met minder kliks.</p>
<img src="assets/new-canvas3.gif"/>
<p>Naast het verbeterde ontwerp van het reiscanvas introduceren we de mogelijkheid om de laatste 24 uur metriek direct in het reiscanvas te zien. </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong>Opmerking</strong>: Deze wijzigingen worden geleidelijk doorgevoerd in alle omgevingen vanaf de release van april.</p>
<p>Raadpleeg de <a href="new-canvas.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Verbeteringen {#apr-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Configuratie**

* U kunt nu een marketingactie op het niveau van het kanaaloppervlak selecteren. Bij gebruik op een oppervlak worden alle toestemmingsbeleidsregels die aan die marketingactie zijn gekoppeld, benut om de voorkeuren van uw klanten te respecteren. [Meer informatie](../action/consent.md#surface-marketing-actions)
* Het gebruik van Toegangsbeheer op objectniveau is nu beschikbaar voor kanaaloppervlakken. [Meer informatie](../configuration/channel-surfaces.md#create-channel-surface)
* Terwijl het toelaten van lijst unsubscribe in een kanaaloppervlakte, kunt u het toestemmingsniveau nu bepalen om zich aan te sluiten bij hoe u toestemming van alle andere bronnen beheert. [Meer informatie](../email/email-settings.md#list-unsubscribe)

**Inhoudsbeheer**

* U kunt nu inhoudssjablonen voor alle kanalen simuleren. [Meer informatie](../content-management/content-templates.md#test-templates)

**Personalisatie**

* De nieuwe **toInt** hulpfunctie is beschikbaar in de Redacteur van de Uitdrukking. U kunt elk van deze typen (getal, dubbel, int, lang, zwevend, kort, byte, boolean, tekenreeks) omzetten in een geheel getal. [Meer informatie](../personalization/functions/math.md#to-int)



## Opmerkingen bij de release maart 2024 {#mar-2024}

**Releasedatum**: 19-20 maart 2024

### Nieuwe functie {#mar-features}

Met deze release wordt de nieuwe functionaliteit hieronder beschreven.

<table>
<thead>
<tr>
<th><strong>Ervaringen op basis van code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met het nieuwe op code-gebaseerde ervaringskanaal, staat Adobe Journey Optimizer u toe om geavanceerde verpersoonlijking en het testen voor om het even welk van uw binnenkomende eigenschappen te doen, toelatend naadloze levering van op maat gemaakte ervaringen over diverse aanraakpunten zoals Web apps, mobiele apps, Desktop apps, videoconsoles, TV aangesloten apparaten, slimme TVs, kiosken, ATMs, IoT apparaten, en meer.</p>
<P>De belangrijkste mogelijkheden omvatten:</p>
<ul><li> Universele verpersoonlijking: vergroot persoonlijke ervaringen op alle aanraakpunten, zodat een samenhangende en op maat gesneden gebruikersreis mogelijk is</li>
<li>Precisie voor bewerking in korrels: bewerk specifieke inhoud op afzonderlijke locaties in uw apps of webpagina's</li>
<li>Veelzijdige implementatie: ondersteuning voor implementatiemethoden die zijn gebaseerd op servers, API's of SDK's, zodat deze naadloos kunnen worden geïntegreerd met uw ontwikkelomgeving.</li></ul></p>
<p>Raadpleeg de <a href="../code-based/get-started-code-based.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/code-based.gif"> 
</tr>
</tbody>
</table>

### Verbeteringen {#mar-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Contentsjablonen**

* **Miniaturen** - A **Rasterweergave** De modus is nu beschikbaar voor inhoudssjablonen en geeft miniaturen weer voor verbeterde visuele toegang. Momenteel worden alleen e-mailsjablonen ondersteund. [Meer informatie](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Dit vermogen wordt vrijgegeven in Beperkte Beschikbaarheid (LA) voor een kleine reeks klanten.

**Reizen**

Er zijn nieuwe tussenliggende statussen toegevoegd aan de levenscyclus van de reisontwerpfase:

* **Publiceren** tussen de **Concept** en de **Live** status
* **Stoppen** tussen de **Live** en de **Gestopt** status
* **Testmodus activeren** of **Deactivering van de testmodus** statussen tussen de **Concept** en de **Concept (test)** status

Wanneer een reis in een tussenstadium is, is het read-only. [Meer informatie](../building-journeys/journey-gs.md#filter)

## Opmerkingen bij de release februari 2024 {#feb-2024}

**Releasedatum**: 21 februari 2024

### Nieuwe functies{#feb-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.


<table>
<thead>
<tr>
<th><strong>Webberichten in de app</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt het nieuwe Web in-App overseinenvermogen nu gebruiken om gepersonaliseerde inhoud direct op websites, door modaal-bekledingsberichten te tonen. Met deze functie kunt u effectief contact opnemen met webbezoekers, waardoor de interactie, het behoud en de conversiesnelheden van gebruikers worden verbeterd.<br/><br/></p>
<p>Raadpleeg de <a href="../in-app/create-in-app-web.md">gedetailleerde documentatie</a> voor meer informatie.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Sjablonen voor multikanaalsinhoud</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Naast E-mail, zijn de inhoudsmalplaatjes nu beschikbaar voor de volgende kanalen: Duw, In-app, SMS en Directe post, elk kanaal dat specifieke malplaatjetypes heeft. Voor E-mail, kunt u het inhoudstype nu selecteren, dat u toestaat om de onderwerpregel als deel van uw e-mailmalplaatje te bewaren. <br/><br/></p>
<p>Raadpleeg de <a href="../content-management/content-templates.md">gedetailleerde documentatie</a> voor meer informatie.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif"> 
</tr>
</tbody>
</table>


### Verbeteringen {#feb-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Doelgroepen**

* **Zaadlijsten** - Varianten worden nu ondersteund bij gebruik **zaadlijsten**. De zaadadressen ontvangen een exemplaar van alle varianten van het zelfde bericht (zoals de verschillende behandelingen van een inhoudexperiment). [Meer informatie](../configuration/seed-lists.md)

Eerder beschikbaar als Beta, zijn de volgende verbeteringen nu beschikbaar aan alle gebruikers:

* U kunt nu **publiek gemaakt via publiekscompositie** en verrijkingskenmerken gebruiken in Reizen. [Meer informatie](../building-journeys/read-audience.md)

* U kunt nu **publiek geüpload uit een CSV-bestand** in reizen en campagnes. [Meer informatie](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* Het gebruik van soorten publiek en kenmerken van de compositie van het publiek en aangepaste upload (CSV-bestand) is momenteel niet beschikbaar voor gebruik met het gezondheidsschild of het privacyschild.
  >* De **publiek uploaden uit een CSV-bestand** de verbetering wordt geleidelijk doorgevoerd in de loop van enkele dagen na de eerste introductie . Terwijl sommige gebruikers directe toegang hebben, kunnen anderen een vertraging ervaren alvorens het in hun milieu beschikbaar wordt.

**Reizen**

* **Uw reizen filteren** - U kunt nu **aangepaste datums om de reizen te filteren** voorraad, naast de bestaande vooraf gedefinieerde datumfilters. Op deze manier kunt u de lijst verfijnen door ritten weer te geven die op een bepaalde datum zijn gemaakt of gepubliceerd, binnen een bepaalde maand, gedurende een heel jaar of binnen een opgegeven tijdbereik. [Meer informatie](../building-journeys/journey-gs.md#filter)
* **Aangepaste acties** - U kunt nu het dialoogvenster **inhoudstype** header. Deze nieuwe **inhoudstype** verwijst naar JSON-inhoud. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)
* **Configuratie** - Het attribuut identityMap in stepEvents is nu voorgevuld. De primaire identiteit wordt gedefinieerd als &quot;primary = true&quot;. [Meer informatie](../reports/sharing-field-list.md)
* **Gebruikersinterface** - De bovenste balk, in reisschermen, is gereorganiseerd voor een betere ervaring. Onder de verschillende updates ziet u dat het potlood-pictogram waarmee u de reiseigenschappen kunt openen nu links van de bovenste balk naast de naam van de rit wordt weergegeven. [Meer informatie](../building-journeys/journey-gs.md#change-properties)

**Sms-kanaal**

* **Trefwoorden voor aanmelden/uitschakelen** - Wanneer u uw SMS-kanaal configureert, kunt u nu het **Trefwoorden voor Inschakelen en Uitschakelen** volgens uw voorkeuren. Journey Optimizer activeert de reactie op basis van deze opgegeven trefwoorden. [Meer informatie](../sms/sms-configuration.md)

**Campagnes**

* **API-gestuurde campagnes** - De cURL-code die is gegenereerd na het activeren van een API-geactiveerde campagne is verbeterd. Het omvat nu alle personaliseringsvariabelen (profiel en context) die in het bericht worden gebruikt. [Meer informatie](../campaigns/api-triggered-campaigns.md#execute)

**Frequentieregels**

* Naast E-mail en Duw, kunt u de regels van de Frequentie voor SMS en Directe kanalen van de Post nu tot stand brengen. De frequentieregels sluiten over-gevraagde profielen automatisch uit van berichten en acties wanneer de frequentiedrempel wordt bereikt. [Meer informatie](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## Opmerkingen bij de release januari 2024 {#jan-2024}

**Releasedatum**: 30-31 januari 2024

### Nieuwe functies{#jan24-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.

<table>
<thead>
<tr>
<th><strong>Updates van de leverbaarheid</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ondersteunt nu de DMARC-verificatietechnologie.</p>
<p>Vanaf 1 februari 2024, Google en Yahoo! vereisen dat u een DMARC-record hebt voor elk domein dat u gebruikt om e-mail naar hen te verzenden. Zorg ervoor dat u DMARC- verslag opstelling voor alle subdomeinen hebt hebt die u of aan Adobe in Journey Optimizer hebt gedelegeerd.</p>
<p>Raadpleeg de <a href="../configuration/dmarc-record-update.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Playbooks voor gebruiksscenario</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gebruik een catalogus met branchespecifieke gebruiksscenario's voor afspeelboeken in Real-Time CDP en Journey Optimizer om veelvoorkomende gebruikssituaties aan te pakken die u kunt uitvoeren met Adobe Experience Platform en Adobe Journey Optimizer.</p><p>Zodra u playbook hebt gekozen die het best aan uw behoeften past, kunt u het toelaten om de activa te produceren nodig om uw gebruikscase zoals reizen, berichten, schema's of segmenten te steunen, en hen aan uw schema voor snellere tijd aan waarde aan te passen.</p>
<p>Raadpleeg de <a href="../start/playbooks.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Verbeteringen {#jan24-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Rapportage**

* **Nieuwe op domein gebaseerde widgets voor indeling** - Er zijn nieuwe widgets toegevoegd om uw campagne- en journalistieke rapporten te verbeteren. De **Bounce Reden per domein**, **Verzonden en geleverd op domeinen**, **Opent en klikt op domein** en **Stuiteren en fouten per domein** widgets bieden een gedetailleerde uitsplitsing op domeinniveau voor belangrijke gegevens voor het verzenden van e-mail en het bijhouden van gegevens. [Meer informatie](../reports/channel-report.md)

**SMS-kanaal**

* **Dubbele plug-in** - De dubbele Opt-In workflow voor SMS garandeert dat gebruikers zich expliciet aanmelden om berichten te ontvangen wanneer het verzoek van hun apparaat wordt geïnitieerd. Gebruikers starten het goedkeuringsproces door een binnenkomend SMS-bericht te verzenden. Na bevestiging van hun toestemming wordt een vervolgbericht verzonden waarin om een definitieve verificatie wordt verzocht. Als een gebruikersprofiel niet bestaat, wordt het gecreeerd na succesvolle bevestiging. [Meer informatie](../sms/sms-configuration.md)

  Merk op dat dit vermogen met de leveranciers van SMS van Sinch en Infobip beschikbaar is.

**Reizen**

* **Duur van reactiegebeurtenissen** - De maximale duur die u kunt definiëren in het dialoogvenster **Gebeurtenissen van Reaction** is nu 29 dagen in plaats van 30. [Meer informatie](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Lees publiek**  - de **Publiek lezen** De activiteit baseert zich nu op de dataset van de profielmomentopname voor partijsegmenten, die slechts eenmaal per dag wordt geproduceerd nadat de geplande dagelijkse partijbaan in werking wordt gesteld, vandaar zullen de gegevens tot die laatste dagelijkse partijbaan vers zijn. [Meer informatie](../building-journeys/read-audience.md)

* **Veldgroepen** - Deze release verhelpt een probleem dat ervoor zorgde dat Veldgroepen in bepaalde gevallen niet konden worden opgeslagen.

* Steun voor `<listObject>` is gewijzigd in meerdere functies.

**Frequentieregels**

* **Wekelijkse frequentie** - U kunt nu het maximumaantal berichten dat naar een klantprofiel wordt verzonden per week, plus de maand specificeren. De maximale frequentie is gebaseerd op de geselecteerde kalenderperiode en wordt opnieuw ingesteld aan het begin van het corresponderende tijdkader. [Meer informatie](../configuration/frequency-rules.md#create-new-rule)

  >[!NOTE]
  >
  >Dagelijkse frequentiegrens is ook beschikbaar op verzoek. Neem contact op met uw Adobe.

**Beslissingsbeheer**

* **Frequentiecorrectie op rand** - De teller van de frequentiecappend wordt nu bijgewerkt en beschikbaar in een besluit van de Beslissing API van de Rand in minder dan 3 seconden. [Meer informatie](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
