---
title: Batchbeslissing
description: Leer hoe u beslissingen kunt aanbieden voor alle profielen in een bepaald Adobe Experience Platform-segment.
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 0%

---


# Batchbeslissing {#deliver}

## Aan de slag met batch-beslissingen {#start}

Journey Optimizer stelt u in staat om beslissingen te geven voor alle profielen in een bepaald Adobe Experience Platform-segment.

Hiervoor moet u in Journey Optimizer een taakverzoek maken dat informatie bevat over het segment waarop u zich wilt richten en over het besluit dat u wilt aanbieden. De aanbiedingsinhoud voor elk profiel in het segment wordt dan geplaatst in een dataset van Adobe Experience Platform waar het voor de werkschema&#39;s van de douanepartij beschikbaar is.

Batchlevering kan ook worden uitgevoerd met behulp van API&#39;s. Raadpleeg voor meer informatie de [Batchbeslissings-API-documentatie](api-reference/offer-delivery-api/batch-decisioning-api.md).

## Vereisten {#prerequisites}

Voordat u een taakaanvraag configureert, moet u controleren of u het volgende hebt gemaakt:

* **Een gegevensset** in Adobe Experience Platform. Deze dataset zal worden gebruikt om het beslissingsresultaat op te slaan gebruikend het schema &quot;ODE DecisionEvents&quot;. Meer informatie in het dialoogvenster [Documentatie over gegevenssets](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html).

* **Een segment** in Adobe Experience Platform. Het segment zou dan moeten worden geëvalueerd en worden bijgewerkt. Leer hoe te om de evaluatie van het segmentlidmaatschap bij te werken in [Documentatie voor segmentatieservice](http://www.adobe.com/go/segmentation-overview-en)

   >[!NOTE]
   >
   >Een batchtaak loopt van de profielmomentopname die één keer per dag plaatsvindt. Met de optie Batch-beslissingen wordt de frequentie vastgelegd en worden profielen altijd geladen vanaf de meest recente momentopname.

* **Een besluit** in Adobe Journey Optimizer. [Leer hoe u een beslissing maakt](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## Een taakaanvraag maken

Volg onderstaande stappen om een nieuwe taakaanvraag te maken.

1. In de **[!UICONTROL Offers]** menu, opent u de **[!UICONTROL Batch decisioning]** en klik vervolgens op **[!UICONTROL Create request]**.

   ![](assets/batch-create.png)

1. Geef uw taakverzoek een naam en selecteer vervolgens de gegevensset waarin de taakgegevens moeten worden verzonden.

1. Selecteer het Adobe Experience Platform-segment dat u als doel wilt instellen.

1. Selecteer één of veelvoudige het besluitvormingswerkingsgebied van de aanbieding dat u wilt gebruiken om aanbiedingen aan het segment te leveren:
   1. Selecteer een plaatsing in de lijst.
   1. De beslissingen die beschikbaar zijn voor de geselecteerde plaatsingsweergave. Selecteer de gewenste beslissing en klik op **[!UICONTROL Add]**.
   1. Herhaal de bewerking om zoveel beslissingsbereik toe te voegen als u wilt.

   ![](assets/batch-decision.png)

1. Standaard wordt één aanbieding van het beslissingsbereik geretourneerd voor elk profiel. U kunt het aantal geretourneerde voorstellen aanpassen met de opdracht **[!UICONTROL Request offer per profile]** optie. Als u bijvoorbeeld 2 selecteert, worden de beste 2 aanbiedingen weergegeven voor het geselecteerde beslissingsbereik.

   >[!NOTE]
   >
   >U kunt maximaal 30 voorstellen aanvragen per beslissingsbereik.

1. Als u de aanbiedingsinhoud in de dataset wilt omvatten, knevel van **[!UICONTROL Include content]** optie ingeschakeld. Deze optie is standaard uitgeschakeld.

1. Klikken **[!UICONTROL Create]** om de taakaanvraag uit te voeren.

## Batchtaken controleren

Alle aangevraagde batchtaken zijn toegankelijk vanuit de **[!UICONTROL Batch decisioning]** tab. Bovendien, zijn de onderzoek en het filtreren hulpmiddelen beschikbaar om u te helpen de lijst verfijnen.

![](assets/batch-list.png)

### Status van taakaanvragen

Nadat een taakaanvraag is gemaakt, worden meerdere statussen gebruikt voor de batchtaak:

>[!NOTE]
>
>Om ervoor te zorgen dat u de recentste informatie over de status van een baanverzoek krijgt, gebruik de ellipse knoop naast de baan om het te verfrissen.

1. **[!UICONTROL Queued]**: Het taakverzoek is gemaakt en is in de verwerkingswachtrij geplaatst. Tot 5 partijbanen kunnen in een tijd per dataset worden in werking gesteld. Om het even welke andere partijverzoeken met de zelfde outputdataset worden toegevoegd aan de rij. Er wordt een taak in de wachtrij opgehaald om te worden verwerkt zodra de vorige taak is voltooid.
1. **[!UICONTROL Processing]**: Het taakverzoek wordt verwerkt
1. **[!UICONTROL Ingesting]**: Het baanverzoek is uitgevoerd, resultaatgegevens worden opgenomen in de geselecteerde dataset,
1. **[!UICONTROL Completed]**: Het taakverzoek is uitgevoerd en de resultaatgegevens worden nu opgeslagen in de geselecteerde dataset.

   >[!NOTE]
   >
   >U kunt tot de dataset toegang hebben waar de resultaten van een baan door zijn naam in baanlijst te klikken worden opgeslagen.

Als er een fout optreedt terwijl de taakaanvraag wordt uitgevoerd, krijgt deze de opdracht **[!UICONTROL Error]** status. Probeer de batchtaak te dupliceren om een nieuwe aanvraag te maken. [Leer hoe u een batchtaak dupliceert](#duplicate)

### Procestijd batchtaak

De tijd van begin tot eind voor elke partijbaan is de duur van de tijd de werkbelasting aan de tijd wordt gecreeerd wanneer het beslissingsresultaat in de outputdataset beschikbaar is.

De segmentgrootte is de belangrijkste factor die van invloed is op de eindtijd van de batch-beslissing. Als voor de in aanmerking komende aanbieding een algemeen frequentiegrenswaarde is ingeschakeld, duurt het nemen van batchbeslissingen meer tijd om dit te voltooien. Hieronder volgen een aantal benaderingen van de verwerkingstijd van begin tot eind voor hun respectieve segmentgrootte, zowel met als zonder frequentietoewijzing voor in aanmerking komende aanbiedingen:

Met frequentiegrens ingeschakeld voor in aanmerking komende aanbiedingen:

| Segmentgrootte | Eind-aan-eind verwerkingstijd |
|--------------|----------------------------|
| 10.000 profielen of minder | 7 minuten |
| 1 miljoen profielen of minder | 30 minuten |
| 15 miljoen profielen of minder | 50 minuten |

Zonder frequentiegrens voor in aanmerking komende aanbiedingen:

| Segmentgrootte | Eind-aan-eind verwerkingstijd |
|--------------|----------------------------|
| 10.000 profielen of minder | 6 minuten |
| 1 miljoen profielen of minder | 8 minuten |
| 15 miljoen profielen of minder | 16 minuten |

## Een taakaanvraag dupliceren {#duplicate}

U kunt gegevens van een bestaande taak opnieuw gebruiken om een nieuwe aanvraag te maken.

Klik hiertoe op het pictogram voor dupliceren, bewerk indien nodig de taakgegevens en klik op **[!UICONTROL Create]** om de nieuwe aanvraag te maken.

![](assets/batch-duplicate.png)
