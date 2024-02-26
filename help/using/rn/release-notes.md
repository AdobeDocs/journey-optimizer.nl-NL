---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
description: Aanvullende informatie voor Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ee33923ff5bfb73974935864c7e241ea4b0353c5
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 7%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} vandaag, en ontvang de recentste productupdates, opwindende verhalen, gebruiksgevallen, uiteinden en meer die direct aan uw Postbus worden geleverd elk kwartaal.

## Opmerkingen bij de release februari 2024 {#feb-2024}

**Releasedatum**: 21 februari 2024

### Nieuwe functies{#feb-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.


<table>
<thead>
<tr>
<th><strong>Webberichten in de app</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt het nieuwe Web in-App overseinenvermogen nu gebruiken om gepersonaliseerde inhoud direct op websites, door modaal-bekledingsberichten te tonen. Met deze functie kunt u effectief contact opnemen met webbezoekers, waardoor de interactie, het behoud en de conversiesnelheden van gebruikers worden verbeterd.<br/><br/></p>
<p>Raadpleeg de <a href="../in-app/create-in-app-web.md">gedetailleerde documentatie</a> voor meer informatie.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Sjablonen voor multikanaalsinhoud</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Naast E-mail, zijn de inhoudsmalplaatjes nu beschikbaar voor de volgende kanalen: Duw, In-app, SMS en Directe post, elk kanaal dat specifieke malplaatjetypes heeft. Voor E-mail, kunt u het inhoudstype nu selecteren, dat u toestaat om de onderwerpregel als deel van uw e-mailmalplaatje te bewaren. <br/><br/></p>
<p>Raadpleeg de <a href="../content-management/content-templates.md">gedetailleerde documentatie</a> voor meer informatie.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif">
</tr>
</tbody>
</table>


### Verbeteringen {#feb-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Doelgroepen**

* **Zaadlijsten** - Varianten worden nu ondersteund bij gebruik **zaadlijsten**. De zaadadressen ontvangen een exemplaar van alle varianten van het zelfde bericht (zoals de verschillende behandelingen van een inhoudexperiment). [Meer informatie](../configuration/seed-lists.md)

Eerder beschikbaar als Beta, zijn de volgende verbeteringen nu beschikbaar aan alle gebruikers:

* U kunt nu **publiek gemaakt via publiekscompositie** en verrijkingskenmerken gebruiken in Reizen. [Meer informatie](../building-journeys/read-audience.md)

* U kunt nu **publiek geüpload uit een CSV-bestand** in reizen en campagnes. [Meer informatie](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* Het gebruik van soorten publiek en kenmerken van de compositie van het publiek en aangepaste upload (CSV-bestand) is momenteel niet beschikbaar voor gebruik met het gezondheidsschild of het privacyschild.
  >* De **publiek uploaden uit een CSV-bestand** de verbetering wordt geleidelijk doorgevoerd in de loop van enkele dagen na de eerste introductie . Terwijl sommige gebruikers directe toegang hebben, kunnen anderen een vertraging ervaren alvorens het in hun milieu beschikbaar wordt.

**Reizen**

* **Uw reizen filteren** - U kunt nu **aangepaste datums om de reizen te filteren** voorraad, naast de bestaande vooraf gedefinieerde datumfilters. Op deze manier kunt u de lijst verfijnen door ritten weer te geven die op een bepaalde datum zijn gemaakt of gepubliceerd, binnen een bepaalde maand, gedurende een heel jaar of binnen een opgegeven tijdbereik. [Meer informatie](../building-journeys/journey-gs.md#filter)
* **Aangepaste acties** - U kunt nu het dialoogvenster **inhoudstype** header. Deze nieuwe **inhoudstype** verwijst naar JSON-inhoud. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)
* **Configuratie** - Het attribuut identityMap in stepEvents is nu voorgevuld. De primaire identiteit wordt gedefinieerd als &quot;primary = true&quot;. [Meer informatie](../reports/sharing-field-list.md)
* **Gebruikersinterface** - De bovenste balk, in reisschermen, is gereorganiseerd voor een betere ervaring. Onder de verschillende updates ziet u dat het potlood-pictogram waarmee u de reiseigenschappen kunt openen nu links van de bovenste balk naast de naam van de rit wordt weergegeven. [Meer informatie](../building-journeys/journey-gs.md#change-properties)

**Sms-kanaal**

* **Trefwoorden voor aanmelden/uitschakelen** - Wanneer u uw SMS-kanaal configureert, kunt u nu het **Trefwoorden voor Inschakelen en Uitschakelen** volgens uw voorkeuren. Journey Optimizer activeert de reactie op basis van deze opgegeven trefwoorden. [Meer informatie](../sms/sms-configuration.md#create-api)

**Campagnes**

* **API-gestuurde campagnes** - De cURL-code die is gegenereerd na het activeren van een API-geactiveerde campagne is verbeterd. Het omvat nu alle personaliseringsvariabelen (profiel en context) die in het bericht worden gebruikt. [Meer informatie](../campaigns/api-triggered-campaigns.md#execute)

**Frequentieregels**

* Naast E-mail en Duw, kunt u de regels van de Frequentie voor SMS en Directe kanalen van de Post nu tot stand brengen. De frequentieregels sluiten over-gevraagde profielen automatisch uit van berichten en acties wanneer de frequentiedrempel wordt bereikt. [Meer informatie](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->

<!--
**Content templates**

* **Thumbnails** - A **Grid view** is now available for content templates for improved visual access.

   >[!AVAILABILITY]
   >
   >This capability is released in Limited Availability (LA) for a small set of customers.
-->


## Opmerkingen bij de release januari 2024 {#jan-2024}

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
<p>Vanaf 1 februari 2024, Google en Yahoo! vereisen dat u een DMARC-record hebt voor elk domein dat u gebruikt om e-mail naar hen te verzenden. Zorg ervoor dat u DMARC- verslag opstelling voor alle subdomeinen hebt hebt die u of aan Adobe in Journey Optimizer hebt gedelegeerd.</p>
<p>Raadpleeg de <a href="../configuration/dmarc-record-update.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Playbooks voor gebruiksscenario</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gebruik een catalogus met branchespecifieke gebruiksscenario's voor afspeelboeken in Real-Time CDP en Journey Optimizer om veelvoorkomende gebruikssituaties aan te pakken die u kunt uitvoeren met Adobe Experience Platform en Adobe Journey Optimizer.</p><p>Zodra u playbook hebt gekozen die het best aan uw behoeften past, kunt u het toelaten om de activa te produceren nodig om uw gebruikscase zoals reizen, berichten, schema's of segmenten te steunen, en hen aan uw schema voor snellere tijd aan waarde aan te passen.</p>
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

* Steun voor `<listObject>` is gewijzigd in meerdere functies.

**Frequentieregels**

* **Wekelijks en dagelijks frequentiegrens** - U kunt nu het maximum aantal berichten opgeven dat naar een klantprofiel wordt verzonden in een week of een dag, in aanvulling op de maand. De maximale frequentie is gebaseerd op de geselecteerde kalenderperiode en wordt opnieuw ingesteld aan het begin van het corresponderende tijdkader. [Meer informatie](../configuration/frequency-rules.md#create-new-rule)


**Beslissingsbeheer**

* **Frequentiecorrectie op rand** - De teller van de frequentiecappend wordt nu bijgewerkt en beschikbaar in een besluit van de Beslissing API van de Rand in minder dan 3 seconden. [Meer informatie](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
