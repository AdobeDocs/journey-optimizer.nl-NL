---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Opmerkingen bij de vervroegde release van Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1c65043965d1335297127f6cc6c23ec9a7893463
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 2%

---

# Vroege aanvullende informatie {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd op de laatste week van elke maand in de [releaseopmerkingen](release-notes.md).

Opmerkingen bij de eerste release hieronder kunnen zonder voorafgaande kennisgeving worden gewijzigd tot de beschikbaarheidsdatum van de release. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in [releaseopmerkingen](release-notes.md), op de datum van vrijgave.

## Opmerkingen bij de vervroegde release februari 2024 {#e-2024}

**Releasedatum**: 21 februari 2024

### Nieuwe functies{#e-features}

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
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Frequentieregels voor SMS en Direct Mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu Frequentieregels voor SMS en Direct Mail-kanalen maken. De frequentieregels sluiten over-gevraagde profielen automatisch uit van berichten en acties wanneer de frequentiedrempel wordt bereikt. <br/><br/></p>
<img src="assets/do-not-localize/sms-dm-rules.gif">
</tr>
</tbody>
</table>

### Verbeteringen {#e-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Doelgroepen**

* **Zaadlijsten** - Varianten worden nu ondersteund bij gebruik **zaadlijsten**. Zoals elk profiel van het doelpubliek, ontvangen de zaadadressen een exemplaar van alle varianten van het zelfde bericht (zoals de verschillende behandelingen van een inhoudexperiment).

Eerder beschikbaar als Beta, zijn de volgende verbeteringen nu beschikbaar aan alle gebruikers:

* U kunt nu **publiek gemaakt via publiekscompositie** en verrijkingskenmerken gebruiken in Reizen. [Meer informatie](../building-journeys/read-audience.md)

* U kunt nu **publiek geüpload uit een CSV-bestand** in reizen en campagnes. [Meer informatie](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* Het gebruik van soorten publiek en kenmerken van de compositie van het publiek en aangepaste upload (CSV-bestand) is momenteel niet beschikbaar voor gebruik met het gezondheidsschild of het privacyschild.
  >* Houd er rekening mee dat het uploaden van het publiek vanaf een CSV-bestandsverbetering geleidelijk wordt uitgevoerd gedurende enkele dagen na de eerste release. Sommige gebruikers hebben direct toegang, maar anderen kunnen een vertraging ervaren voordat deze beschikbaar wordt in hun accounts.

**Reizen**

* **Uw reizen filteren** - U kunt nu **aangepaste datums om de reizen te filteren** voorraad, naast de bestaande vooraf gedefinieerde datumfilters. Op deze manier kunt u de lijst verfijnen door ritten weer te geven die op een bepaalde datum zijn gepubliceerd, binnen een bepaalde maand, gedurende een heel jaar, of binnen een bepaald tijdsbereik.
* **Aangepaste acties** - U kunt nu een update uitvoeren naar de header &#39;content-type&#39; in **aangepaste handelingen**.
* **Configuratie** - Het attribuut identityMap in stepEvents is nu voorgevuld. De primaire identiteit wordt gedefinieerd als &quot;primary = true&quot;.
* **Gebruikersinterface** - De bovenste balk, in reisschermen, is gereorganiseerd voor een betere ervaring. Onder de verschillende updates ziet u dat het potlood-pictogram waarmee u de reiseigenschappen kunt openen nu links van de bovenste balk naast de naam van de rit wordt weergegeven.

**Sms-kanaal**

* **Trefwoorden voor aanmelden/uitschakelen** - Wanneer u uw SMS-kanaal configureert, kunt u nu het **Trefwoorden voor Inschakelen en Uitschakelen** volgens uw voorkeuren. Journey Optimizer activeert de reactie op basis van deze opgegeven trefwoorden.

**Campagnes**

* **API-gestuurde campagnes** - De cURL-code die is gegenereerd na het activeren van een API-geactiveerde campagne is verbeterd. Het omvat nu alle personaliseringsvariabelen (profiel en context) die in het bericht worden gebruikt.

**Beslissingsbeheer**

* **Afdekregels** - U kunt nu toevoegen **meerdere uitlijningsregels** voor één voorstel. Dit staat u toe om het niveau van controle over de manier te verhogen de aanbiedingen worden verzonden.

**Contentsjablonen**

* **Miniatuur** - A **miniatuurweergave** is nu beschikbaar voor inhoudssjablonen en fragmenten voor betere visuele toegang.

  >[!AVAILABILITY]
  >
  >Deze mogelijkheid wordt geleidelijk geïmplementeerd in de omgeving van klanten die deze release start.

* **Multikanaalsjablonen** - Inhoudssjablonen zijn nu beschikbaar voor **alle kanalen**, behalve Web. Voor E-mail kunt u nu het type (HTML of Inhoud) selecteren.
