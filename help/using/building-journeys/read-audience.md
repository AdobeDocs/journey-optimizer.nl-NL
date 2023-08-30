---
solution: Journey Optimizer
product: journey optimizer
title: Een publiek gebruiken voor een reis
description: Leer hoe u een publiek kunt gebruiken op een reis
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: activiteit, reis, lezen, publiek, platform
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 392bd63b666e4db72c2865e4b7134bb3c1711816
workflow-type: tm+mt
source-wordcount: '1344'
ht-degree: 3%

---

# Een publiek gebruiken voor een reis {#segment-trigger-activity}

## Een activiteit van het leespubliek toevoegen {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Activiteit publiek lezen"
>abstract="Met de activiteit &#39;Lezen publiek&#39; kunt u alle personen die tot een Adobe Experience Platform-publiek behoren een reis laten maken. Het starten van een journey kan één keer, of op regelmatige basis plaatsvinden."

Gebruik de **Publiek lezen** activiteit om alle individuen van een publiek de reis te maken. Het starten van een journey kan één keer, of op regelmatige basis plaatsvinden.

Neem bijvoorbeeld het publiek voor het openen en uitchecken van de Luma-app dat is gemaakt in het dialoogvenster [Stimulerend publiek](../audience/about-audiences.md) use case. Met de activiteit van het Leespubliek, kunt u alle individuen die tot dit publiek behoren tot een reis maken en hen tot geïndividualiseerde reizen maken die alle reisfunctionaliteit, voorwaarden, timers, gebeurtenissen, acties zullen hefboomwerking.

>[!NOTE]
>
>Voor reizen die gebruikmaken van een activiteit van het leespubliek is er een maximumaantal reizen dat precies op hetzelfde moment kan beginnen. Het systeem zal tests uitvoeren, maar u moet vermijden dat meer dan vijf reizen (met Leespubliek, gepland of &quot;zo snel mogelijk&quot; te starten) op precies hetzelfde tijdstip beginnen door deze over een bepaalde tijd te verspreiden, bijvoorbeeld 5 tot 10 minuten uit elkaar.
>
>U kunt gebeurtenisveldgroepen niet gebruiken voor reizen die beginnen met een leespubliek, een kwalificatie Audience of een activiteit voor een zakelijke gebeurtenis.

### De activiteit configureren {#configuring-segment-trigger-activity}

De stappen om de Gelezen activiteit van het Publiek te vormen zijn als volgt:

1. Ontvouw de **[!UICONTROL Orchestration]** categorie en zet een **[!UICONTROL Read Audience]** op uw canvas.

   De activiteit moet als eerste stap van een reis worden geplaatst.

1. Voeg een **[!UICONTROL Label]** aan de activiteit (facultatief).

1. In de **[!UICONTROL Audience]** en kies Adobe Experience Platform-publiek dat de reis zal betreden. Klik vervolgens op **[!UICONTROL Save]**.

   U kunt de kolommen in de lijst aanpassen en sorteren.

   >[!NOTE]
   >
   >Alleen de personen met de **Realistisch** en **Bestaande** de status van de publieksparticipatie zal de reis betreden . Raadpleeg voor meer informatie over het evalueren van een publiek de [Documentatie voor segmentatieservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

   ![](assets/read-segment-selection.png)

   Als het publiek eenmaal is toegevoegd, wordt de opdracht **[!UICONTROL Copy]** kunt u de naam en de id kopiëren:

   `{"name":"Luma app opening and checkout","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. In de **[!UICONTROL Namespace]** gebruiken, kiest u de naamruimte die u wilt gebruiken om de personen te identificeren. Het veld wordt standaard voorgevuld met de laatst gebruikte naamruimte. [Meer informatie over naamruimten](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Personen die tot een publiek behoren dat niet de geselecteerde identiteit (naamruimte) onder hun verschillende identiteiten heeft, kunnen de reis niet betreden. U kunt alleen een naamruimte selecteren die is gebaseerd op personen. Als u een naamruimte voor een opzoektabel hebt gedefinieerd (bijvoorbeeld: ProductID-naamruimte voor een productzoekopdracht), is deze niet beschikbaar in het dialoogvenster **Naamruimte** vervolgkeuzelijst.

1. Stel de **[!UICONTROL Reading rate]**. Dit is het maximumaantal profielen dat de reis per seconde kan ingaan. Dit tarief geldt alleen voor deze activiteit en niet voor andere activiteiten op de reis. Als u bijvoorbeeld een vertragingsfactor voor aangepaste handelingen wilt definiëren, moet u de vertragings-API gebruiken. Zie dit [page](../configuration/throttling.md).

   Deze waarde wordt opgeslagen in de lading van de reisversie. De standaardwaarde is 5.000 profielen per seconde. U kunt deze waarde wijzigen van 500 tot 20.000 profielen per seconde.

   >[!NOTE]
   >
   >De algemene leessnelheid per sandbox is ingesteld op 20.000 profielen per seconde. De leessnelheid van alle leessoorten die tegelijkertijd in dezelfde sandbox worden uitgevoerd, kan daarom maximaal 20.000 profielen per seconde bedragen. U kunt dit uiteinde niet wijzigen.

1. De **[!UICONTROL Read Audience]** U kunt de tijd opgeven waarop het publiek de reis zal betreden. Om dit te doen, klik **[!UICONTROL Edit journey schedule]** verbinding om tot de eigenschappen van de reis toegang te hebben, dan vorm **[!UICONTROL Scheduler type]** veld.

   ![](assets/read-segment-schedule.png)

   Het publiek betreedt standaard de reis **[!UICONTROL As soon as possible]**. Als u wilt dat het publiek de reis op een specifieke datum/tijd of op een terugkomende basis ingaat, selecteer de gewenste waarde van de lijst.

   >[!NOTE]
   >
   >Let erop dat de **[!UICONTROL Schedule]** -sectie is alleen beschikbaar als een **[!UICONTROL Read Audience]** activiteit is weggelaten op het canvas.

   ![](assets/read-segment-schedule-list.png)

   **Incrementeel lezen** optie: wanneer een reis met een terugkerende **Lees publiek** voert voor het eerst uit, alle profielen in het publiek gaan de reis in. Met deze optie kunt u zich na de eerste keer richten op alleen de personen die het publiek zijn binnengekomen sinds de laatste uitvoering van de reis.

   **Herkomst forceren bij herhaling**: met deze optie kunt u alle profielen die zich nog in de reis bevinden, automatisch laten afsluiten bij de volgende uitvoering. Als u bijvoorbeeld een wachttijd van twee dagen hebt op een dagelijkse terugkerende reis door deze optie in te schakelen, worden profielen altijd verplaatst bij de volgende uitvoering van de reis (dus de dag erna), ongeacht of ze zich in het volgende publiek bevinden of niet. Als de levensduur van uw profielen tijdens deze reis langer kan zijn dan de herhalingsfrequentie, activeer deze optie niet om ervoor te zorgen dat profielen hun reis kunnen voltooien.

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
>Eenmalig Leespubliek reizen 30 dagen na de uitvoering van de reis over naar de voltooide status. Voor een gepland leespubliek duurt het 30 dagen na de uitvoering van het laatste exemplaar.

### De journey testen en publiceren {#testing-publishing}

De **[!UICONTROL Read Audience]** met deze activiteit kunt u de reis testen op een uniform profiel of op 100 willekeurig gekozen testprofielen uit de profielen die voor het publiek in aanmerking komen .

Hiervoor activeert u de testmodus en selecteert u de gewenste optie in het linkerdeelvenster.

![](assets/read-segment-test-mode.png)

U kunt de testwijze dan vormen en in werking stellen zoals gebruikelijk. [Leer hoe u een reis test](testing-the-journey.md).

Als de test eenmaal is uitgevoerd, wordt **[!UICONTROL Show logs]** met de knop kunt u de testresultaten bekijken volgens de geselecteerde testoptie:

* **[!UICONTROL Single profile at a time]**: de teststammen geven dezelfde informatie weer als wanneer de monitaire testmodus wordt gebruikt. Raadpleeg [deze sectie](testing-the-journey.md#viewing_logs) voor meer informatie

* **[!UICONTROL Up to 100 profiles at once]**: Met de testlogboeken kunt u de voortgang van de publieksexport vanuit Adobe Experience Platform bijhouden, evenals de individuele voortgang van alle personen die de reis hebben betreden.

  Houd er rekening mee dat u door het testen van de reis met maximaal 100 profielen tegelijk de voortgang van de individuele personen op de reis niet kunt bijhouden met behulp van de visuele stroom.

  ![](assets/read-segment-log.png)

Wanneer de tests succesvol zijn, kunt u uw reis publiceren (zie [De reis publiceren](publishing-the-journey.md)). Personen die tot de doelgroep behoren, nemen de reis op de in de eigendommen van de reis aangegeven datum/tijd in **[!UICONTROL Scheduler]** sectie.

>[!NOTE]
>
>Voor terugkerende, op het publiek gebaseerde reizen zal de reis automatisch sluiten zodra zijn laatste voorkomen wordt uitgevoerd. Als er geen einddatum/tijd is opgegeven, moet u de reis naar nieuwe ingangen handmatig sluiten om deze te beëindigen.

## Doelgerichtheid van het publiek bij reizen op basis van het publiek

Reizen op basis van het publiek beginnen altijd met een **Publiek lezen** activiteit om personen op te halen die tot een Adobe Experience Platform-publiek behoren.

Het publiek dat bij het publiek hoort, wordt één keer of op regelmatige basis opgehaald.

Na het betreden van de reis, kunt u publiek tot stand brengen orkestgebruik gevallen, die individuen van het aanvankelijke publiek in verschillende takken van de reis leiden.

**Segmentering**

U kunt voorwaarden gebruiken om segmentatie uit te voeren gebruikend **Voorwaarde** activiteit. U kunt VIP personen bijvoorbeeld een bepaald pad laten maken en niet-VIP laten doorlopen in een ander pad.

De segmentatie kan worden gebaseerd op:

* gegevensbrongegevens
* de context van de gebeurtenissen maakt deel uit van de reisgegevens , bijvoorbeeld : heeft iemand op het bericht geklikt dat een uur geleden werd ontvangen ?
* een datum, bijvoorbeeld: zijn we in juni wanneer iemand de reis doorloopt?
* een tijd , bijvoorbeeld : is het &#39; s morgens in de tijdzone van de betrokkene ?
* een algoritme waarin het publiek dat de reis volgt wordt gesplitst op basis van een percentage , bijvoorbeeld : 90 % - 10 % om een controlegroep uit te sluiten

![](assets/read-segment-audience1.png)

**Uitsluiting**

Hetzelfde **Voorwaarde** de activiteit die voor segmentatie wordt gebruikt (zie hierboven) staat u ook toe om een deel van de bevolking uit te sluiten. U kunt bijvoorbeeld VIP personen uitsluiten door ze na afloop naar een vertakking te laten gaan met een eindstap.

Deze uitsluiting kan direct na het opvragen van het publiek gebeuren, voor het tellen van de bevolking of langs een reis in meerdere stappen.

![](assets/read-segment-audience2.png)

**Samenvoeging**

Met ritten kunt u N-vertakkingen maken en deze na een segmentatie samenvoegen.

Hierdoor kunt u twee soorten publiek terugbrengen naar een algemene ervaring.

Zo kunnen VIP en niet-VIP klanten na een andere ervaring gedurende tien dagen op een reis terugkeren naar hetzelfde pad.

Na een vereniging, kunt u het publiek opnieuw verdelen door een segmentatie of een uitsluiting uit te voeren.

![](assets/read-segment-audience3.png)
