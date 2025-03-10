---
solution: Journey Optimizer
product: journey optimizer
title: De planningsactiviteit gebruiken
description: Leer hoe u de Planneractiviteit in een meerfasencampagne kunt gebruiken
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 6%

---

# Planner {#scheduler}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Planningsactiviteit"
>abstract="De **Planner** activiteit staat u toe om te plannen wanneer de multi-step campagne begonnen wordt. Deze activiteit moet worden beschouwd als een geplande start. Het kan alleen worden gebruikt als de eerste activiteit van de meerfasencampagne."


De **planner** activiteit is de controle **activiteit van de a** Stroom. Zo kunt u plannen wanneer de campagne met meerdere stappen wordt gestart. Deze activiteit moet worden beschouwd als een geplande start. Het kan alleen worden gebruikt als de eerste activiteit van de meerfasencampagne.

## Best practices{#scheduler-best-practices}

* Plan geen campagne in meerdere stappen om meer dan om de 15 minuten uit te voeren, aangezien dit de algehele systeemprestaties kan belemmeren en blokken in de database kan maken.
* Als u één-schot levering in uw multi-step campagne wilt verzenden, kunt u een planneractiviteit toevoegen en het plaatsen om **eens** in werking te stellen. U kunt het **Programma** in de montages van de levering ook bepalen.
* Als u een terugkomende levering in uw multi-step campagne wilt verzenden, moet u a **Planner** activiteit gebruiken en de uitvoeringsfrequentie plaatsen. De terugkomende leveringsactiviteit staat u niet toe om een programma te bepalen.

## De planningsactiviteit configureren {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="Geldigheid van planner"
>abstract="U kunt een geldigheidsperiode voor de planner bepalen. Deze kan permanent zijn (standaard) of geldig zijn tot een bepaalde datum."


>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="Planningsopties"
>abstract="Bepaal de frequentie van de planner. Het kan op een specifiek moment, één keer of verscheidene keren per dag, week of maand worden uitgevoerd."

Volg deze stappen om de **Planner** activiteit te vormen:

![](../assets/workflow-scheduler.png)

1. Voeg a **Planner** activiteit aan uw multi-step campagne toe.

1. Vorm de **frequentie van de Uitvoering**:

   * **Eenmaal**: De multi-step campagne wordt uitgevoerd één keer.

   * **Dagelijks**: de multi-step campagne wordt uitgevoerd op een specifiek tijdstip, eens per dag.

   * **verscheidene tijden per dag:** de multi-step campagne wordt regelmatig uitgevoerd verscheidene keren per dag. U kunt uitvoeringen instellen op specifieke tijdstippen of periodiek.

   * **Wekelijks**: de multi-step campagne wordt uitgevoerd op een gespecificeerd moment, eens of verscheidene keren per week.

   * **Maandelijks**: de multi-step campagne wordt uitgevoerd op een gespecificeerd moment, eens of verscheidene tijden per maand. U kunt maanden selecteren, wanneer u de multi-step campagne moet uitvoeren. U kunt uitvoeringen ook instellen op bepaalde weekdagen van de maand, zoals de tweede dinsdag van de maand.

1. Definieer de details van de uitvoering op basis van de geselecteerde frequentie. De detailvelden variëren, afhankelijk van de gebruikte frequentie (tijd, herhalingsfrequentie, opgegeven dagen, enz.).

1. Klik **de lanceringstijden van de Voorproef** om het programma van volgende tien uitvoeringen van uw multi-step campagne te controleren.

1. Bepaal de geldigheidsperiode van de planner:

   * **Permanent (verloopt nooit)**: de multi-step campagne wordt uitgevoerd, volgens de gespecificeerde frequentie, zonder enige grenzen aan het tijdkader of aantal herhalingen.

   * **Geldigheidsperiode**: de multi-step campagne wordt uitgevoerd volgens de gespecificeerde frequentie, tot een specifieke datum. U moet begin- en einddatums opgeven.

>[!NOTE]
>
>Als u de multi-step campagne wilt onmiddellijk beginnen, kunt u **klikken in afwachting van taak** in de hoogste actiebar van de planner uitvoeren. Deze knop is alleen beschikbaar wanneer u de campagne voor meerdere stappen hebt gestart.

## Voorbeeld{#scheduler-example}

In het volgende voorbeeld, wordt de activiteit gevormd zodat de multi-step campagne verscheidene keren per dag om 9 en 12 AM, elke dag van de week van 1 Oktober, 2025 aan 1 Januari, 2026 loopt.

![](../assets/workflow-scheduler2.png)
