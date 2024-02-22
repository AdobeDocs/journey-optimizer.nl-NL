---
solution: Journey Optimizer
product: journey optimizer
title: Tijdzonebeheer
description: Meer informatie over tijdzonebeheer
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: tijdzone, eigendommen, transport, conditie, tijd, datum, aangepast
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 2%

---

# Tijdzonebeheer {#timezone_management}

U kunt een tijdzone definiëren in het dialoogvenster [eigenschappen](../building-journeys/journey-gs.md#change-properties) van je reis.

Klik op het potloodpictogram rechtsboven in het scherm om de eigenschappen van Reis te openen.

Deze tijdzone wordt gebruikt voor elke activiteit van de reis die een tijdselement bevat, zoals:

* [Tijdconditie](../building-journeys/condition-activity.md#time_condition)
* [Datumvoorwaarde](../building-journeys/condition-activity.md#date_condition)
* [Aangepast wachten](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

U kunt een [vaste tijdzone](#fixed-timezone) of kies een tijdzone [gedefinieerd in het gebruikersprofiel](#timezone-from-profiles).

## Een vaste tijdzone definiëren {#fixed-timezone}

De tijdzone kan ook worden vastgesteld. Wis de vooraf gedefinieerde tijdzone en kies een tijdzone in de vervolgkeuzelijst. Als je een vaste tijdzone gebruikt, zal dat hetzelfde zijn voor iedereen die de reis binnenkomt.

Daartoe, in **[!UICONTROL Journey Properties]** selecteert u een tijdzone.

![](assets/journey72.png)

## Profielen gebruiken om de tijdzone van het transport te definiëren {#timezone-from-profiles}

Als de entry-gebeurtenis van de reis een naamruimte heeft, wat betekent dat de reis de Real-time service van het Profiel van de Klant van Adobe Experience Platform kan bereiken, kunt u de tijdzone willen gebruiken die op het profielniveau wordt bepaald. Daartoe, in **Eigenschappen**, controle **Tijdzone profiel gebruiken in wachtwoorden en omstandigheden**. Deze optie is niet standaard ingeschakeld.

Als een tijdzone voor een profiel is gedefinieerd, zal het door de reis worden teruggewonnen en gebruikt. Als dit niet het geval is, wordt de tijdzone gebruikt die is gedefinieerd in het tijdzone-veld.

![](assets/journey73.png)

>[!NOTE]
>
>De tijdzone van het profiel werkt met **timeZone** in het **Voorkeursdetails** veldgroep.

## Tijdzones gebruiken in expressies {#timezone-in-expressions}

De begin- en einddatum van een reis kunnen niet worden gekoppeld aan een specifieke tijdzone. Ze worden automatisch gekoppeld aan de tijdzone van de instantie.
