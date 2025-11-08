---
solution: Journey Optimizer
product: journey optimizer
title: Ervaar gebeurtenissen opzoeken tijdens reizen
description: Leer hoe u Experience Events lookup kunt gebruiken tijdens reizen
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
version: Journey Orchestration
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 1%

---

# Opzoeken van gebeurtenissen tijdens reizen beleven {#ee-journeys}

>[!CAUTION]
>
>Vanaf 8 juli 2025 wordt in nieuwe klantenorganisaties het maken van expressies met behulp van ervaringsgebeurtenissen niet langer ondersteund in de expressie-editor die wordt gebruikt in reisomstandigheden. Dientengevolge, kan de ervaringsgebeurtenissen in de [&#x200B; gegevensbron van Experience Platform &#x200B;](../datasource/adobe-experience-platform-data-source.md) niet voor het creëren van uitdrukkingen worden gebruikt. Hieronder wordt verwezen naar alternatieve benaderingen en aanbevolen methoden voor het maken van expressies/logica met ervaringsgebeurtenissen.
>
>Wilt u meer details? [&#x200B; las uit Veelgestelde vragen &#x200B;](#faq-ee).

Deze pagina schetst gemeenschappelijke patronen en scalable benaderingen om u te helpen de Gebeurtenissen van de Ervaring in Adobe Journey Optimizer optimaal maken. Deze gebruiksgevallen zijn ontworpen om u te helpen veelvoorkomende uitdagingen op te lossen, zoals het beheren van opt-outs, het controleren van berichtfrequentie, het personaliseren van inhoud die op gebruikersgedrag wordt gebaseerd, en het reageren op signalen in real time.

Door gebruik te maken van deze strategieën kunt u gedragsgegevens omzetten in betekenisvolle acties, zoals onderdrukken, kwalificeren of uitsluiten van profielen op basis van de gebeurtenissen die ze activeren of de kenmerken die ze dragen. Of u logica voor aankoopdrempels bouwt, ontslagtrekkers, of stuiterende behandeling, deze voorbeelden bieden praktische begeleiding u aan uw behoeften kunt aanpassen.

Als u de beste aanpak kiest, moet u rekening houden met de latentievereisten van uw gebruikscase om ervoor te zorgen dat uw reizen responsief en effectief blijven.

## Onderdrukking uitschakelen

Om profielen te onderdrukken die uit marketing mededelingen hebben verkozen, gebruik ingebouwde toestemmingsbeheer. Voorkeuren voor het uitschakelen worden automatisch vastgelegd in de toestemmingsvelden van het profiel. Er kan rechtstreeks naar worden verwezen in reisomstandigheden en deze worden automatisch afgedwongen door Journey Optimizer tijdens het verzenden van berichten.

Meer informatie:

* [Toestemming beheren](../privacy/opt-out.md)
* [&#x200B; e-mail opt-out beheer &#x200B;](../email/email-opt-out.md)
* [Uitschakelen van beheer voor tekstberichten](../sms/sms-opt-out.md)


## Onderdrukking op basis van stuit

Als u profielen wilt uitsluiten waarvoor e-mailblokkeringen zijn opgetreden, kunt u gebruikmaken van de automatische suppressielijst voor Adobe Journey Optimizer voor samengevouwen adressen. Dit ingebouwde mechanisme zorgt ervoor dat ongeldige of onbereikbare e-mails van de toekomst worden uitgesloten verzendt zonder aangepaste logica te vereisen.

Meer informatie:

* [De vervolgkeuzelijst beheren](../configuration/manage-suppression-list.md)


## Algemene onderdrukking

Als u profielen wilt onderdrukken die bepaalde gedragingen hebben aangetoond, gebruikt u batchdoelgroepen met op gebeurtenissen gebaseerde logica om profielen vast te leggen die aan de onderdrukkingscriteria voldoen. Verwijs naar dit publiek in reisomstandigheden.

Meer informatie:

* Adobe Experience Platform [&#x200B; de bouwer van het Segment - Gebeurtenissen &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* De bouwer van het Segment van Adobe Experience Platform [&#x200B; - de beperkingen van de Tijd &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Gebruik van soorten publiek in omstandigheden](../building-journeys/condition-activity.md#using-a-segment)

* [inAudience() functie](../building-journeys/functions/functioninaudience.md)


## Communicatie-ontvangst uitsluiting

Om het verzenden van berichten naar profielen te verhinderen die om het even welke mededelingen binnen een recent tijdvenster hebben ontvangen:

* Gebruik batchdoelgroepen met tijdgebonden criteria en gebruik deze als referentie in reisomstandigheden.
* Pas frequentie het begrenzen bedrijfsregels toe om dagelijkse of wekelijkse berichtgrenzen af te dwingen.


Meer informatie met doelgroepen:

* Adobe Experience Platform [&#x200B; de bouwer van het Segment - Gebeurtenissen &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* De bouwer van het Segment van Adobe Experience Platform [&#x200B; - de beperkingen van de Tijd &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Gebruik van soorten publiek in omstandigheden](../building-journeys/condition-activity.md#using-a-segment)

* [inAudience() functie](../building-journeys/functions/functioninaudience.md)


Zie ook:

* [Frequentiecapaciteit per kanaal en communicatietype](../conflict-prioritization/channel-capping.md)



## Specifieke opname/uitsluiting van berichten

Als u profielen wilt opnemen of uitsluiten op basis van het feit of ze een bepaald bericht hebben ontvangen, maakt u batchdoelgroepen die deze logica inkapselen en er in de reisomstandigheden naar verwijzen.


Meer informatie:

* Adobe Experience Platform [&#x200B; de bouwer van het Segment - Gebeurtenissen &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* De bouwer van het Segment van Adobe Experience Platform [&#x200B; - de beperkingen van de Tijd &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Gebruik van soorten publiek in omstandigheden](../building-journeys/condition-activity.md#using-a-segment)

* [inAudience() functie](../building-journeys/functions/functioninaudience.md)

## Verpersoonlijking voor afgedankte winkels of winkels

Om mededelingen te personaliseren die op de recentste kar worden gebaseerd of gebeurtenissen over veelvoudige karttypes of productmeningen te doorbladeren:

* Als u toegang tot [&#x200B; Gegevens Distiller van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/overview){target="_blank"} hebt, vorm geautomatiseerde vragen om de vereiste gegevens uit de gebeurtenis te halen, het te manipuleren om het gebruiksgeval te passen, en het terug naar een profiel-toegelaten dataset voor activering te schrijven.
* Als de gegevens van het verlaten van de plaats op het profiel met scalaire attributen kunnen worden gemodelleerd, denk na gebruikend Berekende attributen om de recentste informatie te vangen en dan naar deze attributen in de reis te verwijzen om de mededeling te construeren. [&#x200B; leer meer in de documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}


## Reizen op basis van gedrag

Als u profielen van de reis wilt verwijderen wanneer ze een bepaald gedrag vertonen, gebruikt u afsluitcriteria om het profiel van de reis af te sluiten wanneer een bepaalde gebeurtenis wordt ontvangen of het profiel in aanmerking komt voor een bepaald publiek.

Meer informatie:

* [De eigenschappen van uw reis instellen - criteria afsluiten](journey-properties.md#exit-criteria)

## Kwalificatie op basis van aankoop met drempelwaarden

Om ritten op aankopen te activeren en onderdrukken als de waarde boven of onder een drempel ligt, definieert u berekende kenmerken voor de som van aankopen over een specifieke periode. Maak een publiek dat profielen bevat waarvan het uitgavenbedrag aan bepaalde criteria voldoet.

Meer informatie:

* Adobe Experience Platform [&#x200B; Berekende attributen overzicht &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## Veelgestelde vragen {#faq-ee}

Hieronder vindt u Veelgestelde vragen over het opzoeken van gebeurtenissen Experience tijdens reizen.

Wilt u meer details? Gebruik terugkoppelen opties bij de bodem van deze pagina om uw vraag op te roepen, of met [&#x200B; gemeenschap van Adobe Journey Optimizer &#x200B;](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"} te verbinden.

+++Welke specifieke mogelijkheden worden beïnvloed? 

Alleen het opzoeken van ervaringsgebeurtenissen in de expressieeditor heeft invloed. De volgende mogelijkheden zijn **niet** beïnvloed en blijven het zelfde:

* Waarnemen van ervaringsgebeurtenissen die zijn gekoppeld aan een specifiek profiel in de profielinterface

* Het gebruiken van ervaringsgebeurtenissen in gegevens verwerkte attributenregels en de toegang tot van de gegevens verwerkte attributen in een reis

* Een reis voortbrengen met een eenheids- of bedrijfsevenement

* Het gebruiken van de gegevens van de reiscontext van de gebeurtenissen die de reis in uitdrukking en verpersoonlijkingsredacteuren teweegbrengen

* Luisteren naar een gebeurtenis tijdens een reis

* Gebeurtenissen configureren om een rit te activeren

* Gebeurtenissen voor de reactie van de eindgebruiker op marketingberichten detecteren (bijvoorbeeld e-mail open)

+++

+++Heeft deze update invloed op mijn bestaande Adobe-organisatie? 

Dit heeft alleen gevolgen voor uw Adobe-organisatie als u de zoekfunctie voor ervaringsgebeurtenissen nog niet hebt gebruikt. Als u reeds ervaringsgebeurtenissen in de [&#x200B; gegevensbron van Experience Platform &#x200B;](../datasource/adobe-experience-platform-data-source.md) gebruikt, blijft uw organisatie van Adobe steun voor de raadpleging van de ervaringsgebeurtenis hebben.

+++

+++Ik heb een nieuwe Adobe Organisatie. Hoe kan ik mijn gebruikscase oplossen die ervaringsgebeurtenisgegevens vereist? 

Er zijn hierboven alternatieve benaderingen en beste praktijken met ervaringen beschikbaar om de gewenste gebruiksgevallen te bereiken.

+++

+++ Wat als alternatieve benaderingen niet werken voor mijn gebruiksgeval?

Neem contact op met uw Adobe-vertegenwoordiger als uw gebruikscase niet kan worden opgelost met een van de bovenstaande alternatieve methoden.

+++
