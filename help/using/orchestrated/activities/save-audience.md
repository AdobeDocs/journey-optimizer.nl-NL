---
solution: Journey Optimizer
product: journey optimizer
title: De publieksactiviteit Opslaan gebruiken
description: Leer hoe u de publieksactiviteit Opslaan in een geordende campagne gebruikt
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: 458e0b19725147e0a3ad34891ca55b61f1ac44a8
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Doelgroep opslaan {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Activiteit van publiek opslaan"
>abstract="**sparen publiek** activiteit is a **richtend** activiteit die u toestaat om een bestaand publiek bij te werken of nieuwe te creëren van de bevolking die vroeger in de Geordende campagne wordt geproduceerd. Zodra gecreeerd, worden deze publiek toegevoegd aan de lijst van toepassingspubliek en kan van het **Publiek** menu worden betreden."


+++ Inhoudsopgave

| Welkom bij Geordende campagnes | Start uw eerste geordende campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met Geordende campagnes ](../gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](../gs-schemas.md)</li><li>[ Handmatig schema ](../manual-schema.md)</li><li>[ het uploadschema van het Dossier ](../file-upload-schema.md)</li><li>[ Ingest gegevens ](../ingest-data.md)</li></ul>[ toegang en beheer Geordende campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen om een Geordende campagne ](../gs-campaign-creation.md)<br/><br/>[ tot stand te brengen en de campagne te plannen ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) te controleren | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) sparen publiek <b>[ - ](save-audience.md)</b> Gesplitst [ - ](split.md) wacht [](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

De **[!UICONTROL Save audience]** -activiteit is een **[!UICONTROL Targeting]** -activiteit die wordt gebruikt om een nieuw publiek te maken of om een bestaand publiek bij te werken op basis van de bevolking die eerder in de geordende campagne is gegenereerd. Nadat het publiek is opgeslagen, wordt het toegevoegd aan de lijst met doelgroepen van de toepassing en wordt het toegankelijk via het menu **[!UICONTROL Audiences]** .

Het wordt doorgaans gebruikt om publiekssegmenten vast te leggen die in dezelfde campagne zijn gemaakt, zodat deze beschikbaar zijn voor hergebruik in toekomstige campagnes. Doorgaans is dit gekoppeld aan andere doelactiviteiten, zoals **[!UICONTROL Build audience]** of **[!UICONTROL Combine]** , om de uiteindelijke doelpopulatie te besparen.

## Vorm sparen publieksactiviteit {#save-audience-configuration}

Voer de volgende stappen uit om de **[!UICONTROL Save audience]** -activiteit te configureren:

1. Voeg een **[!UICONTROL Save audience]** activiteit aan uw Geordende campagne toe.

1. Voer een **[!UICONTROL Audience label]** in die het opgeslagen publiek identificeert.

1. Kies een **[!UICONTROL Profile mapping field&#x200B;]** optie in de doeldimensie van uw campagne.

   ➡️ [ volg de stappen in deze pagina worden gedetailleerd om uw Campagne te creëren richtend afmeting ](../target-dimension.md)

   ![](../assets/save-audience-1.png)

1. Klik op **[!UICONTROL Add audience mappings]** als u het opgeslagen publiek wilt koppelen aan extra identiteitsvelden.

   ![](../assets/save-audience-2.png)

1. Voltooi uw opstelling door de Geordende campagne te bewaren en te publiceren. Hierdoor wordt uw publiek gegenereerd en opgeslagen.

De inhoud van het opgeslagen publiek is dan beschikbaar in de detailweergave van het publiek, die toegankelijk is via het menu **[!UICONTROL Audiences]** , of kan worden geselecteerd wanneer het doel wordt ingesteld op een publiek, bijvoorbeeld met een **[!UICONTROL Read audience]** -activiteit.

![](../assets/save-audience-4.png)


## Voorbeeld {#save-audience-example}

In het volgende voorbeeld ziet u hoe u een eenvoudig publiek kunt maken door doelframes in te stellen. Een vraag identificeert alle ontvangers die een reis in de laatste 30 dagen door deze bevolking binnen uw Geordende campagne te filtreren boekten. Door **Ontvangers te kiezen - CRMID** als **het richten dimensie**, richt het publiek elke individuele het boeken gebeurtenis eerder dan enkel de ontvanger als geheel. De **[!UICONTROL Save audience]** -activiteit legt deze profielen vervolgens vast om een herbruikbaar publiek van recente kopers te maken.

![](../assets/save-audience-3.png)
