---
solution: Journey Optimizer
product: journey optimizer
title: Gangbare campagnes en beperkingen
description: Meer informatie over geordende campagnes, instructies en beperkingen
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# Afvoerkanalen en beperkingen {#guardrails}

+++ Inhoudsopgave

| Welkom bij Geordende campagnes | Start uw eerste geordende campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met Geordende campagnes ](gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](gs-schemas.md)</li><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul>[ toegang en beheer Geordende campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Zeer belangrijke stappen om een Geordende campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [&#128279;](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Beperkingen van gegevensstroom tot gegevensset

Elke dataset in Adobe Experience Platform kan slechts met één actieve dataflow tegelijkertijd worden geassocieerd. Deze 1 :1 kardinaliteit wordt strikt afgedwongen door het platform.

Als u gegevensbronnen moet schakelen (bijvoorbeeld van Amazon S3 naar Salesforce):

U moet de bestaande gegevensstroom schrappen die met de dataset wordt verbonden.

Dan, creeer een nieuwe gegevensstroom met de nieuwe bron die aan de zelfde dataset wordt in kaart gebracht.

Dit garandeert betrouwbare gegevensinvoer en is van essentieel belang bij het gebruik van Change Data Capture (CDC), die afhankelijk is van een gedefinieerde primaire sleutel en versioning-eigenschap (bijvoorbeeld laatst gewijzigd) voor incrementele updates.


## Relationele schema&#39;s/beperkingen voor gegevensinvoer

* Tot 200 relationele schema&#39;s (lijsten) worden gesteund in de relationele datastore.

* De totale grootte van een relationeel schema dat voor de Orchestratie van de Campagne wordt gebruikt zou niet 100 GB moeten overschrijden.

* Inname in de batch voor Campaign Orchestration dient niet vaker dan eens per 15 minuten plaats te vinden.

* Dagelijkse wijzigingen in een relationeel schema moeten onder 20% van het totale aantal records blijven.

## Gegevensmodellering

* Versiedescriptor is verplicht voor alle schema&#39;s, inclusief feitelijke tabellen.

* Voor elke tabel is een primaire sleutel vereist.

* Table_name die tijdens datasetverwezenlijking wordt toegewezen wordt gebruikt over de segmentatie UI en verpersoonlijkingseigenschappen.

  Deze naam is permanent en kan na het maken niet worden gewijzigd.

* Veldgroepen worden momenteel niet ondersteund.

## Gegevensopname

* Profiel + relationele gegevensinvoer is vereist.

* Een veranderingstype gebied wordt vereist voor op dossier-gebaseerde opname, terwijl het registreren van de lijst voor de opname van de DB van de Wolk moet worden toegelaten. Dit is nodig voor Change Data Capture (CDC).

* De latentie van inname tot gegevensbeschikbaarheid in Snowflake varieert van 15 minuten tot 2 uur, afhankelijk van gegevensvolume, gelijktijdige uitvoering en het type bewerkingen (invoegen is sneller dan updates).

* Er wordt momenteel gewerkt aan toezicht op de gegevens in Snowflake; er is momenteel geen native bevestiging voor succesvolle inname.

* Directe updates voor Snowflake of de dataset worden niet ondersteund. Alle veranderingen moeten door bronnen van CDC stromen.

  De queryservice is alleen-lezen.

* ETL wordt niet ondersteund — klanten moeten gegevens in de vereiste indeling leveren.

* Gedeeltelijke updates zijn niet toegestaan. Elke rij moet worden opgegeven als een volledige record.

* De congestie baseert zich op de Dienst van de Vraag en Gegevens Distiller.

## Segmentatie

* LOV (Lijst met waarden) en opsommingen zijn momenteel beschikbaar.

* Opgeslagen soorten publiek zijn statische lijsten, de inhoud ervan geeft de gegevens weer die beschikbaar zijn op het moment dat de campagne wordt uitgevoerd.

* Toevoegen aan een opgeslagen publiek wordt niet ondersteund. Voor updates is volledige overschrijving vereist.

* Het publiek mag alleen scalaire kenmerken hebben; kaarten en arrays worden niet ondersteund.

* Segmentatie ondersteunt vooral relationele gegevens. Terwijl het mengen met profielgegevens wordt toegestaan, kan het brengen van grote profieldatasets prestaties beïnvloeden. Om dit te voorkomen:

* Er zijn hulplijnen aanwezig, zoals het beperken van het aantal profielkenmerken dat is geselecteerd in batch- of streaming-doelgroepen.

* Leesgroepen worden niet in de cache geplaatst. Elke campagnerun zorgt voor een volledige leesbewerking.

  Optimalisatie is nodig voor grote of complexe doelgroepen.