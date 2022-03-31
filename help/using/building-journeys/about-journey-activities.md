---
title: Informatie over reisactiviteiten
description: Meer informatie over reisactiviteiten
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 24%

---

# Informatie over reisactiviteiten {#about-journey-activities}

Combineer de verschillende actie-, orkestratie- en gebeurtenisactiviteiten om uw kanaaloverschrijdende scenario’s met meerdere stappen te maken.

## Gebeurtenisactiviteiten {#event-activities}

De gebeurtenissen die door de technische gebruiker worden gevormd (zie [deze pagina](../event/about-events.md)) worden allemaal weergegeven in de eerste categorie van het palet, links op het scherm. De volgende activiteiten zijn beschikbaar:

* [Algemene gebeurtenissen](../building-journeys/general-events.md)
* [Reactie](../building-journeys/reaction-events.md)
* [Segmentkwalificatie](../building-journeys/segment-qualification-events.md)

![](assets/journey43.png)

Begin de reis door een gebeurtenisactiviteit te slepen en neer te zetten. U kunt er ook op dubbelklikken.

![](assets/journey44.png)

## Orkestratieactiviteiten {#orchestration-activities}

In het palet zijn aan de linkerkant van het scherm de volgende orkestactiviteiten beschikbaar:

* [Voorwaarde](../building-journeys/condition-activity.md)
* [Einde](../building-journeys/end-activity.md)
* [Wachten](../building-journeys/wait-activity.md)
* [Segment lezen](../building-journeys/read-segment.md)

![](assets/journey49.png)

## Actieactiviteiten {#action-activities}

Vanuit het palet, links van het scherm, onder **[!UICONTROL Events]** en **[!UICONTROL Orchestration]**, vindt u de **[!UICONTROL Actions]** categorie. De volgende activiteiten zijn beschikbaar:

* [Bericht](../building-journeys/journeys-message.md)
* [Aangepaste acties](../building-journeys/using-custom-actions.md)
* [Springen](../building-journeys/jump.md)

![](assets/journey58.png)

Deze activiteiten staan voor de verschillende beschikbare communicatiekanalen. U kunt ze combineren om een scenario voor meerdere kanalen te maken.

Als u douaneacties hebt gevormd, zullen zij hier verschijnen (zie [deze pagina](../building-journeys/using-custom-actions.md)).

## Best practices {#best-practices}

Met de meeste activiteiten kunt u een **[!UICONTROL Label]**. Hiermee voegt u een achtervoegsel toe aan de naam die onder uw activiteit op het canvas wordt weergegeven. Dit is handig als u dezelfde activiteit meerdere keren gebruikt en u deze gemakkelijker wilt identificeren. Het zal ook het zuiveren in het geval van fouten gemakkelijker maken en het zal rapporten gemakkelijker te lezen maken. U kunt ook een optionele **[!UICONTROL Description]**.

![](assets/journey59bis.png)

Wanneer er een fout in een actie of een voorwaarde optreedt, eindigt de journey van een individu. De enige manier om door te gaan is het selectievakje **[!UICONTROL Add an alternative path in case of a timeout or an error]** in te schakelen. Zie [deze sectie](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)