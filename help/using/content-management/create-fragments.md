---
solution: Journey Optimizer
product: journey optimizer
title: Een fragment maken
description: Leer hoe u fragmenten maakt om inhoud te hergebruiken in Journey Optimizer-campagnes en -reizen
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: da3ffe9c-a244-4246-b4b5-a3a1d0508676
source-git-commit: bcccc7b385f031fba2c2b57ec62cae127eda8466
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Een fragment maken {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Selecteer het visuele type"
>abstract="Maak een zelfstandig visueel fragment om uw inhoud te hergebruiken in een e-mail binnen een reis, een campagne of een inhoudssjabloon."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments" text="Visuele fragmenten toevoegen aan uw e-mails"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Expressietype selecteren"
>abstract="Maak een zelfstandig expressiefragment om uw inhoud te hergebruiken voor meerdere reizen en campagnes. Wanneer u de verpersoonlijkingseditor gebruikt, kunt u alle uitdrukkingsfragmenten benutten die in de huidige sandbox zijn gemaakt."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments" text="Expressiefragmenten benutten"

U kunt geheel nieuwe fragmenten maken in het menu links van **[!UICONTROL Fragments]** . Bovendien kunt u een gedeelte van bestaande inhoud als fragment opslaan wanneer u inhoud ontwerpt. [ leer hoe ](#save-as-fragment)

Als het fragment eenmaal is opgeslagen, kan het worden gebruikt in een reis, een campagne of een sjabloon. U kunt dit fragment gebruiken bij het maken van inhoud binnen reizen en campagnes. Zie [ visuele fragmenten ](../email/use-visual-fragments.md) en [ de uitdrukkingsfragmenten van de Leverage ](../personalization/use-expression-fragments.md) toevoegen

Voer de onderstaande stappen uit om een fragment te maken.

## De eigenschappen van het fragment definiëren {#properties}

1. Open de fragmentlijst via het menu **[!UICONTROL Content Management]** > **[!UICONTROL Fragments]** links.

1. Selecteer **[!UICONTROL Create fragment]** en vul de fragmentnaam en -beschrijving in (indien nodig).

   ![](assets/fragment-details.png)

1. Selecteer of maak Adobe Experience Platform-tags in het veld **[!UICONTROL Tags]** om het fragment te categoriseren voor een betere zoekopdracht. [ Leer hoe te met Verenigde Markeringen ](../start/search-filter-categorize.md#tags) te werken

1. Selecteer het fragmenttype: **Visueel fragment** of **het fragment van de Uitdrukking**. [ leer meer op visuele en uitdrukkingsfragmenten ](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >Voor nu, zijn de visuele fragmenten beschikbaar voor het **E-mail** slechts kanaal.

1. Als u een expressiefragment maakt, selecteert u het type code dat u wilt gebruiken: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** of **[!UICONTROL Text]** .

   ![](assets/fragment-expression-type.png)

1. Als u aangepaste of basislabels voor gegevensgebruik aan het fragment wilt toewijzen, klikt u op de knop **[!UICONTROL Manage access]** in de bovenste sectie van het scherm. [ leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC) ](../administration/object-based-access.md).

1. Klik op **[!UICONTROL Create]** om de inhoud van het fragment te ontwerpen.

## De fragmentinhoud ontwerpen {#content}

Nadat u de eigenschappen van het fragment hebt geconfigureerd, wordt de e-mail-Designer of de personalisatie-editor geopend, afhankelijk van het type fragment dat u maakt.

* Voor visuele fragmenten kunt u de inhoud naar wens bewerken, net zoals u dat zou doen voor elke e-mail in een rit of campagne. [Meer informatie](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

* Voor expressiefragmenten gebruikt u de [!DNL Journey Optimizer] personalization-editor met al zijn personalisatie- en ontwerpmogelijkheden om de fragmentinhoud samen te stellen. [Meer informatie](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

Wanneer uw inhoud klaar is, klik **sparen** knoop. Het fragment wordt gecreeerd en aan de fragmentlijst met de **status van het Ontwerp** toegevoegd. U kunt een voorvertoning weergeven en deze publiceren om deze beschikbaar te maken tijdens reizen en campagnes.

## Het fragment voorvertonen en publiceren {#publish}

>[!NOTE]
>
>Om een fragment te publiceren, moet u de ](../administration/ootb-product-profiles.md#content-library-manager) gebruikerstoestemming van het Fragment van 0} Publish hebben.[

Als uw fragment klaar is om live te gaan, kunt u het voorbeeld bekijken en publiceren en het beschikbaar maken tijdens uw reizen en campagnes. Voer hiertoe de volgende stappen uit:

1. Ga terug naar het scherm voor het maken van fragmenten nadat u de inhoud hebt ontworpen, of open het vanuit de lijst met fragmenten.

1. Een voorproef van het fragment is beschikbaar onder het **gebied van Markeringen**, toestaand om zijn het teruggeven te controleren. Als u om het even welke verandering moet aanbrengen, klik **uitgeven** knoop in de hogere sectie van het scherm om E-mail Designer of de verpersoonlijkingsredacteur afhankelijk van het fragmenttype te openen.

   ![](assets/fragment-preview.png)

1. Klik de **knoop van Publish** in de hoger-juiste hoek om het fragment te publiceren.

   Als het fragment tijdens een live reis of campagne wordt gebruikt, verschijnt er een bericht om u hiervan op de hoogte te stellen. Klik **zie meer** verbinding om tot de lijst van reizen en/of campagnes toegang te hebben waar het van verwijzingen wordt voorzien. [ leer hoe te om verwijzingen van een fragment ](../content-management/manage-fragments.md#explore-references) te onderzoeken

   Klik **bevestigen** om het fragment te publiceren en het in de levende reizen/campagnes bij te werken die het gebruiken.

   ![](assets/fragment-publish.png){width="70%" align="center"}

Het fragment is nu Levend ****, en wordt beschikbaar wanneer het bouwen van om het even welke inhoud binnen de [!DNL Journey Optimizer] E-mail Designer of verpersoonlijkingsredacteur:

* [Leer hoe u visuele fragmenten kunt gebruiken](../email/use-visual-fragments.md)
* [Leer hoe u expressiefragmenten kunt gebruiken](../personalization/use-expression-fragments.md)
