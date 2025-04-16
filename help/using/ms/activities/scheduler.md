---
solution: Journey Optimizer
product: journey optimizer
title: De planningsactiviteit gebruiken
description: Leer hoe u de planneractiviteit in een georkestreerde campagne kunt gebruiken
hide: true
hidefromtoc: true
exl-id: da77a0bf-7b17-40fc-b2cb-2f0940152e64
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 6%

---

# Planner {#scheduler}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Planningsactiviteit"
>abstract="De **Planner** activiteit staat u toe om te plannen wanneer de georkestreerde campagne begonnen wordt. Deze activiteit moet worden beschouwd als een geplande start. Het kan alleen worden gebruikt als de eerste activiteit van de georkestreerde campagne."


De **planner** activiteit is de controle **activiteit van de a** Stroom. Zo kunt u plannen wanneer de georkestreerde campagne van start gaat. Deze activiteit moet worden beschouwd als een geplande start. Het kan alleen worden gebruikt als de eerste activiteit van de georkestreerde campagne.

## Best practices{#scheduler-best-practices}

* Plan geen georkestreerde campagne om meer dan om de 15 minuten in werking te stellen aangezien het algemene systeemprestaties kan belemmeren en tot blokken in het gegevensbestand kan leiden.
* Als u één-schot levering in uw georkestreerde campagne wilt verzenden, kunt u een planneractiviteit toevoegen en het plaatsen om **eens** in werking te stellen. U kunt het **Programma** in de montages van de levering ook bepalen.
* Als u een terugkomende levering in uw geordende campagne wilt verzenden, moet u a **Planner** activiteit gebruiken en de uitvoeringsfrequentie plaatsen. De terugkomende leveringsactiviteit staat u niet toe om een programma te bepalen.

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

1. Voeg a **Planner** activiteit aan uw geordende campagne toe.

1. Vorm de **frequentie van de Uitvoering**:

   * **Eenmaal**: De georkestreerde campagne wordt uitgevoerd één keer.

   * **Dagelijks**: De georkestreerde campagne wordt uitgevoerd op een specifiek tijdstip, eens per dag.

   * **verscheidene tijden per dag:** de georkestreerde campagne wordt regelmatig uitgevoerd verscheidene keren per dag. U kunt uitvoeringen instellen op specifieke tijdstippen of periodiek.

   * **Wekelijks**: de georkestreerde campagne wordt uitgevoerd op een gespecificeerd ogenblik, één of verscheidene tijden per week.

   * **Maandelijks**: De georkestreerde campagne wordt uitgevoerd op een gespecificeerd moment, eens of verscheidene tijden per maand. U kunt maanden selecteren wanneer u de georkestreerde campagne moet uitvoeren. U kunt uitvoeringen ook instellen op bepaalde weekdagen van de maand, zoals de tweede dinsdag van de maand.

1. Definieer de details van de uitvoering op basis van de geselecteerde frequentie. De detailvelden variëren, afhankelijk van de gebruikte frequentie (tijd, herhalingsfrequentie, opgegeven dagen, enz.).

1. Klik **de lanceringstijden van de Voorproef** om het programma van volgende tien uitvoeringen van uw georkestreerde campagne te controleren.

1. Bepaal de geldigheidsperiode van de planner:

   * **Vaste (verloopt nooit)**: de georkestreerde campagne wordt uitgevoerd, volgens de gespecificeerde frequentie, zonder enige grenzen aan het tijdkader of aantal herhalingen.

   * **Geldigheidsperiode**: de georkestreerde campagne wordt uitgevoerd volgens de gespecificeerde frequentie, tot een specifieke datum. U moet begin- en einddatums opgeven.

>[!NOTE]
>
>Als u de georkestreerde campagne direct wilt beginnen, kunt u **klikken in afwachting van taak uitvoeren** in de hoogste actiebar van de planner. Deze knop is alleen beschikbaar wanneer u de georkestreerde campagne hebt gestart.

## Voorbeeld{#scheduler-example}

In het volgende voorbeeld, wordt de activiteit gevormd zodat de georkestreerde campagne verscheidene keren per dag om 9 en 12 AM, elke dag van de week van 1 Oktober, 2025 aan 1 Januari, 2026 loopt.

![](../assets/workflow-scheduler2.png)
