---
solution: Journey Optimizer
product: journey optimizer
title: Uw eerste compositieworkflow maken
description: Leer hoe u samenstellingsworkflows maakt om bestaande soorten publiek te combineren en te rangschikken.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
badge: label="Beta" type="Informatief"
source-git-commit: 2acb92e5157b4e0ecc026b66078f65e82f76ff5e
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Uw eerste compositieworkflow maken {#create-compositions}

>[!BEGINSHADEBOX]

Wat u in deze documentatie zult vinden:

* [Aan de slag met publiekscompositie](get-started-audience-orchestration.md)
* **[Uw eerste compositieworkflow maken](create-compositions.md)**
* [Werken met het compositicanvas](composition-canvas.md)
* [Toegang tot en beheer van het publiek](access-audiences.md)

>[!ENDSHADEBOX]

## Een compositieworkflow maken {#create}

Ga als volgt te werk om een compositieworkflow te maken:

1. Toegang krijgen tot **[!UICONTROL Segments]** en selecteert u **[!UICONTROL Create Audience]**.

1. Selecteer **[!UICONTROL Compose Audience]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >De **[!UICONTROL Build rule]** Met de methode waarmee u een nieuw segment kunt maken, kunt u [Segmenteringsservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

1. Het compositicanvas wordt weergegeven met twee standaardactiviteiten:

   * **[!UICONTROL Audience]**: het uitgangspunt van uw samenstelling. Met deze activiteit kunt u een of meer soorten publiek selecteren als basis voor uw workflow.

   * **[!UICONTROL Save]**: de laatste stap van uw compositie. Met deze activiteit kunt u het resultaat van uw workflow opslaan in een nieuw publiek.

   Voor meer informatie over hoe te om activiteiten in het canvas van het samenstellingswerkschema te vormen, verwijs naar [Werken met het compositicanvas](composition-canvas.md).

1. Open de compositieeigenschappen om een titel en een beschrijving op te geven.

   Als er geen titel in de eigenschappen is gedefinieerd, wordt het label van de compositie ingesteld op &quot;Compositie&quot;, gevolgd door de aanmaakdatum en -tijd.

   ![](assets/audiences-properties.png)

1. Vorm uw samenstelling door zo vele activiteiten toe te voegen zoals nodig tussen **[!UICONTROL Audience]** en **[!UICONTROL Save]** activiteiten. [Leer hoe u met het compositicanvas werkt](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Zodra uw samenstelling klaar is, klik **[!UICONTROL Publish]** om de compositie te publiceren en het resulterende publiek op te slaan in Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >U kunt maximaal 10 composities publiceren in een bepaalde sandbox. Als u deze drempel hebt bereikt, moet u een samenstelling schrappen om ruimte vrij te maken en nieuwe te publiceren.

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

![](assets/audiences-compositions.png)

>[!NOTE]
>
>U kunt een bestaande compositie op elk gewenst moment dupliceren of verwijderen met de knop voor weglatingen in de lijst.
