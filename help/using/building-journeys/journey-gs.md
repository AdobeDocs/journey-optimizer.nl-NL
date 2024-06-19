---
solution: Journey Optimizer
product: journey optimizer
title: Uw eerste journey maken
description: Belangrijke stappen om uw eerste journey met Adobe Journey Optimizer te maken
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: reis, eerste, begin, snel-begin, publiek, gebeurtenis, actie
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 6ff54583c729175c74b3a7ea4ab9188505fde897
workflow-type: tm+mt
source-wordcount: '2583'
ht-degree: 3%

---

# Uw eerste journey maken{#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Reizen maken"
>abstract="Gebruiken **Adobe Journey Optimizer** gebruiken voor het maken van realtime-formulieren voor het orkestgebruik met gebruik van contextuele gegevens die zijn opgeslagen in gebeurtenissen of gegevensbronnen."



## Vereisten{#start-prerequisites}

Voor het verzenden van berichten met ritten zijn de volgende configuraties vereist:

1. **Een gebeurtenis configureren**: als u uw reizen tijdelijk wilt activeren wanneer een gebeurtenis wordt ontvangen, moet u een gebeurtenis configureren. U bepaalt de verwachte informatie en hoe te om het te verwerken. Deze stap wordt uitgevoerd door een **technisch gebruiker**. [Meer informatie](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Een publiek maken**: uw reis kan ook luisteren naar Adobe Experience Platform-publiek om berichten in batch te verzenden naar een opgegeven reeks profielen. Hiervoor moet u een publiek maken. [Meer informatie](../audience/about-audiences.md).

   ![](assets/segment2.png)

1. **De gegevensbron configureren**: u kunt een verbinding met een systeem definiëren om aanvullende informatie op te halen die in uw reizen wordt gebruikt, bijvoorbeeld in uw omstandigheden. Tijdens de provisioning wordt ook een ingebouwde Adobe Experience Platform-databron geconfigureerd. Deze stap is niet vereist als u alleen data gebruikt van de gebeurtenissen in uw journey. Deze stap wordt uitgevoerd door een **technisch gebruiker**. [Meer informatie](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Een handeling configureren**: Als u berichten verzendt met een systeem van derden, kunt u een aangepaste handeling maken. Meer informatie in deze [sectie](../action/action.md). Deze stap wordt uitgevoerd door een **technisch gebruiker**. Als u de ingebouwde berichtmogelijkheden van Journey Optimizer gebruikt, hoeft u alleen maar een kanaalactie aan uw reis toe te voegen en uw inhoud te ontwerpen.

   ![](assets/custom2.png)

## Toegang tot reizen {#journey-access}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Journeys"
>abstract="Ontwerpen van klantritten om persoonlijke, contextuele ervaringen te bieden. Met Journey Optimizer kunt u in real-time gebruikmaken van het orkestgebruik en contextuele gegevens opslaan in gebeurtenissen of gegevensbronnen. De **Overzicht** wordt een dashboard weergegeven met de belangrijkste maatstaven voor uw reizen. De **Bladeren** wordt de lijst met bestaande reizen weergegeven."

### Belangrijkste metriek en reislijst {#access-metrics}

Klik in de menusectie JOURNEY MANAGEMENT op **[!UICONTROL Journeys]**. Er zijn twee tabbladen beschikbaar:

**Overzicht**: op dit tabblad wordt een dashboard weergegeven met de belangrijkste maatstaven voor uw reizen:

* **Profielen verwerkt**: totaal aantal profielen dat in de afgelopen 24 uur is verwerkt
* **Levende reizen**: totaal aantal rechtstreekse reizen met verkeer in de afgelopen 24 uur. Levende reizen omvatten **Eenheidstreizen** (op basis van gebeurtenissen) en **Batchreizen** (lees publiek).
* **Foutfrequentie**: verhouding van alle profielen die fout zijn in vergelijking met het totale aantal profielen dat in de afgelopen 24 uur is ingevoerd.
* **Percentage negeren**: verhouding tussen alle genegeerde profielen en het totale aantal profielen dat in de afgelopen 24 uur is ingevoerd. Een weggegooid profiel vertegenwoordigt iemand die niet in aanmerking komt om de reis binnen te gaan, bijvoorbeeld vanwege een onjuiste naamruimte of vanwege regels voor opnieuw betreden.

>[!NOTE]
>
>Dit dashboard houdt rekening met de reizen met verkeer in de afgelopen 24 uur. Alleen de reizen waartoe u toegang hebt, worden weergegeven. De metriek worden verfrist om de 30 minuten en slechts wanneer de nieuwe gegevens beschikbaar zijn.

![](assets/journeys-dashboard.png)

**Bladeren**: op dit tabblad wordt de lijst met bestaande reizen weergegeven. U kunt reizen zoeken, filters gebruiken en basishandelingen op elk element uitvoeren. U kunt bijvoorbeeld een item dupliceren of verwijderen. Raadpleeg [deze sectie](../start/user-interface.md#filter-lists) voor meer informatie.

![](assets/journeys-browse.png)

### Reizen filteren {#filter}

In de lijst met reizen kunt u verschillende filters gebruiken om de lijst met reizen te verfijnen, zodat u deze beter leesbaar kunt maken.

![](assets/filter-journeys.png)

Hier zijn de diverse het filtreren verrichtingen die u kunt uitvoeren:

Reizen filteren op basis van hun status, type, versie en toegewezen tags van de **[!UICONTROL Status and version filters]**.

Het type kan zijn: **[!UICONTROL Unitary event]**, **[!UICONTROL Audience qualification]**, **[!UICONTROL Read audience]** of **[!UICONTROL Business event]**.

De status kan zijn:

* **Gesloten**: de reis is afgesloten met de **Dicht bij nieuwe ingangen** knop. De reis houdt in dat nieuwe individuen de reis kunnen betreden. Personen die al onderweg zijn, kunnen de reis normaal afmaken.
* **Concept**: de reis bevindt zich in de eerste fase. Het is nog niet gepubliceerd.
* **Concept (testen)**: de testmodus is geactiveerd met behulp van de **Testmodus** knop.
* **Voltooid**: de reis schakelt na 91 dagen automatisch over naar deze status [standaardtime](journey-gs.md#global_timeout). Profielen die al op reis zijn, worden normaal afgehandeld. Nieuwe profielen kunnen niet langer de reis betreden.
* **Live**: de reis is gepubliceerd met behulp van de **Publiceren** knop.
* **Gestopt**: de reis is uitgeschakeld met behulp van de **Stoppen** knop. Alle individuen sluiten onmiddellijk de reis.

>[!NOTE]
>
>De publicatielevenscyclus van de Reis omvat ook een reeks tussenliggende statussen die niet beschikbaar zijn voor filtering: &quot;Publishing&quot; (tussen &quot;Draft&quot; en &quot;Live&quot;), &quot;Activating test mode&quot; of &quot;Deactivating test mode&quot; (tussen &quot;Draft&quot; en &quot;Draft (test)&quot;) en &quot;Stopping&quot; (tussen &quot;Live&quot; en &quot;Gestopt&quot;). Wanneer een reis in een tussenstadium is, is het read-only.

Gebruik de **[!UICONTROL Creation filters]** om reizen te filteren op basis van de aanmaakdatum of de gebruiker die ze heeft gemaakt.

Reizen weergeven die gebruikmaken van een specifieke gebeurtenis, veldgroep of handeling van de **[!UICONTROL Activity filters]** en **[!UICONTROL Data filters]**.

Gebruik de **[!UICONTROL Publication filters]** om een publicatiedatum of een gebruiker te selecteren. U kunt bijvoorbeeld kiezen of u de nieuwste versies wilt weergeven van live reizen die gisteren zijn gepubliceerd.

Als u reizen wilt filteren op basis van een specifiek datumbereik, selecteert u **[!UICONTROL Custom]** van de **[!UICONTROL Published]** vervolgkeuzelijst.

Daarnaast worden in de configuratievensters Gebeurtenis, Gegevensbron en Handeling de **[!UICONTROL Used in]** in het veld wordt het aantal ritten weergegeven dat van die specifieke gebeurtenis, veldgroep of handeling gebruikmaakt. U kunt klikken op de knop **[!UICONTROL View journeys]** om de lijst met corresponderende journey’s weer te geven.

![](assets/journey3bis.png)

## Uw reis maken{#jo-build}

Deze stap wordt uitgevoerd door de **zakelijke gebruiker**. Hier maak je je reizen. Combineer de verschillende gebeurtenis-, organisatie- en actieactiviteiten om uw meerstapsscenario&#39;s voor meerdere kanalen te maken.

➡️ [Deze functie in video detecteren](journey.md#video)

Hier volgen de belangrijkste stappen voor het verzenden van berichten via reizen:

1. Van de **Bladeren** tabblad, klikt u op **[!UICONTROL Create Journey]** om een nieuwe reis te maken.

1. Bewerk de eigenschappen van de journey in het configuratievenster dat aan de rechterkant wordt weergegeven. Meer informatie in deze [sectie](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Begin door een gebeurtenis of een **Publiek lezen** van het palet naar het canvas. Raadpleeg voor meer informatie over het ontwerpen van reizen de [deze sectie](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Sleep de volgende stappen die het individu zal volgen en zet ze neer. U kunt bijvoorbeeld een voorwaarde toevoegen, gevolgd door een kanaalactie. Voor meer informatie over activiteiten raadpleegt u [deze sectie](using-the-journey-designer.md).

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

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="Criteria voor het verlaten van de reis"
>abstract="In dit gedeelte worden de opties voor afsluitcriteria weergegeven. U kunt één of veelvoudige regels van de uitgangscriteria voor uw reis tot stand brengen."

Klik op het potloodpictogram naast de naam van de reis om de eigenschappen ervan te openen.

U kunt de naam van de reis wijzigen, een beschrijving toevoegen, opnieuw toegang toestaan, begin- en einddatum kiezen en, als Admin-gebruiker, een **[!UICONTROL Timeout and error]** duur. U kunt Adobe Experience Platform Verenigde Markeringen aan uw reis ook toewijzen. Op deze manier kunt u ze gemakkelijk classificeren en de zoekopdracht in de lijst met campagnes verbeteren. [Leer hoe u met tags kunt werken](../start/search-filter-categorize.md#tags)

Voor live reizen worden in dit scherm de publicatiedatum en de naam weergegeven van de gebruiker die de reis heeft gepubliceerd.

De **Technische details kopiëren** staat u toe om technische informatie over de reis te kopiëren die het steunteam kan gebruiken om problemen op te lossen. De volgende informatie wordt gekopieerd: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Entrance en re-entry {#entrance}

Nieuwe reizen zijn standaard geschikt voor herbinnenkomst. U kunt de controle van **Hernieuwde toegang toestaan** optie voor &quot;één enkele schot&quot;reizen, bijvoorbeeld als u een eenmalig geschenk wilt aanbieden wanneer een persoon een winkel ingaat.

Wanneer de **Hernieuwde toegang toestaan** -optie is geactiveerd, de **Wachttijd bij terugkeer** wordt weergegeven. In dit veld kunt u de tijd definiëren die u moet wachten voordat u een profiel toestaat om de reis opnieuw te betreden tijdens een enkele reis (te beginnen met een evenement of een publiekskwalificatie). Hierdoor wordt voorkomen dat ritten meerdere keren ten onrechte worden geactiveerd voor dezelfde gebeurtenis. Het veld wordt standaard ingesteld op 5 minuten. De maximale duur is 29 dagen.

Meer informatie over toegang tot profielen en beheer van nieuwe toegang, in [deze sectie](entry-management.md).

### Toegang beheren {#manage-access}

Als u aangepaste of basislabels voor gegevensgebruik aan de reis wilt toewijzen, klikt u op de knop **[!UICONTROL Manage access]** knop. [Meer informatie over OLA (Object Level Access Control)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### Tijdzones voor reizen en profielen {#timezone}

De tijdzone wordt gedefinieerd op het niveau van de reis. U kunt een vaste tijdzone invoeren of Adobe Experience Platform-profielen gebruiken om de tijdzone van de reis te definiëren. Als een tijdzone in Adobe Experience Platform-profiel is gedefinieerd, kan deze tijdens de reis worden opgehaald.

Zie voor meer informatie over tijdzonebeheer [deze pagina](../building-journeys/timezone-management.md).

### Begin- en einddatum {#dates}

U kunt een **Begindatum**. Als u er geen hebt opgegeven, wordt deze automatisch gedefinieerd op het moment van publicatie.

U kunt ook een **Einddatum**. Hiermee kunnen profielen automatisch worden afgesloten wanneer de datum wordt bereikt. Als er geen einddatum is opgegeven, kunnen profielen blijven tot de [algemene time-out](#global_timeout) (over het algemeen 91 dagen, en met de toevoeging aan het gezondheidsschild tot 7 dagen teruggebracht). De enige uitzondering is terugkerende publiekstrajecten met **Herkomst forceren bij herhaling** geactiveerd, die eindigt op de begindatum van het volgende exemplaar.

### Tijdslimiet en fout bij reisactiviteiten {#timeout_and_error}

Wanneer u een actie of voorwaardenactiviteit bewerkt, kunt u een alternatief pad definiëren in het geval van een fout of time-out. Indien de verwerking van de activiteit die een derdenstelsel ondervraagt, langer duurt dan de in de eigendommen van de reis vastgestelde tijdsduur (**[!UICONTROL Timeout and error]** (veld), wordt het tweede pad gekozen om een mogelijke fallback-actie uit te voeren.

Toegestane waarden liggen tussen 1 en 30 seconden.

We raden u aan om een zeer korte definitie te geven **[!UICONTROL Timeout and error]** waarde als uw reis tijdgevoelig is (bijvoorbeeld: het reageren op de plaats in real time van een persoon) omdat u uw actie niet meer dan een paar seconden kunt vertragen. Als uw reis minder tijdgevoelig is, kunt u een langere waarde gebruiken om meer tijd aan het geroepen systeem te geven om een geldige reactie te verzenden.

De reizen gebruikt ook een globale onderbreking. Zie de [volgende sectie](#global_timeout).

### Globale time-out voor transport {#global_timeout}

Naast de [timeout](#timeout_and_error) Bij reisactiviteiten wordt ook een wereldwijde reistijd gebruikt die niet in de interface wordt weergegeven en niet kan worden gewijzigd.

Door deze wereldwijde time-out wordt de voortgang van individuen tijdens de reis gestopt **91 dagen** nadat ze zijn binnengekomen. Deze time-out wordt beperkt tot **7 dagen** met de toevoeging aan het gezondheidsschild. Dit betekent dat de reis van een individu niet langer mag duren dan 91 dagen (of 7 dagen). Na deze time-outperiode worden de gegevens van de persoon verwijderd. Personen die aan het einde van de time-outperiode nog onderweg zijn, worden gestopt en er wordt geen rekening mee gehouden bij de rapportage. Je zou dus meer mensen op de reis zien komen dan vertrekken.

>[!NOTE]
>
>De reizen reageren niet direct op privacy opt-out, toegang of schrappingsverzoeken. De wereldwijde time-out zorgt er echter voor dat individuen nooit langer dan 91 dagen op een reis blijven.

Vanwege de reistijd van 91 dagen, wanneer het niet is toegestaan om de reis opnieuw te betreden, kunnen we er niet voor zorgen dat het blokkeren van de terugkeer meer dan 91 dagen zal duren. Aangezien we alle informatie over personen die 91 dagen na hun binnenkomst de reis hebben betreden, verwijderen, kunnen we niet weten dat de persoon eerder, meer dan 91 dagen geleden, is binnengekomen.

Een individu kan alleen een wachtdienst doen als hij of zij genoeg tijd in de reis heeft om de wachttijd vóór de reisonderbreking van 91 dagen te voltooien. Zie [deze pagina](../building-journeys/wait-activity.md).


#### Time-to-live (TTL) en veelgestelde vragen over gegevensinvoer {#timeout-faq}

**Voor eenheidsreizen**
<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met de reis die wordt gepubliceerd na de introductie van de TTL-uitbreiding?</p>
    </td>
    <td>
      <p>Profielen die de nieuwe reis ingaan, hebben automatisch een TTL van 91 dagen.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een profiel dat een reis ingaat die vóór de lancering van de uitbreiding van TTL werd gepubliceerd?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen (7 dagen voor HIPAA) hebben, in overeenstemming met de tijd dat de reis oorspronkelijk werd gepubliceerd.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een profiel dat al een reis is begonnen toen de uitbreiding van de TTL wordt gestart?</p>
    </td>
    <td>
      <p>Het profiel behoudt een TTL van 91 dagen (7 dagen voor HIPAA), volgens de oorspronkelijke publicatietijd van de reis.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een profiel in een vorige reisversie dat opnieuw wordt gepubliceerd na de lancering van de uitbreiding van TTL?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen (7 dagen voor HIPAA) handhaven, die met de de publicatietijd van de originele reisversie wordt gericht.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een nieuw profiel dat een opnieuw gepubliceerde reisversie invoert na de introductie van de uitbreiding van TTL?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen hebben, die TTL van de onlangs opnieuw gepubliceerde reisversie aanpassen.</p>
    </td>
  </tr>
</table>

**Voor segmenttriggerreizen**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met nieuwe eenmalige reizen die na de uitbreiding van de TTL worden gepubliceerd?</p>
    </td>
    <td>
      <p>Profielen die de nieuwe reis ingaan zullen een TTL van 91 dagen automatisch hebben.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met nieuwe terugkerende reizen zonder gedwongen terugkeer die na de uitbreiding van de GVTO worden gepubliceerd?</p>
    </td>
    <td>
      <p>Profielen die de nieuwe reis ingaan zullen een TTL van 91 dagen automatisch hebben.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met nieuwe terugkerende reizen met gedwongen terugkeer die na de uitbreiding van de GVTO worden gepubliceerd?</p>
    </td>
    <td>
      <p>De profielen die de nieuwe reis ingaan zullen een TTL gelijk aan de herhalingsperiode hebben. Bijvoorbeeld, als de reis dagelijks loopt, zal TTL 1 dag zijn.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een profiel dat een reis ingaat die vóór de lancering van de uitbreiding van TTL werd gepubliceerd?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen (7 dagen voor HIPAA) hebben, verenigbaar met de originele publicatietijd. Voor terugkerende ritten met gedwongen terugkeer zal de TTL overeenkomen met de herhalingsperiode.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een profiel dat door een reis loopt wanneer de uitbreiding van TTL wordt gelanceerd?</p>
    </td>
    <td>
      <p>Het profiel behoudt een TTL van 91 dagen (7 dagen voor HIPAA), volgens de oorspronkelijke publicatietijd van de reis. Voor terugkerende ritten met gedwongen terugkeer zal de TTL overeenkomen met de herhalingsperiode.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een lopend profiel in een vorige reisversie die opnieuw wordt gepubliceerd na de lancering van de uitbreiding van TTL?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen (7 dagen voor HIPPA) handhaven, die aan de originele de publicatietijd van de reisversie wordt aangepast. Voor terugkerende ritten met gedwongen terugkeer zal de TTL overeenkomen met de herhalingsperiode.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een nieuw profiel dat een opnieuw gepubliceerde reisversie invoert na de introductie van de uitbreiding van TTL?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen hebben, die TTL van de onlangs opnieuw gepubliceerde reisversie aanpassen. Voor terugkerende ritten met gedwongen terugkeer zal de TTL overeenkomen met de herhalingsperiode.</p>
    </td>
  </tr>
</table>

### Beleid samenvoegen {#merge-policies}

Reis gebruikt samenvoegbeleid terwijl het terugwinnen van profielgegevens van Adobe Experience Platform. Afhankelijk van het type van reis, worden de verschillende samenvoegingsbeleidsvormen gebruikt:

* In kwalificatiereizen voor het publiek of het publiek lezen: het samenvoegbeleid van het publiek wordt gebruikt
* Bij door gebeurtenis geïnitieerde reizen: het standaardsamenvoegbeleid wordt gebruikt

De reis zal het fusieprincipe respecteren dat door de volledige reis wordt gebruikt. Als er daarom meerdere soorten publiek worden gebruikt op een reis (bijvoorbeeld in &quot;inAudience&quot;-functies), waardoor inconsistenties ontstaan met het fusiebeleid dat door de reis wordt gebruikt, wordt een fout opgeworpen en wordt de publicatie geblokkeerd. Nochtans, als een inconsistent publiek in berichtverpersoonlijking wordt gebruikt, wordt een alarm niet opgeheven, ondanks de inconsistentie. Om deze reden, wordt het hoogst geadviseerd om het samenvoegbeleid te controleren verbonden aan uw publiek, wanneer dit publiek in berichtverpersoonlijking wordt gebruikt.

Raadpleeg voor meer informatie over samenvoegingsbeleid [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.

## Een reis dupliceren {#duplicate-a-journey}

U kunt een bestaande reis dupliceren vanaf de **Bladeren** tab. Alle objecten en instellingen worden gedupliceerd naar de reiskopie.

Volg onderstaande stappen om dit te doen:

1. Navigeer naar de reis u wilt kopiëren, klik **Meer handelingen** pictogram (de drie punten naast de naam van het transport).
1. Selecteren **Dupliceren**.

   ![Een reis dupliceren](assets/duplicate-jo.png)

1. Voer de naam van de reis in en bevestig deze. U kunt de naam ook wijzigen in het scherm met de reiseigenschappen. Standaard wordt de naam als volgt ingesteld: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. De nieuwe reis wordt gecreeerd en beschikbaar in de reislijst.
