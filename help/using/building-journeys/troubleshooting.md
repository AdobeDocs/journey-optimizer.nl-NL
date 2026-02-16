---
solution: Journey Optimizer
product: journey optimizer
title: Los fouten op alvorens uw reis te testen of te publiceren
description: Leer hoe u fouten kunt oplossen voordat u uw reis test of publiceert
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: problemen oplossen, problemen oplossen, reis, controle, fouten
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
version: Journey Orchestration
source-git-commit: 0b003420fd0bf466f81f5377ef58f17695283259
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 38%

---

# Los fouten op alvorens uw reis te testen {#troubleshooting}

Leer in deze sectie hoe u problemen met reizen kunt oplossen voordat u gaat testen of publiceren. Alle hieronder vermelde controles kunnen worden uitgevoerd in de testmodus van de journey of wanneer de journey live is. De aanbeveling is om alle onderstaande controles in de testmodus uit te voeren en vervolgens tot publicatie over te gaan. Leer meer over de testwijze op [ deze pagina ](../building-journeys/testing-the-journey.md).

Leer hoe te om reisgebeurtenissen problemen op te lossen, controleer als de profielen uw reis ingegaan, hoe zij door het navigeren, en als de berichten [ op deze pagina ](troubleshooting-execution.md) worden verzonden. Als geen profielen uw op gebeurtenis-gebaseerde reis ondanks gebeurtenissen ingaan die worden opgenomen, verzeker de [ gegevenstypes van de gebeurtenisvoorwaarde het gebeurtenisschema ](troubleshooting-execution.md#verify-event-identity-and-rule-data-types) aanpassen.

Als u binnenkomende acties gebruikt, leer hoe te om hen [ op deze pagina ](troubleshooting-inbound.md) problemen op te lossen.

## Fouten in activiteiten {#activity-errors}

Controleer voordat u uw journey gaat testen en publiceren of alle activiteiten correct zijn geconfigureerd. U kunt geen tests of publicaties uitvoeren als het systeem nog steeds fouten detecteert.

Fouten worden weergegeven met een waarschuwingssymbool dat wordt weergegeven op de activiteiten zelf op het canvas. Plaats de cursor op het uitroepteken om het foutbericht weer te geven. Als u de activiteit selecteert, zou u de lijn in fout met een waarschuwing moeten zien. Bijvoorbeeld:

* als een verplicht veld leeg is, wordt een fout weergegeven

  ![ de bevestigingsfouten van de Reis die in canvas met foutenindicatoren worden getoond ](assets/journey63.png)

* op het canvas, wanneer twee activiteiten worden losgekoppeld, wordt een waarschuwing weergegeven

  ![ het pictogram van de Waarschuwing die losgemaakte activiteiten op het wegcanvas tonen ](assets/canvas-disconnected.png)

## Fouten in de reis {#canvas-errors}

Fouten zijn ook zichtbaar vanaf de knop **[!UICONTROL Alerts]** boven het canvas. Met deze knop kunt u fouten zien die door het systeem zijn gedetecteerd en die de activering van de testmodus of de publicatie van de reis verhinderen.

Het systeem ontdekt twee soorten kwesties: **fouten** en **waarschuwingen**. Fouten blokkeren publicatie en testactivering. Waarschuwingen geven mogelijke problemen aan die testactivering of publicatie niet blokkeren. U ziet een beschrijving van het probleem en een probleemlog-id van het type ERR_XXX_XXX. Dit kan helpen de kwestie identificeren.

![ Fout en waarschuwingsindicatoren in reis met beschrijvingshulpstukken ](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

Fouten en waarschuwingen die globaal zijn voor de journey, worden als eerste in de lijst weergegeven. Fouten en waarschuwingen met betrekking tot specifieke activiteiten worden daarna vermeld, op volgorde van activiteit of weergave in de journey van links naar rechts. Onder aan de lijst met waarschuwingen kunt u met de knop **[!UICONTROL Copy details]** technische informatie over de reis kopiëren. Deze informatie is handig voor het oplossen van problemen.

## Een alternatief pad toevoegen {#canvas-add-path}

U kunt een fallback-actie definiëren in het geval van een fout voor de volgende reisactiviteiten: **[!UICONTROL Optimize]** en **[!UICONTROL Action]** .

Wanneer er een fout in een actie of een voorwaarde optreedt, eindigt de journey van een individu. De enige manier om dit voort te zetten is het oplossen van de kwestie. U kunt voorkomen dat de rit wordt onderbroken door ook de optie **[!UICONTROL Add an alternative path in case of a timeout or an error]** in de eigenschappen van de activiteit in te schakelen. Lees meer in [deze sectie](../building-journeys/using-the-journey-designer.md#paths).
