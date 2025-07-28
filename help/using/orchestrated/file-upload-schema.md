---
solution: Journey Optimizer
product: journey optimizer
title: Configuratiestappen
description: Leer hoe u een relationeel schema maakt in Adobe Experience Platform door een DDL te uploaden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 88eb1438-0fe5-4a19-bfb6-2968a427e9e8
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 0%

---

# Relationele schema&#39;s maken met een DDL-bestand {#file-upload-schema}

+++ Inhoudsopgave

| Welkom bij Geordende campagnes | Start uw eerste geordende campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met Geordende campagnes ](gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](gs-schemas.md)</li><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul>[ toegang en beheer Geordende campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Zeer belangrijke stappen om een Geordende campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [&#128279;](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

Bepaal het relationele gegevensmodel dat voor Geordende campagnes wordt vereist door schema&#39;s zoals **Loyalty Membership**, **Transacties van de Loyalty**, en **Beloningen van de Loyalty** te creëren. Elk schema moet een primaire sleutel, een versieringsattribuut, en aangewezen verhoudingen omvatten om entiteiten zoals **Ontvangers** of **Merken** van verwijzingen te voorzien.

De schema&#39;s kunnen manueel door de interface worden gecreeerd of in bulk worden ingevoerd gebruikend een Ddl- dossier.

Deze sectie biedt stapsgewijze instructies voor het maken van een relationeel schema in Adobe Experience Platform door een DDL-bestand (Data Definition Language) te uploaden. Met behulp van een DDL-bestand kunt u vooraf de structuur van uw gegevensmodel definiëren, inclusief tabellen, kenmerken, sleutels en relaties.

1. [ upload een Ddl- dossier ](#ddl-upload) om relationele schema&#39;s tot stand te brengen en hun structuur te bepalen.

1. [ bepaalt verhoudingen ](#relationships) tussen lijsten in uw gegevensmodel.

1. [ schema&#39;s van de Verbinding ](#link-schema) om uw relationele gegevens met bestaande profielentiteiten zoals Ontvangers of Banden te verbinden.

1. [ Samenvatting gegevens ](ingest-data.md) in uw dataset van gesteunde bronnen.

## Een DDL-bestand uploaden{#ddl-upload}

Door een DDL-bestand te uploaden, kunt u vooraf de structuur van uw gegevensmodel definiëren, inclusief tabellen, kenmerken, sleutels en relaties.

Op Excel gebaseerde schemabestanden worden geüpload. Download het [ verstrekte malplaatje ](assets/template.zip) om uw schemadefinities gemakkelijk voor te bereiden.

+++De volgende functies worden ondersteund bij het maken van relationele schema&#39;s in Adobe Experience Platform

* **ENUM**\
  De gebieden van ENUM worden gesteund in zowel op DDL-Gebaseerde als handschemaverwezenlijking, die u toestaan om attributen met een vaste reeks toegestane waarden te bepalen.

* **Etiket van het Schema voor het Beleid van Gegevens**\
  De etikettering wordt gesteund op het niveau van het schemagebied om gegevens te handhaven governance beleid zoals toegangsbeheer en gebruiksbeperkingen. Voor meer details, verwijs naar [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl).

* **Samengestelde Sleutel**\
  Samengestelde primaire sleutels worden in relationele schemadefinities gesteund, toelatend het gebruik van veelvoudige gebieden samen om verslagen uniek te identificeren.

+++

1. Meld u aan bij Adobe Experience Platform.

1. Navigeer aan het **Beheer van Gegevens** > **Schema** menu.

1. Klik **creëren Schema**.

1. Selecteer **[!UICONTROL Relational]** als uw **type van Schema**.

   ![](assets/admin_schema_1.png)

1. Selecteer **[!UICONTROL Upload DDL file]** om een entiteitrelatiediagram te bepalen en schema&#39;s tot stand te brengen.

   De tabelstructuur moet het volgende bevatten:
   * Ten minste één primaire sleutel
   * Een versie-id, zoals een `lastmodified` veld van het type `datetime` of `number` .
   * Voor CDC-opname (Change Data Capture), een speciale kolom met de naam `_change_request_type` van het type `String` , die het type gegevenswijziging aangeeft (bijv. invoegen, bijwerken, verwijderen) en incrementele verwerking mogelijk maakt


   >[!IMPORTANT]
   >
   > Om het even welk schema dat voor het richten wordt gebruikt moet minstens één identiteitsgebied van type `String` met een bijbehorende **identiteit namespace** omvatten.\
   >Dit zorgt voor compatibiliteit met de Adobe Journey Optimizer-functionaliteit voor het maken van doelen en het oplossen van identiteiten.

1. Sleep en zet het DDL-bestand neer en klik op **[!UICONTROL Next]** .

   De maximale ondersteunde grootte voor een DDL-bestand is 10 MB.

1. Typ uw **[!UICONTROL Schema name]** in.

1. Opstelling elk schema en zijn kolommen, die ervoor zorgen dat een primaire sleutel wordt gespecificeerd.

   Eén kenmerk, zoals `lastmodified` , moet worden opgegeven als een versiedescriptor. Dit kenmerk, doorgaans van het type `datetime`, `long` of `int` , is essentieel voor innameprocessen om ervoor te zorgen dat de gegevensset wordt bijgewerkt met de meest recente gegevensversie.

   ![](assets/admin_schema_2.png)

1. Klik **[!UICONTROL Done]** eenmaal gereed.

U kunt nu de tabel- en velddefinities op het canvas controleren. [ leer meer in de sectie hieronder ](#entities)

## Relaties definiëren {#relationships}

Volg onderstaande stappen om logische verbindingen tussen tabellen in uw schema te definiëren.

1. Open de canvasweergave van uw gegevensmodel en kies de twee tabellen die u wilt koppelen

1. Klik op de knop ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) naast Source Join en sleep de pijl naar Target Join om de verbinding tot stand te brengen.

   ![](assets/admin_schema_5.png)

1. Vul de bepaalde vorm in om de verbinding te bepalen en klik **toepassen** eens gevormd.

   ![](assets/admin_schema_3.png)

   **Kardinaliteit**:

   * **1-n**: één voorkomen van de bronlijst kan verscheidene overeenkomstige voorkomen van de doellijst hebben, maar één voorkomen van de doellijst kan hoogstens één overeenkomstige voorkomen van de bronlijst hebben.

   * **n-1**: één voorkomen van de doellijst kan verscheidene overeenkomstige voorkomen van de bronlijst hebben, maar één voorkomen van de bronlijst kan hoogstens één overeenkomstige voorkomen van de doellijst hebben.

   * **1-1**: één voorkomen van de bronlijst kan hoogstens één overeenkomstige voorkomen van de doellijst hebben.

1. Alle koppelingen die in het gegevensmodel zijn gedefinieerd, worden als pijlen weergegeven in de canvasweergave. Klik op een pijl tussen twee tabellen om details weer te geven, wijzigingen aan te brengen of de koppeling naar wens te verwijderen.

   ![](assets/admin_schema_6.png)

1. Gebruik de werkbalk om het canvas aan te passen en aan te passen.

   ![](assets/toolbar.png)

   * **Gezoem binnen**: vergroot het canvas om details van uw gegevensmodel duidelijker te zien.

   * **Gezoem uit**: Verminder de canvasgrootte voor een bredere mening van uw gegevensmodel.

   * **Passende mening**: Pas het gezoem aan om alle schema&#39;s binnen het zichtbare gebied te passen.

   * **Filter**: Kies welk schema om binnen het canvas te tonen.

   * **de auto lay-out van de Dwinging**: Orden automatisch schema&#39;s voor betere organisatie.

   * **Kaart van de Vertoning**: Ga een minikaartbekleding in-/uitschakelen helpen grote of complexe schemalay-outs gemakkelijker navigeren.

1. Klik **sparen** eens gereed. Deze actie leidt tot de schema&#39;s en bijbehorende gegevensreeksen en laat de gegevensreeks voor gebruik in Geordende Campagnes toe.

1. Klik op **[!UICONTROL Open Jobs]** om de voortgang van de ontwerptaak te volgen. Dit proces kan enkele minuten duren, afhankelijk van het aantal tabellen dat in het DDL-bestand is gedefinieerd.

   U kunt ook uw relationele taken openen door het venster **[!UICONTROL Upload DDL file]** te openen en **[!UICONTROL View all relational Jobs]** te selecteren.

   ![](assets/admin_schema_4.png)

## Koppelingsschema&#39;s {#link-schema}

>[!IMPORTANT]
>
> Alleen relaties die expliciet in het DDL-bestand zijn gedefinieerd, worden door het systeem herkend. Om het even welke entiteitverhoudingen die buiten het Ddl- dossier bestaan zullen worden genegeerd en niet verwerkt.

Vestig een verband tussen het **schema van de 0&rbrace; loyaliteitstransacties &lbrace;en het** Ontvangers **schema om elke transactie met het correcte klantenverslag te associëren.**

1. Navigeer aan **[!UICONTROL Schemas]** en open eerder **loyaliteitstransacties** creëren.

1. Klik op **[!UICONTROL Add Relationship]** van de klant **[!UICONTROL Field properties]** .

   ![](assets/schema_1.png)

1. Selecteer **[!UICONTROL Many-to-One]** als de relatie **[!UICONTROL Type]** .

1. Verbinding met het bestaande **Ontvangers** schema.

   ![](assets/schema_2.png)

1. Voer een **[!UICONTROL Relationship name from current schema]** en **[!UICONTROL Relationship name from reference schema]** in.

1. Klik op **[!UICONTROL Apply]** om de wijzigingen op te slaan.

Ga door een verband tussen het **loyaliteitbeloningen** schema en het **Merken** schema te creëren om elke beloningsingang met het aangewezen merk te associëren.

![](assets/schema_3.png)


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
