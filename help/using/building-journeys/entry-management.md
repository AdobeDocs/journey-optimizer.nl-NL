---
solution: Journey Optimizer
product: journey optimizer
title: Profielbeheer
description: Leer hoe u profielinvoer beheert
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: terugkeer, reis, profiel, terugkerend
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 1%

---


# Profieltoegangsbeheer {#entry-management}

Profielbeheer is afhankelijk van het type reis.

## Soorten reizen {#types-of-journeys}

Met Adobe Journey Optimizer kunt u de volgende soorten reizen maken:

* **Eenheids gebeurtenis** reizen: Deze reizen beginnen met een Unitaire gebeurtenis. Wanneer de gebeurtenis wordt ontvangen, gaat het bijbehorende profiel de reis in. [Meer informatie](#entry-unitary)

* **reizen van de bedrijfs gebeurtenis**: Deze reizen beginnen met een Bedrijfs gebeurtenis onmiddellijk die door a **wordt gevolgd leest publiek** activiteit. Wanneer de gebeurtenis wordt ontvangen, gaan profielen die tot het doelpubliek behoren de reis in. Voor elk profiel wordt één exemplaar van deze reis gemaakt. [Meer informatie](#entry-business)

* **leest publiek** reizen: Deze reizen beginnen met a **gelezen luisteraaractiviteit**. Wanneer de reis wordt uitgevoerd, komen profielen van het doelpubliek de reis binnen. Voor elk profiel wordt één exemplaar van deze reis gemaakt. Deze reizen kunnen terugkeren of &quot;one-shot&quot; zijn. [Meer informatie](#entry-read-audience)

* **reizen van de kwalificatie van het publiek 0&rbrace; &lbrace;: deze reizen beginnen met een de kwalificatiegebeurtenis van het Publiek.** Deze reizen luisteren naar de in- en uitgangen van profielen in het publiek. Wanneer dit gebeurt, gaat het bijbehorende profiel de reis in. [Meer informatie](#entry-unitary)

In alle vervoerstypes, kan een profiel niet veelvoudige tijden in de zelfde reis, tezelfdertijd, voor alle actieve [&#x200B; versies van de reis &#x200B;](publishing-the-journey.md#journey-versions-journey-versions) zijn. Om te controleren of een persoon op reis is, wordt de profielidentiteit gebruikt als sleutel. Het systeem staat niet toe dat dezelfde sleutel, bijvoorbeeld de sleutel `CRMID=3224`, zich op verschillende plaatsen op dezelfde reis bevindt.

## Eenheids- en publiekskwalificatietrajecten{#entry-unitary}

In **de gebeurtenis van de Eenheid** en **de kwalificatiereizen van het publiek**, kunt u terugkeer toelaten of onbruikbaar maken:

* Als de terugkeer wordt toegelaten, kan een profiel een reis verscheidene keren ingaan, maar kan het niet doen tot hij het vorige geval van de reis volledig verliet.

* Als de terugkeer wordt onbruikbaar gemaakt, kan een profiel niet veelvoudige tijden de zelfde reis, binnen de globale reis timeout periode ingaan. Zie deze [&#x200B; sectie &#x200B;](../building-journeys/journey-properties.md#global_timeout).

Bij reizen is standaard terugkeer toegestaan. Wanneer **toe staat terugkeer** optie wordt geactiveerd, **de ingang wacht periode** gebied wordt getoond. Hiermee kunt u de tijd definiëren die moet worden gewacht voordat een profiel de reis opnieuw kan betreden. Hierdoor wordt voorkomen dat ritten meerdere keren ten onrechte worden geactiveerd voor dezelfde gebeurtenis. Het veld wordt standaard ingesteld op 5 minuten. De maximumduur is 91 dagen ([&#x200B; globale onderbreking &#x200B;](journey-properties.md#global_timeout)).

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![](assets/journey-re-entrance.png)

Na de periode van terugkeer kunnen profielen de reis opnieuw ingaan. Als u dit wilt voorkomen en de toegang voor deze profielen volledig wilt uitschakelen, kunt u een voorwaarde toevoegen om te testen of het profiel al dan niet is ingevoerd. Gebruik hiervoor profiel- of publieksgegevens.

<!--
Due to the 30-day journey timeout, when journey reentrance is not allowed, we cannot make sure the reentrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## Zakelijke reizen {#entry-business}

<!--
Business events follow reentrance rules in the same way as for unitary events. If a journey allows reentrance, the next business event will be processed.
-->

In **Bedrijfs reizen**, om veelvoudige bedrijfs gebeurtenisuitvoeringen toe te staan, activeer de overeenkomstige optie in de **[!UICONTROL Execution]** sectie van de reis eigenschappen.

![](assets/business-entry.png)

In het geval van bedrijfsgebeurtenissen, voor een bepaalde reis, worden de publieksgegevens die bij eerste uitvoering worden teruggewonnen opnieuw gebruikt tijdens een tijdvenster van 1 uur.

Een profiel kan meerdere keren aanwezig zijn op dezelfde reis, tegelijkertijd, maar in de context van verschillende bedrijfsgebeurtenissen.

Voor meer informatie, verwijs naar deze [&#x200B; sectie &#x200B;](../event/about-creating-business.md)

## Reizen voor het publiek lezen {#entry-read-audience}

**leest publiek** reizen kan terugkomen of &quot;one-shot&quot;zijn:

* Voor eenmalige of eenmalige ritten: het profiel komt één keer en slechts één keer op de reis binnen.

* Voor terugkerende reizen: standaard komen alle profielen van het publiek de reis in bij elke terugkerende reis. Ze moeten de reis afmaken voordat ze in een ander voorval kunnen terugkeren.

Er zijn verschillende opties beschikbaar voor terugkerende lezersreizen. Voor meer informatie, verwijs naar [&#x200B; Gebruik een publiek in een reis &#x200B;](../building-journeys/read-audience.md) sectie.

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
