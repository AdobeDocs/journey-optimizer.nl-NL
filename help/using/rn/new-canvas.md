---
solution: Journey Optimizer
product: journey optimizer
title: Nieuwe interface voor reizen
feature: Release Notes
topic: Content Management
description: Nieuwe interface voor reizen
hide: true
hidefromtoc: true
exl-id: 03828fca-dde7-4b3b-b890-2c007d1245cc
source-git-commit: 17dc12f66a740b1ebea360aa20453d9b750d3e5c
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Welkom bij de verbeterde reisontwerper {#new-canvas}

>[!CONTEXTUALHELP]
>id="ajo_new_canvas"
>title="Nieuwe functies"
>abstract="Nieuw canvas"

Welkom bij de verbeterde reisontwerper!

We hebben een **vereenvoudigd reismodel** dat beoogt de interne processen te verbeteren . Hoewel dit nieuwe model een back-endverbetering is, heeft ons team de gelegenheid aangegrepen om functies toe te voegen die zichtbaar en gunstig zijn voor Journey Optimizer-gebruikers:

* A **herontworpen reiscanvas** gemaakt voor een gemoderniseerde gebruikersinterface-ervaring
* A **live rapportage** UI direct beschikbaar in het wegcanvas

>[!AVAILABILITY]
>
>Houd er rekening mee dat de rollout voor deze functie progressief zal zijn. De wijzigingen worden misschien niet meteen weergegeven.

## Updates van het reismodel

Het nieuwe reismodel zal naast het bestaande model leven, wat betekent dat er reizen zullen worden gemaakt met **twee verschillende modellen**:

* De oude, genaamd &quot;v1&quot;
* En de nieuwe, genaamd &quot;v2&quot;

Alle reizen in v1 blijven in v1. U kunt deze nog steeds bewerken, testen of publiceren. Elke nieuwe versie die van een v1 wordt gemaakt, blijft ook in v1. Er zijn **geen functionele wijzigingen** rond v1 - reizen.

Zoals u in het onderstaande schermafbeelding ziet, zijn de knooppunten ronde vormen. Dit is de oude interface voor reizen op het v1-model.

![](assets/new-canvas.png)

Wanneer u echter **een nieuwe reis maken** of **bestaande dupliceren**, het wordt een v2 - reis .  We zijn van plan om v1-reizen te blijven ondersteunen totdat een meerderheid van de klanten overstappen op v2-reizen.

Er is één beperking op het nieuwe reismodel: **kan geen activiteiten kopiëren en plakken van een v1-reis naar een v2-reis en omgekeerd**. Als u dit wilt doen, raden we u aan uw v1-reis te dupliceren om er een v2 van te maken en vervolgens uw activiteiten te kopiëren.

In de onderstaande schermafbeelding ziet u de opnieuw ontworpen gebruikersinterface voor het reiscanvas (alleen beschikbaar met het v2-model):

![](assets/new-canvas2.png)

**Elke nieuwe functie die aan de reisontwerper wordt toegevoegd (inclusief live rapportering), is alleen beschikbaar voor v2-reizen vanaf dit moment.**

## Verbeterd ontwerp van reiscanvas

Met het nieuwe reismodel introduceren we een nieuw en verbeterd model **interface reiscanvas**, die naadloos past binnen het Adobe Experience Cloud-systeem voor oplossingen en toepassingen, waardoor een intuïtieve en efficiënte gebruikerservaring mogelijk wordt. Elke reis in de v2 stapel zal op dat nieuwe ontwerp zijn.

![](assets/new-canvas3.gif)

De activiteiten zullen nu worden vertegenwoordigd door vierkante dozen met de volgende mogelijkheden:

* De eerste regel die het activiteitstype vertegenwoordigt en die vaak wordt overschreven door meer contextuele informatie (bijvoorbeeld: bij Lezen publiek bevat deze de naam van het geselecteerde publiek) of door een aangepast label als u er een definieert.
* De tweede regel vertegenwoordigt altijd het type activiteit.

![](assets/new-canvas4.png)

Deze nieuwe interface verbetert de leesbaarheid van het reiscanvas door **duidelijkere activiteitenetiketten en types**.

Het staat het productteam ook toe om meer informatie op het canvas met minder kliks toe te voegen. Een voorbeeld van &quot;meer informatie&quot; zou de opname van live rapportering in het reiscanvas zijn, waar u profielen kunt zien die uw activiteiten betreden en verlaten vanwege fouten.

![](assets/new-canvas5.png)


## Live rapportering op het canvas van de reis

Naast het verbeterde ontwerp van het reiscanvas introduceren we de mogelijkheid om te zien, **op elke activiteit**, het aantal profielen dat deze activiteit heeft ingevoerd en het nummer dat is afgesloten vanwege een fout:

<!--
**last 24 hours reporting metrics** (called "live reporting") directly in the journey canvas.

![](assets/new-canvas6.png)

With every live journey on the new model, you will be able to see two types of "last 24 hours" reporting information:

* On a **new insert**, you will see:
    * The number of profiles that have been exported for audience-triggered journeys. You will see the number of profiles available in the last export job alongside the time when that export has been made.
    * The number of profiles who exited the journey
    * The percentage of errors
    ![](assets/new-canvas7.png)

* **On each activity**, you will see the number of profiles who entered that activity and the number who exited because of an error:
-->

![](assets/new-canvas8.png)

De gebruikersinterface wordt automatisch elke minuut vernieuwd.

<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
