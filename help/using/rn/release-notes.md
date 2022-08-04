---
title: Aanvullende informatie
description: Journey Optimizer Release-aantekeningen
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 8766f64c4ea7985c6c9d6e4ba022ef6b1fc0dbed
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 9%

---

# Aanvullende informatie {#release-notes}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen voor [!DNL Journey Optimizer]. U kunt ook de [meest recente documentatie-updates](documentation-updates.md) pagina voor meer wijzigingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} vandaag en ontvang de nieuwste productupdates, spannende artikelen, gebruiksscenario&#39;s, tips en nog veel meer die elk kwartaal rechtstreeks aan uw Postvak IN worden bezorgd.

## Release van juli 2022 {#july-2022-release}

### Nieuwe functies

<table>
<thead>
<tr>
<th><strong>Nieuwe in-line overseinenstroom</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer biedt een nieuwe stroom voor het schrijven van berichten in de pers. In-line berichten besparen gebruikers aanzienlijke tijd en stroomlijnen het workflowproces voor het maken en leveren van een e-mail, een pushmelding of een SMS in Journey Optimizer. Door Berichten als afzonderlijke stap te verwijderen en in plaats daarvan editable in-line als deel van een actie op het Canvas van de Reis, zullen de gebruikers minder knopen moeten klikken en minder schermen navigeren om hun inhoud te ontwerpen en uit te geven.</p>
<img src="assets/do-not-localize/inline.gif"/>
<p>Raadpleeg de <a href="../messages/get-started-content.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Op kenmerken gebaseerde toegangscontrole (beperkte beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt schemagebieden met etiketten nu identificeren die organisatorisch of gegevensgebruikswerkingsgebied bepalen. De beheerders kunnen de interface van Toestemmingen gebruiken om toegangsbeleid te bepalen dat XDM schemagebieden behandelt en beter de toegang beheren die aan gebruikers of groepen gebruikers (interne, externe, of derdegebruikers) wordt gegeven, en toegang tot specifieke types van gegevens (d.w.z. Gevoelige Persoonlijke Gegevens/SPD) te beheren.</p>
<p>Het gebruik van op attributen-gebaseerde toegangsbeheer is momenteel beperkt tot geselecteerde gebruikers, en zal aan alle milieu's in een toekomstige versie worden opgesteld.</p>
<p>Raadpleeg de <a href="../administration/attribute-based-access.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Batchbeslissingstaken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt taken voor batchbepaling nu uitvoeren vanuit de gebruikersinterface, zodat ik geen ontwikkelaar nodig heb om taken voor batchverwerking uit te voeren en de tijd die nodig is voor marketing kan verminderen. Met deze nieuwe interface kunt u nieuwe taken maken en huidige en vroegere taken beheren.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Raadpleeg de <a href="../offers/batch-delivery.md">gedetailleerde documentatie voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gebruik automatisch de best presterende aanbieding in uw besluiten (beperkte beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu gepersonaliseerde optimalisatiemodelsystemen gebruiken in Beslissingsbeheer. Met dit nieuwe type model kunt u aanbiedingen optimaliseren en aanpassen op basis van segmenten en prestaties bieden.</p>
<p>Het gebruik van gepersonaliseerde optimalisatie-AI-modellen is momenteel beperkt tot geselecteerde gebruikers en wordt in een toekomstige release geïmplementeerd in alle omgevingen.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Raadpleeg de <a href="../offers/ranking/personalized-optimization-model.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Journeys**

* **Een reis beëindigen** - Op het canvas **Einde** activiteit is verwijderd uit het palet. Eindtags worden nu standaard aan het einde van elk pad toegevoegd en kunnen niet worden verwijderd. Dankzij deze verbetering kan beter worden aangegeven waar een klant de reis heeft verlaten, zonder dat de reisdeskundige enige actie hoeft te ondernemen. Zie de [documentatie](../building-journeys/journey-end.md) en [functievideo](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.

**Berichten**

* Voorinstellingen voor berichten zijn nu **kanaaloppervlakken**. [Meer informatie](../configuration/channel-surfaces.md)

**Beheer**

* **PTR-recordeditie** - Wanneer u nu een PTR-record bijwerkt, duurt de verwerkingstijd maximaal 3 uur. [Meer informatie](../configuration/ptr-records.md#processing)

* **UI lijst van gewenste personen** - U kunt nu de Journey Optimizer-gebruikersinterface gebruiken om nieuwe e-mailadressen of domeinen aan de lijst van gewenste personen toe te voegen. [Meer informatie](../configuration/allow-list.md)

* **Update voor logica van lijst van gewenste personen** - De logica lijst van gewenste personen wordt nu toegepast zodra de functie is ingeschakeld, zelfs als de lijst leeg is. [Meer informatie](../configuration/allow-list.md#logic)

* **Parameters voor URL-tracking** - U kunt de Expressieeditor nu gebruiken om URL-volgparameters in uw e-mailoppervlakken (dus voorinstellingen) te configureren. [Meer informatie](../configuration/email-settings.md#url-tracking)

**offer decisioning**

* **Grootte publiek** - Een nieuwe de schattingscomponent van de publieksgrootte wordt nu getoond in het gebruikersinterface wanneer het creëren van een besluitvormingsregel, wanneer het selecteren van een segment of een regel om een aanbiedingsontvankelijkheid te plaatsen, of wanneer het toevoegen van een segment of een regel aan een besluitvormingswerkingsgebied.