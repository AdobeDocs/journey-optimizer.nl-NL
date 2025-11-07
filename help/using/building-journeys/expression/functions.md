---
solution: Journey Optimizer
product: journey optimizer
title: Functies
description: Meer informatie over functies in reisexpressies
feature: Journeys
role: Developer
level: Experienced
keywords: functie, expressies, editor, reis, gegevens, manipulatie
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 99053c6c1327818645adc4ab9a5d3dd30eb96b87
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 7%

---

# Functies {#functions}

Functies zijn de bouwstenen van dynamische reisexpressies in Adobe Journey Optimizer. Zij laten u toe om gegevens in real time om te zetten, te berekenen, te bevestigen en te manipuleren om gepersonaliseerde klantenervaringen tot stand te brengen. Met meer dan 60 functies die in intuïtieve categorieën worden georganiseerd, kunt u geavanceerde voorwaarden bouwen, complexe berekeningen uitvoeren, en gegeven-gedreven besluiten bij elke stap van de klantenreis nemen.

## Functies begrijpen

Functies in reisexpressies volgen een consistent syntaxispatroon:

`<function name>` (`<expression as param 1>`, `<expression as param 2>` , ...,`<expression as param N>`)

**Zeer belangrijke kenmerken:**

* **Veelvoudige handtekeningen**: Een functie kan verschillende handtekeningen (verschillende reeksen bevolen parameters) hebben om diverse gebruiksgevallen aan te passen
* **Type-specifieke winst**: Elke functie heeft een specifiek teruggekeerd type (koord, geheel, boolean, datum, lijst, enz.)
* **Nul aan de parameters van N**: De functies kunnen uitdrukkingen 0-N als bevolen parameters goedkeuren, die flexibiliteit in verstrekken hoe u hen gebruikt

## Waarom functies gebruiken?

Met functies kunt u:

* **creeer dynamische voorwaarden** - de rijwegen van de tak die op gegevensevaluatie in real time worden gebaseerd
* **Personaliseer bij schaal** - de inhoud en de ervaringen van de Klantengegevens en gedragsinzichten gebruiken
* **Automatiseer besluiten** - bouw intelligente logica zonder handinterventie
* **de gegevens van de Transformatie** - zet, formatteert, en manipuleert gegevenstypes om verenigbaarheid te verzekeren
* **voer berekeningen** uit - voer wiskundige verrichtingen en statistische analyse uit
* **bevestigt input** - de kwaliteit en de volledigheid van de gegevens van de controle alvorens actie te voeren

## Functies per categorie

Blader door functies die door hun primaire doel worden georganiseerd om snel het juiste gereedschap voor uw behoeften te vinden.

### Adobe Experience Platform {#aep-functions}

**segmentatie van het publiek en het richten**

Evalueer publiekslidmaatschap om persoonlijke reiswegen tot stand te brengen die op klantensegmenten worden gebaseerd die in Adobe Experience Platform worden bepaald.

| Functie | Beschrijving |
|----------|-------------|
| [&#x200B; inAudience &#x200B;](../functions/functioninaudience.md) | Controleren of een individu tot een bepaald publiek behoort |

[Adobe Experience Platform-functiedetails weergeven →](../functions/functioninaudience.md)

### Samenvoegingsfuncties {#aggregation-functions}

**Statistische berekeningen en gegevenssamenvatting**

Berekenen van sets waarden om inzichten af te leiden, zoals gemiddelden, tellingen, sommen en min/max-waarden. Essentieel voor gegevensgestuurde besluitvorming.

| Functie | Beschrijving |
|----------|-------------|
| [avg](../functions/aggregation-functions.md#avg) | Gemiddelde waarde berekenen |
| [count](../functions/aggregation-functions.md#count) | Elementen tellen die niet null zijn |
| [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) | Alleen null-waarden tellen |
| [countWithNull](../functions/aggregation-functions.md#countWithNull) | Alle elementen tellen, inclusief null |
| [distinctCount](../functions/aggregation-functions.md#distinctCount) | Unieke waarden tellen die niet gelijk zijn aan null |
| [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) | Unieke waarden tellen inclusief null |
| [max](../functions/aggregation-functions.md#max) | Maximumwaarde zoeken |
| [min](../functions/aggregation-functions.md#min) | Minimumwaarde zoeken |
| [sum](../functions/aggregation-functions.md#sum) | Totaalbedrag berekenen |

[Alle aggregatiefuncties weergeven →](../functions/aggregation-functions.md)

### Conversiefuncties {#conversion-functions}

**het type van Gegevens transformatie**

Zet gegevens tussen verschillende types (koord, geheel, decimaal, boolean, datum, duur) om verenigbaarheid over verrichtingen en gegevensbronnen te verzekeren.

| Functie | Beschrijving |
|----------|-------------|
| [toBool](../functions/conversion-functions.md#toBool) | Omzetten in Boolean |
| [&#x200B; toDateOnly &#x200B;](../functions/conversion-functions.md#toDateOnly) | Converteren naar alleen datum (geen tijd) |
| [toDateTime](../functions/conversion-functions.md#toDateTime) | Omzetten in datum met tijd |
| [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) | Converteren naar datum en tijd zonder tijdzone |
| [toDecimal](../functions/conversion-functions.md#toDecimal) | Omzetten in decimaal getal |
| [toDuration](../functions/conversion-functions.md#toDuration) | Omzetten in duur |
| [toInteger](../functions/conversion-functions.md#toInteger) | Omzetten in geheel getal |
| [toString](../functions/conversion-functions.md#toString) | Omzetten in tekenreeks |

[Alle conversiefuncties weergeven →](../functions/conversion-functions.md)

### Datumfuncties {#date-functions}

**manipulatie van de Datum en van de tijd**

Werk met datums, tijden en tijdzones om op tijd gebaseerde voorwaarden te maken, acties te plannen en tijdelijke berekeningen uit te voeren.

| Functie | Beschrijving |
|----------|-------------|
| [&#x200B; currentTimeInMillis &#x200B;](../functions/date-functions.md#currentTimeInMillis) | Huidige tijd in milliseconden ophalen |
| [inLastDays](../functions/date-functions.md#inLastDays) | Controleren of de datum in de laatste N dagen valt |
| [inLastHours](../functions/date-functions.md#inLastHours) | Controleren of de datum binnen de laatste N uur valt |
| [inLastMonths](../functions/date-functions.md#inLastMonths) | Controleren of de datum binnen de laatste N maanden valt |
| [inLastYears](../functions/date-functions.md#inLastYears) | Controleren of de datum binnen de laatste N jaar valt |
| [inNextDays](../functions/date-functions.md#inNextDays) | Controleren of de datum binnen N dagen valt |
| [inNextHours](../functions/date-functions.md#inNextHours) | Controleren of de datum binnen de volgende N uur valt |
| [inNextMonths](../functions/date-functions.md#inNextMonths) | Controleren of de datum binnen de volgende N maanden valt |
| [inNextYears](../functions/date-functions.md#inNextYears) | Controleren of de datum binnen de volgende N jaar valt |
| [now](../functions/date-functions.md#now) | Huidige datum-tijd ophalen |
| [nowWithDelta](../functions/date-functions.md#nowWithDelta) | Huidige tijd ophalen met verschuiving |
| [setHours](../functions/date-functions.md#setHours) | Specifieke uren in datumtijd instellen |
| [setDays](../functions/date-functions.md#setDays) | Specifieke dagen in datumtijd instellen |
| [&#x200B; updateTimeZone &#x200B;](../functions/date-functions.md#updateTimeZone) | Tijdzone van datum-tijd bijwerken |

[Alle datumfuncties weergeven →](../functions/date-functions.md)

### Lijstfuncties {#list-functions}

**manipulatie en analyse van de Inzameling**

U kunt arrays en lijsten filteren, sorteren, transformeren en analyseren om met complexe gegevensstructuren te werken en ingestelde bewerkingen uit te voeren.

| Functie | Beschrijving |
|----------|-------------|
| [distinct](../functions/list-functions.md#distinct) | Unieke waarden ophalen (exclusief null) |
| [distinctWithNull](../functions/list-functions.md#distinctWithNull) | Unieke waarden ophalen (inclusief null) |
| [&#x200B; filter &#x200B;](../functions/list-functions.md#filter) | Filterlijst op basis van criteria |
| [getListItem](../functions/list-functions.md#getListItem) | Item ophalen bij specifieke index |
| [in](../functions/list-functions.md#in) | Controleren of de waarde bestaat in de lijst |
| [&#x200B; snijdt &#x200B;](../functions/list-functions.md#intersect) | Gemeenschappelijke elementen tussen lijsten zoeken |
| [&#x200B; grens &#x200B;](../functions/list-functions.md#limit) | Aantal geretourneerde items beperken |
| [listSize](../functions/list-functions.md#listSize) | Grootte van lijst ophalen |
| [serializeList](../functions/list-functions.md#serializeList) | Lijst omzetten in tekenreeks |
| [sort](../functions/list-functions.md#sort) | Lijstelementen sorteren |

[Alle lijstfuncties weergeven →](../functions/list-functions.md)

### Math-functies {#math-functions}

**Wiskundige verrichtingen**

Numerieke berekeningen en transformaties uitvoeren voor gegevensverwerking en bedrijfslogica.

| Functie | Beschrijving |
|----------|-------------|
| [random](../functions/math-functions.md#random) | Willekeurig getal genereren (0-1) |
| [round](../functions/math-functions.md#round) | Rond naar dichtstbijzijnd geheel getal |

[Alle wiskundige functies weergeven →](../functions/math-functions.md)

### Reeksfuncties {#string-functions}

**manipulatie en bevestiging van de Tekst**

Tekstgegevens verwerken, transformeren, zoeken en valideren voor het maken van dynamische inhoud en voorwaardelijke logica.

| Functie | Beschrijving |
|----------|-------------|
| [concat](../functions/string-functions.md#concat) | Tekenreeksen samenvoegen |
| [contain](../functions/string-functions.md#contain) | Controleren of een tekenreeks een subtekenreeks bevat |
| [&#x200B; containIgnoreCase &#x200B;](../functions/string-functions.md#containIgnoreCase) | Controle bevat (hoofdlettergevoelig) |
| [endWith](../functions/string-functions.md#endWith) | Controleren of tekenreeks eindigt met achtervoegsel |
| [&#x200B; endWithIgnoreCase &#x200B;](../functions/string-functions.md#endWithIgnoreCase) | Einden controleren met (hoofdlettergevoelig) |
| [&#x200B; equalIgnoreCase &#x200B;](../functions/string-functions.md#equalIgnoreCase) | Tekenreeksen vergelijken (hoofdlettergevoelig) |
| [indexOf](../functions/string-functions.md#indexOf) | Eerste voorvalpositie zoeken |
| [isEmpty](../functions/string-functions.md#isEmpty) | Controleren of tekenreeks leeg is |
| [isNotEmpty](../functions/string-functions.md#isNotEmpty) | Controleren of tekenreeks niet leeg is |
| [lastIndexOf](../functions/string-functions.md#lastIndexOf) | Laatste voorvalpositie zoeken |
| [length](../functions/string-functions.md#length) | Tekenlengte ophalen |
| [lower](../functions/string-functions.md#lower) | Omzetten in kleine letters |
| [matchRegExp](../functions/string-functions.md#matchRegExp) | Reguliere expressie afstemmen |
| [&#x200B; notEqualIgnoreCase &#x200B;](../functions/string-functions.md#notEqualIgnoreCase) | Inschakelen is niet gelijk (hoofdlettergevoelig) |
| [replace](../functions/string-functions.md#replace) | Eerste instantie vervangen |
| [replaceAll](../functions/string-functions.md#replaceAll) | Alle vermeldingen vervangen |
| [split](../functions/string-functions.md#split) | Tekenreeks splitsen in array |
| [startWith](../functions/string-functions.md#startWith) | Controleren of tekenreeks begint met voorvoegsel |
| [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) | Controle begint met (hoofdlettergevoelig) |
| [substr](../functions/string-functions.md#substr) | Subtekenreeks extraheren |
| [trim](../functions/string-functions.md#trim) | Voorloopspaties/volgspaties verwijderen |
| [upper](../functions/string-functions.md#upper) | Omzetten in hoofdletters |
| [uuid](../functions/string-functions.md#uuid) | UUID genereren |

[Alle tekenreeksfuncties weergeven →](../functions/string-functions.md)

## Volgende stappen

Nu u de beschikbare functies begrijpt, verkent u:

* **[Geavanceerde uitdrukkingsredacteur](expressionadvanced.md)** - Leer hoe te om complexe uitdrukkingen te bouwen gebruikend de geavanceerde redacteur
* **[syntaxis van de Uitdrukking](generalities.md)** - Meester de syntaxisregels voor het schrijven van reisuitdrukkingen
* **[Exploitanten](operators.md)** - ontdekt exploitanten u met functies kunt gebruiken om logica te bouwen
* **[verwijzingen van het Gebied](field-references.md)** - begrijp hoe te om gegevensgebieden in uw uitdrukkingen van verwijzingen te voorzien
