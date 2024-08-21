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
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 5%

---

# Vroege aanvullende informatie {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle veranderingen worden geconsolideerd aan het eind van elke maand in de [ versienota&#39;s ](release-notes.md).

**de vroege versienota&#39;s hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de datum van de versiebeschikbaarheid**. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in de [ versienota&#39;s ](release-notes.md), bij de versiedatum.

## Opmerkingen bij de vervroegde release augustus 2024 {#e-2024}

**de datum van de Versie**: Augustus 20-21, 2024

### Nieuwe functies {#e-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden beschreven.

<table>
<thead>
<tr>
<th><strong>Variabelen in inhoudsfragmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De fragmenten kunnen nu inputvariabelen, zowel in <a href="../personalization/use-expression-fragments.md"> uitdrukkingsfragmenten </a> als <a href="../email/use-visual-fragments.md"> visuele fragmenten </a> verbruiken. U kunt deze variabelen gebruiken om uw berichtinhoud en parameters, in uw campagnes en reizen te personaliseren.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Beschikbaarheidsdatum: aug, 13</p>
<p>Als u e-mail op een gloednieuw IP adres verzendt, kunt u IP opwarmingswerkschema's nu gemakkelijk direct van het gebruikersinterface uitvoeren. Adobe Journey Optimizer biedt een gestandaardiseerde en efficiënte manier om uw IP adressen op te warmen die de beste praktijken voor optimale leverbaarheid volgen.</p>
<p>Raadpleeg de <a href="../configuration/ip-warmup-gs.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Verbeteringen {#e-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Reizen**

* In de **voorwaarde** activiteit, door gebrek, wordt de voorwaarde van de Tijd nu geplaatst door uur, van 00:00 tot 12:00. [Meer informatie](../building-journeys/condition-activity.md#time_condition)
* Wanneer u uw reizen maakt, worden waarschuwingen nu weergegeven in een vervolgkeuzelijst, zodat deze kunnen worden afgestemd op campagnewaarschuwingen en een consistente gebruikerservaring mogelijk maken. [Meer informatie](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* De zoomopties op de werkbalk voor reizen zijn verbeterd. Het zoompercentage is nu zichtbaar en u kunt de zoomwaarde nu gemakkelijk terugzetten op 100%.

**Doelgroepen**

* Het gebruik van soorten publiek via aangepaste upload (CSV-bestand) is nu beschikbaar voor gebruik met Privacy en beveiligingsschild.
* Wanneer u een aangepast upload-publiek (CSV-bestand) als doel instelt, kunt u nu kenmerken uit het bestand gebruiken in uw campagnes en reizen. Deze attributen zijn beschikbaar in de verpersoonlijkingsredacteur, om uw berichten, en de reis geavanceerde uitdrukkingsredacteur te personaliseren.


<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
