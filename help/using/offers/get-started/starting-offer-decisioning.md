---
title: Aan de slag met Beslissingsbeheer
description: Ontdek hoe Adobe Journey Optimizer u kan helpen uw klanten het juiste aanbod op het juiste moment te sturen
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 46%

---

# Over Besluitbeheer {#about-decision-management}

Gebruiken [!DNL Journey Optimizer] om uw klanten de beste aanbieding en ervaring op alle aanraakpunten op het juiste moment te bieden. Als u ze eenmaal hebt ontworpen, richt u zich op uw publiek met persoonlijke aanbiedingen.

Beslissingsbeheer maakt personalisatie gemakkelijk met een centrale bibliotheek van marketing aanbiedingen en een besluitvormingsmotor die regels en beperkingen op rijke, real-time profielen toepast die door Adobe Experience Platform worden gecreeerd om u te helpen uw klanten het juiste aanbod op het juiste ogenblik verzenden.

De beslissingsmanagementcapaciteit bestaat uit twee hoofdcomponenten:

* De **Gecentraliseerde aanbiedingsbibliotheek** Dit is de interface waar u de verschillende elementen creeert en beheert die uw aanbiedingen vormen, en hun regels en beperkingen bepalen.
* De **Beslissingsengine voorstellen** die gebruikmaakt van Adobe Experience Platform-gegevens en realtime klantprofielen, samen met de aanbiedingsbibliotheek, om de juiste tijd, klanten en kanalen te selecteren waaraan de aanbiedingen worden geleverd.

![](../assets/architecture.png)

Voordelen zijn:

* Verbeterde campagneprestatie door persoonlijke aanbiedingen op meerdere kanalen te leveren,
* Verbeterde workflows: in plaats van meerdere verzendingen of campagnes te maken kunnen marketingteams de workflows verbeteren door één verzending te maken en de aanbiedingen in verschillende delen van de sjabloon te variëren,
* De controle over het aantal keren dat een aanbieding wordt getoond aan campagnes en klanten.

➡️ [Meer informatie over het beheer van beslissingen vindt u in deze video&#39;s](#video)


>[!NOTE]
>
>Als u een [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target=&quot;_blank&quot;} gebruiker gebruikt de **offer decisioning** alle functies voor Beslissingsbeheer die in deze sectie worden beschreven, zijn ook op u van toepassing.

## Aanbiedingen en beslissingen {#about-offers-and-decisions}

Een **Aanbieding** bestaat uit content, geschiktheidsregels en restricties die de voorwaarden bepalen waaronder deze aan uw klanten wordt gepresenteerd.

De aanbieding wordt gemaakt aan de hand van de **Aanbiedingsbibliotheek**, die een centrale aanbiedingscatalogus verstrekt waar u geschiktheidsregels en restricties kunt koppelen aan meerdere stukken content om aanbiedingen te maken en te publiceren (zie [Gebruikersinterface van de Aanbiedingsbibliotheek](../get-started/user-interface.md)).

![](../assets/offer_structure.png)

Zodra de Aanbiedingsbibliotheek is verrijkt met aanbiedingen, kunt u uw aanbiedingen integreren in **beslissingen**.

Besluiten zijn containers voor uw aanbiedingen die gebruikmaken van de Offertenbeslissingsengine om de beste aanbieding te kiezen, afhankelijk van het doel van de levering.

## Vaak voorkomende gebruiksscenario&#39;s {#common-use-cases}

Dankzij de mogelijkheden voor Beslissingsbeheer en de integratie met Adobe Experience Platform kunt u tal van gebruiksgevallen verwerken om u te helpen de betrokkenheid en conversie van klanten te vergroten.

* Geef op de startpagina van uw website de aanbiedingen weer die passen bij de belangstelling van de bezoekende klant, op basis van gegevens van Adobe Experience Platform.

   ![](../assets/website.png)

* Als klanten in de buurt van één van uw winkels lopen, stuur ze dan pushmeldingen om hen te herinneren aan beschikbare aanbiedingen op basis van hun kenmerken (loyaliteitsniveau, gender, eerdere aankopen...).

   ![](../assets/push_sample.png)

* Beslissingsbeheer helpt u ook de ervaring van uw klanten te verbeteren wanneer u contact opneemt met uw ondersteuningsteam. Het Beheer APIs van het besluit staat u toe om in uw portaalinformatie van de agenten van het vraagcentrum over de terugbetaalde klant en volgende beste aanbiedingen te tonen.

   ![](../../assets/do-not-localize/call-center.png)

## Toegang verlenen tot het beheer van besluiten {#granting-acess-to-decision-management}

Machtigingen voor toegang tot en gebruik van beslissingsmogelijkheden worden beheerd met behulp van de [Adobe Admin Console](https://helpx.adobe.com/nl/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

Om toegang tot de functionaliteit van het Beheer van het Besluit te verlenen, moet u tot een **[!UICONTROL Product profile]** en wijs de overeenkomstige toestemmingen aan uw gebruikers toe. Meer informatie over beheren [!DNL Journey Optimizer] gebruikers en machtigingen in [deze sectie](../../administration/permissions.md).

De machtigingen die specifiek zijn voor Beslissingsbeheer worden vermeld in [deze sectie](../../administration/high-low-permissions.md#decisions-permissions).

## Woordenlijst {#glossary}

U kunt onder de lijst van de belangrijkste concepten vinden u zult werken met wanneer het gebruiken van Beslissingsbeheer.

* **Limitering** of **Frequentiebeperking**: limitering (ofwel beperking) wordt gebruikt om een limiet in te stellen voor het aantal keren dat een aanbieding wordt ingezet. Er zijn twee soorten limieten: een limiet voor het aantal keren dat een aanbieding aan de gecombineerde doelgroep kan worden aangeboden, ook wel ‘totaallimiet’ genoemd, en een limiet voor het aantal keren dat een aanbieding aan dezelfde eindgebruiker kan worden aangeboden, ook wel ‘profiellimiet’ genoemd.

* **Verzamelingen**: verzamelingen zijn subsets van aanbiedingen die zijn gebaseerd op vooraf gedefinieerde voorwaarden die door een marketeer zijn gedefinieerd, zoals de categorie van de aanbieding.

* **Besluit**: Een beslissing bevat de logica die de selectie van een aanbieding informeert.

* **Beslissingsregel**: beslissingsregels zijn restricties die aan een persoonlijke aanbieding worden toegevoegd en op een profiel worden toegepast om te bepalen of dat profiel in aanmerking komt voor een aanbieding.

* **Geschikte aanbieding**: een geschikte aanbieding voldoet aan de restricties die op een hoger niveau zijn ingesteld zodat de aanbieding consistent aan een profiel kan worden aangeboden.

* **Beslissingsbeheer**: Staat u toe om eindgebruiker gepersonaliseerde aanbiedingservaringen over kanalen en toepassingen tot stand te brengen en te leveren gebruikend bedrijfslogica en besluitvormingsregels.

* **Alternatieve aanbiedingen**: een alternatieve aanbieding is de standaardaanbieding die wordt weergegeven wanneer een eindgebruiker niet in aanmerking komt voor een van de persoonlijke aanbiedingen in de verzameling.

* **Aanbieding**: een aanbieding is een marketingbericht waaraan regels gekoppeld kunnen zijn die bepalen wie in aanmerking komt om de aanbieding te zien.

* **Bibliotheek van aanbieding**: De aanbiedingsbibliotheek is een centrale bibliotheek die wordt gebruikt om gepersonaliseerde en terugvalaanbiedingen, besluitvormingsregels en besluiten te beheren.

* **Persoonlijke aanbiedingen**: een persoonlijke aanbieding is een aanpasbaar marketingbericht op basis van geschiktheidsregels en restricties.

* **Plaatsingen**: een plaatsing is de locatie en/of de context waarin een aanbieding voor een eindgebruiker wordt weergegeven.

* **Prioriteit**: prioriteiten worden gebruikt om aanbiedingen te rangschikken die voldoen aan alle restricties, zoals geschiktheid, kalender en beperking.

* **Weergaven**: een weergave is informatie (bijv. de locatie of taal) die door een kanaal wordt gebruikt om een aanbieding te tonen.

## Instructievideo&#39;s{#video}

>[!NOTE]
>
>Deze video&#39;s zijn van toepassing op de Offer Decisioning-toepassingsservice die op Adobe Experience Platform is gebouwd en zijn niet specifiek voor [!DNL Adobe Journey Optimizer]. Zij bieden echter algemene richtsnoeren voor het gebruik van Beslissingsbeheer in de context van [!DNL Journey Optimizer].

### Wat is het beheer van besluiten? {#what-is-offer-decisioning}

In de onderstaande video wordt een inleiding gegeven op de belangrijkste mogelijkheden, architectuur en gebruiksscenario&#39;s van het beheer van beslissingen:

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### Aanbiedingen definiëren en beheren {#use-offer-decisioning}

In de onderstaande video ziet u hoe u Beslissingsbeheer kunt gebruiken om uw aanbiedingen te definiëren en te beheren en real-time klantgegevens kunt gebruiken.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)


