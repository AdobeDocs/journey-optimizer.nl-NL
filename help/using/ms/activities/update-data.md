---
solution: Journey Optimizer
product: journey optimizer
title: Gebruik de gegevensactiviteit van de Update in uw multi-step campagnes
description: Leer hoe u de gegevensactiviteit Bijwerken gebruikt
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
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

Om de **gegevens van de Update** activiteit te vormen, begin door de activiteit aan uw multi-step campagne toe te voegen en een etiket te bepalen.

![](../assets/workflow-update-data.png)

### Type bewerking

Het **type van Verrichting** gebied laat u het proces kiezen dat op de gegevens in het gegevensbestand moet worden uitgevoerd:

* **Tussenvoegsel of update**: neem gegevens op of werk het bij als de verslagen reeds in het gegevensbestand bestaan.
* **Tussenvoegsel**: neem slechts gegevens op. De al bestaande records worden niet bijgewerkt. Als er afstemmingscriteria worden gedefinieerd, worden alleen de niet-afgestemde records toegevoegd.
* **Update**: werk gegevens van de verslagen bij die reeds in het gegevensbestand slechts bestaan.
* **Schrapping**: schrap gegevens.

Het **gebied van de Partij** laat u het aantal binnenkomende overgangselementen selecteren die moeten worden bijgewerkt. Als u bijvoorbeeld 500 opgeeft, worden de eerste 500 records die worden afgehandeld, bijgewerkt.

### Registeridentificatie

In deze sectie kunt u opgeven hoe de records in de database moeten worden geïdentificeerd:

* Als de gegevensingangen op bestaand richten afmeting betrekking hebben, selecteer **Gebruikend de het richten afmeting** optie en selecteer het van in **het richten afmeting om** gebied bij te werken.
* U kunt **ook selecteren Gebruikend douaneverbindingen** en één of meerdere verbindingen specificeren die identificatie van de gegevens in het gegevensbestand zullen toelaten
* Als het geselecteerde verrichtingstype een update vereist, moet u **gebruiken Gebruikend verzoeningsregels** optie.

### Bij te werken velden

In de **Velden om** sectie bij te werken, voeg de gebieden toe waarop de update zal worden toegepast en, indien nodig, voeg voorwaarden toe zodat deze update wordt uitgevoerd. Om dit te doen, gebruik **in aanmerking genomen als** gebied. De voorwaarden worden een na een toegepast in de volgorde van de lijst. Gebruik de pijlen aan de rechterkant om de volgorde van de updates te wijzigen. U kunt hetzelfde bestemmingsveld meerdere keren gebruiken.

U kunt gebieden automatisch verbinden gebruikend de **auto-afbeelding** knoop. Door automatische koppeling worden velden met dezelfde naam gedetecteerd.

Tijdens **Tussenvoegsel of werk** verrichtingstype bij, kunt u de verrichting individueel selecteren om voor elk gebied van toepassing te zijn. Om dit te doen, selecteer de waarde u op het **type van Verrichting** gebied zou willen.

### Geavanceerde opties

De **Geavanceerde opties** laten u extra opties specificeren om het bijwerken van gegevens evenals het beheren van duplicaten te behandelen.

<!--
* **Disable automatic key management**
* **Disable audit**
* **Empty the destination value if the source value is empty**
* **Update all columns with matching names**
* **Ignore records which concern the same target**: only the first in the list of expressions will be considered
-->

Met de laatste twee opties kunt u specifieke handelingen uitvoeren:

* **produceer een uitgaande overgang**: leidt tot een uitgaande overgang die aan het eind van uitvoering zal worden geactiveerd. Het bijwerken signaleert gewoonlijk het eind van een het richten multi-step campagne, en de optie wordt daarom niet door gebrek geactiveerd.

* **produceer een uitgaande overgang voor verwerpt**: leidt tot een uitgaande overgang die verslagen bevatten die niet correct na de update (bijvoorbeeld als er een dubbel is) zijn verwerkt. De update markeert over het algemeen het einde van een doelcampagne met meerdere stappen en daarom wordt de optie niet standaard geactiveerd.
