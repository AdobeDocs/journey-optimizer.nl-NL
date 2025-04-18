---
solution: Journey Optimizer
product: journey optimizer
title: De publieksactiviteit Opslaan gebruiken
description: Leer hoe u de vorkactiviteit in een georkestreerde campagne kunt gebruiken
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 84e34d21-dca1-4203-8539-f2b20e461936
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

---

# Doelgroep opslaan {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Een publiek opslaan"
>abstract="Gebruik deze activiteit om een bestaand publiek bij te werken of een nieuw publiek van de bevolking te creëren die stroomopwaarts in de georkestreerde campagne wordt berekend. Het gecreeerde publiek wordt toegevoegd aan de lijst van publiek, en beschikbaar via het **Publiek** menu."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_saveaudience_outbound"
>title="Uitgaande overgang genereren"
>abstract="Gebruik deze optie als u een overgang na **wilt toevoegen sparen publiek** activiteit."

**sparen publiek** activiteit is a **richtend** activiteit. Met deze activiteit kunt u een bestaand publiek bijwerken of een nieuw publiek maken van de bevolking die in een georkestreerde campagne stroomopwaarts is berekend. Het gecreeerde publiek wordt toegevoegd aan de lijst van toepassingspubliek, en beschikbaar gemaakt via het **publiek** menu.

Deze activiteit wordt hoofdzakelijk gebruikt om populatiegroepen in de zelfde georkestreerde campagne te berekenen, door hen in herbruikbaar publiek om te zetten. Verbind het met andere het richten activiteiten zoals a **bouwt publiek** of a **combineer** activiteit.

## Vorm sparen publieksactiviteit{#save-audience-configuration}

Volg deze stappen om **te vormen sparen publiek** activiteit:

![](../assets/workflow-save-audience.png)

1. Voeg a **sparen publiek** activiteit aan uw georkestreerde campagne toe.

1. Op de **drop-down Wijze**, selecteer de actie die u zou willen uitvoeren:

   * **creeer of werk een bestaand publiek** bij: bepaal een **etiket van het Publiek**. Als het publiek reeds bestaat, zal het worden bijgewerkt, anders zal een nieuw publiek worden gecreeerd.

   * **werk een bestaand publiek** bij: kies het **Publiek** u wenst om onder de lijst van bestaand publiek bij te werken.

1. Selecteer de **wijze van de Update** die voor bestaand publiek zal van toepassing zijn:

   * **vervangt publieksinhoud met nieuwe gegevens**: al publieksinhoud wordt vervangen. De oude data gaan verloren. Alleen de gegevens van de binnenkomende overgang van de activiteit voor het opslaan van het publiek blijven behouden. Met deze optie wist u het publiekstype en de doeldimensie van het bijgewerkte publiek.

   * **Volledig publiek met nieuwe gegevens**: de oude publieksinhoud wordt gehouden en de gegevens van de inbound overgang van de sparen publieksactiviteit wordt toegevoegd aan het.

1. Controle **produceert een uitgaande overgang** optie als u wenst om een overgang na **toe te voegen sparen publiek** activiteit.

De inhoud van het bewaarde publiek is dan beschikbaar in de detailmening van het publiek, dat van het **Publiek** menu kan worden betreden. De kolommen beschikbaar van deze mening beantwoorden aan de kolommen van de binnenkomende overgang van de georkestreerde campagne **sparen publiek** activiteit.


## Voorbeeld{#save-audience-example}

In het volgende voorbeeld ziet u hoe u een eenvoudige publieksupdate maakt. Een planner wordt toegevoegd om de georkestreerde campagne eens per maand in werking te stellen. Met een query worden alle profielen hersteld die zijn geabonneerd op de verschillende beschikbare toepassingen. **sparen publiek** activiteit werkt het publiek bij door profielen te schrappen die van de dienst sinds de laatste georkestreerde campagneuitvoering hebben afgemeld en door de onlangs ingetekende profielen toe te voegen.
