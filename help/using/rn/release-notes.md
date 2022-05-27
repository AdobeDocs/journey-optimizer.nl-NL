---
title: Aanvullende informatie
description: Journey Optimizer Release-aantekeningen
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 53a625c0e62fbfae703b40bb1d47105c168730ea
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 11%

---

# Aanvullende informatie {#release-notes}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen voor [!DNL Journey Optimizer]. U kunt ook de [meest recente documentatie-updates](documentation-updates.md) pagina voor meer wijzigingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} vandaag en ontvang de nieuwste productupdates, spannende artikelen, gebruiksscenario&#39;s, tips en nog veel meer die elk kwartaal rechtstreeks aan uw Postvak IN worden bezorgd.

## Release van mei 2022 {#may-2022-release}

### Nieuwe functies

<!--table>
<thead>
<tr>
<th><strong>Message Frequency Rules</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now set cross-channel business rules that will automatically exclude over-solicited profiles from messages and actions.</p>
<img src="assets/frequency-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/frequency-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>BCC e-mailen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Beschikbaarheidsdatum: <strong>31 mei</strong></p>
<p>U kunt nu de e-mailfunctie BCC (blinde koolstofkopie) gebruiken om e-mails op te slaan die door Adobe Journey Optimizer zijn verzonden. Schakel deze optie in uw e-mailvoorinstellingen in, zodat elke verzonden e-mail blind wordt gekopieerd naar uw BCC-adres.</p>
<img src="assets/bcc-rn.gif"/>
<p>Raadpleeg de <a href="../configuration/email-settings.md#bcc-email">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Decision Management - AI Ranking auto-optimization model</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use trained model systems in Decision Management. This new capability ranks offers to display for a given profile.</p>
<img src="assets/optimization.gif"/>
<p>For more information, refer to the <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer Audit Logs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu de acties controleren die gebruikers op Adobe Journey Optimizer-bronnen uitvoeren.</p>
<img src="assets/audit-rn.gif"/>
<p>Raadpleeg de <a href="../reports/audit-logs.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen

**Personalisatie**

* **Nieuwe hulpfunctie voor verborgen tekens** - de `mask` Met de hulpfunctie kunt u een deel van een tekenreeks vervangen door &quot;X&quot;-tekens. [Meer informatie](../personalization/functions/string.md#mask)

**Landingspagina’s**

* **Pagina&#39;s zonder formulier landen** - U kunt nu een bestemmingspagina maken en publiceren die geen formulier bevat en geen actie van bezoekers vereist.
* **Sjablonen voor bestemmingspagina** - U kunt een landingspagina nu opslaan als een sjabloon en deze opnieuw gebruiken bij het maken van andere bestemmingspagina&#39;s. [Meer informatie](../landing-pages/lp-templates.md)
* **Terug naar de primaire pagina** - U kunt nu een koppeling naar de primaire pagina toevoegen vanuit elke subpagina binnen dezelfde bestemmingspagina.
* **Aangepaste JavaScript-ondersteuning** - U kunt nu aangepaste JavaScript toevoegen aan uw bestemmingspagina-inhoud om geavanceerde stijlen uit te voeren of aangepaste gedragingen toe te voegen aan uw bestemmingspagina&#39;s.	[Meer informatie](../landing-pages/lp-custom-js.md)

<!--**Decision management**

* **HTML and JSON files support** - You can now drag and drop external HTML and JSON files from the AEM repository into the offer representation content.-->

**Journeys**

* **Segment lezen** - Eenmalig Leessegment-reizen gaan nu 30 dagen na de uitvoering van de reis over naar de voltooide status. Voor geplande Gelezen segmenten, is het 30 dagen na de uitvoering van het laatste voorkomen. [Meer informatie](../building-journeys/read-segment.md)
* **Expression-editor** - de [limiet](../building-journeys/functions/functionlimit.md) Er is een functie toegevoegd waarmee u het aantal items in een lijst kunt beperken. De [sorteren](../building-journeys/functions/functionsort.md) Met deze functie kunt u nu een lijstobject sorteren. De ondersteuning van listObject is ook toegevoegd aan de [ontkenning](../building-journeys/functions/functiondistinct.md) en [differentWithNull](../building-journeys/functions/functiondistinctwithnull.md) functies.
