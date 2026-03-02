---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Ondersteunde functies in de expressieeditor
description: Leer welke personalisatie redacteursfuncties in Beslissingsbeheer (Offer Decisioning) worden gesteund.
badge: label="Verouderd" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
source-git-commit: 8dcac6e63f6a38874b3aff4996fc317e3606cb9b
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 5%

---

# Ondersteunde functies in de expressieeditor {#personalization-editor-supported-functions}

In het Beheer van het Besluit, bouwt u uitdrukkingen gebruikend de verpersoonlijkingsredacteur. U gebruikt deze editor met name wanneer:

* **het bepalen van aanbiedingsinhoud** - wanneer u [ vertegenwoordiging ](offer-library/add-representations.md) toevoegt en de aanbiedingsinhoud (beelden, tekst, verbindingen) personaliseert
* **Creërend besluitvormingsregels** - wanneer u [ verkiesbaarheid ](offer-library/creating-decision-rules.md) voor aanbiedingen bepaalt
* **de rangschikkende formules van de Bouw** - wanneer u [ het rangschikken formules ](ranking/create-ranking-formulas.md) creeert om aanbiedingen tot stand te brengen

De Offer Decisioning backend steunt slechts a **ondergroep** van de functies beschikbaar in de verpersoonlijkingsredacteur. Deze pagina bevat elke functie die u veilig kunt gebruiken. Breid elke sectie uit om de gesteunde exploitanten, helpers, en functies te zien.

## Lijst met ondersteunde functies {#supported-functions-list}

+++ Operatoren

* `+` `-` `*` `/` `%` (rekenkundig)
* `and` `or` `!` (logisch)
* `=` `!=` `>` `>=` `<` `<=` (vergelijking)

+++

+++ Helpers

* Elk
* Met
* Indien
* Tenzij
* Laat
* Standaardfallbackwaarde
* fragment
* datasetLookup
* externalDataLookup (Alpha)
* Inline
* URL
* Metagegevens van uitvoering
* valueAtPath

+++

+++ Reeksfuncties

| Weergavenaam | Interne naam |
|--------------|---------------|
| Kleine letters | lowerCase |
| Hoofdletters | upperCase |
| Camel case | camelCase |
| Alles Beginhoofdletter | titleCase |
| Verkleinen | trim |
| Links bijsnijden | leftTrim |
| Rechts bijsnijden | rightTrim |
| Is leeg | isEmpty |
| Gelijk aan hoofdletter negeren | equalsIgnoreCase |
| Niet gelijk aan hoofdletter negeren | notEqualWithIgnoreCase |
| Vervangen | replace |
| Alles vervangen | replaceAll |
| Concat | concat |
| Splitsen | split |
| Encode64 | encode64 |
| Lengte | lengte |
| MD5 | md5 |
| SHA256 | sha256 |
| leuk | leuk |
| Starts with (Begint met) | startWith |
| Begint niet met | doesNotStartWith |
| Ends with (Eindigt met) | endWith |
| Eindigt niet met | doesNotEndWith |
| Bevat | contains |
| Bevat niet | doesNotContain |
| Gelijk | equals |
| Niet gelijk aan | notEqualTo |
| Overeenkomsten | overeenkomsten |
| Groep met reguliere expressies | regexGroup |
| Tekenreeks naar nummer | stringToNumber |
| Tekenreeks naar datum | stringToDate |
| Tot op heden | toDateTime |
| Alleen tot op heden tijd | toDateTimeOnly |
| E-maildomein extraheren | extractEmailDomain |
| E-mailgebruikersnaam uitnemen | extractEmailGebruikersnaam |
| Is niet leeg | isNotEmpty |
| Index van | indexOf |
| Laatste index van | lastIndexOf |
| Subtekenreeks | substr |
| Naar bool | toBool |
| Tekenreeks naar geheel getal | string_to_integer |
| Masker | masker |
| Opmaakvaluta ophalen | formatCurrency |
| Unicode-waarde van teken ophalen | charCodeAt |
| QR-code voor willekeurige tekst ophalen | qrCode |

+++

+++ Array-, lijst- en instelfuncties

| Weergavenaam | Interne naam |
|--------------|---------------|
| Afzonderlijk | distinct |
| In | in |
| Niet in | notIn |
| Doorsnede | doorsnede |
| Subset van | subsetOf |
| Superset van | supersetOf |
| Inclusief | include |
| Sorteren en eerste N in array ophalen | topN |
| Laatste N in array sorteren en ophalen | bottomN |
| Eerste object | kop |
| Aantal | count |
| Som | sum |
| Gemiddelde | gemiddelde |
| Minimaal | min |
| Maximum | max |

+++

+++ Toewijzingsfuncties

| Weergavenaam | Interne naam |
|--------------|---------------|
| Get | get |
| Toetsen | toetsen |
| Waarden | waarden |

+++

+++ Objectfuncties

| Weergavenaam | Interne naam |
|--------------|---------------|
| Is null | isNull |
| Is niet null | isNotNull |

+++

+++ Math-functies

| Weergavenaam | Interne naam |
|--------------|---------------|
| Naar percentage | toPercentage |
| Omhoog afronden | roundUp |
| Omlaag afronden | roundDown |
| Naar precisie | toPrecision |
| Absoluut | absoluut |
| Willekeurig | random |
| Naar Hexadecimaal | toHexString |
| Nummer ophalen voor landinstelling | formatNumber |
| Naar tekenreeks | toString |
| Naar int | toInt |
| Tot lang | toLong |

+++

+++ Datumtijdfuncties

| Weergavenaam | Interne naam |
|--------------|---------------|
| Nu | now |
| Get CurrentZonedDateTime | getCurrentZonedDateTime |
| Tot op heden | toDate |
| Naar tijd | toTime |
| Tot op heden | toDateTime |
| Alleen tot op heden tijd | toDateTimeOnly |
| Alleen tot op heden | toDateOnly |
| Alleen naar tijd | toTimeOnly |
| Naar tijdzone | toTimeZone |
| Indelingsdatum | formatDate |
| Datumnotatie | formatDateTime |
| Opmaaktijd | formatTime |
| Parseerdatum | parseDate |
| Tijdstip parsdatum | parseDateTime |
| Parseertijd | parseTime |
| Dagen toevoegen | addDays |
| Maanden toevoegen | addMonths |
| Jaren toevoegen | addYear |
| Uren toevoegen | addHours |
| Minuten toevoegen | addMinutes |
| Seconden toevoegen | addSeconds |
| Dagen aftrekken | subtractDays |
| Maanden verwijderen | subtractMonths |
| Jaren aftrekken | subtractYars |
| Uren verwijderen | subtractHours |
| Minuten verwijderen | subtractMinutes |
| Seconden verwijderen | subtractSecond |
| Verschil in dagen | diffDays |
| Verschil in maanden | diffMonths |
| Verschil in jaren | diffYaren |
| Verschil in uren | diffHours |
| Verschil in minuten | diffMinutes |
| Verschil in seconden | diffSeconds |
| Begin van dag | startOfDay |
| Einde van dag | endOfDay |
| Is voor | isBefore |
| Is na | isAfter |

+++

+++ URL-functies

| Weergavenaam | Interne naam |
|--------------|---------------|
| URL coderen | encodeUrl |
| URL decoderen | decodeUrl |
| URL-queryparam ophalen | getUrlQueryParam |
| URL-protocol ophalen | getUrlProtocol |
| URL-host ophalen | getUrlHost |

+++

>[!NOTE]
>
>Als u een functie gebruikt die niet in de bovenstaande lijst staat, kan de expressie mislukken bij uitvoering of onverwachte resultaten opleveren. Voor de volledige reeks functies beschikbaar in [!DNL Journey Optimizer] verpersoonlijking, zie [ de functielijst van de Helper ](../personalization/functions/functions.md). Alleen de subset die op deze pagina wordt beschreven, wordt ondersteund in Offer Decisioning.
