---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f69e482daf457f1c331d158d1bf04b4cfb392197
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 6%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** levert onophoudelijk nieuwe eigenschappen, verhogingen aan bestaande eigenschappen, en insectenmoeilijke situaties. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] volgt een doorlopend leveringsmodel, dat Adobe in staat stelt voortdurend nieuwe functies, verbeteringen en correcties te leveren. Deze benadering maakt een schaalbare, gefaseerde implementatie van mogelijkheden mogelijk om prestaties en stabiliteit in alle omgevingen te garanderen.

Vanwege dit model worden releaseopmerkingen bijgewerkt tussen maandelijkse releases.  Een specifieke [ Recentste updates ](#updates-rn) sectie benadrukt nieuwe mogelijkheden en verbeteringen aangezien zij aan productie-zodat wordt opgesteld u altijd op de hoogte gebracht van alle veranderingen in echt - tijd. <!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

[!DNL Adobe Journey Optimizer] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

## Opmerkingen bij de release van oktober 1925 {#oct-25-10-rn}

**de datum van de Versie**: 22 oktober, 2025

### Nieuwe functies {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>Quiet-uren/uitsluitingen op basis van tijd</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met stille uren kunt u op tijd gebaseerde uitsluitingen definiëren voor e-mail-, SMS-, push- en WhatsApp-kanalen. Zij zorgen ervoor dat geen berichten tijdens specifieke periodes worden verzonden, die u helpen klantenvoorkeur en nalevingsvereisten respecteren.</p>
<p>U kunt stille uren toepassen via regelsets, die u kunt toewijzen aan afzonderlijke acties in campagnes of reizen voor een nauwkeurige controle.</p>
<p>De regels voor de korte uren zijn momenteel alleen beschikbaar voor een aantal organisaties (Beperkte Beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger om aan de wachtlijst toe te voegen.</p>
<img src="assets/do-not-localize/quiet-hour.gif">
<p>Raadpleeg de <a href="../conflict-prioritization/quiet-hours.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 22 oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new Journey Optimizer API is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
<p>For more information, refer to the <a href="../start/get-started-sources.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table>-->

<!--table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>High throughput messaging for API triggered email campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new high throughput transactional messaging mode is available in API triggered campaigns. This mode is designed for large-scale, real-time transactional messaging and supports up to 5,000 transactions per second with higher availability. This mode also supports transactional messages without referencing or creating customer profiles, such as guest checkout, order confirmation, password resets, security notifications, and one-time passwords for two-factor authentication.</p>
<p>This capability is only available for the email channel, for organizations that have purchased the Adobe High Throughput Transactional Messaging add-on offering. Contact your Adobe representative for more details.</p>
<p>For more information, refer to the <a href="../campaigns/api-triggered-campaign-action.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Herbruikbare richtingsregels</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Om u tijd en moeite te besparen, staat Journey Optimizer u nu toe om herbruikbare regels van een specifiek menu van UI tot stand te brengen en hen te gebruiken wanneer het bouwen van het richten, of als deel van inhoud Optimization in een campagne of een reis, of in Optimize reisactiviteit.</p>
<p>De gerichte regels zijn momenteel in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang. Houd er rekening mee dat deze mogelijkheid alleen beschikbaar is voor organisaties die de invoegtoepassing voor besluiten hebben aangeschaft. Het zal geleidelijk aan aan alle klanten worden uitgevoerd.</p>
<img src="assets/do-not-localize/targeting-rules.gif">
<p>Raadpleeg de <a href="../experience-decisioning/rules.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 22 oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nieuwe reiswaarschuwingen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nieuwe vooraf geconfigureerde waarschuwingen zijn beschikbaar om de uitvoering van de reis te controleren:</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate"> Profiel verwerpt Tarief dat </a> wordt overschreden: Verhouding van profielteruggooi naar ingegaan profielen over de laatste 5 minuten overschrijdt drempel</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate"> het Tarief van de Fout van de Actie van de Douane overtrok </a>: Verhouding van de fouten van de douaneactie aan succesvolle vraag van HTTP over de laatste 5 minuten overschrijdt drempel</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate"> het Tarief van de Fout van het Profiel overtrok </a>: Verhouding van profiel-in-fout aan ingegaan profielen over de laatste 5 minuten overschrijdt drempel.</li></ul> <p>U kunt drempelwaarden wijzigen en u kunt zich abonneren op individuele waarschuwingen op het niveau van de reis ten opzichte van de rest van de wereld.</p>
<p>Raadpleeg de <a href="../reports/alerts.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 14 oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Help voor metagegevens van uitvoering</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Een nieuwe hulpfunctie 'executeMetadata' is beschikbaar in de verpersoonlijkingsredacteur. Hiermee kunt u contextuele informatie toevoegen aan elke native actie en deze vastleggen in een gegevensset voor export naar externe systemen.</p>
<p>Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<img src="assets/do-not-localize/execution-metadata.gif">
<p>Raadpleeg de <a href="../personalization/functions/helpers.md#execution-metadata">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 13 oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentation Accelerator met Experimentation Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator beschikt nu over de Experimentation Agent, een door AI aangedreven, conversationele tool waarmee u kunt communiceren met uw experimenten, inzichten en mogelijkheden. Het verbetert de ervaring van Journey Optimizer Experimentation Accelerator, helpt u efficiënter experimenten in werking te stellen, te ontdekken wat werkt, en te ontdekken waar te om daarna te optimaliseren.</p>
<p>Raadpleeg de <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html" target="_blank">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 10 oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>PDF-bijlagen bij e-mailberichten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu een statisch PDF-bestand toevoegen aan een e-mailbericht dat met Journey Optimizer is verzonden.</p>
<ul>
<li>U kunt maximaal zes berichten verzenden met een PDF-bijlage per profiel per jaar.</li>
<li>De maximaal toegestane bestandsgrootte voor elke bijlage is 5 MB.</li>
<li>Voor elke extra grootte of elk ander volume kunt u de invoegtoepassing PDF-bijlagen aanschaffen. Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.</li>
</ul>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Raadpleeg de <a href="../email/pdf-attachments.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 30 september 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Openbare API om reizen op te halen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Er is nu een nieuwe Journey Optimizer API beschikbaar voor het ophalen van reizen en de bijbehorende objecten, zoals campagnes en oppervlakken.</p>
<p>Voor meer informatie, verwijs naar de <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/"> gedetailleerde documentatie </a></p>
<p>Beschikbaarheidsdatum: 25 september 2025</p>
</td>
</tr>
</tbody>
</table>

<!--
## Latest updates {#updates-rn}

New capabilities and improvements released in the past weeks are listed below, with their availability date. They will be grouped with the next release notes content at the end of the month. See also the latest [release notes below](#latest-rn).
-->

### Verbeteringen {#updates-improvements}

<!--Availability date: October 22, 2025-->

**gebied van de Uitvoering voor het Kanaal WhatsApp**

Naast e-mail en SMS, kunt u het standaard uitvoeringsgebied voor uw leveringen WhatsApp op het zandbakniveau weten bij te werken. Het is ook mogelijk om het uitvoeringsgebied met voeten te treden dat globaal door het in de WhatsApp reisactiviteit geavanceerde parameters of in de WhatsApp kanaalconfiguratie wordt geplaatst te veranderen. [Meer informatie](../configuration/primary-email-addresses.md)

Beschikbaarheidsdatum: 22 oktober 2025

**de kenmerkensteun van de Douane voor (unsubscribe) adres Mailto**

Als u met Journey Optimizer toestemming buiten Adobe beheert, kunt u externe aangepaste eindpunten instellen door uw eigen koppeling voor het uit-schrijven van abonnementen met één klik te definiëren en een aangepast e-mailadres voor het afmelden van abonnementen in de e-mailconfiguratie. Wanneer uw ontvangers op de koppeling voor afmelden klikken, voegt Journey Optimizer enkele standaardprofielspecifieke parameters toe aan de gebeurtenis voor het bijwerken van de toestemming.

Als u uw aangepaste eindpunten verder wilt aanpassen, kunt u nu aangepaste kenmerken definiëren die ook aan de gebeurtenis permission worden toegevoegd. [Meer informatie](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Deze mogelijkheid is al beschikbaar voor de aangepaste versie **[!UICONTROL One-click Unsubscribe URL]** sinds augustus 1995 en wordt nu vrijgegeven voor de optie **[!UICONTROL Mailto (unsubscribe)]** in Beperkte beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

Beschikbaarheidsdatum: 6 oktober 2025

### Binnenkort beschikbaar {#oct-25-10-soon}

In de komende dagen zijn de volgende mogelijkheden en verbeteringen gepland voor release. **de Informatie is onderworpen aan verandering**. De bijgewerkte verbindingen, de schermen, en de documentatie zullen worden gedeeld zodra deze updates in productie levend zijn.

### Nieuwe functies {#oct-25-10-soon-features}

<table>
<thead>
<tr>
<th><strong>Thema's in de Designer-e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu snel vooraf goedgekeurde thema's toepassen om de consistentie van uw merk in alle e-mails te garanderen, het aanmaakproces van uw campagne te versnellen en onafhankelijk e-mails van hoge kwaliteit te produceren en de afhankelijkheid van ontwerpteams te verminderen.</p>
<p>Eerder in bètaversie is deze mogelijkheid nu beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<!--img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p>Availability date: November 4, 2025</p-->
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#oct-25-10-soon-improvements}

**Beslissing in e-mail door AI modellen**

U kunt nu AI-modellen gebruiken om de beste inhoud in uw e-mail te optimaliseren door Beslissing te gebruiken. Met deze functie kunt u bijvoorbeeld de beste inhoud aanbieden op basis van aangepaste gebeurtenissen zoals Aankopen, Knopklikken, Toevoegen aan winkelwagentje, enz.

<!--
<table>
<thead>
<tr>
<th><strong>New Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports Web Push notifications, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app.</p>
<p>This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Custom action monitoring and reporting is now available. This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary, and Kobie loyalty apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>
-->
