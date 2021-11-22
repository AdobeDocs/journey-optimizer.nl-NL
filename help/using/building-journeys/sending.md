---
title: Beginnen met uitvoering van de reis
description: Leer hoe u uw reis start en berichten verzendt
source-git-commit: 9e152f50c2360010d83ffccbe536380879ffb5da
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 2%

---


# Uitvoering van reizen {#message-execution}

## Uw reis testen

U kunt uw reis testen met testprofielen. Deze stap wordt aanbevolen om uw instellingen en berichten te valideren.

Meer informatie in deze [sectie](testing-the-journey.md).

## Uw reis activeren

U moet uw reis publiceren om het te activeren.

![](../assets/jo-journeyuc2_32bis.png)

Meer informatie in deze [sectie](publishing-the-journey.md).


Na publicatie kunt u uw reis controleren met behulp van de speciale rapportagetools om de effectiviteit van uw reis te meten.

![](../assets/jo-dynamic_report_journey_12.png)

[Meer informatie over rapporten](../reports/live-report.md)

## Berichten verzenden {#send-messages}

Wanneer voor uw bericht een inhoud is gedefinieerd en gepubliceerd, kan het bericht worden verzonden via een [reis](journey.md).

>[!NOTE]
>
>U kunt een bericht toevoegen dat nog in ontwerpwijze aan een reis is, maar zorg ervoor het bericht wordt gepubliceerd alvorens de reis te publiceren.

Zodra een bericht wordt verzonden, kunt u zijn uitvoering door veelvoudige indicatoren controleren. [Meer informatie over het controleren van berichtuitvoering](../message-monitoring.md).

## Abonnementen {#schedule-messages}

Berichten kunnen via de **[!UICONTROL Read Segment]** in een [reis](journey.md). U kunt specificeren wanneer het segment de reis zal ingaan. [Meer informatie over de activiteit Leessegment](read-segment.md).

Volg de onderstaande stappen om dit te doen:

1. Een reis bewerken, een pad slepen en neerzetten **[!UICONTROL Read Segment]** activiteit en begin het vormen. [Meer informatie over het configureren van de activiteit Leessegment](read-segment.md#configuring-segment-trigger-activity).

1. Klik op de knop **[!UICONTROL Edit journey schedule]** verbinding met de eigendommen van de reis.

   ![](../assets/message-read-segment-schedule.png)

1. Configureer de **[!UICONTROL Scheduler type]** veld: Selecteer de gewenste waarde in de lijst om ervoor te zorgen dat het segment de reis op een specifieke datum/tijd of op een terugkerende basis ingaat.

   >[!NOTE]
   >
   >De **[!UICONTROL Schedule]** -sectie alleen beschikbaar als een **[!UICONTROL Read Segment]** activiteit is neergezet op het canvas.

   ![](../assets/message-read-segment-scheduler.png)

1. Als u **[!UICONTROL Once]** een specifieke datum en tijd vast waarop het segment de reis zal betreden.

   ![](../assets/message-read-segment-scheduler-once.png)

1. Als u een terugkerende methode selecteert, bewerkt u de begindatum en -tijd. U kunt ook een optionele einddatum en -tijd definiëren.

   ![](../assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >De segmenten gaan standaard de reis in **[!UICONTROL As soon as possible]**, dat wil zeggen 1 uur na publicatie van de reis.

1. Klikken **[!UICONTROL OK]** om uw wijzigingen op te slaan.

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
