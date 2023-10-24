---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Opmerkingen bij de vervroegde release van Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1b37da28e6dbb03c8c76dd9a6637dfd95447eb7e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 2%

---

# Vroege aanvullende informatie {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd op de laatste week van elke maand in de [releaseopmerkingen](release-notes.md).

Opmerkingen bij de eerste release hieronder kunnen zonder voorafgaande kennisgeving worden gewijzigd tot de beschikbaarheidsdatum van de release. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in [releaseopmerkingen](release-notes.md), op de datum van vrijgave.

## Opmerkingen bij de vervroegde release oktober 2023 {#oct-rn-2023}

**Releasedatum**: 25-26 oktober 2023

### Nieuwe functies{#oct-2023-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.

<table>
<thead>
<tr>
<th><strong>Gereedschap Sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met gereedschappen voor sandboxen kunt u objecten kopiëren naar meerdere sandboxen door gebruik te maken van exporteren en importeren van pakketten. Een pakket kan uit één object of uit meerdere objecten bestaan. Alle objecten die in een pakket zijn opgenomen, moeten afkomstig zijn uit dezelfde sandbox.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>MMS (Multimedia Message Service) in SMS (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met het Kanaal van SMS, kunt u uw mededeling nu verbeteren door de MMS-berichten (Multimedia Message Service) te verzenden, toelatend het delen van beelden, GIFFEN, of video's met uw klanten. Deze functie is momenteel alleen beschikbaar in Beta met Sinch.</p>
<!--img src="assets/channel-reports.png"/-->
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

### Verbeteringen {#oct-2023-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Doelgroepen**

* U kunt nu doelgroepen kiezen die vanuit een CSV-bestand naar reizen en campagnes zijn geüpload.
* U kunt nu doelgroepen kiezen die zijn gemaakt door de publiekscompositie en de verrijkingskenmerken van de doelgroep in de stappen.

>[!AVAILABILITY]
>
>Deze mogelijkheden zijn momenteel beschikbaar als een persoonlijke bètaversie.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Waarschuwing**

* Wanneer er een fout optreedt in een van uw campagnes, verschijnt er nu een waarschuwingspictogram in de lijst met campagnes naast de status van de campagne.

**Campagnes**

* U kunt nu een live eenmalige campagne stoppen, wijzigingen aanbrengen en deze hervatten. Deze verbetering is beschikbaar in Beta.

**Journeys**

* De maximale tijdsduur die u in een wachttijd kunt definiëren, is nu 29 dagen in plaats van 30. Dit geldt voor:

   * de **Tijd** in het veld [wachtactiviteiten](../building-journeys/wait-activity.md)
   * de **Wachttijd bij terugkeer** in [reiseigenschappen](../building-journeys/journey-gs.md#entrance)
   * de **Wacht op** veld in de time-outdefinitie van [algemeen](../building-journeys/general-events.md#events-specific-time) en [reactie](../building-journeys/reaction-events.md) gebeurtenissen.

**Toestemming in kanaalconfiguratie**

* U kunt nu een marketingactie op het niveau van het kanaaloppervlak selecteren. Bij gebruik op een oppervlak worden alle toestemmingsbeleidsregels die aan die marketingactie zijn gekoppeld, benut om de voorkeuren van uw klanten te respecteren.

**Beslissingsbeheer**

* Verschillende etiketten met betrekking tot het aanbieden van plafonnering in de besluitvormingsinterface zijn bijgewerkt.
