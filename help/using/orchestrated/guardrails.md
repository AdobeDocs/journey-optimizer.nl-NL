---
solution: Journey Optimizer
product: journey optimizer
title: Gangbare campagnes en beperkingen
description: Meer informatie over geordende campagnes, instructies en beperkingen
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Afvoerkanalen en beperkingen {#guardrails}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](gs-schemas.md)</li><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul>[ toegang en beheer georkestreerde campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Zeer belangrijke stappen om een georkestreerde campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [&#128279;](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Beperkingen van gegevensstroom tot gegevensset

Elke dataset in Adobe Experience Platform kan slechts met één actieve dataflow tegelijkertijd worden geassocieerd. Deze 1:1-kardinaliteit wordt strikt door het platform gehandhaafd.

Als u gegevensbronnen moet schakelen (bijvoorbeeld van Amazon S3 naar Salesforce):

U moet de bestaande gegevensstroom schrappen die met de dataset wordt verbonden.

Dan, creeer een nieuwe gegevensstroom met de nieuwe bron die aan de zelfde dataset wordt in kaart gebracht.

Dit garandeert betrouwbare gegevensinvoer en is van essentieel belang bij het gebruik van Change Data Capture (CDC), die afhankelijk is van een gedefinieerde primaire sleutel en versioning-eigenschap (bijvoorbeeld laatst gewijzigd) voor incrementele updates.


## Relationele schema&#39;s/beperkingen voor gegevensinvoer

* Aantal schema&#39;s - Maximum aantal relationele schema&#39;s (lijsten in de relationele datastore) is 200
* De grootte van het relationele Schema - de Maximale Grootte van het Relationele Schema voor de Orchestratie van de Campagne zal 100GB zijn.
* Frequentie van inname van gegevens - De Ingestiefrequentie van de Gegevens van de Partij voor Campagne Orchestratie niet om de 15 minuten overschrijden.
* Wijzigingen/updates - Dagelijkse updates/wijzigingen moeten lager zijn dan 20% van het totale aantal records voor een bepaald relationeel schema
