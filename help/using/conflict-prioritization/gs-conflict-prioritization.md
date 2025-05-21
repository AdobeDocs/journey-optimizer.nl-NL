---
title: Conflictbeheer en prioritering
description: Leer hoe u Journey Optimizer-tools voor conflicten en prioritering kunt gebruiken.
role: User
level: Beginner
badge: label="Beperkte beschikbaarheid"
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: f55f985375cf360ce55074cb227b6c424db05b5c
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Conflictbeheer en prioritering {#conflict-prioritization}

>[!AVAILABILITY]
>
>Conflict- en prioriteitsmogelijkheden zijn momenteel beschikbaar in Beperkte beschikbaarheid voor een geselecteerde groep klanten. Houd er rekening mee dat deze functies in de toekomst geleidelijk aan voor meer gebruikers beschikbaar zullen zijn. Neem contact op met uw accountteam als u interesse hebt in het toevoegen van deze functies aan de wachtlijst.

In Journey Optimizer is het beheren van het volume en de timing van campagnes en reizen van essentieel belang om te voorkomen dat klanten met te veel interacties worden overspoeld. Journey Optimizer biedt verschillende tools voor conflictbeheer en prioritering.

Deze hulpmiddelen zijn beschikbaar voor campagnes en unitaire, de Kwalificatie van het Publiek, en gelezen publiekstrajecten.

Door gebruik te maken van deze gereedschappen kunt u zorgen voor soepelere en meer gerichte marketinginspanningen, zodat u de juiste boodschap op het juiste moment kunt afgeven en conflicten en overbelasting kunt voorkomen.

## Hulpprogramma&#39;s voor conflictbeheer en -prioriteiten {#tools}

Met het **hulpmiddel van de conflictopsporing**, kunt u potentiële overlappingen in reizen en campagnes identificeren. Dit is essentieel aangezien teveel gelijktijdige mededelingen tot klantenvermoeidheid kunnen leiden. Met Journey Optimizer kunt u elementen controleren, zoals tijdlijnen, overlappende doelgroepen en kanaalconfiguraties. Door conflicten vroegtijdig te identificeren, kunt u uw campagnes verfijnen om het bombarderen van klanten met veelvoudige berichten tezelfdertijd te vermijden. [ Leer hoe te om potentiële conflicten in reizen &amp; campagnes te ontdekken ](conflicts.md)

Bovendien, **prioritaire scores** hulp u controleert welke campagnes of reizen belangrijkheid nemen wanneer een klant voor veelvoudige mededelingen kwalificeert. Dit is met name handig voor binnenkomende kanalen, zoals het web en mobiele apparaten, waar op elk moment slechts één campagne kan worden weergegeven. Door een prioritaire score toe te wijzen aan elke reis of campagne, kunt u ervoor zorgen dat de belangrijkste boodschap eerst wordt geleverd. [ Leer hoe te om prioritaire scores aan reizen &amp; campagnes toe te wijzen ](priority-scores.md)

**Eis het in kaart brengen &amp; de arbitrage** staat u toe om te beperken hoe vaak en hoeveel reizen een klant binnen een bepaald tijdkader kan ingaan. U kunt regels instellen om het aantal reisitems voor een profiel te beperken of het aantal reizen te beperken waarin een klant tegelijkertijd kan worden ingeschreven. Bovendien kunt u arbitrageinstellingen gebruiken om te beslissen welke reis een klant moet invoeren als hij of zij in aanmerking komt voor meerdere reizen, waarbij u prioriteitsscores gebruikt om de beste pasvorm te bepalen. [ Leer hoe te met reis het afschilderen &amp; arbitrage te werken ](journey-capping.md)

Tot slot kunt u regelreeksen ook gebruiken om **frequentie het in kaart brengen door communicatietype** (b.v., Verkoop, Bevordering) te plaatsen om het overbelasten van klanten met gelijkaardige berichten te verhinderen. U kunt de frequentie in meerdere kanalen bepalen, waarbij al te gevraagde profielen automatisch worden uitgesloten voor een betere ervaring met klanten. [ leer hoe te met regelreeksen ](../configuration/rule-sets.md) werken</li></ul>

Door deze functies te benutten, kunt u ervoor zorgen dat marketing soepeler en gerichter wordt uitgevoerd, zodat u de juiste boodschap op het juiste moment kunt afgeven en conflicten en overbelasting worden voorkomen.

## Afbeeldingen en beperkingen

**het in kaart brengen van de Frequentie &amp; partijpubliek**

Voor frequentiecontrole, zowel kanaal als reis, als het gebruikte publiek een partijpubliek is, dan zal de waarde van de profielteller die op het tijdstip van ingang in de reis van verwijzingen wordt voorzien, of berichtruntime voor een kanaalmededeling van de dagelijkse momentopname zijn die wordt genomen.

Dit kan problematisch zijn, omdat klanten de maximale frequentiegrenzen kunnen overschrijden als ze een andere reis hebben aangedaan of een andere communicatie hebben ontvangen tussen het tijdstip van de dagelijkse momentopname en het tijdstip van de reis (of het bericht dat wordt bezorgd).

**het in kaart brengen van de Frequentie &amp; het stromen publiek**

Voor streaming publiek kan het tot 2 uur duren voordat het systeem een bijgewerkte tellerwaarde herkent en daarom raden we aan om communicatie en reizen met tussenpozen minimaal twee uur te laten duren om dit risico te beperken.

**Reizen begin tijd**

Om ervoor te zorgen dat de functies voor conflictbeheer en prioritering correct werken, raden we u aan de begintijd van uw reis ten minste 10 minuten in de toekomst in te stellen, zodat het systeem de teller dienovereenkomstig kan bijwerken.

Als klanten hun plafond al hebben bereikt bij het betreden van een reis, zullen ze nog steeds geen toegang krijgen, maar als ze hun plafond nog niet hebben bereikt, zal de teller niet worden verhoogd.

**Reisarbitrage**

Vooralsnog worden alleen lezenkijkreizen ondersteund voor reisarbitrage. Arbitrageinstellingen kunnen niet worden gebruikt voor eenheids- of publieksclassificatietrajecten.
