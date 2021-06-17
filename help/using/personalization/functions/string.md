---
title: String-functies, bibliotheek
description: String-functies, bibliotheek
feature: Personalisatie
topic: Personalisatie
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 4%

---

# Tekenreeksfuncties {#string}

Leer hoe u String-functies in de Expressieeditor kunt gebruiken.

## Camel Case {#camelCase}

De functie `camelCase` kapitaliseert de eerste letter van elk woord van een tekenreeks.

**Indeling**

```sql
{%= camelCase(string)%}
```

**Voorbeeld**

Met de volgende functie krijgt de eerste letter van het woord een hoofdletter in het adres van het profiel.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Concat {#concate}

De functie `concat` combineert twee tekenreeksen in één.

**Indeling**

```sql
{%= concat(string,string) %}
```

**Voorbeeld**

De volgende functie combineert profielstad en land in één tekenreeks.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Bevat {#contains}

De functie `contains` wordt gebruikt om te bepalen als een koord een gespecificeerde substring bevat.

**Indeling**

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

De functie `doesNotContain` wordt gebruikt om te bepalen als een koord geen gespecificeerde substring bevat.

**Indeling**

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

De functie `doesNotEndWith` wordt gebruikt om te bepalen als een koord niet met een gespecificeerde substring beëindigt.

**Indeling**

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

De functie `doesNotStartWith` wordt gebruikt om te bepalen als een koord niet met een gespecificeerde substring begint.

**Indeling**

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

De functie `encode64` wordt gebruikt om een koord te coderen om Persoonlijke Informatie (PI) te bewaren als om bijvoorbeeld in een URL moet worden omvat.

**Indeling**

```sql
{%= encode64(string) %}
```

## Ends with (Eindigt met){#endsWith}

De functie `endsWith` wordt gebruikt om te bepalen of een tekenreeks eindigt met een opgegeven subtekenreeks.

**Indeling**

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


## Equals (Is gelijk aan){#equals}

De functie `equals` wordt gebruikt om te bepalen of een tekenreeks gelijk is aan de opgegeven tekenreeks, met hoofdlettergevoeligheid.

**Indeling**

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

**Indeling**

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

De functie `extractEmailDomain` wordt gebruikt om het domein van een e-mailadres te halen.

**Indeling**

```sql
{%= extractEmailDomain(string) %}
```

**Voorbeeld**

De volgende query extraheert het e-maildomein van het persoonlijke e-mailadres.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Is empty {#isEmpty}

De functie `isEmpty` wordt gebruikt om te bepalen of een tekenreeks leeg is.

**Indeling**

```sql
{%= isEmpty(string) %}
```

**Voorbeeld**

De volgende functie retourneert &#39;true&#39; als het mobiele telefoonnummer van het profiel leeg is. Anders wordt &#39;false&#39; geretourneerd.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Links bijsnijden {#leftTrim}

De functie `leftTrim` wordt gebruikt om witte ruimten uit het begin van een koord te verwijderen.

**Indeling**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

De functie `length` wordt gebruikt om het aantal karakters in een koord of een uitdrukking te krijgen.

**Indeling**

```sql
{%= length(string) %}
```

**Voorbeeld**

De volgende functie retourneert de lengte van de stadsnaam van het profiel.

```sql
{%= length(profile.homeAddress.city) %}
```

## leuk{#like}

De functie `like` wordt gebruikt om te bepalen als een koord een gespecificeerd patroon aanpast.

**Indeling**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De expressie die moet overeenkomen met de eerste tekenreeks. Er zijn twee ondersteunde speciale tekens voor het maken van een expressie: `%` en `_`. <ul><li>`%` wordt gebruikt om nul of meer tekens te vertegenwoordigen.</li><li>`_` wordt gebruikt om precies één teken te vertegenwoordigen.</li></ul> |

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

De functie `matches` wordt gebruikt om te bepalen als een koord een specifieke regelmatige uitdrukking aanpast. Raadpleeg [dit document](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) voor meer informatie over overeenkomende patronen in reguliere expressies.

**Indeling**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Voorbeeld**

De volgende vraag bepaalt, zonder case gevoeligheid, als de naam van de persoon met &quot;John&quot;begint.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Niet gelijk aan{#notEqualTo}

De functie `notEqualTo` wordt gebruikt om te bepalen of een tekenreeks niet gelijk is aan de opgegeven tekenreeks.

**Indeling**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die met de eerste tekenreeks moet worden vergeleken. |

**Voorbeeld**

De volgende vraag bepaalt, met gevalgevoeligheid, als de naam van de persoon niet &quot;John&quot;is.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Groep met reguliere expressies{#regexGroup}

De functie `Group` wordt gebruikt om specifieke informatie te halen, die op de regelmatige verstrekte uitdrukking wordt gebaseerd.

**Indeling**

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
{%= regexGroup(emailAddress,"@(\w+)", 1) %}
```

## Replace {#replace}

De functie `replace` wordt gebruikt om een bepaalde subtekenreeks in een tekenreeks te vervangen door een andere subtekenreeks.

**Indeling**

```sql
{%= replace(string,string,string) %}
```

**Voorbeeld**

De volgende functie.

```sql

```


## Alles vervangen{#replaceAll}

De functie `replaceAll` wordt gebruikt om alle subtekenreeksen van een tekst te vervangen die het &quot;doel&quot;met het gespecificeerde letterlijke &quot;vervangingskoord&quot;aanpast. De vervanging vindt plaats vanaf het begin van de tekenreeks tot het einde. Als u bijvoorbeeld &quot;aa&quot; vervangt door &quot;b&quot; in de tekenreeks &quot;aaa&quot;, resulteert dit in &quot;ba&quot; in plaats van &quot;ab&quot;.

**Indeling**

```sql
{%= replaceAll(string,string,string) %}
```


## Rechts bijsnijden {#rightTrim}

De functie `rightTrim` wordt gebruikt verwijdert witte ruimten van het eind van een koord.


**Indeling**

```sql
{%= rightTrim(string) %}
```

## Splitsen {#split}

De functie `split` wordt gebruikt om een tekenreeks door een bepaald teken te splitsen.

**Indeling**

```sql
{%= split(string,string) %}
```

<!--
**Example**

The following function .

```sql

```

-->

## Starts with (Begint met){#startsWith}

De functie `startsWith` wordt gebruikt om te bepalen als een koord met gespecificeerde substring begint.

**Indeling**

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

## Alles Beginhoofdletter{#titleCase}

De functie **titleCase** wordt gebruikt om eerste letters van elke woorden van een koord te kapitaliseren.

**Syntaxis**

```sql
{%= titleCase(string) %}
```

**Voorbeeld**

Als de persoon in Washington high street woont, zal deze functie Washington High Street terugsturen.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## Verkleinen{#trim}

De functie **trim** verwijdert alle witte ruimten van het begin en aan het eind van een koord.

**Syntaxis**

```sql
{%= trim(string) %}
```

## Hoofdletters{#upper}

De functie **upperCase** zet een tekenreeks om in hoofdletters.

**Syntaxis**

```sql
{%= upperCase(string) %}
```

**Voorbeeld**

Deze functie converteert de achternaam van het profiel naar hoofdletters.

```sql
{%= upperCase(profile.person.name.lastName) %}
```
