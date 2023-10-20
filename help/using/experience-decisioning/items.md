---
title: Beslissingsitems
description: Meer informatie over hoe u met beslissingsobjecten kunt werken
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: f92e3882d3b5e515e672a4af8e787813d4d939ce
workflow-type: tm+mt
source-wordcount: '982'
ht-degree: 1%

---

# Beslissingsitems {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="Beslissingsitems beheren"
>abstract="Met Journey Optimizer kunt u marketingaanbiedingen maken, ook wel &#39;beslissingsitems&#39; genoemd, die u kunt maken en indelen in een gecentraliseerde catalogus en verzamelingen. Momenteel worden alle gemaakte beslissingsitems geconsolideerd in één catalogus met &quot;voorstellen&quot;. Vanuit dit scherm kunt u ook het schema van de catalogus openen met de opdracht **Schema bewerken** en maak aangepaste kenmerken voor uw beslissingsitems."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html" text="De itemcatalogus configureren"

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Aan de slag met Experience Decisition](gs-experience-decisioning.md)
* Je beslissingsobjecten beheren
   * [De itemcatalogus configureren](catalogs.md)
   * **[Beslissingsitems maken](items.md)**
   * [Objectverzamelingen beheren](collections.md)
* Selectie van items configureren
   * [Beslissingsregels maken](rules.md)
   * [Classificatiemethoden maken](ranking.md)
* [Selectiestrategieën maken](selection-strategies.md)
* [Beslissingsbeleid maken](create-decision.md)

>[!ENDSHADEBOX]

Met Journey Optimizer kunt u marketingaanbiedingen maken, ook wel &#39;beslissingsitems&#39; genoemd, die u kunt maken en indelen in een gecentraliseerde catalogus en verzamelingen. Ze bestaan uit standaard- en aangepaste kenmerken die precies op uw behoeften zijn afgestemd. Bovendien, nemen zij profielbeperkingen op die u toestaan om te bepalen aan wie een besluitpunt kan worden getoond.

Voordat u een beslissingsonderdeel maakt, moet u controleren of u een **beslissingsregel** als u voorwaarden wilt plaatsen om aan te bepalen aan wie het besluitpunt kan worden getoond. [Leer hoe u beslissingsregels](rules.md) maakt .

## Je eerste beslissingsobject maken

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="De prioriteit van het beslissingsitem definiëren"
>abstract="Als een profiel voor meerdere items in aanmerking komt, kan dit beslissingsitem met anderen worden vergeleken. Bij een hogere prioriteit krijgt de post voorrang boven andere."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="De aangepaste kenmerken definiëren"
>abstract="Aangepaste kenmerken zijn specifieke kenmerken die zijn toegesneden op uw behoeften en die u kunt toewijzen aan een beslissingsitem. Zij worden gecreeerd in het de catalogusschema van besluitvormingspunten. Deze sectie wordt alleen weergegeven als u ten minste één aangepast kenmerk aan het catalogusschema hebt toegevoegd."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html" text="De itemcatalogus configureren"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="Soorten publiek of beslissingsregels toevoegen"
>abstract="Standaard kunnen alle profielen in aanmerking komen voor het item voor een beslissing, maar u kunt het publiek of de regels gebruiken om het item te beperken tot specifieke profielen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html" text="Soorten publiek gebruiken"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/selection/rules.html" text="Beslissingsregels gebruiken"

Voer de volgende stappen uit om een beslissingsitem te maken:

1. Ga naar **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Items]**.

1. Definieer de standaardkenmerken van het beslissingsitem:

   1. Geef een naam en een beschrijving op.
   1. Begin- en einddatum opgeven. De beslissingsmotor zal het punt pas binnen deze data in overweging nemen.
   1. Stel de **[!UICONTROL Priority]** van de besluitvormingscomponent vergeleken met andere, als een profiel voor meerdere items in aanmerking komt. Bij een hogere prioriteit krijgt de post voorrang boven andere.

   ![](assets/item-attributes.png)

1. Aangepaste kenmerken zijn specifieke kenmerken die zijn toegesneden op uw behoeften en die u kunt toewijzen aan een beslissingsitem. Zij worden bepaald in het de catalogusschema van besluitvormingspunten. [Leer werken met catalogi](catalogs.md)

1. Wanneer de kenmerken van het beslissingsitem zijn gedefinieerd, klikt u op **[!UICONTROL Next]** om profielbeperkingen voor het item in te stellen.

   Standaard komen alle profielen in aanmerking om het beslissingsitem te ontvangen, maar u kunt het publiek of de regels gebruiken om het item te beperken tot specifieke profielen, beide oplossingen voor verschillende toepassingen. Vouw de onderstaande sectie uit voor meer informatie:

   +++Publiek gebruiken versus beslissende regels

   In feite is de uitvoer van een publiek een lijst met profielen, terwijl een beslissingsregel een functie is die op aanvraag tegen één profiel wordt uitgevoerd tijdens het besluitvormingsproces.

   * **Soorten publiek**: Enerzijds is het publiek een groep Adobe Experience Platform-profielen die overeenkomen met een bepaalde logica op basis van profielkenmerken en ervaringsgebeurtenissen. Aanbiedingsbeheer berekent het publiek echter niet opnieuw, wat mogelijk niet up-to-date is wanneer het voorstel wordt gepresenteerd.

   * **Besluitvormingsregels**: Anderzijds is een beslissingsregel gebaseerd op in Adobe Experience Platform beschikbare gegevens en bepaalt aan wie een aanbieding kan worden getoond. Zodra geselecteerd in een aanbieding of een besluit voor een bepaalde plaatsing, wordt de regel uitgevoerd telkens als een besluit wordt genomen, die ervoor zorgt dat elk profiel de recentste en beste aanbieding krijgt.

+++

   ![](assets/item-constraints.png)

   * Als u de presentatie van het besluititem wilt beperken tot de leden van een of meer Adobe Experience Platform-doelgroepen, selecteert u de optie **[!UICONTROL Visitors who fall into one or multiple audiences]** voegt u vervolgens een of meer soorten publiek toe vanuit het linkervenster en combineert u deze via het **[!UICONTROL And]** / **[!UICONTROL Or]** logische operatoren. [Meer informatie over publiek](../audience/about-audiences.md).

   * Als u een specifieke beslissingsregel wilt koppelen aan het beslissingsitem, selecteert u **[!UICONTROL By rule]** Sleep vervolgens de gewenste lijn van het linkerdeelvenster naar het centrale gebied. [Meer informatie over beslissingsregels](rules.md).

   Wanneer u publiek of beslissingsregels selecteert, kunt u informatie over de geschatte gekwalificeerde profielen zien. Klikken **[!UICONTROL Refresh]** gegevens bijwerken.

   >[!NOTE]
   >
   >Profielramingen zijn niet beschikbaar wanneer regelparameters gegevens bevatten die niet in het profiel staan, zoals contextgegevens. Bijvoorbeeld, een toelatingsregel die het huidige weer om 80 graden vereist te zijn.

1. Zodra de beperkingen van het besluitpunt worden bepaald, klik **[!UICONTROL Next]** om het item te bekijken en op te slaan.

1. Het beslissingsitem wordt nu in de lijst weergegeven, met de opdracht **[!UICONTROL Draft]** status. Wanneer het klaar is om aan profielen te worden getoond, klik de ellipknoop en selecteer **[!UICONTROL Approve]**.

   ![](assets/item-approve.png)

## Beslissingsitems beheren

Vanuit de lijst met beslissingsitems kunt u een beslissingsitem bewerken, de status ervan wijzigen (**Concept**, **Goedgekeurd**, **Gearchiveerd**), dupliceren of verwijderen.

Als u een beslissingsonderdeel wilt wijzigen, opent u het, brengt u de wijzigingen aan en slaat u het op.

Als u een beslissingsitem selecteert of op de knop Ovaal klikt, worden de hieronder beschreven handelingen ingeschakeld.

* **[!UICONTROL Approve]**: Stelt de status van het beslissingsitem in op Goedgekeurd.
* **[!UICONTROL Undo approve]**: Stelt de status van het beslissingsitem weer in op **[!UICONTROL Draft]**.
* **[!UICONTROL Duplicate]**: Maakt een beslissingsitem met identieke kenmerken en beperkingen. Standaard bevat het nieuwe item het **[!UICONTROL Draft]** status.
* **[!UICONTROL Delete]**: Hiermee wordt het beslissingsitem uit de lijst verwijderd.

  >[!IMPORTANT]
  >
  >Nadat de beslissing is verwijderd, zijn het item en de inhoud ervan niet meer toegankelijk. Deze handeling kan niet ongedaan worden gemaakt. Als het beslissingselement wordt gebruikt in een collectie of een beslissing, kan het niet worden verwijderd. U moet het beslissingsitem eerst uit een willekeurig object verwijderen.

* **[!UICONTROL Archive]**: Hiermee wordt de status van het beslissingstitem ingesteld op **[!UICONTROL Archived]**. Het beslissingsitem is nog steeds beschikbaar in de lijst, maar u kunt de status niet terugzetten op **[!UICONTROL Draft]** of **[!UICONTROL Approved]**. U kunt deze alleen dupliceren of verwijderen.
