---
title: Aan de slag met Beslissingsbeheer
description: Aan de slag met Beslissingsbeheer. Meer informatie over de architectuur, aanbiedingen en beslissingen en over veelvoorkomende gebruiksgevallen die u kunt uitvoeren.
feature: Aanbiedingen
topic: Integraties
role: User
level: Beginner
source-git-commit: 22520570d96db43d39931149296b27a6211f7aa5
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 50%

---


# Over Besluitbeheer {#about-offer-decision}

Gebruik [!DNL Journey Optimizer] om uw klanten de beste aanbieding en ervaring op alle aanraakpunten op het juiste moment te bieden. Als u ze eenmaal hebt ontworpen, richt u zich op uw publiek met persoonlijke aanbiedingen.

De beslissingsmanagementcapaciteit bestaat uit twee hoofdcomponenten:

* De **Gecentraliseerde Bibliotheek van de Aanbieding** die de interface is waar u creeert en de verschillende elementen beheert die uw aanbiedingen samenstellen, en hun regels en beperkingen bepalen.
* De **beslissingsengine voor aanbiedingen** die gebruikmaakt van Adobe Experience Platform-gegevens en realtime klantprofielen, samen met de aanbiedingsbibliotheek, om de juiste tijd, klanten en kanalen te selecteren waaraan aanbiedingen worden geleverd.

![](../../assets/architecture.png)

Voordelen zijn:

* Verbeterde campagneprestatie door persoonlijke aanbiedingen op meerdere kanalen te leveren,
* Verbeterde workflows: in plaats van meerdere verzendingen of campagnes te maken kunnen marketingteams de workflows verbeteren door één verzending te maken en de aanbiedingen in verschillende delen van de sjabloon te variëren,
* De controle over het aantal keren dat een aanbieding wordt getoond aan campagnes en klanten.

➡️ [Bekijk deze zelfstudievideo&#39;s](#tutorial-videos) voor meer informatie over Beslissingsbeheer.

## Aanbiedingen en beslissingen {#offers-offer-activities}

Een **Aanbieding** bestaat uit content, geschiktheidsregels en restricties die de voorwaarden bepalen waaronder deze aan uw klanten wordt gepresenteerd.

De aanbieding wordt gemaakt aan de hand van de **Aanbiedingsbibliotheek**, die een centrale aanbiedingscatalogus verstrekt waar u geschiktheidsregels en restricties kunt koppelen aan meerdere stukken content om aanbiedingen te maken en te publiceren (zie [Gebruikersinterface van de Aanbiedingsbibliotheek](../get-started/user-interface.md)).

![](../../assets/offer_structure.png)

Nadat de bibliotheek met aanbiedingen is verrijkt, kunt u uw aanbiedingen integreren in **decisions** (voorheen bekend als &#39;aanbiedingsactiviteiten&#39;).

Besluiten zijn containers voor uw aanbiedingen die gebruikmaken van de Offertenbeslissingsengine om de beste aanbieding te kiezen, afhankelijk van het doel van de levering.

## Vaak voorkomende gebruiksscenario&#39;s

Dankzij de mogelijkheden voor Beslissingsbeheer en de integratie met Adobe Experience Platform kunt u tal van gebruiksgevallen verwerken om u te helpen de betrokkenheid en conversie van klanten te vergroten.

* Geef op de startpagina van uw website de aanbiedingen weer die passen bij de belangstelling van de bezoekende klant, op basis van gegevens van Adobe Experience Platform.

   ![](../../assets/website.png)

* Als klanten in de buurt van één van uw winkels lopen, stuur ze dan pushmeldingen om hen te herinneren aan beschikbare aanbiedingen op basis van hun kenmerken (loyaliteitsniveau, gender, eerdere aankopen...).

   ![](../../assets/push_sample.png)

* Beslissingsbeheer helpt u ook de ervaring van uw klanten te verbeteren wanneer u contact opneemt met uw ondersteuningsteam. Het Beheer APIs van het besluit staat u toe om in uw portaalinformatie van de agenten van het vraagcentrum over de terugbetaalde klant en volgende beste aanbiedingen te tonen.

   ![](../../assets/do-not-localize/call-center.png)


## Woordenlijst {#glossary}

U kunt onder de lijst van de belangrijkste concepten vinden u zult werken met wanneer het gebruiken van Beslissingsbeheer.

* **Limitering** of **Frequentiebeperking**: limitering (ofwel beperking) wordt gebruikt om een limiet in te stellen voor het aantal keren dat een aanbieding wordt ingezet. Er zijn twee soorten limieten: een limiet voor het aantal keren dat een aanbieding aan de gecombineerde doelgroep kan worden aangeboden, ook wel ‘totaallimiet’ genoemd, en een limiet voor het aantal keren dat een aanbieding aan dezelfde eindgebruiker kan worden aangeboden, ook wel ‘profiellimiet’ genoemd.

* **Verzamelingen**: verzamelingen zijn subsets van aanbiedingen die zijn gebaseerd op vooraf gedefinieerde voorwaarden die door een marketeer zijn gedefinieerd, zoals de categorie van de aanbieding.

* **Besluit**  (voorheen bekend als Aanbiedingsactiviteit): Een beslissing bevat de logica die de selectie van een aanbieding informeert.

* **Beslissingsregel**: beslissingsregels zijn restricties die aan een persoonlijke aanbieding worden toegevoegd en op een profiel worden toegepast om te bepalen of dat profiel in aanmerking komt voor een aanbieding.

* **Geschikte aanbieding**: een geschikte aanbieding voldoet aan de restricties die op een hoger niveau zijn ingesteld zodat de aanbieding consistent aan een profiel kan worden aangeboden.

* **Beslissingsbeheer**: Staat u toe om eindgebruiker gepersonaliseerde aanbiedingservaringen over kanalen en toepassingen tot stand te brengen en te leveren gebruikend bedrijfslogica en besluitvormingsregels.

* **Alternatieve aanbiedingen**: een alternatieve aanbieding is de standaardaanbieding die wordt weergegeven wanneer een eindgebruiker niet in aanmerking komt voor een van de persoonlijke aanbiedingen in de verzameling.

* **Aanbieding**: een aanbieding is een marketingbericht waaraan regels gekoppeld kunnen zijn die bepalen wie in aanmerking komt om de aanbieding te zien.

* **Bibliotheek** voorstel: De aanbiedingsbibliotheek is een centrale bibliotheek die wordt gebruikt om gepersonaliseerde en terugvalaanbiedingen, besluitvormingsregels en besluiten te beheren.

* **Persoonlijke aanbiedingen**: een persoonlijke aanbieding is een aanpasbaar marketingbericht op basis van geschiktheidsregels en restricties.

* **Plaatsingen**: een plaatsing is de locatie en/of de context waarin een aanbieding voor een eindgebruiker wordt weergegeven.

* **Prioriteit**: prioriteiten worden gebruikt om aanbiedingen te rangschikken die voldoen aan alle restricties, zoals geschiktheid, kalender en beperking.

* **Weergaven**: een weergave is informatie (bijv. de locatie of taal) die door een kanaal wordt gebruikt om een aanbieding te tonen.


## Tutorialvideo’s {#tutorial-videos}

>[!NOTE]
>
>Deze video&#39;s zijn van toepassing op de toepassingsservice van de Offer decisioning die op Adobe Experience Platform is gebouwd en zijn niet specifiek voor [!DNL Adobe Journey Optimizer]. Het biedt echter algemene richtlijnen voor het gebruik van Beslissingsbeheer in de context van [!DNL Journey Optimizer].

### Wat is het beheer van besluiten? {#what-is-offer-decisioning}

In de onderstaande video wordt een inleiding gegeven op de belangrijkste mogelijkheden, architectuur en gebruiksscenario&#39;s van het beheer van beslissingen:

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### Aanbiedingen definiëren en beheren {#use-offer-decisioning}

In de onderstaande video ziet u hoe u Beslissingsbeheer kunt gebruiken om uw aanbiedingen te definiëren en te beheren en real-time klantgegevens kunt gebruiken.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)
