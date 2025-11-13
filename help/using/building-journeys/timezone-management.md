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
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# Tijdzonebeheer {#timezone_management}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="Tijdzone"
>abstract="Selecteer de tijdzone van de reis. Wanneer een vaste tijdzone wordt gebruikt, is dit hetzelfde voor alle personen die de reis betreden."


U kunt een tijdzone in de [ eigenschappen ](../building-journeys/journey-properties.md#timezone) van uw reis bepalen.

Als u de eigenschappen van een rit wilt openen, selecteert u het potloodpictogram rechtsboven in het scherm.

Deze tijdzone wordt gebruikt voor elke activiteit van de reis die een tijdselement bevat, zoals:

* [Tijdconditie](../building-journeys/condition-activity.md#time_condition)
* [Datumvoorwaarde](../building-journeys/condition-activity.md#date_condition)
* [Aangepast wachten](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

U kunt a [ vaste tijdzone ](#fixed-timezone) selecteren of verkiezen om de tijdzone [ te gebruiken die in het gebruikersprofiel ](#timezone-from-profiles) wordt bepaald.

## Een vaste tijdzone definiëren {#fixed-timezone}

De tijdzone kan worden vastgesteld. Wis de vooraf gedefinieerde tijdzone en kies een tijdzone in de vervolgkeuzelijst. Als je een vaste tijdzone gebruikt, zal dat hetzelfde zijn voor iedereen die de reis binnenkomt.

Selecteer hiertoe in het deelvenster **[!UICONTROL Journey Properties]** een tijdzone.

![ de selectiedrop-down van de tijdzoneselectie in reiseigenschappen ](assets/journey72.png)

## Tijdzone profielen gebruiken {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="Tijdzone profiel gebruiken"
>abstract="Schakel het selectievakje in als u de tijdzone van het real-time profiel wilt gebruiken die wacht- en voorwaardenactiviteiten. Als een tijdzone voor een profiel is gedefinieerd, zal het door de reis worden teruggewonnen en gebruikt. Als dat niet het geval is, wordt de tijdzone gedefinieerd in het bovenstaande tijdzone-veld."

Als de entry-gebeurtenis van de reis een naamruimte heeft, wat betekent dat de reis de Real-time service van het Profiel van de Klant van Adobe Experience Platform kan bereiken, kunt u de tijdzone willen gebruiken die op het profielniveau wordt bepaald. Om dit, in **Eigenschappen** te doen, controleer **de tijdzone van het Profiel van het Gebruik in wacht en voorwaarden**. Deze optie is niet standaard ingeschakeld.

Als een tijdzone voor een profiel is gedefinieerd, zal het door de reis worden teruggewonnen en gebruikt. Als dit niet het geval is, wordt de tijdzone gebruikt die is gedefinieerd in het tijdzone-veld.

![ de tijdzoneconfiguratie van het Profiel in gegevensbronnen voor gepersonaliseerde timing ](assets/journey73.png)

>[!NOTE]
>
>De streek van de profieltijd werkt met het **timeZone** gebied bestaand in de **3} gebiedsgroep van de Details van de Voorkeur {.**

## Tijdzones gebruiken in expressies {#timezone-in-expressions}

De begin- en einddatum van een reis kunnen niet worden gekoppeld aan een specifieke tijdzone. Ze worden automatisch gekoppeld aan de tijdzone van de instantie.
