---
solution: Journey Optimizer
product: journey optimizer
title: De reis publiceren
description: Leer hoe u op uw gekozen metrisch traject rapporteert
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publiceren, reizen, live, geldigheid, controle
exl-id: 95d0267e-fab4-4057-8ab5-6f7c9c866b0f
source-git-commit: 1e35c2ea2b0a6c8edd5b870311bb32b4b4b58e9a
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 1%

---

# Vorm en spoor uw reis metrisch {#success-metrics}

Met reismetriek, kunt u effectief het effect van uw activiteiten meten door hun prestaties tegen vooraf bepaalde metriek te volgen.
Door deze metriek te volgen, kunt u zien hoe goed uw reis presteert, gebieden voor verbetering identificeren, en geïnformeerde besluiten nemen om klantenbetrokkenheid te verbeteren.

## Vereisten {#prerequisites}

Alvorens uw reis metrisch te gebruiken, moet u een dataset toevoegen die `Commerce Details`, `Web` en `Mobile` [ gebiedsgroepen ](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group) {target="_blank"} omvat.

## Beschikbare cijfers {#metrics}

De lijst van metriek varieert afhankelijk van de [ gebiedsgroepen ](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group) {target="_blank"} inbegrepen aan uw dataset.

Als uw dataset niet wordt gevormd, slechts zullen de volgende metriek beschikbaar zijn: **[!UICONTROL Click]**, **[!UICONTROL Unique Click]**, **[!UICONTROL Clickthrough Rate]** en **[!UICONTROL Open Rate]**.

Met een Customer Journey Analytics-licentie kunt u aangepaste succeswaarden maken. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/participation-metric)


| Metrics | Verwante veldgroep |
|-|-|
| Klikken | Geen veldgroep vereist |
| Unieke klikken | Geen veldgroep vereist |
| Doorkliksnelheid (CTR) | Geen veldgroep vereist |
| Klikken door open snelheid (CTOR) | Geen veldgroep vereist |
| Paginaweergaven | Webveldgroep |
| App Launches | Mobiele veldgroep |
| First App Launches | Mobiele veldgroep |
| App-installaties | Mobiele veldgroep |
| App-upgrades | Mobiele veldgroep |
| Aankopen | Commerce Details, veldgroep |
| Afbeeldingen | Commerce Details, veldgroep |
| Extra winkelwagentjes | Commerce Details, veldgroep |
| Kleurafopen | Commerce Details, veldgroep |
| Kleuraweergaven | Commerce Details, veldgroep |
| Winkelwagentjes verwijderen | Commerce Details, veldgroep |
| Productweergaven | Commerce Details, veldgroep |
| Opslaan voor later | Commerce Details, veldgroep |

## Attributie {#attribution}

Elke metrisch komt met een vastgestelde attributie die bepaalt welke aanraakpunten of interactie tot een specifiek resultaat hebben bijgedragen.

* **Attributie van Metriek met de vergunning van Journey Optimizer**:

  Met Journey Optimizer-licentie alleen wordt het maximale beschikbare terugzoekvenster voor elke geselecteerde metrische waarde ingesteld op 7 dagen. Voor deze metriek, wordt het attributiemodel geplaatst door gebrek aan **Laatste aanraking**, d.w.z. de meest recente interactie vóór omzetting.

  U kunt bijvoorbeeld bijhouden of een aankoop is gedaan nadat een klant de laatste 7 dagen met uw reis heeft gewerkt.

* **Attributie van Metriek met de vergunning van Customer Journey Analytics**:

  Met Journey Optimizer- en Customer Journey Analytics-licenties kunt u aangepaste metriek maken met specifieke attributie-instellingen of de kenmerken van de ingebouwde metriek wijzigen.

  Leer meer op [ modellen van de Attributie ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)

## Uw metrische gegevens voor reizen toewijzen {#assign}

Volg de onderstaande stappen om uw metrische gegevens over de reis te volgen:

1. Klik in het menu **[!UICONTROL Journeys]** op **[!UICONTROL Create Journey]** .

1. Bewerk het configuratievenster van de rit om de naam van de rit te definiëren en de eigenschappen ervan in te stellen. Leer hoe te om de eigenschappen van uw reis in [ te plaatsen deze pagina ](../building-journeys/journey-properties.md).

1. Kies de **[!UICONTROL Journey metrics]** die wordt gebruikt om de effectiviteit van uw reis te meten.

   Merk op dat de meetgegevens van toepassing zijn op de reis zelf en van toepassing zijn op alle onderdelen van de reis.

   ![](assets/success_metric.png)

1. Klik op **[!UICONTROL Save]**.

1. Ontwerp uw reis met de benodigde **[!UICONTROL Activities]** .

1. Test en publiceer uw reis.

1. Open uw reisrapport om de prestaties van uw toegewezen succes metrisch te volgen.

   Uw gekozen metrisch wordt getoond in de lijst van KPIs en van de Stats van de Reis van het rapport.

   ![](assets/success_metric_2.png)
