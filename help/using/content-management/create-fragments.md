---
solution: Journey Optimizer
product: journey optimizer
title: Een fragment maken
description: Leer hoe u fragmenten maakt om inhoud te hergebruiken in Journey Optimizer-campagnes en -reizen
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 83997271d16e15fb0d7ccdd21aa8ac8b8221a0d5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 1%

---


# Een geheel nieuw fragment maken {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Selecteer het visuele type"
>abstract="Maak een zelfstandig visueel fragment om uw inhoud te hergebruiken in een e-mail binnen een reis, een campagne of een inhoudssjabloon."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html" text="Visuele fragmenten toevoegen aan uw e-mails"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Expressietype selecteren"
>abstract="Maak een zelfstandig expressiefragment om uw inhoud te hergebruiken voor meerdere reizen en campagnes. Wanneer u de verpersoonlijkingseditor gebruikt, kunt u alle uitdrukkingsfragmenten benutten die in de huidige sandbox zijn gemaakt."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html" text="Expressiefragmenten benutten"

Fragmenten worden gemaakt op basis van de **[!UICONTROL Fragments]** links. Bovendien kunt u een gedeelte van bestaande inhoud als fragment opslaan wanneer u inhoud ontwerpt. [Meer informatie](#save-as-fragment)

Als het fragment eenmaal is opgeslagen, kan het worden gebruikt in een reis, een campagne of een sjabloon. U kunt dit fragment nu gebruiken wanneer u inhoud maakt binnen [!DNL Journey Optimizer]. Zie [Visuele fragmenten toevoegen](../email/use-visual-fragments.md) en [Expressiefragmenten benutten](../personalization/use-expression-fragments.md)

Voer de onderstaande stappen uit om een geheel nieuw fragment te maken.

1. [De fragmentlijst openen](#access-manage-fragments) via de **[!UICONTROL Content Management]** > **[!UICONTROL Fragments]** links.

1. Selecteren **[!UICONTROL Create fragment]**.

1. Vul de fragmentdetails in, d.w.z. naam en beschrijving (indien nodig).

   ![](assets/fragment-details.png)

1. Adobe Experience Platform-tags selecteren of maken vanuit het menu **[!UICONTROL Tags]** veld om het fragment te categoriseren voor een betere zoekopdracht. [Meer informatie](../start/search-filter-categorize.md#tags)

1. Selecteer het fragmenttype: [Visueel fragment](#create-visual-fragment) of [Expressiefragment](#create-expression-fragment).

   >[!NOTE]
   >
   >Op dit moment geldt voor visuele fragmenten alleen het dialoogvenster **E-mail** wordt ondersteund.

1. Als u een expressiefragment maakt, selecteert u het type code dat u wilt gebruiken: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** of **[!UICONTROL Text]**.

   ![](assets/fragment-expression-type.png)

1. Als u aangepaste of basislabels voor gegevensgebruik aan het fragment wilt toewijzen, selecteert u **[!UICONTROL Manage access]**. [Leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC)](../administration/object-based-access.md).

1. Klikken **[!UICONTROL Create]**.

1. De [E-mailDesigner](../email/get-started-email-design.md) of de verpersoonlijkingseditor wordt geopend, afhankelijk van het type fragment dat u maakt.

   * Voor visuele fragmenten kunt u de inhoud naar wens bewerken, net zoals u dat zou doen voor elke e-mail in een rit of campagne.

     >[!NOTE]
     >
     >U kunt aanpassingsvelden en dynamische inhoud toevoegen, maar contextafhankelijke kenmerken worden niet ondersteund in fragmenten.

     ![](assets/fragment-designer.png)

   * Gebruik voor expressiefragmenten de optie [!DNL Journey Optimizer] personalisatie-editor met al zijn personalisatie- en ontwerpmogelijkheden om uw fragmentinhoud samen te stellen. [Meer informatie](../personalization/personalization-build-expressions.md)

     ![](assets/fragment-expression-editor.png)

1. Wanneer het fragment gereed is, klikt u op **[!UICONTROL Save]**.

Het fragment wordt toegevoegd aan de [fragmentlijst](#access-manage-fragments). Het is nu gereed om te worden gebruikt wanneer u inhoud maakt binnen de [!DNL Journey Optimizer] E-mailontwerper of personalisatie-editor.

* [Leer hoe u visuele fragmenten kunt gebruiken](../email/use-visual-fragments.md)
* [Leer hoe u expressiefragmenten kunt gebruiken](../personalization/use-expression-fragments.md)
