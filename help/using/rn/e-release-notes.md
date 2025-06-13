---
solution: Journey Optimizer
product: journey optimizer
title: Vroege aanvullende informatie
description: Opmerkingen bij de vervroegde release van Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: eff3f2fb4d1c369e77a22013ae1576b57449a8b7
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 3%

---

# Vroege aanvullende informatie {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle veranderingen worden geconsolideerd aan het eind van elke maand in de [ versienota&#39;s ](release-notes.md).

**de vroege versienota&#39;s hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in de [ versienota&#39;s ](release-notes.md), bij de versiedatum.


## Opmerkingen bij de vervroegde release juni 25 {#25-6-rn}


**de vroege versienota&#39;s hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. Koppelingen, schermen en bijgewerkte documentatie worden gepubliceerd op de releasedatum.

**de datum van de Versie**: 18 Juni, 2025


### Nieuwe functies {#25-06-features}

De nieuwe mogelijkheden die met deze release worden geleverd, worden hieronder beschreven.




<table>
<thead>
<tr>
<th><strong>RCS-berichten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Het overseinen van RCS (Rich Communication Services) wordt nu gesteund in Journey Optimizer, toelatend de volgende verbeterde overseinenmogelijkheden afhankelijk van leverancier en dragersteun:</p>
<ul>
<li>Branded en de geverifieerde steun van de afzender: verzend berichten gebruikend geverifieerde bedrijfsprofielen met branding elementen (embleem, afzendernaam, enz.).</li>
<li>Inzichten van de levering van berichten: Ontvang gedetailleerde leveringsrapporten met inbegrip van updates van de berichtstatus (b.v., verzonden, geleverd, gelezen).</li>
<li>Koppelingentracering: sluit URL's in RCS-berichten in en traceer deze voor betrokkenheidsanalyses.</li>
<li>Terugvallen op SMS: Automatische fallback aan SMS wanneer het apparaat van het profiel geen RCS steunt of tijdelijk onbereikbaar via RCS is.</li>
<li>Basisberichtcompositie: Verstuur op tekst gebaseerde RCS-berichten met optionele media en rijke elementen, afhankelijk van de providerondersteuning.</li>
</ul>
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>True Multi-Tenant Unitary Delivery</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Formuliervelden in ervaringsinhoud op basis van code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu specifieke bewerkbare velden definiëren in JSON- of HTML-inhoudssjablonen, waarmee niet-technische gebruikers inhoud gemakkelijk kunnen bewerken in op code gebaseerde ervaringen zonder dat code hoeft te worden bewerkt.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aangepaste delegatiemethode voor subdomeinen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Naast de volledige delegatie en de methode CNAME, is een nieuwe subdomain configuratiemethode nu beschikbaar: de de delegatiemethode van de Douane, die u toelaat om volledig het controleren en het handhaven van alle aspecten van DNS te bezitten die voor het leveren, het teruggeven en het volgen van berichten worden vereist.</p>
<p>Eerder vrijgegeven in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's (Algemene Beschikbaarheid).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Inhoudsbesnoeiingsactiviteit tijdens reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu persoonlijke aanbiedingen opnemen in uw reizen door middel van een speciale activiteit voor het bepalen van inhoud in het reiscanvas en deze gebruiken in reisactiviteiten, waaronder voorwaarden en aangepaste acties.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid) en wordt globaal geïmplementeerd in een toekomstige release.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Experience Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->



<table>
<thead>
<tr>
<th><strong>Reizen op reis</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Reis Dry run is een speciale publicatiemodus in Adobe Journey Optimizer die reisartsen in staat stelt een reis te testen met behulp van echte productiegegevens zonder contact op te nemen met echte klanten of profielinformatie bij te werken. Deze functie helpt reisartsen vertrouwen te winnen in hun reisontwerp en doelgroep voordat ze het live publiceren.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid) en wordt globaal geïmplementeerd in een toekomstige release.</p>
</td>
</tr>
</tbody>
</table>


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
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid) en wordt globaal geïmplementeerd in een toekomstige release.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Schaal de winnaar van uw proefversie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Schaal de winnaar van de proefversie kunt u de winnende variatie van een experiment automatisch of handmatig voor alle gebruikers uitrollen. Deze functie zorgt ervoor dat u, zodra een topuitvoerder is geïdentificeerd, het bereik en de effectiviteit ervan kunt maximaliseren zonder voortdurend handmatig toezicht.</p>
<p>Raadpleeg de <a href="../content-management/content-experiment.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 2 juni 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflict en prioriteit</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer is het beheren van het volume en de timing van campagnes en reizen van essentieel belang om te voorkomen dat klanten met te veel interacties worden overspoeld. Journey Optimizer biedt nu diverse hulpmiddelen voor conflictbeheer en prioritering - voorheen alleen beschikbaar voor organisaties met beperkte toegang (LA) - die nu algemeen beschikbaar zijn (GA).</p>
<p>Eerder uitgebracht in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's. Met deze algemene release zijn de volgende verbeteringen aangebracht:</p>
<ul>
<li>Uitgebreide ondersteuning: de tools voor conflictbeheer ondersteunen nu niet alleen publiekstrajecten, maar ook eenheidsreizen en kwalificatiereizen voor het publiek.</li>
<li>Verbeterd het Oplossen van problemen: Twee nieuwe gebieden van de stapgebeurtenis zijn nu beschikbaar in de Dienst van de Vraag, toelatend u om te analyseren waarom een profiel van een reis of een campagne werd verworpen.</li>
<li>Verbeterde rapportage: in rapporten wordt nu aangegeven welke specifieke regel een profiel van een reis of campagne heeft uitgesloten, waardoor meer transparantie en activeerbare inzichten worden geboden.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Raadpleeg de <a href="../conflict-prioritization/gs-conflict-prioritization.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 3 juni 2025</p>
</td>
</tr>
</tbody>
</table>


### Verbeteringen {#25-06-improv}

De verbeteringen die bij deze release worden geleverd, worden hieronder weergegeven.

* **de regelreeksen van het Kanaal**

   * **venster van de Duur van de Douane** voor het in kaart brengen - een nieuw **gebied van de Telling van de Herhaling** is nu beschikbaar in het scherm van de reeksen van de kanaalregel, toestaand u om frequentie het in kaart brengen regels over veelvoudige dagen, weken, of maanden, afhankelijk van de gespecificeerde duur toe te passen.

   * **Uurduur** - u kunt het bedekken op een uurbasis voor de reeksen van de kanaalregel nu toepassen.

* **op code-gebaseerde ervaringen**

  Het besluitvormingsbeleid is nu beschikbaar in code-gebaseerde malplaatjes van de ervaringsinhoud en op de code redacteur juiste spoorlijn.

* **Email Designer**

   * **de Steun van CSS van de Douane** - Journey Optimizer staat u nu toe om douane CSS aan uw e-mailinhoud direct binnen de E-mailontwerper toe te voegen.
   * **de wijzessteun van de Donker** - de e-mailontwerper van Journey Optimizer biedt nu de capaciteit aan om op donkere wijze te schakelen waar u specifieke montages kunt bepalen.


* **Beslissing** - de datum van de Beschikbaarheid: 3 Juni, 2025

  Decisioning-objecten kunnen nu worden gekopieerd tussen sandboxen, waardoor test- en implementatieworkflows worden gestroomlijnd. [Meer informatie](../configuration/copy-objects-to-sandbox.md#decisioning)

* **de kenmerksteun van het Punt van het Besluit voor beslissingsregels** - de datum van de Beschikbaarheid: 4 juni, 2025

  U kunt nu kenmerken van beslissingspunten gebruiken om beslissingsregels te maken. [Meer informatie](../experience-decisioning/rules.md#create)

* **Interactieve update van API van de Uitvoering van het Bericht** - de datum van de Beschikbaarheid: 6 juni, 2025

  De Interactieve API van de Uitvoering van het Bericht staat u nu toe om het programma van aanstaande campagneuitvoering te schrappen. [Meer informatie](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}