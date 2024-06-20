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
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 1%

---


# Profieltoegangsbeheer {#entry-management}

Er zijn vier soorten reizen:

* **Eenmalige gebeurtenis** ritten: deze reizen beginnen met een eenmalig evenement. Wanneer de gebeurtenis wordt ontvangen, gaat het bijbehorende profiel de reis in. [Meer informatie](#entry-unitary)

* **Zakelijke gebeurtenis** ritten: deze reizen beginnen met een Business-evenement, onmiddellijk gevolgd door een Read-publiek. Wanneer de gebeurtenis wordt ontvangen, gaan profielen die tot het doelpubliek behoren de reis in. Voor elk profiel wordt één exemplaar van deze reis gemaakt. [Meer informatie](#entry-business)

* **Lees publiek** ritten: deze reizen beginnen met een Leespubliek. Wanneer de reis wordt uitgevoerd, komen profielen van het doelpubliek de reis binnen. Voor elk profiel wordt één exemplaar van deze reis gemaakt. Deze reizen kunnen terugkeren of eenmalig zijn. [Meer informatie](#entry-read-audience)

* **kwalificatie publiek** ritten: deze reizen beginnen met een kwalificatieevenement Publiek. Deze reizen luisteren naar de in- en uitgangen van profielen in het publiek. Wanneer dit gebeurt, gaat het bijbehorende profiel de reis in. [Meer informatie](#entry-unitary)

In alle reistypes kan een profiel niet meerdere keren tegelijk aanwezig zijn in dezelfde reis. Om te controleren of een persoon op reis is, wordt de profielidentiteit gebruikt als sleutel. Het systeem staat niet toe dat dezelfde sleutel, bijvoorbeeld de sleutel CRMID=3224, zich op verschillende plaatsen op dezelfde reis bevindt.

## Eenheids- en publiekskwalificatietrajecten{#entry-unitary}

Bij eenheids- en publiekskwalificatietrajecten kunt u re-entry in- of uitschakelen:

* Als re-entry wordt toegelaten, kan een profiel een reis verscheidene keren ingaan, maar kan het niet doen tot hij het vorige geval van de reis volledig verliet.

* Als re-entry gehandicapt is, kan een profiel niet veelvoudige tijden de zelfde reis, binnen de globale reis timeout ingaan. Zie dit [sectie](../building-journeys/journey-properties.md#global_timeout).

Bij reizen is standaard opnieuw toegang mogelijk. Wanneer de **Hernieuwde toegang toestaan** -optie is geactiveerd, de **Wachttijd bij terugkeer** wordt weergegeven. Hiermee kunt u de tijd definiëren die moet worden gewacht voordat een profiel de reis opnieuw kan betreden. Hierdoor wordt voorkomen dat ritten meerdere keren ten onrechte worden geactiveerd voor dezelfde gebeurtenis. Het veld wordt standaard ingesteld op 5 minuten. De maximale duur is 91 dagen ([algemene time-out](journey-properties.md#global_timeout)).

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![](assets/journey-re-entrance.png)

Na de hertoelatingsperiode kunnen profielen de reis opnieuw betreden. Als u dit wilt voorkomen en het opnieuw invoeren van deze profielen volledig wilt uitschakelen, kunt u een voorwaarde toevoegen om te testen of het profiel al dan niet is ingevoerd met behulp van profiel- of publieksgegevens.

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## Zakelijke reizen{#entry-business}

<!--
Business events follow re-entrance rules in the same way as for unitary events. If a journey allows re-entrance, the next business event will be processed.
-->

Als u meerdere bedrijfsgebeurtenissen wilt uitvoeren, activeert u de bijbehorende optie in het dialoogvenster **[!UICONTROL Execution]** sectie van de reiseigenschappen.

![](assets/business-entry.png)

In het geval van bedrijfsgebeurtenissen, voor een bepaalde reis, worden de publieksgegevens die bij eerste uitvoering worden teruggewonnen opnieuw gebruikt tijdens een tijdvenster van 1 uur.

Een profiel kan meerdere keren aanwezig zijn op dezelfde reis, tegelijkertijd, maar in de context van verschillende bedrijfsgebeurtenissen.

Raadpleeg deze voor meer informatie [sectie](../event/about-creating-business.md)

## Reizen voor het publiek lezen{#entry-read-audience}

Lezen van het publiek kunnen terugkerend of one-shot zijn:

* Voor niet-terugkerende ritten: het profiel komt slechts eenmaal binnen.

* Voor terugkerende reizen: standaard komen alle profielen van het publiek de reis in bij elke terugkerende reis. Ze moeten de reis afmaken voordat ze in een ander voorval kunnen terugkeren.

Er zijn twee opties beschikbaar voor terugkerende lezersreizen:

* **Incrementeel lezen** optie: wanneer een reis met een terugkerende **Lees publiek** voert voor het eerst uit, alle profielen in het publiek gaan de reis in. Met deze optie kunt u zich na de eerste keer richten op alleen de personen die het publiek zijn binnengekomen sinds de laatste uitvoering van de reis.

  >[!NOTE]
  >
  >Als u zich richt op [aangepast uploadpubliek](../audience/about-audiences.md#segments-in-journey-optimizer) tijdens uw reis worden profielen alleen bij de eerste herhaling opgehaald als deze optie is ingeschakeld tijdens een terugkerende reis , omdat deze doelgroepen vast zijn .

* **Herkomst forceren bij herhaling**: met deze optie kunt u alle profielen die zich nog in de reis bevinden, automatisch laten afsluiten bij de volgende uitvoering. Als de levensduur van uw profielen tijdens deze reis langer kan zijn dan de herhalingsfrequentie (bijvoorbeeld als u wachtactiviteiten gebruikt), activeert u deze optie niet om ervoor te zorgen dat profielen hun reis kunnen voltooien.

![](assets/read-audience-options.png)

Raadpleeg deze voor meer informatie [sectie](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
