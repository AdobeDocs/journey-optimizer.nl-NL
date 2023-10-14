---
product: experience platform
solution: Experience Platform
title: Gepersonaliseerd optimalisatiemodel
description: Meer informatie over aangepaste optimalisatiemodellen
feature: Ranking Formulas, Offers
role: User
level: Intermediate
exl-id: c73b3092-e96d-4957-88e6-500e99542782
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# Gepersonaliseerd optimalisatiemodel {#personalized-optimization-model}

## Overzicht {#overview}

Door de geavanceerde technologieën in het gecontroleerde machine leren en diep leren te gebruiken, staat de auto-verpersoonlijking een bedrijfsgebruiker (marktleider) toe om bedrijfsdoelstellingen te bepalen en hun klantengegevens te gebruiken om zaken-georiënteerde modellen te trainen om gepersonaliseerde aanbiedingen te dienen en KPIs te maximaliseren.

![](../../rn/assets/do-not-localize/ai-ranking.gif)

## Belangrijkste modelaannames en -beperkingen {#key}

Om het voordeel van het gebruiken van auto-verpersoonlijking te maximaliseren, zijn er enkele belangrijke veronderstellingen en beperkingen om zich van bewust te zijn.

* **Aanbiedingen zijn anders genoeg, zodat gebruikers verschillende voorkeuren hebben voor de aanbiedingen in kwestie**. Als de aanbiedingen te gelijkaardig zijn, zal een resulterend model minder effect hebben aangezien de reacties schijnbaar willekeurig zijn.
Als een bank bijvoorbeeld twee creditcardaanbiedingen heeft met het enige verschil in kleur, dan maakt het niet uit welke kaart wordt aanbevolen, maar als elke kaart andere voorwaarden heeft, geeft dit een reden waarom bepaalde klanten er een zouden kiezen en voldoende verschil tussen de aanbiedingen zouden maken om een onhandiger model op te bouwen.
* **Gebruikersverkeerssamenstelling is stabiel**. Als de samenstelling van het gebruikersverkeer tijdens modelopleiding en het voorspellen dramatisch verandert, zouden de modelprestaties kunnen degraderen. Bijvoorbeeld, veronderstel in model opleidingsfase, slechts zijn de gegevens voor gebruikers in publiek A beschikbaar, maar het opgeleide model wordt gebruikt om voorspellingen voor gebruikers in publiek B te produceren, dan modelprestaties zouden kunnen worden beïnvloed.
* **De prestaties van aanbiedingen veranderen niet drastisch over een korte periode** aangezien dit model wekelijks bijwerkt en de veranderingen in prestaties worden overgebracht als modelupdates. Een product was bijvoorbeeld al eerder erg populair, maar in een openbaar rapport wordt het product geïdentificeerd als schadelijk voor onze gezondheid, en dit product wordt extreem snel impopulair. In dit scenario, kon het model dit product blijven voorspellen tot het model met veranderingen in gebruikersgedrag bijwerkt.

## Hoe het werkt {#how}

Het model leert complexe eigenschapinteractie tussen aanbiedingen, gebruikersinformatie en contextafhankelijke informatie om gepersonaliseerde aanbiedingen aan eind - gebruikers aan te bevelen. Functies zijn invoer in het model.

Er zijn drie typen functies:

| Typen functies | Functies toevoegen aan modellen |
|--------------|----------------------------|
| Decisioning-objecten (placementID, activityID, DecisionScopeID) | Deel van de feedback-ervaringen over het beheer van beslissingen die naar het AEP zijn verzonden |
| Doelgroepen | Het publiek 0-50 kan worden toegevoegd als functies bij het maken van het Willekeurige AI-model |
| Contextgegevens | Een deel van de beslissing feedback over ervaringen die naar AEP zijn gestuurd. Beschikbare contextgegevens die aan het schema moeten worden toegevoegd: Details van de handel, Details van het Kanaal, Details van de Toepassing, Details van het Web, Details van het Milieu, Apparaatdetails, PlaceContext |

Het model heeft twee fasen:

* In de **offline modeltraining** fase, wordt een model getraind door het leren en het memoriseren eigenschapinteractie in historische gegevens.
* In de **online conferentie** De kandidaten worden gerangschikt op basis van real-time scores die door het model worden gegenereerd. In tegenstelling tot traditionele samenwerkings het filtreren technieken, die moeilijk om eigenschappen voor gebruikers en aanbiedingen te omvatten is, is auto-verpersoonlijking een diepe het leren gebaseerde raadsmethode, en kan complexe en niet-lineaire de patronen van de eigenschapinteractie omvatten en leren.

Hier volgt een vereenvoudigd voorbeeld om het basisidee achter auto-personalisatie te illustreren. Veronderstel wij een dataset hebben die historische interactie tussen gebruikers en aanbiedingen opslaat, die in Figuur 1 wordt getoond. Er zijn:
* Twee aanbiedingen, aanbieding_1 en aanbieding_2,
* Twee functies, feature_1 en feature_2,
* Een responskolom.

De waarde van feature_1, feature_2 en response is 0 of 1. Wanneer wij de blauwe dozen en de oranje dozen in Figuur 1 bekijken, kunnen wij vinden dat voor aanbieding_1, de reacties eerder 1 zijn wanneer feature_1 en feature_2 de zelfde waarden hebben, terwijl voor offer_2, de etiketten eerder 1 zijn wanneer feature_1 0 is en feature_2 1 is. We kunnen ook zien dat in het rode vak, aanbieding_1 wordt gediend wanneer feature_1 0 is en feature_2 1 is, en de reactie 0 is. Gebaseerd op het patroon dat wij in oranje dozen zien, wanneer feature_1 0 is en feature_2 1 is, biedt_2 waarschijnlijk een betere aanbeveling is.

In feite is dit het idee om historische eigenschapinteractie te leren en te herdenken en deze toe te passen om gepersonaliseerde voorspellingen te genereren.

![](../assets/perso-ranking-schema.png)

## Probleem met koude start {#cold-start}

Koud-startprobleem doet zich voor wanneer er onvoldoende gegevens zijn om een aanbeveling te doen. Voor auto-verpersoonlijking, zijn er twee soorten koudstartproblemen.

* **Na het maken van een nieuw AI-model zonder historische gegevens**, worden de aanbiedingen voor een bepaalde periode willekeurig bediend om gegevens te verzamelen, en de gegevens worden gebruikt om het eerste model op te leiden.
* **Nadat het eerste model is vrijgegeven** 10% van het totale verkeer zal worden toegewezen voor willekeurig verkeer, terwijl 90% van het verkeer zal worden gebruikt voor modelaanbevelingen. Als nieuwe aanbiedingen aan het AI-model worden toegevoegd, zouden deze dus worden geleverd als onderdeel van de 10% van het verkeer. De gegevens die over die aanbiedingen worden verzameld zouden het aantal tijden bepalen het onder de 90% van verkeer wordt geselecteerd aangezien het model blijft worden bijgewerkt.

## Herscholing {#re-training}

Modellen worden opnieuw getraind om de nieuwste functies-interacties te leren en de verslechtering van de modelprestaties wekelijks te beperken.
