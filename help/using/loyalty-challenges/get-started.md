---
solution: Journey Optimizer
product: journey optimizer
title: Uitdagingen van Loyalty begrijpen
description: Meer informatie over Loyalty Challenges-functies, -workflow en -mogelijkheden in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private bèta" type="Informative"
source-git-commit: 419c7b3913ca4da50c69ed36ffc1a8c8520607b4
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---


# Uitdagingen van Loyalty begrijpen {#understand-loyalty-challenges}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="Informatie over Loyalty Challenges"
>abstract="Met Loyalty Challenges kunt u persoonlijke serviceaanbiedingen maken die klanten motiveren om specifieke acties te voltooien en beloningen te verdienen."

Loyalty Challenges laat u toe om gepersonaliseerde betrokkenheidsaanbiedingen te ontwerpen en op te stellen die klanten motiveren om specifieke acties te voltooien en beloningen te verdienen.

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* [&#x200B; begin met de Uitdagingen van de Loyalty &#x200B;](gs-loyalty-challenges.md) - Snel overzicht en volgende stappen
* **Begrijp Loyalty Uitdagingen** {2 }︎ ◀ u **- Eigenschappen, werkschema, eerste vereisten bent**
* [&#x200B; creeer uitdagingen &#x200B;](create-challenges.md) - bouw en vorm uitdagingen
* [&#x200B; beheert uitdagingen &#x200B;](manage-challenges.md) - geef uit, controleer, optimaliseer

>[!ENDSHADEBOX]

## Overzicht {#overview}

Loyalty Challenges verstrekt een volledige oplossing voor het creëren van loyaliteitsprogramma&#39;s op schaal, van het bepalen van taken en mijlpalen aan het leveren van inhoud en het volgen van prestaties over kanalen. U kunt drie soorten uitdagingservaringen tot stand brengen, beloningen vormen, multi-kanaalberichten verzenden bij zeer belangrijke levenscyclusstadia, en prestaties controleren door automatisch geproduceerde reizen-allen terwijl het handhaven van integratie met uw extern systeem van het loyaliteitsbeheer.

## Werking {#how-it-works}

Het creëren en lanceren van een loyaliteitsuitdaging volgt deze werkschema:

1. **de gegevensopname van de opstelling** - Vorm de bronschakelaars van Experience Platform (als Capillary) aan ingeste loyaliteitsgebeurtenisgegevens die klantenacties en vooruitgang volgen.

2. **creeer een uitdaging** - bepaal de basisuitdagingseigenschappen met inbegrip van naam, type (Norm, Streak, of Opeenvolgend), publiek, en datumwaaier.

3. **voegt taken** toe - bepaal de specifieke acties klanten, met inbegrip van taaktypes (aankoop, uitgeven, bezoek, enz.), hoeveelheden, productfilters, en beloningen moeten voltooien.

4. **de inhoudskaarten van het Ontwerp** - creeer de visuele vertegenwoordiging van uw uitdaging gebruikend de inhoudskaarten van Journey Optimizer die op klantenapparaten tonen.

5. **vorm overseinen** (Facultatief) - Opstelling multi-kanaalberichten (in-app, e-mail, duw) voor zeer belangrijke stadia: lancering, lopend, en voltooiing.

6. **Overzicht en publiceer** - test uw uitdaging met testprofielen, dan publiceer het om het ter beschikking te stellen van uw doelpubliek.

7. **Auto-Geproduceerde reis** - wanneer u publiceert, leidt Journey Optimizer automatisch tot een reis die de levering en het overseinen van de inhoudskaart orkestreert.

8. **activeer reis** - de auto-geproduceerde reis activeert op uw datum van het uitdagingsbegin en beheert alle klanteninteractie.

9. **prestaties van de Monitor** - de participatie van het spoor, voltooiingstarieven, beloningsdistributie, en berichtovereenkomst door ingebouwde rapporten en het wegcanvas.

>[!NOTE]
>
>De automatisch gegenereerde reis wordt weergegeven in uw reisvoorraad en kan indien nodig worden aangepast. Nochtans, synchroniseren de veranderingen die rechtstreeks aan de reis worden aangebracht niet terug naar de uitdagingsconfiguratie.

## Belangrijkste mogelijkheden {#key-capabilities}

Loyalty-uitdagingen gebruiken voor:

* **creeer drie soorten uitdagingen**:
   * **Norm**: De klanten voltooien om het even welk aantal taken om beloningen te verdienen.
   * **Streak**: De klanten voltooien de zelfde taak veelvoudige tijden.
   * **Opeenvolgend**: De klanten voltooien taken in een specifieke orde.

* **de uitdagingsinhoud van het Ontwerp**: De inhoudskaarten van Journey Optimizer van het gebruik om de visuele vertegenwoordiging van uw uitdaging op klantenapparaten tot stand te brengen. De kaarten van de inhoud tonen de uitdagingsinformatie, vooruitgang, en beloningen op het apparaat van de klant.

* **de taakvereisten van de opstelling**: Bepaal welke klanten moeten doen om beloningen te verdienen, die omvatten:
   * Taaktypen (aankoop, bedrag uit te geven, bezoek, enz.)
   * Hoeveelheidsvereisten
   * Productinclusies/uitsluitingen waarbij gebruik wordt gemaakt van SKU&#39;s
   * Aangepaste kenmerken en voorwaarden

* **vorm beloningen**: Bepaal beloningen die de klanten of bij taakvoltooiing of na de voltooiing van de volledige uitdaging verdienen

* **verzendt berichten**: Lever berichten over veelvoudige kanalen (in-app, e-mail, duw) in zeer belangrijke stadia:
   * **Lancering**: Wanneer de uitdaging begint
   * **Bezig**: Wanneer de klanten door partway zijn
   * **Volledig**: Wanneer de klanten de uitdaging beëindigen

* **prestaties van het Spoor**: De monitor automatisch geproduceerde reizen en de prestaties van de overzichtsuitdaging

### Belangrijke beperkingen {#limitations}

* **Geen grootboeksysteem**: De Uitdagingen van de Loyalty volgen geen monetaire waarden of puntsaldi. Wanneer de klanten een uitdaging voltooien en een beloning verdienen, roept Journey Optimizer uw extern systeem van het loyaliteitsbeheer om punttoewijzing te behandelen.

* **de selectie van het publiek slechts**: U kunt bestaand publiek selecteren maar kan geen nieuw publiek van de Uitdagingen UI van de Loyalty tot stand brengen.

## Vereisten {#prerequisites}

Voordat u Loyalty Challenges gaat gebruiken, moet u controleren of u beschikt over:

### Instellingen voor gegevensinvoer {#data-ingestion}

Loyalty Challenges baseert zich op gegevens die door de bronschakelaars van Experience Platform worden opgenomen om klantenvooruitgang en taakvoltooiing te volgen.

1. **vorm een gesteunde bronschakelaar**: Momenteel, is de Capillaire schakelaar algemeen beschikbaar. Aanvullende connectors zijn gepland.

2. **bevestigt gegevensopname**: Zorg ervoor dat de loyaliteitsgebeurtenissen en de klantengegevens in Experience Platform stromen en beschikbaar in Journey Optimizer.

Zie voor gedetailleerde instructies:

* [&#x200B; Experience Platform brondocumentatie &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Bronconnectors configureren in Journey Optimizer](../start/get-started-sources.md)

### Vereiste machtigingen {#required-permissions}

Als u Loyalty Challenges wilt gebruiken, hebt u de juiste machtigingen in Journey Optimizer nodig. Neem contact op met de beheerder als u de functie niet kunt openen.

## Loyalty-uitdagingen openen {#access}

Toegang krijgen tot Loyalty-uitdagingen:

1. Selecteer in Adobe Journey Optimizer **[!UICONTROL Loyalty challenges]** in het navigatiemenu aan de linkerkant.

2. De inventaris van de Uitdagingen van de Loyalty toont alle bestaande uitdagingen met informatie zoals:
   * Naam en beschrijving van uitdaging
   * Status (concept, live, gestopt, enz.)
   * Uitdagingstype (Standaard, Streak, Opeenvolgend)
   * Begin- en einddatum
   * Laatste wijzigingsdatum

3. Selecteer **[!UICONTROL Create challenge]** om een nieuwe uitdaging te beginnen maken.

### Uitdagingen voor zoeken en filteren {#search-filter}

Gebruik de zoek- en filtermogelijkheden om snel specifieke uitdagingen te vinden:

* **Onderzoek**: Ga uitdagingsnaam of sleutelwoorden op het gebied van het Onderzoek in
* **Filter door status**: Ontwerp, Gepland, Levend, Voltooid, Gestopt, of Gearchiveerd
* **Filter door type**: Standaard, Streak, of Opeenvolgende uitdagingen
* **Filter door datum**: Uitdagingen binnen een specifieke datumwaaier
* **Filter door markeringen**: Uitdagingen met specifieke toegepaste markeringen

## Volgende stappen {#next-steps}

Nu u Loyalty Uitdagingen begrijpt, leer hoe te om uw eerste uitdaging tot stand te brengen:

* [Uitdagingen maken](create-challenges.md)
* [Uitdagingen beheren](manage-challenges.md)
