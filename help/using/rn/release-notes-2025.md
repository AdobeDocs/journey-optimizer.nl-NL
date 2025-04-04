---
solution: Journey Optimizer
product: journey optimizer
title: Opmerkingen bij de release 2025
description: Opmerkingen bij de release van Journey Optimizer 2025
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: e80554570d62d1ddb52516366be55711387c5d19
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 7%

---

# Aanvullende informatie 2025 {#release-notes-2025}

Deze pagina bevat een overzicht van alle functies en verbeteringen die [!DNL Journey Optimizer] in 2025 heeft uitgebracht.

## Opmerkingen bij de release van februari &#39;25 {#25-02-rn}

**de datum van de Versie**: 18-19 februari, 2025


### Nieuwe functies {#25-02-features}

De nieuwe mogelijkheden die met deze release worden geleverd, worden hieronder beschreven.

<table>
<thead>
<tr>
<th><strong>Zakelijke regels maken en beheren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu bedrijfsregels maken met behulp van regelsets. Regelsets zijn groepen regels die u helpen verzonden berichten binnen campagnes en reisacties te beperken over kanalen, en om de invoer van profielen in reizen te controleren.<p>
<p><ul><li>Creeer kanaalregelreeksen om het aantal berichten te beperken die over één of veelvoudige kanalen worden verzonden. Pas ze toe op campagnes of reisacties om de regels af te dwingen die zijn gedefinieerd in de regelset. De de regelreeks van het kanaal staat u toe om het begrenzen regels toe te passen die op communicatie types worden gebaseerd. Stel bijvoorbeeld een regel in die is ingesteld op het beperken van 'promotionele berichten' en een andere regel voor 'nieuwsbrieven'. Pas de toepasselijke regel toe die in uw campagne of reisactie is ingesteld, afhankelijk van het type communicatie dat u verzendt.</li>
<li> Reisregelsets maken om profielinvoer in reizen te regelen. Beperk hoe vaak een profiel een reis binnen een bepaalde periode kan ingaan of het aantal reizen een profiel kan gelijktijdig worden ingeschreven. Pas deze toe op het niveau van de reis om te zorgen voor een goed beheer van de toegang.</li></ul></p>
<p>Eerder beschikbaar voor een reeks organisaties (LA), zijn de bedrijfsregels nu beschikbaar aan alle gebruikers (GA). De bedrijfsregels voor het domein van de reis blijven slechts beschikbaar voor een beperkte reeks organisaties (LA).</p>
<p>Raadpleeg de <a href="../configuration/rule-sets.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Landingspagina's genereren met de AI-assistent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu boeiende inhoud voor uw openingspagina's, met inbegrip van volledige paginaontwerpen, gepersonaliseerde tekst, en aangepaste visuele hulpmiddelen, met de hulp van de AI medewerker ambachtelijk maken.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>Raadpleeg de <a href="../content-management/generative-lp.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Merken met de AI Assistant (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu uw eigen merken instellen om de visuele en verbale identiteit van uw merk te definiëren. </p>
<p>Deze mogelijkheid wordt als een persoonlijke bètaversie vrijgegeven aan een beperkt aantal klanten. Het zal in toekomstige versies geleidelijk beschikbaar zijn voor alle klanten.</p>
<p>Raadpleeg de <a href="../content-management/brands.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aangepaste acties oplossen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu een aangepaste actieconfiguratie valideren door echte API-aanroepen rechtstreeks vanuit Adobe Journey Optimizer te maken. Deze nieuwe mogelijkheid helpt u bij het oplossen van problemen met uw aangepaste handelingen voordat of nadat u deze hebt gebruikt voor een reis. </p>
<p>Raadpleeg de <a href="../action/troubleshoot-custom-action.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Flexibele publieksevaluatie (Beperkte Beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dankzij de flexibele publieksevaluatie kunt u een segmentatietaak uitvoeren op aanvraag voor een geselecteerd publiek, zodat u altijd over de meest actuele publieksgegevens beschikt voordat u deze doelt op Journey Optimizer-reizen en -campagnes.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Raadpleeg de <a href="../audience/creating-a-segment-definition.md#flexible">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.</p>
<p>Beschikbaarheidsdatum: 28 januari 2025</p>
</tr>
</tbody>
</table>
</table>


### Verbeteringen {#25-02-improvements}

De verbeteringen hieronder komen met de update van februari.

* **Tijd-aan-levende Dataset (TTL)** - Beginnend deze maand, zal een tijd-aan-levende (TTL) guardrail aan systeem-geproduceerde datasets van Journey Optimizer in nieuwe zandbakken en nieuwe organismen als volgt worden uitgerold:

   * 90 dagen voor gegevens in de profielopslag
   * 13 maanden voor gegevens in het data Lake

  Deze wijziging wordt in een volgende fase doorgevoerd in bestaande sandboxen voor klanten.

  Leer meer over deze update in [ specifieke FAQ ](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Directe post** - een nieuw servertype, Gegevens landende streek, wordt nu gesteund voor dossier dat in de directe configuratie van het postkanaal verplettert. [Meer informatie](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS** - u kunt SMS berichtlevering van multi-regionale eindpunten nu beheren door levering, terugkoppelen, binnenkomend, en callback URLs te overschrijven. Ter ondersteuning hiervan is een nieuwe veld Overschrijf-URL toegevoegd aan de configuratie van API-referenties. Deze wijziging is alleen beschikbaar bij de Sinch-provider. [Meer informatie](../sms/sms-configuration-sinch.md)

* **Personalization** (de datum van de Beschikbaarheid: Jan 29, 2025) - de Nieuwe datum/tijdhulpfuncties zijn beschikbaar voor gebruik in de verpersoonlijkingsredacteur. [Meer informatie](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **E-mailconfiguratie** - als u toestemming buiten Adobe beheert, kunt u een douane plaatsen unsubscribe e-mailadres en een douane één-klik unsubscribe URL als deel van uw montages van de de kanaalconfiguratie van e-mail. [ las meer ](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Beslissing** (de datum van de Beschikbaarheid: Jan 28, 2025) - het Besluiten steunt nu de gegevenstypes van Objecten wanneer het uitgeven van het schema van de puntcatalogus. [Meer informatie](../experience-decisioning/catalogs.md)

