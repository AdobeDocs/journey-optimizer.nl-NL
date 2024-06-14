---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Opmerkingen bij de vervroegde release van Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: d27689b2b89374859a045a09bbfc41bdf70f750e
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 5%

---

# Opmerkingen bij de eerste release {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd aan het einde van elke maand in de [releaseopmerkingen](release-notes.md).

**Opmerkingen bij de eerste release hieronder kunnen zonder voorafgaande kennisgeving worden gewijzigd tot de beschikbaarheidsdatum van de release**. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in [releaseopmerkingen](release-notes.md), op de datum van vrijgave.

## Opmerkingen bij de vervroegde release juni 2024 {#e-2024}

**Releasedatum**: 18-19 juni 2024

### Nieuwe functies {#e-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden beschreven.

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
<p>Raadpleeg de <a href="../configuration/ip-warmup-gs.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Content Fragments customization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define specific fields in a fragment that can be edited when the fragment is added to a campaign or journey. This allows for the adjustment of content portions at the time of use, providing flexibility to override default values with context-specific details.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->


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


<!--table>
<thead>
<tr>
<th><strong>Reporting with Customer Journey Analytics (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer reporting is now fully integrated with Customer Journey Analytics capabilities, standardizing reporting across both platforms and improving data consistency and reliability. This seamless integration between Journey Optimizer and Customer Journey Analytics provides a clearer view of performance metrics, enabling users to make more informed decisions.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns  (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Experimentation in journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Already available in campaigns, Adobe Journey Optimizer now supports experiments in journeys. Experiments are randomized trials, which in the context of online testing, means that you expose some randomly selected users to a given variation of a message, and another randomly selected set of users to some other variation or treatment. After exposure, you can then measure the outcome metrics you are interested in, such as opens of emails, subscriptions, or purchases.</p>
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


**Beslissingsbeheer**

* **Ondersteuning van meerdere regels in het besluitvormingsbeheer** - U kunt nu maximaal 10 afkapregels toevoegen voor een bepaald aanbod in Beslissingsbeheer. Dit staat u toe om het niveau van controle over de manier te verhogen de aanbiedingen worden verzonden. [Meer informatie](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

<!--**Content fragments**

* Fragments can now be edited, and changes can be propagated across all live journeys and campaigns where they are used.
* New statuses for content fragments have been introduced: **Draft**, **Live**, **Publishing**, and **Archived**. 
* To use a fragment in a journey or campaign, it must now be in the **Live** status. A new step has been added to the fragment creation process, allowing the fragment to be published and made available for use in journeys and campaigns. Note that fragment publishing requires a new permission.
   
   **CAUTION** - Since **Draft** and **Live** statuses have been introduced with Journey Optimizer June release, all fragments created before this release have the **Draft** status, even if they are used in a journey or campaign. Learn how to update your existing fragments in this section.-->

**Reizen**

* De wereldwijde time-out van de reis is verhoogd van 30 naar 91 dagen.
* Adobe Journey Optimizer ondersteunt nu verzoeken om privacyverwijdering/toegang en verzoeken om gegevenslevenscyclusbeheer.
* U kunt nu de grootte van de kolommen in de reisinventaris wijzigen.
* **Geavanceerde expressie-editor in gebeurtenisconfiguratie** is nu GA - U kunt nu de geavanceerde expressie-editor gebruiken tijdens het configureren van een gebeurtenis, zodat u complexere expressies kunt definiëren of functies kunt gebruiken in de toestand van de gebeurtenis-id. Deze mogelijkheid wordt vrijgegeven in Beperkte Beschikbaarheid voor geselecteerde klanten. [Meer informatie](../event/about-creating.md)
* **Beleid samenvoegen** zijn nu GA - Het samenvoegingsbeleid dat door een reis wordt gebruikt, is nu zichtbaar en consistent gedurende de hele reis. Deze mogelijkheid wordt vrijgegeven in Beperkte Beschikbaarheid voor geselecteerde klanten. [Meer informatie](../building-journeys/journey-gs.md#merge-policies)



**Campagnes**

* Wanneer u een campagne maakt in Adobe Journey Optimizer, kunt u nu het type campagne (gepland of geactiveerd) kiezen in een nieuw modaal.

**Email channel**

* **List-unsubscribe** - Na de recente Gmail- en Yahoo-aankondigingen voor bulkafzenders biedt Journey Optimizer ondersteuning voor de optie &quot;Na/1-klik&quot; List-Unsubscribe. <!--Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**SMS-kanaal**

* U kunt nu unieke korte codes toevoegen voor elke sandbox met één API-configuratie, waardoor het proces efficiënter en gestroomlijnder wordt.
  <!--* You can now modify existing SMS configurations.-->

**Kanaal in app**

* **Expressiefragment** - Expressiefragmenten zijn nu beschikbaar voor de **Kanaal in app**. [Meer informatie](../personalization/use-expression-fragments.md)


* U kunt nu de Edge Delivery-plug-in gebruiken om informatie op te halen die nodig is om uw binnenkomende implementaties te begrijpen en problemen op te lossen.


