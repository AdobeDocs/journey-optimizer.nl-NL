---
title: Aanvullende informatie
description: Journey Optimizer Release-aantekeningen
source-git-commit: 0fb6d8f611a849696d83e0f129e6462431e5fe83
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 12%

---


# Release-opmerkingen {#release-notes}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen voor Journey Optimizer.
U kunt ook de nieuwste [Documentatie-updates](documentation-updates.md) raadplegen.

## Release juli 2021 {#july-2021-release}

<table>
<thead>
<tr>
<th><strong>Schema-relaties benutten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform staat u toe om verhoudingen tussen schema's te bepalen om één dataset als raadplegingslijst voor een andere te gebruiken. Journey Optimizer kan nu gebruikmaken van gegevens die afkomstig zijn van een gekoppeld schema.</p>
<p>Deze gebieden zijn beschikbaar in unitaire gebeurtenisconfiguratie, reisvoorwaarden, berichtverpersoonlijking en douane actieprijdbaarheid.
<p>Raadpleeg de <a href="event/experience-event-schema.md#leverage_schema_relationships">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

* De algemene vertragingssnelheid van alle gelezen segmenten die gelijktijdig in dezelfde sandbox worden uitgevoerd, is beperkt tot 17.000 berichten per seconde. [Meer informatie](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Het veld **Cacheduur** is verwijderd uit het configuratievenster van de gegevensbron. [Meer informatie](datasource/about-data-sources.md)
* Voor externe gegevensbronnen, wordt een het maximum van 15 vraag per seconde nu automatisch bepaald. [Meer informatie](configuration/external-systems.md#capping)
* Voor live reizen worden in het scherm met de reiseigenschappen nu de publicatiedatum en de naam van de gebruiker weergegeven die de reis heeft gepubliceerd. [Meer informatie](building-journeys/journey-gs.md#change-properties)
* In het scherm van de reislijst, is het filter van het reistype toegevoegd. [Meer informatie](user-interface.md#section_lgm_hpz_pgb)
* De parameter [!UICONTROL Throttling rate] is toegevoegd in de Gelezen segmentactiviteit. [Meer informatie](building-journeys/read-segment.md#configuring-segment-trigger-activity)
