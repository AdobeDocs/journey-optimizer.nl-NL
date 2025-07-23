---
solution: Journey Optimizer
product: journey optimizer
title: Configuratiestappen
description: Leer hoe u gegevens van ondersteunde bronnen, zoals SFTP, cloudopslag of databases, naar Adobe Experience Platform kunt overbrengen.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: 6447f5d1a060037c0ceaa374db20966097585f9c
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 1%

---

# Samenvattingsgegevens {#ingest-data}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets </br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](gs-schemas.md)</li><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul>[ toegang en beheer georkestreerde campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Zeer belangrijke stappen om een georkestreerde campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Om de gegevensbron voor een dataset te veranderen, moet u eerst bestaande dataflow schrappen alvorens tot nieuwe te leiden die de zelfde dataset en de nieuwe bron verwijzingen.
>
>Adobe Experience Platform dwingt een strikte één-op-één verhouding tussen gegevensstromen en datasets af. Dit staat u toe om synchronisatie tussen de bron en de dataset voor nauwkeurige stijgende opname te handhaven.

Adobe Experience Platform staat toe dat gegevens uit externe bronnen worden opgenomen en biedt u de mogelijkheid om inkomende gegevens te structureren, labelen en verbeteren met behulp van Experience Platform-services. U kunt gegevens invoeren uit verschillende bronnen, zoals Adobe-toepassingen, opslag in de cloud, databases en vele andere.

## Ondersteunde bronnen voor geordende campagnes {#supported}

De volgende bronnen worden ondersteund voor gebruik met geordende campagnes:

<table>
  <thead>
    <tr>
      <th>Type</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">Cloud Storage</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3">Amazon S3</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/google-cloud-storage">Google Cloud Storage</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/sftp">SFTP</a></td>
    </tr>
      <td rowspan="4">Cloud Data Warehouses</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/snowflake">Snowflake</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/bigquery">Google BigQuery</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/data-landing-zone">Gegevenslandingszone<a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/databricks">Azure Databricks</a></td>
    </tr>
    <tr>
      <td rowspan="3">Bestandsgebaseerde uploads</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/local-system/local-file-upload">Lokaal bestand uploaden<a></td>
    </tr>

</tbody>
</table>

## Een gegevensstroom configureren

In dit voorbeeld wordt getoond hoe u een gegevensstroom configureert die gestructureerde gegevens in Adobe Experience Platform opneemt. De gevormde gegevensstroom steunt geautomatiseerde, geplande opname en laat updates in real time toe.

1. Via het menu **[!UICONTROL Connections]** opent u het menu **[!UICONTROL Sources]** .

1. Kies uw bron afhankelijk van de [ Gesteunde Bronnen voor Geordende campagnes ](#supported).

   ![](assets/admin_sources_1.png)

1. Sluit uw Cloud Storage- of Google Cloud Storage-account aan als u bronnen op basis van cloud hebt gekozen.

   ![](assets/admin_sources_2.png)

1. Kies de gegevens die u in Adobe Experience Platform wilt opnemen.

   ![](assets/S3_config_1.png)

1. Schakel **[!UICONTROL Dataset details]** vanaf de pagina **[!UICONTROL Enable Change data capture]** in om alleen gegevenssets weer te geven die zijn toegewezen aan relationele schema&#39;s en die zowel een primaire sleutel als een versiedescriptor bevatten.

   >[!IMPORTANT]
   >
   > Voor **dossier-gebaseerde slechts bronnen**, moet elke rij in het gegevensdossier een `_change_request_type` kolom met waarden `U` (upsert) of `D` (schrapping) omvatten. Zonder deze kolom, zal het systeem niet de gegevens als ondersteunend verandering volgen erkennen, en de Geordende knevel van de Campagne zal niet verschijnen, verhinderend de dataset voor het richten wordt geselecteerd.

   ![](assets/S3_config_6.png)

1. Selecteer de eerder gemaakte gegevensset en klik op **[!UICONTROL Next]** .

   ![](assets/S3_config_3.png)

1. Als u alleen op bestanden gebaseerde bronnen gebruikt, uploadt u vanuit het **[!UICONTROL Select data]** -venster uw lokale bestanden en geeft u een voorvertoning van de structuur en inhoud ervan weer.

   De maximale ondersteunde grootte is 100 MB.

1. Controleer in het venster **[!UICONTROL Mapping]** of elk kenmerk van het bronbestand correct is toegewezen aan de corresponderende velden in het doelschema.

   Klik **[!UICONTROL Next]** eenmaal gereed.

   ![](assets/S3_config_4.png)

1. Configureer de gegevensstroom **[!UICONTROL Schedule]** op basis van de gewenste frequentie.

1. Klik op **[!UICONTROL Finish]** om de gegevensstroom te maken. Deze wordt automatisch uitgevoerd volgens het gedefinieerde schema.

1. Selecteer **[!UICONTROL Connections]** in het menu **[!UICONTROL Sources]** en open het tabblad **[!UICONTROL Data Flows]** om de uitvoering van de flow bij te houden, ingesloten records te controleren en eventuele fouten op te lossen.

   ![](assets/S3_config_5.png)

