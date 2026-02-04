---
solution: Journey Optimizer
product: journey optimizer
title: Taken maken voor loyaliteitsuitdagingen
description: Leer hoe u taken voor loyaliteitsuitdagingen in Adobe Journey Optimizer kunt maken en configureren.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private bèta" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---


# Taken maken {#create-tasks}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* [&#x200B; wordt begonnen met de Uitdagingen van de Loyalty &#x200B;](get-started.md) - Overzicht, werkschema, eerste vereisten
* [&#x200B; de Uitdagingen van de Loyalty van de Toegang &#x200B;](access-loyalty-challenges.md) - Inventaris en het filtreren
* [&#x200B; creeer uitdagingen &#x200B;](create-challenges.md) - bouw en vorm uitdagingen
* **creeer taken** {2 }︎ ◀ u hier **bent - bepaal uitdagingstaken**
* [&#x200B; beheert uitdagingen &#x200B;](manage-challenges.md) - geef uit, controleer, optimaliseer

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger als u toegang wilt aanvragen. Leer meer over [&#x200B; beschikbaarheidslabels &#x200B;](../rn/releases.md#availability-labels).

## Overzicht {#overview}

De taken bepalen de specifieke acties of de mijlpalen die de klanten moeten voltooien om beloningen in een loyaliteitsuitdaging te verdienen. U kunt taaktypes, hoeveelheden, productvereisten, en beloningswaarden vormen om het in dienst nemen en gepersonaliseerde loyaliteitservaringen tot stand te brengen.

Elke taak vertegenwoordigt een meetbare actie die tot uitdagingsvoltooiing bijdraagt. De taken zijn herbruikbare componenten die onafhankelijk kunnen worden tot stand gebracht en dan aan één of meerdere uitdagingen worden toegevoegd, of direct binnen een uitdaging worden gecreeerd.

### Hoe de taken in verschillende uitdagingstypes werken {#task-overview}

<!-- VISUAL: Diagram showing how task completion works differently for Standard, Streak, and Sequential challenges with examples -->

Afhankelijk van uw uitdagingstype (Standaard, Streak, of Opeenvolgend), voltooien de klanten taken verschillend:

* **Standaard uitdagingen**: De klanten voltooien om het even welk gespecificeerd aantal taken in om het even welke orde
* **de uitdagingen van de Streak**: De klanten voltooien achtereenvolgens de zelfde taak veelvoudige tijden
* **Opeenvolgende uitdagingen**: De klanten voltooien taken in een bepaalde orde

## Een taak maken {#create-task}

<!-- SCREENSHOT: Two screenshots side by side showing the two entry points: Tasks tab with "Create task" button, and challenge editor with "Add task" button -->

U kunt taken maken op basis van twee invoerpunten. Het configuratieproces is het zelfde ongeacht waar u begint.

+++Van de inventaris van Taken

1. Navigeer naar **[!UICONTROL Loyalty challenges]** in Journey Optimizer.

1. Selecteer het tabblad **[!UICONTROL Tasks]**. 

1. Selecteer **[!UICONTROL Create task]**.

Taken die zijn gemaakt op basis van de inventaris, worden opgeslagen en beschikbaar voor hergebruik voor meerdere uitdagingen.

+++

+++Van binnen een uitdaging

1. Open een bestaande uitdaging of maak een nieuwe.

1. Ga naar de sectie **[!UICONTROL Tasks]** .

1. Selecteer **[!UICONTROL Add task]** en kies vervolgens **[!UICONTROL Create new task]** .

Taken die op deze manier worden gemaakt, worden automatisch toegevoegd aan uw taak en worden ook opgeslagen in de takenvoorraad voor hergebruik in andere uitdagingen.

+++

### Taakeigenschappen definiëren {#define-task-properties}

<!-- SCREENSHOT: Task properties form showing Task name and Task description fields -->

Vorm de basistaakinformatie:

* **naam van de Taak**: Ga een beschrijvende naam voor de taak in. Deze naam is zichtbaar voor u en uw team, maar wordt mogelijk niet weergegeven aan klanten, afhankelijk van het ontwerp van uw inhoudskaart.
* **beschrijving van de Taak**: (Facultatief) voeg details over het taakdoel of de vereisten toe.

### Klantenactiviteit kiezen {#choose-activity}

<!-- SCREENSHOT: Activity type selection showing Purchase and Spend options with radio buttons -->

Selecteer het type van klantenactiviteit dat de klanten moeten uitvoeren om deze taak te voltooien:

* **[!UICONTROL Purchase]**: Klanten moeten een of meer items aanschaffen om deze taak te voltooien
* **[!UICONTROL Spend]**: Klanten moeten een opgegeven bedrag besteden om deze taak te voltooien

Selecteer de klantenactiviteit die het best op uw resultaatdoelstellingen richt. Elk activiteitstype heeft specifieke configureerbare attributen om de taakvereisten verder te bepalen en te vormen.

### Kenmerken definiëren {#define-attributes}

<!-- SCREENSHOT: Attributes form for Purchase activity showing Quantity field, Eligible items & exclusions field, and parameters icon for optional attributes -->

Configureer de taakkenmerken op basis van het geselecteerde type activiteit:

+++Voor koopactiviteiten

Configureer de volgende kenmerken:

* **Aantal**: Ga het aantal punten in die moeten worden gekocht om deze taak te voltooien
* **In aanmerking komende punten &amp; uitsluitingen**: Bepaal punten of puntgroepen die naar taakvoltooiing en die tellen die niet. Leer meer over [&#x200B; het bepalen van in aanmerking komende punten en uitsluitingen &#x200B;](#eligible-items-exclusions)

**Facultatieve attributen** (vorm via het parameterpictogram):

* **Minimale uitgeeft waardebedrag**: Plaats een minimumvereiste van het aankoopbedrag
* **Maximum aantal transacties**: Beperk hoeveel transacties kunnen worden gebruikt om de taak te voltooien

+++

+++Voor bestedingsactiviteit

Configureer de volgende kenmerken:

* **Bedrag**: Ga het totale besteedbedrag in dat wordt vereist om de taak te voltooien
* **Maximum aantal transacties**: Specificeer hoeveel transacties worden toegestaan om aan het uitgavenvereiste te voldoen. U kunt dit kenmerk deactiveren via het parameterpictogram als u het aantal transacties niet wilt beperken
* **In aanmerking komende punten &amp; uitsluitingen**: (Facultatieve) Bepaal punten of puntgroepen die naar taakvoltooiing en die tellen die niet. Leer meer over [&#x200B; het bepalen van in aanmerking komende punten en uitsluitingen &#x200B;](#eligible-items-exclusions)

+++

Nadat u alle kenmerken hebt geconfigureerd, selecteert u **[!UICONTROL Create]** om de taak op te slaan. De taak wordt bewaard aan uw inventaris van Taken en, als gecreeerd van binnen een uitdaging, automatisch toegevoegd aan die uitdaging.

## In aanmerking komende items en uitsluitingen definiëren {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Voor zowel aankoop- als uitgavenactiviteiten kunt u in aanmerking komende objecten en groepen definiëren en items en groepen uitsluiten. Dit staat u toe om specifieke producten, categorieën, of plaatsen te richten aan uw uitdagingsdoelstellingen.

**gevallen van het Gebruik:**

* Maak een taak die klanten belont voor het aanschaffen van koffieartikelen, maar geen opruimingsproducten
* Een uitgaventaak beperken tot specifieke productcategorieën
* Kaarten of promotiepunten uitsluiten van aftellen naar voltooiing van een taak

### In aanmerking komende items configureren {#configure-eligible-items}

Gebruik de sectie **[!UICONTROL Eligible task purchases are limited to the following]** om in aanmerking komende items te definiëren:

* Geef specifieke item-id&#39;s, categorieën of doel-id&#39;s op, gescheiden door komma&#39;s
* Voorbeeld: `SKU001, SKU002, CategoryA, StoreLocation123`
* **Uiteinde**: Ga `*` binnen om alle aankopen (standaardgedrag als verlaten leeg) in aanmerking te laten komen

### Uitsluitingen configureren {#configure-exclusions}

Gebruik de sectie **[!UICONTROL The following are excluded from this task]** om items uit te sluiten van de taak:

* Voer specifieke item-id&#39;s, categorieën of doel-id&#39;s in die niet moeten worden meegenomen in de voltooiing van de taak
* Voorbeeld: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`
* Algemene uitsluitingen: verkoop- of opruimingsartikelen, cadeaukaarten, promotieartikelen

>[!NOTE]
>
>Uitsluitingen hebben voorrang op in aanmerking komende items. Als een item overeenkomt met zowel een in aanmerking komend als een uitgesloten item, wordt het van de taak uitgesloten.

## Volgende stappen {#next-steps}

Nu u weet om taken tot stand te brengen en te vormen:

* [&#x200B; creeer uitdagingen &#x200B;](create-challenges.md) - leer hoe te om volledige uitdagingen te bouwen en beloningen te vormen
* [&#x200B; beheert uitdagingen &#x200B;](manage-challenges.md) - Leer hoe te, uitdagingen uit te geven te controleren en te optimaliseren
