---
title: String-functies, bibliotheek
description: String-functies, bibliotheek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 3%

---

# Tekenreeksfuncties {#string}

Leer hoe u String-functies in de Expressieeditor kunt gebruiken.

## Camel Case {#camelCase}

De `camelCase` functie kapitaliseert de eerste letter van elk woord van een tekenreeks.

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

De `concat` functie combineert twee tekenreeksen in één.

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

De `contains` wordt gebruikt om te bepalen of een tekenreeks een opgegeven subtekenreeks bevat.

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

De `doesNotContain` wordt gebruikt om te bepalen of een tekenreeks geen opgegeven subtekenreeks bevat.

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

De `doesNotEndWith` wordt gebruikt om te bepalen of een tekenreeks niet eindigt met een opgegeven subtekenreeks.

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

De `doesNotStartWith` wordt gebruikt om te bepalen of een tekenreeks niet begint met een opgegeven subtekenreeks.

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

De `encode64` Deze functie wordt gebruikt om een tekenreeks te coderen zodat Personal Information (PI) behouden blijft als deze bijvoorbeeld in een URL moet worden opgenomen.

**Indeling**

```sql
{%= encode64(string) %}
```

## Ends with (Eindigt met){#endsWith}

De `endsWith` wordt gebruikt om te bepalen of een tekenreeks eindigt met een opgegeven subtekenreeks.

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

De `equals` wordt gebruikt om te bepalen of een tekenreeks gelijk is aan de opgegeven tekenreeks, met hoofdlettergevoeligheid.

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

De `equalsIgnoreCase` wordt gebruikt om te bepalen of een tekenreeks gelijk is aan de opgegeven tekenreeks, zonder hoofdlettergevoeligheid.

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

De `extractEmailDomain` wordt gebruikt om het domein van een e-mailadres te extraheren.

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

De `isEmpty` wordt gebruikt om te bepalen of een tekenreeks leeg is.

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

De `leftTrim` wordt gebruikt om witruimten te verwijderen uit het begin van een tekenreeks.

**Indeling**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

De `length` wordt gebruikt om het aantal tekens in een tekenreeks of expressie op te halen.

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

De `like` wordt gebruikt om te bepalen of een tekenreeks overeenkomt met een opgegeven patroon.

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

De `lowerCase` functie converteert een tekenreeks naar kleine letters.

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

De `matches` wordt gebruikt om te bepalen of een tekenreeks overeenkomt met een specifieke reguliere expressie. Zie [dit document](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) voor meer informatie over overeenkomende patronen in reguliere expressies.

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

De `notEqualTo` wordt gebruikt om te bepalen of een tekenreeks niet gelijk is aan de opgegeven tekenreeks.

**Indeling**

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

## Groep met reguliere expressies{#regexGroup}

De `Group` Deze functie wordt gebruikt om specifieke informatie te extraheren op basis van de reguliere expressie die wordt gegeven.

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

De `replace` Deze functie wordt gebruikt om een bepaalde subtekenreeks in een tekenreeks te vervangen door een andere subtekenreeks.

**Indeling**

```sql
{%= replace(string,string,string) %}
```

**Voorbeeld**

De volgende functie.

```sql

```


## Alles vervangen{#replaceAll}

De `replaceAll` Deze functie wordt gebruikt om alle subtekenreeksen van een tekst te vervangen die overeenkomt met &quot;target&quot; met de opgegeven letterlijke tekenreeks &quot;replacement&quot;. De vervanging vindt plaats vanaf het begin van de tekenreeks tot het einde. Als u bijvoorbeeld &quot;aa&quot; vervangt door &quot;b&quot; in de tekenreeks &quot;aaa&quot;, resulteert dit in &quot;ba&quot; in plaats van &quot;ab&quot;.

**Indeling**

```sql
{%= replaceAll(string,string,string) %}
```


## Rechts bijsnijden {#rightTrim}

De `rightTrim` functie wordt gebruikt verwijdert witte ruimten van het eind van een koord.


**Indeling**

```sql
{%= rightTrim(string) %}
```

## Splitsen {#split}

De `split` functie wordt gebruikt om een tekenreeks te splitsen op een bepaald teken.

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

De `startsWith` wordt gebruikt om te bepalen of een tekenreeks begint met een opgegeven subtekenreeks.

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

De **titleCase** functie wordt gebruikt om eerste letters van elke woorden van een tekenreeks met hoofdletters te maken.

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

De **bijsnijden** verwijdert alle spaties van het begin tot het einde van een tekenreeks.

**Syntaxis**

```sql
{%= trim(string) %}
```

## Hoofdletters{#upper}

De **upperCase** functie converteert een tekenreeks naar hoofdletters.

**Syntaxis**

```sql
{%= upperCase(string) %}
```

**Voorbeeld**

Deze functie converteert de achternaam van het profiel naar hoofdletters.

```sql
{%= upperCase(profile.person.name.lastName) %}
```