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
version: Journey Orchestration
source-git-commit: 5eddbb1f9ab53f1666ccd8518785677018e10f6f
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 3%

---

# Wachtactiviteit {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Wachtactiviteit"
>abstract="Als u wilt wachten alvorens de volgende activiteit in de weg uit te voeren, kunt u een Wacht activiteit gebruiken. Hiermee kunt u bepalen wanneer de volgende activiteit wordt uitgevoerd. Er zijn twee opties beschikbaar: duur en aangepast."

U kunt een **[!UICONTROL Wait]** -activiteit gebruiken om een duur te definiëren voordat u de volgende activiteit uitvoert.  Het maximum wacht duur is **90 dagen**.

U kunt twee types van **plaatsen wacht** activiteit:

* Een wachttijd op basis van een relatieve duur. [Meer informatie](#duration)
* Een aangepaste datum, die functies gebruikt om deze te berekenen. [Meer informatie](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Aanbevelingen {#wait-recommendations}

### Meerdere wachtactiviteiten {#multiple-wait-activities}

Wanneer het gebruiken van veelvoudige **wacht** activiteiten in een reis, me ervan bewust ben dat de [ globale onderbreking ](journey-properties.md#global_timeout) voor reizen 91 dagen is, betekenend dat de profielen altijd uit het reismaximum 91 dagen zijn nadat zij het inging. Leer meer op [ deze pagina ](journey-properties.md#global_timeout).

Een individu kan a **ingaan wacht** activiteit slechts als zij genoeg tijd in de reis verlaten hebben om de wachttijdduur vóór de 91 dagen reisonderbreking te voltooien.

### Wacht en ingang {#wait-reentrance}

Een beste praktijk om **niet te gebruiken wacht** activiteiten om ingang te blokkeren. In plaats daarvan, gebruik **terugkeer** optie op het niveau van de reiseigenschappen toestaan. Leer meer op [ deze pagina ](../building-journeys/journey-properties.md#entrance).

### Wachten en testmodus {#wait-test-mode}

Op testwijze, staat de **[!UICONTROL Wait time in test]** parameter u toe om de tijd te bepalen dat elk **** activiteit zal duren. De standaardtijd is 10 seconden. Zo krijgt u de testresultaten snel. Leer meer op [ deze pagina ](../building-journeys/testing-the-journey.md).

### Wachten en mobiele kanalen {#wait-mobile-channels}

Als u een [ in-app bericht ](../in-app/create-in-app.md) kort na het verzenden van a [ duw bericht ](../../rp_landing_pages/push-landing-page.md) wilt tonen, gebruik a **wacht** activiteit om de in-app tijd van de berichtlading toe te staan om zich te verspreiden. Meestal wordt een wachttijd van 5 tot 15 minuten aanbevolen, maar de exacte wachttijden kunnen variëren afhankelijk van de complexiteit van de lading en de behoeften aan personalisatie.

## Configuratie {#wait-configuration}

### Wachten op duur {#duration}

Selecteer het **type van de Duur** om de relatieve duur van te plaatsen wacht vóór de uitvoering van de volgende activiteit. De maximumduur is **90 dagen**.

![ bepaalt de wachttijdduur ](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### Aangepast wachten {#custom}

Selecteer het **type van de Douane** om een douanedatum te bepalen, gebruikend een geavanceerde uitdrukking die op een gebied wordt gebaseerd dat uit een gebeurtenis of een reactie van de douaneactie komt. U kunt een relatieve duur niet rechtstreeks definiëren, bijvoorbeeld 7 dagen, maar u kunt functies gebruiken om de duur te berekenen als dat nodig is (bijvoorbeeld 2 dagen na aankoop).

![ bepalen een douane wacht met een uitdrukking ](assets/journey57.png)

De expressie in de editor moet een `dateTimeOnly` -indeling hebben. Verwijs naar [ deze pagina ](expression/expressionadvanced.md). Voor meer informatie over dateTimeOnly formaat, verwijs naar [ deze pagina ](expression/data-types.md).

De beste manier is om aangepaste datums te gebruiken die specifiek zijn voor uw profielen en om te voorkomen dat voor iedereen dezelfde datum wordt gebruikt. Definieer bijvoorbeeld niet `toDateTimeOnly('2024-01-01T01:11:00Z')` , maar `toDateTimeOnly(@event{Event.productDeliveryDate})` die specifiek is voor elk profiel. Houd er rekening mee dat het gebruik van vaste datums problemen kan veroorzaken bij het uitvoeren van de reis. Leer meer over het effect van de activiteiten van de Wacht op tarief van de reisverwerking in [ deze sectie ](entry-management.md#wait-activities-impact).


>[!NOTE]
>
>U kunt een `dateTimeOnly` -expressie benutten of een functie gebruiken om om te zetten in een `dateTimeOnly` . Bijvoorbeeld: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, het gebied in de gebeurtenis die van vorm 2023-08-12T09 :46: 06Z is.
>
>De **tijdzone** wordt verwacht in de eigenschappen van uw reis. Dientengevolge, van het gebruikersinterface, is het niet mogelijk om bij volledig te richten timestamp mengen tijd en tijdzone van ISO-8601 die als 2023-08-12T09 :46: 06.982-05 wordt verschoven. [Meer informatie](../building-journeys/timezone-management.md).


Om te bevestigen dat de wachttijdactiviteit zoals verwacht werkt, kunt u step gebeurtenissen gebruiken. [Meer informatie](../reports/query-examples.md#common-queries).

## Automatisch wachtknooppunt  {#auto-wait-node}


>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="Over het automatische wachtknooppunt"
>abstract="A **wacht** activiteit wordt automatisch toegevoegd na deze activiteit. Deze wordt ingesteld voor 3 dagen. U kunt het verwijderen of het vormen zoals nodig."

Elke binnenkomende ervaringsactiviteit (In-app bericht, op code-gebaseerde ervaring, of Kaart) komt met een 3 dagen **wachten** activiteit. Aangezien de binnenkomende berichten automatisch beëindigen wanneer een profiel uit het eind van de reis bereikt, veronderstellen wij dat u uw gebruikers het ten minste 3 dagen wilt zien. U kunt dit **verwijderen wacht** activiteit, of verandert zijn configuratie indien nodig.