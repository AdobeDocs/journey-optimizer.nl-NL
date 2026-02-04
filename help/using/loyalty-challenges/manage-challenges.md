---
solution: Journey Optimizer
product: journey optimizer
title: Beleidsuitdagingen beheren
description: Leer hoe u loyaliteitsproblemen in Adobe Journey Optimizer kunt beheren, bewaken en optimaliseren.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private bèta" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---


# Uitdagingen beheren {#manage-challenges}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* [&#x200B; wordt begonnen met de Uitdagingen van de Loyalty &#x200B;](get-started.md) - Overzicht, werkschema, eerste vereisten
* [&#x200B; de Uitdagingen van de Loyalty van de Toegang &#x200B;](access-loyalty-challenges.md) - Inventaris en het filtreren
* [&#x200B; creeer uitdagingen &#x200B;](create-challenges.md) - bouw en vorm uitdagingen
* [&#x200B; creeer taken &#x200B;](create-tasks.md) - bepaal uitdagingstaken
* **beheer uitdagingen** {2 }︎ ◀ u hier **bent - geef uit, controleer, optimaliseer**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger als u toegang wilt aanvragen. Leer meer over [&#x200B; beschikbaarheidslabels &#x200B;](../rn/releases.md#availability-labels).

## Uitdagingen beheren {#manage-challenges-section}

### Levenscyclus van uitdagingen {#challenge-lifecycle}

<!-- VISUAL: Flowchart diagram showing challenge lifecycle with status transitions: Draft → Scheduled → Live → Completed/Stopped/Archived -->

De uitdagingen bewegen zich door verschillende statussen tijdens hun levenscyclus:

* **Ontwerp**: De uitdaging wordt gecreeerd of uitgegeven en is nog niet beschikbaar aan klanten
* **Gepland**: De uitdaging is gepubliceerd en zal automatisch actief op de gespecificeerde begindatum worden
* **Levend**: De uitdaging is momenteel actief en de klanten kunnen deelnemen
* **Voltooid**: De uitdaging is geëindigd - of de einddatum is overgegaan of alle doelstellingen zijn verwezenlijkt
* **Gestopt**: De uitdaging werd manueel tegengehouden alvorens zijn natuurlijke voltooiing te bereiken
* **Gearchiveerd**: De uitdaging is gearchiveerd voor organisatorische doeleinden en is niet meer zichtbaar in de belangrijkste inventaris

### Uitdagingen bewerken {#edit-challenges}

U kunt uitdagingen afhankelijk van hun huidige status uitgeven:

* **de uitdagingen van het Ontwerp**: Het volledige het uitgeven vermogen - alle eigenschappen kunnen worden gewijzigd
* **Gepland/Levende uitdagingen**: Beperkte het uitgeven - u kunt inhoud bijwerken, overseinen, en data uitbreiden, maar kan kern uitdagingsstructuur (type, publiek, of taakdefinities) niet veranderen

Een uitdaging bewerken:

1. Navigeer naar het tabblad **[!UICONTROL Challenges]** in de lijst Loyalty Challenges.

1. Zoek de uitdaging die u wilt bewerken.

1. Selecteer de uitdagingsnaam om het in te openen uitgeeft wijze.

1. Breng uw veranderingen aan die op de uitdagingsstatus worden gebaseerd:
   * **de uitdagingen van het Ontwerp**: wijzig om het even welke eigenschappen, taken, inhoud, of overseinen
   * **Gepland/Levende uitdagingen**: De kaarten van de inhoud van de update, overseinen, of breidt einddata uit zoals nodig

1. Sla uw wijzigingen op. Voor geplande of live uitdagingen worden de wijzigingen onmiddellijk van kracht of volgens uw updateschema.

>[!NOTE]
>
>Voor veranderingen die belangrijke wijzigingen vereisen (zoals veranderend uitdagingstype, publiek, of taakstructuur), dupliceer de uitdaging en creeer een nieuwe versie in plaats van het uitgeven van bestaande.

### Dubbele uitdagingen {#duplicate-challenges}

Dubbele uitdagingen voor:

* Herhaal succesvolle uitdagingen voor nieuwe tijdsperioden
* Variaties maken voor verschillende soorten publiek
* Taakvereisten of beloningen bijwerken
* Ge-gedaan of voltooide uitdagingen opnieuw activeren

Het dupliceren van een uitdaging leidt tot een nauwkeurige exemplaar met alle taken, inhoud, en overseinen intact, die u toestaan om nieuwe versies snel tot stand te brengen zonder van kras te beginnen.

Een uitdaging dupliceren:

1. Navigeer naar het tabblad **[!UICONTROL Challenges]** in de lijst Loyalty Challenges.

1. Zoek de uitdaging die u wilt dupliceren.

1. Selecteer het menu Meer handelingen (drie punten) naast die uitdaging.

1. Kies **[!UICONTROL Duplicate]** .

1. Een exemplaar van de uitdaging wordt gecreeerd met &quot;[ Exemplaar ]&quot;toegevoegd aan zijn naam.

1. Open de gedupliceerde uitdaging en wijzig de noodzakelijke eigenschappen:
   * Werk de uitdagingsnaam bij
   * Begin- en einddatums aanpassen
   * Wijzig het doelpubliek indien nodig
   * Pas taken, beloningen, inhoud of overseinen zonodig aan

1. Controleer en publiceer de gedupliceerde uitdaging.

### Monitorprestaties {#monitor-performance}

<!-- SCREENSHOT: Challenge Performance tab showing key metrics dashboard with participation, completion, reward, and engagement metrics -->

Houd de prestaties van de uitdaging aan via belangrijke meetgegevens:

* **metriek van de Deelname**:
   * Inschrijving: Aantal klanten die zich bij de uitdaging hebben aangesloten
   * Actieve deelnemers: klanten die momenteel met de uitdaging te maken hebben
* **metriek van de Voltooiing**:
   * Afsluitingspercentages: percentage ingeschreven klanten dat de uitdaging heeft voltooid
   * Gemiddelde voltooiingstijd: gemiddelde tijd die nodig is om alle taken te voltooien
* **keert metriek** terug:
   * Totaal uitgekeerde beloningen: Geaggregeerde waarde van alle toegekende beloningen
   * Prijzen naar type: Uitsplitsing van beloningen naar beloningscategorie
* **metriek van de Betrokkenheid**:
   * Afbeeldingen van inhoudskaarten: Aantal malen dat contentkaarten zijn weergegeven
   * Berichtlevering: Aantal berichten dat via alle kanalen is verzonden

Voor toegang tot prestatiegegevens:

1. Navigeer naar het tabblad **[!UICONTROL Challenges]** in de lijst Loyalty Challenges.

1. Selecteer de uitdaging u wilt controleren.

1. Open het tabblad **[!UICONTROL Performance]** om metrische gegevens en analyses in real time weer te geven.

<!-- SCREENSHOT: Journey report showing challenge performance data with graphs and tables -->

U kunt tot gedetailleerde prestatiesgegevens in de [&#x200B; auto-geproduceerde reisrapporten &#x200B;](../reports/journey-global-report-cja.md) ook toegang hebben, die extra inzichten en historische tendensen verstrekken.

## Taken beheren {#manage-tasks}

De taken zijn herbruikbare componenten die over veelvoudige uitdagingen kunnen worden gebruikt. Het beheren van taken verzekert effectief consistentie over uw loyaliteitsprogramma en maakt het gemakkelijker om taakdefinities centraal bij te werken. Taken die in één uitdaging worden gecreëerd, kunnen in andere uitdagingen worden hergebruikt, waardoor dubbel werk wordt voorkomen en de standaardisering wordt gehandhaafd.

### Taken bewerken {#edit-tasks}

U kunt bestaande taken bewerken via de takenvoorraad. Overweeg het volgende:

* **Taken niet die in actieve uitdagingen** worden gebruikt: Kan vrij worden uitgegeven - alle eigenschappen kunnen zonder effect worden gewijzigd
* **Taken die in levende uitdagingen** worden gebruikt: De voorzichtigheid van de oefening, aangezien de veranderingen alle uitdagingen beïnvloeden gebruikend de taak - de wijzigingen zijn onmiddellijk van toepassing op alle verwijzende uitdagingen

Een taak bewerken:

1. Navigeer naar het tabblad **[!UICONTROL Tasks]** in de lijst Loyalty Challenges.

1. Zoek de taak die u wilt bewerken.

1. Selecteer de taaknaam om deze te openen in de bewerkingsmodus.

1. Wijzig desgewenst de taakeigenschappen:
   * Taaknaam of beschrijving bijwerken
   * Type activiteit of kenmerken wijzigen
   * In aanmerking komende items en uitsluitingen aanpassen
   * Vereisten voor hoeveelheid of hoeveelheid wijzigen

1. Sla uw wijzigingen op.

>[!WARNING]
>
>Wanneer het uitgeven van een taak die actief in levende uitdagingen wordt gebruikt, denk na creërend een duplicaat met een nieuwe versie eerder dan het wijzigen van origineel. Hierdoor worden ongewenste wijzigingen in actieve uitdagingen voorkomen en kunt u wijzigingen testen voordat u ze toepast.

### Taken verwijderen {#delete-tasks}

Taken kunnen alleen worden verwijderd als ze momenteel niet worden gebruikt voor uitdagingen. Voordat u een taak verwijdert:

* Controleer het **[!UICONTROL Used in challenges]** aantal in de inventaris van Taken
* Zorg ervoor dat er geen concepten, geplande of live uitdagingen zijn die verwijzen naar de taak

Een taak verwijderen:

1. Navigeer naar het tabblad **[!UICONTROL Tasks]** in de lijst Loyalty Challenges.

1. Zoek de taak die u wilt verwijderen.

1. Controleer of het **[!UICONTROL Used in challenges]** -aantal 0 weergeeft. Als het aantal groter is dan 0, moet u de taak uit alle uitdagingen alvorens schrapping eerst verwijderen.

1. Selecteer het menu Meer handelingen (drie punten) naast de taak.

1. Kies **[!UICONTROL Delete]** .

1. Bevestig de verwijdering in het dialoogvenster.

>[!NOTE]
>
>Als een taak in om het even welke uitdaging (ontwerp, gepland, of levende) wordt gebruikt, moet u het uit alle uitdagingen eerst verwijderen alvorens u het kunt schrappen. U kunt overwegen taken te archiveren of te dupliceren in plaats van ze te verwijderen als u ze in de toekomst nodig hebt.
