---
solution: Journey Optimizer
product: journey optimizer
title: Opmerkingen voor de release van Journey Optimizer
description: Opmerkingen bij de release Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1a5f6be689c9e91ee0dc0b5f024dbe8020424337
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 0%

---

# Opmerkingen voorafgaand aan de release {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle veranderingen worden geconsolideerd aan het eind van elke maand in de [&#x200B; versienota&#39;s &#x200B;](release-notes.md).


## Opmerkingen bij de pre-release oktober 25 {#25-10-rn}

**de pre-versienota&#39;s hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. Koppelingen, schermen en bijgewerkte documentatie worden gepubliceerd in de releaseopmerkingen op de releasedatum.

Zie ook [&#x200B; de pre-versienota&#39;s van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**de datum van de Versie**: Oktober 21-22, 2025

### Nieuwe functies {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail-kanaal op reis</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct Mail Channel, dat voorheen beperkt was tot Campagnes, is nu beschikbaar op het reiscanvas, zodat u Direct Mail in uw reizen kunt opnemen. Directe post kan nu in zowel partij als 1:1 reisscenario's, met steun voor de configuratie van de dossierextractie en op tijd-gebaseerde frequentiemontages worden gebruikt.</p>
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

<table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met het nieuwe Basistoe:voegen-op aanbod RCS, kunt u basisCommunicatie van de Diensten (RCS) overseinen in Journey Optimizer nu leveren, toelatend de volgende verbeterde overseinenmogelijkheden afhankelijk van leverancier en geografische steun:</p>
<ul>
<li><strong> Brandde en geverifieerde afzendersteun:</strong> verzend berichten gebruikend geverifieerde bedrijfsprofielen met branding elementen (embleem, afzendernaam, enz.).</li>
<li><strong> de leveringsinzichten van het Bericht:</strong> ontvang gedetailleerde leveringsrapporten met inbegrip van de updates van de berichtstatus (b.v., verzonden, geleverd, gelezen).</li>
<li><strong> het volgen van de Verbinding:</strong> bedt en volgt URLs binnen RCS- berichten voor betrokkenheidsanalyses in.</li>
<li><strong> Fallback aan SMS:</strong> Automatische fallback aan SMS wanneer het apparaat van de ontvanger geen RCS steunt of tijdelijk onbereikbaar via RCS is.</li>
<li><strong> Basisberichtsamenstelling:</strong> verzendt basis op tekst-gebaseerde RCS- berichten.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct mail kanaal in geordende campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail kanaal is nu beschikbaar in georkestreerde campagnes. De direct-mailactiviteit vergemakkelijkt direct mail verzenden binnen uw Geordende campagne, voor zowel eenmalige als terugkomende berichten. Hiermee wordt het genereren van het extractiebestand geautomatiseerd dat is vereist door directe-mailproviders. U kunt kanaalactiviteiten in het Geordende campagnecanvas combineren om kanaalcampagnes tot stand te brengen die acties kunnen teweegbrengen die op klantengedrag en gegevens worden gebaseerd.</p>
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
<th><strong>Nieuwe functie Metagegevens van uitvoering</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Een nieuwe hulpfunctie van executeMetadata is beschikbaar in de verpersoonlijkingsredacteur. Hiermee kunt u contextuele informatie toevoegen aan elke native actie en deze vastleggen in een gegevensset voor export naar externe systemen.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Beschikbaarheidsdatum: 13 oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De Experimentation Agent is een door AI aangedreven hulpmiddel dat moderniseert hoe u digitale experimenten over websites, e-mails, pushberichten, en toepassingen kunt in werking stellen en beheren. De Experimentation Agent is gebaseerd op Adobe Experience Platform AI-platform en experimentatiegereedschappen en helpt u om experimenten efficiënter uit te voeren, bedrijfsdoelstellingen te ordenen en inzichten te genereren die uitvoerbaar zijn, te benadrukken wat werkte, wat niet en waar vervolgens te experimenteren.</p>
<p>Als onderdeel van de nieuwe Experimentation Accelerator-functie levert de agent:</p>
<ul>
<li><strong> Prestaties:</strong> een duidelijke mening van wat in het experiment gebeurde</li>
<li><strong> Inzichten:</strong> een verklaring waarom de resultaten voorkwamen</li>
<li><strong> Kansen:</strong> begeleiding op de volgende te nemen acties</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Beschikbaarheidsdatum: 9 oktober 2025</p>
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
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Beschikbaarheidsdatum: 25 september 2025</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

- **campagnes, Ervaring Beslissing, Schavens**
   - **Uitgezochte herbruikbare regels in het richten** - u kunt hefboomwerking de regelbouwer nu wanneer het gebruiken van het richten van regels met de eigenschap van de Optimalisering van het Bericht in reizen en campagnes. <!-- [Read more](../FILE.md) -->

- **Kanaal - WhatsApp**
   - **gebied van de Uitvoering voor het Kanaal WhatsApp** - naast E-mail en SMS, is het nu mogelijk om het standaard uitvoeringsgebied bij te werken WhatsApp. Het is ook mogelijk om het uitvoeringsgebied met voeten te treden dat globaal in de WhatsApp reisactiviteit geavanceerde parameters of in de WhatsApp kanaalconfiguratie wordt geplaatst. <!-- [Read more](../FILE.md) -->

- **Toestemmingen**
   - **Reis/de schepper van de Campagne zou niet** moeten kunnen goedkeuren - toegevoegde een optie wanneer het creëren van of het plaatsen van het Beleid van de Goedkeuring om de scheppers van de Reis/van de Campagne te verhinderen hun eigen voorwerpen goed te keuren. <!-- [Read more](../FILE.md) -->

- **Kanaal - duw**
   - **Mobiele Levende Activiteiten - Privé bèta** - De Levende Activiteiten verstrekken updates in real time en interactieve ervaringen binnen mobiele apps, die gebruikers toestaan om over aan de gang zijnde gebeurtenissen of taken direct op het scherm van hun apparaat te blijven. Deze functie verbetert de betrokkenheid door live-informatie te leveren, zoals voortgangscontrole, updates van gebeurtenissen of interactieve inhoud, zonder dat gebruikers de app hoeven te openen. <!-- [Read more](../FILE.md) -->

- **Reizen**
   - **Nieuwe Alarm van de Reis** - de datum van Beschikbaarheid: 14 oktober, 2025
Er zijn nieuwe vooraf geconfigureerde waarschuwingen beschikbaar voor reizen: het percentage verwijderde profielgegevens is overschreden (de verhouding tussen de verwijderde profielprofielen en de ingevoerde profielen is overschreden gedurende de laatste 5 minuten), het foutenpercentage voor aangepaste acties is overschreden (de verhouding tussen fouten met aangepaste handelingen en geslaagde HTTP-oproepen in de afgelopen 5 minuten is overschreden), het foutenpercentage van het profiel is overschreden (de verhouding tussen de ingevoerde profielen in de laatste 5 minuten is overschreden). <!-- [Read more](../FILE.md) -->

- **Configuratie**
   - **de kenmerkensteun van de Douane met Één-Klik unsubscribe URL** - de datum van de Beschikbaarheid: 6 Oktober, 2025
Met Journey Optimizer, als u toestemming buiten Adobe beheert, kunt u een extern douaneeindpunt plaatsen door uw eigen één-klik te bepalen unsubscribe verbinding in de e-mailconfiguratie. Wanneer uw ontvangers op de koppeling voor afmelden klikken, voegt Journey Optimizer enkele standaardprofielspecifieke parameters toe aan de gebeurtenis voor het bijwerken van de toestemming. Als u het e-mailadres voor opzeggen verder wilt aanpassen, kunt u nu aangepaste kenmerken definiëren die worden toegevoegd aan de gebeurtenis permission. Dit vermogen is reeds beschikbaar voor de douane één-klik Unsubscribe URL sinds Augustus 25 en wordt nu vrijgegeven voor de (unsubscribe) optie van de Brievenbus in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang. <!-- [Read more](../FILE.md) -->

- **Kanaal - E-mail**
   - **de gehechtheid van PDF aan e-mail** - de datum van de Beschikbaarheid: 30 september, 2025
U kunt nu een statisch PDF-bestand toevoegen aan een e-mailbericht dat met Journey Optimizer is verzonden. U kunt maximaal 6 berichten verzenden met een PDF-bijlage per profiel per jaar. De maximaal toegestane bestandsgrootte voor elke bijlage is 5 MB. Voor elke extra grootte of elk ander volume kunt u de invoegtoepassing voor PDF-bijlagen aanschaffen. Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

  >[!AVAILABILITY]
  >
  >Eerder uitgebracht in Beperkte Beschikbaarheid, is deze verbetering nu beschikbaar aan alle milieu&#39;s (Algemene Beschikbaarheid).

  <!-- [Read more](../FILE.md) -->

