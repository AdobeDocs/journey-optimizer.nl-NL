---
solution: Journey Optimizer
product: journey optimizer
title: Gebruik de activiteit van de Wacht in multi-step campagnes
description: Leer hoe u de activiteit Wachten in multi-step campagnes gebruikt
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '168'
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

1. Voeg a **toe wacht** activiteit in uw multi-step campagne.

1. Specificeer de **Duur** van het wachten tussen de binnenkomende en uitgaande overgangen.

1. Selecteer de tijdeenheid op het **gebied van Punten**: seconden, notulen, uren, dagen.

## Voorbeeld{#wait-example}

Het volgende voorbeeld illustreert **wacht** activiteit in een typisch gebruiksgeval. U stuurt een e-mailuitnodiging voor een evenement. 24 uur nadat het is verzonden, wordt een SMS-verzending naar dezelfde populatie verzonden.

![](../assets/workflow-wait-example.png)
