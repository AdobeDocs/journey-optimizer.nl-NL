---
solution: Journey Optimizer
product: journey optimizer
title: De publieksactiviteit Opslaan gebruiken
description: Leer hoe u de publieksactiviteit Opslaan in een georkestreerde campagne gebruikt
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: 81f0338935ee36b152963f2b1c0e7989b86f5f8a
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# Doelgroep opslaan {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Activiteit van publiek opslaan"
>abstract="**sparen publiek** activiteit is a **richtend** activiteit die u toestaat om een bestaand publiek bij te werken of nieuwe te creëren van de bevolking die vroeger in de georkestreerde campagne wordt geproduceerd. Zodra gecreeerd, worden deze publiek toegevoegd aan de lijst van toepassingspubliek en kan van het **Publiek** menu worden betreden."


+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](../gs-schemas.md)</li><li>[ Handmatig schema ](../manual-schema.md)</li><li>[ het uploadschema van het Dossier ](../file-upload-schema.md)</li><li>[ Ingest gegevens ](../ingest-data.md)</li></ul>[ toegang en beheer georkestreerde campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen om een georkestreerde campagne ](../gs-campaign-creation.md)<br/><br/>[ tot stand te brengen en te plannen de campagne ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) te controleren | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) sparen publiek <b>[ - ](save-audience.md)</b> Gesplitst [ - ](split.md) wacht [&#128279;](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

De **[!UICONTROL Save audience]** -activiteit is een **[!UICONTROL Targeting]** -activiteit die wordt gebruikt om een nieuw publiek te maken of om een bestaand publiek bij te werken op basis van de bevolking die eerder in de georkestreerde campagne is gegenereerd. Nadat het publiek is opgeslagen, wordt het toegevoegd aan de lijst met doelgroepen van de toepassing en wordt het toegankelijk via het menu **[!UICONTROL Audiences]** .

Het wordt doorgaans gebruikt om publiekssegmenten vast te leggen die zijn gemaakt in dezelfde campagneworkflow en deze beschikbaar te maken voor hergebruik in toekomstige campagnes. Doorgaans is dit gekoppeld aan andere doelactiviteiten, zoals **[!UICONTROL Build audience]** of **[!UICONTROL Combine]** , om de uiteindelijke doelpopulatie te besparen.

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
