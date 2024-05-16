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
source-git-commit: 2eb1ffff7101362b52ae91f1a7277188664b2954
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 5%

---

# Vroege aanvullende informatie {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd aan het einde van elke maand in de [releaseopmerkingen](release-notes.md).

Opmerkingen bij de eerste release hieronder kunnen zonder voorafgaande kennisgeving worden gewijzigd tot de beschikbaarheidsdatum van de release. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in [releaseopmerkingen](release-notes.md), op de datum van vrijgave.

## Opmerkingen bij de vervroegde release mei 2024 {#e-2024}

**Releasedatum**: 21 mei 2024

### Nieuwe functies {#e-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden beschreven.


<table>
<thead>
<tr>
<th><strong>Ervaring beslissen - Beperkte beschikbaarheid</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ervaring Beslissen vereenvoudigt personalisatie door een gecentraliseerde catalogus van marketingaanbiedingen aan te bieden, die bekend staan als 'beslissingspunten' en een geavanceerde beslissingsengine. Deze motor hanteert regels en rangschikkingscriteria om de meest relevante beslissingsitems te selecteren en aan elk individu voor te leggen.</p>
<p>Deze beslissingsitems worden naadloos geïntegreerd in een breed scala aan binnenkomende oppervlakken via het nieuwe op code gebaseerde ervaringskanaal, dat nu toegankelijk is in Journey Optimizer-campagnes. Het beleid van de Beslissing van de ervaring is beschikbaar voor gebruik in code-gebaseerde ervaringscampagnes slechts.</p>
<p>Experience Decisioning is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Raadpleeg de <a href="../experience-decisioning/gs-experience-decisioning.md">gedetailleerde documentatie</a> voor meer informatie.</p>
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
<p>Als u e-mail op een gloednieuw IP adres verzendt, kunt u IP opwarmingswerkschema's nu gemakkelijk direct van het gebruikersinterface uitvoeren. Adobe Journey Optimizer biedt een gestandaardiseerde en efficiënte manier om uw IP adressen op te warmen die de beste praktijken voor optimale leverbaarheid volgen.</p>
<p>Raadpleeg de <a href="../configuration/ip-warmup-gs.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Bedrijfsregels - bèta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt korrelige frequentiecappende regels nu tot stand brengen en hen op verschillende soorten marketing mededelingen door regelreeksen toepassen. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Uitgebreide personalisatiegegevens - bèta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu gegevenswaarden opzoeken en ophalen in Adobe Experience Platform-gegevenssets en deze waarden gebruiken om voorwaarden te maken in Adobe Journey Optimizer. U kunt hefboomwerkings gegevens van een raadplegingsdataset wanneer een verhouding gebruikend een attribuut binnen van een serie van voorwerpen is bepaald. U kunt niet-profiel toegelaten datasets voor raadpleging specificeren. Zodra toegelaten, kunt u een profielattribuut als verbindingssleutel aan de gespecificeerde dataset gebruiken om verdere gegevens voor verpersoonlijking terug te winnen.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#e-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Ervaar beslissingsvermogen**

Van bèta naar LA zijn de volgende verbeteringen toegevoegd:

* **Ervaring beslissen + op code gebaseerde ervaringen (LA)**: U kunt nu de functie Ervaring beslissen gebruiken om beslissingsitems te gebruiken in uw op code gebaseerde campagnes. Opmerking: het op code gebaseerde ervaringskanaal en de ervaringsbeslissingen zijn niet beschikbaar voor organisaties die de add-on Adobe van het gezondheidsschild en privacy- en beveiligingsschild hebben aangeschaft. [Meer informatie](../code-based/get-started-code-based.md)
* Je kunt nu contextgegevens van Adobe Experience Platform gebruiken in je beslissingsregels en rangschikkingsformules. [Meer informatie](../experience-decisioning/context-data.md)
* Er is nu een nieuwe machtiging &quot;Ervaring beheren&quot; beschikbaar voor de Beslissingsbeheerbron. Hiermee kunt u rechten beheren die betrekking hebben op het bepalen van ervaring. [Meer informatie](../experience-decisioning/gs-experience-decisioning.md)
* U kunt nu veelvoudige het begrenzen regels voor een bepaald besluitpunt in het Beslissen van de Ervaring toevoegen. Dit staat u toe om het niveau van controle over de manier te verhogen de aanbiedingen worden verzonden. [Meer informatie](../experience-decisioning/items.md#capping)
* U kunt nu aangepaste rapporteringsdashboards maken van campagnes voor het nemen van beslissingen over ervaringen met [!DNL Customer Journey Analytics]. [Meer informatie](../experience-decisioning/cja-reporting.md)


**Offer decisioning**

* **Ondersteuning voor meerdere regels** - U kunt nu maximaal 10 afkapregels toevoegen voor een bepaald aanbod in Beslissingsbeheer. Dit staat u toe om het niveau van controle over de manier te verhogen de aanbiedingen worden verzonden.
* **Audits** - de **Logbestand wijzigen** , zodat u kunt zien welke wijzigingen in een voorstel of een beslissing zijn aangebracht. Wijzigingen met betrekking tot aanbiedingen en besluiten zijn nu te zien in de **Audits** -menu.


**E-mailkanaal**

* **List-unsubscribe** - Na de recente Gmail- en Yahoo-aankondigingen voor bulkafzenders biedt Journey Optimizer ondersteuning voor de optie &quot;Na/1-klik&quot; List-Unsubscribe.
* **Spamscoring** (Beta) - U kunt nu de scoring van de inhoudspam controleren in een speciaal Spam-rapport. Met SpamAssassin kan Adobe Journey Optimizer nu uw e-mailinhoud testen en deze een score geven om aan te geven of ISP-providers het als spam zullen beschouwen of niet. [Meer informatie](../content-management/spam-report.md)


**Doelgroepen**

* Het gebruik van soorten publiek en kenmerken van de compositie van het publiek en aangepaste upload (CSV-bestand) is nu beschikbaar voor gebruik met Healthcare Shield of Privacy and Security Shield.

**Personalisatie**

* **Expressiefragment** - Expressiefragmenten zijn nu beschikbaar voor de **Kanaal in app**. [Meer informatie](../personalization/use-expression-fragments.md)

**Reizen**

* **Beleid samenvoegen** - Het beleid voor samenvoegen kan nu worden geconfigureerd en gebruikt voor uw reizen.
* **mTLS-ondersteuning** - Het mTLS-protocol wordt nu ondersteund in Journey Optimizer API&#39;s en aangepaste handelingen.
* **Tabellen opzoeken in gebeurtenissen** - U kunt nu hefboomwerkings gegevens van een raadplegingsdataset wanneer een verhouding gebruikend een attribuut binnen van een serie van voorwerpen is bepaald. De opzoekwaarden zijn beschikbaar voor reizen (voorwaarden, aangepaste handelingen, enz.) en berichtpersonalisatie.
