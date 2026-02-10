---
solution: Journey Optimizer
product: journey optimizer
title: '[!DNL Adobe Campaign] Handelingen voor v7/v8'
description: Meer informatie over  [!DNL Adobe Campaign]  v7/v8-acties
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: reis, integratie, campagne, v7, v8
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# [!DNL Adobe Campaign] Handelingen voor v7/v8 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Aangepaste acties"
>abstract="Er is integratie beschikbaar als u [!DNL Adobe Campaign] v7 of v8 hebt. Hiermee kunt u e-mails, pushberichten en SMS verzenden met de mogelijkheden van [!DNL Adobe Campaign] Transactieberichten."

Er is integratie beschikbaar als u [!DNL Adobe Campaign] v7 of v8 hebt. Hiermee kunt u e-mails, pushberichten en SMS verzenden met de mogelijkheden van [!DNL Adobe Campaign] Transactieberichten.

De verbinding tussen de Journey Optimizer- en Campagneinstanties wordt door Adobe tijdens de levering ingesteld. Neem contact op met Adobe.

**wanneer te gebruiken**: De acties van de Campagne v7/v8 van het gebruik wanneer uw overseinen op de transactiesjablonen van de Campagne, campagne-specifieke gegevensmodellen, of bestaande de leveringswerkschema&#39;s van de Campagne baseert.

**Vereisten**

* Uw [!DNL Adobe Campaign] v7/v8-exemplaar wordt geleverd en verbonden met Journey Optimizer door Adobe.
* U hebt toegang tot het Transactioneel Overseinen van de Campagne en de vereiste toestemmingen.

Om dit te werken, moet u een specifieke actie vormen. Verwijs naar deze [ sectie ](../action/acc-action.md).

Een gebruiksgeval van begin tot eind wordt voorgesteld in deze [ sectie ](../building-journeys/ajo-ac.md).

1. Ontwerp uw reis, te beginnen met een gebeurtenis. Zie deze [ sectie ](../building-journeys/journey.md).
1. In de **sectie van de Actie** van het palet, selecteer een actie van de Campagne en voeg het aan uw reis toe.
1. In de **parameters van de Actie**, worden alle gebieden die in de berichtlading worden verwacht getoond. U moet elk van deze gebieden met het gebied in kaart brengen u, of van de gebeurtenis of van de gegevensbron wilt gebruiken. Dit is vergelijkbaar met aangepaste handelingen. Verwijs naar deze [ sectie ](../building-journeys/using-custom-actions.md).

>[!NOTE]
>
>* Campagne v7/v8-acties kunnen samen met native kanaalacties op dezelfde reis worden gebruikt. Dit geldt niet voor Campaign Standard-acties. Zie [ de activiteitenbegeleiding van de Campagne ](../start/guardrails.md#ac-g).
>* De acties van de campagne v7/v8 kunnen niet met de activiteiten van de Erkenning van het publiek of van het Publiek worden gebruikt. Zie de handleidingen bij Audience Read and Audience Qualification op de pagina Guardrails.

![[!DNL Adobe Campaign] Configuratie en integratie-instellingen voor v7/v8-acties ](assets/accintegration2.png)
