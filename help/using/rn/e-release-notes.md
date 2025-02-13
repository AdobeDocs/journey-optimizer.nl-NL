---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Opmerkingen bij de vervroegde release van Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: d4aa8eea87baf5f23e88ac3f1fc63095d36386d5
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 4%

---

# Vroege aanvullende informatie {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle veranderingen worden geconsolideerd aan het eind van elke maand in de [ versienota&#39;s ](release-notes.md).

**de vroege versienota&#39;s hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in de [ versienota&#39;s ](release-notes.md), bij de versiedatum.

## 25 februari vervroegde release {#25-02-rn}

### Nieuwe functies {#25-02-features}

De nieuwe mogelijkheden die met deze release worden geleverd, worden hieronder beschreven.

<table>
<thead>
<tr>
<th><strong>Bedrijfsvoorschriften</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu bedrijfsregels maken met behulp van regelsets. Regelsets zijn groepen regels die u helpen verzonden berichten binnen campagnes en reisacties te beperken over kanalen, en om de invoer van profielen in reizen te controleren.<p>
<p><ul><li>Creeer kanaalregelreeksen om het aantal berichten te beperken die over één of veelvoudige kanalen worden verzonden. Pas ze toe op campagnes of reisacties om de regels af te dwingen die zijn gedefinieerd in de regelset. De de regelreeks van het kanaal staat u toe om het begrenzen regels toe te passen die op communicatie types worden gebaseerd. Stel bijvoorbeeld een regel in die is ingesteld op het beperken van 'promotionele berichten' en een andere regel voor 'nieuwsbrieven'. Pas de toepasselijke regel toe die in uw campagne of reisactie is ingesteld, afhankelijk van het type communicatie dat u verzendt.</li>
<li> Reisregelsets maken om profielinvoer in reizen te regelen. Beperk hoe vaak een profiel een reis binnen een bepaalde periode kan ingaan of het aantal reizen een profiel kan gelijktijdig worden ingeschreven. Pas deze toe op het niveau van de reis om te zorgen voor een goed beheer van de toegang.</li></p>
<p>Eerder beschikbaar voor een reeks organisaties (LA), zijn de bedrijfsregels nu beschikbaar aan alle gebruikers (GA).</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Multiregionale ondersteuning voor SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt de berichtlevering van SMS van multi-regionale eindpunten nu beheren door levering, terugkoppelen, binnenkomend, en callback URLs met voeten te treden. Ter ondersteuning hiervan is een nieuwe veld Overschrijf-URL toegevoegd aan de configuratie van API-referenties. Deze wijziging is alleen beschikbaar bij de Sinch-provider.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Customer Journey Analytics-sjablonen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Je hebt nu de mogelijkheid om je Journey Optimizer-rapporten te verbeteren met behulp van Customer Journey Analytics-sjablonen. Met deze nieuwe functie kunt u uw rapportageproces stroomlijnen met vooraf ontworpen sjablonen die zijn afgestemd op uw analysebehoeften.
</p>
<img src="assets/do-not-localize/cja-templates.gif">
<p>Raadpleeg de <a href="../reports/report-cja-manage.md#cja-template">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: vanaf 15 januari 2025</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Flexibele evaluatie van het publiek (Beperkte Beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dankzij de flexibele publieksevaluatie kunt u een segmentatietaak uitvoeren op aanvraag voor een geselecteerd publiek, zodat u altijd over de meest actuele publieksgegevens beschikt voordat u deze doelt op Journey Optimizer-reizen en -campagnes.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Raadpleeg de <a href="../audience/about-audiences.md#flexible">gedetailleerde documentatie</a> voor meer informatie.</p>
<p> De flexibele publieksevaluatie is slechts beschikbaar voor een reeks organisaties (Beperkte Beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p>Beschikbaarheidsdatum: 28 januari 2025</p>
</tr>
</tbody>
</table>


### Verbeteringen {#25-02-improvements}

De verbeteringen hieronder komen met de update van februari.

* **Tijd-aan-levende Dataset (TTL)** - Beginnend deze maand, zal een tijd-aan-levende (TTL) guardrail aan systeem-geproduceerde datasets van Journey Optimizer in nieuwe zandbakken en nieuwe organismen als volgt worden uitgerold:

   * 90 dagen voor gegevens in de profielopslag
   * 13 maanden voor gegevens in het data Lake

  Deze wijziging wordt in een volgende fase doorgevoerd in bestaande sandboxen voor klanten.

* **Playbooks** - u kunt uw eigen Playbooks van het Geval van het Gebruik in Journey Optimizer nu tot stand brengen en publiceren.

* **Directe post** - DLZ (Geplaatst Gebied van DAta) wordt nu gesteund als servertype voor dossier dat in Directe postconfiguratie verplettert.

**E-mailconfiguratie** - de datum van de Beschikbaarheid: 12 Feb, 2025

* Als u toestemming buiten Adobe beheert, kunt u nu een aangepast e-mailadres voor opzeggen en een aangepaste, één-klik-URL voor opzeggen instellen als onderdeel van de configuratie-instellingen voor e-mailkanalen. [ las meer ](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

  >[!AVAILABILITY]
  >
  >Dit vermogen wordt vrijgegeven in Beperkte Beschikbaarheid (LA) voor een kleine reeks klanten.

**Beslissing** - de datum van de Beschikbaarheid: Jan 28, 2025

* Het besluit steunt nu de gegevenstypes van Objecten wanneer het uitgeven van het schema van de puntcatalogus. [Meer informatie](../experience-decisioning/catalogs.md)

**Personalization** - de datum van de Beschikbaarheid: 29 jan, 2025

* De nieuwe datum/tijdhulpfuncties zijn beschikbaar voor gebruik in de verpersoonlijkingsredacteur. [Meer informatie](../personalization/functions/dates.md)