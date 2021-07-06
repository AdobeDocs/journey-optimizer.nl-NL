---
title: Aangepaste aanbiedingen in een e-mail gebruiken
description: Ontdek een voorbeeld van begin tot eind dat alle stappen toont nodig om aanbiedingen te vormen en hen in een e-mail te gebruiken.
feature: Aanbiedingen
topic: Integraties
role: User
level: Intermediate
source-git-commit: a25264cb43f77671c29f18522110fd85d0155697
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 3%

---

# Hoofdlettergebruik: Aangepaste aanbiedingen configureren om deze in een e-mail te gebruiken {#configure-add-personalized-offers-email}

Deze sectie stelt een voorbeeld van begin tot eind voor om te tonen hoe te om aanbiedingen te vormen en hen te gebruiken in een e-mail, die op een besluit wordt gebaseerd u eerder creeerde.

## Belangrijkste stappen

De belangrijkste stappen om aanbiedingen te vormen, hen te omvatten in een besluit en hefboomwerking dit besluit in een e-mail zijn hieronder vermeld:

1. Voordat u aanbiedingen maakt, [definieert u uw componenten](#define-components)

   * Plaatsingen maken
   * Beslissingsregels maken
   * Tags maken
   * Classificaties maken (optioneel)

1. [De aanbiedingen configureren](#configure-offers)

   * Aanbiedingen maken
   * Voor elke aanbieding:

      * Weergaven maken en een plaatsing en een element selecteren voor elke representatie
      * Voeg een regel toe voor elke aanbieding
      * Een prioriteit voor elke aanbieding definiëren

1. [Een alternatieve aanbieding maken](#create-fallback)

1. [Maak een ](#create-collection) verzameling waarin de door u gemaakte persoonlijke aanbiedingen worden opgenomen

1. [De beslissing configureren](#configure-decision)

   * Een beslissing nemen
   * Selecteer de plaatsen u creeerde
   * Selecteer voor elke plaatsing de verzameling
   * Selecteer voor elke plaatsing een positie (optioneel)
   * Selecteer de fallback

1. [De beslissing invoegen in een e-mail](#insert-decision-in-email)

   * Selecteer een plaatsing die overeenkomt met de aanbiedingen die u wilt weergeven
   * Selecteer de beslissing uit de items die compatibel zijn met de geselecteerde plaatsing
   * Je voorstellen bekijken

Het algemene besluitvormingsproces voor het gebruik van aanbiedingen in een e-mail kan als volgt worden beschreven:

![](../assets/offers-e2e-process.png)

## De componenten definiëren {#define-components}

Voordat u aanbiedingen gaat maken, moet u verschillende componenten definiëren die u in uw aanbiedingen wilt gebruiken.

U vindt ze onder **[!UICONTROL Decision Management]** > **[!UICONTROL Components menu]**.

1. Begin door **plaatsingen** voor uw aanbiedingen te creëren.

   U gebruikt deze plaatsingen om te bepalen waar de resulterende aanbieding zal verschijnen wanneer het bepalen van uw biedingsbesluit.

   In dit voorbeeld maakt u drie plaatsen met de volgende kanaal- en inhoudstypen:

   * *Web - Afbeelding*
   * *E-mail - Afbeelding*
   * *Niet-digitaal - tekst*

   ![](../assets/offers-e2e-placements.png)

   De gedetailleerde stappen om plaatsingen tot stand te brengen worden beschreven in [deze sectie](../../using/offers/offer-library/creating-placements.md).

1. Maak **beslissingsregels**.

   Beslissingsregels zullen een profiel in Adobe Experience Platform het beste aanbieden.

   Vorm twee eenvoudige regels door het **[!UICONTROL XDM Individual Profile > Person > Gender]** attribuut te gebruiken:

   * *Vrouwelijke klanten*
   * *Mannelijke klanten*

   ![](../assets/offers-e2e-rules.png)

   De gedetailleerde stappen om regels tot stand te brengen worden beschreven in [deze sectie](../../using/offers/offer-library/creating-decision-rules.md).

1. U kunt ook een **tag** maken.

   Vervolgens kunt u het aan uw aanbiedingen koppelen en deze tag gebruiken om uw voorstellen samen in een verzameling te groeperen.

   In dit voorbeeld maakt u de tag *Yoga*.

   ![](../assets/offers-e2e-tag.png)

   De gedetailleerde stappen voor het maken van tags worden beschreven in [deze sectie](../../using/offers/offer-library/creating-tags.md).

1. Als u regels wilt definiëren die bepalen welke aanbieding als eerste voor een bepaalde plaatsing moet worden gepresenteerd (in plaats van rekening te houden met de prioriteitsscores van de aanbiedingen), kunt u een **rangschikkingsformule** maken.

   De gedetailleerde stappen om rangschikkingsformules tot stand te brengen worden beschreven in [deze sectie](../../using/offers/offer-library/create-ranking-formulas.md#create-ranking-formula).

   >[!NOTE]
   >
   >In dit voorbeeld zullen we alleen de prioriteitsscores gebruiken. Meer informatie over [geschiktheidsregels en beperkingen](../../using/offers/offer-library/creating-personalized-offers.md#eligibility).

## Aanbiedingen configureren {#configure-offers}

U kunt nu uw aanbiedingen maken en configureren. In dit voorbeeld maakt u vier aanbiedingen die u volgens elk specifiek profiel wilt weergeven.

1. Een aanbieding maken. Meer informatie vindt u in [deze sectie](../../using/offers/offer-library/creating-personalized-offers.md#create-offer).

1. In deze aanbieding, creeer drie vertegenwoordiging. Elke vertegenwoordiging moet een combinatie van een plaatsing zijn die u vroeger creeerde en activa:

   * Eén voor de plaatsing *Web - Afbeelding*
   * Eén voor de *e-mail - Afbeelding*-plaatsing
   * Eén voor de *Niet-digitaal - Text*-plaatsing

   >[!NOTE]
   >
   >Een aanbieding kan op verschillende plaatsen in een bericht worden getoond om meer kansen tot gebruik van de aanbieding in verschillende plaatsingscontexten tot stand te brengen.

   Leer meer op vertegenwoordiging in [deze sectie](../../using/offers/offer-library/creating-personalized-offers.md#representations).

1. Selecteer een geschikte afbeelding voor de eerste twee plaatsen. Voer aangepaste tekst in voor de plaatsing *Niet-digitaal - Tekst*.

   ![](../assets/offers-e2e-representations.png)

1. Selecteer **[!UICONTROL Offer eligibility]** in de sectie **[!UICONTROL By defined decision rule]** en sleep de regel van uw keuze.

   ![](../assets/offers-e2e-eligibility.png)

1. Vul **[!UICONTROL Priority]** in. In dit voorbeeld voegt u *25* toe.

1. Controleer uw voorstel en klik op **[!UICONTROL Save and approve]**.

   ![](../assets/offers-e2e-review.png)

1. In dit voorbeeld maakt u nog drie aanbiedingen met dezelfde weergaven, maar met verschillende elementen. Wijs hen met verschillende regels en prioriteiten toe, zoals:

   * Eerste aanbieding - Beslissingsregel: *Vrouwelijke klanten*, prioriteit: *25*
   * Tweede aanbod - Beslissingsregel: *Vrouwelijke klanten*, prioriteit: *15*
   * Derde aanbieding - Beslissingsregel: *Mannelijke klanten*, prioriteit: *25*
   * Vierde aanbod - Beslissingsregel: *Mannelijke klanten*, prioriteit: *15*

   ![](../assets/offers-e2e-offers-created.png)

De gedetailleerde stappen om aanbiedingen tot stand te brengen en te vormen worden beschreven in [deze sectie](../../using/offers/offer-library/creating-personalized-offers.md).

## Een alternatieve aanbieding maken {#create-fallback}

1. Een alternatieve aanbieding maken.

1. Definieer dezelfde representaties als voor de aanbiedingen, met de juiste middelen (deze moeten verschillen van de afbeeldingen die in uw aanbiedingen worden gebruikt).

   Elke vertegenwoordiging moet een combinatie van een plaatsing zijn die u vroeger creeerde en activa:

   * Eén voor de plaatsing *Web - Afbeelding*
   * Eén voor de *e-mail - Afbeelding*-plaatsing
   * Eén voor de *Niet-digitaal - Text*-plaatsing

   ![](../assets/offers-e2e-fallback-representations.png)

1. Herzie uw reserveaanbieding, dan klik **[!UICONTROL Save and approve]**.

![](../assets/offers-e2e-fallback.png)

Je fallbackvoorstel is nu klaar om te worden gebruikt in een beslissing.

De gedetailleerde stappen om een reserveaanbieding tot stand te brengen en te vormen worden beschreven in [deze sectie](../../using/offers/offer-library/creating-fallback-offers.md).

## Een verzameling maken {#create-collection}

Wanneer het vormen van het besluit, zult u uw gepersonaliseerde aanbiedingen als deel van een inzameling moeten toevoegen.

1. Om het besluitvormingsproces te versnellen, creeer een dynamische inzameling.

1. Gebruik de tag *Yoga* om de vier persoonlijke aanbiedingen te selecteren die u eerder hebt gemaakt.

   ![](../assets/offers-e2e-collection-using-tag.png)

De gedetailleerde stappen om een inzameling tot stand te brengen worden beschreven in [deze sectie](../../using/offers/offer-library/creating-collections.md).

## De beslissing configureren {#configure-decision}

Nu moet u een besluit maken dat plaatsingen zal combineren met de gepersonaliseerde aanbiedingen en het fallback-aanbod dat u net hebt gemaakt.

Deze combinatie wordt door de Offer decisioning-engine gebruikt om de beste aanbieding voor een specifiek profiel te vinden: in dit voorbeeld zal het gebaseerd zijn op de prioriteit en beslissingsregel u aan elk aanbod toewees.

Om een aanbiedingsbesluit tot stand te brengen en te vormen, volg de belangrijkste stappen hieronder:

1. Een beslissing nemen. Meer informatie vindt u in [deze sectie](../../using/offers/offer-activities/create-offer-activities.md#create-activity).

1. Selecteer *Web - Afbeelding*, *E-mail - Afbeelding* en *Niet-digitaal - Tekst* plaatsen.

   ![](../assets/offers-e2e-decision-placements.png)

1. Voeg voor elke plaatsing de verzameling toe die u hebt gemaakt.

   ![](../assets/offers-e2e-decision-collection.png)

1. Als u een rangschikking bepaalde wanneer [bouwend uw componenten](#define-components), kunt u het aan een plaatsing in het besluit toewijzen. Indien meerdere aanbiedingen in aanmerking komen om in deze plaatsing te worden gepresenteerd, wordt in de beslissing gebruik gemaakt van deze formule om te berekenen welke aanbieding het eerst wordt geleverd.

   De gedetailleerde stappen om een rangschikkende formule aan een plaatsing toe te wijzen worden beschreven in [deze sectie](../../using/offers/offer-activities/configure-offer-selection.md#assign-ranking-formula).

1. Selecteer de fallback-aanbieding die u hebt gemaakt. Het wordt weergegeven als een beschikbare fallback-aanbieding voor de drie geselecteerde plaatsingen.

   ![](../assets/offers-e2e-decision-fallback.png)

1. Herzie uw besluit, dan klik **[!UICONTROL Save and approve]**.

   ![](../assets/offers-e2e-review-decision.png)

Uw beslissing is nu klaar om te worden gebruikt voor het aanbieden van geoptimaliseerde en persoonlijke aanbiedingen.

De gedetailleerde stappen om een besluit tot stand te brengen en te vormen worden beschreven in [deze sectie](../../using/offers/offer-activities/create-offer-activities.md).

## De beslissing invoegen in een e-mail {#insert-decision-in-email}

Nu uw beslissing live is, kunt u deze invoegen in een e-mailbericht. Hiervoor voert u de volgende stappen uit:

1. Maak uw e-mail en open vervolgens [E-mailontwerper](../../using/design-emails.md) om de inhoud ervan te configureren.

1. Voeg een structuurcomponent toe vanuit het linkerpalet.

1. Voeg een **[!UICONTROL Offer decision]** inhoudscomponent toe. Leer hoe te om inhoudscomponenten in [deze sectie](../../using/content-components.md) te gebruiken.

   ![](../assets/offers-e2e-decision-component.png)

1. Selecteer het. Klik in het rechterpalet op **[!UICONTROL Select offer decision]** om een beslissing toe te voegen.

   ![](../assets/offers-e2e-select-offer-decision.png)

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Placements]** de plaatsing die overeenkomt met de aanbiedingen die u wilt weergeven.

   In dit geval, van de plaatsingen die u eerder als deel van dit voorbeeld creeerde, slechts is **E-mail - Beeld** plaatsing beschikbaar aangezien u de beslissing in een e-mail wilt gebruiken. Meer informatie over [plaatsen maken](../../using/offers/offer-library/creating-placements.md).

   ![](../assets/offers-e2e-select-placement-in-decision.png)

1. Besluiten die overeenkomen met de plaatsing **E-mail - Afbeelding** worden weergegeven. Selecteer de beslissing die u in de inhoudscomponent wilt gebruiken en klik op **[!UICONTROL Add]**.

   ![](../assets/offers-e2e-matching-placement-in-decision.png)

   >[!NOTE]
   >
   >Alleen beslissingen die compatibel zijn met de geselecteerde plaatsing worden weergegeven in de lijst.

U ziet nu alle persoonlijke aanbiedingen en de fallback-aanbieding die in de e-mailontwerper worden weergegeven.

![](../assets/offers-e2e-offers-displayed.png)

Gebruik de sectie **[!UICONTROL Offers]** of de inhoudcomponenten pijlen (rechter en linkerpijlen) om gegevens te doorbladeren. U kunt de verschillende aanbiedingen die deel uitmaken van het besluit ook met een klantenprofiel tonen. Meer informatie vindt u in [deze sectie](../../using/deliver-personalized-offers.md#preview-offers-in-email).

Nadat u uw wijzigingen hebt opgeslagen en het bericht is gepubliceerd, kunt u uw voorstellen weergeven voor de relevante profielen wanneer u het bericht verzendt als onderdeel van een reis.

**Verwante onderwerpen:**

* Leer hoe te om de berichtvoorproef in [deze sectie](../../using/preview.md#preview-your-messages) te controleren.

* Leer hoe te om berichten in [deze sectie](../../using/publish-manage-message.md) te publiceren.

* Leer hoe berichten door één of meerdere reizen in [deze sectie](../building-journeys/journey.md) worden teweeggebracht.

