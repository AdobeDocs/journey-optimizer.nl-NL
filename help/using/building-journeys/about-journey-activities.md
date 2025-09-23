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
version: Journey Orchestration
source-git-commit: 9336b77e5b7682923dca6e95f0ede67c0d9b0f85
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 11%

---

# Aan de slag met reisactiviteiten {#about-journey-activities}

Combineer de verschillende gebeurtenis-, organisatie- en actieactiviteiten om uw meerstapsscenario&#39;s voor meerdere kanalen te maken.

## Gebeurtenisactiviteiten {#event-activities}

Persoonlijke reizen worden veroorzaakt door gebeurtenissen, zoals een online aankoop. Als een profiel eenmaal een reis binnengaat, worden deze als individu doorlopen en bewegen geen twee personen zich met dezelfde snelheid of langs hetzelfde pad. Wanneer u uw reis met een gebeurtenis begint, teweegbrengt de reis teweeg wanneer de gebeurtenis wordt ontvangen. Elke persoon op de reis volgt dan, individueel, de volgende stappen die in uw reis worden bepaald.

De gebeurtenissen die door de technische gebruiker worden gevormd (zie [ deze pagina ](../event/about-events.md)) worden allen getoond in de eerste categorie van het palet, op de linkerkant van het scherm. De volgende gebeurtenisactiviteiten zijn beschikbaar:

* [Algemene gebeurtenissen](../building-journeys/general-events.md)
* [Reactie](../building-journeys/reaction-events.md)
* [Poortkwalificatie](../building-journeys/audience-qualification-events.md)

![ de activiteitenpalet van de Gebeurtenis in de reisontwerper ](assets/journey43.png)

U start de reis door een gebeurtenisactiviteit te slepen en neer te zetten. U kunt er ook op dubbelklikken.

![ belemmering en dalingsgebeurtenisactiviteit in de reisontwerper ](assets/journey44.png)

## Orchestratie {#orchestration-activities}

Orchestratieactiviteiten zijn verschillende omstandigheden die helpen de volgende stap in de reis te bepalen. Deze voorwaarden kunnen omvatten of de persoon een open steungeval heeft, het weer dat op zijn huidige plaats wordt voorspeld, of zij een aankoop voltooiden, of of zij 10.000 loyaliteitspunten bereikt.

In het palet zijn aan de linkerkant van het scherm de volgende orkestactiviteiten beschikbaar:

<!--* [Optimize](optimize.md)-->
* [Publiek lezen](read-audience.md)
* [Wachten](wait-activity.md)
* [Inhoudsbeslissing](content-decision.md)
* [Opzoeken gegevensset](dataset-lookup.md)

![ de activiteitenpalet van Orchestratie in de reisontwerper ](assets/journey-orchestration-activities.png)

## Actieactiviteiten {#action-activities}

Handelingen zijn wat u wilt doen als gevolg van een of andere trigger, zoals het verzenden van een bericht. Het is het stukje van de reis dat de klant ervaart.

In het palet, links op het scherm, onder **[!UICONTROL Events]** en **[!UICONTROL Orchestration]** , kunt u de categorie **[!UICONTROL Actions]** vinden. De volgende activiteiten zijn beschikbaar:

* [Ingebouwde kanaalhandelingen](../building-journeys/journeys-message.md)
* [Aangepaste acties](../building-journeys/using-custom-actions.md)
* [Springen](../building-journeys/jump.md)

![ Activiteiten van de Actie palet in de reisontwerper ](assets/journey58.png)

Deze activiteiten staan voor de verschillende beschikbare communicatiekanalen. U kunt ze combineren om een scenario voor meerdere kanalen te maken.

U kunt ook specifieke acties instellen om berichten te verzenden:

* Als u berichten verzendt met een systeem van derden, kunt u een specifieke aangepaste handeling maken. [Meer informatie](../action/action.md)

* Raadpleeg de volgende secties als u werkt met Campagne en Journey Optimizer:

   * [[!DNL Journey Optimizer] en Campagne v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] en Campaign Standard](../action/acs-action.md)
   * [[!DNL Journey Optimizer] en Marketo Engage](../action/marketo-engage.md)

## Best practices {#best-practices}

### Een label toevoegen

Met de meeste activiteiten kunt u een **[!UICONTROL Label]** definiëren. Hiermee voegt u een achtervoegsel toe aan de naam die onder uw activiteit op het canvas wordt weergegeven. Dit is handig als u dezelfde activiteit meerdere keren gebruikt en u deze gemakkelijker wilt identificeren. Het maakt het zuiveren ook gemakkelijker in het geval van fouten en maakt rapporten gemakkelijker te lezen. U kunt ook een optionele **[!UICONTROL Description]** toevoegen.

![ Etiket en de gebieden van de Beschrijving in de eigenschappen van de reisactiviteit ](assets/journey-action-label.png)

>[!NOTE]
>
>Voor bepaalde activiteiten is de id ook zichtbaar in het deelvenster. Deze id kan worden gebruikt in rapportage als een stabielere sleutel dan het label, dat kan veranderen.

### Geavanceerde parameters beheren {#advanced-parameters}

De meeste activiteiten geven een aantal geavanceerde en/of technische parameters weer die u niet kunt wijzigen.

![ Geavanceerde parametergebieden in de eigenschappen van de reisactiviteit ](assets/journey-advanced-parameters.png)

Verberg deze parameters voor een betere leesbaarheid met de knop **[!UICONTROL Hide read-only fields]** boven in het rechterdeelvenster.

![ verberg read-only gebiedspictogram in de eigenschappen van de reisactiviteit ](assets/journey-hide-read-only-fields.png)

In bepaalde situaties kunt u de waarden van deze parameters voor specifiek gebruik overschrijven. Als u een waarde wilt afdwingen, klikt u op het pictogram **[!UICONTROL Enable parameter override]** rechts van het veld. [Meer informatie](../configuration/primary-email-addresses.md#journey-parameters)

![ laat parameteropheffing optie in de eigenschappen van de E-mailactiviteit toe ](assets/journey-enable-parameter-override.png)

>[!NOTE]
>
>Klik op de knop **[!UICONTROL Show read-only fields]** als de geavanceerde parameters verborgen zijn
>
>![ toon read-only gebiedenpictogram in de eigenschappen van de reisactiviteit ](assets/journey-show-read-only-fields.png){width=60%}

### Een alternatief pad toevoegen

Wanneer er een fout in een actie of een voorwaarde optreedt, eindigt de journey van een individu. De enige manier om door te gaan is het selectievakje **[!UICONTROL Add an alternative path in case of a timeout or an error]** in te schakelen. Zie [deze sectie](../building-journeys/using-the-journey-designer.md#paths).

![ voeg een alternatieve wegoptie in de eigenschappen van de voorwaardenactiviteit ](assets/journey42.png) toe

## Problemen oplossen {#troubleshooting}

Controleer voordat u uw journey gaat testen en publiceren of alle activiteiten correct zijn geconfigureerd. U kunt geen tests of publicaties uitvoeren als het systeem nog steeds fouten detecteert.

Leer hoe te om fouten in activiteiten en in de reis [ op deze pagina ](troubleshooting.md) problemen op te lossen.
