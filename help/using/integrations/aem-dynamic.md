---
solution: Journey Optimizer
product: journey optimizer
title: Dynamische media
description: Dynamische media gebruiken met Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: 3e777cc5-a935-4e68-9de7-60b241e78f63
source-git-commit: 3a10f8440515bd569f9def6d15ac74d57427c1cf
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Werken met dynamische media {#aem-dynamic}

>[!AVAILABILITY]
>
>Deze integratie is uitsluitend beschikbaar voor klanten die Dynamic Media Manager as a Cloud Service gebruiken.

De Asset-kiezer ondersteunt nu Dynamische media waarmee u goedgekeurde dynamische media-uitvoeringen naadloos kunt selecteren en gebruiken in Journey Optimizer. Wijzigingen die u aanbrengt in elementen in Adobe Experience Manager, worden direct weerspiegeld in uw Journey Optimizer-inhoud. Zo weet u zeker dat de meest actuele versies altijd worden gebruikt zonder dat u handmatige updates hoeft uit te voeren.

Meer op Dynamische Media in Adobe Experience Manager as a Cloud Service leren, verwijs naar [ documentatie van Experience Manager ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media).

## Dynamische media toevoegen en beheren

Verbeter en optimaliseer uw inhoud voor om het even welk scherm of browser door dynamische media van Adobe Experience Manager as a Cloud Service direct in uw inhoud van Journey Optimizer op te nemen.  Vervolgens kunt u het formaat van de aanpassingen desgewenst aanpassen, uitsnijden, verbeteren en andere aanpassingen aanbrengen.

1. Sleep een **[!UICONTROL HTML component]** naar de inhoud.

1. Selecteer **[!UICONTROL Show the source code]**.

   ![](assets/dynamic-media-1.png)

1. Navigeer in het menu **[!UICONTROL Edit HTML]** naar **[!UICONTROL Assets]** en klik vervolgens op **[!UICONTROL Open asset selector]** .

   U kunt ook de URL van het element kopiëren en plakken.

   ![](assets/dynamic-media-2.png)

1. Blader door uw AEM-middelen en selecteer de middelen die u aan uw inhoud wilt toevoegen.

1. Pas de afbeeldingsparameters (bijv. hoogte, breedte, roteren, spiegelen, helderheid, kleurtoon, enz.) naar wens aan de vereisten voor het element aan.

   Voor een uitvoerige lijst van beeldparameters die aan URL kunnen worden toegevoegd, verwijs naar [ documentatie van Experience Manager ](https://experienceleague.adobe.com/en/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/c-command-reference).

   ![](assets/dynamic-media-3.png)

1. Klik op **[!UICONTROL Save]**.

Uw inhoud bevat nu dynamische media. Alle updates die u aanbrengt in Experience Manager, worden automatisch weergegeven in Journey Optimizer.

## Uw tekstbedekking aanpassen

U kunt alle dynamische media eenvoudig aanpassen door de bestaande tekstbedekking te vervangen door nieuwe tekst van uw keuze, zodat u naadloze updates en personalisatie kunt uitvoeren.

Met de experimentatiefunctie kunt u bijvoorbeeld de bestaande tekstbedekking bijwerken door deze te vervangen door een andere tekst voor elke behandeling, zodat deze voor elk profiel wordt aangepast wanneer de berichten worden geopend.

![](assets/dynamic-media-layout-1.png)

1. Sleep een **[!UICONTROL HTML component]** naar de inhoud.

1. Selecteer **[!UICONTROL Show the source code]**.

1. Open **[!UICONTROL Assets]** then **[!UICONTROL Open asset selector]** via het menu **[!UICONTROL Edit HTML]** .

   U kunt ook gewoon de URL van uw elementen kopiëren en plakken.

1. Blader door uw AEM-elementen en selecteer de element die u aan uw inhoud wilt toevoegen.

1. Vervang de bedekking door de gewenste tekst.

   ![](assets/do-not-localize/dynamic_media_layout.gif)

1. Werk de afbeeldingsparameters bij:

   * **Laag**: ga het basiselement in waar uw tekst wordt geplaatst.
   * **Grootte**: werk de grootte van uw tekstblok bij.
   * **TextAttr**: pas de grootte van uw tekstdoopvont aan.
   * **Pos**: plaats de positie van uw tekst in het beeld.

   >[!WARNING]
   >
   >De parameter van de Laag wordt vereist om uw dynamische media bij te werken.

   ![](assets/dynamic-media-layout-2.png)

1. Klik op **[!UICONTROL Save]**.

Uw inhoud bevat nu uw bijgewerkte tekstbedekking.

![](assets/dynamic-media-layout-3.png)

<!--
## Personalization with Text Overlay

Easily customize any dynamic media by replacing the existing text overlay with new text of your choice, allowing for seamless updates and personalization.

In this example, our goal is to update the existing text overlay by replacing it with a new validity date and adding a personalization block, ensuring it is customized for each profile when they open their messages.

1. Drag and drop an **[!UICONTROL HTML component]** into your content.

1. Select **[!UICONTROL Show the source code]**.

1. From the **[!UICONTROL Edit HTML]** menu, access **[!UICONTROL Assets]** then **[!UICONTROL Open asset selector]**.

    You can also simply copy and paste your assets URL.

1. Browse through your AEM assets and select the one you want to add to your content.

1. Replace the overlay with the desired text.

    Here we change the validity date from 31st December 2024 to the 1st July 2025.

1. Add the required personalization fields to your image.

1. Click **[!UICONTROL Save]**.

Your content now includes your updated text overlay and personalization.

## Add Dynamic media conditional content

Enable conditional content in your dynamic media to better target your audience and deliver a more personalized experience.

1. Drag and drop an **[!UICONTROL HTML component]** into your content.

1. Select **[!UICONTROL Show the source code]**.

1. From the **[!UICONTROL Edit HTML]** menu, access **[!UICONTROL Assets]** then **[!UICONTROL Open asset selector]**.

    You can also simply copy and paste your assets URL.

1. Browse through your AEM assets and select the one you want to add to your content.

1. Once your dynamic media is inserted to your content, select **[!UICONTROL Enable conditional]** content from your HTML component toolbar to create your different user experiences. 

1. From the Variant - 1, click **[!UICONTROL Select condition]** to fine tune your audience.

1. Choose your condition or create a new one if needed and click **[!UICONTROL Select]**.

    [Learn more on conditions](../personalization/create-conditions.md)

1. Select your **[!UICONTROL Component]** and access the **[!UICONTROL Settings]** menu.

1. In the **[!UICONTROL Custom Attributes]** menu, populate the Dynamic Media text and personalization fields to customize the content for your audience.

-->
