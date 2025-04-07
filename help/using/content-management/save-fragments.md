---
solution: Journey Optimizer
product: journey optimizer
title: Inhoud opslaan als fragment
description: Leer hoe u inhoud kunt opslaan als fragmenten om inhoud te hergebruiken in Journey Optimizer-campagnes en -reizen
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 70e88ea0-f2b0-4c13-8693-619741762429
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Inhoud opslaan als fragment {#save-as-fragment}

Wanneer u inhoud bewerkt in [!DNL Journey Optimizer] , kunt u de inhoud geheel of gedeeltelijk opslaan als fragment en deze later opnieuw gebruiken. U kunt inhoud als fragment of [ van E-mail Designer ](#save-as-visual-fragment) bewaren, of [ van de uitdrukkingsredacteur ](#save-as-expression-fragment).

## Opslaan als visueel fragment {#save-as-visual-fragment}

Voer de volgende stappen uit om inhoud van de e-mailtoepassing als fragment op te slaan:

1. In [ E-mail Designer ](../email/get-started-email-design.md), klik de ellips op hoogste recht van het scherm.

1. Selecteer **[!UICONTROL Save as fragment]** in de vervolgkeuzelijst.

   ![](assets/fragment-save-as.png)

1. Het scherm **[!UICONTROL Save as fragment]** wordt weergegeven. Hier selecteert u de elementen die u in het fragment wilt opnemen, inclusief personalisatievelden en dynamische inhoud. Contextuele kenmerken worden niet ondersteund in fragmenten.

   ![](assets/fragment-save-as-screen.png)

   >[!CAUTION]
   >
   >U kunt alleen secties selecteren die aan elkaar grenzen. U kunt geen lege structuur of een ander fragment selecteren.

1. Klik op **[!UICONTROL Create]** en vul de fragmentnaam en -beschrijving in (indien nodig).

1. Als u aangepaste of basislabels voor gegevensgebruik aan het fragment wilt toewijzen, klikt u op de knop **[!UICONTROL Manage access]** in de bovenste sectie van het scherm. [ leer meer over de Controle van de Toegang van het Niveau van Objecten (OLAC) ](../administration/object-based-access.md).

1. Selecteer of creeer de markeringen van Adobe Experience Platform van het **gebied van Markeringen** om uw malplaatje voor beter onderzoek te categoriseren. [Meer informatie](../start/search-filter-categorize.md#tags)

1. Klik op **[!UICONTROL Create]**. Het fragment wordt toegevoegd aan de [ fragmentlijst ](#access-manage-fragments) met de **3} status van het Ontwerp {.** Het wordt een zelfstandig fragment dat kan worden gebruikt als elk ander visueel fragment uit die lijst.

   >[!NOTE]
   >
   >Wijzigingen in dat nieuwe fragment worden niet doorgegeven aan het e-mailbericht of de sjabloon waaruit het fragment afkomstig is. Op dezelfde manier wordt het nieuwe fragment niet gewijzigd wanneer de oorspronkelijke inhoud wordt bewerkt in het e-mailbericht of de sjabloon.

1. Als u het fragment wilt kunnen gebruiken tijdens reizen en campagnes, moet u het live maken. [ leer hoe te om een fragment ](../content-management/create-fragments.md#publish) voor te vertonen en te publiceren

## Opslaan als expressiefragment {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Opslaan als expressiefragment"
>abstract="In de [!DNL Journey Optimizer] personalization editor kunt u inhoud opslaan als expressiefragmenten. Deze expressies zijn vervolgens beschikbaar voor het samenstellen van gepersonaliseerde inhoud."

In de [!DNL Journey Optimizer] personalization editor kunt u inhoud opslaan als expressiefragmenten. Deze expressies zijn vervolgens beschikbaar voor het samenstellen van gepersonaliseerde inhoud.

Voer de onderstaande stappen uit om inhoud op te slaan als een expressiefragment.

1. In de [ interface van de verpersoonlijkingsredacteur ](../personalization/personalization-build-expressions.md), bouw een uitdrukking, dan klik **[!UICONTROL Save as fragment]**.

   >[!NOTE]
   >
   >Expressies mogen niet groter zijn dan 200 kB.

1. Voer in het rechterdeelvenster een naam en een beschrijving in voor de expressie, zodat gebruikers deze gemakkelijker kunnen vinden.

   ![](assets/expression-fragment-save-as.png)

1. Klik op **[!UICONTROL Save fragment]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. Het fragment wordt toegevoegd aan de [ fragmentlijst ](#access-manage-fragments) met de **3} status van het Ontwerp {.** Het wordt een zelfstandig fragment dat kan worden gebruikt als elk ander expressiefragment uit die lijst.

1. Als u het fragment wilt kunnen gebruiken tijdens reizen en campagnes, moet u het live maken. [ leer hoe te om een fragment ](../content-management/create-fragments.md#publish) voor te vertonen en te publiceren
