---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Opmerkingen bij de vervroegde release van Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 28a4f04ebcda27213d3bac763fb9bea8ea4a0146
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 3%

---

# Vroege aanvullende informatie {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd op de laatste week van elke maand in de [releaseopmerkingen](release-notes.md).

Opmerkingen bij de eerste release hieronder kunnen zonder voorafgaande kennisgeving worden gewijzigd tot de beschikbaarheidsdatum van de release. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in [releaseopmerkingen](release-notes.md), op de datum van vrijgave.

## Opmerkingen bij de vervroegde release september 2023 {#sept-rn-2023}

**Releasedatum**: september 2023

### Nieuwe functies{#sept-2023-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.


<table>
<thead>
<tr>
<th><strong>Geconsolideerde Kanaalrapporten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De functie Kanaalrapport biedt analisten en marketers een uitgebreid overzicht van verkeers- en betrokkenheidsgegevens op kanaalniveau. Als u het menu Rapport wilt openen, hebt u de machtiging Kanaalrapporten weergeven nodig.</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Dataset-exportdoelen (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer-gegevenssets die naar Cloud Storage-doelen worden geëxporteerd, zijn nu over het algemeen beschikbaar. Met deze functie kunt u een live verbinding maken met opslaglocaties in de cloud om de inhoud van uw gegevenssets te exporteren.</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Opslag van gebruikersgegevens voor mobiele toepassingen per sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met deze nieuwe functie kunt u pushgegevens eenvoudig beheren en koppelen aan een specifieke sandbox in App Surfaces.</p>
<p>Raadpleeg de <a href="../in-app/inapp-configuration.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Berekende kenmerken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met berekende kenmerken kunt u gebeurtenisgegevens eenvoudig samenvatten in profielkenmerken via een intuïtieve gebruikersinterface voor verbeterde op gedrag gebaseerde segmentatie, personalisatie en activering. Met deze functie kunt u berekende kenmerken op een zelfservermanier maken, deze beheren en ze in segmentatie gebruiken, in realtime klantprofielbestemmingen of Journey Optimizer.<br/><br/>
Bovendien vereenvoudigt de berekende attributen segmentatie en reisworkflows om u te helpen relevante ervaringen naadloos te leveren. Meer informatie in het dialoogvenster <a href="https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html">gedetailleerde documentatie</a>.</p>
<img src="assets/do-not-localize/computed-attributes.gif">
</tr>
</tbody>
</table>


### Verbeteringen {#sept-2023-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**Personalisatie**

* Naast visuele fragmenten is het nu mogelijk om expressiefragmenten te maken, op te slaan en opnieuw te gebruiken vanuit de Journey Optimizer-interface via de Expressieeditor. Expressiefragmenten vervangen de eerder opgeslagen expressies.

**Waarschuwing**

* Er is een nieuw type systeemwaarschuwing geïntroduceerd. U kunt nu op de hoogte worden gesteld wanneer een publiek dat het lezen uitvoert, mislukt.

**Webkanaal**

* Toepassingen van één pagina (SPA) kunnen nu worden ontworpen in de visuele editor van de webontwerper, zodat u kunt selecteren op welke specifieke weergaven u de wijzigingen van uw webpagina wilt toepassen. Een weergave kan worden gedefinieerd als een hele site of een groep visuele elementen op een site, zoals de startpagina, de hele productsite of het voorkeurenframe voor levering op alle afrekenpagina&#39;s. Om Adobe Journey Optimizer-webcampagnes op SPA te maken en uit te voeren, is een eenmalige ontwikkelaarsinstelling nodig om de weergaven in de Adobe Experience Platform Web SDK-implementatie te definiëren.

* Wanneer u een pagina bewerkt met de webontwerper, kunt u nu rechtstreeks vanuit de **Wijzigingen** deelvenster - zonder dat u een component hoeft te selecteren en te bewerken in de ontwerpinterface.
* Wanneer u websubdomeinen instelt, kunt u nu ook uw eigen subdomein toevoegen, naast het gebruik van een subdomein dat al is gedelegeerd aan de Adobe.

**Journeys**

* Ondersteuning voor aangepaste acties is nu GA. Hierdoor kunt u API-aanroepreacties gebruiken in aangepaste handelingen en uw reis ordenen op basis van deze reacties. Bovendien is een nieuwe guardrail toegevoegd om alle douaneacties tot 5000 vraag/s per eindpunt te beperken.
* Wanneer u een reis dupliceert, kunt u nu de naam van de reiskopie definiëren.

<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**E-mailkanaal**

Met een nieuwe optie in de configuratie van het e-mailoppervlak kunt u ervoor kiezen om transactieberichten naar profielen te verzenden, zelfs als hun e-mailadres voorkomt in de lijst met Adobe Journey Optimizer-onderdrukking.

**Sms-kanaal**

Twee nieuwe velden, **Bericht bij aanmelden** en **Help-bericht**, zijn toegevoegd aan het API-configuratiescherm, zodat gebruikers reacties voor binnenkomende trefwoorden kunnen aanpassen. Merk op dat dit slechts voor de leverancier van SMS van Sinch beschikbaar is.

**Rapportage**

U kunt nu Journey Optimizer-rapporten exporteren als CSV-bestand. [Meer informatie](../reports/global-report.md#export-reports)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->
