---
solution: Journey Optimizer
product: journey optimizer
title: Meerdere stappen starten en controleren met Adobe Journey Optimizer
description: Meer informatie over het starten en bewaken van multi-step campagnes met Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 70864a3e14a748562518c699513184e0f63c1139
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%

---

# Uw georkestreerde campagnes starten en controleren {#start-monitor}

<audio controls><source src="../ms/assets/do-not-localize/sound.mp3" type="audio/mpeg">Uw browser ondersteunt het audio-element niet.</audio>

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Georkestreerde campagne publiceren"
>abstract="Als u uw campagne wilt starten, moet u deze publiceren. Zorg ervoor dat alle waarschuwingen zijn gewist voordat u ze publiceert."


Nadat u de georkestreerde en ontworpen taken hebt gemaakt die u op het canvas wilt uitvoeren, kunt u deze publiceren en controleren hoe deze wordt uitgevoerd.

## Een campagne met meerdere stappen starten {#start}

Als u een campagne met meerdere stappen wilt starten, navigeert u naar het tabblad **[!UICONTROL Multi-step]** van het menu **[!UICONTROL Campaign]** en selecteert u de campagne die u wilt starten. Klik vervolgens op de knop **[!UICONTROL Start]** in de rechterbovenhoek van het canvas.

Zodra de campagne met meerdere stappen wordt uitgevoerd, wordt elke activiteit op het canvas in opeenvolgende volgorde uitgevoerd, tot het einde van de campagne met meerdere stappen is bereikt.

U kunt de voortgang van doelprofielen in real time volgen gebruikend een visuele stroom. Hierdoor kunt u snel de status van elke activiteit en het aantal profielen identificeren dat tussen de activiteiten overgaat.

![](assets/workflow-execution.png){zoomable="yes"}

## Meerdere fases in de campagne {#transitions}

In multi-step campagnes, worden de gegevens die van één activiteit aan een andere door overgangen worden vervoerd opgeslagen in een tijdelijke het werklijst. Deze gegevens kunnen voor elke overgang worden weergegeven. Selecteer hiertoe een overgang om de eigenschappen ervan in de rechterkant van het scherm te openen.

* Klik op **[!UICONTROL Preview schema]** om het schema van de werktabel weer te geven.
* Klik op **[!UICONTROL Preview results]** om de gegevens te visualiseren die in de geselecteerde overgang worden verzonden.

![](assets/transition.png){zoomable="yes"}

## Activiteitenuitvoering controleren {#activities}

De visuele indicatoren in de hoger-juiste hoek van elke activiteitendoos staan u toe om hun uitvoering te controleren:

| Visuele indicator | Beschrijving |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | De activiteit wordt momenteel uitgevoerd. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | De activiteit vereist uw aandacht. Dit kan inhouden dat de verzending van een levering wordt bevestigd of dat de nodige actie wordt ondernomen. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | Er is een fout opgetreden in de activiteit. Open de logboeken met meerdere stappen voor meer informatie om het probleem op te lossen. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | De activiteit is met succes uitgevoerd. |

## Logboeken en taken controleren {#logs-tasks}

Het controleren van werkstromen logboeken en taken is een zeer belangrijke stap om uw multi-step campagnes te analyseren en ervoor te zorgen zij behoorlijk lopen. Ze zijn toegankelijk via het pictogram **[!UICONTROL Logs]** dat beschikbaar is in de werkbalk Handeling en in het deelvenster Eigenschappen van elke activiteit.

Het menu **[!UICONTROL Logs and tasks]** bevat een geschiedenis van de uitvoering van de campagne in meerdere stappen, waarbij alle handelingen van de gebruiker worden opgenomen en fouten worden aangetroffen.
![](assets/workflow-logs.png){zoomable="yes"}

Er zijn twee soorten informatie beschikbaar:

* Het tabblad **[!UICONTROL Log]** bevat de uitvoeringsgeschiedenis van alle campagneactiviteiten die uit meerdere stappen bestaan. De uitgevoerde bewerkingen en uitvoeringsfouten worden chronologisch geïndexeerd.
* Het tabblad **[!UICONTROL Tasks]** bevat details over de uitvoeringsvolgorde van de activiteiten.

Op beide tabbladen kunt u de weergegeven kolommen en hun volgorde kiezen, filters toepassen en het zoekveld gebruiken om snel de gewenste informatie te zoeken.

## Opdrachten voor het uitvoeren van meerdere campagnes {#execution-commands}

De actiebalk in de rechterbovenhoek bevat opdrachten waarmee u de uitvoering van de campagne in meerdere stappen kunt beheren. U kunt:

* **[!UICONTROL Start]** / **[!UICONTROL Resume]** de uitvoering van de opdracht   meerstapse campagne, die vervolgens de status In progress krijgt. Als de meerfasencampagne is gepauzeerd, wordt deze hervat, anders wordt de campagne gestart en worden de initiële activiteiten vervolgens geactiveerd.

* **[!UICONTROL Pause]** de uitvoering van de campagne met meerdere stappen, die vervolgens de status Gepauzeerd krijgt. Er zullen geen nieuwe activiteiten worden geactiveerd totdat de activiteiten worden hervat, maar de lopende activiteiten worden niet opgeschort.

* **[!UICONTROL Stop]** een meerstapscampagne die wordt uitgevoerd en die vervolgens de status Voltooid krijgt. De lopende bewerkingen worden indien mogelijk onderbroken. U kunt de campagne met meerdere stappen niet hervatten vanaf dezelfde plaats als waar de campagne is gestopt.
