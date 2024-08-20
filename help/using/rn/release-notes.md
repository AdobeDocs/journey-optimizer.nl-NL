---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
description: Aanvullende informatie voor Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d971d857a480868f5ef502f3a3f2c209afc93cca
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 6%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** levert onophoudelijk nieuwe eigenschappen, verhogingen aan bestaande eigenschappen, en insectenmoeilijke situaties. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen.

[!DNL Adobe Journey Optimizer] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html) {target="_blank"}.

![ Nieuwsbrief ](../assets/do-not-localize/nl-icon.png) Teken omhoog voor het [ driemaandelijkse bulsletter van Adobe Journey Optimizer ](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html) {target="_blank"} vandaag, en ontvang de recentste productupdates, opwindende verhalen, gebruiksgevallen, uiteinden en meer die rechtstreeks aan uw inbox elk kwart worden geleverd.

## Opmerkingen bij de vervroegde release augustus 2024 {#e-2024}

**de datum van de Versie**: Augustus 20-21, 2024

>[!CAUTION]
>
>**de vroege versienota&#39;s hieronder zijn onderworpen aan verandering zonder voorafgaande kennisgeving tot de versiedatum**. Koppelingen, schermen en bijgewerkte documentatie worden gepubliceerd op de releasedatum.
>

### Nieuwe functies {#e-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden beschreven.

<!--table>
<thead>
<tr>
<th><strong>Guided Channel Setup</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Guided Channel Setup enables you to automate and validate channel setup in a unified experience, speeding up the process of getting started with Journey Optimizer. This new guided setup streamlines rapid channel configuration, ensuring all necessary resources are readily installed and working within Experience Platform, Journey Optimizer, and Data Collection. This enables marketing, product and data engineering teams to quickly begin with campaign and journey creation.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Content Cards</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content card is a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Improved Channel Configurations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The current channel surface capabilities have been enhanced for a consistent approach across all channels. You can now define, manage, and reuse these configurations for any of your channels, including Web, In-app messaging, or Code-based experience.</p>
<p><ul>
<li>Channel surfaces are now renamed to <strong>Channel configurations</strong></li>
<li>You can attach one or multiple marketing actions to enforce consent and data governance policies</li>
<li>Object level access control (OLAC) is now available for each channel configuration, allowing you to decide which of your users are allowed to create or use specific configurations</li>
<li>For some channels, you can create channel configurations that target multiple platforms. An example here would be an In-app messaging channel configuration that can target a web page, an iOS app and an Android app.</li>
</ul></p>
</td>
</tr>
</tbody>
</table-->

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
<th><strong>Variabelen in inhoudsfragmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De fragmenten kunnen nu inputvariabelen, zowel in <a href="../personalization/use-expression-fragments.md"> uitdrukkingsfragmenten </a> als <a href="../email/use-visual-fragments.md"> visuele fragmenten </a> verbruiken. U kunt deze variabelen gebruiken om uw berichtinhoud en parameters, in uw campagnes en reizen te personaliseren.</p>
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


### Verbeteringen {#e-improvements}

Deze release brengt de hieronder vermelde verbeteringen aan.

**Reizen**

<!--* In the **Condition** activity, by default, the Time condition is now set by hour, from 00:00 to 12:00. [Read more](../building-journeys/condition-activity.md#time_condition)-->
* Wanneer u uw reizen maakt, worden waarschuwingen nu weergegeven in een vervolgkeuzelijst, zodat deze kunnen worden afgestemd op campagnewaarschuwingen en een consistente gebruikerservaring mogelijk maken. [Meer informatie](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* De zoomopties op de werkbalk voor reizen zijn verbeterd. Het zoompercentage is nu zichtbaar en u kunt de zoomwaarde nu gemakkelijk terugzetten op 100%.

**Doelgroepen**

* Het gebruik van soorten publiek via aangepaste upload (CSV-bestand) is nu beschikbaar voor gebruik met de invoegtoepassing Privacy en beveiligingsschild.
* Wanneer u een aangepast upload-publiek (CSV-bestand) als doel instelt, kunt u nu kenmerken uit het bestand gebruiken in uw campagnes en reizen. Deze attributen zijn beschikbaar in de verpersoonlijkingsredacteur, om uw berichten, en de reis geavanceerde uitdrukkingsredacteur te personaliseren.

## Opmerkingen bij de release juli 2024 {#24-7-2024}

**de datum van de Versie**: 30-31 juli, 2024

### Nieuwe functies {#27-4-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.

<table>
<thead>
<tr>
<th><strong>SMS-kanaal bij elke provider (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt extra leveranciers van SMS binnen Journey Optimizer, naast standaardleveranciers nu vormen Sinch, Infobip, en Twilio.</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>Raadpleeg de <a href="../sms/sms-configuration-custom.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Federated Audience Composition (Beperkte Beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Federated Audience Composition is nu beschikbaar in Adobe Journey Optimizer. Hierdoor kunnen ondernemingen gegevens samenstellen voor een beter gebruik in verschillende gebruiksgevallen. Met deze nieuwe benadering, als Adobe Real-time Customer Data Platform en/of gebruiker van Adobe Journey Optimizer, kunt u datasets van uw bestaand gegevenspakhuis direct federeren om het publiek en de attributen van Adobe Experience Platform te bouwen en te verrijken allen in één systeem.</p>
<p>Raadpleeg de <a href="https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home"  target="_blank">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#27-4-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Reizen**

* (De datum van de Beschikbaarheid: 8 juli) **Geavanceerde uitdrukkingsredacteur in de configuratie van de reisgebeurtenis** - u kunt hefboomwerking de geavanceerde uitdrukkingsredacteur nu terwijl het vormen van een gebeurtenis, die u toestaan om complexere uitdrukkingen of gebruiksfuncties in de voorwaarde van identiteitskaart van de Gebeurtenis te bepalen. [Meer informatie](../event/about-creating.md#adv-exp-editor)

