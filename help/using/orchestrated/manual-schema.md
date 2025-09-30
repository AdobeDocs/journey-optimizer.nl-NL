---
solution: Journey Optimizer
product: journey optimizer
title: Configuratiestappen
description: Leer hoe u op modellen gebaseerde schema's rechtstreeks via de gebruikersinterface kunt maken.
exl-id: 8c785431-9a00-46b8-ba54-54a10e288141
version: Campaign Orchestration
source-git-commit: e189bb6a52691770655a436e45c6788d1011a8ca
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---

# Een handmatig op een model gebaseerd schema instellen {#manual-schema}

Op modellen gebaseerde schema&#39;s kunnen direct door het gebruikersinterface worden gecreeerd, toelatend gedetailleerde configuratie van attributen, primaire sleutels, versieringsgebieden, en verhoudingen.

Het volgende voorbeeld bepaalt manueel het **schema van het Membership van de Loyalty** om de vereiste structuur voor Geordende campagnes te illustreren.

1. [ creeer manueel een model-gebaseerd schema ](#schema) gebruikend de interface van Adobe Experience Platform.

1. [ voegt attributen ](#schema-attributes) zoals klant identiteitskaart, lidmaatschapsniveau, en statusgebieden toe.

1. [ Verbinding uw schema ](#link-schema) aan ingebouwde schema&#39;s zoals Ontvangers voor campagne het richten.

1. [ creeer een dataset ](#dataset) die op uw schema wordt gebaseerd en laat het voor gebruik in Geordende campagnes toe.

1. [ Samenvatting gegevens ](ingest-data.md) in uw dataset van gesteunde bronnen.

➡️ [ Leer meer over handmodel-gebaseerde schema&#39;s in de documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/ui/resources/schemas#create-manually)

## Uw schema maken {#schema}

Begin door een nieuw model-gebaseerd schema manueel in Adobe Experience Platform te creëren. Met dit proces kunt u de schemastructuur helemaal opnieuw definiëren, inclusief de naam en het gedrag.

1. Meld u aan bij Adobe Experience Platform.

1. Ga naar het menu **[!UICONTROL Data Management]** > **[!UICONTROL Schema]** .

1. Klik op **[!UICONTROL Create Schema]**.

1. Selecteer **[!UICONTROL Model-based]** als uw **type van Schema**.

   ![](assets/admin_schema_1.png){zoomable="yes"}

1. Kies **[!UICONTROL Create manually]** om het schema samen te stellen door handmatig velden toe te voegen.

1. Voer uw **[!UICONTROL Schema display name]** in.

   ![](assets/schema_manual_8.png){zoomable="yes"}

1. Klik **Afwerking** om aan uw schemaverwezenlijking te werk te gaan.

U kunt nu kenmerken aan uw schema toevoegen om de structuur ervan te definiëren.

## Kenmerken toevoegen aan uw schema {#schema-attributes}

Voeg vervolgens kenmerken toe om de structuur van het schema te definiëren. Deze gebieden vertegenwoordigen de belangrijkste gegevenspunten die in Geordende campagnes, zoals klantenherkenningstekens, lidmaatschapsdetails, en activiteitendata worden gebruikt. Het bepalen van hen verzekert nauwkeurig betrouwbare verpersoonlijking, segmentatie, en het volgen.

Schema&#39;s die worden gebruikt voor activering, moeten ten minste één identiteitsveld van het type `String` met een bijbehorende naamruimte bevatten. Dit zorgt voor compatibiliteit met de Adobe Journey Optimizer-functionaliteit voor het maken van doelen en het oplossen van identiteiten.

+++De volgende functies worden ondersteund bij het maken van modelgebaseerde schema&#39;s in Adobe Experience Platform

* **ENUM**\
  De gebieden van ENUM worden gesteund in zowel op DDL-Gebaseerde als handschemaverwezenlijking, die u toestaan om attributen met een vaste reeks toegestane waarden te bepalen.

* **Etiket van het Schema voor het Beleid van Gegevens**\
  De etikettering wordt gesteund op het niveau van het schemagebied om gegevens te handhaven governance beleid zoals toegangsbeheer en gebruiksbeperkingen. Voor meer details, verwijs naar [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl).

* **Samengestelde Sleutel**\
  Samengestelde primaire sleutels worden ondersteund in modelgebaseerde schemadefinities, waardoor het gebruik van meerdere velden samen mogelijk wordt om records uniek te identificeren.

+++

1. In het canvas, klik ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) naast uw **naam van het Schema** beginnen attributen toe te voegen.

   ![](assets/schema_manual_1.png){zoomable="yes"}

1. Voer het kenmerk **[!UICONTROL Field name]** , **[!UICONTROL Display name]** en **[!UICONTROL Type]** in.

   In dit voorbeeld, hebben wij de attributen toegevoegd die in de lijst hieronder aan het **het lidmaatschapsschema van de Loyalty** worden gedetailleerd.

   +++ Voorbeelden van kenmerken

   | Kenmerknaam | Gegevenstype | Aanvullende kenmerken |
   |-|-|-|
   | klant | TEKENREEKS | Primaire sleutel |
   | membership_level | TEKENREEKS | Vereist |
   | points_balance | INTEGER | Vereist |
   | enrollment_date | DATE | Vereist |
   | last_status_change | DATE | Vereist |
   | expiration_date | DATE | - |
   | is_active | BOOLEAN | Vereist |
   | laatstelijk | DATETIME | Vereist |

   +++ 

1. Wijs de desbetreffende velden toe als de **[!UICONTROL Primary Key]** en **[!UICONTROL Version Descriptor]** .

   Zorg ervoor dat de volgende essentiële velden zijn opgenomen wanneer u een handmatig schema maakt:

   * Ten minste één primaire sleutel
   * Een versie-id, zoals een `lastmodified` veld van het type `datetime` of `number` .
   * Voor CDC-opname (Change Data Capture) gebruikt u een speciale kolom met de naam `_change_request_type` van het type `String` , die het type gegevenswijziging aangeeft (bijvoorbeeld invoegen, bijwerken, verwijderen) en incrementele verwerking mogelijk maakt. `_change_request_type` mag geen deel uitmaken van het tabelschema, maar moet alleen tijdens de opname aan het gegevensbestand worden toegevoegd.

   ![](assets/schema_manual_2.png){zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

Nadat u kenmerken hebt gemaakt en opgeslagen, kunt u het schema koppelen aan andere relationele schema&#39;s door relaties te definiëren.

## Koppelingsschema&#39;s {#link-schema}

Als u een relatie tussen twee schema&#39;s maakt, kunt u Geordende campagnes verbeteren met gegevens buiten het primaire profielschema.

1. Selecteer in het nieuwe schema het kenmerk dat u als koppeling wilt gebruiken en klik op **[!UICONTROL Add relationship]** .

   ![](assets/schema_manual_3.png){zoomable="yes"}

1. Kies de **[!UICONTROL Reference schema]** en **[!UICONTROL Reference field]** om de relatie tot stand te brengen.

   In dit voorbeeld is het kenmerk `customer` gekoppeld aan het schema `recipients` .

   ![](assets/schema_manual_4.png){zoomable="yes"}

1. Voer een naam voor de relatie in vanuit het huidige schema en het referentieschema.

1. Klik op **[!UICONTROL Apply]** zodra dit is geconfigureerd.

## Creeer een dataset voor het schema {#dataset}

Na het bepalen van uw schema, kunt u een dataset nu tot stand brengen die op het wordt gebaseerd. De dataset slaat uw opgenomen gegevens op en moet voor Geordende Campagnes worden toegelaten om toegankelijk te zijn.

1. Ga naar het menu **[!UICONTROL Data Management]** > **[!UICONTROL Datasets]** en klik op **[!UICONTROL Create dataset]** .

   ![](assets/schema_manual_5.png){zoomable="yes"}

1. Selecteer **[!UICONTROL Create dataset from schema]**.

1. Kies uw eerder gecreeerd schema, hier **het lidmaatschap van de Loyalty**, en klik **[!UICONTROL Next]**.

   ![](assets/schema_manual_6.png){zoomable="yes"}

1. Voer een **[!UICONTROL Name]** voor uw **[!UICONTROL Dataset]** in en klik op **[!UICONTROL Finish]** .

U moet nu uw Dataset voor Geordende Campagnes toelaten.

## Dataset inschakelen voor geordende campagnes {#enable}

>[!CONTEXTUALHELP]
>id="ajo_oc_enable_dataset_for_oc"
>title="Geordende campagnes"
>abstract="Na het creëren van uw dataset, moet u het voor Geordende Campagnes uitdrukkelijk toelaten. Deze stap zorgt ervoor dat uw dataset beschikbaar is voor organisatie en verpersoonlijking in real time binnen Adobe Journey Optimizer."


Na het creëren van uw dataset, moet u het voor Geordende Campagnes uitdrukkelijk toelaten. Deze stap zorgt ervoor dat uw dataset beschikbaar is voor organisatie en verpersoonlijking in real time binnen Adobe Journey Optimizer.

Verwijs naar [ documentatie van Adobe Developer ](https://developer.adobe.com/journey-optimizer-apis/references/orchestrated-campaign-dataset/#tag/DatasetEnablement) om Geordende Uitbreiding van de Campagne op Dataset te bevestigen of toe te laten.

1. Zoek de gegevensset in de lijst **[!UICONTROL Datasets]** .

1. Van de **[!UICONTROL Datasets]** montages, laat de **Geordende 2&rbrace; optie van Campagnes &lbrace;toe om de dataset beschikbaar voor gebruik in uw Geordende Campagnes te merken.**

   ![](assets/schema_manual_7.png){zoomable="yes"}

1. Wacht een paar minuten tot het activeringsproces is voltooid. De gegevensinvoer en het campagnegebruik zijn alleen mogelijk als deze instelling volledig is geactiveerd.

U kunt nu gegevens in uw schema beginnen op te nemen gebruikend de bron van uw keus.

➡️ [ Leer hoe te om gegevens in te voeren ](ingest-data.md)
