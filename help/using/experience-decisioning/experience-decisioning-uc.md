---
title: Gebruiksscenario voor beslissing
description: Leer hoe te om besluiten tot stand te brengen gebruikend experimenten met het op code-gebaseerde kanaal
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
badge: label="Beperkte beschikbaarheid"
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 6%

---

# Gebruiksscenario voor beslissing {#experience-decisioning-uc}

In dit geval definieert u twee leveringsbehandelingen die elk een ander beslissingsbeleid bevatten om te meten welke het beste voor uw doelpubliek presteert.

## Items en strategieën maken

U moet eerst punten tot stand brengen, hen groeperen samen in inzamelingen, opstellingsregels en het rangschikken methodes. Met deze elementen kunt u selectiestrategieën maken.

1. Navigeer naar **[!UICONTROL Decisioning]** > **[!UICONTROL  Catalogs]** en maak verschillende aanbiedingsitems. Stel beperkingen in met gebruik van soorten publiek of regels om elk item te beperken tot specifieke profielen. [Meer informatie](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. Creeer **inzamelingen** om uw besluitvormingspunten volgens uw voorkeur te categoriseren en te groeperen. [Meer informatie](collections.md)

1. Creeer **besluitvormingsregels** om te bepalen aan wie een besluitpunt kan worden getoond. [Meer informatie](rules.md)

1. Creeer **het rangschikken methodes** en pas hen binnen besluitvormingsstrategieën toe om de prioritaire orde te bepalen om besluitpunten te selecteren. [Meer informatie](ranking.md)

1. Bouw **selectiestrategieën** die hefboominzamelingen, besluitvormingsregels, en het rangschikken methodes om de besluitvormingspunten te identificeren geschikt voor het tonen aan profielen. [Meer informatie](selection-strategies.md)

## Beslissingsbeleid maken

Als u uw bezoekers de beste dynamische aanbieding en ervaring wilt laten zien op uw website of mobiele app, voegt u een beslissingsbeleid toe aan een op code gebaseerde campagne.

Definieer twee leveringsbehandelingen die elk een ander beslissingsbeleid bevatten.

1. Maak een campagne en selecteer de handeling **[!UICONTROL Code-base experience]** . [Meer informatie](../code-based/create-code-based.md)

1. Klik in de overzichtspagina van de campagne op **[!UICONTROL Create experiment]** om uw inhoudexperiment te configureren. [Meer informatie](../content-management/content-experiment.md)

1. Selecteer het pictogram **[!UICONTROL Decisions]** , klik op **[!UICONTROL Create a decision]** en vul de beslissingsdetails in. [Meer informatie](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Geef de selectiestrategieën voor uw beslissing op. Klik op **[!UICONTROL Add strategy]**.

1. Klik op **[!UICONTROL Create]**. De nieuwe beslissing wordt toegevoegd onder **[!UICONTROL Decisions]** .

   ![](assets/decision-code-based-decision-added.png)

1. Klik op het pictogram Meer handelingen (drie punten) en selecteer **[!UICONTROL Add]** . Nu kunt u alle beslissingskenmerken toevoegen die u in deze map wilt opnemen.

   ![](assets/decision-code-based-add-decision.png)

1. U kunt ook alle andere kenmerken toevoegen die beschikbaar zijn in de verpersoonlijkingseditor, zoals profielkenmerken.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Bouw behandeling B en herhaal de stappen hierboven om een andere beslissing tot stand te brengen.

1. Sla uw inhoud op.


