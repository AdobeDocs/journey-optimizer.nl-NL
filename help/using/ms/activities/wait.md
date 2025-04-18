---
solution: Journey Optimizer
product: journey optimizer
title: Gebruik de activiteit van de Wacht in georkestreerde campagnes
description: Leer hoe te om de activiteit van de Wacht in georkestreerde campagnes te gebruiken
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 26%

---

# Wachten {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Wachtactiviteit"
>abstract="**wacht** activiteit wordt gebruikt om de overgang van een activiteit aan een andere te vertragen."

**wacht** activiteit is de controle **activiteit van de a** Stroom. Het wordt gebruikt om een bepaalde hoeveelheid tijd toe te staan om tussen twee uit te voeren activiteiten over te gaan. Bijvoorbeeld als u een aantal dagen wilt wachten na een e-mailleveringsactiviteit om het aantal open- en klikacties tijdens die periode te analyseren voordat u follow-upbewerkingen gaat uitvoeren (herinneringsmail, doelgroep maken, enz.).

## Configuratie{#wait-configuration}

Volg deze stappen om **te vormen wachten** activiteit:

1. Voeg a **toe wacht** activiteit in uw georkestreerde campagne.

1. Specificeer de **Duur** van het wachten tussen de binnenkomende en uitgaande overgangen.

1. Selecteer de tijdeenheid op het **gebied van Punten**: seconden, notulen, uren, dagen.

## Voorbeeld{#wait-example}

Het volgende voorbeeld illustreert **wacht** activiteit in een typisch gebruiksgeval. U stuurt een e-mailuitnodiging voor een evenement. 24 uur nadat het is verzonden, wordt een SMS-verzending naar dezelfde populatie verzonden.

![](../assets/workflow-wait-example.png)
