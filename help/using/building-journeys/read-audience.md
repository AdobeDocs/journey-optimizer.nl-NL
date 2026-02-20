---
solution: Journey Optimizer
product: journey optimizer
title: Een publiek gebruiken voor een reis
description: Leer hoe te om de Gelezen activiteit van het Publiek te vormen en te gebruiken om individuen van  [!DNL Adobe Experience Platform]  publiek te maken reizen ingaan.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: activiteit, reis, gelezen publiek, publiek, segment, partij, ingangspunt, trekker, programma, de Kwalificatie van het publiek
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
version: Journey Orchestration
source-git-commit: 76f2563d415b3f82e231837566b20d9586166876
workflow-type: tm+mt
source-wordcount: '3541'
ht-degree: 0%

---

# Een publiek gebruiken voor een reis {#segment-trigger-activity}

Gebruik de activiteit van het publiek lezen om reizen met bepaald publiek te beginnen. U kiest het publiek en wanneer het loopt; dan gebruik voorwaarden, tijdopnemers, en acties om de weg van elk profiel te personaliseren.

## Informatie over de activiteit van het leespubliek {#about-segment-trigger-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Activiteit publiek lezen"
>abstract="Voeg alle gekwalificeerde profielen van een geselecteerd publiek [!DNL Adobe Experience Platform] toe aan deze reis. Voer een keer of volgens een schema uit."

De **Gelezen activiteit van het Publiek** is de reis entry-point activiteit die alle profielen van een geselecteerd [!DNL Adobe Experience Platform] publiek aan een reis toevoegt. U kunt de ingang één keer of op een terugkerend programma in werking stellen. In API&#39;s en technische referenties wordt deze activiteit ook wel segmenttriggers of op het publiek gebaseerde reisgegevens genoemd.

**wanneer te gebruiken Gelezen Publiek vs de Kwalificatie van het Publiek**

| Gebruik **Gelezen Publiek** wanneer | De Kwalificatie van het publiek van het gebruik **[wanneer](audience-qualification-events.md)** |
|----------------------------|-----------------------------------------------------------------------|
| U wilt een reis één keer of op een programma (partij) in werking stellen. | U hebt profielen nodig om de reis in real time in te gaan aangezien zij kwalificeren. |
| Uw publiek wordt gebatchleerd (bijvoorbeeld dagelijkse momentopname). | Uw publiek streamt of is gebaseerd op gebeurtenissen. |
| U bent oké met een vertraging tussen de evaluatie van het publiek en de ingang van de reis. | U hebt directe invoer nodig wanneer een profiel in aanmerking komt. |

**Zeer belangrijke grenzen:** Één Gelezen Publiek per reis (moet de eerste activiteit zijn); één publiek per activiteit; tot vijf gelijktijdige Gelezen looppas van de Publiek per organisatie; 20.000 profielen per seconde per zandbak; de baanonderbreking van 12 uur. De volledige details in [&#x200B; Grafieken en aanbevelingen &#x200B;](#must-read).

**Eerste vereisten:** Een [!DNL Adobe Experience Platform] publiek dat wordt gebouwd en geëvalueerd (Realized status), een op mensen-gebaseerde identiteit namespace die voor de reis wordt geselecteerd, en-voor het terugkomen looppas-begrip van [&#x200B; het plannen en productiegrenzen &#x200B;](#must-read).

Bijvoorbeeld, kan het `Luma app opening and checkout` publiek dat in [&#x200B; wordt gecreeerd het 2&rbrace; gebruiksgeval van de Bouwstijl van publiek &lbrace;als ingangspunt worden gebruikt. &#x200B;](../audience/about-audiences.md) Alle gekwalificeerde profielen voeren de reis en de vooruitgang door geïndividualiseerde wegen in gebruikend voorwaarden, tijdopnemers, gebeurtenissen, en acties.

➡️ [Ontdek deze functie in video](#video)


>[!CAUTION]
>
>* Alvorens de Gelezen publieksactiviteit te gebruiken, [&#x200B; lees de Grafieken en Beperkingen &#x200B;](#must-read).

## De activiteit configureren {#configuring-segment-trigger-activity}

U zult plaatsen: **Publiek** (verplicht), **Namespace** (verplicht), **Leestarief** (verplicht, gebrek 5.000/s), en **Programma** (wanneer de reis) loopt. Voeg naar keuze a **Etiket** en **Aanvullende herkenningsteken** toe. Met de onderstaande stappen doorloopt u elke instelling.

### Activiteiten toevoegen en publiek selecteren {#add-activity-and-select-audience}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_label"
>title="Label"
>abstract="Facultatief etiket om deze activiteit in rapportering en testwijzelogboeken te identificeren."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_audience"
>title="Doelgroep"
>abstract="Selecteer het publiek van [!DNL Adobe Experience Platform] waarvan de profielen deze reis zullen ingaan."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_namespace"
>title="Naamruimte"
>abstract="Kies welke identiteit (bijvoorbeeld e-mail, ECID) wordt gebruikt om personen die de reis binnenkomen te identificeren. Kies de bovenste optie in de lijst voor de beste compatibiliteit met Business Rules en Capping."

1. Ontgrendel de categorie **[!UICONTROL Orchestration]** en zet een **[!UICONTROL Read Audience]** -activiteit neer op uw canvas.

   De activiteit moet als eerste stap van een reis worden geplaatst.

1. Voeg een **[!UICONTROL Label]** toe aan de activiteit (optioneel). Met een optioneel label kunt u de activiteit in de rapportering en in de logboeken van de testmodus identificeren.

1. Kies in het veld **[!UICONTROL Audience]** het [!DNL Adobe Experience Platform] -publiek dat de rit zal betreden en klik vervolgens op **[!UICONTROL Save]** . U kunt om het even welk [!DNL Adobe Experience Platform] publiek selecteren dat gebruikend [&#x200B; segmentdefinities &#x200B;](../audience/creating-a-segment-definition.md) wordt geproduceerd.

   >[!NOTE]
   >
   >Bovendien kunt u [!DNL Adobe Experience Platform] publiek richten dat gebruikend [&#x200B; wordt gecreeerd publiekssamenstellingen &#x200B;](../audience/get-started-audience-orchestration.md).
   >U kunt publiek ook richten [&#x200B; geupload van een Csv- dossier &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}.
   >[&#x200B; Leer meer over hoe te om publiek in Journey Optimizer te produceren en te richten &#x200B;](../audience/about-audiences.md).

   U kunt de kolommen in de lijst aanpassen en sorteren.

   ![&#x200B; de selectieinterface die van het publiek beschikbaar [!DNL Adobe Experience Platform] publiek toont &#x200B;](assets/read-segment-selection.png)

   Nadat het publiek is toegevoegd, kunt u met de knop **[!UICONTROL Copy]** de naam en de id van het publiek kopiëren:

   `{"name":"Luma app opening and checkout","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![&#x200B; knoop van het Exemplaar om publieksnaam en identiteitskaart in formaat te kopiëren JSON &#x200B;](assets/read-segment-copy.png)

   >[!NOTE]
   >
   >Slechts zullen de individuen met de **Realized** status van de publieksparticipatie de reis ingaan. Voor meer op hoe te om een publiek te evalueren, verwijs naar de [&#x200B; documentatie van de Dienst van de Segmentatie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. Kies in het veld **[!UICONTROL Namespace]** de naamruimte die u wilt gebruiken om de personen te identificeren. Het veld wordt standaard voorgevuld met de laatst gebruikte naamruimte. [&#x200B; Leer meer over namespaces &#x200B;](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Personen die tot een publiek behoren dat niet de geselecteerde identiteit (naamruimte) onder hun verschillende identiteiten heeft, kunnen de reis niet betreden. U kunt alleen een naamruimte selecteren die is gebaseerd op personen. Als u een namespace voor een raadplegingslijst (bijvoorbeeld: ProductID namespace voor een raadpleging van het Product) hebt bepaald, zal het niet in **Namespace** dropdown lijst beschikbaar zijn.

### Aanvullende identificatiecode {#read-audience-supplemental-id}

U kunt naar keuze toelaten **Gebruik een supplementaire herkenningsteken** om de reis in de context van een secundair herkenningsteken (bijvoorbeeld, een orde identiteitskaart of boekende identiteitskaart) naast profielidentiteitskaart in werking te stellen Hierdoor zijn meerdere ingangen van hetzelfde profiel mogelijk wanneer de aanvullende id verschilt.

[&#x200B; leer hoe te om supplementaire herkenningstekens in reizen &#x200B;](supplemental-identifier.md) te gebruiken. Voor ritten voor lezers moet de aanvullende id een profielkenmerk zijn; de leessnelheid is beperkt tot 500 profielen per seconde wanneer een aanvullende id wordt gebruikt.

### Guardrails en aanbevelingen {#must-read}

* Er kan slechts één **[!UICONTROL Read Audience]** -activiteit worden gebruikt tijdens een rit en dit moet de eerste activiteit op het canvas zijn.

* De **[!UICONTROL Read audience]** -activiteit kan zich richten op slechts één publiek. Als er meerdere soorten publiek nodig zijn, kunt u die soorten publiek vóór gebruik samenvoegen tot één publiek. [&#x200B; leer hoe te om publiek te combineren gebruikend samenstellingswerkschema&#39;s &#x200B;](../audience/get-started-audience-orchestration.md)

* Voor reizen die a **gebruiken Gelezen de activiteit van het publiek**, is er een maximumaantal reizen dat precies tezelfdertijd kan beginnen. Het systeem voert opnieuw tests uit. Nochtans, vermijd het hebben van meer dan vijf reizen (met **Gelezen Publiek**, gepland of die &quot;zo snel mogelijk&quot;beginnen) tezelfdertijd. De beste manier is om ze over een tijdsverloop te verspreiden, bijvoorbeeld 5 tot 10 minuten na elkaar.

* De groepen van het de gebeurtenisgebied van de ervaring kunnen niet in reizen worden gebruikt die met a **beginnen gelezen publiek** activiteit, een **[kwalificatie van het Publiek](audience-qualification-events.md)** activiteit, of een bedrijfsgebeurtenisactiviteit.

* Als beste praktijken, adviseren wij u slechts partijpubliek in a **Gelezen publiek** activiteit. Dit zal een betrouwbare en consistente telling van de tijdens de reis gebruikte doelgroepen opleveren. Lees het publiek wordt ontworpen voor partijgebruik gevallen. Als uw gebruiksgeval gegevens in real time gelieve vereist te gebruiken {de kwalificatieactiviteit van 0} Audience **[.](audience-qualification-events.md)**

* Het publiek [&#x200B; werd ingevoerd uit een Csv- dossier &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience) of resulterend uit [&#x200B; samenstellingswerkschema&#39;s &#x200B;](../audience/get-started-audience-orchestration.md) kan in de **Gelezen activiteit van het Publiek** worden geselecteerd. Deze doelgroepen zijn niet beschikbaar in de **activiteit van de Kwalificatie van het publiek 0&rbrace;.**

* Gelijktijdige leeslimiet per organisatie: elke organisatie kan maximaal vijf instanties van het type Audience lezen tegelijk uitvoeren. Dit omvat zowel geplande looppas als die teweeggebracht door bedrijfsgebeurtenissen. De limiet geldt voor alle sandboxen en reizen. Deze limiet wordt gehandhaafd om te zorgen voor een eerlijke en evenwichtige toewijzing van middelen in alle organisaties.

* Doorvoerbeheer voor sandbox: het systeem beheert dynamisch de verwerkingsdoorvoer per sandbox met een maximale limiet van 20.000 profielen per seconde die worden gedeeld door alle activiteiten van het leespubliek. De individuele Gelezen activiteiten van het Publiek kunnen met een minimumtarief van 500 profielen per seconde worden gevormd. Als de doorvoergrenzen op sandboxniveau worden bereikt, kunnen de taken in de wachtrij worden geplaatst om een eerlijke toewijzing van bronnen te garanderen.

* Tijdslimiet voor taakverwerking: taken van het type Audience lezen die niet binnen 12 uur kunnen worden verwerkt vanwege de limiet van de guardrail, worden automatisch opgeschoond en nooit uitgevoerd. Dit voorkomt het opbouwen van arbeidsplaatsen en zorgt voor stabiliteit van het systeem.

* Wanneer het gebruiken van partijsegmenten, verzeker uw opname en dagelijkse momentopname werkt ruim vóór de reis begint. Overweeg een extra wachttijdperiode als de segmenten op gegevens moeten wijzen die de zelfde dag worden opgenomen. Als onmiddellijke profielversheid kritiek is, gebruik een gebeurtenis-gebaseerde of het stromen benadering in plaats van een dagelijkse partijbenadering. Alternatief, neem een wachtend mechanisme op om bijgewerkte gegevens toe te staan om vóór de reisevaluatie te verspreiden.

De begeleiding met betrekking tot **Gelezen de activiteit van het publiek** wordt vermeld in [&#x200B; deze pagina &#x200B;](../start/guardrails.md#read-segment-g).

>[!CAUTION]
>
>[&#x200B; Guardrails voor gegevens en segmentatie van het Profiel van de Klant in real time &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html){target="_blank"} zijn ook op [!DNL Adobe Journey Optimizer] van toepassing.

**daarna:** plaats het [&#x200B; lezingstarief &#x200B;](#profile-entry-and-reading-rate) en [&#x200B; programma &#x200B;](#schedule), toen [&#x200B; test en publiceert &#x200B;](#testing-publishing).

### Profielinvoer en leessnelheid {#profile-entry-and-reading-rate}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_reading_rate"
>title="Leesfrequentie"
>abstract="Maximumprofielen die de reis per seconde ingaan (500-20.000). De standaardwaarde is 5.000."

Stel de waarde **[!UICONTROL Reading rate]** (verplicht) in. Dit is het maximumaantal profielen dat de reis per seconde kan ingaan. Dit tarief geldt alleen voor deze activiteit en niet voor andere activiteiten op de reis. Als u bijvoorbeeld een vertragingsfactor voor aangepaste handelingen wilt definiëren, moet u de vertragings-API gebruiken. Verwijs naar deze [&#x200B; pagina &#x200B;](../configuration/throttling.md).

Deze waarde wordt opgeslagen in de lading van de reisversie. De standaardwaarde is 5.000 profielen per seconde. U kunt deze waarde wijzigen van 500 tot 20.000 profielen per seconde.

>[!NOTE]
>
>De algemene leessnelheid per sandbox is ingesteld op 20.000 profielen per seconde. De leessnelheid van alle leessoorten die tegelijkertijd in dezelfde sandbox worden uitgevoerd, kan daarom maximaal 20.000 profielen per seconde bedragen. U kunt dit uiteinde niet wijzigen. Leer meer over de tarieven van de reisverwerking en productie in [&#x200B; deze sectie &#x200B;](entry-management.md#journey-processing-rate).

### Reizen plannen {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_start_date"
>title="Begindatum/-tijd"
>abstract="Bepaal wanneer deze reis moet beginnen."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_repeat_until"
>title="Herhalen tot"
>abstract="Bepaal de einddatum voor terugkomende looppas."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_repeat_every"
>title="Elke herhaling"
>abstract="Hoe vaak de reis loopt (bijvoorbeeld dagelijks, wekelijks)."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_incremental_read"
>title="Incrementeel lezen"
>abstract="Na de eerste run komen alleen nieuwe profielen die aan het publiek zijn toegevoegd, de reis binnen."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_force_reentrance"
>title="Ingang forceren"
>abstract="Wis alle deelnemers van de reis alvorens elk nieuw publiek leest."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_synchronize_audience"
>title="Trigger na batchpublieksevaluatie"
>abstract="Voer de reis pas uit nadat het batchpubliek vers is geëvalueerd."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_synchronize_audience_wait_time"
>title="Wacht op tijd voor nieuwe publieksevaluatie"
>abstract="Hoe lang de reis wacht op nieuwe publieksgegevens (1-6 uur, in minuten of uren)."

Door gebrek, worden de reizen gevormd om eens te lopen. Om een specifieke datum/tijd en frequentie te bepalen waarop de reis zou moeten lopen, volg de hieronder stappen.

>[!NOTE]
>
>Één-schot Gelezen publiekstrajecten bewegen zich aan de **Voltooide** status 91 dagen ([&#x200B; reis globale onderbreking &#x200B;](journey-properties.md#global_timeout)) na de reisuitvoering. Voor een gepland publiek van Lees, is het 91 dagen na de uitvoering van het laatste voorkomen.

1. Selecteer **[!UICONTROL Read audience]** in de eigenschappen van de **[!UICONTROL Edit journey schedule]** -activiteit.

   ![&#x200B; geeft de knoop van het reisschema in Gelezen eigenschappen van de publieksactiviteit uit &#x200B;](assets/read-segment-schedule.png)

1. De eigendommen van de reis worden weergegeven. Selecteer in de vervolgkeuzelijst **[!UICONTROL Scheduler type]** de frequentie waarmee u de reis wilt uitvoeren.

   ![&#x200B; het type dropdown van de Planner met frequentieopties: eens, dagelijks, wekelijks, maandelijks &#x200B;](assets/read-segment-schedule-list.png)

Voor terugkerende reizen zijn specifieke opties beschikbaar om u te helpen de toegang van profielen tot de reis beheren. Vouw de onderstaande secties uit voor meer informatie over elke optie.

![&#x200B; leest publiek terugkomende opties: Incrementele gelezen, Ingang van de Kracht, Trekker na partij &#x200B;](assets/read-audience-options.png)

+++**[!UICONTROL Incremental read]**

Wanneer een reis met een terugkomende **gelezen publiek** voor het eerst uitvoert, gaan alle profielen in het publiek de reis in. Met deze optie kunt u zich na de eerste keer richten op alleen de personen die het publiek zijn binnengekomen sinds de laatste uitvoering van de reis.

Wanneer het gebruiken van deze optie, kijkt het systeem terug **24 uren** van de tijd van de laatste baan van de publieksevaluatie die door de segmenteringsdienst van [!DNL Adobe Experience Platform] wordt uitgevoerd.

Nadat de segmentatie is voltooid, wordt een uitvoertaak voor een profielmomentopname gestart, waarmee Journey Optimizer nieuwe profielen kan detecteren en verwerken. Als de reis tussen deze twee banen gepland is, zal het stijgende lezen geen profielen oppakken die lid van het publiek sinds de laatste uitvoering van de reis werden.

U minimaliseert het risico van ontbrekende profielen door:
* Schakel de optie **[!UICONTROL Trigger after batch audience evaluation]** in om de terugkijkperiode uit te breiden naar het tijdstip van de laatste geslaagde uitvoering van de reis, ongeacht hoelang deze zich heeft voorgedaan
* Reizen plannen die lang moeten duren nadat de dagelijkse batchsegmentatietaken zijn voltooid (doorgaans 2-3 uur buffer)
* Voor tijd-kritieke gebruiksgevallen die directe profielopname vereisen, denk na gebruikend [&#x200B; activiteiten van de Kwalificatie van het publiek 0&rbrace; &lbrace;met het stromen publiek in plaats daarvan](audience-qualification-events.md)

>[!CAUTION]
>
>Als u a [&#x200B; douane richt uploadt publiek &#x200B;](../audience/about-audiences.md#about-segments) in uw reis, worden de profielen slechts teruggewonnen op de eerste herhaling wanneer deze optie in een terugkomende reis wordt toegelaten. Deze doelgroepen zijn vast.

+++

+++**[!UICONTROL Force reentrance on recurrence]**

Met deze optie kunt u alle profielen die nog aanwezig zijn op de reis automatisch laten afsluiten bij de volgende uitvoering.

Als u bijvoorbeeld een wachttijd van twee dagen hebt tijdens een dagelijkse terugkerende reis, worden bij het activeren van deze optie de profielen verplaatst naar de volgende uitvoering van de reis. Dit gebeurt de dag erna, of ze al dan niet in het volgende publiek zitten.

Als de levensduur van uw profielen tijdens deze reis langer kan zijn dan de herhalingsfrequentie, activeer deze optie niet om ervoor te zorgen dat profielen hun reis kunnen voltooien.

+++

+++**[!UICONTROL Trigger after batch audience evaluation]**

Voor ritten die dagelijks worden gepland en die op partijpubliek gericht zijn, kunt u een tijdvenster van tot 6 uren voor de reis bepalen om op nieuwe publieksgegevens van batch segmentatietaken te wachten. Als de segmentatietaak binnen het tijdvenster wordt voltooid, wordt de rit geactiveerd. Anders slaat het de reis over tot de volgende keer. Met deze optie zorgt u ervoor dat reizen worden uitgevoerd met nauwkeurige en actuele publieksgegevens.

Als een reis bijvoorbeeld om 18.00 uur per dag gepland is, kunt u een aantal minuten of uren opgeven die moeten worden gewacht voordat de rit wordt uitgevoerd. Wanneer de reis om 18.00 uur wakker wordt, zoekt het naar een nieuw publiek, wat betekent dat een publiek nieuwer is dan het publiek dat in de vorige uitvoering van de reis werd gebruikt. Tijdens het gespecificeerde tijdvenster, zal de reis onmiddellijk na het ontdekken van het nieuwe publiek uitvoeren. Als geen nieuw publiek wordt ontdekt, zal de reisuitvoering voor die dag worden overgeslagen.

+++

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

## De reis testen en publiceren {#testing-publishing}

Met de **[!UICONTROL Read Audience]** -activiteit kunt u de rit testen op een uniform profiel.

Activeer de testmodus om dit te doen.

![&#x200B; de modusinterface van de Test voor Gelezen activiteit van het Publiek met de selectie van het testprofiel &#x200B;](assets/read-segment-test-mode.png)

Vorm en stel de testwijze in werking zoals gebruikelijk. [&#x200B; leer hoe te om een reis &#x200B;](testing-the-journey.md) te testen.

Wanneer de test is uitgevoerd, kunt u de testresultaten zien met de knop **[!UICONTROL Show logs]** . Voor meer op dit, verwijs naar [&#x200B; deze sectie &#x200B;](testing-the-journey.md#viewing_logs)

![&#x200B; Logboeken van de Test die de resultaten van de publieksuitvoering en profielstroom tonen &#x200B;](assets/read-segment-log.png)

Zodra de tests succesvol zijn, kunt u uw reis publiceren (zie [&#x200B; het Publiceren van de reis &#x200B;](../building-journeys/publish-journey.md)). Personen die tot het publiek behoren, nemen de reis op de datum/tijd in die is opgegeven in de sectie Eigenschappen van de reis **[!UICONTROL Scheduler]** .

>[!NOTE]
>
>Voor terugkerende, op het publiek gebaseerde reizen zal de reis automatisch sluiten zodra zijn laatste voorkomen wordt uitgevoerd. Als er geen einddatum/tijd is opgegeven, moet u de reis naar nieuwe ingangen handmatig sluiten om deze te beëindigen.

## Doelgerichtheid van het publiek bij reizen

De op publiek-gebaseerde reizen beginnen altijd met a **Gelezen activiteit van het publiek** om individuen terug te winnen die tot een [!DNL Adobe Experience Platform] publiek behoren. Deze profielen worden één keer of volgens een terugkerend schema gelezen.

Nadat zij de reis ingaan, organiseert u hen gebruikend **Voorwaarde** activiteiten: segment door attributen of gedrag, sluit een deel van de bevolking uit, of verenigt takken samen (verenigen). In de onderstaande secties wordt elk patroon beschreven.

**Segmentatie**

U kunt voorwaarden gebruiken om segmentatie uit te voeren gebruikend de **Condition** activiteit. U kunt bijvoorbeeld VIP-personen een bepaald pad laten volgen en niet-VIP-stromen in een ander pad.

De segmentatie kan worden gebaseerd op:

* gegevensbrongegevens
* de context van de gebeurtenissen maakt deel uit van de reisgegevens , bijvoorbeeld : heeft iemand op het bericht geklikt dat een uur geleden werd ontvangen ?
* een datum, bijvoorbeeld: zijn we in juni wanneer iemand de reis doorloopt?
* een tijd , bijvoorbeeld : is het &#39; s morgens in de tijdzone van de betrokkene ?
* een algoritme waarin het publiek dat de reis volgt wordt gesplitst op basis van een percentage , bijvoorbeeld : 90 % - 10 % om een controlegroep uit te sluiten

![&#x200B; de activiteit van de Voorwaarde voor publiekssegmentatie in de wegen van VIP en niet-VIP &#x200B;](assets/read-segment-audience1.png)

>[!NOTE]
>
>Wanneer u het plannertype ‘Dagelijks’ gebruikt met een **[!UICONTROL Read Audience]** -activiteit, kunt u een tijdvenster voor de reis definiëren om te wachten op nieuwe publieksgegevens. Dit zorgt ervoor dat u zich nauwkeurig kunt richten en voorkomt problemen die worden veroorzaakt door vertragingen in batchsegmentatietaken. [&#x200B; leer hoe te om een reis &#x200B;](#schedule) te plannen

**Uitsluiting**

De zelfde **activiteit van de Voorwaarde 0&rbrace; &lbrace;die voor segmentatie (zie hierboven) wordt gebruikt staat u ook toe om een deel van de bevolking uit te sluiten.** U kunt bijvoorbeeld VIP-personen uitsluiten door deze naar een vertakking te laten gaan met een eindstap direct erna.

Deze uitsluiting kan direct na het opvragen van het publiek gebeuren, voor het tellen van de bevolking of langs een reis in meerdere stappen.

![&#x200B; weg van de Reis met uitsluitingstak gebruikend de activiteit van het Eind &#x200B;](assets/read-segment-audience2.png)

**Samenvoeging**

Met ritten kunt u N-vertakkingen maken en deze na een segmentatie samenvoegen. Hierdoor kunt u twee soorten publiek terugbrengen naar een algemene ervaring.

Zo kunnen VIP- en niet-VIP-klanten na een andere ervaring gedurende tien dagen op reis terugkeren naar hetzelfde pad. Na een vereniging, kunt u het publiek opnieuw verdelen door een segmentatie of een uitsluiting uit te voeren.

![&#x200B; wegen van de Reis die samen achter na segmentatie samenvoegen gebruikend unie &#x200B;](assets/read-segment-audience3.png)

## Problemen oplossen {#audience-count-mismatch}

Deze sectie helpt u **wanverhoudingen van het kijkcijfer** oplossen (minder of meer profielen die dan verwacht ingaan), **verwerkt nul profielen** (Gelezen alarm van het Publiek of geen ingangen), en **vertraagde of ontbrekende ingangen** (timing en gegevenspropagatie).

>[!NOTE]
>
>Wanneer een activiteit van het publiek lezen uitvoert, produceert het systeem interne gebeurtenissen (genoemd `segmentExportJob` gebeurtenissen) om de levenscyclus van de publieksuitvoer verrichting te volgen. Deze gebeurtenissen worden geregistreerd op het activiteitsniveau, niet per individueel profiel, en kunnen voor controle en het oplossen van problemendoeleinden worden gevraagd. Leer meer over [&#x200B; het vragen Gelezen gebeurtenissen van het Publiek &#x200B;](../reports/query-examples.md#read-segment-queries).

**vind uw kwestie:**

| Symptoom | Ga naar |
|---------|--------|
| Minder (of meer) ingevoerde profielen dan de publieksgrootte | [&#x200B; Timing en gegevenspropagatie &#x200B;](#timing-and-data-propagation), [&#x200B; de bevestiging en controle van Gegevens &#x200B;](#data-validation-and-monitoring) |
| Gesproken publiek lezen heeft nulprofielen verwerkt; waarschuwing geactiveerd | [&#x200B; Nul verwerkte profielen &#x200B;](#zero-profiles-processed) |
| Vermeldingen voor batchpubliek zijn uitgesteld of ontbreken | [&#x200B; Timing en gegevenspropagatie &#x200B;](#timing-and-data-propagation) |
| Status van segmenttaak of naamruimte moet worden geverifieerd | [&#x200B; de bevestiging en controle van Gegevens &#x200B;](#data-validation-and-monitoring) |

### Geen profielen verwerkt {#zero-profiles-processed}

Als de **Gelezen activiteit van het Publiek** geen profiel heeft verwerkt (b.v. u ziet het [&#x200B; Gelezen alarm van het Publiek &#x200B;](../reports/alerts.md#alert-read-audiences)):

1. **Controle als het publiek** - binnen [!DNL Adobe Experience Platform] leeg is, verifieer de publieksgrootte en dat de profielen in **gerealiseerde** status zijn. Een leeg of nog niet geëvalueerd publiek zal in nul ingangen resulteren.
2. **Controle namespace** - namespace die in Gelezen activiteit van het Publiek wordt geselecteerd moet op de profielen in uw publiek aanwezig zijn. Profielen zonder die identiteit kunnen niet op reis. [&#x200B; Leer meer over namespaces &#x200B;](../event/about-creating.md#select-the-namespace).
3. {het 0} Alarm van het Overzicht en herprobeert **- de Mislukkingen worden gemeld in** Alarm **.** Het systeem probeert elke 10 minuten gedurende maximaal 1 uur opnieuw taken te maken. [&#x200B; Leer meer over pogingen en alarm &#x200B;](#read-audience-retry).

Als de kwestie na deze controles voortduurt, zie [&#x200B; Timing en gegevenspropagatie &#x200B;](#timing-and-data-propagation) en [&#x200B; de bevestiging en controle van Gegevens &#x200B;](#data-validation-and-monitoring) voor partij en configuratieoorzaken.

### Tijdstip en gegevensdoorgave {#timing-and-data-propagation}

* **de baanvoltooiing van de segmentatie van de partij**: Voor partijpubliek, zorg ervoor dat de dagelijkse baan van de partijsegmentatie heeft voltooid en de momentopnamen worden bijgewerkt alvorens de reis loopt. Het publiek van de partij wordt klaar voor gebruik ongeveer **2 uren** na de voltooiing van de segmentatietaak. Leer meer over [&#x200B; methodes van de publieksevaluatie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#evaluate-segments){target="_blank"}.

* **de ingangstijdstip van Gegevens**: Verifieer dat de opname van profielgegevens volledig vóór de reisuitvoering heeft voltooid. Als profielen kort voor het begin van de rit werden opgenomen, worden ze mogelijk nog niet in het publiek weergegeven. Leer meer over [&#x200B; gegevensopname in  [!DNL Adobe Experience Platform] &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html){target="_blank"}.

* **Gebruik &quot;Trekker na de optie van de partijpublieksevaluatie&quot;**: Voor dagelijkse geplande reizen die partijpubliek gebruiken, denk na toelatend de **[!UICONTROL Trigger after batch audience evaluation]** optie. Dit zorgt ervoor dat de reis op nieuwe publieksgegevens (tot 6 uur) alvorens uit te voeren wacht. [&#x200B; Leer meer over het plannen &#x200B;](#schedule)

* **voeg een Wacht activiteit** toe: Voor het stromen publiek met onlangs opgenomen gegevens, denk na toevoegend a **wacht** activiteit aan het begin van de reis om tijd voor gegevenspropagatie en profielkwalificatie toe te staan. [&#x200B; Leer meer over de Wacht activiteit &#x200B;](wait-activity.md)

### Gegevensvalidatie {#data-validation-and-monitoring}

* **de status van de segmentatietaak van de Controle**: De tijden van de taakvoltooiing van de partijsegmentatie in [!DNL Adobe Experience Platform] [&#x200B; controledashboard &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/dataflows/ui/monitor-segments.html){target="_blank"}. Gebruik het om te verifiëren wanneer de publieksgegevens klaar zijn.

* **verifieer samenvoegbeleid**: Zorg ervoor dat het fusiebeleid voor uw publiek wordt gevormd het verwachte gedrag aanpast om profielgegevens van verschillende bronnen te combineren. Leer meer over [&#x200B; samenvoegbeleid in  [!DNL Adobe Experience Platform] &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/overview.html){target="_blank"}.

* **de segmentdefinities van het Overzicht**: Bevestig dat de segmentdefinities correct worden gevormd en alle verwachte kwalificatiecriteria omvatten. Leer meer over [&#x200B; bouwend publiek &#x200B;](../audience/creating-a-segment-definition.md). Let vooral op:
   * Op tijd gebaseerde voorwaarden die profielen op tijdstempels van gebeurtenissen kunnen uitsluiten
   * Kenmerkkwalificaties die afhankelijk zijn van recent bijgewerkte gegevens
   * Streaming versus batchevaluatiemethoden

* **bevestigt namespace configuratie**: Verzeker namespace die in **wordt geselecteerd gelezen de activiteit van het publiek** past de primaire identiteit aan die door profielen in uw publiek wordt gebruikt. Profielen zonder de geselecteerde naamruimte worden niet meegenomen. Leer meer over [&#x200B; identiteitsnaamruimten &#x200B;](../event/about-creating.md#select-the-namespace).

### Best practices

* **ritten van het Programma na segmentatie**: Voor partijpubliek, de uitvoering van de planningsreis minstens 2-3 uur na de typische tijd van de baanvoltooiing van de partijsegmentatie. [&#x200B; leer meer over reis het plannen &#x200B;](#schedule)

* **het stromen publiek van het Gebruik voor gebruiksgevallen in real time**: Als u directe profielkwalificatie en reisingang nodig hebt, gebruik [&#x200B; de activiteiten van de Kwalificatie van het Publiek &#x200B;](audience-qualification-events.md) met het stromen publiek in plaats van **Gelezen Publiek** met partijpubliek.

* **Test met kleiner publiek eerst**: Alvorens grote reizen te lanceren, test met een kleinere ondergroep om te bevestigen dat de tellingen gelijke verwachtingen aanpassen. [&#x200B; leer hoe te om een reis &#x200B;](testing-the-journey.md) te testen

* **Monitor regelmatig**: Opstelling regelmatig toezicht op publieksgrootte en de metriek van de reisingang om discrepanties vroeg te ontdekken. Leer meer over [&#x200B; tarieven van de reisverwerking en ingangsbeheer &#x200B;](entry-management.md).

### Wanneer contact opnemen met ondersteuning

Neem contact op met de ondersteuning van Adobe als het aantal aanvragen niet overeenkomt of de uitvoering van het nulprofiel aanhoudt nadat u de bovenstaande stappen hebt uitgevoerd. Heb klaar: publieksnaam/identiteitskaart, reisnaam/identiteitskaart, geplande runtime(s), zandbak, en een korte beschrijving van de discrepantie (b.v. &quot;het publiek toont 10K gerealiseerde, slechts 2K ging de reis op [ datum ] binnen.)

## Opnieuw {#read-audience-retry}

De pogingen worden toegepast door gebrek op publiek-getriggerde reizen (die met a **Gelezen Publiek** of a **BedrijfsGebeurtenis** beginnen) terwijl het terugwinnen van de uitvoerbaan. Als er een fout optreedt tijdens het maken van de exporttaak, worden de pogingen om de 10mn opnieuw uitgevoerd, tot maximaal 1 uur. Daarna zullen we het als een mislukking beschouwen. Deze soorten reizen kunnen daarom tot 1 uur na de geplande tijd worden uitgevoerd.

De onsuccesvolle **Gelezen trekkers van het publiek** worden gevangen en getoond in **Alarm**. Het **Gelezen alarm van het Publiek** waarschuwt u als de a **gelezen activiteit van het Publiek** geen profiel 10 minuten na de geplande uitvoeringstijd heeft verwerkt. Deze fout kan worden veroorzaakt door technische problemen of een leeg publiek. Als de fout te wijten is aan technische problemen, kunnen er nog steeds nieuwe pogingen worden uitgevoerd, afhankelijk van het type uitgave. Als het maken van een exporttaak mislukt, proberen we elke 10 minuten opnieuw gedurende maximaal 1 uur. [Meer informatie](../reports/alerts.md#alert-read-audiences)

## Verwante onderwerpen

* [Stimulerend publiek](../audience/about-audiences.md)
* [Kwalificatieactiviteit van het publiek](audience-qualification-events.md)
* [Aanvullende id&#39;s gebruiken tijdens reizen](supplemental-identifier.md)
* [Reiseigenschappen en -paden](../start/guardrails.md#read-segment-g)
* [Verwerkingssnelheden en toegangsbeheer](entry-management.md)
* [Een journey testen](testing-the-journey.md)
* [Een journey publiceren](../building-journeys/publish-journey.md)

## Hoe kan ik-video {#video}

Begrijp de toepasselijke gebruiksgevallen voor een reis die door de gelezen publieksactiviteit wordt teweeggebracht. Leer hoe u op batches gebaseerde journeys kunt bouwen en welke aanbevolen procedures u kunt toepassen.

>[!VIDEO](https://video.tv.adobe.com/v/3424997?quality=12)
