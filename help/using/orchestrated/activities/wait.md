---
solution: Journey Optimizer
product: journey optimizer
title: Gebruik de activiteit van de Wacht in Geordende campagnes
description: Leer hoe te om de activiteit van de Wacht in Geordende campagnes te gebruiken
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---

# Wachten {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Wachtactiviteit"
>abstract="**wacht** activiteit wordt gebruikt om de overgang van een activiteit aan een andere te vertragen."


+++ Inhoudsopgave

| Welkom bij Geordende campagnes | Start uw eerste geordende campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met Geordende campagnes ](../gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](../gs-schemas.md)</li><li>[ Handmatig schema ](../manual-schema.md)</li><li>[ het uploadschema van het Dossier ](../file-upload-schema.md)</li><li>[ Ingest gegevens ](../ingest-data.md)</li></ul>[ toegang en beheer Geordende campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen om een Geordende campagne ](../gs-campaign-creation.md)<br/><br/>[ tot stand te brengen en de campagne te plannen ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) te controleren | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) sparen publiek [ - ](save-audience.md) Gesplitst [ - ](split.md) wacht <b>[&#128279;](wait.md)</b> |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

De **[!UICONTROL Wait]** -activiteit is een **[!UICONTROL Flow control]** -component die wordt gebruikt om een vertraging tussen twee activiteiten in een geordende campagne in te voeren. Dit helpt ervoor te zorgen dat uw follow-upactiviteiten een beter tijdstip hebben en relevanter zijn voor de betrokkenheid van gebruikers.

U kunt bijvoorbeeld een paar dagen na het verzenden van een e-mailbericht wachten om te controleren of het bericht wordt geopend en vervolgens klikken voordat u een vervolgbericht verzendt.

## Configuratie{#wait-configuration}

Voer de volgende stappen uit om de **[!UICONTROL Wait]** -activiteit te configureren:

1. Voeg een **[!UICONTROL Wait]** activiteit in uw Geordende campagne toe.

1. Selecteer het type Wacht dat het beste bij uw behoeften past:

   * **[!UICONTROL Duration]**: geef een vertraging op in seconden, minuten, uren of dagen voordat u verdergaat met de volgende activiteit.

   * **[!UICONTROL Fixed time]**: stel een specifieke datum en tijd in waarna de volgende activiteit begint.

   ![](../assets/wait_activity.png)

## Voorbeeld{#wait-example}

Het volgende voorbeeld illustreert de **[!UICONTROL Wait]** activiteit in een typisch gebruikscase.  Er wordt een e-mail met een promotiecode verzonden naar profielen die hun verjaardagen vieren. Na 29 dagen wordt een SMS verzonden naar dezelfde groep als een herinnering dat hun verjaardagspromotiecode bijna verlopen is.

![](../assets/wait-example.png)
