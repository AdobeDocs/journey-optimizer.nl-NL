---
title: Beslissingsitems
description: Meer informatie over hoe u met beslissingsobjecten kunt werken
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Beperkte beschikbaarheid"
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '1684'
ht-degree: 0%

---

# Je eerste beslissingsobject maken {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="Beslissingsitems beheren"
>abstract="Met Journey Optimizer kunt u marketingaanbiedingen maken, ook wel &#39;beslissingsitems&#39; genoemd, die u kunt maken en indelen in een gecentraliseerde catalogus en verzamelingen. Momenteel worden alle gemaakte beslissingsitems geconsolideerd in één catalogus met &quot;voorstellen&quot;. Vanuit dit scherm kunt u ook het schema van de catalogus openen met de opdracht **Schema bewerken** en maak aangepaste kenmerken voor uw beslissingsitems."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html" text="De itemcatalogus configureren"

Met Journey Optimizer kunt u marketingaanbiedingen maken, ook wel &#39;beslissingsitems&#39; genoemd, die u kunt maken en indelen in een gecentraliseerde catalogus en verzamelingen. Ze bestaan uit standaard- en aangepaste kenmerken die precies op uw behoeften zijn afgestemd. Bovendien, nemen zij profielbeperkingen op die u toestaan om te bepalen aan wie een besluitpunt kan worden getoond.

Voordat u een beslissingsonderdeel maakt, moet u controleren of u een **beslissingsregel** als u voorwaarden wilt plaatsen om aan te bepalen aan wie het besluitpunt kan worden getoond. [Leer hoe u beslissingsregels maakt](rules.md).

Als u een beslissingsitem wilt maken, navigeert u naar **[!UICONTROL Experience Decisioning]** > **[!UICONTROL  Catalogs]** en klik vervolgens op **[!UICONTROL Create item]** Voer vervolgens de stappen uit die in de onderstaande secties worden beschreven.

## De kenmerken van het beslissingsitem definiëren {#attributes}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="De prioriteit van het beslissingsitem definiëren"
>abstract="Als een profiel voor meerdere items in aanmerking komt, kan dit beslissingsitem met anderen worden vergeleken. Bij een hogere prioriteit krijgt de post voorrang boven andere."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="De aangepaste kenmerken definiëren"
>abstract="Aangepaste kenmerken zijn specifieke kenmerken die zijn toegesneden op uw behoeften en die u kunt toewijzen aan een beslissingsitem. Zij worden gecreeerd in het de catalogusschema van besluitvormingspunten. Deze sectie wordt alleen weergegeven als u ten minste één aangepast kenmerk aan het catalogusschema hebt toegevoegd."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html" text="De itemcatalogus configureren"

Begin door de standaard en douanekenmerken van het besluitpunt te bepalen:

![](assets/item-attributes.png)

1. Geef een naam en een beschrijving op.
1. Begin- en einddatum opgeven. De beslissingsmotor zal het punt pas binnen deze data in overweging nemen.
1. Stel de **[!UICONTROL Priority]** van de besluitvormingscomponent vergeleken met andere, als een profiel voor meerdere items in aanmerking komt. Bij een hogere prioriteit krijgt de post voorrang boven andere.
1. De **Tags** staat u toe om de Verenigde Markeringen van Adobe Experience Platform aan uw besluitvormingspunten toe te wijzen. Op deze manier kunt u ze gemakkelijk classificeren en zoeken verbeteren. [Leer hoe u met tags kunt werken](../start/search-filter-categorize.md#tags)

   >[!NOTE]
   >
   >De prioriteit is een gegevenstype van gehele getallen. Alle attributen die geheelgegevenstypes zijn zouden geheelwaarden (geen decimalen) moeten bevatten.

1. Aangepaste kenmerken opgeven (optioneel). Aangepaste kenmerken zijn specifieke kenmerken die zijn toegesneden op uw behoeften en die u kunt toewijzen aan een beslissingsitem. Zij worden bepaald in het de catalogusschema van besluitvormingspunten. [Leer werken met catalogi](catalogs.md)

1. Wanneer de kenmerken van het beslissingsitem zijn gedefinieerd, klikt u op **[!UICONTROL Next]**.

## De geschiktheid van het beslissingsitem configureren {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="Soorten publiek of beslissingsregels toevoegen"
>abstract="Standaard kunnen alle profielen in aanmerking komen voor het item voor een beslissing, maar u kunt het publiek of de regels gebruiken om het item te beperken tot specifieke profielen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html" text="Soorten publiek gebruiken"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/selection/rules.html" text="Beslissingsregels gebruiken"

Standaard komen alle profielen in aanmerking om het beslissingsitem te ontvangen, maar u kunt het publiek of de regels gebruiken om het item te beperken tot specifieke profielen, beide oplossingen voor verschillende toepassingen. Vouw de onderstaande sectie uit voor meer informatie:

+++Publiek gebruiken versus beslissende regels

In feite is de uitvoer van een publiek een lijst met profielen, terwijl een beslissingsregel een functie is die op aanvraag tegen één profiel wordt uitgevoerd tijdens het besluitvormingsproces.

* **Soorten publiek**: Enerzijds is het publiek een groep Adobe Experience Platform-profielen die overeenkomen met een bepaalde logica op basis van profielkenmerken en ervaringsgebeurtenissen. Aanbiedingsbeheer berekent het publiek echter niet opnieuw, wat mogelijk niet up-to-date is wanneer het voorstel wordt gepresenteerd.

* **Besluitvormingsregels**: Anderzijds is een beslissingsregel gebaseerd op in Adobe Experience Platform beschikbare gegevens en bepaalt aan wie een aanbieding kan worden getoond. Zodra geselecteerd in een aanbieding of een besluit voor een bepaalde plaatsing, wordt de regel uitgevoerd telkens als een besluit wordt genomen, die ervoor zorgt dat elk profiel de recentste en beste aanbieding krijgt.

+++

* Als u de presentatie van het besluititem wilt beperken tot de leden van een of meer Adobe Experience Platform-doelgroepen, selecteert u de optie **[!UICONTROL Visitors who fall into one or multiple audiences]** voegt u vervolgens een of meer soorten publiek toe vanuit het linkervenster en combineert u deze via het **[!UICONTROL And]** / **[!UICONTROL Or]** logische operatoren. [Meer informatie over publiek](../audience/about-audiences.md).

* Als u een specifieke beslissingsregel wilt koppelen aan het beslissingsitem, selecteert u **[!UICONTROL By rule]** Sleep vervolgens de gewenste lijn van het linkerdeelvenster naar het centrale gebied. [Meer informatie over beslissingsregels](rules.md).

![](assets/item-constraints.png)

Wanneer u publiek of beslissingsregels selecteert, kunt u informatie over de geschatte gekwalificeerde profielen zien. Klikken **[!UICONTROL Refresh]** gegevens bijwerken.

>[!NOTE]
>
>Profielramingen zijn niet beschikbaar wanneer regelparameters gegevens bevatten die niet in het profiel staan, zoals contextgegevens. Bijvoorbeeld, een toelatingsregel die het huidige weer om 80 graden vereist te zijn.

## Lijnen voor uitlijnen instellen {#capping}

Afkappen wordt gebruikt als beperking om het maximumaantal keren te bepalen dat een aanbieding kan worden voorgesteld. Door het aantal keren dat gebruikers specifieke aanbiedingen krijgen te beperken, kunt u voorkomen dat uw klanten te veel vragen en zo elk aanraakpunt optimaliseren met de beste aanbieding. U kunt tot 10 titels voor een bepaald besluitpunt tot stand brengen.

![](assets/item-capping.png)

>[!NOTE]
>
>
>De waarde van de afluisterteller kan tot 3 seconden duren om bij te werken. Stel bijvoorbeeld dat u een webbanner weergeeft die een aanbieding op uw website weergeeft. Als een bepaalde gebruiker in minder dan 3 seconden naar de volgende pagina van uw website bladert, wordt de tellerwaarde niet voor die gebruiker verhoogd.

Als u uitlijningsregels wilt instellen voor het beslissingsitem, klikt u op de knop **[!UICONTROL Create capping]** Voer vervolgens de volgende stappen uit:

1. Definiëren welke **[!UICONTROL Capping event]** zal in aanmerking worden genomen om de teller te verhogen.

   * **[!UICONTROL Decision event]** (standaardwaarde): een aanbieding kan maximaal worden weergegeven.
   * **[!UICONTROL Impression]** (Alleen binnenkomende kanalen): het maximale aantal keren dat de aanbieding aan een gebruiker kan worden weergegeven.
   * **[!UICONTROL Clicks]**: Het maximum aantal keren dat een gebruiker op het beslissingsitem kan klikken.
   * **[!UICONTROL Custom event]**: U kunt een aangepaste gebeurtenis definiëren die wordt gebruikt om het aantal keren dat het item wordt verzonden, tot een maximum te beperken. U kunt bijvoorbeeld het aantal aflossingen beperken tot ze gelijk zijn aan 10000 of tot een bepaald profiel één keer is afgelost. Gebruik hiervoor [Adobe Experience Platform XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"} schema&#39;s om een regel van de douanegebeurtenis te bouwen.

   >[!NOTE]
   >
   >Voor alle begrenzingsgebeurtenissen behalve beslissingsgebeurtenis, kan de terugkoppeling van het beslissingsbeheer niet automatisch worden verzameld, wat ertoe kan leiden dat de afspeelteller niet correct wordt verhoogd. Om ervoor te zorgen dat elke begrenzingsgebeurtenis wordt bijgehouden en in de afluisterteller wordt rekenschap gegeven, zorg ervoor dat het schema dat wordt gebruikt om ervaringsgebeurtenissen te verzamelen de correcte gebiedsgroep voor die gebeurtenis omvat. Gedetailleerde informatie over gegevensverzameling is beschikbaar in de Journey Optimizer-documentatie voor besluitvormingsbeheer:
   >* [Verzameling van beslissingsbeheersgegevens](../offers/data-collection/data-collection.md)
   >* [Gegevensverzameling configureren](../offers/data-collection/schema-requirement.md)

1. Kies het type bijschrift:

   * Selecteren **[!UICONTROL In total]** om te bepalen hoe vaak het punt over het gecombineerde doelpubliek kan worden voorgesteld, betekenend over alle gebruikers. Als u bijvoorbeeld een elektronicawinkel bent met een &#39;tv-huis-deal&#39;, wilt u dat het aanbod slechts 200 keer wordt geretourneerd voor alle profielen.

* Selecteren **[!UICONTROL Per profile]** om te bepalen hoe vaak de aanbieding aan dezelfde gebruiker kan worden voorgesteld. Als je bijvoorbeeld een bank bent met een &#39;Platinum credit card&#39;-aanbieding, wil je niet dat dit voorstel meer dan vijf keer per profiel wordt weergegeven. U bent namelijk van mening dat als de gebruiker het aanbod vijf keer heeft gezien en er niet op heeft gereageerd, hij een grotere kans heeft om op het volgende beste aanbod in te gaan.

1. In de **[!UICONTROL Capping count limit]** in het veld het aantal keren opgeven dat de aanbieding aan alle gebruikers of per profiel kan worden weergegeven, afhankelijk van het geselecteerde type aftopping. Het getal moet een geheel getal groter dan 0 zijn.

   U hebt bijvoorbeeld een aangepaste gebeurtenis voor het toewijzen van plafonds gedefinieerd, waarmee rekening wordt gehouden, zoals het aantal uitcheckgebeurtenissen. Als u 10 in **[!UICONTROL Capping count limit]** , worden na 10 afboekingen geen voorstellen meer verzonden.

1. In de **[!UICONTROL Reset capping frequency]** vervolgkeuzelijst, stelt u de frequentie in waarmee de afluisterteller wordt teruggezet. Hiervoor definieert u de tijdsperiode voor het tellen (dagelijks, wekelijks of maandelijks) en voert u het aantal dagen/weken/maanden van uw keuze in. Als u bijvoorbeeld wilt dat het aantal bijschriften elke twee weken opnieuw wordt ingesteld, selecteert u **[!UICONTROL Weekly]** uit de bijbehorende vervolgkeuzelijst en type **2** in het andere veld.

   >[!NOTE]
   >
   >De teller voor het aftappen van de frequentie wordt opnieuw ingesteld bij **12 uur UTC**, op de door u bepaalde dag of op de eerste dag van de week/maand, indien van toepassing. De startdag van de week is **zondag**. De duur die u kiest, mag niet langer zijn dan **2 jaar** (d.w.z. het overeenkomstige aantal maanden, weken of dagen).
   >
   >Na publicatie van het beslissingsobject kunt u de tijdsperiode (maandelijks, wekelijks of dagelijks) die u voor de frequentie hebt geselecteerd, niet meer wijzigen. U kunt de frequentietoewijzing nog steeds bewerken als het item **[!UICONTROL Draft]** status en nooit eerder gepubliceerd met ingeschakelde frequentiecapping.

1. Klikken **[!UICONTROL Create]** om het maken van de aftapregel te bevestigen. U kunt tot 10 regels voor één enkel besluitpunt tot stand brengen. Klik hiertoe op de knop **[!UICONTROL Create capping]** en herhaalt u de bovenstaande stappen.

   ![](assets/item-capping-rules.png)

1. Als de regels voor het in aanmerking nemen en aftopping van het beslissingselement zijn gedefinieerd, klikt u op **[!UICONTROL Next]** om het item te bekijken en op te slaan.

1. Het beslissingsitem wordt nu in de lijst weergegeven, met de opdracht **[!UICONTROL Draft]** status. Wanneer het klaar is om aan profielen te worden getoond, klik de ellipknoop en selecteer **[!UICONTROL Approve]**.

   ![](assets/item-approve.png)

<!--* Identifying how many times a given customer has been shown a decision item. 
If a marketer wants to determine how many times a specific customer has been shown an offer, they can do that. Go to Profiles menu, Attributes tab. You’ll see all counter values. The alphanumeric string is associated to the offer. To make the map, go to an item, in the URL check the last alphanumeric strings. D stands for day, w stands for week, m for month. “Ce” custom event-->

## Beslissingsitems beheren {#manage}

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
