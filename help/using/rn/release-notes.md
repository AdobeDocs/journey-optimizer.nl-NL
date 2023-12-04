---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Aanvullende informatie voor Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 299b34dec2e864fff5eb874b3fd491da80bc0c16
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 8%

---

# Aanvullende informatie {#release-notes}


>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nieuwe functies"
>abstract="**Adobe Journey Optimizer** biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen."

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen.

Opmerkingen bij vorige release zijn beschikbaar in [deze pagina](release-notes-2023.md). U kunt ook de [meest recente documentatie-updates](documentation-updates.md) pagina voor meer wijzigingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} vandaag, en ontvang de recentste productupdates, opwindende verhalen, gebruiksgevallen, uiteinden en meer die direct aan uw Postbus worden geleverd elk kwartaal.

## Opmerkingen bij de release oktober 2023 {#oct-rn-2023}

### Nieuwe functies{#oct-2023-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.

<table>
<thead>
<tr>
<th><strong>Gereedschap Sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met gereedschappen voor sandboxen kunt u objecten kopiëren naar meerdere sandboxen door gebruik te maken van exporteren en importeren van pakketten. Een pakket kan uit één object of uit meerdere objecten bestaan. Alle objecten die in een pakket zijn opgenomen, moeten afkomstig zijn uit dezelfde sandbox.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<p>Raadpleeg de <a href="../building-journeys/copy-to-sandbox.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>MMS (Multimedia Message Service) in SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met het Kanaal van SMS, kunt u uw mededeling nu verbeteren door de MMS-berichten (Multimedia Message Service) te verzenden, toelatend het delen van beelden, GIFFEN, of video's met uw klanten. Deze functie is momenteel alleen beschikbaar voor Sinch.</p>
<img src="assets/do-not-localize/mms.gif"/>
<p>Raadpleeg de <a href="../sms/create-sms.md#mms-content">gedetailleerde documentatie</a> voor meer informatie.</p>
</tr>
</tbody>
</table>

### Verbeteringen {#oct-2023-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Doelgroepen**

* U kunt nu doelgroepen kiezen die vanuit een CSV-bestand naar reizen en campagnes zijn geüpload. [Meer informatie](../audience/about-audiences.md#segments-in-journey-optimizer)
* U kunt nu doelgroepen kiezen die zijn gemaakt door de publiekscompositie en de verrijkingskenmerken van de doelgroep in de stappen. [Meer informatie](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>Deze mogelijkheden zijn momenteel beschikbaar als een persoonlijke bètaversie.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Campagnes**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* Wanneer er een fout optreedt in een van uw campagnes, verschijnt er nu een waarschuwingspictogram in de lijst met campagnes naast de status van de campagne. [Meer informatie](../campaigns/modify-stop-campaign.md#statuses)

**Reizen**

* De maximale tijdsduur die u in een wachttijd kunt definiëren, is nu 29 dagen in plaats van 30. Deze verbetering is ingevoerd om te voorkomen dat wachttijden langer duren dan de 30 dagen durende reisduur. Dit geldt voor:

   * de **Tijd** in het veld [wachtactiviteiten](../building-journeys/wait-activity.md)
   * de **Wachttijd bij terugkeer** in [reiseigenschappen](../building-journeys/journey-gs.md#entrance)
   * de **Wacht op** veld in de time-outdefinitie van [gebeurtenisactiviteiten](../building-journeys/general-events.md#events-specific-time).

<!--
**Consent in channel configuration**

* You can now select a marketing action at the channel surface level. When used in a surface, all consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers.-->

**Beslissingsbeheer**

* Verschillende etiketten met betrekking tot het aanbieden van plafonnering in de besluitvormingsinterface zijn bijgewerkt. [Meer informatie](../offers/offer-library/add-constraints.md#capping)

