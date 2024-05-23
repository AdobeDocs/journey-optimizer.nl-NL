---
title: Gebruiksscenario bij beslissingen van ervaring
description: Leer hoe te om besluiten tot stand te brengen gebruikend experimenten met het op code-gebaseerde kanaal
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
badge: label="Beperkte beschikbaarheid"
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 5%

---

# Gebruiksscenario bij beslissingen van ervaring {#experience-decisioning-uc}

In dit geval definieert u twee leveringsbehandelingen die elk een ander beslissingsbeleid bevatten om te meten welke het beste voor uw doelpubliek presteert.

## Items en strategieën maken

U moet eerst punten tot stand brengen, hen groeperen samen in inzamelingen, opstellingsregels en het rangschikken methodes. Met deze elementen kunt u selectiestrategieën maken.

1. Navigeren naar **[!UICONTROL Experience Decisioning]** > **[!UICONTROL  Catalogs]** en maak meerdere aanbiedingen. Stel beperkingen in met gebruik van soorten publiek of regels om elk item te beperken tot specifieke profielen. [Meer informatie](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. Maken **verzamelingen** om uw beslissingsitems te categoriseren en te groeperen op basis van uw voorkeuren. [Meer informatie](collections.md)

1. Maken **beslissingsregels** om te bepalen aan wie een beslissingselement kan worden getoond. [Meer informatie](rules.md)

1. Maken **waarderingsmethoden** en ze toepassen binnen besluitvormingsstrategieën om de prioriteitsvolgorde voor de selectie van besluitvormingselementen te bepalen. [Meer informatie](ranking.md)

1. Opbouwen **selectiestrategieën** die gebruikmaakt van verzamelingen, besluitvormingsregels en rangschikkingsmethoden om de beslissingsitems te identificeren die geschikt zijn voor weergave naar profielen. [Meer informatie](selection-strategies.md)

## Beslissingsbeleid maken

Als u uw bezoekers de beste dynamische aanbieding en ervaring wilt laten zien op uw website of mobiele app, voegt u een beslissingsbeleid toe aan een op code gebaseerde campagne.

Definieer twee leveringsbehandelingen die elk een ander beslissingsbeleid bevatten.

1. Maak een campagne en selecteer de **[!UICONTROL Code-base experience]** handeling. [Meer informatie](../code-based/create-code-based.md)

1. Klik op de pagina met het overzicht van de campagne **[!UICONTROL Create experiment]** om uw inhoudexperiment te configureren. [Meer informatie](../campaigns/content-experiment.md)

1. Selecteer de **[!UICONTROL Decisions]** pictogram, klikken **[!UICONTROL Create a decision]** en vult de beslissingsdetails in. [Meer informatie](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Geef de selectiestrategieën voor uw beslissing op. Klikken **[!UICONTROL Add strategy]**.

1. Klikken **[!UICONTROL Create]**. Het nieuwe besluit wordt toegevoegd onder **[!UICONTROL Decisions]**.

   ![](assets/decision-code-based-decision-added.png)

1. Klik op het pictogram Meer handelingen (drie punten) en selecteer **[!UICONTROL Add]**. Nu kunt u alle beslissingskenmerken toevoegen die u in deze map wilt opnemen.

   ![](assets/decision-code-based-add-decision.png)

1. U kunt ook alle andere kenmerken toevoegen die beschikbaar zijn in de verpersoonlijkingseditor, zoals profielkenmerken.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Bouw behandeling B en herhaal de stappen hierboven om een andere beslissing tot stand te brengen.

1. Sla uw inhoud op.


