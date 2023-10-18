---
solution: Journey Optimizer
product: journey optimizer
title: Wachtactiviteit
description: Meer informatie over wachtactiviteiten
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: wachten, activiteit, reis, volgende, canvas
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 5%

---

# Wachtactiviteit{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Wachtactiviteit"
>abstract="Als u wilt wachten alvorens de volgende activiteit in de weg uit te voeren, kunt u een Wacht activiteit gebruiken. Hiermee kunt u bepalen wanneer de volgende activiteit wordt uitgevoerd. Er zijn twee opties beschikbaar: duur en aangepast."

Als u wilt wachten voordat u de volgende activiteit in het pad uitvoert, kunt u een **[!UICONTROL Wait]** activiteit. Hiermee kunt u bepalen wanneer de volgende activiteit wordt uitgevoerd. De volgende opties zijn beschikbaar:

* [Duur](#duration)
* [Aangepast](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Informatie over de activiteit Wachten{#about_wait}

De maximale wachttijd is 30 dagen. In de testmodus **[!UICONTROL Wait time in test]** parameter staat u toe om de tijd te bepalen dat elke wachttijdactiviteit zal duren. De standaardtijd is 10 seconden. Zo krijgt u de testresultaten snel. Zie [deze pagina](../building-journeys/testing-the-journey.md).

Wees voorzichtig als u meerdere wachtactiviteiten gebruikt op een reis terwijl de wereldwijde time-out van de reis 30 dagen bedraagt, wat betekent dat een profiel altijd maximaal 30 dagen na het vertrek zal verdwijnen. Zie [deze pagina](../building-journeys/journey-gs.md#global_timeout).

Een individu kan alleen een wachtdienst doen als hij of zij genoeg tijd in de reis heeft om de wachttijd voor de 30 dagen reisonderbreking te voltooien. Als u bijvoorbeeld twee wachtactiviteiten toevoegt die elk op 20 dagen zijn ingesteld, detecteert het systeem dat de tweede wachttijd na de time-out van 30 dagen eindigt. De tweede wachttijd zal daarom genegeerd worden en de persoon zal de reis verlaten alvorens het te beginnen. In dat voorbeeld zal de klant in totaal 20 dagen op de reis blijven.

Het is aan te raden om geen wachttijden te gebruiken om hertoetreding te blokkeren. Gebruik in plaats daarvan de opdracht **Hernieuwde toegang toestaan** optie op het niveau van de reiseigenschappen. Zie [deze pagina](../building-journeys/journey-gs.md#entrance).

## Wachten op duur{#duration}

Selecteer de duur van de wachttijd voordat de volgende activiteit wordt uitgevoerd.

![](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

## Aangepast wachten{#custom}

Met deze optie kunt u een aangepaste datum definiëren, bijvoorbeeld 12 juli 2020 om 17.00 uur, met een geavanceerde expressie die is gebaseerd op een veld dat afkomstig is van een gebeurtenis of gegevensbron. U kunt hiermee geen aangepaste duur definiëren, bijvoorbeeld 7 dagen. De expressie in de expressie-editor moet een dateTimeOnly-indeling hebben. Zie dit [page](expression/expressionadvanced.md). Voor meer informatie over de dateTimeOnly-indeling raadpleegt u deze [page](expression/data-types.md).

>[!NOTE]
>
>U kunt een dateTimeOnly-expressie gebruiken of een functie gebruiken om om te zetten in een dateTimeOnly. Bijvoorbeeld: toDateTimeOnly(@{Event.biedOpened.activity.endTime}), waarbij het veld in de gebeurtenis van de vorm 2016-08-12T09 is:46:06Z.
>
>De **tijdzone** wordt verwacht in de eigenschappen van uw reis. Dientengevolge, is het vandaag van de interface niet mogelijk om bij volledig ISO-8601 timestamp het mengen tijd en de tijdzonecompensatie zoals 2016-08-12T09 direct te richten:46:06.982-05. Zie [deze pagina](../building-journeys/timezone-management.md).

![](assets/journey57.png)

Om te bevestigen dat de wachttijdactiviteit zoals verwacht werkt, kunt u step gebeurtenissen gebruiken. Zie [deze pagina](../reports/query-examples.md#common-queries).

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you’ll be notified that the default time applies.

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
