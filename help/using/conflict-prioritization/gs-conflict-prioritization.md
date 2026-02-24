---
title: Conflictbeheer en prioritering
description: Leer hoe u Journey Optimizer-tools voor conflicten en prioritering kunt gebruiken.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: a0eda2e1d021af37eb54f3ffa5bac0ac6e8ef6ce
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---

# Conflictbeheer en prioritering {#conflict-prioritization}

In Journey Optimizer is het beheren van het volume en de timing van campagnes en reizen van essentieel belang om te voorkomen dat klanten met te veel interacties worden overspoeld. Het beheer van het conflict en de prioriteitenhulpmiddelen helpen u bedachtzame, goed-getimed mededeling-verhinderend klantenvermoeidheid en het verzekeren van de juiste berichten uw publiek bereiken. Door conflictopsporing, prioriteitsscores en regelsets te gebruiken, kunt u campagnes en reizen stroomlijnen om overlappingen te voorkomen en de frequentie van de balans tussen kanalen te verdelen.

Deze hulpmiddelen zijn beschikbaar voor campagnes en voor unitary, de Kwalificatie van het Publiek, en lees publiekstrajecten. Of u beperkingen instelt op hoe vaak berichten worden verzonden of bepaalt welke campagnes voorrang hebben, deze functies werken samen om de besluitvorming te vereenvoudigen en uw marketingstrategie te optimaliseren.

## Waar begint u {#where-to-start}

| Uw doel | Tool | Actie |
|-----------|------|--------|
| Controleren of reizen of campagnes elkaar overlappen (tijdlijn, publiek, kanaal) | **de opsporing van het Conflict** | [&#x200B; identificeer potentiële conflicten &#x200B;](conflicts.md) |
| Bepaal welk bericht wint wanneer een profiel voor verscheidene kwalificeert | **Prioriteitsscores** | [&#x200B; wijs prioritaire scores toe &#x200B;](priority-scores.md) |
| Beperken hoe vaak of hoeveel berichten een profiel ontvangt | {de reeksen van de 0} Regel **(frequentie die, reis die, stille uren afschilderen) aftappen** | [&#x200B; plaats bericht &amp; reis het begrenzen regels &#x200B;](../../rp_landing_pages/capping-rules-landing-page.md) |

**Typische stroom:** de conflictopsporing van het Gebruik aan vlek overlapt, dan past prioritaire scores en regelreeksen toe om te controleren welke berichten worden verzonden en hoe vaak.

## Hulpmiddelen voor conflictbeheer en -prioritering {#tools}

### Conflictdetectie

Met het **hulpmiddel van de conflictopsporing**, kunt u potentiële overlappingen in reizen en campagnes identificeren. Dit is essentieel aangezien teveel gelijktijdige mededelingen tot klantenvermoeidheid kunnen leiden. Met Journey Optimizer kunt u elementen controleren, zoals tijdlijnen, overlappende doelgroepen en kanaalconfiguraties. Door conflicten vroegtijdig te identificeren, kunt u uw campagnes verfijnen om het bombarderen van klanten met veelvoudige berichten tezelfdertijd te vermijden.

[Leer hoe u mogelijke conflicten tijdens reizen en campagnes kunt detecteren](conflicts.md)

### Prioriteitsscores

**Prioriteitsscores** helpen u controleren welke campagnes of reizen belangrijkheid nemen wanneer een klant voor veelvoudige mededelingen kwalificeert. Dit is met name handig voor binnenkomende kanalen, zoals het web en mobiele apparaten, waar op elk moment slechts één campagne kan worden weergegeven. Door een prioritaire score toe te wijzen aan elke reis of campagne, kunt u ervoor zorgen dat de belangrijkste boodschap eerst wordt geleverd.

[Leer hoe u prioriteitsscores kunt toewijzen aan reizen en campagnes](priority-scores.md)

### Regelsets

De reeksen van de regel staan u toe om **samen veelvoudige regels** te groeperen en hen op de reizen en de campagnes van uw keus toe te passen. Dit verstrekt betere granulariteit om te beperken hoe vaak en hoeveel reizen een klant binnen een bepaald tijdkader kan ingaan, of om te controleren hoe vaak de gebruikers berichten afhankelijk van het type van mededeling ontvangen.

* **Reis het in kaart brengen &amp; arbitrage** - Beperk hoe vaak en hoeveel reizen een klant binnen een bepaald tijdkader kan ingaan. U kunt het aantal reisingangen voor een profiel begrenzen of het aantal reizen beperken een klant kan tezelfdertijd worden ingeschreven. Gebruik arbitrageinstellingen om te bepalen welke reis een klant moet invoeren als hij of zij in aanmerking komt voor meerdere reizen, waarbij gebruik wordt gemaakt van prioriteitsscores om te bepalen wat het beste past. [&#x200B; Leer hoe te met reis het afschilderen &amp; arbitrage te werken &#x200B;](journey-capping.md)

* **het Afbakenen van de Frequentie door kanaal en communicatietype** - vastgestelde frequentie die door communicatie type (b.v., Verkoop, Bevordering) wordt begrensd om het overbelasten van klanten met gelijkaardige berichten te verhinderen. Regelfrequentie over meerdere kanalen, automatisch met uitzondering van al te gevraagde profielen. [&#x200B; Leer hoe te om frequentie het in kaart brengen door kanaal en communicatietype te plaatsen &#x200B;](channel-capping.md)

* **Stil uren** - bepaal op tijd-gebaseerde uitsluitingen zodat worden geen berichten verzonden tijdens specifieke periodes (E-mail, SMS, Duw, WhatsApp). [&#x200B; Leer hoe te om stille uren &#x200B;](quiet-hours.md) te plaatsen

[Leer hoe u met regelsets werkt](rule-sets.md)

## Afbeeldingen en beperkingen {#guardrails}

* **Campagnes &amp; prioritaire scores** - In campagnes, is de prioritaire score beschikbaar voor het **Web**, **in-app**, en **code-Gebaseerde** binnenkomende slechts kanalen.

* **de tegendatentie van het Profiel** - het kan tot 10 minuten nemen nadat een klant een reis voor de waarde van de profielteller is ingegaan die moet worden bijgewerkt. Als een profiel twee reizen binnen een kort tijdsbestek aflegt, wordt bij de tweede reis mogelijk niet goed erkend dat de frequentiegrens al is bereikt, waardoor het profiel beide reizen kan betreden.

* **de prioriteit van Namespace voor het aftappen van de reisingangen** - de toegang het aftappen wordt slechts gesteund als namespace die in de reis wordt geselecteerd de hoogste prioritaire namespace is die in de zandbak wordt bepaald. Als namespace prioriteit niet uitdrukkelijk is gevormd, is de gebrek hoogste prioriteit e-mail.

* **Gelijktijdige activeringen in de reizen van de publiekskwalificatie** - wanneer de veelvoudige reizen van de publiekskwalificatie door de zelfde gebeurtenis van de publiekskwalificatie worden geactiveerd, tellen voor ingangstmogelijkheden zullen niet nauwkeurig zijn. Als het aantal cijfers onder het plafond ligt, blijft de reis arbitrair, maar zal de reis niet in staat zijn de meest actuele aantallen te krijgen met gelijktijdige activering.

## Aanvullende bronnen

* **[identificeer potentiële conflicten](conflicts.md)** - leer hoe te om conflicten tussen overlappende campagnes en reizen te ontdekken en op te lossen.
* **[wijs prioritaire scores](priority-scores.md)** toe - begrijp hoe te om prioritaire scores toe te wijzen en te gebruiken om de prioriteit van de berichtlevering te controleren.
* **[Werk met regelreeksen](rule-sets.md)** - Leer hoe te om regelreeksen voor conflictbeheer en berichtbeheer te bouwen en toe te passen.
* **[Reis het in kaart brengen &amp; arbitrage](journey-capping.md)** - de de afschilderingsregels en arbitrage van het de reis-niveau van de opstelling.
* **[het In kaart brengen van de Frequentie door kanaal](channel-capping.md)** - plaats kanaal-vlakke frequentiecappen om over-overseinen te verhinderen.
* **[plaats stille uren](quiet-hours.md)** - bepaal op tijd-gebaseerde uitsluitingen voor berichtlevering.
* **[het beheersleerprogramma&#39;s van het Conflict &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}** - geleidelijke videoleerprogramma&#39;s.
