---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Opmerkingen bij de vervroegde release van Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 91a687563ecd989c89061996b5906bcc77e82e23
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 3%

---

# Vroege aanvullende informatie {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd aan het einde van elke maand in de [releaseopmerkingen](release-notes.md).

Opmerkingen bij de eerste release hieronder kunnen zonder voorafgaande kennisgeving worden gewijzigd tot de beschikbaarheidsdatum van de release. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in [releaseopmerkingen](release-notes.md), op de datum van vrijgave.

## Opmerkingen bij de vervroegde release mei 2024 {#e-2024}

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
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als u e-mail op een gloednieuw IP adres verzendt, kunt u IP opwarmingswerkschema's nu gemakkelijk direct van het gebruikersinterface uitvoeren. Adobe Journey Optimizer biedt een gestandaardiseerde en efficiënte manier om uw IP adressen op te warmen die de beste praktijken voor optimale leverbaarheid volgen.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Bedrijfsregels - bèta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt korrelige frequentiecappende regels nu tot stand brengen, en hen toepassen op verschillende types van marketing mededelingen door regelreeksen. Met deze nieuwe functie kunt u bepalen hoe vaak uw publiek een bericht ontvangt door kanaalregels in te stellen die automatisch overgevraagde profielen uitsluiten van berichten en acties.</p>
<p>De mogelijkheden van de bedrijfsregels zijn momenteel beschikbaar als openbare bèta.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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

### Verbeteringen {#e-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Ervaar beslissingsvermogen** (Beperkte beschikbaarheid)

Van bèta tot deze release zijn de volgende verbeteringen toegevoegd:

* **Ervaring kiezen + op code gebaseerde ervaringen** - U kunt nu de functie Ervaring beslissen gebruiken om beslissingen te nemen in uw op code gebaseerde campagnes. Opmerking: het op code gebaseerde ervaringskanaal en de ervaringsbeslissingen zijn niet beschikbaar voor organisaties die de add-on Adobe van het gezondheidsschild en privacy- en beveiligingsschild hebben aangeschaft. [Meer informatie](../code-based/get-started-code-based.md)
* **Contextgegevens** - Je kunt nu contextgegevens van Adobe Experience Platform gebruiken in je besluitvormingsregels en rangschikkingsformules. [Meer informatie](../experience-decisioning/context-data.md)
* **Nieuwe machtiging** - Er is nu een nieuwe machtiging &#39;Ervaring beheren&#39; beschikbaar voor de beslissingsbeheerbron. Hiermee kunt u rechten beheren die betrekking hebben op het bepalen van ervaring. [Meer informatie](../experience-decisioning/gs-experience-decisioning.md)
* **Afdekregels** - U kunt nu meerdere begrenzingsregels toevoegen voor een bepaald beslissingselement in het Ervaring-besluit. Dit staat u toe om het niveau van controle over de manier te verhogen de aanbiedingen worden verzonden. [Meer informatie](../experience-decisioning/items.md#capping)
* **Rapportage** - U kunt nu aangepaste rapporteringsdashboards maken van campagnes voor het nemen van beslissingen over ervaringen met [!DNL Customer Journey Analytics]. [Meer informatie](../experience-decisioning/cja-reporting.md)


**Beslissingsbeheer**

* **Ondersteuning voor meerdere regels** - U kunt nu maximaal 10 afkapregels toevoegen voor een bepaald aanbod in Beslissingsbeheer. Dit staat u toe om het niveau van controle over de manier te verhogen de aanbiedingen worden verzonden.
* **Audits** - de **Logbestand wijzigen** , zodat u kunt zien welke wijzigingen in een voorstel of een beslissing zijn aangebracht. Wijzigingen met betrekking tot aanbiedingen en besluiten zijn nu te zien in de **Audits** -menu.


**E-mailkanaal**

* **List-unsubscribe** - Na de recente Gmail- en Yahoo-aankondigingen voor bulkafzenders biedt Journey Optimizer ondersteuning voor de optie &quot;Na/1-klik&quot; List-Unsubscribe.
* **Spamscoring** (Beta) - U kunt nu de scoring van de inhoudspam controleren in een speciaal Spam-rapport. Met SpamAssassin kan Adobe Journey Optimizer nu uw e-mailinhoud testen en deze een score geven om aan te geven of ISP-providers het als spam zullen beschouwen of niet.
  <!--[Read more](../content-management/spam-report.md)-->


**Doelgroepen**

* Het gebruik van soorten publiek en kenmerken van de compositie van het publiek en aangepaste upload (CSV-bestand) is nu beschikbaar voor gebruik met Healthcare Shield of Privacy and Security Shield.

**Personalisatie**

* **Expressiefragment** - Expressiefragmenten zijn nu beschikbaar voor de **Kanaal in app**.
  <!--[Read more](../personalization/use-expression-fragments.md)-->

**Reizen**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **mTLS-ondersteuning** - mTLS-verificatie wordt nu ondersteund in aangepaste handelingen. Er is geen extra configuratie vereist in de douaneactie of de reis om mTLS te activeren; het komt automatisch voor wanneer een mTLS-Toegelaten eindpunt wordt ontdekt.
* **Tabellen opzoeken in gebeurtenissen** - U kunt nu hefboomwerkings gegevens van een raadplegingsdataset wanneer een verhouding gebruikend een attribuut binnen van een serie van voorwerpen is bepaald. De opzoekwaarden zijn beschikbaar voor reizen (voorwaarden, aangepaste handelingen, enz.) en berichtpersonalisatie.
