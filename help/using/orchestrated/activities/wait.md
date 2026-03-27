---
solution: Journey Optimizer
product: journey optimizer
title: Gebruik de activiteit van de Wacht in Geordende campagnes
description: Leer hoe te om de activiteit van de Wacht in Geordende campagnes te gebruiken
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
version: Campaign Orchestration
source-git-commit: c783d638bd2a64298ff587067c29639636da0c54
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---


# Wachten {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Wachtactiviteit"
>abstract="**wacht** activiteit wordt gebruikt om de overgang van een activiteit aan een andere te vertragen."

De **[!UICONTROL Wait]** -activiteit is een **[!UICONTROL Flow control]** -component die wordt gebruikt om een vertraging tussen twee activiteiten in een geordende campagne in te voeren. Dit helpt ervoor te zorgen dat uw follow-upactiviteiten een beter tijdstip hebben en relevanter zijn voor de betrokkenheid van gebruikers.

U kunt bijvoorbeeld een paar dagen na het verzenden van een e-mailbericht wachten om te controleren of het bericht wordt geopend en vervolgens klikken voordat u een vervolgbericht verzendt.

## Configuratie{#wait-configuration}

>[!IMPORTANT]
>
>De gegevens in tijdelijke lijsten blijven niet voorbij **5 dagen**. Wanneer u **[!UICONTROL Duration]** of **[!UICONTROL Fixed time]** wacht, zorg ervoor de verstreken tijd tot de volgende activiteit binnen die grens voltooit zodat de middengegevens beschikbaar blijven.

Voer de volgende stappen uit om de **[!UICONTROL Wait]** -activiteit te configureren:

1. Voeg een **[!UICONTROL Wait]** activiteit in uw Geordende campagne toe.

1. Selecteer het type Wacht dat het beste bij uw behoeften past:

   * **[!UICONTROL Duration]**: geef een vertraging op in seconden, minuten, uren of dagen voordat u verdergaat met de volgende activiteit.

   * **[!UICONTROL Fixed time]**: stel een specifieke datum en tijd in waarna de volgende activiteit begint.

   ![](../assets/wait_activity.png)

## Voorbeeld{#wait-example}

Het volgende voorbeeld illustreert de **[!UICONTROL Wait]** activiteit in een typisch gebruikscase.  Er wordt een e-mail met een promotiecode verzonden naar profielen die hun verjaardagen vieren. Na twee dagen wordt een SMS verzonden naar dezelfde groep als een herinnering dat de aanbiedingscode van deze groep bijna verlopen is.

![](../assets/wait-example.png)
