---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b3e683e503f1784d61f6de4f0d866fc965515c1c
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 8%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** levert onophoudelijk nieuwe eigenschappen, verhogingen aan bestaande eigenschappen, en insectenmoeilijke situaties. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen.

[!DNL Adobe Journey Optimizer] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html) {target="_blank"}.

![ Nieuwsbrief ](../assets/do-not-localize/nl-icon.png) Teken omhoog voor het [ driemaandelijkse bulsletter van Adobe Journey Optimizer ](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html) {target="_blank"} vandaag, en ontvang de recentste productupdates, opwindende verhalen, gebruiksgevallen, uiteinden en meer die rechtstreeks aan uw inbox elk kwart worden geleverd.

## Updates september {#9-2024}

<table>
<thead>
<tr>
<th><strong>AI Assistant - Inhoud versnellen </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als je bericht eenmaal hebt gemaakt en gepersonaliseerd, ga je naar het volgende niveau met de AI Assistant in Journey Optimizer for Content Acceleration. U kunt de AI-assistent nu gebruiken om de impact van uw bericht te optimaliseren door te experimenteren met verschillende hoofdtitels en afbeeldingen. Elke variant wordt beheerd als een unieke behandeling, om te meten en te vergelijken welke titel effectief meer kliks produceert.</p>
<p>Ga zelf in een hands-on ervaring met <a href="https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator"> binnen onze levende eigenschapvoorproef </a>, die wordt ontworpen om u zijn eigenschappen eerst te laten onderzoeken en volledig zijn mogelijkheden te begrijpen.</a></p>
<p>Raadpleeg de <a href="../content-management/gs-generative.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/ai-content.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Kanaal instellen met instructies</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met de functie Kanaalinstellingen met instructies kunt u kanaalinstellingen in één ervaring automatiseren en valideren, zodat u sneller aan de slag kunt met Journey Optimizer. Deze nieuwe, geleide opstelling stroomlijnt snelle kanaalconfiguratie, die ervoor zorgt dat alle noodzakelijke middelen gemakkelijk worden geïnstalleerd en binnen Experience Platform, Journey Optimizer, en de Inzameling van Gegevens werken. Hierdoor kunnen marketing-, product- en gegevensontwikkelingsteams snel beginnen met het maken van campagnes en reizen.</p>
<p>Raadpleeg de <a href="../configuration/set-mobile-config.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/guided-setup.gif"/>
<p>Beschikbaarheidsdatum: september 3</p>
</br>
</td>
</tr>
</tbody>
</table>

**Reizen**

(De datum van de Beschikbaarheid: Sept 10) **probeert vermogen** opnieuw - is nu toegepast door gebrek op publiek-getriggerde reizen (die met a **Gelezen Publiek** of a **BedrijfsGebeurtenis** beginnen) terwijl het terugwinnen van de uitvoerbaan. Als er een fout optreedt tijdens het maken van de exporttaak, worden de pogingen om de 10mn opnieuw uitgevoerd, tot maximaal 1 uur. Daarna zullen we het als een mislukking beschouwen. Deze soorten reizen kunnen daarom tot 1 uur na de geplande tijd worden uitgevoerd. [Meer informatie](../building-journeys/read-audience.md#retries)

## Opmerkingen bij de release augustus 2024 {#8-2024}

**de datum van de Versie**: Augustus 20-21, 2024

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

### Nieuwe functies {#8-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden beschreven.

<!--
<table>
<thead>
<tr>
<th><strong>Content Cards (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content cards are a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</br>
<p>Content card are currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Verbeterde kanaalconfiguraties</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De huidige mogelijkheden van het kanaaloppervlak zijn verbeterd voor een consistente aanpak op alle kanalen. U kunt deze configuraties nu definiëren, beheren en opnieuw gebruiken voor al uw kanalen, zoals Web, In-app-berichten of Code-gebaseerde ervaring.</p>
<p><ul>
<li>De oppervlakten van het kanaal worden nu anders genoemd aan <strong> configuraties van het Kanaal </strong></li>
<li>U kunt één of meerdere marketing acties verbinden om toestemmings en gegeven beheersbeleid te handhaven</li>
<li>Het toegangsbeheer van het niveau van objecten (OLAC) is nu beschikbaar voor elke kanaalconfiguratie, toestaand u om te beslissen welke van uw gebruikers specifieke configuraties mogen tot stand brengen of gebruiken</li>
<li>Voor sommige kanalen kunt u kanaalconfiguraties maken die op meerdere platforms zijn gericht. Een voorbeeld hiervan is een in-app berichtkanaalconfiguratie die zich kan richten op een webpagina, een iOS-app en een Android-app.</li>
</ul></p>
<p>Raadpleeg de <a href="../configuration/channel-surfaces.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

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
<p>Raadpleeg de <a href="../action/marketo-engage.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Variabelen in inhoudsfragmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Globale fragmentvariabelen verbeteren de bestaande fragmentfunctionaliteit om de herbruikbaarheid van inhoud en het gebruik van scripts te verbeteren. Fragmenten kunnen nu invoervariabelen gebruiken en uitvoervariabelen maken die bruikbaar zijn in campagne- en reisinhoud. De fragmenten kunnen inputvariabelen verbruiken, zowel in <a href="../personalization/use-expression-fragments.md"> uitdrukkingsfragmenten </a> als <a href="../email/use-visual-fragments.md"> visuele fragmenten </a>. U kunt deze variabelen gebruiken om uw berichtinhoud en parameters, in uw campagnes en reizen te personaliseren.</p>
<p>Raadpleeg de <a href="../personalization/use-expression-fragments.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</p>
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
<p>Beschikbaarheidsdatum: aug, 13</p>
<p>Als u e-mail op een gloednieuw IP adres verzendt, kunt u IP opwarmingswerkschema's nu gemakkelijk direct van het gebruikersinterface uitvoeren. Adobe Journey Optimizer biedt een gestandaardiseerde en efficiënte manier om uw IP adressen op te warmen die de beste praktijken voor optimale leverbaarheid volgen.</p>
<p>Raadpleeg de <a href="../configuration/ip-warmup-gs.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#8-improvements}

Deze release brengt de hieronder vermelde verbeteringen aan.

**Reizen**

* In de **activiteit van de Voorwaarde**, door gebrek, wordt **[!UICONTROL Time condition]** nu geplaatst door uur, van 00:00 tot 12:00. [Meer informatie](../building-journeys/condition-activity.md#time_condition)
* Wanneer het bouwen van uw reizen, worden het alarm nu getoond van de **Alarm** knoop, om met andere alarm te richten en een verenigbare gebruikerservaring te brengen. [Meer informatie](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* De zoomopties op de werkbalk voor reizen zijn verbeterd. Het zoompercentage is nu zichtbaar en u kunt de zoomwaarde nu eenvoudiger herstellen.

<!--**Audiences and Profiles**-->

<!--* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield add-on.-->
<!--* When targeting a custom upload (CSV file) audience, you can now use attributes from the file in your campaigns and journeys. These attributes are available in the personalization editor, to personalize your messages, and the journey advanced expression editor.-->
<!--* The License usage dashboard now shows the count of Engageable Profiles. [Read more](../audience/license-usage.md)-->

**het kanaal van de duw**

* U kunt nu uw pushgegevens voor mobiele toepassingen toevoegen in de configuratie-instellingen voor Adobe Journey Optimizer-kanalen. Het maken van een App-oppervlak in Adobe Experience Platform Data Collection is niet langer vereist.

### Andere wijzigingen {#changes}

**Meldend**

* De huidige ervaring met rapportage wordt vanaf de release van oktober opgeheven. Na deze datum wordt de nieuwe ervaring met rapportage de norm. We raden u aan bekend te maken met de nieuwe functies en functies om een soepele overgang te garanderen.

[Ga aan de slag met de nieuwe rapportinterface van Journey Optimizer](../reports/report-gs-cja.md)

* Nieuwe gebruiksgevallen zijn toegevoegd aan de nieuwe ervaring met rapportage:

   * U kunt aangepaste berekende metriek rechtstreeks in uw rapporten maken.
   * Creeer een Publiek van het melden van gegevens.
   * Met het gereedschap Verkennende analyse kunt u eenvoudig tabellen en visualisaties maken op basis van de geselecteerde **[!UICONTROL Dimensions]** en **[!UICONTROL Metrics]** .

  Raadpleeg de [gedetailleerde documentatie](../reports/report-cja-manage.md) voor meer informatie.
