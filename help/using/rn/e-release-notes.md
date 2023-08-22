---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Opmerkingen bij de vervroegde release van Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 132121b4dd9c20149e4a5b24e90ebffd4ebbdcbc
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 4%

---

# Vroege aanvullende informatie {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd op de laatste week van elke maand in de [releaseopmerkingen](release-notes.md).

Opmerkingen bij de eerste release hieronder kunnen zonder voorafgaande kennisgeving worden gewijzigd tot de beschikbaarheidsdatum van de release. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in [releaseopmerkingen](release-notes.md), op de datum van vrijgave.

## Opmerkingen bij de vervroegde release augustus 2023 {#aug-rn-2023}

**Releasedatum**: 23-24 augustus 2023

### Nieuwe functies{#aug-2023-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.

<table>
<thead>
<tr>
<th><strong>In-app berichten verzenden tijdens uw reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu persoonlijke In-app-berichten naar uw app-gebruikers verzenden voor een reis. Met Journey Optimizer kunt u meldingen ontwerpen en de lay-out, weergave, tekst en knoppen van berichten aanpassen voor een naadloze ervaring.</p>
<img src="assets/in_app_journey_1.png"/>
<p>Raadpleeg de <a href="../in-app/get-started-in-app.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>E-mails met lijsten met zaden valideren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu zaadlijsten maken en beheren in Journey Optimizer. Een zaadlijst bestaat uit teste-mailadressen waarnaar u een e-mail verzendt voordat u deze naar uw werkelijke publiek verzendt. Met deze functie kunt u de verzonden e-mailkopieën controleren en controleren of alle weergaveformaten, URL's, afbeeldingen en koppelingen correct zijn.</p>
<img src="../configuration/assets/seed-list-details.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Tekst en afbeeldingen genereren met de Content Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Wanneer u uw bericht hebt gemaakt en gepersonaliseerd, neemt u de inhoud naar het volgende niveau met de Content Assistant. U kunt nu de Content Assistant gebruiken om de impact van uw bericht te optimaliseren door te experimenteren met verschillende hoofdtitels en afbeeldingen. Elke variant wordt beheerd als een unieke behandeling, om te meten en te vergelijken welke titel effectief meer kliks produceert.</p>
<p>Deze mogelijkheid is momenteel beschikbaar als een persoonlijke bètaversie.</p>
<img src="assets/gen-ai-image-2.png"/>
<!--p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>



### Verbeteringen {#aug-2023-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**API&#39;s**

Er is nu een nieuwe API beschikbaar voor het maken en beheren van inhoudsfragmenten. [Meer informatie](https://developer.adobe.com/journey-optimizer-apis/references/content-templates/#tag/Content-fragment-API){target="_blank"}.

**E-mailkanaal**

* Er is een nieuwe optie beschikbaar in de instellingen van het e-mailoppervlak om e-mailadressen op te nemen die zijn onderdrukt als gevolg van een spamklacht bij het publiek van uw transactieberichten. Zelfs als zij marketing berichten als spam merkten, kunnen deze profielen transactieberichten, zoals wachtwoordterugstellen of rekeningsverklaringen dan ontvangen. Deze optie is standaard uitgeschakeld.

**Journeys**

* U kunt nu API vraagreacties in douaneacties gebruiken en uw reis structureren die op deze reacties wordt gebaseerd. Deze functie is momenteel beschikbaar als een persoonlijke bètaversie.
* Er is een nieuw type systeemwaarschuwing geïntroduceerd. U kunt nu een melding krijgen wanneer een aangepaste handeling mislukt.
* Wanneer u een reis dupliceert, kunt u nu de naam van de reiskopie definiëren.


**Direct mail**

* Steun Azure Blob als verpletterende bestemming.
* Ondersteuning `&` als een aangepast scheidingsteken.