---
title: Aanvullende informatie
description: Journey Optimizer Release-aantekeningen
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: fedc0f70f336a9fa7917ad34a06e4d1845c1fdd4
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 10%

---

# Aanvullende informatie {#release-notes}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen voor [!DNL Journey Optimizer]. U kunt ook de [meest recente documentatie-updates](documentation-updates.md) pagina voor meer wijzigingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} vandaag en ontvang de nieuwste productupdates, spannende artikelen, gebruiksscenario&#39;s, tips en nog veel meer die elk kwartaal rechtstreeks aan uw Postvak IN worden bezorgd.

## Release van juni 2022 {#june-2022-release}

### Nieuwe functies

<table>
<thead>
<tr>
<th><strong>SMS verzenden naar uw gebruikers (beperkte beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu SMS in Journey Optimizer maken, personaliseren en verzenden via integratie met <b>Sinch</b> of <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Het SMS-kanaal is momenteel alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.</p>
<p>Leer hoe u in dit venster een SMS maakt en verzendt <a href="../messages/create-sms.md">gedetailleerde documentatie</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Snellere afbeeldingen zoeken dankzij Adobe Stock-integratie</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met de integratie-insteekmodule Adobe Stock en Adobe Journey Optimizer Email Designer kunnen klanten eenvoudig door afbeeldingen navigeren, licenties aanschaffen en afbeeldingen opslaan voor gebruik in berichtontwerpen. </br> De nieuwe <b>Vergelijkbare stockfoto's zoeken</b> kunt u ook Stock-foto's zoeken die overeenkomen met de inhoud, kleur en compositie van de afbeeldingen. </p>
<img src="assets/do-not-localize/stock-rn.gif"/>
<p>Raadpleeg de <a href="../design/stock.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>BCC via e-mail gebruiken op al uw e-mails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu de e-mailfunctie BCC (blinde koolstofkopie) gebruiken om e-mails op te slaan die door Adobe Journey Optimizer zijn verzonden. Schakel deze optie in uw e-mailvoorinstellingen in, zodat elke verzonden e-mail blind wordt gekopieerd naar uw BCC-adres.</p>
<img src="assets/do-not-localize/bcc-rn.gif"/>
<p>Raadpleeg de <a href="../configuration/bcc-email.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Objecten kopiëren tussen sandboxen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt de ervaringen nu opnieuw maken van een Journey Optimizer-sandbox naar een andere sandbox, bijvoorbeeld van een niet-productiesandbox naar een productiesandbox. Deze nieuwe mogelijkheid kopieert een volledige Reis, inclusief alle objecten waarvan de Reis afhankelijk is om correct te worden uitgevoerd, van de ene omgeving naar de andere. Naast de Reizen, kunt u andere componenten, zoals Aanbiedingen, Berichten, Schema's, Datasets, Gegevensbronnen, Gebeurtenissen, en Acties ook kopiëren.</p>
<p>Raadpleeg de <a href="../building-journeys/copy-to-sandbox.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content. In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Verbeteringen

**Beslissingsbeheer**

* **Ondersteuning voor HTML- en JSON-bestanden** - U kunt nu externe HTML- en JSON-bestanden van de Adobe Experience Cloud Asset-bibliotheek naar de inhoud van de aanbiedingsweergave slepen. [Meer informatie](../offers/offer-library/add-representations.md#html-json)


**E-mail**

* **Opslaan als sjabloon** - U kunt nu e-mailinhoud opslaan als een sjabloon en deze opnieuw gebruiken wanneer u andere berichten maakt. [Meer informatie](../design/email-templates.md)

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

-->

**Beheer**

<!--* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.-->

* **Voorvertoning van URL-parameters bijhouden** - Als u een berichtvoorinstelling configureert en URL-trackingparameters definieert, wordt nu een dynamische voorvertoning van de resulterende URL weergegeven. [Meer informatie](../configuration/email-settings.md#url-tracking)

* **Berichtvoorinstelling maken** - De verwerkingstijd voor het maken van een berichtvoorinstelling kan nu maximaal 3 uur in beslag nemen. [Meer informatie](../configuration/message-presets.md#create-message-preset)

* **IP-pooleditie** - Nu kan de verwerkingstijd voor IP pool update slechts tot 3 uren vergen. [Meer informatie](../configuration/ip-pools.md#edit-ip-pool)

<!--* **Personalize tracking URL parameters** - You can now use the Expression Editor to configure URL tracking parameters in your message presets. [Learn more](../configuration/email-settings.md#url-tracking)-->

<!--
**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.
-->
