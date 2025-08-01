---
solution: Journey Optimizer
product: journey optimizer
title: De publieksactiviteit Lezen gebruiken
description: Leer hoe u de Lees-publieksactiviteit gebruikt in een geordende campagne
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ef8eba57-cd33-4746-8eb4-5214ef9cbe2f
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Doelgroep lezen {#read-audience}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_read_audience"
>title="Activiteit voor publiek opbouwen"
>abstract="De **gelezen publiek** activiteit staat u toe om het publiek te selecteren dat de Geordende campagne zal ingaan. Dit publiek kan een bestaand Adobe Experience Platform-publiek zijn of een publiek dat uit een CSV-bestand is opgehaald. Wanneer het verzenden van berichten in de context van een Geordende campagne, wordt het berichtpubliek niet bepaald in de kanaalactiviteit, maar in a **gelezen publiek** of a **bouwt publiek** activiteit."


+++ Inhoudsopgave

| Welkom bij Geordende campagnes | Start uw eerste geordende campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met Geordende campagnes ](../gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](../gs-schemas.md)</li><li>[ Handmatig schema ](../manual-schema.md)</li><li>[ het uploadschema van het Dossier ](../file-upload-schema.md)</li><li>[ Ingest gegevens ](../ingest-data.md)</li></ul>[ toegang en beheer Geordende campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen om een Geordende campagne ](../gs-campaign-creation.md)<br/><br/>[ tot stand te brengen en de campagne te plannen ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) te controleren | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) sparen publiek [ - ](save-audience.md) Gesplitst [ - ](split.md) wacht [&#128279;](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

Met de **[!UICONTROL Read audience]** -activiteit kunt u een bestaand publiek ophalen (dat eerder is opgeslagen of geïmporteerd) en dit opnieuw gebruiken in een geordende campagne. Deze activiteit is vooral nuttig voor het richten van een vooraf bepaalde reeks profielen zonder de behoefte om een nieuw segmenteringsproces uit te voeren.

Wanneer het publiek is geladen, kunt u dit optioneel verfijnen door een uniek identiteitsveld te selecteren en het publiek te verrijken met extra profielkenmerken voor doelgerichte, personalisatie- of rapportagedoeleinden.

## De activiteit voor het lezen van het publiek configureren {#read-audience-configuration}

Voer de volgende stappen uit om de **[!UICONTROL Read audience]** -activiteit te configureren:

1. Voeg een **[!UICONTROL Read audience]** activiteit aan uw Geordende campagne toe.

   ![](../assets/read-audience-1.png)

1. Voer een **[!UICONTROL Label]** in voor uw activiteit.

1. Klik ![ pictogram van het omslagonderzoek ](../assets/do-not-localize/folder-search.svg) om het publiek te selecteren u wenst om voor uw Geordende campagne te richten.

   ![](../assets/read-audience-2.png)

1. Kies een **[!UICONTROL Entity&#x200B;]** optie in de doeldimensie van uw campagne.

   ➡️ [ volg de stappen in deze pagina worden gedetailleerd om uw Campagne te creëren richtend afmeting ](../target-dimension.md)

   ![](../assets/read-audience-3.png)

1. Selecteer **[!UICONTROL Add attribute]** om het geselecteerde publiek te verrijken met extra gegevens. Het resulterende publiek bevat een lijst met ontvangers die elk zijn verrijkt met de geselecteerde profielkenmerken.

1. Kies **[!UICONTROL Attributes]** u aan uw publiek wilt toevoegen.

   ![](../assets/read-audience-4.png)

## Voorbeeld

In het onderstaande voorbeeld wordt de **[!UICONTROL Read audience]** -activiteit gebruikt om een eerder gemaakt en opgeslagen publiek op te halen van profielen die zijn geabonneerd op de nieuwsbrief. Het publiek wordt dan verrijkt met het **1&rbrace; attribuut van het Loyalty lidmaatschap &lbrace;om het richten van gebruikers toe te laten die lid van het loyaliteitsprogramma zijn.**

![](../assets/read-audience-5.png)
