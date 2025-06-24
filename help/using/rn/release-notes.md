---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3282f2f5b6fa4eacafc4b017ea0ca713b90cab82
workflow-type: tm+mt
source-wordcount: '1176'
ht-degree: 8%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** levert onophoudelijk nieuwe eigenschappen, verhogingen aan bestaande eigenschappen, en insectenmoeilijke situaties. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen. [!DNL Adobe Journey Optimizer] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=nl-NL){target="_blank"}.


## Opmerkingen bij de release van juni &#39;25 {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**de datum van de Versie**: 18 Juni, 2025

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/nl/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Nieuwe functies {#25-06-features}

De nieuwe mogelijkheden die met deze release worden geleverd, worden hieronder beschreven.

<table>
<thead>
<tr>
<th><strong>Adobe Experience Platform datasets in decisions (bèta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform-gegevenssets die voorheen beschikbaar waren voor personalisatie, kunnen nu worden gebruikt voor beslissingen. Dit staat u toe om de definitie van uw beslissingsattributen tot extra gegevens in datasets voor bulkupdates uit te breiden die periodiek veranderen zonder het moeten manueel de attributen één voor één bijwerken. Bijvoorbeeld beschikbaarheid, wachttijden, enz.</p>
<p>Deze mogelijkheid is momenteel beschikbaar voor alle klanten als een openbare bètaversie. Neem contact op met uw accountvertegenwoordiger als u toegang wilt.</p>
<p>Raadpleeg de <a href="../experience-decisioning/aep-data-exd.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 20 juni 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>RCS-berichten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Het Rich Communication Services (RCS) overseinen wordt nu gesteund in Journey Optimizer, toelatend de volgende verbeterde overseinenmogelijkheden afhankelijk van leverancier en dragersteun:</p>
<ul>
<li>Branded en de geverifieerde steun van de afzender: verzend berichten gebruikend geverifieerde bedrijfsprofielen met branding elementen (embleem, afzendernaam, enz.).</li>
<li>Inzichten van de levering van berichten: Ontvang gedetailleerde leveringsrapporten met inbegrip van updates van de berichtstatus (b.v., verzonden, geleverd, gelezen).</li>
<li>Koppelingentracering: sluit URL's in RCS-berichten in en traceer deze voor betrokkenheidsanalyses.</li>
<li>Terugvallen op SMS: Automatische fallback aan SMS wanneer het apparaat van het profiel geen RCS steunt of tijdelijk onbereikbaar via RCS is.</li>
<li>Basisberichtcompositie: Verstuur op tekst gebaseerde RCS-berichten met optionele media en rijke elementen, afhankelijk van de providerondersteuning.</li>
</ul>
<p>Raadpleeg de <a href="../sms/sms-configuration.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formuliervelden in ervaringsinhoud op basis van code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu specifieke bewerkbare velden definiëren in JSON- of HTML-inhoudssjablonen, waarmee niet-technische gebruikers inhoud eenvoudig kunnen bewerken in een formulierweergave in de op code gebaseerde ervaring in het maken van kanalen zonder dat ze code hoeven te bewerken.<br /> meer dan dat, wanneer het bepalen van de code-gebaseerde malplaatjes van de ervaringsinhoud kunt u besluitvormingsbeleid in het malplaatje nu opnemen, die herbruikbaarheid en gebruiksgemak verhogen.</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>Raadpleeg de <a href="../code-based/code-based-form-fields.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Activiteiten in verband met inhoudsbeslissingen tijdens reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu persoonlijke aanbiedingen opnemen in uw reizen door middel van een speciale actie voor het nemen van beslissingen over inhoud in het reiscanvas en deze gebruiken in reisactiviteiten, waaronder voorwaarden en aangepaste acties.</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid) en wordt globaal geïmplementeerd in een toekomstige release.</p>
<p>Raadpleeg de <a href="../building-journeys/content-decision.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reizen op reis</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Reis Dry run is een speciale publicatiemodus in Adobe Journey Optimizer die reisartsen in staat stelt een reis te testen met behulp van echte productiegegevens zonder contact op te nemen met echte klanten of profielinformatie bij te werken. Deze functie helpt reisartsen vertrouwen te winnen in hun reisontwerp en doelgroep voordat ze het live publiceren.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid) en wordt globaal geïmplementeerd in een toekomstige release.</p>
<p>Raadpleeg de <a href="../building-journeys/journey-dry-run.md">gedetailleerde documentatie</a> voor meer informatie.</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reizen onderbreken en hervatten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu uw reizen pauzeren en hervatten. Deze mogelijkheid geeft reisartsen meer controle en flexibiliteit door het tijdelijk stilleggen van de actieve reizen toe te staan zonder de ervaring van de klant te verstoren. Wanneer gepauzeerd, worden geen mededelingen verzonden, en de profielen blijven in een geschorste staat tot de reis wordt hervat.</p>
<p>U kunt slechts één reis pauzeren en hervatten, of bulkpauze uitvoeren en verrichtingen aan een groep reizen hervatten.</p>
<p>Bovendien kunt u algemene filters toepassen op gepauzeerde reizen om profielen uit te sluiten op basis van hun kenmerken.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid) en wordt globaal geïmplementeerd in een toekomstige release.</p>
<p>Raadpleeg de <a href="../building-journeys/journey-pause.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Schaal de winnaar van uw proefversie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Schaal de winnaar van de proefversie kunt u de winnende variatie van een experiment automatisch of handmatig voor alle gebruikers uitrollen. Deze functie zorgt ervoor dat u, zodra een topuitvoerder is geïdentificeerd, het bereik en de effectiviteit ervan kunt maximaliseren zonder voortdurend handmatig toezicht.</p>
<p>Raadpleeg de <a href="../content-management/content-experiment.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 2 juni 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflict en prioriteit</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer is het beheren van het volume en de timing van campagnes en reizen van essentieel belang om te voorkomen dat klanten met te veel interacties worden overspoeld. Journey Optimizer biedt nu diverse hulpmiddelen voor conflictbeheer en prioritering - voorheen alleen beschikbaar voor organisaties met beperkte toegang (LA) - die nu algemeen beschikbaar zijn (GA).</p>
<p>Eerder uitgebracht in Beperkte Beschikbaarheid, is deze capaciteit nu beschikbaar aan alle milieu's. Met deze algemene release zijn de volgende verbeteringen aangebracht:</p>
<ul>
<li>Uitgebreide ondersteuning: de tools voor conflictbeheer ondersteunen nu niet alleen publiekstrajecten, maar ook eenheidsreizen en kwalificatiereizen voor het publiek.</li>
<li>Verbeterd het Oplossen van problemen: Twee nieuwe gebieden van de stapgebeurtenis zijn nu beschikbaar in de Dienst van de Vraag, toelatend u om te analyseren waarom een profiel van een reis of een campagne werd verworpen.</li>
<li>Verbeterde rapportage: in rapporten wordt nu aangegeven welke specifieke regel een profiel van een reis of campagne heeft uitgesloten, waardoor meer transparantie en activeerbare inzichten worden geboden.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Raadpleeg de <a href="../conflict-prioritization/gs-conflict-prioritization.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>Beschikbaarheidsdatum: 3 juni 2025</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#25-06-improv}

De verbeteringen die bij deze release worden geleverd, worden hieronder weergegeven.

* **de regelreeksen van het Kanaal**

   * **venster van de Duur van de Douane** voor het in kaart brengen - een nieuw **Elk** gebied is nu beschikbaar in het scherm van de de reeksen van de kanaalregel, toestaand u om de regels van de frequentie het in kaart brengen over veelvoudige dagen, weken, of maanden, afhankelijk van de gespecificeerde duur toe te passen.

   * **de frequentie van het terugstellen van de Uur het afschilderen** - u kunt het afschilderen op een uurbasis voor de reeksen van de kanaalregel nu toepassen. Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met de klantenservice om de functie in te schakelen.

   * **Dagelijkse duur** - eerder beschikbaar in Beperkte Beschikbaarheid, &quot;Dagelijkse&quot;frequentietoewijzing in de reeksen van de kanaalregel is nu beschikbaar aan alle klanten.

  Raadpleeg de [gedetailleerde documentatie](../conflict-prioritization/channel-capping.md) voor meer informatie.

* **op code-gebaseerde ervaringen**

   * Het toevoegen van een besluitvormingsbeleid is nu beschikbaar in code-gebaseerde malplaatjes van de ervaringsinhoud, waar het aan hefboomwerking aanbiedingen in editable vormgebieden kan worden gebruikt. [Meer informatie](../code-based/code-based-form-fields.md)

   * Van het op code-gebaseerde de ervaringstraject of scherm van de campagneuitgave, kunt u direct een besluitvormingsbeleid toevoegen, zonder de verpersoonlijkingsredacteur te openen. [Meer informatie](../code-based/create-code-based.md#edit-code)

* **de Steun van CSS van de Douane in E-mail Designer**

  Met Journey Optimizer kunt u nu aangepaste CSS rechtstreeks in de e-mailtoepassing toevoegen aan uw e-mailinhoud. [Meer informatie](../email/custom-css.md)

* **Nieuwe van labels voorzien navigatie voor campagnes**

  Een nieuw navigatiepatroon maakt snellere toegang tot het ontwerpen van inhoud mogelijk en ondersteunt verdere uitbreiding van instellingen in alle campagnes. [Meer informatie](../campaigns/create-campaign.md)

* **Beslissing**

   * **Sandbox exemplaar &amp; Beslissing** (beschikbaarheidsdatum: 3 Juni, 2025) - De beslissende voorwerpen kunnen nu tussen zandbakken worden gekopieerd, die het testen en plaatsingswerkschema&#39;s stroomlijnen. [Meer informatie](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **de kenmerksteun van het Punt van het Besluit voor besluitvormingsregels** (beschikbaarheidsdatum: 4 juni, 2025) - u kunt de attributen van het besluitvormingspunt nu hefboomwerking besluiten om besluitvormingsregels tot stand te brengen. [Meer informatie](../experience-decisioning/rules.md#create)

* **Interactieve update van API van de Uitvoering van het Bericht** - de datum van de Beschikbaarheid: 6 juni, 2025

  De Interactieve API van de Uitvoering van het Bericht staat u nu toe om het programma van aanstaande campagneuitvoering te schrappen. [Meer informatie](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
