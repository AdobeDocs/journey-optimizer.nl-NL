---
solution: Journey Optimizer
product: journey optimizer
title: Opmerkingen voor de release van Journey Optimizer
description: Opmerkingen bij de release Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 6326e1e3056f41f1550ac785bcbf83af175b37cc
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# Opmerkingen voorafgaand aan de release {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle veranderingen worden geconsolideerd aan het eind van elke maand in de [ versienota&#39;s ](release-notes.md).

**de Nota&#39;s van de pre hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in de [ versienota&#39;s ](release-notes.md), bij de versiedatum.


## Opmerkingen bij de pre-release augustus &#39;25 {#25-7-rn}

**de Nota&#39;s van de pre hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. Koppelingen, schermen en bijgewerkte documentatie worden gepubliceerd op de releasedatum.

Zie ook [ de pre-versienota&#39;s van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**de datum van de Versie**: 19 augustus, 2025


### Nieuwe functies {#Aug-25-8-features}

<table>
<thead>
<tr>
<th><strong>Reizen onderbreken en hervatten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu uw reizen pauzeren en hervatten. Deze mogelijkheid geeft reisartsen meer controle en flexibiliteit door het tijdelijk stilleggen van de actieve reizen toe te staan zonder de ervaring van de klant te verstoren. Wanneer gepauzeerd, worden geen mededelingen verzonden, en de profielen blijven in een geschorste staat tot de reis wordt hervat.</p>
<p>U kunt slechts één reis pauzeren en hervatten, of bulkpauze uitvoeren en verrichtingen aan een groep reizen hervatten.</p>
<p>Bovendien kunt u algemene filters toepassen op gepauzeerde reizen om profielen uit te sluiten op basis van hun kenmerken.</p>
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Kalenderweergave</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In de lijsten met reizen en campagnes is nu een kalenderweergave beschikbaar. Hiermee kunt u alle reizen en campagnes in de respectieve lijsten visualiseren.</p>
<p>Eerder beschikbaar in Beperkte Beschikbaarheid, is deze eigenschap nu beschikbaar aan alle milieu's. Met deze algemene beschikbaarheidsrelease omvat deze functie:</p>
<ul>
<li>Ontwerpverbeteringen voor de navigatie in datums</li>
<li>De mogelijkheid om conceptiecampagnes weer te geven als u een begin- en einddatum hebt ingesteld</li>
<li>Een nieuwe instelling voor het verbergen en weergeven van kalenderitems die lange tijd worden uitgevoerd</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Donkere modus in de Designer-e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De Journey Optimizer Email Designer biedt nu de mogelijkheid om over te schakelen naar de weergave in de donkere modus, waar u bovendien specifieke aangepaste instellingen kunt definiëren die alleen worden weergegeven voor ontvangers die hun e-mails in de donkere modus lezen.</p>
<p>Let op het volgende:</p>
<ul>
<li>De uiteindelijke rendering in de donkere modus kan variëren en is afhankelijk van de e-mailclient van de ontvanger.</li>
<li>Niet alle e-mailclients ondersteunen de aangepaste donkere modus. Bovendien passen sommige e-mailclients alleen hun eigen standaard donkere modus toe op alle ontvangen e-mails. In beide gevallen kunnen de aangepaste instellingen die u in de e-mailtoepassing hebt gedefinieerd, niet worden weergegeven.</li>
</ul>
<P>Deze mogelijkheid is momenteel beschikbaar in bètaversie en alleen voor bètaklanten. Neem contact op met uw Adobe-vertegenwoordiger als u wilt deelnemen aan het bètaprogramma.</p>
<p><!--img src="assets/do-not-localize/dark-mode.gif"/>--></p>
<p><!--For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Platform-gegevens gebruiken voor personalisatie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gebruik Adobe Experience Platform-gegevens in de personalisatie-editor om uw inhoud aan te passen. Om dit te doen, moeten de datasets nodig voor raadplegingsverpersoonlijking eerst door een API vraag worden toegelaten. Als u klaar bent, kunt u hun gegevens gebruiken om uw inhoud aan te passen aan [!DNL Journey Optimizer] .</p>
<p>Eerder uitgebracht in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's. Met deze algemene release zijn de volgende verbeteringen aangebracht:</p>
<ul>
<li>Ondersteuning van binnenkomende kanalen</li>
<li>De hulpfunctie "datasetLookup" kan nu worden gebruikt binnen expressies en visuele fragmenten om inhoud te personaliseren met behulp van gegevens uit Adobe Experience Platform-gegevenssets,</li>
<li>Een optie in de dataset staat u nu toe om datasets voor raadpleging toe te laten verpersoonlijking, zonder het moeten een API vraag uitvoeren.</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Beslissing in e-mailkanaal gebruiken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu beleidsregels voor beslissingen toevoegen aan e-mailreizen en -campagnes. Beslissingsbeleid is containers voor uw aanbiedingen die de beslissingsengine gebruiken om dynamisch de beste inhoud te retourneren die voor elk publiekslid kan worden geleverd.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aangepaste formulieren op de bestemmingspagina</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Journey Optimizer kunt u nu aangepaste formulieren maken en deze gebruiken in bestemmingspagina's om profielkenmerken vast te leggen in de gegevensset die voor elk formulier is gedefinieerd.</p>
<p>Deze mogelijkheid is momenteel beschikbaar in bètaversie en alleen voor bètaklanten. Neem contact op met uw Adobe-vertegenwoordiger als u wilt deelnemen aan het bètaprogramma.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reisoptimalisatie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer biedt u nu de mogelijkheid om uw reizen te optimaliseren door gebruik te maken van AI- en experimentatiekaders en tegelijk een naadloze bruikbaarheid en differentiatie tussen conditie en optimalisatiefuncties te garanderen.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### Verbeteringen {#Aug-25-8-improv}

De verbeteringen die bij deze release worden geleverd, worden hieronder weergegeven.


- **Campagnes**
   - **controle van het Tarief in uitgaande campagnes** - u kunt throttling tariefcontrole voor uitgaande campagnes (E-mail, SMS, Push berichten) nu toelaten, toestaand u om overbelasting op stroomafwaartse systemen, zoals het landen van pagina&#39;s of de platforms van de klantenzorg te verhinderen.
   - **campagne die van de Actie** plant - de campagne dagelijks, wekelijkse en maandelijkse planners zijn bijgewerkt voor betere granulariteit. U kunt nu bijvoorbeeld het aantal weken/maanden tussen de schema&#39;s instellen, bepalen op welke dag de uitvoering moet plaatsvinden en besluiten te stoppen na een bepaald aantal gevallen of op een bepaalde datum.

- **Beheer**
   - **de configuratiecontrolealarm van het Kanaal** - u kunt nu intekenen om systeemalarm, of door e-mail of in het het kennisgevingscentrum van Journey Optimizer te ontvangen, voor het geval dat een fout van de kanaalconfiguratie gebeurt of als een DNS verslag mist.

- **Kanaal - duw**
   - **de vervaldatum van het pushbericht** - u kunt nu een vervaldatum voor elk Push- bericht specificeren, dat tijd-gevoelige berichten (zoals de Zwarte Verkoop van Vrijdag) verhindert na een bepaalde datum worden verzonden en zo het leveren van slechte ervaring aan uw klanten vermijdt.

- **Kanaal - E-mail**
   - **de gehechtheid van PDF aan e-mail** - u kunt statische dossiers van PDF aan e-mailberichten nu vastmaken die met Journey Optimizer worden verzonden.

- **Configuratie**
   - **Dynamische domeinsteun** - Journey Optimizer steunt nu verpersoonlijking in het volgen van URLs voor vooraf bepaalde die domeinen op het niveau van de kanaalconfiguratie worden vermeld.
   - **de kenmerkensteun van de Douane met één-Klik unsubscribe URL** - met Journey Optimizer, als u toestemming buiten Adobe beheert, kunt u een extern douaneeindpunt plaatsen door uw eigen te bepalen unsubscribe verbinding in de e-mailconfiguratie. Wanneer uw ontvangers op de koppeling voor afmelden klikken, voegt Journey Optimizer enkele standaardprofielspecifieke parameters toe aan de gebeurtenis voor het bijwerken van de toestemming.

     Als u uw koppeling voor het opzeggen van uw abonnement met één klik verder wilt aanpassen, kunt u nu aangepaste kenmerken definiëren die aan de gebeurtenis voor toestemming worden toegevoegd.

- **Reizen**
   - **activiteit van de Actie in reizen** - Journey Optimizer steunt een nieuwe generische activiteit van de Actie die u toelaat om zowel enig als multi-kanaal uitgaande acties te vormen, die voor gestroomlijnde actieconfiguratie binnen het wegcanvas toestaan. Met deze nieuwe activiteit, hebt u ook de capaciteit om het richten optimalisering, experimenten, en meertalige taalvarianten aan om het even welke ingebouwde kanaalactie toe te voegen.
   - **de bulkverrichtingen van de Reis** - van de lijst van uw reizen, kunt u veelvoudige punten nu selecteren. Als deze optie is geselecteerd, kunt u maximaal tien reizen per keer pauzeren of hervatten.