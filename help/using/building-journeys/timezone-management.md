---
title: Tijdzonebeheer
description: Meer informatie over tijdzonebeheer
feature: Journeys
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: d76eee0efa6735d6d81d7d7c752ed253b4cbebb5
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 3%

---

# Tijdzonebeheer {#timezone_management}

U kunt een tijdzone in [eigenschappen](../building-journeys/journey-gs.md#change-properties) van uw reis bepalen.

Als u eigenschappen wilt openen, klikt u op het potloodpictogram rechtsboven in het scherm.

Deze tijdzone wordt gebruikt voor elke activiteit van de reis die een tijdselement bevat, zoals:

* [Tijdvoorwaarde](../building-journeys/condition-activity.md#time_condition)
* [Datumvoorwaarde](../building-journeys/condition-activity.md#date_condition)
* [Aangepast wachten](../building-journeys/wait-activity.md#custom)
* [Wachttijd voor vaste datum](../building-journeys/wait-activity.md#fixed_date)

U kunt een tijdzone selecteren of de tijdzone gebruiken die is gedefinieerd in het gebruikersprofiel.

>[!NOTE]
>
>De profieltijdzone werkt met het **timeZone** gebied dat in **Preference Details** gebiedsgroep bestaat.

## Een vaste tijdzone {#fixed-timezone} definiëren

De tijdzone kan ook worden vastgesteld. Wis de vooraf gedefinieerde tijdzone en kies een tijdzone in de vervolgkeuzelijst. Als je een vaste tijdzone gebruikt, zal dat hetzelfde zijn voor iedereen die de reis binnenkomt.

Selecteer hiertoe in het deelvenster **[!UICONTROL Journey Properties]** een tijdzone.

![](../assets/journey72.png)

## Profielen gebruiken om de reistijdzone {#timezone-from-profiles} te definiëren

Als de entry-gebeurtenis van de reis een naamruimte heeft, wat betekent dat de reis de Real-time dienst van het Profiel van de Klant van Adobe Experience Platform kan bereiken, is de tijdzone vooraf gedefinieerd met die gespecificeerd in het profiel van de individuele die in de reis stroomt.

Als een tijdzone in Adobe Experience Platform-profiel is gedefinieerd, kan deze tijdens de reis worden opgehaald.

Als het profiel van het individu geen tijdzone bevat, wordt de opgehaalde tijdzone gedefinieerd in het tijdzoneveld.

Om dit te doen, in **[!UICONTROL Properties]**, controleer **[!UICONTROL Use Profile timezone in waits and conditions]**.

![](../assets/journey73.png)

## Tijdzones gebruiken in expressies {#timezone-in-expressions}

De begin- en einddatum van een reis kunnen niet worden gekoppeld aan een specifieke tijdzone. Ze worden automatisch gekoppeld aan de tijdzone van de instantie.
