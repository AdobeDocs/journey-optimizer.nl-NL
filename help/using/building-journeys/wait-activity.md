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
source-git-commit: cae6d394ad1c2356e55bd5f1cb4ad7494c9623dd
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 7%

---

# Wachtactiviteit {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Wachtactiviteit"
>abstract="Als u wilt wachten alvorens de volgende activiteit in de weg uit te voeren, kunt u een Wacht activiteit gebruiken. Hiermee kunt u bepalen wanneer de volgende activiteit wordt uitgevoerd. Er zijn twee opties beschikbaar: duur en aangepast."

U kunt een **[!UICONTROL Wait]** activiteit om een duur te bepalen alvorens de volgende activiteit uit te voeren.  De maximale wachttijd is **90 dagen**.

U kunt twee typen instellen **Wachten** activiteit:

* Een wachttijd op basis van een relatieve duur. [Meer informatie](#duration)
* Een aangepaste datum, die functies gebruikt om deze te berekenen. [Meer informatie](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Aanbevelingen {#wait-recommendations}

### Meerdere wachtactiviteiten {#multiple-wait-activities}

Bij het gebruik van meerdere **Wachten** tijdens een reis, dient u zich ervan bewust te zijn dat de [algemene time-out](journey-properties.md#global_timeout) voor reizen is dit 91 dagen , wat betekent dat profielen altijd buiten de reis vallen , en wel ten hoogste 91 dagen nadat zij de reis hebben betreden . Meer informatie vindt u [op deze pagina](journey-properties.md#global_timeout).

Een individu kan een **Wachten** alleen als zij voldoende tijd hebben om de wachttijd voor de reistijd van 91 dagen af te ronden.

### Wachten en opnieuw betreden {#wait-re-entrance}

Een beste werkwijze om niet te gebruiken **Wachten** activiteiten om hertoetreding te blokkeren. Gebruik in plaats daarvan de opdracht **Hernieuwde toegang toestaan** optie op het niveau van de reiseigenschappen. Meer informatie vindt u [op deze pagina](../building-journeys/journey-properties.md#entrance).

### Wachten en testmodus {#wait-test-modd}

In de testmodus **[!UICONTROL Wait time in test]** parameter staat u toe om de tijd te bepalen die elk **Wachten** de activiteit zal duren. De standaardtijd is 10 seconden. Zo krijgt u de testresultaten snel. Meer informatie vindt u [op deze pagina](../building-journeys/testing-the-journey.md).

## Configuratie {#wait-configuration}

### Wachten op duur {#duration}

Selecteer de **Duur** type om de relatieve duur van de wachttijd vóór de uitvoering van de volgende activiteit in te stellen. De maximale duur is **90 dagen**.

![De wachttijd definiëren](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### Aangepast wachten {#custom}

Selecteer de **Aangepast** type om een douanedatum te bepalen, gebruikend een geavanceerde uitdrukking die op een gebied wordt gebaseerd dat van een gebeurtenis of een reactie van de douaneactie komt. U kunt een relatieve duur niet rechtstreeks definiëren, bijvoorbeeld 7 dagen, maar u kunt functies gebruiken om de duur te berekenen als dat nodig is (bijvoorbeeld 2 dagen na aankoop).

![Een aangepaste wachttijd definiëren met een expressie](assets/journey57.png)

De expressie in de editor moet een `dateTimeOnly` gebruiken. Zie [deze pagina](expression/expressionadvanced.md). Voor meer informatie over de DateTimeOnly-notatie raadpleegt u [deze pagina](expression/data-types.md).

De beste manier is om aangepaste datums te gebruiken die specifiek zijn voor uw profielen en om te voorkomen dat voor iedereen dezelfde datum wordt gebruikt. Definieer bijvoorbeeld niet `toDateTimeOnly('2024-01-01T01:11:00Z')` maar eerder `toDateTimeOnly(@event{Event.productDeliveryDate})` die specifiek is voor elk profiel. Houd er rekening mee dat het gebruik van vaste datums problemen kan veroorzaken bij het uitvoeren van de reis.


>[!NOTE]
>
>U kunt een `dateTimeOnly` expressie of gebruik een functie om te zetten in een `dateTimeOnly`. Bijvoorbeeld: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, waarbij het veld in het geval de vorm 2023-08-12T09 heeft:46:06Z.
>
>De **tijdzone** wordt verwacht in de eigenschappen van uw reis. Als gevolg hiervan is het vanuit de gebruikersinterface niet mogelijk om rechtstreeks te wijzen naar een volledige ISO-8601 tijdstempelmixtijd en tijdzoneverschuiving zoals 2023-08-12T09:46:06.982-05. [Meer informatie](../building-journeys/timezone-management.md).


Om te bevestigen dat de wachttijdactiviteit zoals verwacht werkt, kunt u step gebeurtenissen gebruiken. [Meer informatie](../reports/query-examples.md#common-queries).

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
