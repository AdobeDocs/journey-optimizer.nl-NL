---
solution: Journey Optimizer
product: journey optimizer
title: Werken met geordende campagneactiviteiten
description: Meer informatie over geordende campagneactiviteiten
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: e71cbc5b29a31e2f23b408ae8c8b73379a44275d
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 2%

---

# Informatie over geordende campagneactiviteiten {#orchestrated-campaign-activities}


+++ Inhoudsopgave

| Welkom bij Geordende campagnes | Start uw eerste geordende campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met Geordende campagnes ](../gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](../gs-schemas.md)</li><li>[ Handmatig schema ](../manual-schema.md)</li><li>[ het uploadschema van het Dossier ](../file-upload-schema.md)</li><li>[ Ingest gegevens ](../ingest-data.md)</li></ul>[ toegang en beheer Geordende campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen om een Geordende campagne ](../gs-campaign-creation.md)<br/><br/>[ tot stand te brengen en de campagne te plannen ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) te controleren | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | <b>[ wordt begonnen met activiteiten ](about-activities.md)</b><br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) sparen publiek [ - ](save-audience.md) Gesplitst [ - ](split.md) wacht [&#128279;](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

De geordende campagneactiviteiten zijn gegroepeerd in drie categorieën. Afhankelijk van de context kunnen de beschikbare activiteiten afwijken.

Alle activiteiten worden beschreven in de volgende onderdelen:

* [Targetingactiviteiten](#targeting)
* [Kanaalactiviteiten](#channel)
* [Workflowbeheeractiviteiten](#flow-control)

![ Lijst van activiteiten beschikbaar in het canvas ](../assets/orchestrated-activities.png){width="80%" align="left"}

## Targetingactiviteiten {#targeting}

Deze activiteiten zijn specifiek gericht op de doelgroepen. Met deze instructies kunt u een of meer doelen maken door een publiek te definiëren en deze soorten publiek te splitsen of te combineren met een doorsnede-, samenvoegings- of uitsluitingsbewerking.

![ Lijst van het richten van activiteiten ](../assets/targeting-activities.png){width="40%" align="left"}

* [ bouwt publiek ](build-audience.md): Bepaal uw doelbevolking. U kunt of een bestaand publiek selecteren of de regelbouwer gebruiken om uw eigen vraag te bepalen.
* [ dimensie van de Verandering ](change-dimension.md): Verander de het richten dimensie aangezien u uw Geordende campagne bouwt.
* [ combineren ](combine.md): Voer segmentatie op uw binnenkomende bevolking uit. U kunt een samenvoeging, een doorsnede of een uitsluiting gebruiken.
* [ Deduplicatie ](deduplication.md): Schrap duplicaten in het resultaat(en) van de binnenkomende activiteiten.
* [ Verrijking ](enrichment.md): Bepaal extra gegevens om in uw Geordende campagne te verwerken. Met deze activiteit, kunt u hefboomwerking de binnenkomende overgang en de activiteit vormen om de outputovergang met extra gegevens te voltooien.
* [ Verzoening ](reconciliation.md): Bepaal het verband tussen de gegevens in de gegevens van Journey Optimizer en de gegevens in een het werklijst, bijvoorbeeld gegevens die van een extern dossier worden geladen.
* [ Gesplitst ](split.md): De inkomende bevolking van het segment in verscheidene ondergroepen.

## Kanaalactiviteiten {#channel}

Met Adobe Journey Optimizer kunt u marketingcampagnes op meerdere kanalen automatiseren en uitvoeren. U kunt kanaalactiviteiten in het canvas combineren om dwars-kanaal Geordende campagne tot stand te brengen die acties kan teweegbrengen die op klantengedrag worden gebaseerd. De volgende **activiteiten van het Kanaal** zijn beschikbaar: E-mail en SMS. [ leer hoe te om een kanaalactie in de context van een Geordende campagne ](channels.md) tot stand te brengen.

## Workflowbeheeractiviteiten {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Eindactiviteit"
>abstract="Het **Eind** activiteit staat u toe om het eind van een Geordende campagne grafisch te merken. Deze activiteit heeft geen functioneel effect en is daarom optioneel."

![ Lijst van de activiteiten van de debietcontrole ](../assets/flow-control-activities.png){width="30%" align="left"}

De volgende activiteiten zijn specifiek gericht op het organiseren en uitvoeren van geordende campagnes. Hun voornaamste taak is de coördinatie van de andere activiteiten:

* [ en-sluit zich aan ](and-join.md): Synchroniseer veelvoudige uitvoeringstakken van een Geordende campagne.
* [ Fork ](fork.md): Creeer uitgaande overgangen om verscheidene activiteiten tezelfdertijd te beginnen.
* [ wacht ](wait.md): Onderbreek tijdelijk uitvoering van een deel van een Geordende campagne.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>Het **Eind** activiteit merkt grafisch het eind van een Geordende campagne. Deze activiteit heeft geen functioneel effect en is daarom optioneel
