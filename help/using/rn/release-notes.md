---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Journey Optimizer Release-aantekeningen
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0433e312db84ee16a076c183a82345de372c6ae7
workflow-type: tm+mt
source-wordcount: '1112'
ht-degree: 9%

---

# Aanvullende informatie {#release-notes}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen voor [!DNL Journey Optimizer]. U kunt ook de [meest recente documentatie-updates](documentation-updates.md) pagina voor meer wijzigingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} vandaag en ontvang de nieuwste productupdates, spannende artikelen, gebruiksscenario&#39;s, tips en nog veel meer die elk kwartaal rechtstreeks aan uw Postvak IN worden bezorgd.


## Oktober 2022 {#oct-2022-release}

### Verbeteringen{#oct-2022-improvements}

**Journeys**

* De **Herkomst forceren bij herhaling** Deze optie is toegevoegd in terugkerende parameters van het read-segment. Met deze optie kunt u alle profielen die zich nog in de reis bevinden, automatisch laten afsluiten bij de volgende uitvoering. Wanneer de optie is gedeactiveerd, moeten profielen de reis beëindigen alvorens zij in een ander voorkomen kunnen opnieuw ingaan. [Meer informatie](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Campagnes**

* U kunt voltooide en gestopt campagnes nu archiveren. [Meer informatie](../campaigns/modify-stop-campaign.md#archive)

## Release september 2022{#sept-2022-release}

### Nieuwe functies{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>Dynamische inhoud en nieuwe voorwaardelijke regelbuilder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu dynamische inhoud maken om de inhoud van uw berichten aan te passen op basis van voorwaardelijke regels.</p> 
<p>Voorwaardelijke regels worden gecreeerd gebruikend een visuele regelbouwer binnen de Redacteur van de Uitdrukking, waar u hen voor verder hergebruik over uw reizen en campagnes kunt opslaan.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>Raadpleeg de <a href="../personalization/get-started-dynamic-content.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API-gestuurde campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Naast bestaande geplande campagnes kunt u nu API-getriggerde campagnes maken in Journey Optimizer en deze aanroepen vanuit een extern systeem met behulp van API's.</p>
<p>Dit staat u toe om diverse operationele en transactionele overseinenbehoeften zoals wachtwoordterugstellen, het teken van OTP, onder andere te behandelen.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Raadpleeg de <a href="../campaigns/api-triggered-campaigns.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Toegangsbeheer voor gegevens</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Via op kenmerken gebaseerd toegangsbeheer kunnen beheerders de toegang tot specifieke objecten beheren op basis van bepaalde kenmerken. Deze kenmerken kunnen metagegevens zijn die aan een object worden toegevoegd, zoals labels. Met het oog op deze release kunnen beheerders ook gebruikersrollen definiëren die alleen toegang hebben tot specifieke velden en/of objecten, en gegevens die overeenkomen met die velden en/of objecten.</p>
<p> Het gebruik van op attributen-gebaseerde toegangsbeheer is momenteel beperkt tot geselecteerde klanten, en zal aan alle milieu's in een toekomstige versie worden opgesteld.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>Raadpleeg de <a href="../administration/object-based-access.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Beheer en privacy van gegevens</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met zijn beheerskader voor etikettering en handhaving van gegevensgebruik (DULE) kan Journey Optimizer nu het Adobe Experience Platform-beleid voor governance gebruiken om te voorkomen dat gevoelige velden via aangepaste acties naar systemen van derden worden geëxporteerd. Als het systeem een beperkt veld identificeert in de parameters voor aangepaste handelingen, wordt een fout weergegeven waardoor u de reis niet kunt publiceren.</p>
<p>Het gebruik van de Etikettering en de Handhaving van het Gebruik van Gegevens (DULE) is momenteel beperkt tot geselecteerde klanten, en zal aan alle milieu's in een toekomstige versie worden opgesteld.</p>
<p>Raadpleeg de <a href="../action/action-privacy.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Geautomatiseerde toestemmingshandhaving (toestemmingsbeleid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Adobe Experience Platform kunt u eenvoudig marketingbeleid toepassen en afdwingen om de voorkeuren voor toestemming van uw klanten te respecteren. Beleid voor instemming wordt gedefinieerd in Adobe Experience Platform. In Journey Optimizer kunt u dit beleid voor toestemming toepassen op aangepaste handelingen. U kunt bijvoorbeeld regels voor toestemming definiëren om klanten uit te sluiten die niet hebben ingestemd met het ontvangen van e-mail, push- of SMS-berichten.
<p>Automated Consent Enforcement is momenteel alleen beschikbaar voor organisaties die de Add-on-aanbieding Healthcare Shield hebben aangeschaft.</p>
<p>Raadpleeg de <a href="../action/consent.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Machtigingsbeheer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ondersteunt het definiëren van gebruikersrollen en toegangsbeleid voor het beheren van machtigingen voor functies en objecten. Doorheen <strong>Adobe Experience Cloud-machtigingen</strong>, kunt u rollen tot stand brengen en beheren, evenals de gewenste middeltoestemmingen voor deze rollen toewijzen. Met machtigingen kunt u ook de labels, sandboxen en gebruikers beheren die aan een specifieke rol zijn gekoppeld.</p>
<p> Het gebruik van toestemmingen is momenteel beperkt tot geselecteerde klanten, en zal aan alle milieu's in een toekomstige versie worden opgesteld.</p>
<p>Raadpleeg de <a href="../administration/attribute-based-access.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Waarschuwing en bewaking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als Journey Optimizer-gebruiker kunt u nu systeemwaarschuwingen openen via de gebruikersinterface om op de hoogte te worden gebracht wanneer reizen niet naar behoren werken. U kunt de beschikbare waarschuwingen weergeven en hierop een abonnement nemen. In de eerste waarschuwing die bij deze release beschikbaar is, wordt u gewaarschuwd als een activiteit van het Leessegment tijdens de gedefinieerde tijdsperiode geen profiel heeft verwerkt. Er zal meer komen nu deze workflow ontgrendeld is.</p>
<p>Raadpleeg de <a href="../reports/alerts.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Verbeteringen{#sept-2022-improvements}

**Reizen**

* De **Entiteitsgegevens** is nu beschikbaar als out-of-the-box dataset in Adobe Journey Optimizer. Deze raadplegingsdataset omvat meta- gegevens om het volgen te verrijken en datasetinformatie terug te koppelen. Dit zal u helpen uw rapporten en vragen met begrijpelijkere gegevens verbeteren. [Meer informatie](../start/datasets-query-examples.md#entity-dataset)
* Er is een nieuwe guardrail toegevoegd aan de unitaire reizen (te beginnen met een evenement of een segmentkwalificatie) om te voorkomen dat ritten meerdere keren ten onrechte voor dezelfde gebeurtenis worden gestart. De terugkeer van het profiel wordt nu tijdelijk geblokkeerd door gebrek voor 5 minuten. [Meer informatie](../start/guardrails.md#events-g)

**Beheer**

* Wanneer u de lijst van gewenste personen activeert of deactiveert, wordt nu een nieuwe waarschuwing weergegeven waarin de effecten van elke actie worden beschreven. [Meer informatie](../configuration/allow-list.md#enable-allow-list)
* De gebruikersinterface voor het creëren van kanaaloppervlakken, het creëren van IP-pools, het beheren van de suppressielijst en de lijst van gewenste personen, en het configureren van het SMS-kanaal is bijgewerkt.
* Wanneer u nu het eerste kanaaloppervlak voor een bepaald subdomein maakt, duurt de verwerkingstijd 10 minuten tot 10 dagen en slechts 3 uur voor volgende oppervlakken die dat subdomein gebruiken. [Meer informatie](../configuration/channel-surfaces.md#create-channel-surface)

<!--* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.-->
* De gebruikersinterface voor het maken van voorinstellingen voor openingspagina&#39;s en het landen van subdomeinen van de pagina is bijgewerkt. [Meer informatie](../configuration/lp-subdomains.md)

**Controles van audits**

* Met Journey Optimizer kunt u acties identificeren die door gebruikers in het systeem worden uitgevoerd op verschillende services en mogelijkheden, zoals campagnes, reizen, berichten, landingspagina&#39;s enz. De middelen van het logboek van de controle omvatten nu veranderingen op diverse andere acties, en worden automatisch geregistreerd aangezien de activiteit voorkomt. Meer informatie vindt u [op deze pagina](../privacy/audit-logs.md).

**Ondersteuning voor archivering**

* De nieuwe **Entiteitsgegevens** omvat een gebied van het Malplaatje dat u toelaat om het formaat en de structuur van de verzonden berichten op alle kanalen voor archiveringsdoel uit te voeren. [Meer informatie](../configuration/archiving-support.md)

**Landingspagina’s**

* U kunt nu contextuele gegevens gebruiken die afkomstig zijn van een andere pagina binnen dezelfde landingspagina. Als u bijvoorbeeld een selectievakje koppelt aan een abonnementenlijst op de primaire landingspagina, kunt u die abonnementenlijst op de subpagina &quot;Bedankt&quot; gebruiken. [Meer informatie](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Andere wijzigingen{#sept-2022-other}

* Modus Reisexplosie is vervangen door Modus Snelle levering campagne. [Meer informatie](../campaigns/create-campaign.md#rapid-delivery)
* Om de prestaties te verbeteren, kunnen de de gebeurtenisgebiedgroepen van de Ervaring niet meer in reizen worden gebruikt die met een Gelezen segment, een kwalificatie van het Segment of een bedrijfsgebeurtenisactiviteit beginnen. Deze wijziging geldt alleen voor nieuwe reizen. De bestaande zullen het huidige gedrag houden. [Meer informatie](../start/guardrails.md#expression-editor)
* De beperking van 1 uur voor geplande leesegmentreizen is verwijderd. Deze reizen kunnen nu zonder vertraging worden uitgevoerd.

