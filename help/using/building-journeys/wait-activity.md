---
solution: Journey Optimizer
product: journey optimizer
title: Wachtactiviteit
description: Leer hoe te om de wachttijdactiviteit te vormen
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: wachten, activiteit, reis, volgende, canvas
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 18296fe54dcef6620d4f74374848199368f01475
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 6%

---

# Wachtactiviteit {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Wachtactiviteit"
>abstract="Als u wilt wachten voordat u de volgende activiteit in het pad uitvoert, kunt u een wachtbewerking gebruiken. Hiermee kunt u het moment bepalen waarop de volgende activiteit wordt uitgevoerd. Er zijn twee opties beschikbaar: duur en aangepast."

U kunt een **[!UICONTROL Wait]** -activiteit gebruiken om een duur te definiëren voordat u de volgende activiteit uitvoert.  Het maximum wacht duur is **90 dagen**.

U kunt twee types van **plaatsen wachten** activiteit:

* Een wachttijd op basis van een relatieve duur. [Meer informatie](#duration)
* Een aangepaste datum, die functies gebruikt om deze te berekenen. [Meer informatie](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Aanbevelingen {#wait-recommendations}

### Meerdere wachtactiviteiten {#multiple-wait-activities}

Wanneer het gebruiken van veelvoudige **wacht** activiteiten in een reis, me ervan bewust ben dat de [ globale onderbreking ](journey-properties.md#global_timeout) voor reizen 91 dagen is, betekenend dat de profielen altijd uit het reismaximum 91 dagen zijn nadat zij het inging. Meer informatie vindt u [op deze pagina](journey-properties.md#global_timeout).

Een individu kan a **ingaan wacht** activiteit slechts als zij genoeg tijd in het reis hebben om de wachttijdsduur vóór de onderbrekingen van het 91 dagreis te voltooien.

### Wacht en start opnieuw op {#wait-reentrance}

Een beste praktijk om **niet te gebruiken wacht** activiteiten om ingang te blokkeren. In plaats daarvan, gebruik **toestaan terugkeer** optie op het niveau van de vervoerseigenschappen. Meer informatie vindt u [op deze pagina](../building-journeys/journey-properties.md#entrance).

### Wachten en testmodus {#wait-test-modd}

Op testwijze, staat de **[!UICONTROL Wait time in test]** parameter u toe om de tijd te bepalen dat elk **** activiteit zal duren. De standaardtijd is 10 seconden. Zo krijgt u de testresultaten snel. Meer informatie vindt u [op deze pagina](../building-journeys/testing-the-journey.md).

## Configuratie {#wait-configuration}

### Wachten op duur {#duration}

Selecteer het **type van de Duur** om de relatieve duur van te plaatsen wacht vóór de uitvoering van de volgende activiteit. De maximumduur is **90 dagen**.

![ bepaal de wachttijd duur ](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### Aangepaste wachttijd {#custom}

Selecteer het **type van de Douane** om een douanedatum te bepalen, gebruikend een geavanceerde uitdrukking die op een gebied wordt gebaseerd dat uit een gebeurtenis of een reactie van de douaneactie komt. U kunt een relatieve duur niet rechtstreeks definiëren, bijvoorbeeld 7 dagen, maar u kunt desgewenst functies gebruiken om de duur te berekenen (bijv. 2 dagen na aankoop).

![ bepaal een douane wacht met een uitdrukking ](assets/journey57.png)

De expressie in de editor moet een `dateTimeOnly` -indeling hebben. Verwijs naar [ deze pagina ](expression/expressionadvanced.md). Voor meer informatie over dateTimeOnly formaat, verwijs naar [ deze pagina ](expression/data-types.md).

De beste manier is om aangepaste datums te gebruiken die specifiek zijn voor uw profielen en om te voorkomen dat voor iedereen dezelfde datum wordt gebruikt. Definieer bijvoorbeeld niet `toDateTimeOnly('2024-01-01T01:11:00Z')` , maar `toDateTimeOnly(@event{Event.productDeliveryDate})` die specifiek is voor elk profiel. Houd er rekening mee dat het gebruik van vaste datums problemen kan veroorzaken bij het uitvoeren van de reis.


>[!NOTE]
>
>U kunt een `dateTimeOnly` -expressie benutten of een functie gebruiken om om te zetten in een `dateTimeOnly` . Bijvoorbeeld: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, het gebied in de gebeurtenis die van vorm 2023-08-12T09 :46: 06Z is.
>
>De **tijdzone** wordt verwacht in de eigenschappen van uw reis. Dientengevolge, van het gebruikersinterface, is het niet mogelijk om bij volledig ISO-8601 timestamp het mengen van tijd en tijdzonecompensatie zoals 2023-08-12T09 :46: 06.982-05 direct te wijzen. [Meer informatie](../building-journeys/timezone-management.md).


U kunt stapgebeurtenissen gebruiken om te controleren of de wachtactiviteiten naar behoren werken. [Meer informatie](../reports/query-examples.md#common-queries).

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you'll be notified that the default time applies.

>[!NOTE]
>
>The first event of your journey must have a namespace.
>
>This capability is only available after an **[!UICONTROL Email]** activity. You need to have Adobe Campaign Standard.

1. In the **[!UICONTROL Amount of time]** field, define the number of hours to consider to optimize email sending.
1. In the **[!UICONTROL Optimization type]** field, choose if the optimization should increase clicks or opens.
1. In the **[!UICONTROL Default time]** field, define the default time to wait if the predictive send time score is not available.

    >[!NOTE]
    >
    >Note that the send time score can be unavailable because there is not enough data to perform the calculation. In this case, you will be informed, at publication time, that the default time applies.

![](assets/journey57bis.png)-->

## Automatisch wachtknooppunt  {#auto-wait-node}


>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="Over het automatische wachtknooppunt"
>abstract="A **wacht** activiteit wordt automatisch toegevoegd na deze activiteit. Deze wordt ingesteld voor 3 dagen. U kunt het verwijderen of het vormen zoals nodig."

Elke binnenkomende berichtactiviteit (In-app bericht, op code-gebaseerde ervaring, of Kaart) komt met een 3 dagen **wachten** activiteit. Aangezien de binnenkomende berichten automatisch beëindigen wanneer een profiel uit het eind van de reis bereikt, veronderstellen wij dat u uw gebruikers het ten minste 3 dagen wilt zien. U kunt dit **verwijderen wacht** activiteit, of verandert zijn configuratie indien nodig.