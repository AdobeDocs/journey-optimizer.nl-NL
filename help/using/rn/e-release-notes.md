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
source-git-commit: 9fdaff7a4364bb7ecfeec27446ed8f4b4ce34488
workflow-type: tm+mt
source-wordcount: '306'
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
<th><strong>Aangepaste actie Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu Adobe Journey Optimizer integreren met Adobe Marketo Engage om uw B2B-gebruiksscenario's te maken. Vanaf een reis, staat een nieuwe douaneactie u toe om gegevens in Marketo in te voeren.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verbeterde kanaalconfiguraties</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De huidige mogelijkheden van het kanaaloppervlak zijn verbeterd voor een consistente aanpak op alle kanalen. U kunt deze configuraties nu definiëren, beheren en opnieuw gebruiken voor elk van uw kanalen.</p>
<p><ul>
<li>De oppervlakten van het kanaal worden nu anders genoemd aan <strong> configuraties van het Kanaal </strong></li>
<li>Van de de configuratieinventaris van het Kanaal kunt u herbruikbare kanaalconfiguraties voor alle kanalen, met inbegrip van nu Web, In-app overseinen, of op code-gebaseerde ervaring tot stand brengen</li>
<li>Het toegangsbeheer van het niveau van objecten (OLAC) is nu beschikbaar voor elke kanaalconfiguratie, toestaand u om te beslissen welke van uw gebruikers specifieke configuraties mogen tot stand brengen of gebruiken</li>
<li>Voor sommige kanalen kunt u kanaalconfiguraties maken die op meerdere platforms zijn gericht. Een voorbeeld hiervan is een in-app berichtkanaalconfiguratie die zich kan richten op een webpagina, een iOS-app en een Android-app.</li>
</ul></p>
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

**Doelgroepen**

* Het gebruik van soorten publiek via aangepaste upload (CSV-bestand) is nu beschikbaar voor gebruik met Privacy en beveiligingsschild.

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
