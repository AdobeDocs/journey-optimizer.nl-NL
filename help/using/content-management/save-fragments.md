---
solution: Journey Optimizer
product: journey optimizer
title: Inhoud opslaan als fragment
description: Leer hoe u inhoud kunt opslaan als fragmenten om inhoud te hergebruiken in Journey Optimizer-campagnes en -reizen
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 83997271d16e15fb0d7ccdd21aa8ac8b8221a0d5
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Inhoud opslaan als fragment {#save-as-fragment}

Bij het bewerken van inhoud in [!DNL Journey Optimizer], kunt u de inhoud geheel of gedeeltelijk opslaan als fragment voor toekomstig hergebruik.

## Inhoud opslaan als visueel fragment {#save-as-visual-fragment}

Wanneer u een [inhoudssjabloon](content-templates.md) of een [email](../email/get-started-email-design.md) in een campagne of een reis, kunt u een gedeelte van uw inhoud als visueel fragment bewaren. Volg de onderstaande stappen om dit te doen.

1. In de [E-mailDesigner](../email/get-started-email-design.md)Klik op de ellips rechtsboven in het scherm.

1. Selecteren **[!UICONTROL Save as fragment]** in het keuzemenu.

   ![](assets/fragment-save-as.png)

1. De **[!UICONTROL Save as fragment]** schermweergaven. Hier selecteert u de elementen die u in het fragment wilt opnemen, inclusief personalisatievelden en dynamische inhoud. Contextuele kenmerken worden niet ondersteund in fragmenten.

   >[!CAUTION]
   >
   >U kunt alleen secties selecteren die aan elkaar grenzen. U kunt geen lege structuur of een ander fragment selecteren.

   ![](assets/fragment-save-as-screen.png)

1. Klikken **[!UICONTROL Create]**. Vul de fragmentdetails in, d.w.z. naam en beschrijving (indien nodig).

1. Als u aangepaste of basislabels voor gegevensgebruik aan het fragment wilt toewijzen, selecteert u **[!UICONTROL Manage access]**. [Leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC)](../administration/object-based-access.md).

1. Adobe Experience Platform-tags selecteren of maken vanuit het menu **Tags** veld om de sjabloon te categoriseren voor een betere zoekopdracht. [Meer informatie](../start/search-filter-categorize.md#tags)

1. Klikken **[!UICONTROL Create]** opnieuw. Het fragment wordt opgeslagen in toegevoegd aan de [fragmentlijst](#access-manage-fragments), toegankelijk via de [!DNL Journey Optimizer] speciaal menu.

   Het wordt een zelfstandig fragment dat [benaderd](#access-manage-fragments), [bewerkt](#edit-fragments) en [gearchiveerd](#archive-fragments) zoals elk ander item op die lijst.

U kunt dit fragment nu gebruiken wanneer u een [email](../email/get-started-email-design.md) of [inhoudssjabloon](content-templates.md) binnen [!DNL Journey Optimizer]. [Meer informatie](../email/use-visual-fragments.md)

>[!NOTE]
>
>Wijzigingen in dat nieuwe fragment worden niet doorgegeven aan het e-mailbericht of de sjabloon waaruit het fragment afkomstig is. Op dezelfde manier wordt het nieuwe fragment niet gewijzigd wanneer de oorspronkelijke inhoud wordt bewerkt in het e-mailbericht of de sjabloon.

## Inhoud opslaan als expressiefragment {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Opslaan als expressiefragment"
>abstract="De [!DNL Journey Optimizer] met de personalisatie-editor kunt u inhoud opslaan als expressiefragmenten. Deze expressies zijn vervolgens beschikbaar voor het samenstellen van gepersonaliseerde inhoud."

De [!DNL Journey Optimizer] met de personalisatie-editor kunt u inhoud opslaan als expressiefragmenten. Deze expressies zijn vervolgens beschikbaar voor het samenstellen van gepersonaliseerde inhoud.

Voer de onderstaande stappen uit om inhoud op te slaan als een expressiefragment.

1. In de [personalisatie-editor](../personalization/personalization-build-expressions.md) interface, bouwt een uitdrukking, dan klikt **[!UICONTROL Save as fragment]**.

1. Voer in het rechterdeelvenster een naam en een beschrijving in voor de expressie, zodat gebruikers deze gemakkelijker kunnen vinden.

   ![](assets/expression-fragment-save-as.png)

1. Klikken **[!UICONTROL Save fragment]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. Het uitdrukkingsfragment wordt toegevoegd aan [fragmentlijst](#access-manage-fragments). U kunt het nu gebruiken om gepersonaliseerde inhoud te bouwen.

>[!NOTE]
>
>Expressies mogen niet groter zijn dan 200 kB.
