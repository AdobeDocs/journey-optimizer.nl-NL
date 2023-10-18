---
title: Beslissingen maken
description: Leer hoe u beslissingen maakt
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '2161'
ht-degree: 1%

---

# Beslissingen maken {#create-offer-activities}

Besluiten zijn containers voor uw aanbiedingen die gebruikmaken van de Offertenbeslissingsengine om de beste aanbieding te kiezen, afhankelijk van het doel van de levering.

➡️ [Leer hoe u aanbiedingsactiviteiten kunt maken in deze video](#video)

De lijst van besluiten is toegankelijk in **[!UICONTROL Offers]** menu > **[!UICONTROL Decisions]** tab. De filters zijn beschikbaar om u te helpen besluiten op hun status of begin en einddata terugwinnen.

![](../assets/activities-list.png)

Voordat u een beslissing maakt, moet u controleren of de onderstaande componenten zijn gemaakt in de bibliotheek met aanbiedingen:

* [Plaatsingen](../offer-library/creating-placements.md)
* [Verzamelingen](../offer-library/creating-collections.md)
* [Persoonlijke aanbiedingen](../offer-library/creating-personalized-offers.md)
* [Alternatieve aanbiedingen](../offer-library/creating-fallback-offers.md)

## De beslissing maken {#create-activity}

1. Open de beslissingslijst en klik vervolgens op **[!UICONTROL Create decision]**.

1. Geef de naam van de beslissing op.

1. Geef zo nodig een begin- en einddatum en -tijd op en klik op **[!UICONTROL Next]**.

   ![](../assets/activities-name.png)

1. Als u aangepaste of basislabels voor gegevensgebruik aan de beslissing wilt toewijzen, selecteert u **[!UICONTROL Manage access]**. [Leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC)](../../administration/object-based-access.md)

## Bepaal beslissingsbereik {#add-decision-scopes}

1. Selecteer een plaatsing van de drop-down lijst. Het zal aan het eerste beslissingswerkingsgebied in uw besluit worden toegevoegd.

   ![](../assets/activities-placement.png)

1. Klikken **[!UICONTROL Add]** om evaluatiecriteria voor deze plaatsing te selecteren.

   ![](../assets/activities-evaluation-criteria.png)

   Elk criterium bestaat uit een verzameling aanbiedingen die gekoppeld is aan een geschiktheidsbeperking en een rangschikkingsmethode om de aanbiedingen te bepalen die in de plaatsing moeten worden getoond.

   >[!NOTE]
   >
   >Er is ten minste één evaluatiecriterium vereist.

1. Selecteer de aanbiedingsinzameling die de aanbiedingen bevat om te overwegen, dan klik **[!UICONTROL Add]**.

   ![](../assets/activities-collection.png)

   >[!NOTE]
   >
   >U kunt op de knop **[!UICONTROL Open offer collections]** koppeling om de lijst met verzamelingen op een nieuw tabblad weer te geven, zodat u door de verzamelingen en de aanbiedingen in deze verzamelingen kunt bladeren.

   De geselecteerde verzameling wordt toegevoegd aan de criteria.

   ![](../assets/activities-collection-added.png)

1. Gebruik de **[!UICONTROL Eligibility]** om de selectie van aanbiedingen voor deze plaatsing te beperken.

   Deze beperking kan worden toegepast door een **beslissingsregel**, of een of meer **Adobe Experience Platform-publiek**. Beide zijn gedetailleerd in [deze sectie](../offer-library/add-constraints.md#segments-vs-decision-rules).

   * Als u de selectie van de aanbiedingen wilt beperken tot de leden van een publiek in een Experience Platform, selecteert u **[!UICONTROL Audiences]** en klik vervolgens op **[!UICONTROL Add audiences]**.

     ![](../assets/activity_constraint_segment.png)

     Voeg een of meer soorten publiek toe vanuit het linkervenster en combineer deze via het dialoogvenster **[!UICONTROL And]** / **[!UICONTROL Or]** logische operatoren.

     ![](../assets/activity_constraint_segment2.png)

     Leer hoe u met het publiek kunt werken in [deze sectie](../../audience/about-audiences.md).

   * Als u een selectiegrens met een beslissingsregel wilt toevoegen, gebruikt u de optie **[!UICONTROL Decision rule]** en selecteert u de gewenste regel.

     ![](../assets/activity_constraint_rule.png)

     Leer hoe u een beslissingsregel maakt in [deze sectie](../offer-library/creating-decision-rules.md).

1. Wanneer u publiek of beslissingsregels selecteert, kunt u informatie over de geschatte gekwalificeerde profielen zien. Klikken **[!UICONTROL Refresh]** gegevens bijwerken.

   >[!NOTE]
   >
   >Profielramingen zijn niet beschikbaar wanneer regelparameters gegevens bevatten die niet in het profiel staan, zoals contextgegevens. Bijvoorbeeld, een toelatingsregel die het huidige weer om 80 graden vereist te zijn.

   ![](../assets/activity_constraint-estimate.png)

1. Definieer de waarderingsmethode die u wilt gebruiken om de beste aanbieding voor elk profiel te selecteren. [Meer informatie](../offer-activities/configure-offer-selection.md).

   ![](../assets/activity_ranking-method.png)

   * Als meerdere aanbiedingen standaard in aanmerking komen voor deze plaatsing, wordt de opdracht **[!UICONTROL Offer priority]** de methode gebruikt de waarde die in de aanbiedingen is gedefinieerd: de aanbieding met de hoogste prioriteitsscore wordt aan de gebruiker geleverd.

   * Als u een specifieke berekende score wilt gebruiken om te kiezen welke aanbieding in aanmerking komt, selecteert u **[!UICONTROL Formula]** of **[!UICONTROL AI model]**. [Meer informatie](../offer-activities/configure-offer-selection.md).

1. Klikken **[!UICONTROL Add]** om meer criteria voor dezelfde plaatsing te definiëren.

   ![](../assets/activity_add-collection.png)

1. Wanneer u meerdere criteria toevoegt, worden deze in een bepaalde volgorde geëvalueerd. De eerste verzameling die aan de reeks is toegevoegd, wordt eerst geëvalueerd, enzovoort. [Meer informatie](#evaluation-criteria-order)

   Als u de standaardvolgorde wilt wijzigen, kunt u de verzamelingen slepen en neerzetten om ze naar wens opnieuw te rangschikken.

   ![](../assets/activity_reorder-collections.png)

1. U kunt ook meerdere criteria tegelijk evalueren. U doet dit door de verzameling boven op een andere verzameling te slepen.

   ![](../assets/activity_move-collection.png)

   Ze hebben nu dezelfde rang en zullen dus tegelijkertijd worden geëvalueerd. [Meer informatie](#evaluation-criteria-order)

   ![](../assets/activity_same-rank-collections.png)

   >[!CAUTION]
   >
   >* Indien [AI-model](../ranking/ai-models.md) wordt gebruikt in een groep van evaluatiecriteria, moeten alle evaluatiecriteria in die groep gebruikmaken van de AI-waarderingsmethode en moeten zij hetzelfde specifieke AI-model gebruiken.
   >
   >* Slechts één groep met evaluatiecriteria kan het AI-model gebruiken. Andere groepen binnen een beslissingsbereik moeten andere rangordemethoden gebruiken (prioriteit of formule). [Meer informatie over waarderingsmethoden](../offer-activities/configure-offer-selection.md)

1. Als u een andere plaatsing voor uw voorstellen wilt toevoegen als onderdeel van deze beslissing, gebruikt u de opdracht **[!UICONTROL New scope]** knop. Herhaal bovenstaande stappen voor elk beslissingsbereik.

   ![](../assets/activity_new-scope.png)

   >[!NOTE]
   >
   >Wanneer het toevoegen van veelvoudige beslissingswerkingsgebied, zal de orde van de evaluatiecriteria worden beïnvloed. [Meer informatie](#multiple-scopes)

### Volgorde van de beoordelingscriteria {#evaluation-criteria-order}

Zoals hierboven is beschreven, bestaan de evaluatiecriteria uit een verzameling, subsidiabiliteitsbeperkingen en een rangorde. U kunt de opeenvolgende orde plaatsen u voor de evaluatiecriteria wilt worden geëvalueerd, maar u kunt veelvoudige evaluatiecriteria ook combineren zodat zij samen en niet afzonderlijk worden geëvalueerd.

#### Met één bereik {#one-scope}

Binnen één besluitvormingsgebied bepalen meerdere criteria en de groepering daarvan de prioriteit van de criteria en de rangorde van de in aanmerking komende aanbiedingen. De eerste criteria hebben de hoogste prioriteit en de criteria die in dezelfde &quot;groep&quot; worden gecombineerd, hebben dezelfde prioriteit.

U hebt bijvoorbeeld twee verzamelingen, één in evaluatiecriteria A en één in evaluatiecriteria B. Er worden twee voorstellen teruggestuurd. Laten we zeggen dat er twee in aanmerking komende aanbiedingen zijn uit evaluatiecriteria A en drie in aanmerking komende aanbiedingen uit evaluatiecriteria B.

* Indien de twee evaluatiecriteria **niet gecombineerd** en/of in sequentiële volgorde (1 en 2) worden de twee belangrijkste in aanmerking komende aanbiedingen uit de evaluatiecriteria in de eerste rij teruggegeven. Als er niet twee in aanmerking komende aanbiedingen voor de eerste evaluatiecriteria zijn, zal de beslissingsmotor achtereenvolgens overgaan op de volgende evaluatiecriteria om te zien hoeveel aanbiedingen nog nodig zijn, en uiteindelijk een terugslag teruggeven indien nodig.

  ![](../assets/activity_consecutive-rank-collections.png)

* Als de twee verzamelingen **tegelijk geëvalueerd** Aangezien er twee in aanmerking komende aanbiedingen zijn op basis van beoordelingscriteria A en drie in aanmerking komende aanbiedingen op basis van beoordelingscriteria B, worden de vijf offertes in een stapel geplaatst op basis van de waarde die door de respectieve rangordemethoden wordt bepaald. Er wordt om twee aanbiedingen verzocht, zodat de twee belangrijkste in aanmerking komende aanbiedingen van deze vijf aanbiedingen worden teruggegeven.

  ![](../assets/activity_same-rank-collections.png)

+++ **Voorbeeld met meerdere criteria**

Laten we nu een voorbeeld bekijken waarbij u meerdere criteria hebt voor één bereik dat is verdeeld in verschillende groepen.

U hebt drie criteria gedefinieerd. De criteria 1 en 2 worden in groep 1 samengevoegd en criterium 3 is onafhankelijk (groep 2).

De in aanmerking komende aanbiedingen voor elke criteria en hun prioriteit (gebruikt bij de beoordeling van de rangorde) zijn als volgt:

* Groep 1:
   * Criteria 1 - (Aanbieding 1, Aanbieding 2, Aanbieding 3) - Prioriteit 1
   * Criteria 2 - (Aanbieding 3, Aanbieding 4, Aanbieding 5) - Prioriteit 1

* Groep 2:
   * Criteria 3 - (voorstel 5, voorstel 6) - Prioriteit 0

De hoogste prioritaire aanbiedingen worden eerst geëvalueerd en aan de gerangschikte lijst met aanbiedingen toegevoegd.

**Herhaling 1:**

De criteria 1 en criteria 2 voorstellen worden samen geëvalueerd (voorstel 1, voorstel 2, voorstel 3, voorstel 4, voorstel 5). Laten we zeggen dat het resultaat:

Aanbieding 1 - 10 Aanbieding 2 - 20 Aanbieding 3 - 30 uit criteria 1, 45 uit criteria 2. Het hoogste van beide wordt in overweging genomen, dus er wordt rekening gehouden met 45.
Voorstel 4 - 40 voorstel 5 - 50

Het gerangschikte voorstel is nu als volgt: Voorstel 5, voorstel 3, voorstel 4, voorstel 2, voorstel 1.

**Herhaling 2:**

Criteria 3 worden geëvalueerd (voorstel 5, voorstel 6). Laten we zeggen dat het resultaat:

* Voorstel 5 - Wordt niet geëvalueerd omdat dit al in het bovenstaande resultaat voorkomt.
* Voorstel 6 - 60

De gerangschikte voorstellen zijn nu als volgt: Voorstel 5, voorstel 3, voorstel 4, voorstel 2, voorstel 1, voorstel 6.

+++

#### Met meerdere bereiken {#multiple-scopes}

**Als duplicatie is uitgeschakeld**

Wanneer u meerdere besluitvormingsgebieden aan een besluit toevoegt en wanneer overlappingen niet zijn toegestaan op verschillende plaatsen, worden de in aanmerking komende aanbiedingen opeenvolgend geselecteerd in de volgorde van de beslissingsreikwijdte in het verzoek.

>[!NOTE]
>
>De **[!UICONTROL Allow Duplicates across placements]** parameter wordt ingesteld op het plaatsingsniveau. Als duplicatie is ingesteld op false voor plaatsing in een beslissingsverzoek, nemen alle plaatsen in het verzoek de instelling false over. [Meer informatie over de parameter duplicatie](../offer-library/creating-placements.md)

Neem een voorbeeld waarin u twee beslissingsbereiken hebt toegevoegd, zoals:

* Bereik 1: Er zijn vier in aanmerking komende aanbiedingen (voorstel 1, voorstel 2, voorstel 3, voorstel 4) en het verzoek is om twee voorstellen terug te sturen.
* Bereik 2: Er zijn vier in aanmerking komende aanbiedingen (voorstel 1, voorstel 2, voorstel 3, voorstel 4) en het verzoek is om twee voorstellen terug te sturen.

+++ **Voorbeeld 1**

De selectie ziet er als volgt uit:

1. De bovenste twee in aanmerking komende aanbiedingen uit bereik 1 worden geretourneerd (voorstel 1, voorstel 2).
1. De resterende twee in aanmerking komende aanbiedingen uit bereik 2 worden geretourneerd (voorstel 3, voorstel 4).

+++

+++ **Voorbeeld 2**

In dit voorbeeld heeft Aanbod 1 de limiet voor de frequentiegrenzen bereikt. [Meer informatie over aftopping van frequenties](../offer-library/add-constraints.md#capping)

De selectie ziet er als volgt uit:

1. De resterende twee in aanmerking komende aanbiedingen uit bereik 1 worden geretourneerd (voorstel 2, voorstel 3).
1. Het resterende in aanmerking komende aanbod uit bereik 2 wordt geretourneerd (voorstel 4).

+++

+++ **Voorbeeld 3**

In dit voorbeeld bereikten Aanbod 1 en Aanbieding 3 hun limiet voor de frequentiegrenzen. [Meer informatie over aftopping van frequenties](../offer-library/add-constraints.md#capping)

De selectie ziet er als volgt uit:

1. De resterende twee in aanmerking komende aanbiedingen uit bereik 1 worden geretourneerd (voorstel 2, voorstel 4).
1. Er zijn geen voorstellen die in aanmerking komen voor het tweede bereik, zodat de [fallback-aanbieding](#add-fallback) wordt geretourneerd.

+++

**Als duplicatie is ingeschakeld**

Wanneer duplicatie op alle plaatsen is toegestaan, kan hetzelfde aanbod meerdere keren voor verschillende plaatsen worden voorgesteld. Als deze optie is ingeschakeld, overweegt het systeem dezelfde aanbieding voor meerdere plaatsingen. [Meer informatie over de parameter duplicatie](../offer-library/creating-placements.md)

Neem het zelfde voorbeeld zoals hierboven waar u twee besluitvormingswerkingsgebied zoals toevoegde:

* Bereik 1: Er zijn vier in aanmerking komende aanbiedingen (voorstel 1, voorstel 2, voorstel 3, voorstel 4) en het verzoek is om twee voorstellen terug te sturen.
* Bereik 2: Er zijn vier in aanmerking komende aanbiedingen (voorstel 1, voorstel 2, voorstel 3, voorstel 4) en het verzoek is om twee voorstellen terug te sturen.

+++ **Voorbeeld 1**

De selectie ziet er als volgt uit:

1. De bovenste twee in aanmerking komende aanbiedingen uit bereik 1 worden geretourneerd (voorstel 1, voorstel 2).
1. Dezelfde top twee in aanmerking komende aanbiedingen uit bereik 2 worden geretourneerd (voorstel 1, voorstel 2).

+++

+++ **Voorbeeld 2**

In dit voorbeeld heeft Aanbod 1 de limiet voor de frequentiegrenzen bereikt. [Meer informatie over aftopping van frequenties](../offer-library/add-constraints.md#capping)

De selectie ziet er als volgt uit:

1. De resterende twee in aanmerking komende aanbiedingen uit bereik 1 worden geretourneerd (voorstel 2, voorstel 3).

1. Dezelfde resterende twee in aanmerking komende aanbiedingen uit bereik 2 worden geretourneerd (voorstel 2, voorstel 3).

+++

+++ **Voorbeeld 3**

In dit voorbeeld bereikten Aanbod 1 en Aanbieding 3 hun limiet voor de frequentiegrenzen. [Meer informatie over aftopping van frequenties](../offer-library/add-constraints.md#capping)

De selectie ziet er als volgt uit:

1. De resterende twee in aanmerking komende aanbiedingen uit bereik 1 worden geretourneerd (voorstel 2, voorstel 4).

1. Dezelfde resterende twee in aanmerking komende aanbiedingen uit bereik 2 worden geretourneerd (voorstel 2, voorstel 4).

+++

## Een fallback-aanbieding toevoegen {#add-fallback}

Zodra u het besluitvormingswerkingsgebied bepaalde, bepaal de reserveaanbieding die als laatste redmiddel aan de klanten zal worden voorgesteld die niet de regels en de beperkingen van de aanbiedingen geschiktheid aanpassen.

U doet dit door het te selecteren in de lijst met beschikbare fallback-aanbiedingen voor de plaatsingen die in de beslissing zijn gedefinieerd, en vervolgens op **[!UICONTROL Next]**.

![](../assets/add-fallback-offer.png)

>[!NOTE]
>
>U kunt op de knop **[!UICONTROL Open offer library]** koppeling om de lijst met aanbiedingen op een nieuw tabblad weer te geven.

## Beslissing bekijken en opslaan {#review}

Als alles behoorlijk wordt gevormd, toont een samenvatting van de beslissingseigenschappen.

1. Zorg ervoor dat het besluit klaar is om te worden gebruikt om aanbiedingen aan klanten voor te stellen. Alle besluitvormingswerkingsgebieden en de reserveaanbieding het bevat worden getoond.

   ![](../assets/review-decision.png)

1. U kunt elke plaatsing uitvouwen of samenvouwen. U kunt voor elke plaatsing een voorvertoning weergeven van de beschikbare voorstellen, de geschiktheid en de rangschikkingsgegevens. U kunt ook informatie weergeven over de geschatte gekwalificeerde profielen. Klikken **[!UICONTROL Refresh]** gegevens bijwerken.

   ![](../assets/review-decision-details.png)

1. Klik op **[!UICONTROL Finish]**.
1. Selecteer **[!UICONTROL Save and activate]**.

   ![](../assets/save-activities.png)

   U kunt de beslissing ook opslaan als concept, zodat u deze later kunt bewerken en activeren.

De beslissing wordt in de lijst weergegeven met de **[!UICONTROL Live]** of **[!UICONTROL Draft]** status, afhankelijk van het feit of u deze al dan niet hebt geactiveerd in de vorige stap.

Het is nu klaar om te worden gebruikt om aanbiedingen aan klanten te leveren.

## Beslissingenlijst {#decision-list}

In de beslissingslijst kunt u de beslissing selecteren om de eigenschappen ervan weer te geven. Daar kunt u het ook bewerken, de status ervan wijzigen (**Concept**, **Live**, **Voltooid**, **Gearchiveerd**), de beslissing dupliceren of verwijderen.

![](../assets/decision_created.png)

Selecteer de **[!UICONTROL Edit]** om terug te gaan naar de modus voor beslissingseditie, waar u de beslissing kunt wijzigen [details](#create-activity), [beslissingsbereik](#add-decision-scopes) en [fallback-aanbieding](#add-fallback).

>[!IMPORTANT]
>
>Als er wijzigingen worden aangebracht in een biedbesluit dat wordt gebruikt in een reisbericht, moet u de reis ongedaan maken en opnieuw publiceren.  Dit zal ervoor zorgen dat de veranderingen in het reisbericht worden opgenomen en dat de boodschap in overeenstemming is met de meest recente updates.

Selecteer een live beslissing en klik op **[!UICONTROL Deactivate]** om de beslissingsstatus terug te brengen naar **[!UICONTROL Draft]**.

De status opnieuw instellen op **[!UICONTROL Live]**, selecteert u de **[!UICONTROL Activate]** die nu wordt weergegeven.

![](../assets/decision_activate.png)

De **[!UICONTROL More actions]** schakelt u de hieronder beschreven handelingen in.

![](../assets/decision_more-actions.png)

* **[!UICONTROL Complete]**: stelt de status van het besluit in op **[!UICONTROL Complete]**, wat betekent dat het besluit niet meer kan worden genoemd. Deze handeling is alleen beschikbaar voor geactiveerde beslissingen. Het besluit is nog steeds beschikbaar in de lijst, maar u kunt de status niet terugzetten op **[!UICONTROL Draft]** of **[!UICONTROL Approved]**. U kunt het alleen dupliceren, verwijderen of archiveren.

* **[!UICONTROL Duplicate]**: maakt een beslissing met dezelfde eigenschappen, hetzelfde beslissingsbereik en hetzelfde fallback-aanbod. Het nieuwe besluit heeft standaard de **[!UICONTROL Draft]** status.

* **[!UICONTROL Delete]**: verwijdert de beslissing uit de lijst.

  >[!CAUTION]
  >
  >Het besluit en de inhoud ervan zijn niet meer toegankelijk. Deze handeling kan niet ongedaan worden gemaakt.
  >
  >Als de beslissing in een ander object wordt gebruikt, kan deze niet worden verwijderd.

* **[!UICONTROL Archive]**: stelt de beslissingsstatus in op **[!UICONTROL Archived]**. Het besluit is nog steeds beschikbaar in de lijst, maar u kunt de status niet terugzetten op **[!UICONTROL Draft]** of **[!UICONTROL Approved]**. U kunt deze alleen dupliceren of verwijderen.

U kunt ook de status van meerdere beslissingen tegelijk verwijderen of wijzigen door de desbetreffende selectievakjes in te schakelen.

![](../assets/decision_multiple-selection.png)

Als u de status wilt wijzigen van verschillende beslissingen met verschillende statussen, worden alleen de desbetreffende statussen gewijzigd.

![](../assets/decision_change-status.png)

Nadat u een beslissing hebt gemaakt, kunt u in de lijst op de naam ervan klikken.

![](../assets/decision_click-name.png)

Dit laat u toe om tot gedetailleerde informatie voor dat besluit toegang te hebben. Selecteer de **[!UICONTROL Change log]** tab naar [alle wijzigingen controleren](../get-started/user-interface.md#changes-log) die op het besluit zijn genomen.

![](../assets/decision_information.png)

## Hoe kan ik-video{#video}

Leer hoe u aanbiedingsactiviteiten kunt maken in besluitvormingsbeheer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)


