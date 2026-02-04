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
source-git-commit: 5120eb51311348b8561b0a20f982576f6c945921
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---


# Aan de slag met Loyalty Challenges {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* **wordt begonnen met de Uitdagingen van de Loyalty** {2 }︎ ◀ u bent hier **- Overzicht, werkschema, eerste vereisten**
* [&#x200B; de Uitdagingen van de Loyalty van de Toegang &#x200B;](access-loyalty-challenges.md) - Inventaris en het filtreren
* [&#x200B; creeer uitdagingen &#x200B;](create-challenges.md) - bouw en vorm uitdagingen
* [&#x200B; creeer taken &#x200B;](create-tasks.md) - bepaal uitdagingstaken
* [&#x200B; beheert uitdagingen &#x200B;](manage-challenges.md) - geef uit, controleer, optimaliseer

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger als u toegang wilt aanvragen. Leer meer over [&#x200B; beschikbaarheidslabels &#x200B;](../rn/releases.md#availability-labels).

## Overzicht {#overview}

Loyalty Challenges verstrekken een volledige oplossing voor het creëren van loyaliteitsprogramma&#39;s op schaal, van het bepalen van taken en mijlpalen aan het leveren van inhoud en het volgen van prestaties over kanalen.

U kunt drie soorten uitdagingservaringen tot stand brengen:

* **Standaard uitdagingen**: De klanten voltooien om het even welk gespecificeerd aantal taken in om het even welke orde
* **de uitdagingen van de Streak**: De klanten voltooien achtereenvolgens de zelfde taak veelvoudige tijden
* **Opeenvolgende uitdagingen**: De klanten voltooien taken in een bepaalde orde

Met de Uitdagingen van de Loyalty, kunt u beloningen vormen, multi-kanaalberichten bij zeer belangrijke levenscyclusstadia verzenden, en prestaties door automatisch geproduceerde reizen controleren-allen terwijl het handhaven van integratie met uw extern systeem van het loyaliteitsbeheer.

<!-- SCREENSHOT: High-level diagram showing Loyalty Challenges architecture with: Data ingestion from source connectors -> Challenge creation in JO -> Content cards & messaging -> Customer device -> Journey tracking -->

## Werking {#how-it-works}

<!-- SCHEMA: Visual workflow diagram showing the 8 steps in the loyalty challenge creation process with icons for each step -->

Het creëren en lanceren van een loyaliteitsuitdaging volgt deze werkschema:

1. **de gegevensopname van de opstelling** - Vorm de bronschakelaars van Experience Platform (zoals de Capillaire schakelaar) om loyaliteitsgebeurtenisgegevens in te voeren die klantenacties en vooruitgang volgen. Deze gegevens stellen het bijhouden van taken en het voltooien van taken op de proef.

1. **creeer een uitdaging** - bepaal de basisuitdagingseigenschappen met inbegrip van naam, type (Norm, Streak, of Opeenvolgend), publiek, en datumwaaier. Zie [&#x200B; tot uitdagingen &#x200B;](create-challenges.md) voor gedetailleerde stappen leiden.

1. **voegt taken** toe - bepaal de specifieke acties klanten moeten voltooien, met inbegrip van taaktypes (aankoop, uitgeven, bezoek, overeenkomst, douanegebeurtenissen), hoeveelheden, productfilters, en beloningen. Zie [&#x200B; tot taken &#x200B;](create-tasks.md) voor gedetailleerde instructies leiden.

1. **de inhoudskaarten van het Ontwerp** - creeer de visuele vertegenwoordiging van uw uitdaging gebruikend Journey Optimizer [&#x200B; inhoudskaarten &#x200B;](../content-card/create-content-card.md) die op klantenapparaten tonen. De kaarten van de inhoud tonen uitdagingsinformatie, vooruitgang, en beloningen.

1. **vorm overseinen** (Facultatief) - de berichten van de opstelling multi-channel ([&#x200B; in-app &#x200B;](../in-app/get-started-in-app.md), [&#x200B; e-mail &#x200B;](../email/get-started-email.md), [&#x200B; duw &#x200B;](../push/get-started-push.md)) voor zeer belangrijke levenscyclusstadia: lancering, lopend, en voltooiing.

1. **Overzicht en publiceer** - test uw uitdaging met [&#x200B; testprofielen &#x200B;](../content-management/test-profiles.md), dan publiceer het om het ter beschikking te stellen van uw doelpubliek.

1. **activeer reis** - wanneer u een uitdaging publiceert, leidt Journey Optimizer automatisch tot a [&#x200B; reis &#x200B;](../building-journeys/journey-gs.md) in de status van het Ontwerp die de levering en het overseinen van de inhoudskaart organiseert. Navigeer aan de inventaris van de Reizen, bepaal de plaats van de auto-geproduceerde reis (genoemd &quot;Uitdaging: [ Naam van de Uitdaging ]&quot;), en [&#x200B; activeer het &#x200B;](../building-journeys/publish-journey.md) om de uitdaging beschikbaar te maken aan uw klanten.

1. **prestaties van de Monitor** - de participatie van het spoor, voltooiingstarieven, beloningsdistributie, en berichtovereenkomst door ingebouwde rapporten en het wegcanvas. Zie [&#x200B; uitdagingen &#x200B;](manage-challenges.md) voor het controleren van details beheren.

## Vereisten {#prerequisites}

Voordat u Loyalty Challenges gaat gebruiken, moet u controleren of u beschikt over:

+++Instellingen voor gegevensinvoer

Loyalty Challenges baseren zich op gegevens die door de bronschakelaars van Experience Platform worden opgenomen om klantenvooruitgang en taakvoltooiing te volgen.

1. **vorm een gesteunde bronschakelaar**: Momenteel, is de Capillaire schakelaar algemeen beschikbaar. Extra schakelaars zijn gepland voor toekomstige versies.

1. **bevestigt gegevensopname**: Zorg ervoor dat de loyaliteitsgebeurtenissen en de klantengegevens in Experience Platform stromen en beschikbaar in Journey Optimizer. Verifieer dat het gegevensschema de noodzakelijke gebieden voor het volgen van klantenacties en vooruitgang omvat.

Zie voor gedetailleerde instructies:

* [&#x200B; Experience Platform brondocumentatie &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Bronconnectors configureren in Journey Optimizer](../start/get-started-sources.md)

+++

+++Vereiste machtigingen

Als u Loyalty Challenges wilt gebruiken, hebt u de juiste machtigingen in Journey Optimizer nodig. Vereiste machtigingen zijn:

* Toegang tot de functie **[!UICONTROL Loyalty challenges]**
* Machtigingen om reizen te maken en te beheren
* Machtigingen om inhoudskaarten te maken en te beheren
* Machtigingen om een publiek te maken en te beheren

Neem contact op met de beheerder als u geen toegang hebt tot de functie of aanvullende machtigingen nodig hebt.

+++

+++Doelpubliek

Maak doelgroepen in Experience Platform voordat u uitdagingen gaat creëren. Dit publiek bepaalt welke klanten verkiesbaar zijn om aan uw loyaliteitsuitdagingen deel te nemen. Voor meer informatie over hoe te om publiek tot stand te brengen, verwijs naar [&#x200B; begonnen wordt met publiek &#x200B;](../audience/about-audiences.md).

+++

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
    </p>
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
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
    <!--<img alt="Tasks" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-tasks.md"><strong> creeer taken </strong></a>
    </div>
    <p>
    <em> bepaal acties en beloningen voor uitdagingen </em>
    </p>
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
    </p>
  </td>
</tr>
</table>
