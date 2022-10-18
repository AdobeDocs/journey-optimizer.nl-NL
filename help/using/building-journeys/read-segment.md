---
title: Een segment gebruiken in een journey
description: Leer hoe u een segment kunt gebruiken tijdens een reis
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 15dc5e2854358f7f200a54a3f06fa6e98f146efe
workflow-type: tm+mt
source-wordcount: '1253'
ht-degree: 4%

---

# Een segment gebruiken in een journey {#segment-trigger-activity}

## Een activiteit van het leessegment toevoegen {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Segmentactiviteit lezen"
>abstract="Met de activiteit Leessegment kunt u alle personen die tot een Adobe Experience Platform-segment behoren een reis laten maken. Het starten van een journey kan één keer, of op regelmatige basis plaatsvinden."

Gebruik de **Segment lezen** activiteit om alle individuen van een segment de reis te maken. Het starten van een journey kan één keer, of op regelmatige basis plaatsvinden.

Neem bijvoorbeeld het segment voor het openen en uitchecken van de Luma-app dat is gemaakt in het dialoogvenster [Segmenten maken](../segment/about-segments.md) use case. Met de activiteit van het Leessegment, kunt u alle individuen die tot dit segment behoren een reis maken en hen tot geïndividualiseerde reizen maken die alle reisfunctionaliteit gebruiken: voorwaarden, timers, gebeurtenissen, handelingen.

>[!NOTE]
>
>Voor ritten die een activiteit van het Leessegment gebruiken, is er een maximumaantal reizen dat op het nauwkeurige zelfde ogenblik kan beginnen. Het systeem voert de controles uit, maar vermijd dat meer dan vijf reizen (met Leessegment, gepland of &quot;zo snel mogelijk&quot; te starten) op hetzelfde tijdstip beginnen door ze over een bepaalde tijd te verspreiden, bijvoorbeeld 5 tot 10 minuten na elkaar.
>
>U kunt gebeurtenisveldgroepen niet gebruiken voor reizen die beginnen met een Leessegment, een Segmentkwalificatie of een zakelijke gebeurtenisactiviteit.

### De activiteit configureren {#configuring-segment-trigger-activity}

De stappen om de activiteit van het Leessegment te vormen zijn als volgt:

1. De **[!UICONTROL Orchestration]** categorie en een **[!UICONTROL Read Segment]** op uw canvas.

   De activiteit moet als eerste stap van een reis worden geplaatst.

1. Voeg een **[!UICONTROL Label]** aan de activiteit (facultatief).

1. In de **[!UICONTROL Segment]** het gebied, kies het segment van Adobe Experience Platform dat de reis zal ingaan, dan klik **[!UICONTROL Save]**.

   U kunt de kolommen in de lijst aanpassen en sorteren.

   >[!NOTE]
   >
   >Alleen personen met de **Gerealiseerd** en **Bestaande** de deelnamestatistieken van de segmenten zullen de reis betreden . Raadpleeg voor meer informatie over het evalueren van een segment de [Documentatie voor segmentatieservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.

   ![](assets/read-segment-selection.png)

   Nadat het segment is toegevoegd, wordt het **[!UICONTROL Copy]** kunt u de naam en de id kopiëren:

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. In de **[!UICONTROL Namespace]** gebruiken, kiest u de naamruimte die u wilt gebruiken om de personen te identificeren. [Meer informatie over naamruimten](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Personen die behoren tot een segment dat niet de geselecteerde identiteit (naamruimte) onder hun verschillende identiteiten heeft, kunnen de reis niet betreden.

1. Stel de **[!UICONTROL Throttling rate]** gebied aan de productiegrens van de gelezen segmentactiviteit.

   Deze waarde wordt opgeslagen in de lading van de reisversie. De standaardwaarde is 20.000 berichten per seconde. U kunt deze waarde wijzigen van 500 tot 20.000 berichten per seconde.

   >[!NOTE]
   >
   >De totale vertragingssnelheid per sandbox is ingesteld op 20.000 berichten per seconde. Daarom voegt de vertragingssnelheid van alle gelezen segmenten die gelijktijdig in de zelfde zandbak lopen tot hoogstens 20.000 berichten per seconde toe. U kunt dit uiteinde niet wijzigen.

1. De **[!UICONTROL Read Segment]** de activiteit staat u toe om de tijd te specificeren waarop het segment de reis zal ingaan. Om dit te doen, klik **[!UICONTROL Edit journey schedule]** verbinding om tot de eigenschappen van de reis toegang te hebben, dan vorm **[!UICONTROL Scheduler type]** veld.

   ![](assets/read-segment-schedule.png)

   De segmenten gaan standaard de reis in **[!UICONTROL As soon as possible]**. Als u wilt dat het segment de reis op een specifieke datum/tijd of op een terugkomende basis ingaat, selecteer de gewenste waarde van de lijst.

   >[!NOTE]
   >
   >De **[!UICONTROL Schedule]** -sectie alleen beschikbaar als een **[!UICONTROL Read Segment]** activiteit is weggelaten op het canvas.

   ![](assets/read-segment-schedule-list.png)

   **Incrementeel lezen** optie: wanneer een reis met terugkerende **Segment lezen** voert voor het eerst uit, alle profielen in het segment de reis ingaan. Met deze optie kunt u zich na de eerste keer richten op alleen de personen die het segment hebben betreden sinds de laatste uitvoering van de reis.

   **Herkomst forceren bij herhaling**: met deze optie kunt u alle profielen die nog aanwezig zijn op de reis automatisch laten afsluiten bij de volgende uitvoering. Als u bijvoorbeeld een wachttijd van twee dagen hebt op een dagelijkse terugkerende reis door deze optie in te schakelen, worden profielen altijd verplaatst bij de volgende uitvoering van de reis (dus de dag erna), ongeacht of ze zich in het volgende publiek bevinden of niet. Als de levensduur van uw profielen tijdens deze reis langer kan zijn dan de herhalingsfrequentie, activeer deze optie niet om ervoor te zorgen dat profielen hun reis kunnen voltooien.

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

>[!NOTE]
>
>Eenmalig Leessegment-reizen gaan 30 dagen na de uitvoering van de reis over naar de voltooide status. Voor geplande Gelezen segmenten, is het 30 dagen na de uitvoering van het laatste voorkomen.

### De journey testen en publiceren {#testing-publishing}

De **[!UICONTROL Read Segment]** met deze activiteit kunt u de reis testen op een uniform profiel of op 100 willekeurig gekozen testprofielen uit de profielen die voor het segment in aanmerking komen.

Hiervoor activeert u de testmodus en selecteert u de gewenste optie in het linkerdeelvenster.

![](assets/read-segment-test-mode.png)

U kunt de testwijze dan vormen en in werking stellen zoals gebruikelijk. [Leer hoe u een reis test](testing-the-journey.md).

Als de test eenmaal is uitgevoerd, wordt **[!UICONTROL Show logs]** met de knop kunt u de testresultaten bekijken volgens de geselecteerde testoptie:

* **[!UICONTROL Single profile at a time]**: de teststammen bevatten dezelfde informatie als wanneer de monitaire testmodus wordt gebruikt. Raadpleeg [deze sectie](testing-the-journey.md#viewing_logs) voor meer informatie

* **[!UICONTROL Up to 100 profiles at once]**: Aan de hand van de testlogboeken kunt u de voortgang van de segmentexport vanuit Adobe Experience Platform volgen, evenals de individuele voortgang van alle personen die de reis hebben betreden.

   Houd er rekening mee dat u door het testen van de reis met maximaal 100 profielen tegelijk de voortgang van de individuele personen op de reis niet kunt bijhouden met behulp van de visuele stroom.

   ![](assets/read-segment-log.png)

Wanneer de tests succesvol zijn, kunt u uw reis publiceren (zie [De reis publiceren](publishing-the-journey.md)). Personen die tot het segment behoren, komen de reis binnen op de datum/tijd die in de eigendommen van de reis is vermeld **[!UICONTROL Scheduler]** sectie.

>[!NOTE]
>
>Voor terugkerende segmentreizen wordt de reis automatisch beëindigd zodra de laatste reis is uitgevoerd. Als er geen einddatum/tijd is opgegeven, moet u de reis naar nieuwe ingangen handmatig sluiten om deze te beëindigen.

## Publiek gericht op segmentreizen

Segmentreizen beginnen altijd met een **Segment lezen** activiteiten om personen op te halen die tot een Adobe Experience Platform-segment behoren.

Het publiek dat tot het segment behoort, wordt één keer of op regelmatige basis opgehaald.

Na het ingaan van de reis, kunt u publiek tot stand brengen orkestgebruik gevallen, die individuen van het aanvankelijke segment in verschillende takken van de reis maken.

**Segmentering**

U kunt voorwaarden gebruiken om segmentatie uit te voeren gebruikend **Voorwaarde** activiteit. U kunt VIP personen bijvoorbeeld een bepaald pad laten maken en niet-VIP laten doorlopen in een ander pad.

De segmentatie kan worden gebaseerd op:

* gegevensbrongegevens
* de context van de gebeurtenissen, deel van de reisgegevens, bijvoorbeeld: heeft iemand op het bericht geklikt dat een uur geleden is ontvangen ?
* een datum, bijvoorbeeld: zijn we in juni wanneer iemand de reis doorgaat?
* een tijd, bijvoorbeeld: is het morgenochtend in de tijdzone van de persoon ?
* een algoritme waarin het publiek dat de reis volgt wordt gesplitst op basis van een percentage, bijvoorbeeld: 90% - 10% om een controlegroep uit te sluiten

![](assets/read-segment-audience1.png)

**Uitsluiting**

Hetzelfde **Voorwaarde** de activiteit die voor segmentatie wordt gebruikt (zie hierboven) staat u ook toe om een deel van de bevolking uit te sluiten. U kunt bijvoorbeeld VIP personen uitsluiten door ze na afloop naar een vertakking te laten lopen met een eindstap.

Deze uitsluiting zou direct na het opvragen van segmenten kunnen plaatsvinden, voor het tellen van de bevolking of langs een reis met meerdere stappen.

![](assets/read-segment-audience2.png)

**Samenvoeging**

Met ritten kunt u N-vertakkingen maken en deze na een segmentatie samenvoegen.

Hierdoor kunt u twee soorten publiek terugbrengen naar een algemene ervaring.

Zo kunnen VIP en niet-VIP klanten na een andere ervaring gedurende tien dagen op een reis terugkeren naar hetzelfde pad.

Na een vereniging, kunt u het publiek opnieuw verdelen door een segmentatie of een uitsluiting uit te voeren.

![](assets/read-segment-audience3.png)
