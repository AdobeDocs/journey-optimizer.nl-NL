---
title: String-functies, bibliotheek
description: String-functies, bibliotheek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 1f16b095b3b063f3fb881aee0b2a928644e19143
workflow-type: tm+mt
source-wordcount: '1859'
ht-degree: 3%

---

# Reeksfuncties {#string}

Leer hoe te om de functies van het Koord in de verpersoonlijkingsredacteur te gebruiken.

## Camel Case {#camelCase}

De functie `camelCase` maakt een hoofdletter van de eerste letter van elk woord van een tekenreeks.

**Syntaxis**

```sql
{%= camelCase(string)%}
```

**Voorbeeld**

Met de volgende functie krijgt de eerste letter van het woord een hoofdletter in het adres van het profiel.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Tekencode op {#char-code-at}

De functie `charCodeAt` retourneert ASCII-waarde van een teken, zoals de functie charCodeAt in JavaScript. Er wordt een tekenreeks en een geheel getal gebruikt (de positie van het teken wordt gedefinieerd) als invoerargumenten en de bijbehorende ASCII-waarde wordt geretourneerd.

**Syntaxis**

```sql
{%= charCodeAt(string,int) %}: int
```

**Voorbeeld**

De volgende functie retourneert de ASCII-waarde van o, d.w.z. 111.

```sql
{%= charCodeAt("some", 1)%}
```

## Concat {#concate}

De functie `concat` combineert twee tekenreeksen in één.

**Syntaxis**

```sql
{%= concat(string,string) %}
```

**Voorbeeld**

De volgende functie combineert profielstad en land in één tekenreeks.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Bevat {#contains}

De functie `contains` wordt gebruikt om te bepalen of een tekenreeks een opgegeven subtekenreeks bevat.

**Syntaxis**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `STRING_1` | De tekenreeks die de controle moet uitvoeren. |
| `STRING_2` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `CASE_SENSITIVE` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. Mogelijke waarden: true (standaard) / false. |

**Voorbeelden**

* De volgende functie controleert of de voornaam van het profiel de letter A bevat (in hoofdletters of kleine letters). Als dit het geval is, zal het &quot;waar&quot; terugkeren, anders zal het &quot;onwaar&quot; terugkeren.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* De volgende query bepaalt, met hoofdlettergevoeligheid, of het e-mailadres van de persoon de tekenreeks &quot;2010@gm&quot; bevat.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

## Bevat niet{#doesNotContain}

De functie `doesNotContain` wordt gebruikt om te bepalen of een tekenreeks geen opgegeven subtekenreeks bevat.

**Syntaxis**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `STRING_1` | De tekenreeks die de controle moet uitvoeren. |
| `STRING_2` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `CASE_SENSITIVE` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. Mogelijke waarden: true (standaard) / false. |

**Voorbeeld**

De volgende query bepaalt, met hoofdlettergevoeligheid, of het e-mailadres van de persoon niet de tekenreeks &quot;2010@gm&quot; bevat.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## Eindigt niet met{#doesNotEndWith}

De functie `doesNotEndWith` wordt gebruikt om te bepalen of een tekenreeks niet eindigt met een opgegeven subtekenreeks.

**Syntaxis**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `{CASE_SENSITIVE}` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. Mogelijke waarden: true (standaard) / false. |

**Voorbeeld**

De volgende query bepaalt, met hoofdlettergevoeligheid, of het e-mailadres van de persoon niet eindigt met &quot;.com&quot;.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Begint niet met{#doesNotStartWith}

De functie `doesNotStartWith` wordt gebruikt om te bepalen of een tekenreeks niet begint met een opgegeven subtekenreeks.

**Syntaxis**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `{CASE_SENSITIVE}` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. Mogelijke waarden: true (standaard) / false. |

**Voorbeeld**

De volgende query bepaalt, met hoofdlettergevoeligheid, of de naam van de persoon niet begint met &quot;Joe&quot;.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Coderen 64{#encode64}

De functie `encode64` wordt gebruikt om een tekenreeks te coderen om Personal Information (PI) te behouden als deze bijvoorbeeld in een URL moet worden opgenomen.

**Syntaxis**

```sql
{%= encode64(string) %}
```

## Eindigt met{#endsWith}

De functie `endsWith` wordt gebruikt om te bepalen of een tekenreeks eindigt met een opgegeven subtekenreeks.

**Syntaxis**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `{CASE_SENSITIVE}` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. Mogelijke waarden: true (standaard) / false. |

**Voorbeeld**

De volgende query bepaalt, met hoofdlettergevoeligheid, of het e-mailadres van de persoon eindigt met &quot;.com&quot;.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## Gelijk{#equals}

De functie `equals` wordt gebruikt om te bepalen of een tekenreeks gelijk is aan de opgegeven tekenreeks, met hoofdlettergevoeligheid.

**Syntaxis**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die met de eerste tekenreeks moet worden vergeleken. |

**Voorbeeld**

De volgende vraag bepaalt, met gevalgevoeligheid, als de naam van de persoon &quot;John&quot;is.

```sql
{%=equals(profile.person.name,"John") %}
```

## Gelijk aan hoofdletter negeren{#equalsIgnoreCase}

De functie `equalsIgnoreCase` wordt gebruikt om te bepalen of een tekenreeks gelijk is aan de opgegeven tekenreeks, zonder hoofdlettergevoeligheid.

**Syntaxis**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die met de eerste tekenreeks moet worden vergeleken. |

**Voorbeeld**

De volgende vraag bepaalt, zonder gevalgevoeligheid, als de naam van de persoon &quot;John&quot;is.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## E-maildomein extraheren {#extractEmailDomain}

De functie `extractEmailDomain` wordt gebruikt om het domein van een e-mailadres te extraheren.

**Syntaxis**

```sql
{%= extractEmailDomain(string) %}
```

**Voorbeeld**

De volgende query extraheert het e-maildomein van het persoonlijke e-mailadres.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Valuta opmaken {#format-currency}

De functie `formatCurrency` wordt gebruikt om een willekeurig getal om te zetten in de corresponderende taalgevoelige valutarepresentatie, afhankelijk van de landinstelling die als een tekenreeks in het tweede argument is doorgegeven.

**Syntaxis**

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Voorbeeld**

Deze query retourneert £ 56,00

```sql
{%= formatCurrency(56L,"en_GB") %}
```

## URL-host ophalen {#get-url-host}

De functie `getUrlHost` wordt gebruikt om de hostnaam van een URL op te halen.

**Syntaxis**

```sql
{%= getUrlHost(string) %}: string
```

**Voorbeeld**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Retourneert &quot;www.myurl.com&quot;

## URL-pad ophalen {#get-url-path}

De functie `getUrlPath` wordt gebruikt om het pad na de domeinnaam van een URL op te halen.

**Syntaxis**

```sql
{%= getUrlPath(string) %}: string
```

**Voorbeeld**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Retourneert &quot;/contact.html&quot;

## URL-protocol ophalen {#get-url-protocol}

De functie `getUrlProtocol` wordt gebruikt om het protocol van een URL terug te winnen.

**Syntaxis**

```sql
{%= getUrlProtocol(string) %}: string
```

**Voorbeeld**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Retourneert &quot;http&quot;

## Index van {#index-of}

De functie `indexOf` wordt gebruikt om de positie (in het eerste argument) van de eerste instantie van de tweede parameter te retourneren. Retourneert -1 als er geen overeenkomend actiepunt is.

**Syntaxis**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die moet worden gezocht in de eerste parameter |

**Voorbeeld**

```sql
{%= indexOf("hello world","world" ) %}
```

Retourneert 6.

## Is leeg {#isEmpty}

De functie `isEmpty` wordt gebruikt om te bepalen of een tekenreeks leeg is.

**Syntaxis**

```sql
{%= isEmpty(string) %}
```

**Voorbeeld**

De volgende functie retourneert &#39;true&#39; als het mobiele telefoonnummer van het profiel leeg is. Anders wordt &#39;false&#39; geretourneerd.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Is niet leeg {#is-not-empty}

De functie `isNotEmpty` wordt gebruikt om te bepalen of een tekenreeks niet leeg is.

**Syntaxis**

```sql
{= isNotEmpty(string) %}: boolean
```

**Voorbeeld**

De volgende functie retourneert &#39;true&#39; als het mobiele telefoonnummer van het profiel niet leeg is. Anders wordt &#39;false&#39; geretourneerd.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## Laatste index van {#last-index-of}

De functie `lastIndexOf` wordt gebruikt om de positie (in het eerste argument) van de laatste instantie van de tweede parameter te retourneren. Retourneert -1 als er geen overeenkomend actiepunt is.

**Syntaxis**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die moet worden gezocht in de eerste parameter |

**Voorbeeld**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Retourneert 7.

## Links bijsnijden {#leftTrim}

De functie `leftTrim` wordt gebruikt om witruimten te verwijderen uit het begin van een tekenreeks.

**Syntaxis**

```sql
{%= leftTrim(string) %}
```

## Lengte {#length}

De functie `length` wordt gebruikt om het aantal tekens in een tekenreeks of expressie op te halen.

**Syntaxis**

```sql
{%= length(string) %}
```

**Voorbeeld**

De volgende functie retourneert de lengte van de stadsnaam van het profiel.

```sql
{%= length(profile.homeAddress.city) %}
```

## leuk{#like}

De functie `like` wordt gebruikt om te bepalen of een tekenreeks overeenkomt met een opgegeven patroon.

**Syntaxis**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De expressie die moet overeenkomen met de eerste tekenreeks. Er zijn twee ondersteunde speciale tekens voor het maken van een expressie: `%` en `_` . <ul><li>`%` wordt gebruikt om nul of meer tekens te vertegenwoordigen.</li><li>`_` wordt gebruikt om precies één teken te vertegenwoordigen.</li></ul> |

**Voorbeeld**

Met de volgende query worden alle steden opgehaald waar profielen met het patroon &quot;es&quot; leven.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Kleine letters{#lower}

De functie `lowerCase` zet een tekenreeks om in kleine letters.

**Syntaxis**

```sql
{%= lowerCase(string) %}
```

**Voorbeeld**

Deze functie converteert de voornaam van het profiel naar kleine letters.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## Overeenkomsten{#matches}

De functie `matches` wordt gebruikt om te bepalen of een tekenreeks overeenkomt met een specifieke reguliere expressie. Gelieve te verwijzen naar [&#x200B; dit document &#x200B;](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) voor meer informatie over passende patronen in regelmatige uitdrukkingen.

**Syntaxis**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Voorbeeld**

De volgende vraag bepaalt, zonder case gevoeligheid, als de naam van de persoon met &quot;John&quot;begint.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Masker {#mask}

De functie `Mask` wordt gebruikt om een deel van een tekenreeks te vervangen door &#39;X&#39;-tekens.

**Syntaxis**

```sql
{%= mask(string,integer,integer) %}
```

**Voorbeeld**

De volgende query vervangt de tekenreeks &quot;123456789&quot; door &quot;X&quot;, behalve voor het eerste en laatste 2 tekens.

```sql
{%= mask("123456789",1,2) %}
```

De query retourneert `1XXXXXX89` .

## MD5 {#md5}

De functie `md5` wordt gebruikt om de md5-hash van een tekenreeks te berekenen en te retourneren.

**Syntaxis**

```sql
{%= md5(string) %}: string
```

**Voorbeeld**

```sql
{%= md5("hello world") %}
```

Retourneert &quot;5eb63be01eeed093cb22bb8f5acdc3&quot;

## Niet gelijk aan{#notEqualTo}

De functie `notEqualTo` wordt gebruikt om te bepalen of een tekenreeks niet gelijk is aan de opgegeven tekenreeks.

**Syntaxis**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die met de eerste tekenreeks moet worden vergeleken. |

**Voorbeeld**

De volgende vraag bepaalt, met case gevoeligheid, als de naam van de persoon niet &quot;John&quot; is.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Niet gelijk aan hoofdletter negeren {#not-equal-with-ignore-case}

De functie `notEqualWithIgnoreCase` wordt gebruikt om twee tekenreeksen te vergelijken die case negeren.

**Syntaxis**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die met de eerste tekenreeks moet worden vergeleken. |

**Voorbeeld**

De volgende query bepaalt of de naam van de persoon geen john is, zonder hoofdlettergevoeligheid.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## Groep met reguliere expressies{#regexGroup}

De functie `Group` wordt gebruikt om specifieke informatie te extraheren, gebaseerd op de reguliere expressie die wordt opgegeven.

**Syntaxis**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING}` | De tekenreeks die de controle moet uitvoeren. |
| `{EXPRESSION}` | De reguliere expressie die moet overeenkomen met de eerste tekenreeks. |
| `{GROUP}` | Expressiegroep die moet worden gebruikt. |

**Voorbeeld**

De volgende query wordt gebruikt om de domeinnaam uit een e-mailadres te extraheren.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## Vervangen {#replace}

De functie `replace` wordt gebruikt om een bepaalde subtekenreeks in een tekenreeks te vervangen door een andere subtekenreeks.

**Syntaxis**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks waar de subtekenreeks moet worden vervangen. |
| `{STRING_2}` | The substring to replace. |
| `{STRING_3}` | De vervangende subtekenreeks. |

**Voorbeeld**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Retourneert &quot;Hello Mark, hier is je maandelijkse nieuwsbrief!&quot;

## Alles vervangen{#replaceAll}

De functie `replaceAll` wordt gebruikt om alle subtekenreeksen van een tekst te vervangen die overeenkomt met de expressie &quot;regex&quot; met de opgegeven letterlijke tekenreeks &quot;replacement&quot;. Regex hanteert een speciale afhandeling van &quot;\&quot; en &quot;+&quot; en alle regex-expressies volgen de PQL-escaperestrategie. De vervanging vindt plaats vanaf het begin van de tekenreeks tot het einde. Als u bijvoorbeeld &quot;aa&quot; vervangt door &quot;b&quot; in de tekenreeks &quot;aaa&quot;, resulteert dit in &quot;ba&quot; in plaats van &quot;ab&quot;.

**Syntaxis**

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Wanneer de uitdrukking die als tweede argument wordt genomen een speciaal regex karakter is, gebruik dubbele backslash (`//`).  Speciale regex-tekens zijn: [., +, *, ?, ^, $, (, ), [, ], {, }, |, \.]
> 
> Leer meer in [&#x200B; documentatie van Oracle &#x200B;](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

## Rechts bijsnijden {#rightTrim}

De functie `rightTrim` verwijdert witruimten van het einde van een tekenreeks.

**Syntaxis**

```sql
{%= rightTrim(string) %}
```

## SHA256 {#sha256}

De functie `SHA256` berekent en retourneert de sha256-hash van een tekenreeks.

**Syntaxis**

```sql
{%= sha256(string) %} : string
```

**Voorbeeld**

```sql
{%= sha256("Eliechxh")%}
```

retourneert: `0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d`

## Splitsen {#split}

De functie `split` wordt gebruikt om een tekenreeks door een bepaald teken te splitsen.

**Syntaxis**

```sql
{%= split(string,string) %}
```

## Begint met{#startsWith}

De functie `startsWith` wordt gebruikt om te bepalen of een tekenreeks begint met een opgegeven subtekenreeks.

**Syntaxis**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `{CASE_SENSITIVE}` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. Standaard is dit ingesteld op true. |

**Voorbeeld**

De volgende vraag bepaalt, met gevalsgevoeligheid, als de naam van de persoon met &quot;Joe&quot;begint.

```sql
{%= startsWith(person.name,"Joe") %}
```

## Tekenreeks naar datum {#string-to-date}

De functie `stringToDate` zet een tekenreekswaarde om in een datum-tijdwaarde. Er zijn twee argumenten voor: tekenreeksrepresentatie van een datum-tijd en tekenreeksrepresentatie van de formatter.

**Syntaxis**

```sql
{= stringToDate("date-time value","formatter" %}
```

**Voorbeeld**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## Tekenreeks naar geheel getal {#string-to-integer}

De functie `string_to_integer` wordt gebruikt om een tekenreekswaarde om te zetten in een geheel-getalwaarde.

**Syntaxis**

```sql
{= string_to_integer(string) %}: int
```

## Tekenreeks naar nummer {#string-to-number}

De functie `stringToNumber` wordt gebruikt om een tekenreeks in een getal om te zetten. Deze geeft dezelfde tekenreeks als uitvoer voor ongeldige invoer.

**Syntaxis**

```sql
{%= stringToNumber(string) %}: double
```

## Subtekenreeks {#sub-string}

De functie `Count string` wordt gebruikt om de subtekenreeks van de tekenreeksexpressie tussen de beginindex en de eindindex te retourneren.
**Syntaxis**

```sql
{= substr(string, integer, integer) %}: string
```

## Alles Beginhoofdletter{#titleCase}

De **titleCase** functie wordt gebruikt om eerste brieven van elke woorden van een koord te kapitaliseren.

**Syntaxis**

```sql
{%= titleCase(string) %}
```

**Voorbeeld**

Als de persoon in Washington high street woont, zal deze functie Washington High Street terugsturen.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## Naar bool {#to-bool}

De functie `toBool` wordt gebruikt om een argumentwaarde in een booleaanse waarde om te zetten, afhankelijk van het type.

**Syntaxis**

```sql
{= toBool(string) %}: boolean
```

## Tot op heden {#to-date-time}

De functie `toDateTime` wordt gebruikt om een tekenreeks om te zetten in een datum. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer.

**Syntaxis**

```sql
{%= toDateTime(string, string) %}: date-time
```

## Alleen tot op heden tijd {#to-date-time-only}

De functie `toDateTimeOnly` wordt gebruikt om een argumentwaarde om te zetten in een waarde met alleen datumtijd. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer. Deze functie accepteert veldtypen tekenreeks, datum, lang en int.

**Syntaxis**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## Verkleinen {#trim}

De **versiering** functie verwijdert alle witte ruimten van het begin en aan het eind van een koord.

**Syntaxis**

```sql
{%= trim(string) %}
```

## Hoofdletters{#upper}

De **upperCase** functie zet een koord in hogere hoofdletters om.

**Syntaxis**

```sql
{%= upperCase(string) %}
```

**Voorbeeld**

Deze functie converteert de achternaam van het profiel naar hoofdletters.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## URL-decodering {#url-decode}

De functie `urlDecode` wordt gebruikt om een URL-gecodeerde tekenreeks te decoderen.

**Syntaxis**

```sql
{%= urlDecode(string) %}: string
```

## URL-codering {#url-encode}

De functie `Count only null` wordt gebruikt om een tekenreeks te coderen met url.

**Syntaxis**

```sql
{%= urlEncode(string) %}: string
```
