---
solution: Journey Optimizer
product: journey optimizer
title: Uw eerste journey maken
description: Belangrijke stappen om uw eerste journey met Adobe Journey Optimizer te maken
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: reis, eerste, begin, snel-begin, segment, gebeurtenis, actie
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: b0b65ad119b6939a6d65d6f05edc67b2f2b22a31
workflow-type: tm+mt
source-wordcount: '1507'
ht-degree: 9%

---

# Uw eerste journey maken{#jo-quick-start}

## Vereisten{#start-prerequisites}

Voor het verzenden van berichten met ritten zijn de volgende configuraties vereist:

1. **Een gebeurtenis configureren**: als u uw reizen tijdelijk wilt activeren wanneer een gebeurtenis wordt ontvangen, moet u een gebeurtenis configureren. U bepaalt de verwachte informatie en hoe te om het te verwerken. Deze stap wordt uitgevoerd door een **technische gebruiker**. [Meer informatie](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Een segment maken**: uw reis kan ook naar Adobe Experience Platform segmenten luisteren om berichten in partij naar een gespecificeerde reeks profielen te verzenden. Hiervoor moet u segmenten maken. [Meer informatie](../segment/about-segments.md).

   ![](assets/segment2.png)

1. **De gegevensbron configureren**: u kunt een verbinding met een systeem bepalen om extra informatie terug te winnen die in uw reizen, bijvoorbeeld in uw voorwaarden zal worden gebruikt. Tijdens de provisioning wordt ook een ingebouwde Adobe Experience Platform-databron geconfigureerd. Deze stap is niet vereist als u alleen data gebruikt van de gebeurtenissen in uw journey. Deze stap wordt uitgevoerd door een **technische gebruiker**. [Meer informatie](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Een handeling configureren**: Als u een systeem van derden gebruikt om uw berichten te verzenden, kunt u een douaneactie tot stand brengen. Meer informatie in deze [sectie](../action/action.md). Deze stap wordt uitgevoerd door een **technische gebruiker**. Als u de ingebouwde berichtmogelijkheden van Journey Optimizer gebruikt, hoeft u alleen maar een kanaalactie aan uw reis toe te voegen en uw inhoud te ontwerpen.

   ![](assets/custom2.png)

## Toegang tot reizen {#journey-access}

Klik in de menusectie JOURNEY MANAGEMENT op **[!UICONTROL Journeys]**. Er zijn twee tabbladen beschikbaar:

**Overzicht**: op dit tabblad wordt een dashboard weergegeven met de belangrijkste maatstaven voor uw reizen:

* **Profielen verwerkt**: totaal aantal profielen dat in de afgelopen 24 uur is verwerkt
* **Levende reizen**: totaal aantal rechtstreekse reizen met verkeer in de afgelopen 24 uur. Levende reizen omvatten **Eenheidstreizen** (op basis van gebeurtenissen) en **Batchreizen** (lees segment).
* **Foutfrequentie**: verhouding tussen alle profielen die fout zijn, en het totale aantal profielen dat in de afgelopen 24 uur is ingevoerd.
* **Percentage negeren**: verhouding tussen alle genegeerde profielen en het totale aantal profielen dat in de afgelopen 24 uur is ingevoerd. Een weggegooid profiel vertegenwoordigt iemand die niet in aanmerking komt om de reis binnen te gaan, bijvoorbeeld vanwege een onjuiste naamruimte of vanwege regels voor opnieuw betreden.

>[!NOTE]
>
>Dit dashboard houdt rekening met de reizen met verkeer in de afgelopen 24 uur. Alleen de reizen waartoe u toegang hebt, worden weergegeven.

![](assets/journeys-dashboard.png)

**Bladeren**: op dit tabblad wordt de lijst met bestaande reizen weergegeven. U kunt reizen zoeken, filters gebruiken en basishandelingen op elk element uitvoeren. U kunt bijvoorbeeld een item dupliceren of verwijderen. Raadpleeg [deze sectie](../start/user-interface.md#filter-lists) voor meer informatie.

![](assets/journeys-browse.png)

In de lijst met ritten kunt u de ritten filteren op basis van hun status, type en versie van de **[!UICONTROL Status and version filters]**. Het type kan zijn: **[!UICONTROL Unitary event]**, **[!UICONTROL Segment qualification]**, **[!UICONTROL Read segment]**, **[!UICONTROL Business event]** of **[!UICONTROL Burst]**.

U kunt ervoor kiezen alleen reizen weer te geven die een specifieke gebeurtenis, veldgroep of handeling uit de **[!UICONTROL Activity filters]** en **[!UICONTROL Data filters]**. Daarnaast worden de **[!UICONTROL Publication filters]** Hiermee kunt u een publicatiedatum of een gebruiker selecteren. U kunt bijvoorbeeld kiezen of u de nieuwste versies wilt weergeven van live reizen die gisteren zijn gepubliceerd. [Meer informatie](../building-journeys/using-the-journey-designer.md).

![](assets/filter-journeys.png)

Gebruik de **[!UICONTROL Last update]** en **[!UICONTROL Last update by]** kolommen om te controleren wanneer de laatste update van uw reizen is gebeurd en wie het heeft gered.

In de configuratievensters Gebeurtenis, Gegevensbron en Actie, **[!UICONTROL Used in]** in het veld wordt het aantal ritten weergegeven dat van die specifieke gebeurtenis, veldgroep of handeling gebruikmaakt. U kunt klikken op de knop **[!UICONTROL View journeys]** om de lijst met corresponderende journey’s weer te geven.

![](assets/journey3bis.png)

## Uw reis maken{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Uw reis maken"
>abstract="In dit scherm wordt de lijst met bestaande reizen weergegeven. Open een reis of klik op &#39;Een reis maken&#39; en combineer de verschillende gebeurtenis-, organisatie- en actieactiviteiten om uw meerstapsscenario&#39;s voor meerdere kanalen te maken."

Deze stap wordt uitgevoerd door de **zakelijke gebruiker**. Hier maak je je reizen. Combineer de verschillende actie-, orkestratie- en gebeurtenisactiviteiten om uw kanaaloverschrijdende scenario’s met meerdere stappen te maken.

Hier volgen de belangrijkste stappen voor het verzenden van berichten via reizen:

1. Van de **Bladeren** tabblad, klikt u op **[!UICONTROL Create Journey]** om een nieuwe reis te maken.

1. Bewerk de eigenschappen van de journey in het configuratievenster dat aan de rechterkant wordt weergegeven. Meer informatie in deze [sectie](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Begin door een gebeurtenis of een **Segment lezen** van het palet naar het canvas. Raadpleeg voor meer informatie over het ontwerpen van reizen de [deze sectie](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Sleep de volgende stappen die het individu zal volgen en zet ze neer. U kunt bijvoorbeeld een voorwaarde toevoegen gevolgd door een kanaalactie. Voor meer informatie over activiteiten raadpleegt u [deze sectie](using-the-journey-designer.md).

1. Test uw reis met testprofielen. Meer informatie in deze [sectie](testing-the-journey.md)

1. Publiceer uw reis om deze te activeren. Meer informatie in deze [sectie](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Bewaak uw reis gebruikend de specifieke rapporteringshulpmiddelen om de doeltreffendheid van uw reis te meten. Meer informatie in deze [sectie](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## De eigenschappen van uw reis definiëren {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Journeyeigenschappen"
>abstract="In dit gedeelte worden de eigenschappen van de reis weergegeven. Standaard zijn alleen-lezen parameters verborgen. Welke instellingen beschikbaar zijn, is afhankelijk van de status van de rit, van uw machtigingen en de productconfiguratie."

Klik op het potloodpictogram in de rechterbovenhoek om de eigenschappen van de rit te openen.

U kunt de naam van de reis wijzigen, een beschrijving toevoegen, opnieuw toegang toestaan, begin- en einddatum kiezen en, als Admin-gebruiker, een **[!UICONTROL Timeout and error]** duur. U kunt Adobe Experience Platform Verenigde Markeringen aan uw reis ook toewijzen. Op deze manier kunt u ze gemakkelijk classificeren en de zoekopdracht in de lijst met campagnes verbeteren. [Leer hoe u met tags kunt werken](../start/search-filter-categorize.md#tags)

Voor live reizen worden in dit scherm de publicatiedatum en de naam weergegeven van de gebruiker die de reis heeft gepubliceerd.

De **Technische details kopiëren** staat u toe om technische informatie over de reis te kopiëren die het steunteam kan gebruiken om problemen op te lossen. De volgende informatie wordt gekopieerd: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Entrance{#entrance}

Nieuwe reizen zijn standaard geschikt voor herbinnenkomst. U kunt de controle van **Opnieuw openen toestaan** optie voor &quot;één enkele schot&quot;reizen, bijvoorbeeld als u een eenmalig geschenk wilt aanbieden wanneer een persoon een winkel ingaat.

Wanneer de **Opnieuw openen toestaan** -optie is geactiveerd, de **Wachttijd bij terugkeer** wordt weergegeven. In dit veld kunt u de tijd definiëren die u moet wachten voordat een profiel de reis weer in één keer kan betreden (te beginnen met een gebeurtenis of een segmentkwalificatie). Hierdoor wordt voorkomen dat ritten meerdere keren ten onrechte worden geactiveerd voor dezelfde gebeurtenis. Het veld wordt standaard ingesteld op 5 minuten.

Meer informatie over toegangsbeheer voor profielen vindt u in [deze sectie](entry-management.md).

### Toegang beheren {#access}

Als u aangepaste of basislabels voor gegevensgebruik aan de reis wilt toewijzen, klikt u op de knop **[!UICONTROL Manage access]** knop. [Meer informatie over OLA (Object Level Access Control)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### Tijdzone en profieltijdzone {#timezone}

De tijdzone wordt gedefinieerd op het niveau van de reis.

U kunt een vaste tijdzone invoeren of Adobe Experience Platform-profielen gebruiken om de tijdzone van de reis te definiëren.

Als een tijdzone in Adobe Experience Platform-profiel is gedefinieerd, kan deze tijdens de reis worden opgehaald.

Zie voor meer informatie over tijdzonebeheer [deze pagina](../building-journeys/timezone-management.md).

### Begin- en einddatum {#dates}

U kunt een **Begindatum**. Als u er geen hebt opgegeven, wordt deze automatisch gedefinieerd op het moment van publicatie.

U kunt ook een **Einddatum**. Hiermee kunnen profielen automatisch worden afgesloten wanneer de datum wordt bereikt. Als u geen einddatum opgeeft, kunnen profielen blijven tot de standaardreistime-out (doorgaans 30 dagen, 7 dagen met de invoegtoepassing voor het gezondheidsschild). De enige uitzondering is terugkerende read-segment reizen met **Herkomst forceren bij herhaling** geactiveerd, die eindigt op de begindatum van het volgende exemplaar.

### Tijdslimiet en fout bij reisactiviteiten {#timeout_and_error}

Wanneer u een actie of voorwaardenactiviteit bewerkt, kunt u een alternatief pad opgeven in het geval van een fout of time-out. Als de verwerking van de activiteit, die het vragen van een derdesysteem impliceert, de duur overschrijdt die in de eigenschappen van de reis voor onderbreking en fout behandeling wordt gespecificeerd (**[!UICONTROL Timeout and  error]** (veld), wordt het tweede pad geselecteerd om indien nodig een fallback-actie uit te voeren.

Toegestane waarden liggen tussen 1 en 30 seconden.

We raden u aan om een zeer korte definitie te geven **[!UICONTROL Timeout and error]** waarde als uw reis tijdgevoelig is (voorbeeld: reageren op de locatie in real time van een persoon) omdat u de handeling niet langer dan een paar seconden kunt uitstellen. Als uw reis minder tijdgevoelig is, kunt u een langere waarde gebruiken om meer tijd aan het geroepen systeem te geven om een geldige reactie te verzenden.

De reizen gebruikt ook een globale onderbreking. Zie de [volgende sectie](#global_timeout).

### Globale time-out voor transport {#global_timeout}

Naast de [timeout](#timeout_and_error) Bij reisactiviteiten wordt ook een wereldwijde reistijd gebruikt die niet in de interface wordt weergegeven en niet kan worden gewijzigd. Deze onderbreking zal de vooruitgang van individuen in de reis 30 dagen na hun binnengaan stoppen. Dit betekent dat de reis van een individu niet langer mag duren dan 30 dagen. Na de periode van 30 dagen worden de gegevens van het individu verwijderd. Personen die aan het einde van de time-outperiode nog onderweg zijn, worden gestopt en als fouten in de rapportage worden ze in aanmerking genomen.

>[!NOTE]
>
>De reizen reageren niet direct op privacy opt-out, toegang of schrappingsverzoeken. De wereldwijde time-out zorgt er echter voor dat individuen nooit langer dan 30 dagen op een reis blijven.

Vanwege de 30 dagen durende reistijd, wanneer het niet is toegestaan om de reis opnieuw te betreden, kunnen we er niet voor zorgen dat het blokkeren van de terugkeer meer dan 30 dagen zal duren. Aangezien we alle informatie over personen die 30 dagen na hun binnenkomst de reis hebben betreden, verwijderen, kunnen we niet weten dat de persoon eerder, meer dan 30 dagen geleden, is binnengekomen.

