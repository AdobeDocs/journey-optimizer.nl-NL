---
solution: Journey Optimizer
product: journey optimizer
title: journeyvelden
description: journeyvelden
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 177b4a97-c757-40ca-a190-fbd88169e5e2
source-git-commit: 6961a07e2874f9beb76a9beaebb29997d114d8e7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---

# Reisvelden {#sharing-journey-fields}

Deze gebiedsgroep wordt gebruikt in het **reis** schema (met betrekking tot **tripStepEvent**). Het bevat de onderstaande velden.


>[!NOTE]
>
>Leer meer over de attributen van de reiseigenschappen [&#x200B; in deze sectie &#x200B;](../building-journeys/expression/journey-properties.md#journey-properties-fields).


## tripID {#journeyid-field}

Id van de hoofdreis.

Type: tekenreeks

## tripVersionID {#journeyversionid-field}

Id van de reisversie. Deze id staat voor de identiteit van een reis.

Type: tekenreeks

## name {#name-field}

Naam van de reis.

Type: tekenreeks

>[!NOTE]
>
>De naam van de reis wordt gebruikt om gegevens van de reisuitvoering met rapporteringsdatasets te verbinden. Als u een reis anders noemt, zorg ervoor dat de nieuwe naam de naam in uw rapporteringsdataset aanpast om nauwkeurige rapportering te handhaven. Een probleem kan ertoe leiden dat rapportgegevens niet naar behoren worden weergegeven. Leer meer over [&#x200B; het oplossen van problemen ontbrekende het melden van gegevens &#x200B;](../building-journeys/report-journey.md#troubleshooting-missing-data).

## beschrijving {#description-field}

Beschrijving van de reis.

Type: tekenreeks

## versie {#version-field}

Versie, weergegeven als `major`.`minor`

Type: tekenreeks
