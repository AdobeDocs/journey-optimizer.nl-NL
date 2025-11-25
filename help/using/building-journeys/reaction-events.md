---
solution: Journey Optimizer
product: journey optimizer
title: Gebeurtenissen van Reacties
description: Leer hoe te om reactiegebeurtenissen te gebruiken om aan bericht het volgen gegevens zoals opent en klikt binnen uw reizen, te antwoorden en onderbrekingspaden voor non-responders te vormen.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: reis, gebeurtenissen, reactie, volgen, platform
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
source-git-commit: dff732d14dd143f085b1287274f7571a900a0c87
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 2%

---

# Reactiegebeurtenissen {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Reactiegebeurtenissen"
>abstract="Met deze activiteit kunt u reageren op volggegevens die betrekking hebben op een bericht dat binnen dezelfde reis wordt verzonden. We leggen deze informatie in real time vast op het moment dat ze met Adobe Experience Platform wordt gedeeld."

## Overzicht {#overview}

De ingebouwde **[!UICONTROL Reactions]** -gebeurtenis is een van de verschillende gebeurtenisactiviteiten die beschikbaar zijn in het palet. Met deze activiteit kunt u reageren op volggegevens die betrekking hebben op een bericht dat binnen dezelfde reis wordt verzonden. We leggen deze informatie in real time vast op het moment dat ze met Adobe Experience Platform wordt gedeeld.

U kunt reageren op geklikte of geopende berichten.

Zie [ activiteiten van de Actie ](../building-journeys/about-journey-activities.md#action-activities).

U kunt de **[!UICONTROL Reaction]** -activiteit gebruiken om een actie uit te voeren wanneer er geen reactie is op uw berichten. Hiertoe maakt u een tweede pad parallel aan de **[!UICONTROL Reaction]** -activiteit en voegt u een **[!UICONTROL Wait]** -activiteit toe. Als er geen reactie optreedt tijdens de periode die is gedefinieerd in de **[!UICONTROL Wait]** -activiteit, wordt het tweede pad gekozen. U kunt bijvoorbeeld een vervolgbericht verzenden.

## Hoe te om reactiegebeurtenissen te vormen {#configure}

![ de gebeurtenisconfiguratie van de Reactie met kanaalselectie en gebeurtenistypeopties ](assets/journey45.png)

Voer de volgende stappen uit om de reactiegebeurtenissen te configureren:

1. Plaats a **[!UICONTROL Reaction]** activiteit **onmiddellijk** na de activiteit van de a [ kanaalactie ](journeys-message.md) op het wegcanvas.
1. Voeg een **[!UICONTROL Label]** toe aan de reactie. Deze stap is optioneel.
1. Selecteer in de vervolgkeuzelijst de activiteit waarop u wilt reageren. U kunt alle handelingen selecteren die zich in de vorige stappen van het pad bevinden.
1. Afhankelijk van de actie die u hebt geselecteerd, kiest u waarop u wilt reageren.
1. U kunt een time-out voor de gebeurtenis (tussen 40 seconden en 90 dagen) en een time-outpad definiëren. Hierdoor ontstaat een tweede pad voor personen die niet binnen de gedefinieerde tijdsduur hebben gereageerd. Bij het testen van een reis die een reactiegebeurtenis gebruikt, zijn de standaard- en minimumwaarde van de testmodus **[!UICONTROL Wait time]** 40 seconden. Zie [deze sectie](../building-journeys/testing-the-journey.md).

## Afvoerkanalen en beperkingen {#guardrails-limitations}

* A **[!UICONTROL Reaction]** activiteit moet **onmiddellijk** na de activiteit van de a [ kanaalactie ](journeys-message.md) in het wegcanvas worden geplaatst.
* U kunt een **[!UICONTROL Reaction]** -activiteit niet gebruiken als er nog geen kanaalactieactiviteit is.
* Het plaatsen van een **[!UICONTROL Wait]** -activiteit of enige andere activiteit tussen de kanaalactie en de **[!UICONTROL Reaction]** -activiteit wordt niet ondersteund en kan ertoe leiden dat de reactie niet naar behoren werkt.
* Reactiegebeurtenissen kunnen alleen berichten bijhouden die binnen dezelfde reis worden verzonden. Ze kunnen geen berichten volgen die op een andere reis plaatsvinden.
* In de gebeurtenissentrack van Reaction wordt geklikt op koppelingen van het type &quot;bijgehouden&quot;. Er wordt geen rekening gehouden met abonnements- en spiegelpaginakoppelingen.
* E-mail wordt geopend wordt bijgehouden met een afbeelding van 0 pixels die in de e-mail is opgenomen. Als e-mailclients (zoals Gmail) afbeeldingen blokkeren, wordt er geen rekening gehouden met het openen van e-mailberichten.
