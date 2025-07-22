---
solution: Journey Optimizer
product: journey optimizer
title: Configuratiestappen
description: Leer hoe u gegevens van ondersteunde bronnen, zoals SFTP, cloudopslag of databases, naar Adobe Experience Platform kunt overbrengen.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: a4337df949d25740f75204fe4530837dda1af3dd
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# Samenvattingsgegevens {#ingest-data}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets </br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](gs-schemas.md)</li><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul>[ toegang en beheer georkestreerde campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Zeer belangrijke stappen om een georkestreerde campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [&#128279;](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

Adobe Experience Platform staat toe dat gegevens uit externe bronnen worden opgenomen en biedt u de mogelijkheid om inkomende gegevens te structureren, labelen en verbeteren met behulp van Experience Platform-services. U kunt gegevens invoeren uit verschillende bronnen, zoals Adobe-toepassingen, opslag in de cloud, databases en vele andere.

## Met cloudopslag {#ingest}


>[!IMPORTANT]
>
>Om de gegevensbron voor een dataset te veranderen, moet u eerst bestaande dataflow schrappen alvorens tot nieuwe te leiden die de zelfde dataset en de nieuwe bron verwijzingen.
>
>Adobe Experience Platform dwingt een strikte één-op-één verhouding tussen gegevensstromen en datasets af. Dit staat u toe om synchronisatie tussen de bron en de dataset voor nauwkeurige stijgende opname te handhaven.


U kunt een gegevensstroom vormen om gegevens van een bron van Amazon S3 in Adobe Experience Platform in te voeren. Zodra gevormd, laat de gegevensstroom geautomatiseerde, geplande opname van gestructureerde gegevens toe en steunt updates in real time.

1. Via het menu **[!UICONTROL Connections]** opent u het menu **[!UICONTROL Sources]** .

1. Selecteer de categorie **[!UICONTROL Cloud storage]** , vervolgens Amazon S3 en klik op **[!UICONTROL Add Data]** .

   ![](assets/admin_sources_1.png)

1. Sluit uw S3-account aan:

   * Met een bestaande account

   * Met een nieuwe account

   [ leer meer in de documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#connect)

   ![](assets/admin_sources_2.png)

1. Kies uw map **[!UICONTROL Data format]** , **[!UICONTROL Delimiter]** en **[!UICONTROL Compression type]** .

1. Navigeer door de verbonden S3 bron tot u van gewenste omslagen, bijvoorbeeld **loyaliteitbeloningen** en **loyaliteitstransacties** de plaats bepaalt.

1. Selecteer de map die uw gegevens bevat.

   Als u een map selecteert, worden alle huidige en toekomstige bestanden met dezelfde structuur automatisch verwerkt. Als u één bestand selecteert, moet u echter elke nieuwe gegevensstap handmatig uploaden.

   ![](assets/S3_config_2.png)

1. Kies uw map **[!UICONTROL Data format]** , **[!UICONTROL Delimiter]** en **[!UICONTROL Compression type]** . Controleer de voorbeeldgegevens op nauwkeurigheid en klik op **[!UICONTROL Next]** .

   ![](assets/S3_config_1.png)

1. Schakel **[!UICONTROL Enable Change data capture]** in om alleen gegevenssets weer te geven die zijn toegewezen aan relationele schema&#39;s en zowel een primaire sleutel als een versiedescriptor bevatten.

   ![](assets/S3_config_6.png)

1. Selecteer de eerder gemaakte gegevensset en klik op **[!UICONTROL Next]** .

   ![](assets/S3_config_3.png)

1. Controleer in het venster **[!UICONTROL Mapping]** of elk kenmerk van het bronbestand correct is toegewezen aan de corresponderende velden in het doelschema.

   Klik **[!UICONTROL Next]** eenmaal gereed.

   ![](assets/S3_config_4.png)

1. Configureer de gegevensstroom **[!UICONTROL Schedule]** op basis van de gewenste frequentie.

1. Klik op **[!UICONTROL Finish]** om de gegevensstroom te maken. Deze wordt automatisch uitgevoerd volgens het gedefinieerde schema.

1. Selecteer **[!UICONTROL Connections]** in het menu **[!UICONTROL Sources]** en open het tabblad **[!UICONTROL Data Flows]** om de uitvoering van de flow bij te houden, ingesloten records te controleren en eventuele fouten op te lossen.

   ![](assets/S3_config_5.png)

