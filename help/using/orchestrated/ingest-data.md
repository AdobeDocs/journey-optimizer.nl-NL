---
solution: Journey Optimizer
product: journey optimizer
title: Configuratiestappen
description: Leer hoe u gegevens van ondersteunde bronnen, zoals SFTP, cloudopslag of databases, naar Adobe Experience Platform kunt overbrengen.
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: ea5ef4005be90973046d3f94ea4c2b92eb89ffb4
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Samenvattingsgegevens {#ingest-data}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets </br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](gs-schemas.md)</li><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul>[ toegang en beheer georkestreerde campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Zeer belangrijke stappen om een georkestreerde campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [&#128279;](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

De inhoud

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

Adobe Experience Platform staat toe dat gegevens uit externe bronnen worden opgenomen en biedt u de mogelijkheid om inkomende gegevens te structureren, labelen en verbeteren met behulp van Experience Platform-services. U kunt gegevens invoeren uit verschillende bronnen, zoals Adobe-toepassingen, opslag in de cloud, databases en vele andere.

## Met cloudopslag {#ingest}

<!--
>[!IMPORTANT]
>
>Each dataset in Adobe Experience Platform supports only one active dataflow at a time. For detailed setup guidance on how to switch data sources, refer to this [section](#cdc-ingestion).
-->

U kunt een gegevensstroom vormen om gegevens van een bron van Amazon S3 in Adobe Experience Platform in te voeren. Zodra gevormd, laat de gegevensstroom geautomatiseerde, geplande opname van gestructureerde gegevens toe en steunt updates in real time.

1. Via het menu **[!UICONTROL Connections]** opent u het menu **[!UICONTROL Sources]** .

1. Selecteer de categorie **[!UICONTROL Cloud storage]** , vervolgens Amazon S3 en klik op **[!UICONTROL Add Data]** .

   ![](assets/admin_sources_1.png)

1. Sluit uw S3-account aan:

   * Met een bestaande account

   * Met een nieuwe account

   [ leer meer in de documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#connect)

   ![](assets/admin_sources_2.png)

1. Kies uw map **[!UICONTROL Data format]** , **[!UICONTROL Delimiter]** en **[!UICONTROL Compression type]** .

1. Navigeer door de verbonden S3 bron tot u van de twee die omslagen de plaats bepalen vroeger worden gecreeerd d.w.z. **loyaliteitbeloningen** en **loyaliteitstransacties**.

1. Selecteer de map die uw gegevens bevat.

   Als u een map selecteert, worden alle huidige en toekomstige bestanden met dezelfde structuur automatisch verwerkt. Als u één bestand selecteert, moet u echter elke nieuwe gegevensstap handmatig uploaden.

   ![](assets/S3_config_2.png)

1. Kies uw map **[!UICONTROL Data format]** , **[!UICONTROL Delimiter]** en **[!UICONTROL Compression type]** . Controleer de voorbeeldgegevens op nauwkeurigheid en klik op **[!UICONTROL Next]** .

   ![](assets/S3_config_1.png)

1. Schakel **[!UICONTROL Enable Change data capture]** in om een keuze te maken uit gegevenssets die zijn toegewezen aan relationele schema&#39;s en waarvoor zowel een primaire sleutel als een versiedescriptor zijn gedefinieerd.

1. Selecteer uw [ eerder gecreeerd Dataset ](#entities) en klik **[!UICONTROL Next]**.

   ![](assets/S3_config_3.png)

1. Controleer in het venster **[!UICONTROL Mapping]** of elk kenmerk van het bronbestand correct is toegewezen aan de corresponderende velden in het doelschema.

   Klik **[!UICONTROL Next]** eenmaal gereed.

   ![](assets/S3_config_4.png)

1. Configureer de gegevensstroom **[!UICONTROL Schedule]** op basis van de gewenste frequentie.

1. Klik op **[!UICONTROL Finish]** om de gegevensstroom te maken. Deze wordt automatisch uitgevoerd volgens het gedefinieerde schema.

1. Selecteer **[!UICONTROL Connections]** in het menu **[!UICONTROL Sources]** en open het tabblad **[!UICONTROL Data Flows]** om de uitvoering van de flow bij te houden, ingesloten records te controleren en eventuele fouten op te lossen.

   ![](assets/S3_config_5.png)

<!--### Setting Up Change data capture ingestion {#cdc-ingestion}

If you need to change the data source, you must delete the existing dataflow and create a new one pointing to the same dataset with the new source.

When using Change Data Capture (CDC), it is essential that the source and dataset remain in sync to ensure accurate incremental updates. Follow the steps below:

1. **Schema Requirements**
   - Your schema must include:
     - A **primary key** (e.g., `transaction_id`)
     - A **versioning field** (e.g., `lastmodified` or an incrementing `version_id`)
   - Enable the dataset for **Orchestrated Campaigns** if needed.

2. **CDC Dataflow Setup**
   - During dataflow creation, after choosing your source and files:
     - **Enable the CDC option**
     - Select your CDC-ready dataset
     - Confirm field mappings (especially version field)

3. **Keep Source and Target in Sync**
   - The source system must consistently update the version field so the platform can detect changes accurately.

Once set up, the platform will automatically ingest **only changed or new records** each time the flow runs.
-->