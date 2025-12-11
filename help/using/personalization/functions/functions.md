---
title: Aan de slag met Helper-functies
description: Journey Optimizer Helper-functiebibliotheek
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 8ca1c995bc38b110fa07573f922906c775fd5e6f
workflow-type: tm+mt
source-wordcount: '2434'
ht-degree: 1%

---

# Aan de slag met Helper-functies{#functions}

U kunt de sjabloontaal [!DNL Journey Optimizer] gebruiken om bewerkingen op gegevens uit te voeren, zoals berekeningen, gegevensopmaak of conversies, voorwaarden en deze te bewerken in de context van personalisatie. Leer de richtlijnen van de verpersoonlijkingssyntaxis op [&#x200B; deze pagina &#x200B;](../personalization-syntax.md).

➡️ [&#x200B; Leer hoe te om hulpfuncties in deze video te gebruiken &#x200B;](#video)

De taal van het malplaatje wordt leveraged in helperfuncties beschikbaar in verpersoonlijkingsdrop-down lijst van de verpersoonlijkingsredacteur, zoals hieronder:

![](../assets/access-helper-functions.png)

In de [!DNL Journey Optimizer] verpersoonlijkingsredacteur, helperfuncties worden gegroepeerd in drie categorieën: [&#x200B; Functies &#x200B;](#functions-helper), [&#x200B; Helpers &#x200B;](#helper-helper) en [&#x200B; Operatoren &#x200B;](#operators-helper).

Selecteer een categorie voor toegang tot subcategorieën en functies.

U kunt subcategorieën openen door op het pictogram `>` te klikken. Selecteer een functie door op het pictogram `+` te klikken: de functie wordt automatisch toegevoegd aan het verpersoonlijkingsscherm.

Klik op het pictogram `...` om de beschrijving van de functie weer te geven en deze aan uw favorieten toe te voegen. [Meer informatie](../personalize.md#fav)

>[!NOTE]
>
>De functies en de mogelijkheden beschikbaar in de verpersoonlijkingsredacteur verschillen van degenen beschikbaar in de [&#x200B; Reis geavanceerde uitdrukkingsredacteur &#x200B;](../../building-journeys/expression/expressionadvanced.md). De functie `now()` is bijvoorbeeld alleen beschikbaar in reisexpressies. [Meer informatie](../../email/code-content.md#date-time-limitations)

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
        <td><a href="arrays-list.md#in">In</a></td><td>Deze functie wordt gebruikt om te bepalen of een item lid is van een array of lijst</td>
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
        <td><a href="aggregation.md#min">Minimaal</a></td><td>Deze functie retourneert de kleinste geselecteerde waarden binnen de array</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Niet in</a></td><td>Deze functie bepaalt of een item geen lid is van een array of lijst</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subset van</a></td><td>Deze functie bepaalt of een specifieke array (array A) een subset is van een andere array (array B), dat wil zeggen of alle elementen in array A elementen van array B zijn</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Som</a></td><td>Deze functie retourneert de som van alle geselecteerde waarden binnen de array</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset van</a></td><td>Deze functie bepaalt of een specifieke array (array A) een superset is van een andere array (array B), dat wil zeggen of die array A alle elementen in array B bevat</td>
    </tr>
</table>

### Datumtijdfuncties{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#add-days">Dagen toevoegen</a></td><td>Deze functie past een bepaalde datum met een bepaald aantal dagen aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-hours">Uren toevoegen</a></td><td>Deze functie past een bepaalde datum met een gespecificeerd aantal uren aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-minutes">Minuten toevoegen</a></td><td>Deze functie past een bepaalde datum met een gespecificeerd aantal minuten aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-months">Maanden toevoegen</a></td><td>Deze functie past een bepaalde datum met een gespecificeerd aantal maanden aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-seconds">Seconden toevoegen</a></td><td>Deze functie past een bepaalde datum met een gespecificeerd aantal seconden aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-years">Jaren toevoegen</a></td><td>Deze functie past een bepaalde datum met een gespecificeerd aantal jaren aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age">Leeftijd</a></td><td>Deze functie haalt de leeftijd op van een bepaalde datum.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-days">Leeftijd in dagen</a></td><td>Deze functie berekent de leeftijd van een bepaalde datum in dagen, d.w.z. het aantal dagen dat is verstreken tussen de gegeven datum en de huidige datum, negatief voor toekomstige datums en positief voor vroegere datums.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-months">Leeftijd in maanden</a></td><td>Deze functie berekent de leeftijd van een bepaalde datum in maanden, d.w.z. het aantal maanden dat is verstreken tussen de gegeven datum en de huidige datum, negatief voor toekomstige datums en positief voor datums in het verleden.</td>
    </tr>
    <tr>
        <td><a href="dates.md#compare-dates">Datums vergelijken</a></td><td>Deze functie vergelijkt de eerste inputdatum met andere. Retourneert 0 als date1 gelijk is aan date2, -1 als date1 voor date2 komt en 1 als date1 na date2 komt.</td>
    </tr>
    <tr>
        <td><a href="dates.md#convert-zoned-date-time">ZonedDateTime converteren</a></td><td>Deze functie converteert een datum-tijd naar een bepaalde tijdzone.</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Huidige tijd in milliseconden</a></td><td>Deze functie haalt de huidige tijd in epoch milliseconds op.</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Datumverschil</a></td><td>Deze functie haalt het verschil tussen twee data in aantal dagen op.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-month">Dag van de maand</a></td><td>Deze functie retourneert het getal dat de dag van de maand vertegenwoordigt.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Dag van de week</a></td><td>Deze functie haalt de dag van de week op.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Dag van jaar</a></td><td>Deze functie haalt de dag van het jaar op.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-seconds">Binnen seconden diff</a></td><td>Deze functie retourneert het verschil tussen twee datums in seconden.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-hours">Uren extraheren</a></td><td>Deze functie extraheert de uurcomponent uit een opgegeven tijdstempel.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-minutes">Minuten extraheren</a></td><td>Deze functie extraheert de component minute uit een opgegeven tijdstempel.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-months">Maanden uitnemen</a></td><td>Deze functie extraheert de component month uit een opgegeven tijdstempel.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-seconds">Seconden extraheren</a></td><td>Deze functie extraheert de tweede component uit een opgegeven tijdstempel.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Indelingsdatum</a></td><td>Deze functie maakt een datumtijdwaarde op.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date-locale">Datumnotatie met ondersteuning voor landinstellingen</a></td><td>Deze functie maakt een datumtijdwaarde op in de corresponderende taalgevoelige representatie, d.w.z. in een gewenste landinstelling.</td>
    </tr>
    <tr>
        <td><a href="dates.md#get-current-zoned-date-time">Get CurrentZonedDateTime</a></td><td>Deze functie retourneert de huidige datum en tijd met informatie over de tijdzone.</td>
    </tr>
    <tr>
        <td><a href="dates.md#hours-difference">Verschil in uren</a></td><td>Deze functie retourneert het verschil tussen twee datums in termen van uren.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-minutes">Verschil in minuten</a></td><td>Deze functie retourneert het verschil tussen twee datums in minuten.</td>
    </tr>
    <tr>
        <td><a href="dates.md#months-difference">Verschil in maanden</a></td><td>Deze functie retourneert het verschil tussen twee datums in termen van maanden.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Dagen instellen</a></td><td>Deze functie stelt de dag van de maand in voor de opgegeven datum en tijd.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Uren instellen</a></td><td>Deze functie stelt het uur van de datum-tijd in.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-date-time">Tot op heden</a></td><td>Deze functie converteert string naar date. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">Naar UTC</a></td><td>Deze functie converteert een datetime naar UTC.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-day">Korten naar begin van dag</a></td><td>Deze functie wijzigt een bepaalde datum-tijd door het aan het begin van de dag te plaatsen met de tijd die aan 00:00 wordt geplaatst.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-quarter">truncateToStartOfQuarter</a></td><td>Deze functie verkort een datum-tijd tot de eerste dag van zijn kwart (b.v., Jan 1, Apr 1, jul 1, okt 1) om 00:00.
</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-week">truncateToStartOfWeek</a></td><td>Deze functie wijzigt een bepaalde datum-tijd door het aan het begin van de week (Maandag om 00:00) te plaatsen.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-year">truncateToStartOfYear</a></td><td>Deze functie wijzigt een bepaalde datum-tijd door het te beknotten aan de eerste dag van het jaar (Januari 1st) om 00:00.</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Week van jaar</a></td><td>Deze functie retourneert de week van het jaar</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-years">Verschil in jaren</a></td><td>Deze functie retourneert het verschil tussen twee datums in termen van jaren.</td>
    </tr>
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
        <td><a href="math.md#absolute">Absoluut</a></td><td>Deze functie formatteert om het even welk aantal in zijn taal-gevoelige vertegenwoordiging.</td>
    </tr>
    <tr>
        <td><a href="math.md#format-number">Indelingsnummer</a></td><td>Deze functie formatteert om het even welk aantal in zijn taal-gevoelige vertegenwoordiging.</td>
    </tr>
    <tr>
        <td><a href="math.md#random">Willekeurig</a></td><td>Deze functie retourneert een willekeurige waarde tussen 0 en 1</td>
    </tr>
    <tr>
        <td><a href="math.md#round-down">Omlaag afronden</a></td><td>Deze functie rondt een getal af</td>
    </tr>
    <tr>
        <td><a href="math.md#round-up">Omhoog afronden</a></td><td>Deze functie rondt een getal af</td>
    </tr>
    <tr>
    <td><a href="math.md#to-hex-string">Naar hexadecimale tekenreeks</a></td><td>Zet om het even welk aantal in zijn hexadecimale koord om.</td>
    </tr>
    <tr>
    <td><a href="math.md#to-int">ToInt</a></td><td>Zet om het even welk van deze types (aantal, dubbel, int, lang, vlotter, kort, byte, boolean, koord) in een geheel om.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-percentage">Naar percentage</a></td><td>Deze functie zet een getal om in een percentage</td>
    </tr>
    <tr>
        <td><a href="math.md#to-precision">Naar nauwkeurigheid</a></td><td>Deze functie converteert een getal naar de vereiste precisie</td>
    </tr>
    <tr>
        <td><a href="math.md#to-string">Naar tekenreeks</a></td><td>Deze functie converteert een willekeurig getal naar de tekenreeksrepresentatie. </td>
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

### Reeksfuncties {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a></td><td>Deze functie wordt gebruikt om de eerste letter van elk woord van een tekenreeks met een hoofdletter te kapitaliseren</td>
    </tr>
    <tr>
        <td><a href="string.md#char-code-at">Tekencode op</a></td><td>Deze functie retourneert ASCII-waarde van een teken, zoals de charCodeAt-functie in JavaScript</td>
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
        <td><a href="string.md#encode64">Coderen 64</a></td><td>Deze functie wordt gebruikt om een tekenreeks te coderen</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Eindigt met</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks eindigt met een opgegeven subtekenreeks</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Gelijk</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks niet begint met een opgegeven subtekenreeks, met hoofdlettergevoeligheid</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Gelijk aan hoofdletter negeren</a></td><td>Deze functie wordt gebruikt om te bepalen als een tekenreeks niet begint met een opgegeven subtekenreeks, zonder hoofdlettergevoeligheid</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">E-maildomein extraheren</a></td><td>Deze functie wordt gebruikt om het domein van een e-mailadres te extraheren</td>
    </tr>
    <tr>
        <td><a href="string.md#format-currency">Valuta opmaken</a></td><td>Deze functie converteert een willekeurig getal naar de corresponderende taalgevoelige valutarepresentatie, afhankelijk van de landinstelling die als tekenreeks is doorgegeven in het tweede argument</td>
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
        <td><a href="string.md#length">Lengte</a></td><td>Deze functie wordt gebruikt om het aantal tekens in een tekenreeks of expressie op te halen</td>
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
        <td><a href="string.md#not-equal-with-ignore-case">Niet gelijk aan hoofdletter negeren</a></td><td>Deze functie vergelijkt twee tekenreeksen die hoofdlettergebruik negeren.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Groep met reguliere expressies</a></td><td>Deze functie wordt gebruikt om specifieke informatie te extraheren, gebaseerd op de gegeven reguliere expressie</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Vervangen</a></td><td>Deze functie vervangt een bepaalde subtekenreeks in een tekenreeks door een andere subtekenreeks</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Alles vervangen</a></td><td>Deze functie vervangt alle subtekenreeksen van een tekst die overeenkomt met "target" door de opgegeven letterlijke tekenreeks "replacement"</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Rechts bijsnijden</a></td><td>Deze functie verwijdert witruimten van het einde van een tekenreeks </td>
    </tr>
    <tr>
        <td><a href="string.md#sha256">SHA256</a></td><td>Deze functie berekent en retourneert de sha256 hash van een tekenreeks.</td>
    </tr>
    <tr>
        <td><a href="string.md#split">Splitsen</a></td><td>Deze functie wordt gebruikt om een tekenreeks te splitsen op een bepaald teken</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Begint met</a></td><td>Deze functie wordt gebruikt om te bepalen of een tekenreeks begint met een opgegeven subtekenreeks</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">Tekenreeks naar datum</a></td><td>Deze functie converteert een tekenreekswaarde naar een datum-tijdwaarde</td>
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
        <td><a href="string.md#titleCase">Alles Beginhoofdletter</a></td><td>Deze functie wordt gebruikt om eerste letters van elk woord van een tekenreeks met hoofdletters te maken</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">Naar bool</a></td><td>Deze functie zet een argumentwaarde in een booleaanse waarde om, afhankelijk van het type.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">Tot op heden</a></td><td>Deze functie wordt gebruikt om tekenreeks om te zetten in datum. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">Alleen tijd tot op heden</a></td><td>Deze functie converteert een argumentwaarde naar een waarde die alleen voor de datumtijd kan worden gebruikt. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer.</td>
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

De helpers zijn gedetailleerd op [&#x200B; deze pagina &#x200B;](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">Standaardfallbackwaarde</a></td><td>Deze functie wordt gebruikt om een variabele met gebrek terug te geven</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Elk</a></td><td>Deze functie wordt gebruikt om een array te doorlopen</td>
    </tr>
    <tr>
        <td><a href="helpers.md#execution-metadata">Metagegevens van uitvoering</a></td><td>Met deze functie worden metagegevens van aangepaste sleutels en waarden vastgelegd tijdens het renderen van berichten, zodat deze kunnen worden opgeslagen in het metagegevensobject voor uitvoering van de runtime</td>
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
        <td><a href="arithmetic-functions.md#divide">Splitsen</a></td><td>Deze operator wordt gebruikt om het quotiënt van twee argumentexpressies te vinden</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Vermenigvuldigen</a></td><td>Deze operator wordt gebruikt om het product van twee argumentexpressies te zoeken</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder"> Herinnering </a> </td><td>Deze operator wordt gebruikt om de rest te zoeken na het delen van de twee argumentexpressies</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract"> Aftrekken </a> </td><td>Deze operator zoekt het verschil tussen twee expressies</td>
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
        <td><a href="operators.md#equals">Gelijk</a></td><td>Deze bewerking controleert of de waarden gelijk zijn</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Groter dan</a></td><td>Deze operator controleert of de eerste waarde groter is dan de tweede waarde</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Groter of gelijk aan</a></td><td>Deze operator controleert of de eerste waarde groter dan of gelijk is aan de tweede waarde</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal"> minder dan of evenaart aan </a> </td><td>Deze operator controleert of de eerste waarde kleiner dan of gelijk is aan de tweede waarde</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Niet gelijk aan</a></td><td>Deze operator controleert of de opgegeven expressie niet gelijk is aan de gegeven waarde</td>
    </tr>
</table>

## Hoe kan ik-video{#video}

Leer hoe u waarden voor personalisatie met hulpfuncties voor personalisatie kunt transformeren, en hoe u verschillende gebruiksscenario&#39;s voor hulpfuncties kunt begrijpen.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
