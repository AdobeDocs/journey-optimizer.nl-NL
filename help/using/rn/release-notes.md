---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Journey Optimizer Release-aantekeningen
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 10%

---

# Aanvullende informatie {#release-notes}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen voor [!DNL Journey Optimizer]. U kunt ook de [meest recente documentatie-updates](documentation-updates.md) pagina voor meer wijzigingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} vandaag en ontvang de nieuwste productupdates, spannende artikelen, gebruiksscenario&#39;s, tips en nog veel meer die elk kwartaal rechtstreeks aan uw Postvak IN worden bezorgd.


## Release oktober 2022 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### Verbeteringen {#oct-2022-improvements}

**Journeys**

* De **Herkomst forceren bij herhaling** Deze optie is toegevoegd in terugkerende parameters van het read-segment. Met deze optie kunt u alle profielen die zich nog in de reis bevinden, automatisch laten afsluiten bij de volgende uitvoering. Wanneer de optie is gedeactiveerd, moeten profielen de reis beëindigen alvorens zij in een ander voorkomen kunnen opnieuw ingaan. [Meer informatie](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Beheer**

* Er is een bericht toegevoegd aan de gebruikersinterface om te waarschuwen dat subdomein, landende paginasubdomain, PTR-record en IP-poolconfiguraties algemeen gelden voor alle sandboxen en dat elke wijziging aan een van deze configuraties dus ook van invloed is op de productiesandboxen.
* De stappen voor het uploaden van de suppressielijst als een CSV-bestand vanuit de gebruikersinterface zijn gewijzigd. [Meer informatie](../configuration/manage-suppression-list.md#download-suppression-list)

**Campagnes**

* U kunt voltooide en gestopt campagnes nu archiveren. [Meer informatie](../campaigns/modify-stop-campaign.md#archive)
