---
title: Persoonlijke aanbiedingen maken
description: Leer hoe je persoonlijke aanbiedingen kunt maken in Adobe Experience Platform.
feature: Aanbiedingen
topic: Integraties
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 1%

---

# Persoonlijke aanbiedingen maken {#creating-personalized-offers}

Voordat u een aanbieding maakt, moet u controleren of u het volgende hebt gemaakt:

* A **placement** waarin de aanbieding zal worden getoond. Zie [Plaatsen maken](../offer-library/creating-placements.md)
* Een **beslissingsregel** die de voorwaarde bepaalt waaronder de aanbieding zal worden ingediend. Zie [Beslissingsregels maken](../offer-library/creating-decision-rules.md).
* Een of meer **tags** die u aan de aanbieding wilt koppelen. Zie [Codes maken](../offer-library/creating-tags.md).

➡️ [Ontdek deze functie in video](#video)

De lijst met gepersonaliseerde aanbiedingen is toegankelijk in het menu **[!UICONTROL Offers]**.

![](../../assets/offers_list.png)

## De aanbieding maken {#create-offer}

Ga als volgt te werk om een **aanbieding** te maken:

1. Klik **[!UICONTROL Create offer]**, dan selecteer **[!UICONTROL Personalized offer]**.

   ![](../../assets/create_offer.png)

1. Geef de naam van de aanbieding en de begin- en einddatum en -tijd op. U kunt ook een of meerdere bestaande tags aan de aanbieding koppelen, zodat u de bibliotheek met aanbiedingen eenvoudiger kunt doorzoeken en organiseren.

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >Met de sectie **[!UICONTROL Offer attributes]** kunt u sleutelwaardeparen aan de aanbieding koppelen voor rapportage- en analysedoeleinden.

## De representaties van de aanbieding configureren {#representations}

1. Voeg een of meerdere representaties voor uw aanbieding toe met de knop **[!UICONTROL Add representation]**.

   >[!NOTE]
   >
   >Een aanbieding kan op verschillende plaatsen in een bericht worden getoond: in een bovenste banner met een afbeelding, als tekst in een alinea, als een HTML-blok, enz. Hoe meer vertegenwoordigingen een aanbieding heeft, des te meer mogelijkheden er zijn om het aanbod in verschillende plaatsingscontexten te gebruiken.

1. Geef voor elke representatie de **[!UICONTROL Channel]** en de **[!UICONTROL Placement]** op waar de aanbieding wordt weergegeven.

   ![](../../assets/channel-placement.png)

   Met de knop **[!UICONTROL Browse]** kunt u beschikbare plaatsen filteren en filteren op basis van hun kanaal en/of inhoudstype.

   ![](../../assets/browse-placements.png)

1. Voeg inhoud toe aan elke representatie die afkomstig is uit de Adobe Experience Cloud Assets-bibliotheek of van een externe openbare locatie.

   * Als u inhoud uit de Adobe Experience Cloud Assets-bibliotheek wilt toevoegen, sleept u deze vanuit het linkerdeelvenster naar het weergavegebied en geeft u vervolgens de URL op die u aan de inhoud wilt koppelen in het veld **[!UICONTROL Destination link]**.

      >[!NOTE]
      >
      >Inhoud kan alleen worden gesleept en verwijderd uit de elementkiezer in het linkerdeelvenster. Alleen inhoud die overeenkomt met het inhoudstype van de plaatsing is beschikbaar voor gebruik.

      ![](../../assets/offer_drag_content.png)

   * Als u inhoud van een externe openbare locatie wilt toevoegen, klikt u op de knop **[!UICONTROL Add content]** en geeft u vervolgens de naam, de URL en de koppeling Doel op van de inhoud die u wilt toevoegen.

      Zorg ervoor dat de inhoud die u toevoegt, overeenkomt met het inhoudstype van de geselecteerde plaatsing.

      ![](../../assets/offer_add_content.png)

   * U kunt ook teksttype-inhoud invoegen. Om dit te doen, klik **[!UICONTROL Add content]** knoop, dan selecteer **[!UICONTROL Custom text]** optie. Typ in het veld **[!UICONTROL Text]** de tekst die in de aanbieding wordt weergegeven.

      >[!NOTE]
      >
      >Deze optie is niet beschikbaar voor afbeeldingstypeplaatsingen.

      ![](../../assets/offer_text_content.png)

## Subsidiabiliteitsregels en beperkingen toevoegen {#eligibility}

Met de regels en beperkingen voor geschiktheid kunt u bepalen onder welke voorwaarden een aanbieding wordt weergegeven.

1. Configureer **[!UICONTROL Offer eligibility]**. Standaard is de optie **[!UICONTROL All visitors]** voor de beslissingsregel geselecteerd. Dit houdt in dat elk profiel in aanmerking komt voor presentatie van de aanbieding.

   U kunt de presentatie van het voorstel beperken tot de leden van een of meerdere Adobe Experience Platform-segmenten. Hiervoor activeert u de optie **[!UICONTROL Visitors who fall into one or multiple segments]**, voegt u een of meerdere segmenten uit het linkervenster toe en combineert u deze met de logische operatoren **[!UICONTROL And]** / **[!UICONTROL Or]**.

   Raadpleeg [deze pagina](../../segment/about-segments.md) voor meer informatie over het werken met segmenten.

   ![](../../assets/offer-eligibility-segment.png)

   Als u een specifieke besluitregel aan de aanbieding wilt associëren, uitgezochte **[!UICONTROL By defined decision rule]**, dan sleep de gewenste regel van de linkerruit in **[!UICONTROL Decision rule]** gebied. Voor meer op hoe te om een besluitregel tot stand te brengen, verwijs naar [deze sectie](../offer-library/creating-decision-rules.md).

   ![](../../assets/offer_rule.png)

1. Definieer **[!UICONTROL Priority]** van de aanbieding in vergelijking met andere als de gebruiker voor meer dan één aanbieding in aanmerking komt. Hoe hoger de prioriteit van een aanbieding is, hoe hoger de prioriteit ervan wordt vergeleken met andere aanbiedingen.

1. Geef de **[!UICONTROL Capping]** van de aanbieding op. Dit houdt in dat het aantal keren dat de aanbieding in totaal voor alle gebruikers wordt weergegeven. Als de aanbieding door alle gebruikers is afgeleverd het aantal keren dat u in dit veld hebt opgegeven, wordt de levering gestopt.

   >[!NOTE]
   >
   >Het aantal keren dat een aanbieding wordt voorgesteld, wordt berekend tijdens de voorbereiding van e-mail. Als u bijvoorbeeld een e-mail met een aantal voorstellen voorbereidt, tellen deze nummers mee voor de maximale limiet, ongeacht of de e-mail is verzonden of niet.
   >
   >Als een e-maillevering wordt verwijderd of als de voorbereiding opnieuw wordt uitgevoerd voordat deze wordt verzonden, wordt de grenswaarde voor de aanbieding automatisch bijgewerkt.

   ![](../../assets/offer_capping.png)

   In het bovenstaande voorbeeld:

   * De prioriteit van de aanbieding is vastgesteld op &quot;50&quot;, wat betekent dat de aanbieding wordt gepresenteerd vóór aanbiedingen met een prioriteit tussen 1 en 49 en na de aanbiedingen met een prioriteit van ten minste 51.
   * Dit aanbod wordt alleen in overweging genomen voor gebruikers die voldoen aan de beslissingsregel &quot;Gold Loyalty Customers&quot;.
   * Het voorstel wordt slechts eenmaal per gebruiker weergegeven.

## Het voorstel bekijken {#review}

Zodra de toelatingsregels en de beperkingen zijn bepaald, toont een samenvatting van de aanbiedingseigenschappen. Als alles correct wordt gevormd en uw aanbieding klaar is om aan gebruikers te worden voorgesteld, klik **[!UICONTROL Finish]**, dan uitgezocht **[!UICONTROL Save and approve]**.

U kunt het voorstel ook opslaan als concept, zodat u het later kunt bewerken en goedkeuren.

![](../../assets/offer_review.png)

De aanbieding wordt in de lijst weergegeven met de status **[!UICONTROL Live]** of **[!UICONTROL Draft]**, afhankelijk van het feit of u de aanbieding hebt goedgekeurd of niet in de vorige stap.

Het is nu klaar om aan gebruikers te worden geleverd. U kunt het selecteren om zijn eigenschappen te tonen en het uit te geven of te onderdrukken.

![](../../assets/offer_created.png)

Zodra een aanbieding is gecreeerd, kunt u zijn naam in de lijst klikken om tot gedetailleerde informatie toegang te hebben, evenals alle veranderingen te controleren die aan het gebruikend **[!UICONTROL Change log]** tabel zijn aangebracht. [Meer informatie](../get-started/user-interface.md#monitoring-changes).

## Video over zelfstudie {#video}

>[!NOTE]
>
>Deze video is van toepassing op de Offer decisioning toepassingsservice die op Adobe Experience Platform is gebouwd. Het biedt echter algemene richtlijnen voor het gebruik van Aanbieding in de context van Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
