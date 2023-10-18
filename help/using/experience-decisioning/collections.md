---
title: Verzamelingen
description: Leer hoe u met verzamelingen werkt
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 3%

---

# Verzamelingen {#collections}

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Aan de slag met Experience Decisition](gs-experience-decisioning.md)
* Je beslissingsobjecten beheren
   * [De itemcatalogus configureren](catalogs.md)
   * [Beslissingsitems maken](items.md)
   * **[Objectverzamelingen beheren](collections.md)**
* Selectie van items configureren
   * [Beslissingsregels maken](rules.md)
   * [Classificatiemethoden maken](ranking.md)
* [Selectiestrategieën maken](selection-strategies.md)
* [Beslissingsbeleid maken](create-decision.md)

>[!ENDSHADEBOX]

Met verzamelingen kunt u uw beslissingsitems categoriseren en groeperen op basis van uw voorkeuren. Deze categorieën worden gecreeerd door het ontwerpen van regels die hefboomwerking de attributen van besluitvormingspunten.

Bijvoorbeeld, laten wij zeggen u een &quot;Categorie&quot;douanekenmerk aan het catalogusschema van uw besluitvormingspunten hebt toegevoegd. Dit staat u toe om een inzameling tot stand te brengen die alle besluitpunten met de waarde &quot;Yoga&quot;in het &quot;attribuut van de Categorie&quot;omvat.

De lijst met verzamelingen kan worden geraadpleegd via de **[!UICONTROL Items]** -menu.

Ga als volgt te werk om een verzameling te maken:

1. Navigeren naar **[!UICONTROL Items]** > **[!UICONTROL Collections]** en klik op **[!UICONTROL Create collection]**.
1. Geef een naam en een beschrijving voor de verzameling op.
1. Voeg één of veelvoudige regels toe om de punten te bepalen die in de inzameling moeten worden omvat. Dit doet u als volgt:

   1. Kies een itemkenmerk dat u als criterium wilt gebruiken. De lijst met kenmerken bevat alle standaard- en aangepaste kenmerken die zijn gedefinieerd in het catalogusschema. [Meer informatie over de objectcatalogus](catalogs.md)
   1. Selecteer de gewenste operator en voer de waarde in waarop u wilt filteren.
   1. Herhaal deze stappen om zoveel regels toe te voegen als nodig is. Wanneer u meerdere regels toevoegt, kunt u kiezen tussen de **en** en **of** exploitanten om ze te combineren. Klik hiertoe op het bedieningspaneel om te schakelen tussen de twee keuzen.

   ![](assets/collection-create.png)

1. Als de verzamelingsregels zijn gedefinieerd, klikt u op **[!UICONTROL Create]**. De verzameling wordt nu in de lijst weergegeven.
