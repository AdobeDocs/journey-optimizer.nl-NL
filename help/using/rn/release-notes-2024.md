---
solution: Journey Optimizer
product: journey optimizer
title: Release-aantekeningen 2024
description: Opmerkingen bij de release van Journey Optimizer 2024
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: bae533c5-1bfc-48bf-9f8d-1145383c040c
source-git-commit: 12c3c1e2d6dabdc5c9b741742fd36c35c8b0992c
workflow-type: tm+mt
source-wordcount: '3846'
ht-degree: 6%

---

# Aanvullende informatie 2024 {#release-notes-2024}

Deze pagina bevat een overzicht van alle functies en verbeteringen die [!DNL Journey Optimizer] in 2024 heeft uitgebracht.


## Opmerkingen bij de release augustus 2024 {#8-2024}

**de datum van de Versie**: Augustus 20-21, 2024

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

**het kanaal van de duw**

* U kunt nu uw pushgegevens voor mobiele toepassingen toevoegen in de configuratie-instellingen voor Adobe Journey Optimizer-kanalen. Het maken van een App-oppervlak in Adobe Experience Platform Data Collection is niet langer vereist.

### Andere wijzigingen {#changes}

**Meldend**

* Nieuwe gebruiksgevallen zijn toegevoegd aan de nieuwe ervaring met rapportage:

   * U kunt aangepaste berekende metriek rechtstreeks in uw rapporten maken.
   * Creeer een Publiek van het melden van gegevens.
   * Met het gereedschap Verkennende analyse kunt u eenvoudig tabellen en visualisaties maken op basis van de geselecteerde **[!UICONTROL Dimensions]** en **[!UICONTROL Metrics]** .

  Raadpleeg de [gedetailleerde documentatie](../reports/report-cja-manage.md) voor meer informatie.



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



## Opmerkingen bij de release van juni 2024 {#24-6-2024}

**de datum van de Versie**: 18-19 juni, 2024

### Nieuwe functies {#june-24-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden beschreven.

<table>
<thead>
<tr>
<th><strong>Aanpassing van inhoudsfragmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu specifieke velden in een fragment definiëren die kunnen worden bewerkt wanneer het fragment wordt toegevoegd aan een campagne of reis. Op deze manier kunt u inhoudsdelen aanpassen op het moment dat u ze gebruikt, zodat u de standaardwaarden kunt overschrijven met contextspecifieke details.</p>
<img src="../content-management/assets/do-not-localize/gif-fragments.gif"/>
<p>Raadpleeg de <a href="../content-management/customizable-fragments.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Rapportage met Customer Journey Analytics (beperkte beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer-rapportering wordt geleverd met een verbeterde interoperabiliteit met de mogelijkheden van de Customer Journey Analytics, standaardisering van de rapportage op beide platforms en verbetering van de consistentie en betrouwbaarheid van de gegevens. Deze naadloze integratie tussen Journey Optimizer en Customer Journey Analytics biedt een duidelijker beeld van prestatiesmetriek, toelatend gebruikers om geïnformeerde besluiten te nemen.</p>
<img src="assets/do-not-localize/ajo-cja.gif"/>
<p>Raadpleeg de <a href="../reports/report-gs-cja.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI Assistant in Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De AI Medewerker is een gebruikersinterfaceeigenschap die u kunt gebruiken om te navigeren en Adobe concepten te begrijpen en operationele inzichten voor uw specifieke milieu te krijgen. Het is verkrijgbaar in verschillende producten in Adobe Experience Cloud, waaronder Adobe Journey Optimizer.</p>
<p>Raadpleeg de <a href="../start/ai-assistant.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Meertalige berichten tijdens reizen en campagnes (beperkte beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu moeiteloos inhoud in meerdere talen maken in één campagne of reis. Met deze functie kunt u schakelen tussen talen wanneer u uw campagne of reis bewerkt, het hele bewerkingsproces stroomlijnt en uw mogelijkheden voor efficiënt beheer van meertalige inhoud verbetert.</p>
<p>Meertalige inhoud is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Experimentatie bij reizen (beperkte beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer is al beschikbaar in campagnes en ondersteunt nu experimenten op reizen. Experimenten zijn gerandomiseerde onderzoeken, die in de context van online tests betekenen dat u sommige willekeurig geselecteerde gebruikers aan een bepaalde variatie van een bericht blootstelt, en een andere willekeurig geselecteerde reeks gebruikers aan één of andere andere variatie of behandeling. Na blootstelling, kunt u de resultaatmetriek meten u in geinteresseerd bent, zoals opent van e-mail, abonnementen, of aankopen.</p>
<p>Experimentatie op het gebied van reizen is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Verbeteringen {#june24-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

#### Beslissingsbeheer

* **steun van de multi-regel in Beslissingsbeheer** - u kunt tot 10 het begrenzen regels voor een bepaalde aanbieding in Beslissingsbeheer nu toevoegen. Dit staat u toe om het niveau van controle over de manier te verhogen de aanbiedingen worden verzonden. [Meer informatie](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

#### Inhoudsfragmenten

>[!AVAILABILITY]
>
>Deze verbeteringen zullen geleidelijk worden doorgevoerd in de loop van enkele dagen na de eerste release. Terwijl sommige gebruikers directe toegang zullen hebben, kunnen anderen een vertraging ervaren alvorens het in hun milieu&#39;s beschikbaar wordt.

* Fragmenten kunnen nu worden bewerkt en wijzigingen kunnen worden doorgevoerd in alle live reizen en campagnes waar ze worden gebruikt.
* De nieuwe statussen voor inhoudsfragmenten zijn geïntroduceerd: **Ontwerp**, **Levend**, **het Publiceren**, en **Gearchiveerd**.
* Om een fragment in een reis of een campagne te gebruiken, moet het nu in **Levende** status zijn. Er is een nieuwe stap toegevoegd aan het proces voor het maken van fragmenten, zodat het fragment kan worden gepubliceerd en beschikbaar kan worden gesteld voor gebruik tijdens reizen en campagnes. Voor het publiceren van fragmenten is een nieuwe machtiging vereist.

  **VOORZIENING** - aangezien **het Ontwerp** en **Levende** statussen met de versie van Journey Optimizer Juni zijn geïntroduceerd, hebben alle fragmenten die vóór deze versie worden gecreeerd de **7} status van het Ontwerp {, zelfs als zij in een reis of een campagne worden gebruikt.** Als u om het even welke verandering in deze fragmenten aanbrengt, moet u hen ](../content-management/create-fragments.md#publish) publiceren om hen &quot;Levend&quot;te maken en de veranderingen in de bijbehorende campagnes en de reizen te verspreiden. [ U moet ook een nieuwe reis/campagneversie tot stand brengen en het publiceren.

Lees meer in de [ documentatie van het inhoudsfragment ](../content-management/fragments.md).

#### Journeys

* De wereldwijde time-out van reizen is verlengd tot 91 dagen. [Meer informatie](../building-journeys/journey-properties.md#global_timeout)

  Bij nieuwe reizen wordt deze nieuwe time-out weerspiegeld. Gelieve te verwijzen naar deze [ sectie van Veelgestelde vragen ](../building-journeys/journey-properties.md#timeout-faq) om meer te leren. Deze wijzigingen zullen in de loop van de maand juni geleidelijk worden doorgevoerd.


* Adobe Journey Optimizer ondersteunt nu verzoeken om privacyverwijdering/toegang en verzoeken om gegevenslevenscyclusbeheer. [Meer informatie](../privacy/requests.md)
* U kunt nu de grootte van de kolommen in de reisinventaris wijzigen.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* **beleid van de Fusie** is nu GA - het beleid van de Fusie dat door een Reizen wordt gebruikt is nu zichtbaar en verenigbaar door de reis. [Meer informatie](../building-journeys/journey-properties.md#merge-policies)



#### Campagnes

* Wanneer u een campagne maakt in Adobe Journey Optimizer, kunt u nu het type campagne (gepland of geactiveerd) kiezen in een nieuw modaal. [Meer informatie](../campaigns/create-campaign.md)

#### Email channel

* **lijst-unsubscribe** - na de recente Gmail en aankondigingen Yahoo voor bulkafzenders, steunt Journey Optimizer de &quot;post/1-klik&quot;lijst-Unsubscribe optie. Verwijs naar de volgende pagina&#39;s: [ e-mail opt-out beheer ](../email/email-opt-out.md#unsubscribe-header) en [ vorm e-mailmontages ](../email/email-settings.md#list-unsubscribe).

  **NOTA** - voor om het even welke nieuwe kanaaloppervlakte, door gebrek wordt de lijst unsubscribe kopbaloptie geactiveerd. Voor bestaande oppervlakken is de optie Een-klik-abonnement voor URL opheffen in de instellingen van het kanaaloppervlak standaard uitgeschakeld. Als u een URL voor uitschakelen met één klik eerder in de e-mail gebruikte, blijft deze instelling geldig. Als de één-klik unsubscribe URL in de montages van de kanaaloppervlakte wordt gecontroleerd, zal Adobe Journey Optimizer eerder het gebrek geproduceerde Één-klik gebruiken unsubscribe URL in de montages van de kanaaloppervlakte.

#### SMS-kanaal

* U kunt nu unieke korte codes toevoegen voor elke sandbox met één API-configuratie, waardoor het proces efficiënter en gestroomlijnder wordt. [Meer informatie](../sms/sms-configuration.md)

* Na verwezenlijking, wordt het **Symbolische** gebied van API op de **API credentiedetails** pagina nu gemaskeerd.

<!--* You can now modify existing SMS configurations.-->

#### Kanaal in app

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* U kunt nu de Edge Delivery-insteekmodule gebruiken om informatie op te halen die nodig is voor het begrijpen van en het oplossen van problemen met uw binnenkomende implementaties. [ leer meer op de mening van Edge Delivery ](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery) {target="_blank"}.


#### Direct mailkanaal

* Direct mail kanaal is nu beschikbaar voor alle klanten. [Meer informatie](../direct-mail/get-started-direct-mail.md)



## Opmerkingen bij de release mei 2024 {#may-2024}

**de datum van de Versie**: Mei 21-22, 2024

### Nieuwe functies {#e-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden beschreven.

<table>
<thead>
<tr>
<th><strong>Ervaring beslissen - Beperkte beschikbaarheid</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ervaring Beslissen vereenvoudigt personalisatie door een gecentraliseerde catalogus van marketingaanbiedingen aan te bieden, die bekend staan als 'beslissingspunten' en een geavanceerde beslissingsengine. Deze motor hanteert regels en rangschikkingscriteria om de meest relevante beslissingsitems te selecteren en aan elk individu voor te leggen.</p>
<p>Deze besluitvormingspunten zijn naadloos geïntegreerd in een brede waaier van binnenkomende configuraties door het nieuwe op code-gebaseerde ervaringskanaal, nu toegankelijk binnen de campagnes van Journey Optimizer. Het beleid van de Beslissing van de ervaring is beschikbaar voor gebruik in code-gebaseerde ervaringscampagnes slechts.</p>
<p>Experience Decisioning is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Raadpleeg de <a href="../experience-decisioning/gs-experience-decisioning.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aanpassing e-mailconfiguratie - Beperkte beschikbaarheid</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt dynamische subdomeinen en gepersonaliseerde kopbalparameters nu bepalen wanneer het creëren van configuraties van het e-mailkanaal, voor verhoogde flexibiliteit en controle over uw e-mailmontages.</p>
<p>Aanpassing van de e-mailconfiguratie is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.</p>
<p>Raadpleeg de <a href="../email/surface-personalization.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Verbeteringen {#e-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Ervaring Beslissing** (Beperkte Beschikbaarheid)

Van bèta tot deze release zijn de volgende verbeteringen toegevoegd:

* **Beslissing van de Ervaring + Op code-gebaseerde ervaringen** - u kunt hefboomwerking de het besluiten van de Ervaring eigenschap nu om besluitvormingspunten in uw op code-gebaseerde campagnes te gebruiken. Opmerking: het op code gebaseerde ervaringskanaal en de ervaringsbeslissingen zijn niet beschikbaar voor organisaties die de add-on Adobe van het gezondheidsschild en privacy- en beveiligingsschild hebben aangeschaft. [Meer informatie](../code-based/get-started-code-based.md)
* **de gegevens van de Context** - u kunt hefboomwerkingscontextgegevens van Adobe Experience Platform in uw besluitvormingsregels en rangschikkingsformules nu. [Meer informatie](../experience-decisioning/context-data.md)
* **Nieuwe toestemming** - een nieuwe &quot;beheert de besluiten van de Ervaring&quot;toestemming is nu beschikbaar voor het middel van het Beheer van het Besluit. Hiermee kunt u rechten beheren die betrekking hebben op het bepalen van ervaring. [Meer informatie](../experience-decisioning/gs-experience-decisioning.md)
* **Afschilderende regels** - u kunt veelvoudige het afschilderen regels voor een bepaald besluitpunt in Ervaring nu toevoegen Beslissing. Dit staat u toe om het niveau van controle over de manier te verhogen de aanbiedingen worden verzonden. [Meer informatie](../experience-decisioning/items.md#capping)
* **Meldend** - u kunt douane nu creëren rapporterend dashboards van de campagnes van het Beslissen van de Ervaring gebruikend [!DNL Customer Journey Analytics]. [Meer informatie](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**E-mailkanaal**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Spam het scoren** (Beta) - u kunt uw inhoud nu controleren spam het scoren in een specifiek Spam- rapport. Gebruikend SpamAssassin, kan Adobe Journey Optimizer uw e-mailinhoud nu testen en het een score geven om erop te wijzen als ISPs of de leveranciers van de Brievenbus het als spam of niet zullen beschouwen. [Meer informatie](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >Deze mogelijkheid is momenteel beschikbaar in bètaversie en alleen voor bètaklanten. Neem contact op met uw Adobe als u wilt deelnemen aan het bètaprogramma.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**Reizen**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **mTLS steun** - de authentificatie mTLS wordt nu gesteund in douaneacties. Er is geen extra configuratie vereist in de douaneactie of de reis om mTLS te activeren; het komt automatisch voor wanneer een mTLS-Toegelaten eindpunt wordt ontdekt. [Meer informatie](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **de lijsten van de Raadpleging in gebeurtenissen** - u kunt hefboomwerkingsgegevens van een raadplegingsdataset nu gebruiken wanneer een verhouding gebruikend een attribuut binnen van een serie van voorwerpen is bepaald. De opzoekwaarden zijn beschikbaar voor reizen (voorwaarden, aangepaste handelingen, enz.) en berichtpersonalisatie. [Meer informatie](../event/experience-event-schema.md#relationships_limitations)
* **Geavanceerde uitdrukkingsredacteur in de configuratie van de Gebeurtenis** (LA) - u kunt hefboomwerking de geavanceerde uitdrukkingsredacteur nu terwijl het vormen van een gebeurtenis, toestaand u om complexere uitdrukkingen of gebruiksfuncties in de voorwaarde van gebeurtenisidentiteitskaart te bepalen. Deze mogelijkheid wordt vrijgegeven in Beperkte Beschikbaarheid voor geselecteerde klanten. [Meer informatie](../event/about-creating.md#adv-exp-editor)
* **beleid van de Fusie** (LA) - het beleid van de Fusie dat door een Reis wordt gebruikt is nu zichtbaar en verenigbaar door de reis. Deze mogelijkheid wordt vrijgegeven in Beperkte Beschikbaarheid voor geselecteerde klanten. [Meer informatie](../building-journeys/journey-properties.md#merge-policies)

**Globalization**

Als onderdeel van onze voortdurende inspanningen om een uniforme gebruikerservaring te bieden, harmoniseren we de terminologie die wordt gebruikt in de Adobe Experience Cloud-producten en -toepassingen. Dit is van invloed op de Duitse term &quot;Titel&quot;, die wordt gewijzigd in &quot;Label&quot; wanneer deze betrekking heeft op de naam van een object. De wijzigingen worden geleidelijk doorgevoerd in de gebruikersinterface en de documentatie.




## Opmerkingen bij de release van april 2024 {#apr-2024}

**de datum van de Versie**: 2 mei, 2024

### Nieuwe functies {#apr-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden beschreven.

<table>
<thead>
<tr>
<th><strong>Multimedia Message Service (MMS) - alle providers</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met het Kanaal van SMS, kunt u uw mededeling nu verbeteren door de MMS-berichten (Multimedia Message Service) te verzenden, toelatend het delen van beelden, GIFFEN, of video's met uw klanten. In eerste instantie alleen beschikbaar bij Sinch, is MMS nu ook beschikbaar bij Infobip en Twilio.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verbeterde Journey Designer en live rapportering</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Deze release wordt geleverd met een verbeterde gebruikersinterface voor het canvas voor reizen en biedt een intuïtievere en efficiëntere gebruikerservaring. De activiteiten zijn duidelijker en geven meer informatie over het reiscanvas met minder kliks.</p>
<img src="assets/new-canvas3.gif"/>
<p>Naast het verbeterde ontwerp van het reiscanvas introduceren we de mogelijkheid om de laatste 24 uur metriek direct in het reiscanvas te zien. </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong> Nota </strong>: Deze veranderingen zullen geleidelijk aan alle milieu's worden opgerold die de versie van April beginnen.</p>
<p>Raadpleeg de <a href="new-canvas.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel configurations, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Verbeteringen {#apr-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO channel configuration**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel configuration through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Configuratie**

* U kunt nu een marketingactie op het niveau van de kanaalconfiguratie selecteren. Wanneer gebruikt in een configuratie, wordt al toestemmingsbeleid verbonden aan die marketing actie leveraged om de voorkeur van uw klanten te respecteren. [Meer informatie](../action/consent.md#surface-marketing-actions)
* Het gebruik van het Toegangsbeheer op objectniveau is nu beschikbaar voor kanaalconfiguraties. [Meer informatie](../configuration/channel-surfaces.md#create-channel-surface)
* Terwijl het toelaten van lijst unsubscribe in een kanaalconfiguratie, kunt u het toestemmingsniveau nu bepalen om zich aan te sluiten bij hoe u toestemming van alle andere bronnen beheert. [Meer informatie](../email/email-settings.md#list-unsubscribe)

**Inhoudsbeheer**

* U kunt nu inhoudssjablonen voor alle kanalen simuleren. [Meer informatie](../content-management/content-templates.md#test-templates)

**Personalization**

* De nieuwe **toInt** hulpfunctie is beschikbaar in de Redacteur van de Uitdrukking. U kunt elk van deze typen (getal, dubbel, int, lang, zwevend, kort, byte, boolean, tekenreeks) omzetten in een geheel getal. [Meer informatie](../personalization/functions/math.md#to-int)



## Opmerkingen bij de release maart 2024 {#mar-2024}

**de datum van de Versie**: Maart 19-20, 2024

### Nieuwe functie {#mar-features}

Met deze release wordt de nieuwe functionaliteit hieronder beschreven.

<table>
<thead>
<tr>
<th><strong>Ervaringen op basis van code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met het nieuwe op code-gebaseerde ervaringskanaal, staat Adobe Journey Optimizer u toe om geavanceerde verpersoonlijking en het testen voor om het even welk van uw binnenkomende eigenschappen te doen, toelatend naadloze levering van op maat gemaakte ervaringen over diverse aanraakpunten zoals Web apps, mobiele apps, Desktop apps, videoconsoles, TV aangesloten apparaten, slimme TVs, kiosken, ATMs, IoT apparaten, en meer.</p>
<P>De belangrijkste mogelijkheden omvatten:</p>
<ul><li> Universele verpersoonlijking: vergroot persoonlijke ervaringen op alle aanraakpunten, zodat een samenhangende en op maat gesneden gebruikersreis mogelijk is</li>
<li>Precisie voor bewerking in korrels: bewerk specifieke inhoud op afzonderlijke locaties in uw apps of webpagina's</li>
<li>Veelzijdige implementatie: ondersteuning voor implementatiemethoden die zijn gebaseerd op servers, API's of SDK's, zodat deze naadloos kunnen worden geïntegreerd met uw ontwikkelomgeving.</li></ul></p>
<p>Raadpleeg de <a href="../code-based/get-started-code-based.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<img src="assets/do-not-localize/code-based.gif"> 
</tr>
</tbody>
</table>

### Verbeteringen {#mar-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Contentsjablonen**

* **Duimnagels** - de 3} wijze van de mening van A **Net is nu beschikbaar voor inhoudsmalplaatjes, tonend duimnagels voor betere visuele toegang.** Momenteel worden alleen e-mailsjablonen ondersteund. [Meer informatie](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Dit vermogen wordt vrijgegeven in Beperkte Beschikbaarheid (LA) voor een kleine reeks klanten.

**Reizen**

Er zijn nieuwe tussenliggende statussen toegevoegd aan de levenscyclus van de reisontwerpfase:

* **het Publiceren** status tussen de **3} status van het Ontwerp {en** Levende **status**
* **het Stoppen** status tussen **Levende** status en **beëindigde** status
* **het activeren van testwijze** of **het Deactiveren van testwijze** statussen tussen de **Ontwerp** status en de **(test)** status

Wanneer een reis in een tussenstadium is, is het read-only. [Meer informatie](../building-journeys/journey-gs.md#filter)

## Opmerkingen bij de release februari 2024 {#feb-2024}

**de datum van de Versie**: 21-22 feb, 2024

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

* **zaadlijsten** - de Varianten worden nu gesteund wanneer het gebruiken van **zaadlijsten**. De zaadadressen ontvangen een exemplaar van alle varianten van het zelfde bericht (zoals de verschillende behandelingen van een inhoudexperiment). [Meer informatie](../configuration/seed-lists.md)

Eerder beschikbaar als Beta, zijn de volgende verbeteringen nu beschikbaar voor alle gebruikers:

* U kunt **publiek nu richten dat door publiekssamenstelling** en hefboomverrijkingsattributen in Reizen wordt gecreeerd. [Meer informatie](../building-journeys/read-audience.md)

* U kunt **publiek nu richten dat van een Csv- dossier** in reizen en campagnes wordt geupload. [Meer informatie](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* Het gebruik van soorten publiek en kenmerken van de compositie van het publiek en aangepaste upload (CSV-bestand) is momenteel niet beschikbaar voor gebruik met het gezondheidsschild of het privacyschild.
  >* Het **publiek uploadt van een Csv- dossier** verbetering wordt uit geleidelijk opgerold over de loop van verscheidene dagen na de aanvankelijke versie. Terwijl sommige gebruikers directe toegang hebben, kunnen anderen een vertraging ervaren alvorens het in hun milieu beschikbaar wordt.

**Reizen**

* **filter uw reizen** - u kunt **douanedata nu gebruiken om de reis** inventaris, naast de bestaande vooraf bepaalde datumfilters te filtreren. Op deze manier kunt u de lijst verfijnen door ritten weer te geven die op een bepaalde datum zijn gemaakt of gepubliceerd, binnen een bepaalde maand, gedurende een heel jaar of binnen een opgegeven tijdbereik. [Meer informatie](../building-journeys/journey-gs.md#filter)
* **de acties van de Douane** - u kunt **inhoud-type** kopbal nu bijwerken. Dit nieuwe **inhoud-type** zou inhoud JSON moeten van verwijzingen voorzien. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)
* **Configuratie** - het attribuut identityMap in stepEvents is nu voorgevuld. De primaire identiteit wordt gedefinieerd als &quot;primary = true&quot;. [Meer informatie](../reports/sharing-field-list.md)
* **Gebruikersinterface** - de hoogste bar, in de transmissieschermen, is gereorganiseerd voor een betere ervaring. Onder de verschillende updates ziet u dat het potlood-pictogram waarmee u de reiseigenschappen kunt openen nu links van de bovenste balk naast de naam van de rit wordt weergegeven. [Meer informatie](../building-journeys/journey-properties.md)

**Sms-kanaal**

* **Opt-binnen/opt-out sleutelwoorden** - wanneer het vormen van uw kanaal van SMS, kunt u **Opt-binnen en Opt-out sleutelwoorden** zoals op uw voorkeur nu aanpassen. Journey Optimizer activeert de reactie op basis van deze opgegeven trefwoorden. [Meer informatie](../sms/sms-configuration.md)

**Campagnes**

* **API-teweeggebrachte campagnes** - de cURL code na het activeren van een API-teweeggebrachte campagne is verbeterd. Het omvat nu alle personaliseringsvariabelen (profiel en context) die in het bericht worden gebruikt. [Meer informatie](../campaigns/api-triggered-campaigns.md#execute)

**Regels van de Frequentie**

* Naast E-mail en Duw, kunt u de regels van de Frequentie voor SMS en Directe kanalen van de Post nu tot stand brengen. De frequentieregels sluiten over-gevraagde profielen automatisch uit van berichten en acties wanneer de frequentiedrempel wordt bereikt. [Meer informatie](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## Opmerkingen bij de release januari 2024 {#jan-2024}

**de datum van de Versie**: Jan 30-31, 2024

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
<th><strong>Playbooks voor gebruiksscenario's</strong><br/></th>
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

**Meldend**

* **Nieuwe op domein gebaseerde indeling widgets** - Nieuwe widgets zijn toegevoegd om uw rapporten van de Campagne en van de Reis te verbeteren. De **Bounce Redenen door domein**, **Verzonden en geleverd door domeinen**, **opent &amp; klikt door domein** en **Stuiteren &amp; fouten door domein** widgets verstrekken een gedetailleerde uitsplitsing op het domeinniveau voor zeer belangrijke e-maillevering en het volgen metriek. [Meer informatie](../reports/channel-report.md)

**Kanaal van SMS**

* **dubbel Opt-binnen** - het dubbel kiezen-binnen werkschema voor SMS garandeert dat de gebruikers uitdrukkelijk opt-in om berichten te ontvangen wanneer het verzoek van hun apparaat in werking wordt gesteld. Gebruikers starten het goedkeuringsproces door een binnenkomend SMS-bericht te verzenden. Na bevestiging van hun toestemming wordt een vervolgbericht verzonden waarin om een definitieve verificatie wordt verzocht. Als een gebruikersprofiel niet bestaat, wordt het gecreeerd na succesvolle bevestiging. [Meer informatie](../sms/sms-configuration.md)

  Merk op dat dit vermogen met de leveranciers van SMS van Sinch en Infobip beschikbaar is.

**Reizen**

* **de gebeurtenisduur van de Reactie** - de maximumduur die u in de **gebeurtenissen van de Reactie** kunt bepalen is nu 29 dagen in plaats van 30. [Meer informatie](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **leest publiek** - de **Gelezen activiteit van het publiek** baseert zich nu op de dataset van de profielmomentopname voor partijsegmenten, die slechts eenmaal per dag wordt geproduceerd nadat de geplande dagelijkse partijbaan in werking wordt gesteld, vandaar de gegevens tot die laatste dagelijkse partijbaan vers zullen zijn. [Meer informatie](../building-journeys/read-audience.md)

* **Groepen van het Gebied** - Deze versie lost een kwestie op die de Groepen van het Gebied in bepaalde gevallen blokkeerde worden bewaard.

* Ondersteuning van `<listObject>` is gewijzigd in meerdere functies.

**Regels van de Frequentie**

* **Wekelijks frequentiemaximum** - u kunt nu het maximumaantal berichten specificeren die naar een klantenprofiel per week, naast maand worden verzonden. De maximale frequentie is gebaseerd op de geselecteerde kalenderperiode en wordt opnieuw ingesteld aan het begin van het corresponderende tijdkader. [Meer informatie](../configuration/frequency-rules.md#create-new-rule)

  >[!NOTE]
  >
  >Dagelijkse frequentiegrens is ook beschikbaar op verzoek. Neem contact op met uw Adobe.

**het beheer van het Besluit**

* **het Afbakenen van de Frequentie op Edge** - de frequentie die teller aftappen wordt nu bijgewerkt en beschikbaar in een besluit van Edge die API in minder dan 3 seconden beslist. [Meer informatie](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
