---
solution: Journey Optimizer
product: journey optimizer
title: Configuratiestappen
description: Leer hoe u een relationeel schema maakt in Adobe Experience Platform door een DDL te uploaden
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 3f92dc721648f822687b8efc302c40989b72b145
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 1%

---

# Bestand uploaden {#file-upload-schema}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](gs-schemas.md)</li><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul>[ toegang en beheer georkestreerde campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Zeer belangrijke stappen om een georkestreerde campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [&#128279;](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

Bepaal het relationele gegevensmodel dat voor georkestreerde campagnes wordt vereist door schema&#39;s zoals **Loyalty Membership**, **Transacties van de Loyalty**, en **Beloningen van de Loyalty** te creëren. Elk schema moet een primaire sleutel, een versieringsattribuut, en aangewezen verhoudingen omvatten om entiteiten zoals **Ontvangers** of **Merken** van verwijzingen te voorzien.

<!--
Schemas can be created manually through the interface or imported in bulk using a DDL file.

This section provides step-by-step guidance on how to create a relational schema within Adobe Experience Platform by uploading a DDL (Data Definition Language) file. Using a DDL file allows you to define the structure of your data model in advance, including tables, attributes, keys, and relationships. 

## Upload a DDL file{#ddl-upload}

By uploading a DDL file, you can define the structure of your data model in advance, including tables, attributes, keys, and relationships. 

1. Log in to Adobe Experience Platform.

1. Navigate to the **Data Management** > **Schema**.

1. Click on **Create Schema**.

1. You will be prompted to select between two schema types:

    * **Standard**
    * **Relational**, used specifically for orchestrated campaigns

    ![](assets/admin_schema_1.png)

1. Select **Upload DDL file** to define an entity relationship diagram and create schemas.

    The table structure must contain:
    * At least one primary key
    * A version identifier, such as a `lastmodified` field of type `datetime` or `number`.

1. Drag and drop your DDL file and click **[!UICONTROL Next]**.

1. Type-in your **[!UICONTROL Schema name]**.

1. Set up each schema and its columns, ensuring that a primary key is specified. 

    One attribute, such as `lastmodified`, must be designated as a version descriptor. This attribute, typically of type `datetime`, `long`, or `int`, is essential for ingestion processes to ensure that the dataset is updated with the latest data version.

    ![](assets/admin_schema_2.png)

1. Click **[!UICONTROL Done]** once done.

You can now verify the table and field definitions within the canvas. [Learn more in the section below](#entities)

## Define relationships {#relationships}

To define logical connections between tables within your schema, follow the steps below.

1. Access the canvas view of your data model and choose the two tables you want to link

1. Click the ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) button next to the Source Join, then drag and guide the arrow towards the Target Join to establish the connection.

    ![](assets/admin_schema_5.png)

1. Fill in the given form to define the link and click **Apply** once configured.

    ![](assets/admin_schema_3.png)

    **Cardinality**:

     * **1-N**: one occurrence of the source table can have several corresponding occurrences of the target table, but one occurrence of the target table can have at most one corresponding occurrence of the source table.

    * **N-1**: one occurrence of the target table can have several corresponding occurrences of the source table, but one occurrence of the source table can have at most one corresponding occurrence of the target table.

    * **1-1**: one occurrence of the source table can have at most one corresponding occurrence of the target table.

1. All links defined in your data model are represented as arrows in the canvas view. Click on an arrow between two tables to view details, make edits, or remove the link as needed.

    ![](assets/admin_schema_6.png)

1. Use the toolbar to customize and adjust your canvas.

    ![](assets/toolbar.png)

    * **Zoom in**: Magnify the canvas to see details of your data model more clearly.

    * **Zoom out**: Reduce the canvas size for a broader view of your data model.

    * **Fit view**: Adjust the zoom to fit all schemas within the visible area.

    * **Filter**: Choose which schema to display within the canvas.

    * **Force auto layout**: Automatically arrange schemas for better organization.

    * **Display map**: Toggle a minimap overlay to help navigate large or complex schema layouts more easily.

1. Click **Save** once done. This action creates the schemas and associated data sets and enables the data set for use in Orchestrated Campaigns.

1. Click **[!UICONTROL Open Jobs]** to monitor the progress of the creation job. This process may take couple minutes, depending on the number of tables defined in the DDL file. 

    ![](assets/admin_schema_4.png)

## Link schema {#link-schema}

Establish a relationship between the **loyalty transactions** schema and the **Recipients** schema to associate each transaction with the correct customer record.

1. Navigate to **[!UICONTROL Schemas]** and open your previously create **loyalty transactions**.

1. Click **[!UICONTROL Add Relationship]** from the Customer **[!UICONTROL Field properties]**.

    ![](assets/schema_1.png)

1. Select **[!UICONTROL Many-to-One]** as the relationship **[!UICONTROL Type]**.

1. Link to the existing **Recipients** schema.

    ![](assets/schema_2.png)

1. Enter a **[!UICONTROL Relationship name from current schema]** and **[!UICONTROL Relationship name from reference schema]**.

1. Click **[!UICONTROL Apply]** to save your changes.

Continue by creating a relationship between the **loyalty rewards** schema and the **Brands** schema to associate each reward entry with the appropriate brand.

![](assets/schema_3.png)

-->
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