---
title: Conflictbeheer en prioritering
description: Leer hoe u uw inhoud kunt voorvertonen en testen.
feature: Preview, Proofs
role: User
level: Beginner
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: c609694693f11c77bc61ab31f0e7851262aadcce
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---


# Conflictbeheer en prioritering {#conflict-prioritization}

>[!AVAILABILITY]
>
>De hulpmiddelen voor Conflictbeheer en prioritering zijn momenteel alleen beschikbaar als bètaversie voor geselecteerde gebruikers.

In Journey Optimizer is het beheren van het volume en de timing van campagnes en reizen van essentieel belang om te voorkomen dat klanten met te veel interacties worden overspoeld. De volgende twee secties introduceren zeer belangrijke hulpmiddelen om u te helpen evenwicht handhaven en mededelingen aan effectief voorrang geven.

## Mogelijke conflicten tijdens reizen en campagnes weergeven {#conflict}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Conflicterende viewer in campagnes"
>abstract="Dit hulpmiddel kan u helpen overlappingen met andere reizen, campagnes, of kanaalconfiguraties bepalen. Als u overlappingen op publiek wilt identificeren, begin en einddatum, kanaalconfiguratie, kanaal, of regelreeks kunt u potentiële conflicten hier bekijken."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Conflicterende kijker op reis"
>abstract="Dit hulpmiddel kan u helpen overlappingen met andere reizen, campagnes, of kanaalconfiguraties bepalen. Als u overlappingen op publiek wilt identificeren, begin en einddatum, kanaalconfiguratie, kanaal, of regelreeks kunt u potentiële conflicten hier bekijken."

Naarmate de markt het aantal campagnes en reizen in Journey Optimizer verhoogt, wordt het steeds moeilijker voor een marketeer om te weten of zij hun klanten met te veel marketinginteracties bombarderen. daarom is het van essentieel belang dat bij overlappende campagnes en reizen gemakkelijk kan worden vastgesteld dat zij het juiste evenwicht van de marketingcommunicatie bereiken en tegelijkertijd het risico van vermoeidheid van de klant verminderen .

De belangrijkste gebieden om voor potentiële overlapping te controleren zijn:

* **Chronologie** (begin en einddata): Zijn teveel reizen die gelijktijdig lopen?
* **Publiek**: Welk percentage van mijn reispubliek is ook deel van andere reizen?
* **Kanaal**: Zijn er andere mededelingen die voor zelfde timeframe worden gepland, en als zo, hoeveel?
* **het Bedekken van Reeks van de Regel**: Welke types van reizen ben ik bedekken en is er overlapping binnen die?
* **Configuratie van het Kanaal**: Zijn er andere reizen of campagnes gebruikend deze kanaalconfiguratie die deze campagne voor wordt getoond aan de gebruiker zou kunnen verhinderen?

Met Journey Optimizer kunt u controleren of er overlappingen zijn met andere reizen of campagnes. Ga als volgt te werk om dit te doen:

1. Klik op de knop **[!UICONTROL View Potential Conflicts]** op het moment dat u een reis of campagne maakt.

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >De knop **[!UICONTROL View potential conflicts]** wordt beschikbaar om te selecteren zodra u een van de volgende instellingen hebt toegewezen: **[!UICONTROL Start / end date]**, **[!UICONTROL Audience]**, **[!UICONTROL Channel]**, **[!UICONTROL Channel configuration]** en **[!UICONTROL Rule set]** .

1. Het venster **[!UICONTROL Potential conflicts]** wordt geopend, zodat u alle elementen kunt visualiseren die de huidige reis/campagne overlappen.

   U kunt een overlappende reis of campagne rechtstreeks vanuit dit scherm openen door de naam ervan te selecteren.

   ![](assets/potential-conflicts.png)

>[!NOTE]
>
>Als u uw zoekopdracht naar mogelijke overlappingen verder wilt verfijnen, kunt u uw lijst met campagnes en reizen filteren op basis van de velden die u relevant vindt. Selecteer hiertoe het filterpictogram in de overzichtsweergave. [ leer hoe te met filters ](../start/search-filter-categorize.md#filter-lists) werken

Zodra mogelijke overlappingen zijn geïdentificeerd, biedt Journey Optimizer verschillende manieren om deze aan te pakken.

* Pas de **begin/einddata** aan om overlappende campagnes of reizen te vermijden.
* Verfijn **publiek richtend** om overlapping tussen reizen te minimaliseren.
* Voer **frequentiecappen** uit om klanten te verhinderen te veel mededelingen te ontvangen.
* Verminder het aantal **actieve reizen** om klantenervaring effectiever te beheren.
* Plaats **prioriteiten** op binnenkomende acties om de belangrijkste actie te verzekeren wordt getoond aan klanten.

Door deze mogelijkheden leveraging, kunt u ervoor zorgen dat uw marketing inspanningen worden gericht en dat u het juiste evenwicht in uw communicatie strategie handhaaft.

## Prioritaire scores toewijzen aan reizen en campagnes {#priority}

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Prioriteit"
>abstract="Wijs een prioritaire score aan de reis toe, die zich van 0 tot 100 uitstrekken. Een hoger getal geeft een hogere prioriteit aan. De hier ingevoegde prioriteitswaarde wordt overgeërfd door binnenkomende acties (zoals In-App) die zich in deze reis bevinden. Voor situaties waar deze zelfde binnenkomende kanaalconfiguratie in andere campagnes of reizen wordt gebruikt, wordt de binnenkomende actie met de hoogste prioritaire score getoond aan de ontvanger. Als meerdere reizen of campagnes dezelfde score hebben, wordt het element gekozen dat het laatst is gewijzigd."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Prioriteit"
>abstract="Wijs een prioriteitsscore toe aan de campagne, variërend van 0 tot 100. Een hoger getal geeft een hogere prioriteit aan. Voor situaties waarin deze zelfde binnenkomende kanaalconfiguratie (zoals in-App) in andere campagnes of reizen wordt gebruikt, wordt de binnenkomende actie met de hoogste prioritaire score getoond aan de ontvanger. Als meerdere reizen of campagnes dezelfde score hebben, wordt het element gekozen dat het laatst is gewijzigd."

Met Journey Optimizer kunt u een prioriteitsscore toekennen aan een reis of campagne. Prioriteit is essentieel om prioriteit te geven aan een reis, campagne of actie wanneer er een opgelegde beperking is (zoals een frequentiegrens). In situaties waar een klant voor vele reizen, campagnes, of mededelingen kwalificeert en u selectief wilt zijn wat zij zouden moeten ingaan en ontvangen, zou u dit gebied moeten gebruiken.

>[!NOTE]
>
>Prioriteitsscore is beschikbaar voor binnenkomende kanalen: web, in-app en op code gebaseerde kanalen. In reis, is de prioritaire score beschikbaar voor het **in-app** slechts kanaal.

Het toewijzen van een prioritaire score is essentieel voor binnenkomende communicatie zoals Web, Mobiel, &amp; in-App. Als u meerdere campagnes hebt met dezelfde kanaalconfiguratie (bijvoorbeeld een banner boven op uw webpagina), kan dit problematisch zijn omdat slechts inhoud van één campagne gemakkelijk kan worden weergegeven. Bij de prioriteitsscore voegt u uw voorkeur in waarvoor de campagne moet worden weergegeven wanneer de ontvanger in aanmerking komt voor meer dan één campagne.

Als u een prioriteitsscore wilt toewijzen aan een reis of campagne, voert u een numerieke waarde (van 0 tot 100) in het veld **[!UICONTROL Priority score]** in in de eigenschappen van de reis of campagne. Let op: hoe hoger het getal, hoe hoger de prioriteit. Als u deze campagne zou ontwerpen en ervoor wilde zorgen dat deze inhoud van de campagne wordt getoond, zou u het een score van 100 geven.

![](assets/priority-score.png)

Voor situaties waarin twee campagnes dezelfde prioriteitsscore hebben, wordt de laatst geactiveerde campagne getoond.
