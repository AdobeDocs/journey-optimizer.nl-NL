---
title: Conflictbeheer en prioritering
description: Leer hoe u Journey Optimizer-tools voor conflicten en prioritering kunt gebruiken.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: efb943e5a6f27becc6e8b6128b776e46d6141823
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# Conflictbeheer en prioritering {#conflict-prioritization}

## Hulpprogramma&#39;s voor conflictbeheer en -prioriteiten {#tools}

In Journey Optimizer is het beheren van het volume en de timing van campagnes en reizen van essentieel belang om te voorkomen dat klanten met te veel interacties worden overspoeld. Journey Optimizer biedt verschillende tools voor conflictbeheer en prioritering.

Deze hulpmiddelen zijn beschikbaar voor campagnes en unitaire, de Kwalificatie van het Publiek, en gelezen publiekstrajecten.

Door gebruik te maken van deze gereedschappen kunt u zorgen voor soepelere en meer gerichte marketinginspanningen, zodat u de juiste boodschap op het juiste moment kunt afgeven en conflicten en overbelasting kunt voorkomen.

### Conflictdetectie

Met het **hulpmiddel van de conflictopsporing**, kunt u potentiële overlappingen in reizen en campagnes identificeren. Dit is essentieel aangezien teveel gelijktijdige mededelingen tot klantenvermoeidheid kunnen leiden. Met Journey Optimizer kunt u elementen controleren, zoals tijdlijnen, overlappende doelgroepen en kanaalconfiguraties. Door conflicten vroegtijdig te identificeren, kunt u uw campagnes verfijnen om het bombarderen van klanten met veelvoudige berichten tezelfdertijd te vermijden.

➡️ [&#x200B; Leer hoe te om potentiële conflicten in reizen &amp; campagnes te ontdekken &#x200B;](conflicts.md)

### Prioriteitsscores

**Prioriteitsscores** helpen u controleren welke campagnes of reizen belangrijkheid nemen wanneer een klant voor veelvoudige mededelingen kwalificeert. Dit is met name handig voor binnenkomende kanalen, zoals het web en mobiele apparaten, waar op elk moment slechts één campagne kan worden weergegeven. Door een prioritaire score toe te wijzen aan elke reis of campagne, kunt u ervoor zorgen dat de belangrijkste boodschap eerst wordt geleverd.

➡️ [&#x200B; Leer hoe te om prioritaire scores aan reizen &amp; campagnes toe te wijzen &#x200B;](priority-scores.md)

### Regelsets

De reeksen van de regel staan u toe om **samen veelvoudige regels in regelreeksen** te groeperen en hen op de reizen en de campagnes van uw keus toe te passen. Dit verstrekt betere granulariteit om te beperken hoe vaak en hoeveel reizen een klant binnen een bepaald tijdkader kan ingaan of te controleren hoe vaak de gebruikers een bericht afhankelijk van het type van mededeling zullen ontvangen. [&#x200B; leer hoe te met regelreeksen &#x200B;](../conflict-prioritization/rule-sets.md) werken

* **Reis het in kaart brengen &amp; arbitrage**

  Met regelsets kunt u beperken hoe vaak en hoeveel reizen een klant binnen een bepaald tijdsbestek kan invoeren. U kunt ook regels instellen om het aantal reisitems voor een profiel te beperken of het aantal reizen te beperken waarin een klant tegelijkertijd kan worden ingeschreven.

  Bovendien kunt u arbitrageinstellingen gebruiken om te beslissen welke reis een klant moet invoeren als hij of zij in aanmerking komt voor meerdere reizen, waarbij u prioriteitsscores gebruikt om de beste pasvorm te bepalen.

  ➡️ [&#x200B; Leer hoe te met reis het afschilderen &amp; arbitrage te werken &#x200B;](journey-capping.md)

* **het in kaart brengen van de Frequentie door kanaal en communicatietype**

  U kunt regelreeksen ook gebruiken om frequentie het begrenzen door communicatietype (b.v., Verkoop, Bevordering) te plaatsen om het overbelasten van klanten met gelijkaardige berichten te verhinderen. U kunt de frequentie in meerdere kanalen bepalen, waarbij al te gevraagde profielen automatisch worden uitgesloten voor een betere ervaring met klanten.

  ➡️ [&#x200B; Leer hoe te om frequentie het in kaart brengen door kanaal en communicatietype te plaatsen &#x200B;](../conflict-prioritization/channel-capping.md)

## Afbeeldingen en beperkingen

* **Campagnes &amp; prioritaire scores** - In campagnes, is de prioritaire score beschikbaar voor het **Web**, **in-app**, en **code-Gebaseerde** binnenkomende slechts kanalen.

* **de tegenlatentie van het Profiel**

  Het kan tot 10 minuten duren nadat een klant een reis is ingegaan voor de waarde van de profielteller die moet worden bijgewerkt.

  Als een profiel twee reizen binnen een kort tijdsbestek aflegt, wordt bij de tweede reis mogelijk niet goed erkend dat de frequentiegrens al is bereikt, waardoor het profiel beide reizen kan betreden.

* **prioriteit Namespace voor het aftappen van de reisingang**

  Het begrenzen van de ingang wordt slechts gesteund als namespace in de reis wordt geselecteerd hoogste prioritaire namespace die in de zandbak wordt bepaald is. Als namespace prioriteit niet uitdrukkelijk is gevormd, is de gebrek hoogste prioriteit e-mail.

* **Gelijktijdige activeringen in de reizen van de publiekskwalificatie**

  Wanneer de veelvoudige reizen van de publiekskwalificatie door de zelfde gebeurtenis van de publiekskwalificatie worden geactiveerd, dan tellen voor ingangstmogelijkheden zal niet nauwkeurig zijn. Als het aantal cijfers onder het plafond ligt, blijft de reis arbitrair, maar zal de reis niet in staat zijn de meest actuele aantallen te krijgen met gelijktijdige activering.

## Aanvullende bronnen

* **[beheer conflicten](conflicts.md)** - leer hoe te om conflicten tussen overlappende campagnes en reizen te identificeren en op te lossen.
* **[vastgestelde prioritaire scores](priority-scores.md)** - begrijp hoe te om prioritaire scores toe te wijzen en te gebruiken om de prioriteit van de berichtlevering te controleren.
* **[vorm frequentie het in kaart brengen](channel-capping.md)** - ontdekt hoe te om kanaal-vlakke frequentiecappen te plaatsen om over-overseinen te verhinderen.
* **[creeer regelreeksen](rule-sets.md)** - leer hoe te om bedrijfsregels voor geavanceerd conflictbeheer en berichtbeheer te bouwen.
* **[reis-specifiek het begrenzen](journey-capping.md)** - de de afschilderingsregels van het opstellings reis-niveau om berichtfrequentie binnen reizen te controleren.
* **[het beheersleerprogramma&#39;s van het Conflict &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}** - Onderzoek geleidelijke videoleerprogramma&#39;s op conflictbeheer en prioritering.
