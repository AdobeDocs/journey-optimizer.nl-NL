---
title: Een segment gebruiken in een journey
description: Leer hoe u een segment kunt gebruiken tijdens een reis
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: a5a3b23228a56cb16935dbc0f4d26d4a666d8fd2
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 4%

---

# Een segment gebruiken in een journey {#segment-trigger-activity}

## Informatie over de activiteit Leessegment {#about-segment-trigger-actvitiy}

Met de activiteit Leessegment kunt u alle personen die tot een Adobe Experience Platform-segment behoren een reis laten maken. Het starten van een journey kan één keer, of op regelmatige basis plaatsvinden.

Neem bijvoorbeeld het segment voor het openen en uitchecken van de Luma-app dat is gemaakt in het gebruiksscenario [Build segments](../segment/about-segments.md). Met de activiteit van het Leessegment, kunt u alle individuen die tot dit segment behoren een reis maken en hen tot geïndividualiseerde reizen maken die alle reisfunctionaliteit gebruiken: voorwaarden, timers, gebeurtenissen, handelingen.

>[!NOTE]
>
>Met de Burst Betaalde add-on kunt u zeer snel pushberichten verzenden in grote volumes voor eenvoudige reizen die een leessegment en een eenvoudig pushbericht bevatten. Raadpleeg [deze sectie](../building-journeys/journey-gs.md#burst) voor meer informatie

### De activiteit configureren {#configuring-segment-trigger-activity}

De stappen om de activiteit van het Leessegment te vormen zijn als volgt:

1. Ontvouw de **[!UICONTROL Orchestration]** categorie en laat vallen een **[!UICONTROL Read Segment]** activiteit in uw canvas.

   De activiteit moet als eerste stap van een reis worden geplaatst.

1. Voeg een **[!UICONTROL Label]** aan de activiteit (facultatief) toe.

1. Kies in het veld **[!UICONTROL Segment]** het Adobe Experience Platform-segment dat de rit moet ingaan en klik vervolgens op **[!UICONTROL Save]**.

   U kunt de kolommen in de lijst aanpassen en sorteren.

   >[!NOTE]
   >
   >Alleen de personen met de **Realized** en **Existing**-deelnamestatus zullen de reis betreden. Voor meer op hoe te om een segment te evalueren, verwijs naar [de documentatie van de Dienst van de Segmentatie ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.

   ![](../assets/read-segment-selection.png)

   Zodra het segment wordt toegevoegd, staat **[!UICONTROL Copy]** knoop u toe om zijn naam en identiteitskaart te kopiëren:

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](../assets/read-segment-copy.png)

1. Kies in het veld **[!UICONTROL Namespace]** de naamruimte die u wilt gebruiken om de personen te identificeren. [Meer informatie over naamruimten](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Personen die behoren tot een segment dat niet de geselecteerde identiteit (naamruimte) onder hun verschillende identiteiten heeft, kunnen de reis niet betreden.

1. Stel het veld **[!UICONTROL Throttling rate]** in op de productielimiet van de activiteit van het gelezen segment.

   Deze waarde wordt opgeslagen in de lading van de reisversie. De standaardwaarde is 17.000 berichten per seconde. U kunt deze waarde wijzigen van 500 tot 17.000 berichten per seconde.

   >[!NOTE]
   >
   >De totale vertragingssnelheid per sandbox is ingesteld op 20.000 berichten per seconde. Daarom voegt de vertragingssnelheid van alle gelezen segmenten die gelijktijdig in de zelfde zandbak lopen tot hoogstens 20.000 berichten per seconde toe. U kunt dit uiteinde niet wijzigen.

1. Met de **[!UICONTROL Read Segment]**-activiteit kunt u opgeven op welk tijdstip het segment de reis moet betreden. Om dit te doen, klik **[!UICONTROL Edit journey schedule]** verbinding om tot de eigenschappen van de reis toegang te hebben, dan vorm **[!UICONTROL Scheduler type]** gebied.

   ![](../assets/read-segment-schedule.png)

   Standaard voeren segmenten de reis **[!UICONTROL As soon as possible]** in. Als u wilt dat het segment de reis op een specifieke datum/tijd of op een terugkomende basis ingaat, selecteer de gewenste waarde van de lijst.

   >[!NOTE]
   >
   >De sectie **[!UICONTROL Schedule]** is alleen beschikbaar wanneer een activiteit **[!UICONTROL Read Segment]** op het canvas is neergezet.

   ![](../assets/read-segment-schedule-list.png)

### De journey testen en publiceren {#testing-publishing}

Met de **[!UICONTROL Read Segment]**-activiteit kunt u de reis testen op een uniform profiel of op 100 willekeurig gekozen testprofielen uit de profielen die voor het segment in aanmerking komen.

Hiervoor activeert u de testmodus en selecteert u de gewenste optie in het linkerdeelvenster.

![](../assets/read-segment-test-mode.png)

U kunt de testwijze dan vormen en in werking stellen zoals gebruikelijk. [Leer hoe je een reis](testing-the-journey.md) test.

Wanneer de test is uitgevoerd, kunt u met de knop **[!UICONTROL Show logs]** de testresultaten weergeven volgens de geselecteerde testoptie:

* **[!UICONTROL Single profile at a time]**: de teststammen bevatten dezelfde informatie als wanneer de monitaire testmodus wordt gebruikt. Raadpleeg [deze sectie](testing-the-journey.md#viewing_logs) voor meer informatie

* **[!UICONTROL Up to 100 profiles at once]**: Aan de hand van de testlogboeken kunt u de voortgang van de segmentexport vanuit Adobe Experience Platform volgen, evenals de individuele voortgang van alle personen die de reis hebben betreden.

   Houd er rekening mee dat u door het testen van de reis met maximaal 100 profielen tegelijk de voortgang van de individuele personen op de reis niet kunt bijhouden met behulp van de visuele stroom.

   ![](../assets/read-segment-log.png)

Zodra de tests succesvol zijn, kunt u uw reis publiceren (zie [Het publiceren van de reis](publishing-the-journey.md)). Personen die tot het segment behoren, komen de reis binnen op de datum/tijd die in de sectie **[!UICONTROL Scheduler]** in de eigendommen van de reis is vermeld.

>[!NOTE]
>
>Voor terugkerende segmentreizen wordt de reis automatisch beëindigd zodra de laatste reis is uitgevoerd. Als er geen einddatum/tijd is opgegeven, moet u de reis naar nieuwe ingangen handmatig sluiten om deze te beëindigen.


## Publiek gericht op segmentreizen

Op segmenten gebaseerde reizen beginnen altijd met een **Leessegment** activiteit om individuen op te halen die tot een segment van Adobe Experience Platform behoren.

Het publiek dat tot het segment behoort, wordt één keer of op regelmatige basis opgehaald.

Na het ingaan van de reis, kunt u publiek tot stand brengen orkestgebruik gevallen, die individuen van het aanvankelijke segment in verschillende takken van de reis maken.

**Segmentering**

U kunt voorwaarden gebruiken om segmentatie uit te voeren gebruikend **Condition** activiteit. U kunt VIP personen bijvoorbeeld een bepaald pad laten maken en niet-VIP laten doorlopen in een ander pad.

De segmentatie kan worden gebaseerd op:

* gegevensbrongegevens
* de context van de gebeurtenissen, deel van de reisgegevens, bijvoorbeeld: heeft iemand op het bericht geklikt dat ze een uur geleden heeft ontvangen ?
* een datum, bijvoorbeeld: zijn we in juni wanneer iemand de reis doorgaat?
* een tijd, bijvoorbeeld: is het morgenochtend in de tijdzone van de persoon ?
* een algoritme waarin het publiek dat de reis volgt wordt gesplitst op basis van een percentage, bijvoorbeeld: 90% - 10% om een controlegroep uit te sluiten

![](../assets/read-segment-audience1.png)

**Uitsluiting**

Met dezelfde **Condition**-activiteit die wordt gebruikt voor segmentatie (zie boven) kunt u ook een deel van de populatie uitsluiten. U kunt bijvoorbeeld VIP personen uitsluiten door ze na afloop naar een vertakking te laten gaan met een eindstap.

Deze uitsluiting zou direct na het opvragen van segmenten kunnen plaatsvinden, voor het tellen van de bevolking of langs een reis met meerdere stappen.

![](../assets/read-segment-audience2.png)

**Samenvoeging**

Met ritten kunt u N-vertakkingen maken en deze na een segmentatie samenvoegen.

Hierdoor kunt u twee soorten publiek terugbrengen naar een algemene ervaring.

Zo kunnen VIP en niet-VIP klanten na een andere ervaring gedurende tien dagen op een reis terugkeren naar hetzelfde pad.

Na een vereniging, kunt u het publiek opnieuw verdelen door een segmentatie of een uitsluiting uit te voeren.

![](../assets/read-segment-audience3.png)
