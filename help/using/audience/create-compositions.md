---
solution: Journey Optimizer
product: journey optimizer
title: Uw eerste compositieworkflow maken
description: Leer hoe u samenstellingsworkflows maakt om bestaande soorten publiek te combineren en te rangschikken.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 01c14590fe55d8f11c1ff2b18141933b0b3dd5ca
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Uw eerste compositieworkflow maken {#create-compositions}

>[!BEGINSHADEBOX]

Deze documentatie bevat gedetailleerde informatie over het werken met de compositie van het publiek in Adobe Journey Optimizer. Als u Adobe Journey Optimizer niet gebruikt, [klik hier](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html){target="_blank"}.

>[!ENDSHADEBOX]

## Een compositieworkflow maken {#create}

Ga als volgt te werk om een compositieworkflow te maken:

1. Toegang krijgen tot de **[!UICONTROL Audiences]** en selecteert u **[!UICONTROL Create Audience]**.

1. Selecteer **[!UICONTROL Compose Audience]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >De **[!UICONTROL Build rule]** Met de methode waarmee u een nieuw segment kunt maken, kunt u [Segmenteringsservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

1. Het compositicanvas wordt weergegeven met twee standaardactiviteiten:

   * **[!UICONTROL Audience]**: het beginpunt van de compositie. Met deze activiteit kunt u een of meer soorten publiek selecteren als basis voor uw workflow.

   * **[!UICONTROL Save]**: de laatste stap van uw compositie. Met deze activiteit kunt u het resultaat van uw workflow opslaan in een nieuw publiek.

   Voor meer informatie over hoe te om activiteiten in het canvas van het samenstellingswerkschema te vormen, verwijs naar [Werken met het compositicanvas](composition-canvas.md).

1. Open de compositieeigenschappen om een titel en een beschrijving op te geven.

   Als er geen titel in de eigenschappen is gedefinieerd, wordt het label van de compositie ingesteld op &quot;Compositie&quot;, gevolgd door de aanmaakdatum en -tijd.

   ![](assets/audiences-properties.png)

1. Vorm uw samenstelling door zoveel activiteiten toe te voegen zoals nodig tussen **[!UICONTROL Audience]** en **[!UICONTROL Save]** activiteiten. [Leer hoe u met het compositicanvas werkt](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Zodra uw samenstelling klaar is, klik **[!UICONTROL Publish]** om de compositie te publiceren en het resulterende publiek op te slaan in Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >U kunt maximaal 10 composities publiceren in een bepaalde sandbox. Als u deze drempel hebt bereikt, moet u een samenstelling schrappen om ruimte vrij te maken en nieuwe te publiceren.

   Als er tijdens het publiceren een fout optreedt, worden waarschuwingen weergegeven met informatie over hoe u het probleem kunt oplossen.

   ![](assets/audiences-alerts.png)

1. De compositie wordt gepubliceerd. Het resulterende publiek wordt opgeslagen in Adobe Experience Platform en is klaar om op Journey Optimizer te worden gericht. [Leer hoe u doelgroepen kunt maken in Journey Optimizer](../audience/about-audiences.md#segments-in-journey-optimizer)

## Toegang tot composities {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publish je publiek"
>abstract="Publish uw compositie om de resulterende groep(en) op te slaan in Adobe Experience Platform."

Alle gemaakte composities zijn toegankelijk via de **[!UICONTROL Compositions]** tab. U kunt een bestaande compositie op elk gewenst moment dupliceren of verwijderen met de knop voor weglatingen in de lijst.

Composities kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: de samenstelling is in uitvoering en is niet gepubliceerd.
* **[!UICONTROL Published]**: de compositie is gepubliceerd, het resulterende publiek is opgeslagen en beschikbaar voor gebruik.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>De compositie van het publiek is momenteel niet geïntegreerd met de functie voor het opnieuw instellen van de sandbox. Voordat u een sandbox-reset start, moet u de composities handmatig verwijderen om ervoor te zorgen dat de bijbehorende publieksgegevens op de juiste wijze worden opgeschoond. Gedetailleerde informatie is beschikbaar in Adobe Experience Platform [Sandbox-documentatie](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html#delete-audience-compositions)
