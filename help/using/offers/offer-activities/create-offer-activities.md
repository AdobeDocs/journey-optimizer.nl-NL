---
title: Beslissingen maken
description: Leer hoe u beslissingen maakt
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1389'
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

   Elk criterium bestaat uit een verzameling aanbiedingen die gekoppeld is aan een geschiktheidsbeperking en een waarderingsmethode om de aanbiedingen te bepalen die in de plaatsing moeten worden getoond.

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

1. Wanneer u publiek of beslissingsregels selecteert, kunt u informatie over de geschatte gekwalificeerde profielen zien. Klikken **[!UICONTROL Refresh]** om gegevens bij te werken.

   >[!NOTE]
   >
   >Profielramingen zijn niet beschikbaar wanneer regelparameters gegevens bevatten die niet in het profiel staan, zoals contextgegevens. Bijvoorbeeld, een toelatingsregel die het huidige weer om 80 graden vereist te zijn.

   ![](../assets/activity_constraint-estimate.png)

1. Definieer de waarderingsmethode die u wilt gebruiken om de beste aanbieding voor elk profiel te selecteren. [Meer informatie](../offer-activities/configure-offer-selection.md).

   ![](../assets/activity_ranking-method.png)

   * Als meerdere aanbiedingen standaard in aanmerking komen voor deze plaatsing, wordt de opdracht **[!UICONTROL Offer priority]** de methode gebruikt de waarde die in de aanbiedingen is gedefinieerd: het aanbod met de hoogste prioriteitsscore zal aan de gebruiker worden geleverd.

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

1. Als u een andere plaatsing voor uw voorstellen wilt toevoegen als onderdeel van deze beslissing, gebruikt u de opdracht **[!UICONTROL New scope]** knop. Herhaal bovenstaande stappen voor elk beslissingsbereik.

   ![](../assets/activity_new-scope.png)

### Volgorde van de beoordelingscriteria {#evaluation-criteria-order}

Zoals hierboven is beschreven, bestaan de evaluatiecriteria uit een verzameling, subsidiabiliteitsbeperkingen en een rangorde. U kunt de opeenvolgende orde plaatsen u voor de evaluatiecriteria wilt worden geëvalueerd, maar u kunt veelvoudige evaluatiecriteria ook combineren zodat zij samen en niet afzonderlijk worden geëvalueerd.

U hebt bijvoorbeeld twee verzamelingen, één in evaluatiecriteria A en één in evaluatiecriteria B. Er worden twee voorstellen teruggestuurd. Laten we zeggen dat er twee in aanmerking komende aanbiedingen zijn uit evaluatiecriteria A en drie in aanmerking komende aanbiedingen uit evaluatiecriteria B.

* Indien de twee evaluatiecriteria **niet gecombineerd** en/of in sequentiële volgorde (1 en 2) worden de twee belangrijkste in aanmerking komende aanbiedingen uit de evaluatiecriteria in de eerste rij teruggegeven. Als er niet twee in aanmerking komende aanbiedingen voor de eerste evaluatiecriteria zijn, zal de beslissingsmotor achtereenvolgens overgaan op de volgende evaluatiecriteria om te zien hoeveel aanbiedingen nog nodig zijn, en uiteindelijk een terugslag teruggeven indien nodig.

  ![](../assets/activity_consecutive-rank-collections.png)

* Als de twee verzamelingen **tegelijk geëvalueerd** Aangezien er twee in aanmerking komende aanbiedingen zijn op basis van beoordelingscriteria A en drie in aanmerking komende aanbiedingen op basis van beoordelingscriteria B, worden de vijf offertes in een stapel geplaatst op basis van de waarde die door de respectieve rangordemethoden wordt bepaald. Er wordt om twee aanbiedingen verzocht, zodat de twee belangrijkste in aanmerking komende aanbiedingen van deze vijf aanbiedingen worden teruggegeven.

  ![](../assets/activity_same-rank-collections.png)

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

1. U kunt elke plaatsing uitvouwen of samenvouwen. U kunt voor elke plaatsing een voorvertoning weergeven van de beschikbare voorstellen, de geschiktheid en de waarderingsdetails. U kunt ook informatie weergeven over de geschatte gekwalificeerde profielen. Klikken **[!UICONTROL Refresh]** om gegevens bij te werken.

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

Selecteer **[!UICONTROL Edit]** om terug te gaan naar de modus voor beslissingseditie, waar u de beslissing kunt wijzigen [details](#create-activity), [beslissingsbereik](#add-decision-scopes) en [fallback-aanbieding](#add-fallback).

>[!IMPORTANT]
>
>Als er wijzigingen worden aangebracht in een biedbesluit dat wordt gebruikt in een reisbericht, moet u de reis ongedaan maken en opnieuw publiceren.  Dit zal ervoor zorgen dat de veranderingen in het reisbericht worden opgenomen en dat de boodschap in overeenstemming is met de meest recente updates.

Selecteer een live beslissing en klik op **[!UICONTROL Deactivate]** om de beslissingsstatus terug te brengen naar **[!UICONTROL Draft]**.

De status opnieuw instellen op **[!UICONTROL Live]**, selecteert u de **[!UICONTROL Activate]** die nu wordt weergegeven.

![](../assets/decision_activate.png)

De **[!UICONTROL More actions]** schakelt u de hieronder beschreven handelingen in.

![](../assets/decision_more-actions.png)

* **[!UICONTROL Complete]**: stelt de status van de beslissing in op **[!UICONTROL Complete]**, wat betekent dat het besluit niet meer kan worden genoemd. Deze handeling is alleen beschikbaar voor geactiveerde beslissingen. Het besluit is nog steeds beschikbaar in de lijst, maar u kunt de status niet terugzetten op **[!UICONTROL Draft]** of **[!UICONTROL Approved]**. U kunt het alleen dupliceren, verwijderen of archiveren.

* **[!UICONTROL Duplicate]**: een besluit met dezelfde eigenschappen, beslissingsbereik en terugvalaanbieding. Het nieuwe besluit heeft standaard de **[!UICONTROL Draft]** status.

* **[!UICONTROL Delete]**: Hiermee verwijdert u de beslissing uit de lijst.

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

Dit laat u toe om tot gedetailleerde informatie voor dat besluit toegang te hebben. Selecteer **[!UICONTROL Change log]** tab naar [alle wijzigingen controleren](../get-started/user-interface.md#changes-log) die op het besluit zijn genomen.

![](../assets/decision_information.png)

## Hoe kan ik-video{#video}

Leer hoe u aanbiedingsactiviteiten kunt maken in besluitvormingsbeheer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)


