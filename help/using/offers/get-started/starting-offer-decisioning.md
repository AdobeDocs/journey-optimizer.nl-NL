---
title: Aan de slag met Beslissingsbeheer
description: Ontdek hoe Adobe Journey Optimizer u kan helpen uw klanten het juiste aanbod op het juiste moment te sturen
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: fcd8c4077bead912d709b726c6ff15464357a8be
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 21%

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

➡️ [Meer informatie over beslissingsbeheer in deze video&#39;s](#video)


>[!NOTE]
>
>Als u een [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} gebruiker die de **Offer decisioning** alle functies voor Beslissingsbeheer die in deze sectie worden beschreven, zijn ook op u van toepassing.

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

Machtigingen voor toegang tot en gebruik van beslissingsmogelijkheden worden beheerd met behulp van de [Adobe Admin Console](https://helpx.adobe.com/nl/enterprise/managing/user-guide.html){target="_blank"}.

Om toegang tot de functionaliteit van het Beheer van het Besluit te verlenen, moet u tot een **[!UICONTROL Product profile]** en wijs de overeenkomstige toestemmingen aan uw gebruikers toe. Meer informatie over beheren [!DNL Journey Optimizer] gebruikers en machtigingen in [deze sectie](../../administration/permissions.md).

De machtigingen die specifiek zijn voor Beslissingsbeheer worden vermeld in [deze sectie](../../administration/high-low-permissions.md#decisions-permissions).

## Woordenlijst {#glossary}

U kunt onder de lijst van de belangrijkste concepten vinden u zult werken met wanneer het gebruiken van Beslissingsbeheer.

* **Afbeelding** of **Frequentiecorrectie**: Afdekkingen worden gebruikt als een beperking om te bepalen hoe vaak een aanbieding wordt gepresenteerd. Er zijn twee soorten plafonds, hoeveel keer een aanbod kan worden voorgesteld over het gecombineerde doelpubliek, ook bekend als &quot;Total caps&quot; en hoeveel keer een aanbod kan worden voorgesteld aan dezelfde eindgebruiker, ook bekend als &quot;Profile Cap&quot;.

* **Verzamelingen**: Verzamelingen zijn subsets van aanbiedingen die zijn gebaseerd op vooraf gedefinieerde voorwaarden die door een marketeter zijn gedefinieerd, zoals de categorie van de aanbieding.

* **Besluit**: Een beslissing bevat de logica die de selectie van een aanbieding informeert.

* **Beslissingsregel**: Beslissingsregels zijn beperkingen die aan een gepersonaliseerd aanbod worden toegevoegd en die worden toegepast op een profiel om te bepalen of het in aanmerking komt voor steun.

* **In aanmerking komende aanbieding**: Een in aanmerking komende aanbieding voldoet aan de vooraf gedefinieerde beperkingen die consistent aan een profiel kunnen worden aangeboden.

* **Beslissingsbeheer**: Staat u toe om eindgebruiker gepersonaliseerde aanbiedingservaringen over kanalen en toepassingen tot stand te brengen en te leveren gebruikend bedrijfslogica en besluitvormingsregels.

* **Terugvalvoorstellen**: Een fallback-aanbieding is de standaardaanbieding die wordt weergegeven wanneer een eindgebruiker niet in aanmerking komt voor een van de gepersonaliseerde aanbiedingen in de collectie.

* **Voorstel**: Een aanbieding is een marketingbericht waaraan regels kunnen zijn gekoppeld die bepalen wie in aanmerking komt om de aanbieding te zien.

* **Bibliotheek van aanbieding**: De aanbiedingsbibliotheek is een centrale bibliotheek die wordt gebruikt om gepersonaliseerde en terugvalaanbiedingen, besluitvormingsregels en besluiten te beheren.

* **Persoonlijke aanbiedingen**: Een gepersonaliseerde aanbieding is een aanpasbaar marketingbericht dat is gebaseerd op toelatingsregels en -beperkingen.

* **Plaatsen**: Een plaatsing is de locatie en/of context waarin een aanbieding voor een eindgebruiker verschijnt.

* **Prioriteit**: De prioriteit wordt gebruikt om aanbiedingen te rangschikken die aan alle beperkingen, zoals geschiktheid, kalender, en maximum voldoen.

* **Vertegenwoordigingen**: Een vertegenwoordiging is informatie die door een kanaal, zoals plaats of taal wordt gebruikt om een aanbieding te tonen.

## Hoe kan ik-video&#39;s{#video}

### Wat is het beheer van besluiten? {#what-is-offer-decisioning}

In de onderstaande video wordt een inleiding gegeven op de belangrijkste mogelijkheden, architectuur en gebruiksscenario&#39;s van het beheer van beslissingen:

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### Aanbiedingen definiëren en beheren {#use-offer-decisioning}

In de onderstaande video ziet u hoe u Beslissingsbeheer kunt gebruiken om uw aanbiedingen te definiëren en te beheren en real-time klantgegevens kunt gebruiken.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)


