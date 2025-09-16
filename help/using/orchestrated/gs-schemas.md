---
solution: Journey Optimizer
product: journey optimizer
title: Configuratiestappen
description: Leer hoe u een relationeel schema maakt in Adobe Experience Platform door een DDL te uploaden
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: 69644e85d9c453f34fe8c5d40e0c1e8dce2891a5
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---


# Aan de slag met relationele schema&#39;s en gegevenssets{#gs-schemas}

Deze gids begeleidt u door het proces om een relationeel schema tot stand te brengen, vormend een dataset voor Geordende campagnes en het opnemen van gegevens.

![](assets/do-not-localize/schema_admin.png)

Een dataset is een opslag en beheersconstructie voor een inzameling van gegevens, typisch een lijst, die een schema (kolommen) en gebieden (rijen) bevat. De gegevens die met succes in Experience Platform worden opgenomen worden opgeslagen binnen het gegevensmeer als datasets.

Een schema vertegenwoordigt en valideert de structuur en de indeling van gegevens. Het verstrekt een abstracte definitie van een real-world voorwerp (zoals een persoon) en schetst welke gegevens in elk geval van dat voorwerp (zoals naam, verjaardag, etc.) zouden moeten worden omvat.


1. Creeer [ relationeel schema manueel ](manual-schema.md) of [ gebruikend een Ddl- dossier ](file-upload-schema.md)

   Definieer de structuur van uw gegevensmodel, inclusief tabellen, kenmerken en relaties. Kies ervoor het schema handmatig te bouwen in de gebruikersinterface of een DDL-bestand te uploaden voor een snellere installatie.

   Wanneer het creëren van het schema manueel, dataset moet ook manueel worden gecreeerd en worden toegelaten. Wanneer het gebruiken van een Ddl- dossier, zijn de verwezenlijking van de dataset en enablement automatisch.

1. [Koppelingsschema](file-upload-schema.md)

   Vestig relaties tussen uw schema&#39;s om gegevensconsistentie te verzekeren en dwars-entiteitvragen toe te laten. Koppel bijvoorbeeld loyaliteitstransacties aan ontvangers of beloningen aan merken.

1. [Gegevens samenvoegen](ingest-data.md)

   Breng gegevens van ondersteunde bronnen, zoals SFTP, cloudopslag of databases, naar Adobe Experience Platform.

