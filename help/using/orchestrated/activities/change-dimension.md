---
solution: Journey Optimizer
product: journey optimizer
title: De activiteit Dimensie wijzigen gebruiken
description: Leer hoe u de activiteit Dimensie wijzigen gebruikt
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 25120dd71159d0233783ac4c189f528ff2c93ae3
workflow-type: tm+mt
source-wordcount: '354'
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

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ Handmatig schema ](../manual-schema.md)</li><li>[ het uploadschema van het Dossier ](../file-upload-schema.md)</li><li>[ Ingest gegevens ](../ingest-data.md)</li></ul>[ toegang en beheer georkestreerde campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen om een georkestreerde campagne ](../gs-campaign-creation.md)<br/><br/>[ tot stand te brengen en te plannen de campagne ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) te controleren | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - <b>[ dimensie van de Verandering ](change-dimension.md)</b> - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) sparen publiek [ - ](save-audience.md) Gesplitst [ - ](split.md) wacht [](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

Als markator, kunt u publiek richten verbeteren door van één gegevensentiteit aan verwante binnen een georkestreerde campagne te verschuiven. Op deze manier kunt u verder gaan dan gebruikersprofielen en zich richten op specifieke gedragingen, zoals aankopen, boekingen of andere interacties.

Gebruik hiervoor de **[!UICONTROL Change dimension]** -activiteit. Hiermee kunt u de doeldimensie tijdens de georkestreerde campagne aanpassen.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Vorm de de afmetingsactiviteit van de Verandering {#configure}

Voer de volgende stappen uit om de **[!UICONTROL Change dimension]** -activiteit te configureren:

1. Voeg een **[!UICONTROL Change dimension]** activiteit aan uw georkestreerde campagne toe.

   ![](../assets/orchestrated-change-dimension.png)

1. Definieer de **[!UICONTROL New target dimension]** . Tijdens het wijzigen van de afmetingen worden alle records bewaard.


## Voorbeeld {#example}

Deze gebruikscase richt zich op het verzenden van SMS naar profielen die een verlanglijst binnen de afgelopen maand hebben gecreeerd.

Begin met een **[!UICONTROL Build audience]** -activiteit en gebruik de **[!UICONTROL Wishlist]** -dimensie om alle relevante wenslijsten te identificeren.

Voeg vervolgens een **[!UICONTROL Change dimension]** -activiteit toe om de doeldimensie te wijzigen van **[!UICONTROL Wishlist]** in **[!UICONTROL Recipient].** Deze stap zorgt ervoor dat de georkestreerde campagne zich richt op de correcte profielen verbonden aan die wenslijsten, die SMS toestaan om naar de voorgenomen profielen worden verzonden.

![](../assets/orchestrated-change-dimension-example.png)
