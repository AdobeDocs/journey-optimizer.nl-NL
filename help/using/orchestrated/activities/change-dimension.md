---
solution: Journey Optimizer
product: journey optimizer
title: De activiteit Dimensie wijzigen gebruiken
description: Leer hoe u de activiteit Dimensie wijzigen gebruikt
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---


# Dimensie wijzigen {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Een complement genereren"
>abstract="U kunt een extra uitgaande overgang met de resterende bevolking produceren, die als duplicaat werd uitgesloten. Om dit te doen, op **van een knevel voorzien produceer complement** optie"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Dimensieactiviteit wijzigen"
>abstract="Met deze activiteit kunt u de doeldimensie wijzigen terwijl u een publiek maakt. Het verschuift de as afhankelijk van het gegevensmalplaatje en de inputdimensie. U kunt bijvoorbeeld van de dimensie &quot;contracten&quot; naar de dimensie &quot;clients&quot; schakelen."

Als markator, kunt u publiek richten verbeteren door van één gegevensentiteit aan verwante binnen een Geordende campagne te verschuiven. Op deze manier kunt u verder gaan dan gebruikersprofielen en zich richten op specifieke gedragingen, zoals aankopen, boekingen of andere interacties.

Gebruik hiervoor de **[!UICONTROL Change dimension]** -activiteit. Hiermee kunt u de doeldimensie tijdens de geordende campagne aanpassen.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Vorm de de afmetingsactiviteit van de Verandering {#configure}

Voer de volgende stappen uit om de **[!UICONTROL Change dimension]** -activiteit te configureren:

1. Voeg een **[!UICONTROL Change dimension]** activiteit aan uw Geordende campagne toe.

   ![](../assets/orchestrated-change-dimension.png)

1. Definieer de **[!UICONTROL New target dimension]** . Tijdens het wijzigen van de afmetingen worden alle records bewaard.


## Voorbeeld {#example}

Deze gebruikscase richt zich op het verzenden van SMS naar profielen die een verlanglijst binnen de afgelopen maand hebben gecreeerd.

Begin met een **[!UICONTROL Build audience]** -activiteit en gebruik de **[!UICONTROL Wishlist]** -dimensie om alle relevante wenslijsten te identificeren.

Voeg vervolgens een **[!UICONTROL Change dimension]** -activiteit toe om de doeldimensie te wijzigen van **[!UICONTROL Wishlist]** in **[!UICONTROL Recipient].** Deze stap zorgt ervoor dat de geordende campagne zich richt op de juiste profielen die aan deze wenslijsten zijn gekoppeld, zodat het SMS naar de bedoelde profielen kan worden verzonden.

![](../assets/orchestrated-change-dimension-example.png)
