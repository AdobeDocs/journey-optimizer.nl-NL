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
source-git-commit: 6b9044117dcdd7554dea0c5f791a6dcfb0218010
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Welkom bij de verbeterde reisontwerper {#new-canvas}

Journey Optimizer biedt nu een **vereenvoudigd reismodel** die tot doel heeft de gebruikerservaring en de interne processen te verbeteren. Vanaf april kunt u profiteren van de volgende functies:

* A **herontworpen reiscanvas** gemaakt voor een gemoderniseerde gebruikersinterface-ervaring
* A **live rapportage** UI direct beschikbaar in het wegcanvas

>[!NOTE]
>
>Houd er rekening mee dat de rollout voor deze functie progressief zal zijn. De wijzigingen worden misschien niet meteen weergegeven.

## Updates van het reismodel

Het nieuwe reismodel zal naast het bestaande model leven, wat betekent dat er reizen zullen worden gemaakt met **twee verschillende modellen**:

* Het oudere model
* Het nieuwe model

Alle reizen in het oude model blijven erin. U kunt deze nog steeds bewerken, testen of publiceren. Elke nieuwe versie die is gemaakt op basis van een reis op het oude model, blijft erin staan. Er zijn **geen functionele wijzigingen** rond die reizen.

Zoals u in het hieronder schermschot ziet, zijn de knopen rond-vormig, die oude UI voor reizen op het erfenismodel is.

![](assets/new-canvas.png)

Wanneer u echter **een nieuwe reis maken** of **bestaande dupliceren**, zal het op het nieuwe model staan. De reizen op het erfenismodel zullen nog worden gesteund tot een meerderheid van klanten aan nieuwe worden overgezet.

Er is één beperking op het nieuwe reismodel: **kan geen activiteiten kopiëren en plakken van het oudere model naar het nieuwe model en vice versa**. Als u dit wilt doen, adviseren wij u om uw erfenisreis te dupliceren om het op het nieuwe model over te schakelen, en dan uw activiteiten te kopiëren.

In de onderstaande schermafbeelding ziet u de opnieuw ontworpen interface voor het reiscanvas (alleen beschikbaar bij het nieuwe model):

![](assets/new-canvas2.png)

**Elke nieuwe functie die aan de reisontwerper wordt toegevoegd (inclusief live rapportering), is alleen beschikbaar voor reizen op het nieuwe model vanaf dit moment.**

## Verbeterd ontwerp van reiscanvas

Met het nieuwe reismodel introduceren we een nieuwe en verbeterde **interface reiscanvas**, die naadloos past binnen het Adobe Experience Cloud-systeem voor oplossingen en toepassingen, waardoor een intuïtieve en efficiënte gebruikerservaring mogelijk wordt. Elke reis in het nieuwe model zal op dat nieuwe ontwerp zijn.

![](assets/new-canvas3.gif)

De activiteiten zullen nu worden vertegenwoordigd door vierkante dozen met de volgende mogelijkheden:

* De eerste regel die het activiteitstype vertegenwoordigt dat vaak wordt overschreven door meer contextuele informatie (bij Lezen publiek bevat deze de naam van het geselecteerde publiek) of door een aangepast label als u er een definieert.
* De tweede regel vertegenwoordigt altijd het type activiteit.

![](assets/new-canvas4.png)

Deze nieuwe interface verbetert de leesbaarheid van het reiscanvas door **duidelijkere activiteitenetiketten en types**.

Het staat het productteam ook toe om meer informatie op het canvas met minder kliks toe te voegen. Een voorbeeld van &quot;meer informatie&quot; zou de opname van live rapportering in het reiscanvas zijn, waar u profielen kunt zien die uw activiteiten betreden en verlaten vanwege fouten.

![](assets/new-canvas5.png)

## Live rapportering op het canvas van de reis

Naast de verbeterde lay-out van het reiscanvas, wordt een nieuwe eigenschap geïntroduceerd om gebruikers toe te staan om rapportmetriek in real time van te bekijken **de laatste 24 uur**, ook wel live rapportering genoemd, direct binnen het reiscanvas.

Voor elke activiteit binnen elke levende reis die het nieuwe model gebruikt, hebt u toegang tot:


* Het aantal profielen dat deze activiteit betreedt.
* Het aantal profielen dat deze activiteit verlaat vanwege een fout.

![](assets/new-canvas6bis.png)

<!--`
With every live journey on the new model, you will be able to see two types of "last 24 hours" reporting information:

* On a **new insert**, you will see:
    * The number of profiles that have been exported for audience-triggered journeys. You will see the number of profiles available in the last export job alongside the time when that export has been made.
    * The number of profiles who exited the journey
    * The percentage of errors
    ![](assets/new-canvas7.png)
* **On each activity**, you will see the number of profiles who entered that activity and the number who exited because of an error:
    ![](assets/new-canvas8.png)
-->
<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
