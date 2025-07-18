---
solution: Journey Optimizer
product: journey optimizer
title: Configuratiestappen
description: Leer hoe u een relationeel schema maakt in Adobe Experience Platform door een DDL te uploaden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 3dc0bf4acc4976ca1c46de46cf6ce4f2097f3721
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Aan de slag met schema&#39;s en gegevenssets{#gs-schemas}

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

Deze gids begeleidt u door het proces om een relationeel schema tot stand te brengen, vormend een dataset voor georkestreerde campagnes en het opnemen van gegevens.

![](assets/do-not-localize/schema_admin.png)

1. Creeer [ relationeel schema manueel ](manual-schema.md) of [ gebruikend een Ddl- dossier ](file-upload-schema.md)

   Definieer de structuur van uw gegevensmodel, inclusief tabellen, kenmerken en relaties. Kies ervoor het schema handmatig te bouwen in de gebruikersinterface of een DDL-bestand te uploaden voor een snellere installatie.

1. [Koppelingsschema](#link-schema)

   relaties tussen uw schema&#39;s tot stand brengen om gegevensconsistentie te verzekeren en vragen tussen entiteiten mogelijk te maken. Koppel bijvoorbeeld loyaliteitstransacties aan ontvangers of beloningen aan merken.

1. [Gegevens samenvoegen](#ingest)

   Breng gegevens van ondersteunde bronnen, zoals SFTP, cloudopslag of databases, naar Adobe Experience Platform.

