---
solution: Journey Optimizer
product: journey optimizer
title: Use the Update data activity in your orchestrated campaigns
description: Learn how to use the Update data activity
hide: true
hidefromtoc: true
exl-id: 68e7c929-5f07-4d5a-9831-690e071947f8
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 12%

---

# Gegevens bijwerken {#update-data}

De **gegevens van de Update** activiteit is a **het Beheer van Gegevens** activiteit. Hiermee kunt u een massale update uitvoeren op velden in de database. Met verschillende opties kunt u de gegevensupdate aanpassen.

<!--
The **Operation type** field lets you choose the process to be carried out on the data in the database. Select the first option to add data or update (it if it has already been added). You can also only add data, only update data, or delete data. Select the **Update and merge collections** to select a primary record to link duplicates to, and delete those duplicates safely

Specify how to identify the records in the database: if data relate to an existing targeting dimension, select the **Using the targeting dimension** option and select the targeting dimension and fields to update. Otherwise, specify one or more custom links to identify the data in the database, or direct use of reconciliation keys.

Select the fields to update and reconciliation settings. You can use the **Auto-mapping** option to automatically identify the fields to be updated.

The **Advanced options** section let you specify additional settings to manage data and duplicates.

Toggle the **Generate an outbound transition** option to add an outbound transition that will be activated at the end of the execution of the **Update data** activity. The update generally marks the end of a targeting workflow and therefore the option is not activated by default.

Toggle the **Generate an outbound transition for rejects** option to add an outbound transition containing records that have not been correctly processed after the update (for example if there is a duplicate). The update generally marks the end of a targeting workflow and therefore the option is not activated by default.
-->

## De updategegevensactiviteit configureren{#update-data-configuration}

To configure the **Update data** activity, start by adding the activity to your orchestrated campaign and define a label.

![](../assets/workflow-update-data.png)

### Type bewerking

Het **type van Verrichting** gebied laat u het proces kiezen dat op de gegevens in het gegevensbestand moet worden uitgevoerd:

* **Insert or update**: insert data or update it if the records already exist in the database.
* **Insert**: insert data only. De al bestaande records worden niet bijgewerkt. Als er afstemmingscriteria worden gedefinieerd, worden alleen de niet-afgestemde records toegevoegd.
* **Update**: update data of the records that already exist in the database only.
* **Schrapping**: schrap gegevens.

Het **gebied van de Partij** laat u het aantal binnenkomende overgangselementen selecteren die moeten worden bijgewerkt. Als u bijvoorbeeld 500 opgeeft, worden de eerste 500 records die worden afgehandeld, bijgewerkt.

### Registeridentificatie

In deze sectie kunt u opgeven hoe de records in de database moeten worden geïdentificeerd:

* If data entries relate to an existing targeting dimension, select the **Using the targeting dimension** option and select it from in the **Targeting dimension to update** field.
* You can also select the **Using custom links** and specify one or more links which will enable identification of the data in the database
* If the operation type selected requires an update, you must use the **Using reconciliation rules** option.

### Bij te werken velden

In the **Fields to update** section, add the fields on which the update will be applied and, if necessary, add conditions so that this update is carried out. To do this, use the **Taken into account if** field. De voorwaarden worden een na een toegepast in de volgorde van de lijst. Gebruik de pijlen aan de rechterkant om de volgorde van de updates te wijzigen. U kunt hetzelfde bestemmingsveld meerdere keren gebruiken.

U kunt gebieden automatisch verbinden gebruikend de **auto-afbeelding** knoop. Door automatische koppeling worden velden met dezelfde naam gedetecteerd.

Tijdens **Tussenvoegsel of werk** verrichtingstype bij, kunt u de verrichting individueel selecteren om voor elk gebied van toepassing te zijn. To do this, select the value you would like in the **Operation type** field.

### Geavanceerde opties

The **Advanced options** lets you specify additional options to deal with updating data as well as managing duplicates.

<!--
* **Disable automatic key management**
* **Disable audit**
* **Empty the destination value if the source value is empty**
* **Update all columns with matching names**
* **Ignore records which concern the same target**: only the first in the list of expressions will be considered
-->

Met de laatste twee opties kunt u specifieke handelingen uitvoeren:

* **Generate an outbound transition**: creates an outbound transition that will be activated at the end of execution. Updating usually signals the end of a targeting orchestrated campaign, and the option is therefore not activated by default.

* **Generate an outbound transition for the rejects**: creates an outbound transition containing records that have not been correctly processed after the update (for example if there is a duplicate). The update generally marks the end of a targeting orchestrated campaign and therefore the option is not activated by default.
