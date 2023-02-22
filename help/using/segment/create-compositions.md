---
solution: Journey Optimizer
product: journey optimizer
title: Samenstellingswerkstromen maken
description: Leer hoe u samenstellingsworkflows maakt om bestaande soorten publiek te combineren en te rangschikken.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 0%

---

# Samenstellingswerkstromen maken {#create-compositions}

Met samenstellingsworkflows kunt u bestaande soorten publiek combineren en rangschikken om nieuwe soorten publiek te maken.

## Een compositieworkflow maken {#create}

1. Toegang krijgen tot **[!UICONTROL Segments]** en selecteert u **[!UICONTROL Create Audience]**.

1. Selecteer **[!UICONTROL Compose Audience]**.

   >[!NOTE]
   >
   >De **[!UICONTROL Build rule]** Met de methode waarmee u een nieuw segment kunt maken, kunt u [Segmenteringsservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-create.png)

1. Het compositicanvas wordt weergegeven met twee standaardactiviteiten:

   * **[!UICONTROL Audience]**: het uitgangspunt van uw samenstelling. Met deze activiteit kunt u een of meer soorten publiek selecteren als basis voor uw workflow.

   * **[!UICONTROL Save]**: de laatste stap van uw compositie. Met deze activiteit kunt u het resultaat van uw workflow opslaan in een nieuw publiek.
   Voor meer informatie over hoe te om activiteiten in het canvas van het samenstellingswerkschema te vormen, verwijs naar [Werken met het compositicanvas](composition-canvas.md).

1. Open de compositieeigenschappen om een titel en een beschrijving op te geven.

   Als er geen titel is gedefinieerd in de eigenschappen, wordt het samengestelde label het eerste **[!UICONTROL Audience]** activiteit.

   ![](assets/audiences-properties.png)

1. Vorm uw samenstelling door zo vele activiteiten toe te voegen zoals nodig tussen **[!UICONTROL Audience]** en **[!UICONTROL Save]** activiteiten. [Leer hoe u met het compositicanvas werkt](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Zodra uw samenstelling klaar is, klik **[!UICONTROL Publish]** om de compositie te publiceren en het resulterende publiek op te slaan in Adobe Experience Platform.

   Als er tijdens het publiceren een fout optreedt, worden waarschuwingen weergegeven met informatie over hoe u het probleem kunt oplossen.

   ![](assets/audiences-alerts.png)

1. De compositie wordt gepubliceerd. Het resulterende publiek wordt opgeslagen in Adobe Experience Platform en is klaar om te worden gebruikt in Journey Optimizer-campagnes. [Leer hoe u met campagnes kunt werken](../campaigns/get-started-with-campaigns.md)

## Toegang tot composities {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Uw publiek publiceren"
>abstract="Publiceer uw compositie om het resulterende publiek of de doelgroepen op te slaan in Adobe Experience Platform."

Alle gemaakte composities zijn toegankelijk via de **[!UICONTROL Compositions]** tab. Ze kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: de samenstelling is in uitvoering en is niet gepubliceerd.
* **[!UICONTROL Published]**: de samenstelling is gepubliceerd , het resulterende publiek is opgeslagen en beschikbaar voor gebruik .
* **[!UICONTROL Archived]**: de samenstelling is gearchiveerd .

![](assets/audiences-compositions.png)

>[!NOTE]
>
>U kunt een bestaande compositie op elk gewenst moment dupliceren of verwijderen met de knop voor weglatingen in de lijst.

Meer informatie:

* [Aan de slag met publiekscompositie](get-started-audience-orchestration.md)
* [Werken met het compositicanvas](composition-canvas.md)
* [Toegang tot en beheer van het publiek](access-audiences.md)
