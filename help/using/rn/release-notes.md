---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
description: Journey Optimizer Release-aantekeningen
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 40e4aaa93400daf52c96aa5ac2de17151cdbb07f
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 5%

---

# Aanvullende informatie {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Wat is nieuw?"
>abstract="**Adobe Journey Optimizer** biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} vandaag, en ontvang de recentste productupdates, opwindende verhalen, gebruiksgevallen, uiteinden en meer die direct aan uw Postbus worden geleverd elk kwartaal.


## Opmerkingen bij de release mei 2024 {#may-2024}

**Releasedatum**: 21 mei 2024

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
<p>Deze beslissingsitems worden naadloos geïntegreerd in een breed scala aan binnenkomende oppervlakken via het nieuwe op code gebaseerde ervaringskanaal, dat nu toegankelijk is in Journey Optimizer-campagnes. Het beleid van de Beslissing van de ervaring is beschikbaar voor gebruik in code-gebaseerde ervaringscampagnes slechts.</p>
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
<th><strong>Aanpassing van e-mailoppervlak - Beperkte beschikbaarheid</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt dynamische subdomeinen en gepersonaliseerde kopbalparameters nu bepalen wanneer het creëren van e-mailkanaaloppervlakten, voor verhoogde flexibiliteit en controle over uw e-mailmontages.</p>
<p>De aanpassing van het oppervlak van e-mail is momenteel slechts beschikbaar voor een reeks organisaties (Beperkte Beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.</p>
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

**Ervaar beslissingsvermogen** (Beperkte beschikbaarheid)

Van bèta tot deze release zijn de volgende verbeteringen toegevoegd:

* **Ervaring kiezen + op code gebaseerde ervaringen** - U kunt nu de functie Ervaring beslissen gebruiken om beslissingen te nemen in uw op code gebaseerde campagnes. Opmerking: het op code gebaseerde ervaringskanaal en de ervaringsbeslissingen zijn niet beschikbaar voor organisaties die de add-on Adobe van het gezondheidsschild en privacy- en beveiligingsschild hebben aangeschaft. [Meer informatie](../code-based/get-started-code-based.md)
* **Contextgegevens** - Je kunt nu contextgegevens van Adobe Experience Platform gebruiken in je besluitvormingsregels en rangschikkingsformules. [Meer informatie](../experience-decisioning/context-data.md)
* **Nieuwe machtiging** - Er is nu een nieuwe machtiging &#39;Ervaring beheren&#39; beschikbaar voor de beslissingsbeheerbron. Hiermee kunt u rechten beheren die betrekking hebben op het bepalen van ervaring. [Meer informatie](../experience-decisioning/gs-experience-decisioning.md)
* **Afdekregels** - U kunt nu meerdere begrenzingsregels toevoegen voor een bepaald beslissingselement in het Ervaring-besluit. Dit staat u toe om het niveau van controle over de manier te verhogen de aanbiedingen worden verzonden. [Meer informatie](../experience-decisioning/items.md#capping)
* **Rapportage** - U kunt nu aangepaste rapporteringsdashboards maken van campagnes voor het nemen van beslissingen over ervaringen met [!DNL Customer Journey Analytics]. [Meer informatie](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**Email channel**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Spamscoring** (Beta) - U kunt nu de scoring van de inhoudspam controleren in een speciaal Spam-rapport. Gebruikend SpamAssassin, kan Adobe Journey Optimizer uw e-mailinhoud nu testen en het een score geven om erop te wijzen als ISPs of de leveranciers van de Brievenbus het als spam of niet zullen beschouwen. [Meer informatie](../content-management/spam-report.md)

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
* **mTLS-ondersteuning** - mTLS-verificatie wordt nu ondersteund in aangepaste handelingen. Er is geen extra configuratie vereist in de douaneactie of de reis om mTLS te activeren; het komt automatisch voor wanneer een mTLS-Toegelaten eindpunt wordt ontdekt. [Meer informatie](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **Tabellen opzoeken in gebeurtenissen** - U kunt nu hefboomwerkings gegevens van een raadplegingsdataset wanneer een verhouding gebruikend een attribuut binnen van een serie van voorwerpen is bepaald. De opzoekwaarden zijn beschikbaar voor reizen (voorwaarden, aangepaste handelingen, enz.) en berichtpersonalisatie. [Meer informatie](../event/experience-event-schema.md#relationships_limitations)
* **Geavanceerde expressie-editor in gebeurtenisconfiguratie** (LA) - U kunt nu de geavanceerde expressie-editor gebruiken tijdens het configureren van een gebeurtenis, zodat u complexere expressies kunt definiëren of functies kunt gebruiken in de voorwaarde voor de gebeurtenis-id. Deze mogelijkheid wordt vrijgegeven in Beperkte Beschikbaarheid voor geselecteerde klanten. [Meer informatie](../event/about-creating.md)
* **Beleid samenvoegen** (LA) - Het samenvoegingsbeleid dat door een reis wordt gebruikt, is nu zichtbaar en consistent gedurende de hele reis. Deze mogelijkheid wordt vrijgegeven in Beperkte Beschikbaarheid voor geselecteerde klanten. [Meer informatie](../building-journeys/journey-gs.md#merge-policies)

**Globalisatie**

Als onderdeel van onze voortdurende inspanningen om een uniforme gebruikerservaring te bieden, harmoniseren we de terminologie die wordt gebruikt in de Adobe Experience Cloud-producten en -toepassingen. Dit is van invloed op de Duitse term &quot;Titel&quot;, die wordt gewijzigd in &quot;Label&quot; wanneer deze betrekking heeft op de naam van een object. De wijzigingen worden geleidelijk doorgevoerd in de gebruikersinterface en de documentatie.



