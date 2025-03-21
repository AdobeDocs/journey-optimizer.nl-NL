---
solution: Journey Optimizer
product: journey optimizer
title: De vorkactiviteit gebruiken
description: Leer hoe u de vorkactiviteit kunt gebruiken in een multi-step campagne
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# Vertakking {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="Vorkactiviteit"
>abstract="De **activiteit 0} van het Vonk {staat u toe om uitgaande overgangen tot stand te brengen om verscheidene activiteiten tezelfdertijd te beginnen.**"


>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="Overgangen naar vorkactiviteit"
>abstract="Door gebrek, worden twee overgangen gecreeerd met de activiteit van het a **Fork**. Klik **toevoegen overgangsknoop** om een extra uitgaande overgang te bepalen, en zijn etiket in te gaan."

De **activiteit 0} van het Fork {is de controle** activiteit van de a **Stroom.** Het staat u toe om uitgaande overgangen tot stand te brengen om verscheidene activiteiten tezelfdertijd te beginnen.

## De vorkactiviteit configureren{#fork-configuration}

Volg deze stappen om de **1} activiteit van het Fork {te vormen:**

![](../assets/workflow-fork.png)

1. Voeg de activiteit van het a **Vork** aan uw multi-step campagne toe.
1. Klik **toevoegen overgang** om een nieuwe uitgaande overgang toe te voegen. Standaard zijn twee overgangen gedefinieerd.
1. Voeg een label toe aan elk van uw overgangen.

## Voorbeeld{#fork-example}

In het volgende voorbeeld, gebruiken wij twee **Fork** activiteiten:

* Eén voor de twee query&#39;s, om deze tegelijk uit te voeren.
* Eén na de doorsnede om een e-mail en een sms tegelijk naar de doelgroep te sturen.

![](../assets/workflow-fork-example.png)
