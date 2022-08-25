---
title: Aan de slag met Helper-functies
description: Journey Optimizer Helper-functiebibliotheek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 315c3e8c04b2e3944d0d5b2befb205acbe0ef7c9
workflow-type: tm+mt
source-wordcount: '1738'
ht-degree: 2%

---

# Aan de slag met Helper-functies{#functions}

Gebruiken [!DNL Journey Optimizer] sjabloontaal voor het uitvoeren van bewerkingen op gegevens, zoals berekeningen, gegevensopmaak of conversies, voorwaarden en het manipuleren ervan in de context van personalisatie. Meer informatie over richtlijnen voor de syntaxisaanpassing vindt u in [deze pagina](../personalization-syntax.md).

➡️ [Leer hoe u in deze video hulpfuncties kunt gebruiken](#video)

De taal van het malplaatje wordt leveraged in helperfuncties beschikbaar in verpersoonlijkingsdrop-down lijst van de redacteur van de Uitdrukking, zoals hieronder:

![](../assets/access-helper-functions.png)

In de [!DNL Journey Optimizer] De redacteur van de uitdrukking, helperfuncties worden gegroepeerd in drie categorieën: [Functies](#functions-helper), [Helpers](#helper-helper) en [Operatoren](#operators-helper).

Selecteer een categorie voor toegang tot subcategorieën en functies.

Toegang tot subcategorieën door op de knop `>` pictogram. Selecteer een functie door op de knop `+` pictogram: De functie wordt automatisch toegevoegd aan het verpersoonlijkingsscherm.

Klik op de knop `...` om de beschrijving van de functie weer te geven en deze aan uw favorieten toe te voegen. [Meer informatie](../personalize.md#fav)

## Functies{#functions-helper}

### Samenvoegings- en arrayfuncties

<table>
    <tr>
        <td><a href="aggregation.md#average">Gemiddelde</a></td><td>Deze functie retourneert het rekenkundig gemiddelde van alle geselecteerde waarden binnen de array</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Aantal</a></td><td>Deze functie retourneert het aantal elementen binnen de opgegeven array</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Alleen telling null</a></td><td>Deze functie telt het aantal ongeldige waarden in de lijst.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Tellen met null</a></td><td>Deze functie telt alle elementen van de lijst met inbegrip van ongeldige waarden</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Afzonderlijk</a></td><td>Deze functie haalt waarden op uit een array of een lijst met verwijderde dubbele waarden</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Aantal zonder onderscheid met null</a></td><td>Deze functie telt het aantal verschillende waarden inclusief de null-waarden</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Eerste object</a></td><td>Deze functie retourneert het eerste item in een array of lijst</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Eerste n in array</a></td><td>Deze functie retourneert de eerste 'N'-items in een array, indien gesorteerd in oplopende volgorde op basis van de opgegeven numerieke expressie</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In</a></td><td>Deze functie wordt gebruikt om te bepalen of een punt een lid van een serie of een lijst is</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Inclusief</a></td><td>Deze functie bepaalt of een array of lijst een bepaald item bevat</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Doorsnede</a></td><td>Deze functie bepaalt of twee arrays of lijsten ten minste één gemeenschappelijk lid hebben</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Laatste n in array</a></td><td>Deze functie retourneert de laatste 'N'-items in een array, indien gesorteerd in oplopende volgorde op basis van de opgegeven numerieke expressie</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a></td><td>Deze functie retourneert de grootste van alle geselecteerde waarden binnen een array</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimaal</a></td><td>Deze functie retourneert het kleinste van alle geselecteerde waarden binnen de array</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Niet in</a></td><td>Deze functie bepaalt of een item geen lid is van een array of lijst</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subset van</a></td><td>Deze functie bepaalt of een specifieke array (array A) een subset is van een andere array (array B), d.w.z. of alle elementen in array A elementen van array B zijn</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Som</a></td><td>Deze functie retourneert de som van alle geselecteerde waarden binnen de array</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset van</a></td><td>Deze functie bepaalt of een specifieke array (array A) een superset is van een andere array (array B), d.w.z. of die array A alle elementen in array B bevat</td>
    </tr>
</table>

### Datumtijdfuncties{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#age">Leeftijd</a></td><td>Deze functie haalt de leeftijd op van een bepaalde datum</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Huidige tijd in milliseconden</a></td><td>Deze functie haalt huidige tijd op in epoch millisecond</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Datumverschil</a></td><td>Deze functie haalt het verschil op tussen twee datums in aantal dagen</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Dag van de week</a></td><td>Deze functie haalt de dag van de week op</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Dag van het jaar</a></td><td>Deze functie haalt de dag van het jaar op</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Indelingsdatum</a></td><td>Deze functie formatteert een waarde van de datumtijd</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Dagen instellen</a></td><td>Deze functie stelt de dag van de maand in voor de opgegeven datum en tijd</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Uren instellen</a></td><td>Deze functie stelt het uur van de datum-tijd in</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">Naar UTC</a></td><td>Deze functie converteert een datetime naar UTC</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Week van het jaar</a></td><td>Deze functie retourneert de week van het jaar</td>
    </tr>
</table>
</table>

### Kaartfuncties {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Get</a></td><td>Deze functie wordt gebruikt om de waarde van een kaart voor een bepaalde sleutel terug te winnen</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Toetsen</a></td><td>Deze functie wordt gebruikt om alle sleutels voor een bepaalde kaart terug te winnen</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Waarden</a></td><td>Deze functie haalt alle waarden van een bepaalde kaart op</td>
    </tr>
</table>

### Wiskundige functies {#math-functions}

<table>
    <tr>
        <td><a href="objects.md#absolute">Absoluut</a></td><td>Deze functie converteert een getal dat de absolute waarde heeft</td>
    </tr>
    <tr>
        <td><a href="objects.md#random">Random</a></td><td>Deze functie retourneert een willekeurige waarde tussen 0 en 1</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-down">Omlaag afronden</a></td><td>Deze functie rondt een getal af</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-up">Omhoog afronden</a></td><td>Deze functie rondt een getal af</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-percentage">Naar percentage</a></td><td>Deze functie zet een getal om in een percentage</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-precision">Naar nauwkeurigheid</a></td><td>Deze functie converteert een getal naar de vereiste precisie</td>
    </tr>
</table>

### Objectfuncties {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Is niet null</a></td><td>Deze functie wordt gebruikt om te bepalen of een objecten verwijzing bestaat</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Is null</a></td><td>Deze functie wordt gebruikt om te bepalen of een objectverwijzing niet bestaat</td>
    </tr>
</table>

### Tekenreeksfuncties {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a></td><td>Deze functie wordt gebruikt om de eerste letter van elk woord van een tekenreeks met een hoofdletter te kapitaliseren</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>Deze functie wordt gebruikt om twee tekenreeksen te combineren tot één</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Bevat</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks een opgegeven subtekenreeks bevat</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Bevat niet</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks geen opgegeven subtekenreeks bevat</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Eindigt niet met</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks niet eindigt met een opgegeven subtekenreeks</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Begint niet met</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks niet begint met een opgegeven subtekenreeks</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Coderen 64</a></td><td>Deze functie wordt gebruikt om een tekenreeks te coderen of decoderen</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Ends with (Eindigt met)</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks eindigt met een opgegeven subtekenreeks</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Equals (Is gelijk aan)</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks niet begint met een opgegeven subtekenreeks, met hoofdlettergevoeligheid</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Gelijk aan hoofdletter negeren</a></td><td>Deze functie wordt gebruikt om te bepalen als een tekenreeks niet begint met een opgegeven subtekenreeks, zonder hoofdlettergevoeligheid</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">E-maildomein extraheren</a></td><td>Deze functie wordt gebruikt om het domein van een e-mailadres te extraheren</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">URL-host ophalen</a></td><td>Deze functie wordt gebruikt om url host op te halen.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">URL-pad ophalen</a></td><td>Deze functie wordt gebruikt om url path op te halen</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">URL-protocol ophalen</a></td><td>Deze functie wordt gebruikt om het URL-protocol op te halen</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">Index van</a></td><td>Deze functie retourneert de positie (in het eerste argument) van de eerste instantie van de tweede parameter. Retourneert -1 als er geen overeenkomst is</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Deze functie wordt gebruikt om te controleren of een tekenreeks of expressie leeg is.</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">Is niet leeg</a></td><td>Deze functie retourneert true als de tekenreeks in de parameter niet leeg is.</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">Laatste index van</a></td><td>Deze functie retourneert de positie (in het eerste argument) van de laatste instantie van de tweede parameter. Retourneert -1 als er geen overeenkomend actiepunt is.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Links bijsnijden</a></td><td>Deze functie verwijdert witruimten van het begin van een tekenreeks</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Length</a></td><td>Deze functie wordt gebruikt om het aantal tekens in een tekenreeks of expressie op te halen</td>
    </tr>
    <tr>
        <td><a href="string.md#like">leuk</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks overeenkomt met een opgegeven patroon</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Kleine letters</a></td><td>Deze functie converteert een tekenreeks naar kleine letters</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">Masker</a></td><td>Deze functie wordt gebruikt om een deel van een tekenreeks te vervangen door 'X'-tekens.</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Overeenkomsten</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks overeenkomt met een specifieke reguliere expressie</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>Deze functie retourneert md5 hash of input string.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Niet gelijk aan</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks niet gelijk is aan de opgegeven tekenreeks</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">Niet gelijk aan hoofdletter negeren</a></td><td>Deze functie vergelijkt twee tekenreeksen die hoofdletters en kleine letters negeren.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Groep met reguliere expressies</a></td><td>Deze functie wordt gebruikt om specifieke informatie te extraheren, gebaseerd op de gegeven reguliere expressie</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Replace</a></td><td>Deze functie vervangt een bepaalde subtekenreeks in een tekenreeks door een andere subtekenreeks</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Alles vervangen</a></td><td>Deze functie vervangt alle subtekenreeksen van een tekst die overeenkomt met "target" door de opgegeven letterlijke tekenreeks "replacement"</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Rechts bijsnijden</a></td><td>Deze functie verwijdert witruimten van het einde van een tekenreeks </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Splitsen</a></td><td>Deze functie wordt gebruikt om een tekenreeks te splitsen op een bepaald teken</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Starts with (Begint met)</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks begint met een opgegeven subtekenreeks</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">Tekenreeks naar datum</a></td><td>Deze functie wordt gebruikt om tekenreeks om te zetten in datum. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">Tekenreeks naar geheel getal</a></td><td>Deze functie converteert een tekenreekswaarde naar een geheel-getalwaarde.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">Tekenreeks naar nummer</a></td><td>Deze functie wordt gebruikt om een tekenreeks om te zetten in een getal. Deze geeft dezelfde tekenreeks als uitvoer voor ongeldige invoer.</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">Subtekenreeks</a></td><td>Deze functie retourneert de subtekenreeks van de tekenreeksexpressie tussen de beginindex en de eindindex.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Alles Beginhoofdletter</a></td><td>Deze functie wordt gebruikt om eerste letters van elk woord van een tekenreeks te kapitaliseren</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">Naar bool</a></td><td>Deze functie zet een argumentwaarde in een booleaanse waarde om, afhankelijk van het type.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">Tot op heden</a></td><td>Deze functie wordt gebruikt om tekenreeks om te zetten in datum. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">Alleen tijd tot op heden</a></td><td>Deze functie converteert een argumentwaarde naar een waarde die alleen voor de datumtijd geldt. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Verkleinen</a></td><td>Deze functie verwijdert witruimten van het begin en van het einde van een tekenreeks</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Hoofdletters</a></td><td>Deze functie converteert een tekenreeks naar hoofdletters</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">URL-decodering</a></td><td>Deze functie wordt gebruikt om een URL-gecodeerde tekenreeks te decoderen.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">URL-codering</a></td><td>Deze functie wordt gebruikt om een tekenreeks te coderen door url.</td>
    </tr>
</table>


## Helpers{#helper-helper}

Helpers worden gedetailleerd in [deze pagina](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">Standaardfallbackwaarde</a></td><td>Met deze functie kunt u een variabele met standaard renderen</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Elk</a></td><td>Deze functie wordt gebruikt om een array te doorlopen</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">Indien</a></td><td>Deze functie wordt gebruikt om een voorwaardelijk blok te bepalen - als de uitdrukkingsevaluatie waar terugkeert, wordt het blok teruggegeven</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Laat</a></td><td>Met deze functie kan een expressie worden opgeslagen als een variabele die later in een query moet worden gebruikt</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Tenzij</a></td><td>Deze functie wordt gebruikt om een voorwaardelijk blok te bepalen - als de uitdrukkingsevaluatie vals terugkeert, wordt het blok teruggegeven</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">Met</a></td><td>Deze functie wordt gebruikt om het evaluatietoken van template-part te veranderen</td>
    </tr>
</table>

## Operatoren{#operators-helper}

### Rekenkundige functies {#arithmetic-helper}

Rekenkundige functies worden gebruikt voor het uitvoeren van basisberekeningen op waarden.

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Toevoeging</a></td><td>Deze operator wordt gebruikt om de som van twee argumentexpressies te zoeken</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Verdelen</a></td><td>Deze operator wordt gebruikt om het quotiënt van twee argumentexpressies te vinden</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Vermenigvuldigen</a></td><td>Deze operator wordt gebruikt om het product van twee argumentexpressies te zoeken</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Herinnering</a> </td><td>Deze operator wordt gebruikt om de rest te zoeken na het delen van de twee argumentexpressies</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">Aftrekken</a> </td><td>Deze operator zoekt het verschil tussen twee expressies</td>
    </tr>
</table>


### Booleaanse functies {#boolean-functions}

Booleaanse functies worden gebruikt voor het uitvoeren van Booleaanse logica op verschillende elementen.

<table>
    <tr>
        <td><a href="operators.md#and">en</a></td><td>Deze operator maakt een logische verbinding</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">of</a></td><td>Deze operator maakt een logische scheiding</td>
    </tr>
</table>


### Vergelijkingsfuncties {#comparison-functions}

Vergelijkingsfuncties worden gebruikt om verschillende expressies en waarden met elkaar te vergelijken en om waar of onwaar overeenkomstig te retourneren.

<table>
    <tr>
        <td><a href="operators.md#equals">Equals (Is gelijk aan)</a></td><td>Deze bewerking controleert of de waarden gelijk zijn</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Greater than</a></td><td>Deze operator controleert of de eerste waarde groter is dan de tweede waarde</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Groter of gelijk aan</a></td><td>Deze operator controleert of de eerste waarde groter dan of gelijk is aan de tweede waarde</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Kleiner dan of gelijk aan</a> </td><td>Deze operator controleert of de eerste waarde kleiner dan of gelijk is aan de tweede waarde</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Niet gelijk aan</a></td><td>Deze operator controleert of de opgegeven expressie niet gelijk is aan de gegeven waarde</td>
    </tr>
</table>

## Hoe kan ik-video{#video}

Leer hoe u waarden voor personalisatie met hulpfuncties voor personalisatie kunt transformeren, en hoe u verschillende gebruiksscenario&#39;s voor hulpfuncties kunt begrijpen.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
