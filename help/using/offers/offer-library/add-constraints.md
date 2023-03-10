---
title: Beperkingen aan een aanbieding toevoegen
description: Leer hoe u de voorwaarden voor een aanbieding definieert die moeten worden weergegeven
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: 1bb5fbdc08f8650132e191e659b03caadae8edf4
workflow-type: tm+mt
source-wordcount: '2121'
ht-degree: 1%

---

# Beperkingen aan een aanbieding toevoegen {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="Over aanbiedingsbeperkingen"
>abstract="Met beperkingen, kunt u specificeren hoe de aanbieding aan de gebruiker in vergelijking met andere aanbiedingen voorrang wordt gegeven en wordt voorgesteld."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="Over aanbiedingsbeperkingen"
>abstract="Met beperkingen, kunt u specificeren hoe de aanbieding aan de gebruiker in vergelijking met andere aanbiedingen voorrang wordt gegeven en wordt voorgesteld."

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="Info over aanbiedingsprioriteit"
>abstract="Op dit gebied, kunt u prioritaire montages voor de aanbieding specificeren. Prioriteit is een nummer dat wordt gebruikt om aanbiedingen te rangschikken die aan alle beperkingen voldoen, zoals geschiktheid, datums en aftopping."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="Prioriteit instellen"
>abstract="De prioritaire hulp bepaalt de prioriteit van de aanbieding in vergelijking met andere als de gebruiker voor meer dan één aanbieding in aanmerking komt. Hoe hoger de prioriteit van een aanbieding is, hoe hoger de prioriteit ervan wordt vergeleken met andere aanbiedingen."

Met beperkingen kunt u de voorwaarden definiëren waaronder een aanbieding wordt weergegeven.

1. Configureer de **[!UICONTROL Offer eligibility]**. [Meer informatie](#eligibility)

   ![](../assets/offer-eligibility.png)

1. Definieer de **[!UICONTROL Priority]** van de aanbieding in vergelijking met andere aanbiedingen indien de gebruiker voor meer dan één aanbieding in aanmerking komt. Hoe hoger de prioriteit van een aanbieding is, hoe hoger de prioriteit ervan wordt vergeleken met andere aanbiedingen.

   ![](../assets/offer-priority.png)

1. Geef de aanbiedingen op **[!UICONTROL Capping]**, wat het aantal keren betekent dat het aanbod zal worden ingediend. [Meer informatie](#capping)

   ![](../assets/offer-capping.png)

1. Klikken **[!UICONTROL Next]** om alle beperkingen te bevestigen u bepaalde.

Als u bijvoorbeeld de volgende beperkingen instelt:

![](../assets/offer-constraints-example.png)

* Dit aanbod wordt alleen in overweging genomen voor gebruikers die voldoen aan de beslissingsregel &quot;Gold Loyalty Customers&quot;.
* De prioriteit van de aanbieding is vastgesteld op &quot;50&quot;, wat betekent dat de aanbieding wordt gepresenteerd vóór aanbiedingen met een prioriteit tussen 1 en 49 en na de aanbiedingen met een prioriteit van ten minste 51.
* Het voorstel wordt slechts eenmaal per maand per gebruiker op alle plaatsen gepresenteerd.

## Subsidiabiliteit {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="Geschiktheid definiëren"
>abstract="Standaard kan elk profiel in aanmerking komen voor presentatie van de aanbieding, maar u kunt segmenten of besluitvormingsregels gebruiken om de aanbieding te beperken tot specifieke profielen."

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="Geschiktheid voor aanbieding"
>abstract="In deze sectie kunt u besluitvormingsregels gebruiken om te bepalen welke gebruikers in aanmerking komen voor de aanbieding."
>additional-url="https://video.tv.adobe.com/v/329373" text="Demovideo bekijken"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="Totale profielschatting"
>abstract="Wanneer u segmenten of besluitvormingsregels selecteert, kunt u informatie over de geschatte gekwalificeerde profielen zien."

De **[!UICONTROL Offer eligibility]** kunt u de aanbieding beperken tot specifieke profielen die u het gebruiken van segmenten of besluitvormingsregels bepaalt.

>[!NOTE]
>
>Meer informatie over het gebruik van **segmenten** versus **beslissingsregels** in [deze sectie](#segments-vs-decision-rules).

* Standaard worden de **[!UICONTROL All visitors]** geselecteerd is, wat betekent dat elk profiel in aanmerking komt voor de presentatie van de aanbieding.

   ![](../assets/offer-eligibility-default.png)

* U kunt ook de presentatie van het voorstel beperken tot de leden van een of meerdere [Adobe Experience Platform-segmenten](../../segment/about-segments.md).

   Om dit te doen, activeer **[!UICONTROL Visitors who fall into one or multiple segments]** voegt u vervolgens een of meerdere segmenten toe vanuit het linkervenster en combineert u deze met de optie **[!UICONTROL And]** / **[!UICONTROL Or]** logische operatoren.

   ![](../assets/offer-eligibility-segment.png)

* Als u een specifieke koppeling wilt maken [beslissingsregel](../offer-library/creating-decision-rules.md) aan de aanbieding, selecteer **[!UICONTROL By defined decision rule]** en sleep de gewenste lijn van het linkerdeelvenster naar het deelvenster **[!UICONTROL Decision rule]** gebied.

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >Aanbiedingen op basis van gebeurtenissen worden momenteel niet ondersteund in [!DNL Journey Optimizer]. Als u een beslissingsregel maakt op basis van een [event](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}, je kunt dit object niet gebruiken in een voorstel.

Wanneer u segmenten of besluitvormingsregels selecteert, kunt u informatie over de geschatte gekwalificeerde profielen zien. Klikken **[!UICONTROL Refresh]** om gegevens bij te werken.

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>Profielramingen zijn niet beschikbaar wanneer regelparameters gegevens bevatten die niet in het profiel staan, zoals contextgegevens. Bijvoorbeeld, een toelatingsregel die het huidige weer om 80 graden vereist te zijn.

### Segmenten en beslissingsregels gebruiken {#segments-vs-decision-rules}

Als u een beperking wilt toepassen, kunt u de selectie van aanbiedingen beperken tot de leden van een of meerdere **Adobe Experience Platform-segmenten** of u kunt een **beslissingsregel**, beide oplossingen voor verschillende toepassingen.

In feite, is de output van een segment een lijst van profielen, terwijl een besluitvormingsregel een functie is die op bestelling tegen één enkel profiel tijdens het besluitvormingsproces wordt uitgevoerd. Het verschil tussen deze twee toepassingen wordt hieronder nader toegelicht.

* **Segmenten**

   Aan de ene kant zijn segmenten een groep Adobe Experience Platform-profielen die overeenkomen met een bepaalde logica op basis van profielkenmerken en gebeurtenissen ervaren. Het segment wordt echter niet opnieuw berekend door het Offertenbeheer, dat mogelijk niet up-to-date is wanneer de aanbieding wordt gepresenteerd.

   Meer informatie over segmenten in [deze sectie](../../segment/about-segments.md).

* **Beslissingsregels**

   Anderzijds is een beslissingsregel gebaseerd op in Adobe Experience Platform beschikbare gegevens en bepaalt aan wie een aanbieding kan worden getoond. Zodra geselecteerd in een aanbieding of een besluit voor een bepaalde plaatsing, wordt de regel uitgevoerd telkens als een besluit wordt genomen, die ervoor zorgt dat elk profiel de recentste en beste aanbieding krijgt.

   Meer informatie over beslissingsregels vindt u in [deze sectie](creating-decision-rules.md).

## Afbeelding {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="Over aanbiedingen beperken"
>abstract="In dit veld kunt u opgeven hoe vaak het voorstel kan worden weergegeven."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="Afbeelding gebruiken"
>abstract="Als u wilt voorkomen dat uw klanten te veel vragen, gebruikt u de optie Afdekken om het maximumaantal keren te bepalen dat een aanbieding kan worden gepresenteerd."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints.html#capping-change-date" text="Het wijzigen van datums kan invloed hebben op de plafondfunctie"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="De frequentie voor uitlijnen instellen"
>abstract="U kunt ervoor kiezen om de teller van de aanbiedingstafbeelding dagelijks, wekelijks of maandelijks opnieuw in te stellen. Als je je voorstel hebt opgeslagen, kun je de geselecteerde frequentie niet meer wijzigen."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping_impression"
>title="Impressie"
>abstract="Het gebruik van indrukkingen als afdekkende gebeurtenissen is alleen beschikbaar voor binnenkomende kanalen."

Afkappen wordt gebruikt als beperking om het maximumaantal keren te bepalen dat een aanbieding kan worden voorgesteld.

Door het aantal keren dat gebruikers specifieke aanbiedingen krijgen te beperken, kunt u voorkomen dat uw klanten te veel vragen en zo elk aanraakpunt optimaliseren met de beste aanbieding.

Volg de onderstaande hoofdstappen om de uitlijning in te stellen.

1. Zorg ervoor dat de **[!UICONTROL Include capping]** schakelknop is geselecteerd. Standaard wordt bijschriften opgenomen.

   >[!CAUTION]
   >
   >Het is niet mogelijk om frequentie het in- en uitschakelen voor eerder gemaakte aanbiedingen uit te schakelen. Hiervoor moet u het voorstel dupliceren of een nieuw voorstel maken.

1. Definiëren welke **[!UICONTROL Capping event]** zal in aanmerking worden genomen om de teller te verhogen. [Meer informatie](#capping-event)

1. Bepaal het aantal keren dat de aanbieding kan worden gepresenteerd. [Meer informatie](#capping-type)

1. Stel de **[!UICONTROL Frequency]** om te bepalen hoe vaak de aftaptelling wordt teruggesteld. [Meer informatie](#frequency-capping)

1. Als u meerdere [representaties](add-representations.md) voor je voorstel, geef aan of je de aftopping wilt toepassen **[!UICONTROL Across all placements]** of **[!UICONTROL For each placement]**. [Meer informatie](#placements)

1. Als de aanbieding eenmaal is opgeslagen en goedgekeurd en deze het aantal keren heeft weergegeven dat u in dit veld hebt opgegeven op basis van de criteria en het tijdpad dat u hebt gedefinieerd, wordt de levering gestopt.

Het aantal keren dat een aanbieding wordt voorgesteld, wordt berekend tijdens de voorbereiding van e-mail. Als u bijvoorbeeld een e-mail met een aantal voorstellen voorbereidt, tellen deze nummers mee voor de maximale limiet, ongeacht of de e-mail is verzonden of niet.

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>Afdekkingstellers worden opnieuw ingesteld wanneer de aanbieding vervalt of 2 jaar na de startdatum van de aanbieding, afhankelijk van welke datum het eerst valt. Meer informatie over het definiëren van de datum van een aanbieding in [deze sectie](creating-personalized-offers.md#create-offer).

### gebeurtenis Capping {#capping-event}

De **[!UICONTROL Capping event]** in het veld kunt u bepalen welke **[!UICONTROL Capping event]** zal in aanmerking worden genomen om de teller te verhogen:

* **[!UICONTROL Decision event]** (standaardwaarde): Er kan maximaal een aantal malen een voorstel worden aangeboden.
* **[!UICONTROL Impression]**: Het maximale aantal keer dat de aanbieding aan een gebruiker kan worden weergegeven.

   >[!NOTE]
   >
   >Het gebruik van indrukkingen als afdekkende gebeurtenissen is beschikbaar voor **binnenkomende kanalen** alleen.

* **[!UICONTROL Clicks]**: Een gebruiker kan op het aanbod klikken om het maximumaantal keren te wijzigen.
* **[!UICONTROL Custom event]**: U kunt een aangepaste gebeurtenis definiëren die wordt gebruikt om het aantal verzonden aanbiedingen te beperken. U kunt bijvoorbeeld het aantal aflossingen beperken tot een bepaald profiel één keer is afgelost. Gebruik hiervoor [Adobe Experience Platform XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"} schema&#39;s om een regel van de douanegebeurtenis te bouwen.

   ![](../assets/offer-capping-event.png)

   <!--For example, you can cap on the number of redemptions so that the offer can be shown until redemptions equal 10000. You can only select XDM ExperienceEvents. In the example below, you can cap on the number of subscriptions.-->

   <!--![](../assets/offer-capping-custom-event.png)-->

   >[!CAUTION]
   >
   >Voor alle begrenzingsgebeurtenissen behalve beslissingsgebeurtenis, kan de terugkoppeling van het besluitvormingsbeheer niet automatisch worden verzameld, zodat wordt gewaarborgd dat de gegevens binnen komen. [Meer informatie over gegevensverzameling](../data-collection/data-collection.md)

### Type uitlijnen {#capping-type}

De **[!UICONTROL Capping type]** kunt u het aantal keren opgeven dat de aanbieding kan worden weergegeven.

![](../assets/offer-capping-times.png)

>[!NOTE]
>
>Het getal moet een geheel getal groter dan 0 zijn.

<!--For example, if you defined a custom capping event such as subsciptions are taken into account, if you enter 10 in the **[!UICONTROL Capping count]** field, no more offers will be sent after 10 subscriptions.-->

<!--![](../assets/offer-capping-custom-example.png)-->

U kunt ook opgeven of u de aftopping wilt toepassen op alle gebruikers of op één specifiek profiel:

![](../assets/offer-capping-total.png)

* Selecteren **[!UICONTROL In total]** om te bepalen hoe vaak een aanbieding over het gecombineerde doelpubliek kan worden voorgesteld, betekenend over alle gebruikers.

   Als u bijvoorbeeld een elektronicawinkel bent met een &#39;tv-huis-deal&#39;, wilt u dat het aanbod slechts 200 keer wordt geretourneerd voor alle profielen.

* Selecteren **[!UICONTROL Per profile]** om te bepalen hoe vaak een aanbieding aan dezelfde gebruiker kan worden voorgesteld.

   Als je bijvoorbeeld een bank bent met een &#39;Platinum credit card&#39;-aanbieding, wil je niet dat dit voorstel meer dan vijf keer per profiel wordt weergegeven. U bent namelijk van mening dat als de gebruiker het aanbod vijf keer heeft gezien en er niet op heeft gereageerd, hij een grotere kans heeft om op het volgende beste aanbod in te gaan.

### Frequentiecorrectie {#frequency-capping}

De **[!UICONTROL Frequency]** kunt u definiëren hoe vaak het aantal bijschriften wordt teruggezet. Hiertoe definieert u de tijdsperiode voor het tellen (dagelijks, wekelijks of maandelijks) en voert u het aantal dagen/weken/maanden van uw keuze in.

![](../assets/offer-capping-frequency.png)

>[!NOTE]
>
>De reset vindt plaats om 12.00 uur UTC, op de dag die u hebt gedefinieerd of op de eerste dag van de week/maand, indien van toepassing. De startdag van de week is zondag. De duur die u kiest, mag niet langer zijn dan twee jaar (d.w.z. het overeenkomstige aantal maanden, weken of dagen).

Als u bijvoorbeeld wilt dat het aantal bijschriften elke twee weken opnieuw wordt ingesteld, selecteert u **[!UICONTROL Weekly]** van de **[!UICONTROL Repeat]** vervolgkeuzelijst en type **2** in het andere veld. De reset vindt om de zondag plaats om 23.00 uur UTC.

>[!CAUTION]
>
>Nadat je je voorstel hebt opgeslagen, kun je de tijdsperiode (maandelijks, wekelijks of dagelijks) die je voor de frequentie hebt geselecteerd, niet meer wijzigen.

### Plakken en plaatsen {#placements}

Als u meerdere [representaties](add-representations.md) voor je voorstel, geef aan of je de aftopping wilt toepassen **[!UICONTROL Across all placements]** of **[!UICONTROL For each placement]**.

![](../assets/offer-capping-placement.png)

* **[!UICONTROL Across all placements]**: het beperken van aantallen zal alle besluiten over de plaatsen verbonden aan de aanbieding in totaal nemen.

   Als een aanbieding bijvoorbeeld een **E-mail** plaatsing en **Web** plaatsing, en u plaatst het maximum bij **2 per profiel voor alle plaatsen** Vervolgens kan elk profiel het aanbod in totaal maximaal twee keer ontvangen, ongeacht de plaatsingsmix.

* **[!UICONTROL For each placement]**: Bij het beperken van tellingen worden de beslissingsaantallen voor elke plaatsing afzonderlijk toegepast.

   Als een aanbieding bijvoorbeeld een **E-mail** plaatsing en **Web** plaatsing, en u plaatst het maximum bij **2 per profiel voor elke plaatsing** Vervolgens kan elk profiel tot twee keer de aanbieding voor e-mailplaatsing ontvangen en nog eens twee keer de plaatsing op het web.

### Gevolgen van het wijzigen van datums voor plafonnering {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="Het wijzigen van datums kan invloed hebben op de plafondfunctie"
>abstract="Als er op deze aanbieding een maximumlimiet wordt toegepast, kan dit gevolgen hebben wanneer u de begin- of einddatum wijzigt."

U moet voorzichtig te werk gaan wanneer u de datum van een aanbieding wijzigt, omdat dit van invloed kan zijn op de aftopping als aan de volgende voorwaarden wordt voldaan:

* De aanbieding is [goedgekeurd](#review).
* [Afbeelding](#capping) wordt al toegepast op het voorstel.
* Afdekkingen worden gedefinieerd per profiel.

>[!NOTE]
>
>Meer informatie over het definiëren van de datum van een aanbieding in [deze sectie](creating-personalized-offers.md#create-offer).

Als u per profiel vastlegt, worden de geknipte aantallen op elk profiel opgeslagen. Wanneer u de begin- en einddatum van een goedgekeurd aanbod wijzigt, kan het aantal aftopping voor sommige profielen worden aangepast aan de verschillende hieronder beschreven scenario&#39;s.

![](../assets/offer-capping-change-date.png)

Hier zijn de mogelijke scenario&#39;s wanneer **de begindatum van een aanbieding wijzigen**:

| Scenario:<br>Indien... | Wat gebeurt er?<br>dan... | Mogelijke invloed op het maximumaantal |
|--- |--- |--- |
| ... de aanvangsdatum van de aanbieding wordt bijgewerkt voordat de oorspronkelijke startdatum van de aanbieding is ingegaan; | ... het maximumaantal begint op de nieuwe begindatum. | Nee |
| ... de nieuwe begindatum valt vóór de huidige einddatum; | ... de begrenzing wordt voortgezet met een nieuwe begindatum en het vorige maximumaantal voor elk profiel wordt voortgezet. | Nee |
| ... de nieuwe begindatum valt na de huidige einddatum; | ... de huidige plafonnering verloopt en het nieuwe maximumaantal begint opnieuw bij 0 voor alle profielen op de nieuwe begindatum. | Ja |

Hier zijn de mogelijke scenario&#39;s wanneer **verlenging van de uiterste datum voor de aanbieding**:

| Scenario:<br>Indien... | Wat gebeurt er?<br>dan... | Mogelijke invloed op het maximumaantal |
|--- |--- |--- |
| ... een beslissingsverzoek wordt ingediend vóór de oorspronkelijke einddatum van de aanbieding; | ... het maximumaantal wordt bijgewerkt en het vorige maximumaantal voor elk profiel wordt voortgezet. | Nee |
| ... geen verzoek om een beslissing wordt ingediend vóór de oorspronkelijke einddatum; | ... het maximumaantal wordt opnieuw ingesteld op de oorspronkelijke einddatum voor elk profiel. Het nieuwe maximum aantal zal dan opnieuw van 0 voor om het even welke nieuwe beslissingsverzoeken beginnen die na de originele einddatum zullen voorkomen. | Ja |

**Voorbeeld**

Stel dat je een voorstel hebt met een oorspronkelijke begindatum ingesteld op **1 januari**, verloopt op **31 januari**.

1. De profielen X, Y en Z worden voorgesteld.
1. Aan **10 januari**, wordt de einddatum van de aanbieding gewijzigd in **15 februari**.
1. **11 januari tot en met 31 januari** alleen profiel Z wordt aangeboden.

   * Omdat een beslissingsverzoek vóór de oorspronkelijke einddatum is ingediend **voor profiel Z** kan de uiterste datum van de aanbieding worden verlengd tot **15 februari**.
   * Aangezien er echter geen activiteit heeft plaatsgevonden vóór de oorspronkelijke einddatum voor **profielen X en Y**, zullen hun tellers verlopen en hun het maximum beperken tellingen aan 0 op **31 januari**.

![](../assets/offer-capping-change-date-ex.png)
