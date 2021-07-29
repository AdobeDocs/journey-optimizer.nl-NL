---
title: Aanvullende informatie
description: Journey Optimizer Release-aantekeningen
source-git-commit: cd38b6ec9be0417f5c65e37805c0e7b072d1cb96
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 13%

---


# Release-opmerkingen {#release-notes}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen voor [!DNL Journey Optimizer]. U kunt ook de nieuwste [Documentatie-updates](documentation-updates.md) raadplegen.

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
<p>Adobe Experience Platform staat u toe om verhoudingen tussen schema's te bepalen om één dataset als raadplegingslijst voor een andere te gebruiken. [!DNL Journey Optimizer] kan nu gebruikmaken van gegevens die afkomstig zijn van een gekoppeld schema.</p>
<p>Deze gebieden zijn beschikbaar in unitaire gebeurtenisconfiguratie, reisvoorwaarden, berichtverpersoonlijking en douane actieprijdbaarheid.</p>
<p>Raadpleeg de <a href="event/experience-event-schema.md#leverage_schema_relationships">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Lijst van gewenste personen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu een specifieke verzendende-veilige lijst op het zandbakniveau bepalen, om een veilige milieu voor testend doel te hebben. Op een niet-productiegeval, waar de fouten kunnen voorkomen, verzekert de lijst van gewenste personen u geen risico om ongewenste berichten naar uw klanten te verzenden. Deze functie wordt ingeschakeld door gebruik te maken van onderdrukking-API's.</p>
<p>Raadpleeg de <a href="allow-list.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

* **Journeys**
   * De algemene vertragingssnelheid van alle gelezen segmenten die gelijktijdig in dezelfde sandbox worden uitgevoerd, is beperkt tot 17.000 berichten per seconde. [Meer informatie](building-journeys/read-segment.md#configuring-segment-trigger-activity)
   * Het veld **Cacheduur** is verwijderd uit het configuratievenster van de gegevensbron. [Meer informatie](datasource/about-data-sources.md)
   * Voor externe gegevensbronnen, wordt een het maximum van 15 vraag per seconde nu automatisch bepaald. [Meer informatie](configuration/external-systems.md#capping)
   * Voor live reizen worden in het scherm met de reiseigenschappen nu de publicatiedatum en de naam van de gebruiker weergegeven die de reis heeft gepubliceerd. [Meer informatie](building-journeys/journey-gs.md#change-properties)
   * In het scherm van de reislijst, is het filter van het reistype toegevoegd. [Meer informatie](user-interface.md#section_lgm_hpz_pgb)
   * De parameter **[!UICONTROL Throttling rate]** is toegevoegd in de Gelezen segmentactiviteit. [Meer informatie](building-journeys/read-segment.md#configuring-segment-trigger-activity)

* **Voorvertonen en testen**
   * Identiteit en naamruimte zijn nu zichtbaar in het scherm **[!UICONTROL Preview]**. [Meer informatie](preview.md#preview-your-messages)
   * Het aantal teste-mails voor proefdrukken is nu beperkt tot tien.
   * De tekens die zijn toegestaan voor het **voorvoegsel van de onderwerpregel** in proefdrukken zijn nu beperkt. [Meer informatie](preview.md#send-proofs)

* **Editor voor persoonlijke expressie**
   * De naam van de vervolgkeuzelijst met hulplijnen is gewijzigd en de volgorde ervan is gewijzigd.

### Oplossingen

* Probleem verholpen waarbij dubbele berichten werden afgeleverd voor verzending via batchberichten.
* Gebeurtenissen worden nu overeenkomstig gegenereerd wanneer het verzenden van e-mail niet wordt uitgevoerd wanneer de periode voor opnieuw proberen is verstreken.
* Oplossing voor een probleem waarbij IP-informatie ontbrak in het scherm PTR-records.
* De lokalisatie in het aanbod van het spoor binnen de Redacteur van de Uitdrukking wordt nu uitgevoerd.
* Onjuiste spatiëring in pop-ups met gegevens gecorrigeerd.
