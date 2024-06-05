---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met reisactiviteiten
description: Aan de slag met reisactiviteiten
feature: Journeys, Activities, Overview
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: reis, activiteiten, aan de slag, gebeurtenissen, actie
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 9562a194244e2a3323680d98cc8aa5ed65d93a67
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Aan de slag met reisactiviteiten {#about-journey-activities}

Combineer de verschillende gebeurtenis-, organisatie- en actieactiviteiten om uw meerstapsscenario&#39;s voor meerdere kanalen te maken.

## Gebeurtenisactiviteiten {#event-activities}

Persoonlijke reizen worden veroorzaakt door gebeurtenissen, zoals een online aankoop. Als een profiel eenmaal een reis binnengaat, bewegen ze als individu door en bewegen geen twee individuen zich met dezelfde snelheid of langs hetzelfde pad. Wanneer u uw reis met een gebeurtenis begint, wordt de reis teweeggebracht wanneer de gebeurtenis wordt ontvangen. Elke persoon op de reis volgt dan, individueel, de volgende stappen die in uw reis worden bepaald.

Gebeurtenissen geconfigureerd door de technische gebruiker (zie [deze pagina](../event/about-events.md)) worden allemaal weergegeven in de eerste categorie van het palet, links op het scherm. De volgende activiteiten zijn beschikbaar:

* [Algemene gebeurtenissen](../building-journeys/general-events.md)
* [Reactie](../building-journeys/reaction-events.md)
* [Poortkwalificatie](../building-journeys/audience-qualification-events.md)

![](assets/journey43.png)

Begin de reis door een gebeurtenisactiviteit te slepen en neer te zetten. U kunt er ook op dubbelklikken.

![](assets/journey44.png)

## Orchestratie {#orchestration-activities}

Orchestratieactiviteiten zijn verschillende omstandigheden die helpen de volgende stap in de reis te bepalen. Het kan zijn dat de persoon een open steungeval heeft of niet, het weer dat op zijn huidige locatie wordt voorspeld, als hij een aankoop heeft voltooid of niet, of 10 000 loyaliteitspunten bereikt.

In het palet zijn aan de linkerkant van het scherm de volgende orkestactiviteiten beschikbaar:

* [Voorwaarde](../building-journeys/condition-activity.md)
* [Wachten](../building-journeys/wait-activity.md)
* [Publiek lezen](../building-journeys/read-audience.md)

![](assets/journey49.png)

## Acties {#action-activities}

Handelingen zijn wat u wilt doen als gevolg van een of andere trigger, zoals het verzenden van een bericht. Het is het traject dat de klant ervaart.

Vanuit het palet, links van het scherm, onder **[!UICONTROL Events]** en **[!UICONTROL Orchestration]**, kunt u de **[!UICONTROL Actions]** categorie. De volgende activiteiten zijn beschikbaar:

* [E-mail, SMS, Push](../building-journeys/journeys-message.md)
* [Aangepaste acties](../building-journeys/using-custom-actions.md)
* [Springen](../building-journeys/jump.md)

![](assets/journey58.png)

Deze activiteiten vertegenwoordigen de verschillende beschikbare communicatiekanalen. U kunt ze combineren om een scenario voor meerdere kanalen te maken.

Als u aangepaste handelingen hebt geconfigureerd, worden deze ook hier weergegeven. [Meer informatie](../building-journeys/using-custom-actions.md)).

## Aanbevolen procedures {#best-practices}

### Een label toevoegen

Met de meeste activiteiten kunt u een **[!UICONTROL Label]**. Hiermee voegt u een achtervoegsel toe aan de naam die onder uw activiteit op het canvas wordt weergegeven. Dit is handig als u dezelfde activiteit meerdere keren gebruikt en u deze gemakkelijker wilt identificeren. Het zal ook het zuiveren in het geval van fouten gemakkelijker maken en het zal rapporten gemakkelijker te lezen maken. U kunt ook een optionele **[!UICONTROL Description]**.

![](assets/journey-action-label.png)

>[!NOTE]
>
>Voor bepaalde activiteiten is de id ook zichtbaar in het deelvenster. Deze id kan worden gebruikt in rapportage als een stabielere sleutel dan het label, dat kan veranderen.

### Geavanceerde parameters beheren {#advanced-parameters}

De meeste activiteiten geven een aantal geavanceerde en/of technische parameters weer die u niet kunt wijzigen.

![](assets/journey-advanced-parameters.png)

Voor een betere leesbaarheid kunt u deze parameters verbergen met de opdracht **[!UICONTROL Hide read-only fields]** knop.

![](assets/journey-hide-read-only-fields.png)

In bepaalde situaties kunt u de waarden van deze parameters voor specifiek gebruik overschrijven. Als u een waarde wilt afdwingen, klikt u op de knop **[!UICONTROL Enable parameter override]** rechts van het veld. [Meer informatie](../configuration/primary-email-addresses.md#journey-parameters)

![](assets/journey-enable-parameter-override.png)

### Een alternatief pad toevoegen

Wanneer een fout in een actie of een voorwaarde voorkomt, de reis van een individuele einden. De enige manier om door te gaan is door het selectievakje in te schakelen **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Zie [deze sectie](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
