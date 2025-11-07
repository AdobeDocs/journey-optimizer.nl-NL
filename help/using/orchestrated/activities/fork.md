---
solution: Journey Optimizer
product: journey optimizer
title: De vorkactiviteit gebruiken
description: Leer hoe u de vorkactiviteit in een geordende campagne kunt gebruiken
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '131'
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

De **[!UICONTROL Fork]** -activiteit is een **[!UICONTROL Flow control]** -component waarmee u meerdere uitgaande overgangen kunt maken, waardoor verschillende activiteiten parallel kunnen worden uitgevoerd.

## De vorkactiviteit configureren{#fork-configuration}

Voer de volgende stappen uit om de **[!UICONTROL Fork]** -activiteit te configureren:

![](../assets/workflow-fork.png)

1. Voeg een **[!UICONTROL Fork]** activiteit aan uw Geordende campagne toe.

1. Definieer een **[!UICONTROL Label]** .

1. Wijs een etiket aan elke uitgaande overgang toe. Standaard zijn er twee overgangen beschikbaar.

1. Als u een overgang wilt verwijderen, klikt u op het pictogram ![](../assets/do-not-localize/Smock_Delete_18_N.svg) .

1. Klik indien nodig op **[!UICONTROL Add transition]** om een extra uitgaande overgang toe te voegen.
