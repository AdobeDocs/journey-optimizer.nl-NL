---
title: Aanbiedingen op maat maken
description: Leer hoe je persoonlijke aanbiedingen kunt maken in Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: b08eb138bbdf9c8a594735824eeac3496a58daba
workflow-type: tm+mt
source-wordcount: '1348'
ht-degree: 1%

---

# Aanbiedingen op maat maken {#creating-personalized-offers}

Voordat u een aanbieding maakt, moet u controleren of u het volgende hebt gemaakt:

* A **plaatsing** waarin de aanbieding wordt weergegeven. Zie [Plaatsen maken](../offer-library/creating-placements.md)
* Als u een toelatingsvoorwaarde wilt toevoegen: a **beslissingsregel** daarin wordt bepaald onder welke voorwaarden de aanbieding zal worden ingediend . Zie [Beslissingsregels maken](../offer-library/creating-decision-rules.md).
* Eén of meerdere **tags** die u wellicht aan de aanbieding wilt koppelen. Zie [Tags maken](../offer-library/creating-tags.md).

➡️ [Ontdek deze functie in video](#video)

De lijst met gepersonaliseerde aanbiedingen is toegankelijk in het **[!UICONTROL Offers]** -menu.

![](../../assets/offers_list.png)

## De aanbieding maken {#create-offer}

Om een **aanbieden** Voer de volgende stappen uit:

1. Klikken **[!UICONTROL Create offer]** selecteert u vervolgens **[!UICONTROL Personalized offer]**.

   ![](../../assets/create_offer.png)

1. Geef de naam van de aanbieding en de begin- en einddatum en -tijd op. U kunt ook een of meerdere bestaande tags aan de aanbieding koppelen, zodat u de bibliotheek met aanbiedingen eenvoudiger kunt doorzoeken en organiseren.

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >De **[!UICONTROL Offer attributes]** kunt u sleutelwaardeparen aan de aanbieding koppelen voor rapportage- en analysedoeleinden.

## De representaties van de aanbieding configureren {#representations}

Een aanbieding kan op verschillende plaatsen in een bericht worden getoond: in een bovenste banner met een afbeelding, als tekst in een alinea, als een HTML-blok, enz. Hoe meer vertegenwoordigingen een aanbieding heeft, des te meer mogelijkheden er zijn om het aanbod in verschillende plaatsingscontexten te gebruiken.

Volg onderstaande stappen om een of meerdere vertegenwoordigingen aan uw aanbieding toe te voegen en deze te configureren.

1. Voor de eerste weergave selecteert u eerst de optie **[!UICONTROL Channel]** dat zal worden gebruikt.

   ![](../../assets/channel-placement.png)

   >[!NOTE]
   >
   >Alleen de beschikbare plaatsen voor het geselecteerde kanaal worden weergegeven in het dialoogvenster **[!UICONTROL Placement]** vervolgkeuzelijst.


1. Selecteer een plaatsing in de lijst.

   U kunt ook de knop naast de knop **[!UICONTROL Placement]** vervolgkeuzelijst om door alle plaatsen te bladeren.

   ![](../../assets/browse-button-placements.png)

   Daar kunt u de plaatsingen volgens hun kanaal en/of inhoudstype nog filtreren. Kies een plaatsing en klik op **[!UICONTROL Select]**.

   ![](../../assets/browse-placements.png)

1. Voeg inhoud toe aan uw representatie. Meer informatie over [deze sectie](#content).

1. Wanneer u inhoud zoals een afbeelding of URL toevoegt, kunt u een **[!UICONTROL Destination link]**: de gebruikers die op de aanbieding klikken, worden naar de bijbehorende pagina geleid.

   ![](../../assets/offer-destination-link.png)

1. Tot slot selecteer de taal van uw keus helpen identificeren en beheren wat aan vertoning aan de gebruikers te beheren.

1. Als u een andere representatie wilt toevoegen, gebruikt u de optie **[!UICONTROL Add representation]** en voeg zo veel vertegenwoordigingen toe als nodig is.

   ![](../../assets/offer-add-representation.png)

1. Nadat u al uw representaties hebt toegevoegd, selecteert u **[!UICONTROL Next]**.

## Inhoud definiëren voor uw weergaven {#content}

U kunt verschillende typen inhoud aan een representatie toevoegen.

>[!NOTE]
>
>Alleen inhoud die overeenkomt met het inhoudstype van de plaatsing is beschikbaar voor gebruik.

### Afbeeldingen toevoegen

Als de geselecteerde plaatsing van het afbeeldingstype is, kunt u inhoud toevoegen die afkomstig is van het **Adobe Experience Cloud Asset** bibliotheek, een gecentraliseerde opslagplaats voor door [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> Werken met [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=en){target=&quot;_blank&quot;}, moet u implementeren [!DNL Assets Essentials] voor uw organisatie en zorg ervoor dat de gebruikers een deel van zijn **Assets Essentials Consumer Users** of/en **Assets Essentials-gebruikers** Productprofielen. Meer informatie over [deze pagina](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

1. Kies de optie **[!UICONTROL Asset library]**.

1. Selecteer **[!UICONTROL Browse]**.

   ![](../../assets/offer-browse-asset-library.png)

1. Blader door de elementen om de gewenste afbeelding te selecteren

1. Klik op **[!UICONTROL Select]**.

   ![](../../assets/offer-select-asset.png)

### URL&#39;s toevoegen

Als u inhoud van een externe openbare locatie wilt toevoegen, selecteert u **[!UICONTROL URL]** Voer vervolgens het URL-adres in van de inhoud die u wilt toevoegen.

![](../../assets/offer-content-url.png)

### Aangepaste tekst toevoegen {#custom-text}

U kunt ook teksttype-inhoud invoegen wanneer u een compatibele plaatsing selecteert.

1. Selecteer **[!UICONTROL Custom]** en klik op **[!UICONTROL Add content]**.

   ![](../../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Deze optie is niet beschikbaar voor afbeeldingstypeplaatsingen.

1. Typ de tekst die in de aanbieding wordt weergegeven.

   ![](../../assets/offer-text-content.png)

   U kunt de inhoud aanpassen met de Expressieeditor. Meer informatie over [personalisatie](../../personalization/personalize.md#use-expression-editor).

   ![](../../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Alleen de **[!UICONTROL Profile attributes]**, **[!UICONTROL Segment memberships]** en **[!UICONTROL Helper functions]** bronnen beschikbaar zijn voor het beheer van besluiten.

## Subsidiabiliteitsregels en beperkingen toevoegen {#eligibility}

Aan de hand van de regels en beperkingen op het gebied van geschiktheid kunt u bepalen onder welke voorwaarden een aanbieding wordt weergegeven.

1. Configureer de **[!UICONTROL Offer eligibility]**.

   * Standaard worden de **[!UICONTROL All visitors]** de optie voor de beslissingsregel is geselecteerd , hetgeen betekent dat elk profiel in aanmerking komt voor de indiening van het aanbod .

   * U kunt de presentatie van het voorstel beperken tot de leden van een of meerdere Adobe Experience Platform-segmenten. Om dit te doen, activeer **[!UICONTROL Visitors who fall into one or multiple segments]** voegt u vervolgens een of meerdere segmenten toe vanuit het linkervenster en combineert u deze met de optie **[!UICONTROL And]** / **[!UICONTROL Or]** logische operatoren.

      Raadpleeg voor meer informatie over het werken met segmenten [deze pagina](../../segment/about-segments.md).

      ![](../../assets/offer-eligibility-segment.png)

   * Als u een specifieke beslissingsregel aan de aanbieding wilt koppelen, selecteert u **[!UICONTROL By defined decision rule]** en sleep de gewenste lijn van het linkerdeelvenster naar het deelvenster **[!UICONTROL Decision rule]** gebied. Voor meer over hoe te om een besluitvormingsregel tot stand te brengen, verwijs naar [deze sectie](../offer-library/creating-decision-rules.md).

      ![](../../assets/offer_rule.png)

      >[!CAUTION]
      >
      >Aanbiedingen op basis van gebeurtenissen worden momenteel niet ondersteund in [!DNL Journey Optimizer]. Als u een beslissingsregel maakt op basis van een [event](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}, kunt u deze niet gebruiken in een aanbieding.
   Meer informatie over het gebruik van segmenten versus beslissingsregels in [deze sectie](../offer-activities/create-offer-activities.md#segments-vs-decision-rules).

1. Definieer de **[!UICONTROL Priority]** van de aanbieding in vergelijking met andere aanbiedingen indien de gebruiker voor meer dan één aanbieding in aanmerking komt. Hoe hoger de prioriteit van een aanbieding is, hoe hoger de prioriteit ervan wordt vergeleken met andere aanbiedingen.

1. Geef de aanbiedingen op **[!UICONTROL Capping]**, wat betekent dat het aantal keren dat het aanbod in totaal voor alle gebruikers wordt weergegeven. Als de aanbieding door alle gebruikers is afgeleverd het aantal keren dat u in dit veld hebt opgegeven, wordt de levering gestopt.

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

Zodra de toelatingsregels en de beperkingen zijn bepaald, toont een samenvatting van de aanbiedingseigenschappen.

1. Zorg ervoor alles behoorlijk wordt gevormd.

1. Wanneer uw voorstel klaar is om aan gebruikers te worden aangeboden, klikt u op **[!UICONTROL Finish]**.

1. Selecteer **[!UICONTROL Save and approve]**.

   ![](../../assets/offer_review.png)

   U kunt het voorstel ook opslaan als concept, zodat u het later kunt bewerken en goedkeuren.

De aanbieding wordt in de lijst weergegeven met de **[!UICONTROL Approved]** of **[!UICONTROL Draft]** status, afhankelijk van het feit of u het al dan niet in de vorige stap hebt goedgekeurd.

Het is nu klaar om aan gebruikers te worden geleverd.

![](../../assets/offer_created.png)

## Aanbiedingenlijst {#offer-list}

In de lijst met aanbiedingen kunt u de aanbieding selecteren om de eigenschappen ervan weer te geven. U kunt het ook bewerken, de status wijzigen (**Concept**, **Goedgekeurd**, **Gearchiveerd**), dupliceert de aanbieding of verwijdert deze.

![](../../assets/offer_created.png)

Selecteer **[!UICONTROL Edit]** om terug te gaan naar de modus Uitgave van aanbieding, waar u de [details](#create-offer), [representaties](#representations)en bewerkt u de [subsidiabiliteitsregels en beperkingen](#eligibility).

Selecteer een goedgekeurd voorstel en klik op **[!UICONTROL Undo approve]** om de status van de aanbieding weer in te stellen op **[!UICONTROL Draft]**.

De status opnieuw instellen op **[!UICONTROL Approved]** Selecteer de bijbehorende knop die nu wordt weergegeven.

![](../../assets/offer_approve.png)

De **[!UICONTROL More actions]** schakelt u de hieronder beschreven handelingen in.

![](../../assets/offer_more-actions.png)

* **[!UICONTROL Duplicate]**: een aanbod doet ontstaan met dezelfde eigenschappen, representaties, subsidiabiliteitsregels en beperkingen. Standaard bevat de nieuwe aanbieding de **[!UICONTROL Draft]** status.
* **[!UICONTROL Delete]**: Hiermee verwijdert u het voorstel uit de lijst.

   >[!CAUTION]
   >
   >Het aanbod en de inhoud ervan zijn niet meer toegankelijk. Deze handeling kan niet ongedaan worden gemaakt.
   >
   >Indien de aanbieding in een collectie of een beslissing wordt gebruikt, kan zij niet worden geschrapt. U moet het voorstel eerst uit om het even welke voorwerpen verwijderen.

* **[!UICONTROL Archive]**: stelt de aanbiedingsstatus in op **[!UICONTROL Archived]**. Het voorstel is nog steeds beschikbaar in de lijst, maar u kunt de status niet terugzetten op **[!UICONTROL Draft]** of **[!UICONTROL Approved]**. U kunt deze alleen dupliceren of verwijderen.

U kunt ook de status van meerdere aanbiedingen tegelijk verwijderen of wijzigen door de desbetreffende selectievakjes in te schakelen.

![](../../assets/offer_multiple-selection.png)

Als u de status van meerdere aanbiedingen met verschillende statussen wilt wijzigen, worden alleen de desbetreffende statussen gewijzigd.

![](../../assets/offer_change-status.png)

Nadat u een voorstel hebt gemaakt, kunt u in de lijst op de naam ervan klikken.

![](../../assets/offer_click-name.png)

Op deze manier hebt u toegang tot gedetailleerde informatie voor dat aanbod. Selecteer **[!UICONTROL Change log]** tab naar [alle wijzigingen controleren](../get-started/user-interface.md#monitoring-changes) die aan het aanbod zijn gedaan.

![](../../assets/offer_information.png)

## Video over zelfstudie {#video}

>[!NOTE]
>
>Deze video is van toepassing op de Offer decisioning toepassingsservice die op Adobe Experience Platform is gebouwd. Het biedt echter algemene richtlijnen voor het gebruik van Aanbieding in de context van Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
