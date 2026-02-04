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
source-git-commit: e978d075efbbcb42e7500d921bd8cc3ed1eee890
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---


# Uitdagingen en taken beheren {#manage-challenges}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* [ wordt begonnen met de Uitdagingen van de Loyalty ](get-started.md) - Overzicht, werkschema, eerste vereisten
* [ de Uitdagingen van de Loyalty van de Toegang ](access-loyalty-challenges.md) - Inventaris en het filtreren
* [ creeer uitdagingen ](create-challenges.md) - bouw en vorm uitdagingen
* [ creeer taken ](create-tasks.md) - bepaal uitdagingstaken
* **beheer uitdagingen** {2 }︎ ◀ u hier **bent - geef uit, controleer, optimaliseer**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger als u toegang wilt aanvragen. Leer meer over [ beschikbaarheidslabels ](../rn/releases.md#availability-labels).

## Uitdagingen beheren {#manage-challenges-section}

### Uitdagingsstaten {#challenge-lifecycle}

De uitdagingen bewegen zich door verschillende statussen tijdens hun levenscyclus:

* **Ontwerp**: De uitdaging wordt gecreeerd of uitgegeven en is nog niet beschikbaar aan klanten
* **Gepubliceerd**: De uitdaging is actief, is de bijbehorende reis gecreeerd.

### Uitdagingen bewerken {#edit-challenges}

U kunt uitdagingen uitgeven door hen in de inventaris van Uitdagingen te openen. Het bewerkingsgedrag is afhankelijk van de status van de challenge:

**de uitdagingen van het Ontwerp**: U hebt volledig het uitgeven vermogen. Alle eigenschappen, taken, inhoud, en overseinen kunnen zonder beperkingen worden gewijzigd.

**Gepubliceerde uitdagingen**: Wanneer u een gepubliceerde uitdaging voor het uitgeven opent, moet u het eerst aan de status van het Ontwerp terugkeren.

* Alle aanpassingen die rechtstreeks op de automatisch gegenereerde reis worden aangebracht, gaan verloren
* De uitdaging keert terug naar de staat van het Ontwerp
* Nadat u de wijzigingen hebt aangebracht, moet u de uitdaging opnieuw opslaan en publiceren
* U moet de bijbehorende reis opnieuw activeren om de bijgewerkte uitdaging voor klanten beschikbaar te maken

>[!IMPORTANT]
>
>Het omkeren van een gepubliceerde controle naar een concept kan niet ongedaan worden gemaakt. Overweeg de impact op uw actieve reis alvorens te werk te gaan.

### Dubbele uitdagingen {#duplicate-challenges}

Het dupliceren van een uitdaging leidt tot een nauwkeurige exemplaar met alle taken, inhoud, en overseinen intact, die u toestaan om nieuwe versies snel tot stand te brengen zonder van kras te beginnen.

Een uitdaging dupliceren:

1. Navigeer naar het tabblad **[!UICONTROL Challenges]** en zoek de uitdaging die u wilt dupliceren.

1. Selecteer het pictogram ![](assets/do-not-localize/Smock_More_18_N.svg) naast die uitdaging en kies **[!UICONTROL Duplicate]** .

1. Er wordt een kopie van de challenge gemaakt. Open de gedupliceerde uitdaging en wijzig de vereiste eigenschappen.

1. Bespaar de gedupliceerde uitdaging en produceer de bijbehorende reis.

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

U kunt tot gedetailleerde prestatiesgegevens in de [ auto-geproduceerde reisrapporten ](../reports/journey-global-report-cja.md) ook toegang hebben, die extra inzichten en historische tendensen verstrekken.

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

1. Selecteer het pictogram ![](assets/do-not-localize/Smock_More_18_N.svg) naast de taak.

1. Kies **[!UICONTROL Delete]** .

1. Bevestig de verwijdering in het dialoogvenster.

>[!NOTE]
>
>Als een taak in om het even welke uitdaging (ontwerp, gepland, of levende) wordt gebruikt, moet u het uit alle uitdagingen eerst verwijderen alvorens u het kunt schrappen. U kunt overwegen taken te archiveren of te dupliceren in plaats van ze te verwijderen als u ze in de toekomst nodig hebt.
