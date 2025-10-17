---
solution: Journey Optimizer
product: journey optimizer
title: Opmerkingen voor de release van Journey Optimizer
description: Opmerkingen bij de release Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 93179c7612eda244e512f8144ca396660a8a7537
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# Opmerkingen voorafgaand aan de release {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle veranderingen worden geconsolideerd aan het eind van elke maand in de [&#x200B; versienota&#39;s &#x200B;](release-notes.md).


## Opmerkingen bij de pre-release oktober 25 {#25-10-rn}

**de pre-versienota&#39;s hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. Koppelingen, schermen en bijgewerkte documentatie worden gepubliceerd in de releaseopmerkingen op de releasedatum.

Zie ook [&#x200B; de pre-versienota&#39;s van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

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
<p>U kunt stille uren toepassen via regelsets, die u kunt toewijzen aan afzonderlijke acties in campagnes of reizen voor een nauwkeurige controle. Deze processen stroomlijnen.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Controle en rapportage van aangepaste acties</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Deze mogelijkheid biedt een betere zichtbaarheid in de gezondheid en uitvoering van de reis, inclusief levenscyclusstatus en prestatiewaarschuwingen. U kunt nu snel begrijpen wanneer, waar en waarom een afwijkende situatie zich voordoet in een aangepaste handeling.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

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

<table>
<thead>
<tr>
<th><strong>Nieuwe API om actiecampagnes op te halen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Er is nu een nieuwe Journey Optimizer API beschikbaar, waarmee u campagnegerelateerde gegevens zoals details, versies en configuraties via programmacode kunt ophalen en inspecteren.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nieuwe bronconnectors voor loyaliteitstoepassingen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nieuwe bronschakelaars zijn nu beschikbaar in Adobe Experience Platform voor de Talon.One, Capillary en Kobie loyaliteitApps. Met deze connectors kunt u naadloos loyaliteitsgegevens streamen naar Adobe Experience Platform en deze gegevens benutten in Journey Optimizer.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ondersteuning voor besluitvorming in e-mailkanaal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu beleidsregels voor beslissingen toevoegen aan e-mailreizen en -campagnes. Beslissingsbeleid is containers voor uw aanbiedingen die de beslissingsengine gebruiken om dynamisch de beste inhoud te retourneren die voor elk publiekslid kan worden geleverd.</p>
<p> Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modus voor hoge doorvoer voor door API geïnitieerde e-mailcampagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Er is nu een nieuwe modus voor hoge doorvoer beschikbaar in door de API geïnitieerde campagnes. Deze wijze wordt ontworpen voor grootschalig, in real time overseinen (tot 5000 transacties per seconde) en verstrekt hogere beschikbaarheid met lagere latentie.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor het e-mailkanaal, voor organisaties die de invoegtoepassing voor transactiemeldingen met hoge Adobe-doorvoer hebben aangeschaft. Neem contact op met uw Adobe-vertegenwoordiger voor meer informatie.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
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
<li><a href="../reports/alerts.md#alert-profile-error-rate"> het Tarief van de Fout van het Profiel overtrok </a>: Verhouding van profiel-in-fout aan ingegaan profielen over de laatste 5 minuten overschrijdt drempel</li>.</ul> <p>U kunt drempelwaarden wijzigen en u kunt zich abonneren op individuele waarschuwingen op het niveau van de reis ten opzichte van de rest van de wereld.</p>
<p>Voor meer informatie, verwijs naar de <a href="../reports/alerts.md"> gedetailleerde documentatie </a></p>
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
<p>Voor meer informatie, verwijs naar de <a href="../personalization/functions/helpers.md#execution-metadata"> gedetailleerde documentatie </a></p>
<p>Beschikbaarheidsdatum: 13 oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentenagent is hier!</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aangedreven door <a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator.html" target="_blank"> Adobe Experience Platform Agent Orchestrator </a>, is de Agent van de Experimentatie beschikbaar in Journey Optimizer. </p>
<p>De Experimentation Agent is een door AI aangedreven hulpmiddel dat moderniseert hoe u digitale experimenten over websites, e-mails, pushberichten, en toepassingen kunt in werking stellen en beheren. Het helpt u experimenten efficiënter in werking stellen, bedrijfsdoelstellingen organiseren, en actionable inzichten produceren, benadrukkend wat werkte, wat niet, en waar te om daarna te experimenteren.</p>
<p>Voor meer informatie, verwijs naar de <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html" target="_blank"> gedetailleerde documentatie </a></p>
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
<p>Voor meer informatie, verwijs naar de <a href="../email/pdf-attachments.md"> gedetailleerde documentatie </a></p>
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


### Verbeteringen

**Uitgezochte herbruikbare regels in het richten**

U kunt nu hefboomwerking de regelbouwer wanneer het gebruiken van het richten van regels met de eigenschap van de Optimalisering van het Bericht in reizen en campagnes. <!-- [Read more](../FILE.md) -->

**gebied van de Uitvoering voor het Kanaal WhatsApp**

Naast E-mail en SMS is het nu mogelijk om het standaarduitvoeringsveld WhatsApp bij te werken. Het is ook mogelijk om het uitvoeringsgebied met voeten te treden dat globaal in de WhatsApp reisactiviteit geavanceerde parameters of in de WhatsApp kanaalconfiguratie wordt geplaatst. <!-- [Read more](../FILE.md) -->

**de kenmerkensteun van de Douane voor (unsubscribe) adres Mailto**

Als u met Journey Optimizer toestemming buiten Adobe beheert, kunt u externe aangepaste eindpunten instellen door uw eigen koppeling voor het uit-schrijven van abonnementen met één klik te definiëren en een aangepast e-mailadres voor het afmelden van abonnementen in de e-mailconfiguratie. Wanneer uw ontvangers op de koppeling voor afmelden klikken, voegt Journey Optimizer enkele standaardprofielspecifieke parameters toe aan de gebeurtenis voor het bijwerken van de toestemming.

Als u uw aangepaste eindpunten verder wilt aanpassen, kunt u nu aangepaste kenmerken definiëren die ook aan de gebeurtenis permission worden toegevoegd. [Meer informatie](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Deze mogelijkheid is al beschikbaar voor de aangepaste versie **[!UICONTROL One-click Unsubscribe URL]** sinds augustus 1995 en wordt nu vrijgegeven voor de optie **[!UICONTROL Mailto (unsubscribe)]** in Beperkte beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

Beschikbaarheidsdatum: 6 oktober 2025