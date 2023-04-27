---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met reisactiviteiten
description: Aan de slag met reisactiviteiten
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: reis, activiteiten, aan de slag, gebeurtenissen, actie
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 14%

---

# Aan de slag met reisactiviteiten {#about-journey-activities}

Combineer de verschillende actie-, orkestratie- en gebeurtenisactiviteiten om uw kanaaloverschrijdende scenario’s met meerdere stappen te maken.

## Gebeurtenisactiviteiten {#event-activities}

Gebeurtenissen zijn de aanleiding voor een persoonlijke reis, zoals een online aankoop. Wanneer iemand een reis binnengaat, beweegt hij als individu en bewegen geen twee individuen zich met dezelfde snelheid of langs dezelfde weg. Wanneer u uw reis met een gebeurtenis begint, wordt de reis teweeggebracht wanneer de gebeurtenis wordt ontvangen. Elke persoon op de reis volgt dan, individueel, de volgende stappen die in uw reis worden bepaald.

Gebeurtenissen geconfigureerd door de technische gebruiker (zie [deze pagina](../event/about-events.md)) worden allemaal weergegeven in de eerste categorie van het palet, links op het scherm. De volgende activiteiten zijn beschikbaar:

* [Algemene gebeurtenissen](../building-journeys/general-events.md)
* [Reactie](../building-journeys/reaction-events.md)
* [Segmentkwalificatie](../building-journeys/segment-qualification-events.md)

![](assets/journey43.png)

Begin de reis door een gebeurtenisactiviteit te slepen en neer te zetten. U kunt er ook op dubbelklikken.

![](assets/journey44.png)

## Orkestratieactiviteiten {#orchestration-activities}

Orchestratieactiviteiten zijn verschillende omstandigheden die helpen de volgende stap in de reis te bepalen. Het kan zijn dat de persoon een open steungeval heeft of niet, het weer dat op zijn huidige locatie wordt voorspeld, als hij een aankoop heeft voltooid of niet, of 10 000 loyaliteitspunten bereikt.

In het palet zijn aan de linkerkant van het scherm de volgende orkestactiviteiten beschikbaar:

* [Voorwaarde](../building-journeys/condition-activity.md)
* [Wachten](../building-journeys/wait-activity.md)
* [Segment lezen](../building-journeys/read-segment.md)

![](assets/journey49.png)

## Actieactiviteiten {#action-activities}

Handelingen zijn wat u wilt doen als gevolg van een of andere trigger, zoals het verzenden van een bericht. Het is het traject dat de klant ervaart.

Vanuit het palet, links van het scherm, onder **[!UICONTROL Events]** en **[!UICONTROL Orchestration]**, kunt u de **[!UICONTROL Actions]** categorie. De volgende activiteiten zijn beschikbaar:

* [E-mail, SMS, Push](../building-journeys/journeys-message.md)
* [Aangepaste acties](../building-journeys/using-custom-actions.md)
* [Springen](../building-journeys/jump.md)

![](assets/journey58.png)

Deze activiteiten staan voor de verschillende beschikbare communicatiekanalen. U kunt ze combineren om een scenario voor meerdere kanalen te maken.

Als u aangepaste handelingen hebt geconfigureerd, worden deze ook hier weergegeven. [Meer informatie](../building-journeys/using-custom-actions.md)).

## Best practices {#best-practices}

### Een label toevoegen

Met de meeste activiteiten kunt u een **[!UICONTROL Label]**. Hiermee voegt u een achtervoegsel toe aan de naam die onder uw activiteit op het canvas wordt weergegeven. Dit is handig als u dezelfde activiteit meerdere keren gebruikt en u deze gemakkelijker wilt identificeren. Het zal ook het zuiveren in het geval van fouten gemakkelijker maken en het zal rapporten gemakkelijker te lezen maken. U kunt ook een optionele **[!UICONTROL Description]**.

![](assets/journey-action-label.png)

### Geavanceerde parameters beheren {#advanced-parameters}

De meeste activiteiten geven een aantal geavanceerde en/of technische parameters weer die u niet kunt wijzigen.

![](assets/journey-advanced-parameters.png)

Voor een betere leesbaarheid kunt u deze parameters verbergen met de opdracht **[!UICONTROL Hide read-only fields]** knop.

![](assets/journey-hide-read-only-fields.png)

In bepaalde situaties kunt u de waarden van deze parameters voor specifiek gebruik overschrijven. Als u een waarde wilt afdwingen, klikt u op de knop **[!UICONTROL Enable parameter override]** rechts van het veld. [Meer informatie](../configuration/primary-email-addresses.md#journey-parameters)

![](assets/journey-enable-parameter-override.png)

### Een alternatief pad toevoegen

Wanneer er een fout in een actie of een voorwaarde optreedt, eindigt de journey van een individu. De enige manier om door te gaan is het selectievakje **[!UICONTROL Add an alternative path in case of a timeout or an error]** in te schakelen. Zie [deze sectie](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
