---
solution: Journey Optimizer
product: journey optimizer
title: Configuratiestappen
description: Leer hoe u een model-gebaseerd schema maakt in Adobe Experience Platform door een DDL te uploaden
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: e189bb6a52691770655a436e45c6788d1011a8ca
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 1%

---


# Ga aan de slag met op modellen gebaseerde schema&#39;s en gegevenssets{#gs-schemas}

Deze gids begeleidt u door het proces om een model-gebaseerd schema tot stand te brengen, vormend een dataset voor Geordende campagnes en het opnemen van gegevens.

![ schema ](assets/do-not-localize/schema_admin.png){zoomable="yes"}

## Belangrijkste concepten

In de context van Geordende campagnes, is a **dataset** een opslag en beheersconstructie voor een inzameling van gegevens, typisch een lijst, die een schema (rijen) en gebieden (kolommen) bevat. De gegevens die met succes in Experience Platform worden opgenomen worden opgeslagen binnen het gegevensmeer als datasets.

A **schema** vertegenwoordigt en bevestigt de structuur en het formaat van gegevens. Het verstrekt een abstracte definitie van een real-world voorwerp (zoals een persoon) en schetst welke gegevens in elk geval van dat voorwerp (zoals naam, verjaardag, etc.) zouden moeten worden omvat.

A **gegevensmodel** is de conceptuele blauwdruk van het normaliseren van uw gegevens

Hierin wordt beschreven:

* De entiteiten (bijvoorbeeld klant, campagne, segment)
* De kenmerken van deze entiteiten (bijvoorbeeld naam van de klant, begindatum van campagne)
* De relaties tussen entiteiten (klanten behoren bijvoorbeeld tot segmenten, doelsegmenten voor campagnes)

Een gegevensmodel is logisch en conceptueel, niet gebonden aan een fysieke implementatie in Geordende Campagne

In a **model-gebaseerd gegevensmodel**, wordt het gegeven georganiseerd in lijsten met betrekking tot andere lijsten.

* Elke tabel heeft rijen (records) en kolommen (kenmerken)
* Elke tabel heeft een primaire sleutel om rijen op unieke wijze te identificeren
* Relaties tussen tabellen worden uitgedrukt met behulp van buitenlandse sleutels

A **op model-gebaseerd schema** is de formele definitie van het op model-gebaseerde gegevensmodel.

Hier wordt aangegeven:

* De reeks tabellen
* De kolommen in elke tabel
* De beperkingen
* De relaties tussen tabellen

Het organiseren van schema&#39;s of lijsten in een model-gebaseerd gegevensmodel is over het structureren van uw gegevens in veelvoudige lijsten. Zorg ervoor dat elke tabel één type entiteit/schema&#39;s opslaat

➡️ [ Leer meer over schema&#39;s in de documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/ui/resources/schemas#create-model-based-schema)

## Implementatiestappen {#implementation}

Voer de volgende stappen uit om gegevens in te voeren en op een model gebaseerd schema te maken:

1. Creeer [ model-gebaseerd schema manueel ](manual-schema.md) of [ gebruikend een Ddl- dossier ](file-upload-schema.md)

   Definieer de structuur van uw gegevensmodel, inclusief tabellen, kenmerken en relaties. Kies ervoor het schema handmatig te bouwen in de gebruikersinterface of een DDL-bestand te uploaden voor een snellere installatie.

   Wanneer het creëren van het schema manueel, dataset moet ook manueel worden gecreeerd en worden toegelaten. Wanneer het gebruiken van een Ddl- dossier, zijn de verwezenlijking van de dataset en enablement automatisch.

1. [Koppelingsschema&#39;s](file-upload-schema.md)

   Vestig relaties tussen uw schema&#39;s om gegevensconsistentie te verzekeren en dwars-entiteitvragen toe te laten. Koppel bijvoorbeeld loyaliteitstransacties aan ontvangers of beloningen aan merken.

1. [Gegevensset maken](manual-schema.md#dataset)

   Na het bepalen van uw schema, moet u een dataset tot stand brengen die op het wordt gebaseerd. Deze dataset fungeert als de opslag voor uw opgenomen gegevens.

1. [Geordende campagnes inschakelen](manual-schema.md#enable)

   De dataset slaat uw opgenomen gegevens op en moet voor Geordende Campagnes worden toegelaten om het in Adobe Journey Optimizer toegankelijk te maken.

1. [Gegevens samenvoegen](ingest-data.md)

   Breng gegevens van ondersteunde bronnen, zoals SFTP, cloudopslag of databases, naar Adobe Experience Platform.

