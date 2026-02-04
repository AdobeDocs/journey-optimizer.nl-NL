---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met Loyalty Challenges
description: Leer hoe u in Adobe Journey Optimizer loyaliteitsuitdagingen kunt maken en beheren om aansprekende loyaliteitsprogramma's te maken.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private bèta" type="Informative"
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 0%

---


# Aan de slag met Loyalty Challenges {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* **wordt begonnen met de Uitdagingen van de Loyalty** {2 }︎ ◀ u bent hier **- Overzicht, werkschema, eerste vereisten**
* [&#x200B; de Uitdagingen van de Loyalty van de Toegang &#x200B;](access-loyalty-challenges.md) - Inventaris en het filtreren
* [&#x200B; creeer uitdagingen &#x200B;](create-challenges.md) - bouw en vorm uitdagingen
* [&#x200B; beheert uitdagingen &#x200B;](manage-challenges.md) - geef uit, controleer, optimaliseer

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="Informatie over Loyalty Challenges"
>abstract="Met Loyalty Challenges kunt u persoonlijke serviceaanbiedingen maken die klanten motiveren om specifieke acties te voltooien en beloningen te verdienen."

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

## Overzicht {#overview}

Loyalty Challenges verstrekt een volledige oplossing voor het creëren van loyaliteitsprogramma&#39;s op schaal, van het bepalen van taken en mijlpalen aan het leveren van inhoud en het volgen van prestaties over kanalen. U kunt drie soorten uitdagingservaringen tot stand brengen, beloningen vormen, multi-kanaalberichten verzenden bij zeer belangrijke levenscyclusstadia, en prestaties controleren door automatisch geproduceerde reizen-allen terwijl het handhaven van integratie met uw extern systeem van het loyaliteitsbeheer.

## Belangrijkste mogelijkheden {#key-capabilities}

Loyalty-uitdagingen gebruiken voor:

* **creeer drie soorten uitdagingen**:
   * **Norm**: De klanten voltooien om het even welk aantal taken in om het even welke orde om beloningen te verdienen
   * **Streak**: De klanten voltooien achtereenvolgens de zelfde taak veelvoudige tijden
   * **Opeenvolgend**: De klanten voltooien taken in een specifieke orde

* **de uitdagingsinhoud van het Ontwerp**: De inhoudskaarten van Journey Optimizer van het gebruik om de visuele vertegenwoordiging van uw uitdaging op klantenapparaten tot stand te brengen. Inhoudskaarten geven de informatie over de uitdaging, de voortgang en de beloningen weer.

* **de taakvereisten van de opstelling**: Bepaal welke klanten moeten doen om beloningen te verdienen, die omvatten:
   * Taaktypen (aankoop, uitgaven, bedrag, bezoek, betrokkenheid, aangepaste gebeurtenissen)
   * Hoeveelheidsvereisten
   * Productinclusies/uitsluitingen waarbij gebruik wordt gemaakt van SKU&#39;s, categorieën of kenmerken
   * Aangepaste kenmerken en voorwaarden

* **vorm beloningen**: Bepaal beloningen die de klanten of bij taakvoltooiing (progressieve beloningen) of na de voltooiing van de volledige uitdaging (definitieve beloningen) verdienen.

* **verzend multikanaalberichten**: Lever berichten over veelvoudige kanalen (in-app, e-mail, duw) in zeer belangrijke stadia:
   * **Lancering**: Wanneer de uitdaging begint
   * **Bezig**: Wanneer de klanten door partway zijn
   * **Volledig**: Wanneer de klanten de uitdaging beëindigen

* **prestaties van het Spoor**: De controle produceerde automatisch reizen en de prestaties van de overzichtsuitdaging door ingebouwde rapporten.

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

## Vereisten {#prerequisites}

Voordat u Loyalty Challenges gaat gebruiken, moet u controleren of u beschikt over:

### Instellingen voor gegevensinvoer {#data-ingestion}

Loyalty Challenges baseert zich op gegevens die door de bronschakelaars van Experience Platform worden opgenomen om klantenvooruitgang en taakvoltooiing te volgen.

1. **vorm een gesteunde bronschakelaar**: Momenteel, is de Capillaire schakelaar algemeen beschikbaar. Aanvullende connectors zijn gepland.

2. **bevestigt gegevensopname**: Zorg ervoor dat de loyaliteitsgebeurtenissen en de klantengegevens in Experience Platform stromen en beschikbaar in Journey Optimizer.

Zie voor gedetailleerde instructies:

* [&#x200B; Experience Platform brondocumentatie &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/home)
* [Bronconnectors configureren in Journey Optimizer](../start/get-started-sources.md)

### Vereiste machtigingen {#required-permissions}

Als u Loyalty Challenges wilt gebruiken, hebt u de juiste machtigingen in Journey Optimizer nodig. Neem contact op met de beheerder als u de functie niet kunt openen.

### Doelpubliek {#target-audiences}

Maak doelgroepen in Experience Platform voordat u uitdagingen gaat creëren. U kunt een bestaand publiek selecteren, maar u kunt geen nieuw publiek maken via de gebruikersinterface voor Loyalty Challenges.

## Belangrijke beperkingen {#limitations}

* **Geen grootboeksysteem**: De Uitdagingen van de Loyalty volgen geen monetaire waarden of puntsaldi. Wanneer de klanten een uitdaging voltooien en een beloning verdienen, roept Journey Optimizer uw extern systeem van het loyaliteitsbeheer om punttoewijzing te behandelen.

* **de selectie van het publiek slechts**: U kunt bestaand publiek selecteren maar kan geen nieuw publiek van de Uitdagingen UI van de Loyalty tot stand brengen.

## Volgende stappen {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong> de Uitdagingen van de Loyalty van de Toegang </strong></a>
    </div>
    <p>
    <em> Leer hoe te om tot de inventaris en filteruitdagingen toegang te hebben </em>
    <p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong> creeer uitdagingen </strong></a>
    </div>
    <p>
    <em> bouwt en vormt uw eerste loyaliteitsuitdaging </em>
    <p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <!--<img alt="Manage" src="../assets/do-not-localize/monitor-button.svg">-->
    </a>
    <div>
    <a href="manage-challenges.md"><strong> beheer uitdagingen </strong></a>
    </div>
    <p>
    <em> geef, controleer, en optimaliseer uitdagingen </em> uit
    <p>
  </td>
</tr>
</table>
