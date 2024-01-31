---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
description: Aanvullende informatie voor Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 283983d98905b8e36d41823d1fae5d7a3c269ba3
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 6%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} vandaag, en ontvang de recentste productupdates, opwindende verhalen, gebruiksgevallen, uiteinden en meer die direct aan uw Postbus worden geleverd elk kwartaal.

## Opmerkingen bij de vervroegde release januari 2024 {#jan-2024}

**Releasedatum**: 30-31 januari 2024

### Nieuwe functies{#jan24-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.

<table>
<thead>
<tr>
<th><strong>Updates van de leverbaarheid</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ondersteunt nu de DMARC-verificatietechnologie.</p>
<p>Vanaf 1 februari 2024, Google en Yahoo! u hebt een DMARC-record nodig voor elk domein dat u gebruikt om e-mail naar hen te verzenden. Zorg ervoor dat u DMARC- verslag opstelling voor alle subdomeinen hebt hebt die u of aan Adobe in Journey Optimizer hebt gedelegeerd.</p>
<p>Raadpleeg de <a href="../configuration/dmarc-record-update.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Hoofdletters gebruiken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gebruik een catalogus met branchespecifieke gebruiksscenario's in Real-Time CDP en Journey Optimizer om veelvoorkomende gebruiksgevallen aan te pakken die u kunt uitvoeren met Adobe Experience Platform en Adobe Journey Optimiser.</p><p>Zodra u playbook hebt gekozen die het best aan uw behoeften past, kunt u het toelaten om de activa te produceren nodig om uw gebruikscase zoals reizen, berichten, schema's of segmenten te steunen, en hen aan uw schema voor snellere tijd aan waarde aan te passen.</p>
<p>Raadpleeg de <a href="../start/playbooks.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Verbeteringen {#jan24-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Rapportage**

* **Nieuwe op domein gebaseerde widgets voor indeling** - Er zijn nieuwe widgets toegevoegd om uw campagne- en journalistieke rapporten te verbeteren. De **Bounce Reden per domein**, **Verzonden en geleverd op domeinen**, **Opent en klikt op domein** en **Stuiteren en fouten per domein** widgets bieden een gedetailleerde uitsplitsing op domeinniveau voor belangrijke gegevens voor het verzenden van e-mail en het bijhouden van gegevens. [Meer informatie](../reports/channel-report.md)

**SMS-kanaal**

* **Dubbele plug-in** - De dubbele Opt-In workflow voor SMS garandeert dat gebruikers zich expliciet aanmelden om berichten te ontvangen wanneer het verzoek van hun apparaat wordt geïnitieerd. Gebruikers starten het goedkeuringsproces door een binnenkomend SMS-bericht te verzenden. Na bevestiging van hun toestemming wordt een vervolgbericht verzonden waarin om een definitieve verificatie wordt verzocht. Als een gebruikersprofiel niet bestaat, wordt het gecreeerd na succesvolle bevestiging. [Meer informatie](../sms/sms-configuration.md#create-api)

  Merk op dat dit vermogen met de leveranciers van SMS van Sinch en Infobip beschikbaar is.

**Reizen**

* **Duur van reactiegebeurtenissen** - De maximale duur die u kunt definiëren in het dialoogvenster **Gebeurtenissen van Reaction** is nu 29 dagen in plaats van 30. [Meer informatie](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Lees publiek**  - de **Publiek lezen** De activiteit baseert zich nu op de dataset van de profielmomentopname voor partijsegmenten, die slechts eenmaal per dag wordt geproduceerd nadat de geplande dagelijkse partijbaan in werking wordt gesteld, vandaar zullen de gegevens tot die laatste dagelijkse partijbaan vers zijn. [Meer informatie](../building-journeys/read-audience.md)

* **Veldgroepen** - Deze release verhelpt een probleem dat ervoor zorgde dat Veldgroepen in bepaalde gevallen niet konden worden opgeslagen.

**Frequentieregels**

* **Wekelijks en dagelijks frequentiegrens** - U kunt nu het maximum aantal berichten opgeven dat naar een klantprofiel wordt verzonden in een week of een dag, in aanvulling op de maand. De maximale frequentie is gebaseerd op de geselecteerde kalenderperiode en wordt opnieuw ingesteld aan het begin van het corresponderende tijdkader. [Meer informatie](../configuration/frequency-rules.md#create-new-rule)

**Beslissingsbeheer**

* **Frequentiecorrectie op rand** - De teller van de frequentiecappend wordt nu bijgewerkt en beschikbaar in een besluit van de Beslissing API van de Rand in minder dan 3 seconden. [Meer informatie](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)