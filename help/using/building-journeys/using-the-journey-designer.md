---
title: Uw journey ontwerpen
description: Leer hoe u uw reis ontwerpt
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1998f6fc-60fd-4038-8669-39cd55bc02d1
source-git-commit: afd6bec0151eb2c369ae68d369adf98e772841c9
workflow-type: tm+mt
source-wordcount: '1457'
ht-degree: 1%

---

# Uw journey ontwerpen {#design-your-journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_canvas"
>title="Uw journey ontwerpen"
>abstract="Met de interface voor reizen kunt u activiteiten van het palet gemakkelijk naar het canvas slepen. U kunt ook dubbelklikken op een activiteit om deze in het canvas toe te voegen bij de volgende beschikbare stap."

Met de interface voor reizen kunt u activiteiten van het palet gemakkelijk naar het canvas slepen. U kunt ook dubbelklikken op een activiteit om deze in het canvas toe te voegen bij de volgende beschikbare stap. Elke activiteit heeft een specifieke rol en plaats in het proces. De activiteiten worden gesequenceerd. Wanneer een activiteit wordt gebeëindigd, gaat de stroom verder en verwerkt de volgende activiteit, etc.

## Aan de slag met het ontwerpen van de reis {#gs-journey-design}

De **palet** bevindt zich aan de linkerkant van het scherm. Alle beschikbare activiteiten worden ingedeeld in verschillende categorieën: **[!UICONTROL Events]**, **[!UICONTROL Orchestration]** en **[!UICONTROL Actions]**. U kunt de verschillende categorieën uit- of samenvouwen door op de naam ervan te klikken. Als u een activiteit wilt gebruiken tijdens uw reis, sleept u deze van het palet naar het canvas.

Bij het starten van een nieuwe rit worden elementen die niet op het canvas kunnen worden neergezet als de eerste stap, verborgen. Dit heeft betrekking op alle handelingen, de activiteit van de aandoening, de wachttijd en de reactie.

![](assets/journey38.png)

De **[!UICONTROL Filter items]** kunt u de volgende filters weergeven:

* **Alleen beschikbare objecten weergeven**: niet-beschikbare elementen in het palet verbergen of weergeven, bijvoorbeeld gebeurtenissen die een andere naamruimte gebruiken dan de gebeurtenissen die tijdens de reis worden gebruikt. Niet-beschikbare items zijn standaard verborgen. Als u deze weergeeft, worden ze grijs weergegeven.

* **Alleen recente objecten weergeven**: Met dit filter kunt u alleen de laatste vijf gebruikte gebeurtenissen en handelingen weergeven, naast de gebeurtenissen en handelingen die buiten de box vallen. Dit geldt specifiek voor elke gebruiker. Standaard worden alle items weergegeven.

U kunt ook de opdracht **[!UICONTROL Search]** veld. Alleen gebeurtenissen en handelingen worden gefilterd.

De **canvas** is de centrale zone in de reisontwerper. Het is in deze streek dat u uw activiteiten kunt laten vallen en hen vormen. Klik op een activiteit op het canvas om deze te configureren. Dit opent de ruit van de activiteitenconfiguratie op de rechterkant.

![](assets/journey39.png)

De **activiteitenconfiguratievenster** wordt weergegeven wanneer u op een activiteit in het palet klikt. Vul de vereiste velden in. Klik op de knop **[!UICONTROL Delete]** pictogram om de activiteit te verwijderen. Klikken **[!UICONTROL Cancel]** om de wijzigingen te annuleren of **[!UICONTROL Ok]** ter bevestiging. Als u activiteiten wilt verwijderen, kunt u ook één activiteit (of meerdere activiteiten) selecteren en op de backspace-toets drukken. Als u op de escape-toets drukt, wordt het deelvenster voor activiteitenconfiguratie gesloten.

Standaard worden alleen-lezen velden verborgen. Als u alleen-lezen velden wilt weergeven, klikt u op de knop **Alleen-lezen velden tonen** pictogram linksboven in het deelvenster voor activiteitenconfiguratie. Deze instelling geldt voor alle activiteiten op alle reizen.

![](assets/journey59bis.png)

Afhankelijk van de status van de reis kunt u verschillende handelingen op uw reis uitvoeren met de knoppen in de rechterbovenhoek: **[!UICONTROL Publish]**, **[!UICONTROL Duplicate]**, **[!UICONTROL Delete]**, **[!UICONTROL Journey properties]**, **[!UICONTROL Test]**. Deze knoppen worden weergegeven wanneer er geen activiteit is geselecteerd. Sommige knoppen worden contextueel weergegeven. De knop Logbestand van de testmodus verschijnt wanneer de testmodus wordt geactiveerd.

![](assets/journey41.png)

## Begin uw reis {#start-your-journey}

Wanneer je je reis ontwerpt, wil je je eerst afvragen hoe profielen de reis zullen ingaan. Er zijn twee mogelijkheden:

**Starten met een gebeurtenis**: wanneer een reis naar het luisteren van evenementen is gepland , komen individuele personen de reis binnen **eenzijdig** in real-time. Berichten die in uw reis zijn opgenomen, worden verzonden naar de persoon die momenteel op reis gaat. [Meer informatie over gebeurtenissen](../event/about-events.md)

**Beginnen met een leessegment**: u kunt uw reis plaatsen om naar de segmenten van Adobe Experience Platform te luisteren. In dit geval betreden alle personen die tot het gespecificeerde segment behoren de reis. De berichten inbegrepen in uw reis worden verzonden naar de individuen die tot het segment behoren. [Meer informatie over het lezen van segmenten](read-segment.md).

## De volgende stappen definiëren{#define-next-steps}

Na uw eerste gebeurtenis of Read Segment, kunt u de verschillende activiteiten combineren om uw multi-step scenario&#39;s over het kanaal te bouwen. Kies in het palet de gewenste stappen.

**Gebeurtenissen**

Wanneer u uw reis met een gebeurtenis begint, zal de reis teweeggebracht worden wanneer de gebeurtenis wordt ontvangen. De persoon zal dan, individueel, de volgende stappen volgen die in uw reis worden bepaald.

U kunt **meerdere gebeurtenissen** in uw reis, zolang zij zelfde namespace gebruiken. Gebeurtenissen worden vooraf geconfigureerd. [Meer informatie over gebeurtenissen](about-journey-activities.md#event-activities)

U kunt ook een **Reactie** gebeurtenis na een bericht om te reageren op volggegevens met betrekking tot het bericht. Op deze manier kunt u bijvoorbeeld een ander bericht verzenden als de persoon het vorige bericht heeft geopend of erin heeft geklikt. Meer informatie in deze [sectie](reaction-events.md).

De **Segmentkwalificatie** Met gebeurtenisactiviteiten kunt u ervoor zorgen dat individuen een reis kunnen maken of vooruit kunnen gaan op basis van Adobe Experience Platform-segmenttoegang en -vertrek. U kunt alle nieuwe zilverklanten een reis maken en persoonlijke berichten verzenden. Meer informatie in deze [sectie](segment-qualification-events.md).

**Orchestratie**

In de orkestactiviteiten vindt u de **Segment lezen** activiteit die u toestaat om uw reis te plaatsen om aan een segment van Adobe Experience Platform te luisteren. [Meer informatie over de activiteit Leessegment](read-segment.md).

Met de andere activiteiten kunt u voorwaarden aan uw reis toevoegen om meerdere paden te definiëren, een wachttijd in te stellen voordat u de volgende activiteit uitvoert of uw reis beëindigen. Meer informatie in deze [sectie](about-journey-activities.md#orchestration-activities).

**Acties**

U vindt hier de **Bericht** activiteit die u toestaat om een bericht op te nemen dat in wordt ontworpen [!DNL Journey Optimizer]. [Meer informatie over de activiteit van het Bericht](journeys-message.md)

U zult ook de douaneacties vinden die u hebt gevormd om berichten met derdesystemen te verzenden. Meer informatie in deze [sectie](about-journey-activities.md#action-activities).

## Alternatieve paden toevoegen{#paths}

U kunt een fallback-actie definiëren in het geval van een fout of time-out voor de volgende reisactiviteiten: **[!UICONTROL Condition]** en **[!UICONTROL Action]**.

Als u een fallback-actie voor een activiteit wilt toevoegen, selecteert u de optie **[!UICONTROL Add an alternative path in case of a timeout or an error]** in de eigenschappen van de activiteit: een ander pad wordt toegevoegd na de activiteit. De time-outduur wordt gedefinieerd door Admin-gebruikers in het dialoogvenster [reiseigenschappen](../building-journeys/journey-gs.md#change-properties). Als het bijvoorbeeld te lang duurt om een e-mail te verzenden of als er een fout optreedt, kunt u een pushmelding verzenden.

![](assets/journey42.png)

Met verschillende activiteiten (gebeurtenis, handeling, wachten) kunt u verschillende paden na deze toevoegen. Plaats de cursor op de activiteit en klik op het plusteken (+). Alleen gebeurtenis- en wachtactiviteiten kunnen parallel worden ingesteld. Als meerdere gebeurtenissen parallel worden ingesteld, is het gekozen pad het eerste evenement dat plaatsvindt.

Wanneer u naar een gebeurtenis luistert, raden we u aan niet oneindig op de gebeurtenis te wachten. Het is niet verplicht, maar slechts een goede praktijk. Als u slechts gedurende een bepaalde tijd naar een of meerdere gebeurtenissen wilt luisteren, plaatst u een of meerdere gebeurtenissen en een wachtbewerking parallel. Zie [deze sectie](../building-journeys/general-events.md#events-specific-time).

Als u het pad wilt verwijderen, plaatst u de cursor op het pad en klikt u op de knop **[!UICONTROL Delete path]** pictogram.

![](assets/journey42ter.png)

Wanneer twee activiteiten op het canvas worden losgekoppeld, wordt een waarschuwing weergegeven. Plaats de cursor op het waarschuwingspictogram om het foutbericht weer te geven. U kunt het probleem verhelpen door de ontkoppelde activiteit te verplaatsen en deze aan te sluiten op de vorige activiteit.

![](assets/canvas-disconnected.png)

## Kopiëren en plakken {#copy-paste}

U kunt een of meer activiteiten van een reis kopiëren en deze in dezelfde of een andere reis plakken. Dit staat u toe om tijd te besparen als u talrijke activiteiten wilt hergebruiken die reeds in een vorige reis zijn gevormd.

**Belangrijke opmerkingen**

* U kunt kopiëren/plakken over verschillende tabbladen en browsers. U kunt alleen activiteiten kopiëren/plakken binnen dezelfde instantie.
* U kunt een gebeurtenis niet kopiëren/plakken als de doelreis een gebeurtenis heeft die een andere naamruimte gebruikt.
* Geplakte activiteiten kunnen verwijzen naar gegevens die niet aanwezig zijn in de doelreis, bijvoorbeeld als u kopieert/plakt over verschillende sandboxen. Controleer altijd op fouten en breng de vereiste aanpassingen aan.
* Houd er rekening mee dat u een handeling niet ongedaan kunt maken. Als u geplakte activiteiten wilt verwijderen, moet u deze selecteren en verwijderen. Zorg er daarom voor dat u alleen de activiteiten selecteert die u nodig hebt voordat u deze kopieert.
* U kunt activiteiten van om het even welke reis kopiëren, zelfs degenen die in read-only zijn.
* U kunt elke activiteit selecteren, ook als deze niet is gekoppeld. Gekoppelde activiteiten blijven gekoppeld nadat ze zijn geplakt.

Hier volgen de stappen voor het kopiëren/plakken van activiteiten:

1. Open een reis.
1. Selecteer de activiteiten die u wilt kopiëren door de muis te verplaatsen terwijl u klikt. U kunt ook op elke activiteit klikken terwijl u op de knop **Ctrl/Command** toets. Gebruiken **Ctrl/Command + A** als u alle activiteiten wilt selecteren.
   ![](assets/copy-paste1.png)
1. Druk **Ctrl/Command + C**.
Als u slechts één activiteit wilt kopiëren, kunt u op het klikken en gebruiken **Kopiëren** in de linkerbovenhoek van het deelvenster voor activiteitenconfiguratie.
   ![](assets/copy-paste2.png)
1. Druk tijdens elke reis op **Ctrl/Command + V** om de activiteiten te plakken zonder ze aan een bestaand knooppunt te koppelen. Geplakte activiteiten worden in dezelfde volgorde geplaatst. Na het plakken blijven de activiteiten geselecteerd zodat u ze gemakkelijk kunt verplaatsen. U kunt de cursor ook op een lege plaatsaanduiding plaatsen en op **Ctrl/Command + V**. Geplakte activiteiten worden gekoppeld aan het knooppunt.
   ![](assets/copy-paste3.png)
