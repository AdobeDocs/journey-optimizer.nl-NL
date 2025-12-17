---
title: Aan de slag met beslissing-API's
description: Leer hoe u de API's voor besluitvorming kunt gebruiken om beslissingsitems programmatisch te beheren en persoonlijke aanbiedingen te leveren.
feature: API, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 7a4b5d4e-9c1d-4f3a-b8e9-1d5f6e7a8c3a
version: Journey Orchestration
source-git-commit: e46ab0637a0fa4a2b4b8b6ff3b8ab3eb5d38e0f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Handleiding voor ontwikkelaars van API voor besluitvorming {#decisioning-api-developer-guide}

Het besluiten APIs staat u toe om programmatically de componenten tot stand te brengen en te beheren die worden gebruikt om gepersonaliseerde aanbiedingen aan uw klanten te leveren. Deze RESTful APIs verstrekt volledige CRUD (Create, Read, Update, Schrapping) verrichtingen voor besluitvormingspunten, selectiestrategieën, geschiktheidsregels, en andere beslissingscomponenten.

## Verificatie {#authentication}

Voordat u besluit-API&#39;s kunt gebruiken, moet u verificatie instellen voor toegang tot de API-eindpunten. U kunt naar de [ de authentificatiegids van Journey Optimizer ](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} voor geleidelijke instructies verwijzen.

## Beschikbare API-bewerkingen {#available-operations}

De API&#39;s voor besluitvorming bieden uitgebreide beheermogelijkheden voor besluitvormingscomponenten. De volgende categorieën bewerkingen zijn beschikbaar:

* **de punten van het Besluit** - creeer, lees, werk bij, schrap, en de punten van het lijstbesluit die de aanbiedingen of de inhoud vertegenwoordigen u aan klanten wilt leveren.

  ➡️ [ Leer hoe te om besluitpunten ](decisions-items/create.md) te beheren

* **de inzamelingen van het Punt** - organiseer besluitvormingspunten in inzamelingen voor gemakkelijker beheer en het richten gebruikend toelatingsregels.

  ➡️ [ Leer hoe te om puntinzamelingen ](items-collections/create.md) te beheren

* **de strategieën van de Selectie** - bepalen hoe de besluitvormingspunten worden geselecteerd en gerangschikt wanneer de veelvoudige punten voor levering kwalificeren.

  ➡️ [ Leer hoe te om selectiestrategieën te beheren ](selection-strategies/create.md)

* **Regels van de Belichting** - plaats voorwaarden die bepalen welke profielen verkiesbaar zijn om specifieke besluitvormingspunten te ontvangen.

  ➡️ [ Leer hoe te om toelatingsregels te beheren ](eligibility-rules/create.md)

* **Rangschikkende formules** - creeer douanerangschikkende logica om de orde te bepalen waarin de besluitvormingspunten worden voorgesteld.

  ➡️ [ Leer hoe te om het rangschikken formules ](ranking-formulas/create.md) te beheren

* **Plaatsen** - bepaal de plaatsen of de contexten waar de besluitvormingspunten in uw ervaringen kunnen worden getoond.

  ➡️ [ Leer hoe te om plaatsingen ](exd-placements/create.md) te beheren

## Volgende stappen {#next-steps}

Nu u de grondbeginselen van de Beslissings APIs begrijpt, kunt u aan de specifieke verrichtingen verdergaan:

* [Beslissingsitems maken](decisions-items/create.md)
* [Beslissingsitems weergeven](decisions-items/decision-items-list.md)
* [Selectiestrategieën maken](selection-strategies/create.md)
* [Subsidiabiliteitsregels maken](eligibility-rules/create.md)

Voor meer informatie over het gebruiken van besluit in uw campagnes en reizen, verwijs naar de [ documentatie van het Beslissen ](../gs-experience-decisioning.md).
