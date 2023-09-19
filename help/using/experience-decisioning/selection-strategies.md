---
title: Selectiestrategieën maken
description: Leer hoe u selectiestrategieën maakt
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 4aea5c1434caa07aad26445c49a3d5c6274502ec
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 1%

---

# Selectiestrategieën maken {#selection-strategies}

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Aan de slag met Experience Decisition](gs-experience-decisioning.md)
* Je beslissingsobjecten beheren
   * [De itemcatalogus configureren](catalogs.md)
   * [Beslissingsitems maken](items.md)
   * [Objectverzamelingen beheren](collections.md)
* Selectie van items configureren
   * [Beslissingsregels maken](rules.md)
   * [Classificatiemethoden maken](ranking.md)
* **[Selectiestrategieën maken](selection-strategies.md)**
* [Beslissingsbeleid maken](create-decision.md)

>[!ENDSHADEBOX]

Een selectiestrategie is een herbruikbaar item, dat bestaat uit een verzameling die gekoppeld is aan een geschiktheidsbeperking en een rangschikkingsmethode om de aanbiedingen te bepalen die moeten worden getoond wanneer ze worden geselecteerd in een [beslissingsbeleid](create-decision.md).

## Selectiestrategieën openen en beheren

1. Ga naar **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Configuration]** > **[!UICONTROL Selection strategies]**.

1. Alle selectiestrategieën die tot nu toe zijn ontwikkeld, worden vermeld. Er zijn filters beschikbaar waarmee u volgens de waarderingsmethode strategieën kunt ophalen.

   ![](assets/strategy-list-filters.png)

1. Klik op de naam van een selectiestrategie om deze te bewerken.

1. De voor elke strategie geselecteerde verzameling, rangschikkingsmethode en geschiktheid worden ook weergegeven. U kunt op het pictogram naast elke verzamelingsnaam klikken om een verzameling rechtstreeks te bewerken.

   ![](assets/strategy-list-edit-collection.png)

## Een selectiestrategie maken

Volg onderstaande stappen om een selectiestrategie te maken.

1. Van de **[!UICONTROL Selection strategies]** voorraad, klik **[!UICONTROL Create selection strategy]**.

   ![](assets/strategy-create-button.png)

1. Voeg een naam toe voor uw strategie.

   >[!NOTE]
   >
   >Momenteel alleen de standaardwaarde **[!UICONTROL Offers]** catalogus is beschikbaar.

1. Vul de gegevens voor de selectiestrategie in, te beginnen met de naam.

   ![](assets/strategy-create-screen.png)

1. Selecteer de aanbieding [collectie](collections.md) dat de aanbiedingen bevat die in overweging moeten worden genomen.

1. Gebruik de **[!UICONTROL Eligibility]** om de selectie van de aanbiedingen voor deze selectiestrategie te beperken.

   ![](assets/strategy-create-eligibility.png)

   * Als u de selectie van de aanbiedingen wilt beperken tot de leden van een publiek in een Experience Platform, selecteert u **[!UICONTROL Audiences]** en kiest u een publiek in de lijst. [Leer hoe u met het publiek kunt werken](../audience/about-audiences.md)

   * Als u een selectiegrens met een beslissingsregel wilt toevoegen, gebruikt u de optie **[!UICONTROL Decision rule]** en selecteert u de gewenste regel. [Leer hoe u een regel maakt](rules.md)

1. Definieer de waarderingsmethode die u wilt gebruiken om de beste aanbieding voor elk profiel te selecteren. [Meer informatie](#select-ranking-method)

   ![](assets/strategy-create-ranking.png)

   * Als er meerdere aanbiedingen in aanmerking komen voor deze strategie, worden standaard de [Voorstelprioriteit](#offer-priority) Deze methode gebruikt de waarde die in de aanbiedingen is gedefinieerd.

   * Als u een specifieke berekende score wilt gebruiken om te kiezen welke aanbieding in aanmerking komt, selecteert u [Formule](#ranking-formula) of [AI-model](#ai-ranking).

1. Klik op **[!UICONTROL Create]**. Het is nu klaar om in een [beslissing](create-decision.md)

## Een waarderingsmethode selecteren {#select-ranking-method}

Als meerdere aanbiedingen in aanmerking komen voor een bepaalde selectiestrategie, kunt u bij het maken van een selectiestrategie de methode kiezen waarmee u de beste aanbieding voor elk profiel kunt selecteren. Je kunt voorstellen plaatsen op:

* [Voorstelprioriteit](#offer-priority)
* [Formule](#ranking-formula)
* [AI-rangschikking](#ai-ranking)

### Voorstelprioriteit {#offer-priority}

Wanneer meerdere aanbiedingen in aanmerking komen voor een bepaalde plaatsing in een beslissing, worden standaard de items met de hoogste **prioriteit** wordt eerst aan de klanten geleverd.

![](assets/item-priority.png)

De prioritaire scores van aanbiedingen worden toegewezen wanneer het creëren van [beslissingsitem](items.md).

### Willekeurige formule {#ranking-formula}

Met Journey Optimizer kunt u niet alleen prioriteit bieden, maar ook **waarderingsformules**. Dit zijn formules die bepalen welke aanbieding eerst voor een bepaalde plaatsing moet worden gepresenteerd, in plaats van rekening te houden met de prioriteitsscores van de aanbiedingen.

U kunt bijvoorbeeld de prioriteit verhogen van alle aanbiedingen met een einddatum van minder dan 24 uur, of aanbiedingen verhogen van de categorie &quot;actief&quot; als het interessepunt van het profiel &quot;actief&quot; is. Leer hoe u een waarderingsformule maakt in [deze sectie](ranking.md).

Nadat u de formule hebt gemaakt, kunt u deze gebruiken in een selectiestrategie. Als meerdere aanbiedingen in aanmerking komen om te worden ingediend bij het gebruik van deze selectiestrategie, wordt in de beslissing de geselecteerde formule gebruikt om te berekenen welke aanbieding het eerst moet worden geleverd.

### AI-rangschikking {#ai-ranking}

U kunt ook een getraind modelsysteem gebruiken dat aanbiedingen voor een bepaald profiel automatisch rangschikt door een AI-model te selecteren. Leer hoe u een AI-model maakt in [deze sectie](ranking.md).

Nadat u een AI-model hebt gemaakt, kunt u het gebruiken in een selectiestrategie. Indien meerdere aanbiedingen in aanmerking komen, bepaalt het opgeleide modelsysteem welke aanbieding eerst voor deze selectiestrategie moet worden ingediend.

