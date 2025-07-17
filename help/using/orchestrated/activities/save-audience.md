---
solution: Journey Optimizer
product: journey optimizer
title: De publieksactiviteit Opslaan gebruiken
description: Leer hoe u de publieksactiviteit Opslaan in een georkestreerde campagne gebruikt
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Doelgroep opslaan {#save-audience}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul><br/><br/>[ toegang en beheer georkestreerde campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen om een georkestreerde campagne ](../gs-campaign-creation.md)<br/><br/>[ tot stand te brengen en te plannen de campagne ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) te controleren | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) sparen publiek <b>[ - ](save-audience.md)</b> Gesplitst [ - ](split.md) wacht [&#128279;](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

De **[!UICONTROL Save audience]** -activiteit is een **[!UICONTROL Targeting]** -activiteit waarmee u een bestaand publiek kunt bijwerken of een nieuw publiek kunt maken van de bevolking die eerder in de georkestreerde campagne is gegenereerd. Wanneer deze doelgroepen zijn gemaakt, worden ze toegevoegd aan de lijst met doelgroepen van toepassingen en zijn ze toegankelijk via het menu **[!UICONTROL Audiences]** .

Deze activiteit is bijzonder nuttig om publiekssegmenten te bewaren die binnen de zelfde georkestreerde campagne worden berekend, die hen ter beschikking stellen voor hergebruik in toekomstige campagnes. Het is doorgaans verbonden met andere doelactiviteiten, zoals **[!UICONTROL Build audience]** of **[!UICONTROL Combine]** , om de resulterende populatie vast te leggen en op te slaan.

## Vorm sparen publieksactiviteit {#save-audience-configuration}

Voer de volgende stappen uit om de **[!UICONTROL Save audience]** -activiteit te configureren:

1. Voeg een **[!UICONTROL Save audience]** activiteit aan uw georkestreerde campagne toe.

1. Voer een **[!UICONTROL Audience label]** in die het opgeslagen publiek identificeert.

1. Klik op **[!UICONTROL Add audience attribute]** om te definiëren hoe de publieksgegevens worden gestructureerd en opgeslagen voor toekomstig hergebruik.

   ![](../assets/save-audience-1.png)

1. Selecteer vervolgens de juiste **[!UICONTROL Primary identity field]** &#x200B; en **[!UICONTROL Identity namespace]** voor een nauwkeurige profielresolutie.

   ![](../assets/save-audience-2.png)

1. Voltooi uw installatie door de georkestreerde campagne op te slaan en te publiceren. Hierdoor wordt uw publiek gegenereerd en opgeslagen.

De inhoud van het opgeslagen publiek is vervolgens beschikbaar in de gedetailleerde weergave van het publiek, die u kunt openen via het menu **[!UICONTROL Audiences]** .

![](../assets/save-audience-3.png)

## Voorbeeld {#save-audience-example}

In het volgende voorbeeld ziet u hoe u een eenvoudig publiek kunt maken door doelframes in te stellen. Een query identificeert alle profielen die een aankoop hebben gedaan in de afgelopen 30 dagen. De **[!UICONTROL Save audience]** -activiteit legt deze profielen vervolgens vast om een herbruikbaar publiek van recente kopers te maken.

![](../assets/save-audience-4.png)
