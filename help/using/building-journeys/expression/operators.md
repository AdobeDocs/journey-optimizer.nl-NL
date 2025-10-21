---
solution: Journey Optimizer
product: journey optimizer
title: Operatoren
description: Informatie over operatoren in geavanceerde expressies
feature: Journeys
role: Developer
level: Experienced
keywords: expressie, syntaxis, operatoren, editor, reis
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 5%

---

# Operatoren {#operators}

Er zijn twee soorten exploitanten: unaire exploitanten en binaire exploitanten. Er zijn linkerhand unaire operatoren en rechterhand unaire operatoren.

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@event{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## Belangrijke opmerkingen{#important-notes}

* Wanneer het gebruiken van een vermenigvuldiging (`*`), moeten beide verrichtingsgebieden het zelfde type, of geheel of decimaal hebben. Voorbeeld:
   * het volgende voorbeeld is correct: `3.0 * 4.0`
   * `3 * 4.0` leidt tot een fout

* Wanneer u de operator `+` gebruikt, moet de expressie tussen haakjes worden ingekapseld. Voorbeeld:
   * `toDateTimeOnly(toDateTime((currentTimeInMillis()) + 1))` is correct
   * `toDateTimeOnly(toDateTime(currentTimeInMillis() + 1))` leidt tot een fout

## Logisch  {#logical}

### en

```json
<expression1> and <expression2>
```

Zowel &lt;expression1> als &lt;expression2> moeten booleaans zijn. Het resultaat is booleaans.

Voorbeeld:

```json
3.14 > 2 and 3.15 < 1
```

### of

```json
<expression1> or <expression2>
```

Zowel &lt;expression1> als &lt;expression2> moeten booleaans zijn. Het resultaat is booleaans.

Voorbeeld:

```json
3.14 > 2 or 3.15 < 1
```

### niet

```json
not <expression>
```

&lt;expression> moet Boolean zijn. Het resultaat is booleaans.

Voorbeeld:

```json
not 3.15 < 1
```

## Vergelijking {#comparison}

### is null

```json
<expression> is null
```

Het resultaat is booleaans.

Null betekent dat de expressie geen geëvalueerde waarde heeft.

Voorbeeld:

```json
@event{BarBeacon.location} is null
```

### is niet null

```json
<expression> is not null
```

Het resultaat is booleaans.

Null betekent dat de expressie geen geëvalueerde waarde heeft.

Voorbeeld:

```json
@event{BarBeacon.location} is not null
```

### heeft null

```json
<expression> has null
```

&lt;expression> moet een lijst zijn. Het resultaat is booleaans.

Nuttig om aan te geven dat een lijst minstens één null-waarde bevat.

Voorbeeld:

```json
["foo", "bar", null] has null
```

Retourneert true

```json
["foo", "bar", ""] has null
```

Retourneert false omdat &quot;&quot; niet als null wordt beschouwd.

### ==

```json
<expression1> == <expression2>
```

>[!NOTE]
>
>Voor &lt;expression1> en &lt;expression2> is er geen gegevenstypecontrole.

Voorbeeld:

```json
3.14 == 42
```

```json
"foo" == "bar"
```

### !=

```json
<expression1> != <expression2>
```

>[!NOTE]
>
>Voor &lt;expression1> en &lt;expression2> is er geen gegevenstypecontrole.

Het resultaat is booleaans.

Voorbeeld:

```json
3.14 != 42
```

```json
"foo" != "bar"
```

### >

```json
<expression1> > <expression2>
```

Datetime kan met Datetime worden vergeleken.

Datetimeonly kan met Datetimeonly worden vergeleken.

Zowel geheel als decimaal kunnen met zowel geheel als decimaal worden vergeleken.

Elke andere combinatie is verboden.

Het resultaat is booleaans.

Voorbeeld:

```json
3.14 > 42
```

### >=

```json
<expression1> >= <expression2>
```

Datetime kan met Datetime worden vergeleken.

Datetimeonly kan met Datetimeonly worden vergeleken.

Zowel geheel als decimaal kunnen met zowel geheel als decimaal worden vergeleken.

Elke andere combinatie is verboden.

Het resultaat is booleaans.

Voorbeeld:

```json
42 >= 3.14
```

### &lt;

```json
<expression1> < <expression2>
```

Datetime kan met Datetime worden vergeleken.

Datetimeonly kan met Datetimeonly worden vergeleken.

Zowel geheel als decimaal kunnen met zowel geheel als decimaal worden vergeleken.

Elke andere combinatie is verboden.

Het resultaat is booleaans.

Voorbeeld:

```json
42 < 3.14
```

### &lt;=

```json
<expression1> <= <expression2>
```

Datetime kan met Datetime worden vergeleken.

Datetimeonly kan met Datetimeonly worden vergeleken.

Zowel geheel als decimaal kunnen met zowel geheel als decimaal worden vergeleken.

Elke andere combinatie is verboden.

Het resultaat is booleaans.

Voorbeeld:

```json
42 <= 3.14
```

## Rekenkundig {#arithmetic}

### +

```json
<expression1> + <expression2>
```

Beide expressies moeten numeriek (geheel getal of decimaal) zijn.

Het resultaat is ook numeriek.

Voorbeeld:

```json
1 + 2
```

Retourneert 3

### -

```json
<expression1> - <expression2>
```

Beide expressies moeten numeriek (geheel getal of decimaal) zijn.

Het resultaat is ook numeriek.

Voorbeeld:

```json
2 - 1 
```

Retourneert 1

### /

```json
<expression1> / <expression2>
```

Beide expressies moeten numeriek (geheel getal of decimaal) zijn.

Het resultaat is ook numeriek.

&lt;expression2> mag niet gelijk zijn aan 0 (retourneert 0).

Voorbeeld:

```json
4 / 2
```

Retourneert 2

### *

```json
<expression1> * <expression2>
```

Beide expressies moeten numeriek (geheel getal of decimaal) zijn.

Het resultaat is ook numeriek.

Voorbeeld:

```json
3 * 4
```

Retourneert 12

### %

```json
<expression1> % <expression2>
```

Beide expressies moeten numeriek (geheel getal of decimaal) zijn.

Het resultaat is ook numeriek.

Voorbeeld:

```json
3 % 2
```

Retourneert 1.

## Math {#math}

### is numeriek

```json
<expression> is numeric
```

Het type van de uitdrukking is geheel of decimaal.

Voorbeeld:

```json
@ is numeric
```

### is integer

```json
<expression> is integer
```

Het type van de expressie is geheel getal.

Voorbeeld:

```json
@ is integer
```

### is decimaal

```json
<expression> is decimal
```

Het type van de expressie is decimaal.

Voorbeeld:

```json
@ is decimal
```

## String {#string}

### +

```json
<string> + <expression>
```

```json
<expression> + <string>
```

Twee expressies worden samengevoegd.

Eén expressie moet een kettingtekenreeks zijn.

Voorbeeld:

```json
"the current time is " + (now())
```

Keert &quot;de huidige tijd is 2023-09-23T09 :30: 06.693Z&quot; terug

```json
(now()) + " is the current time"
```

Keert &quot;2023-09-23T09 :30: 06.693Z terug is de huidige tijd&quot;

```json
"a" + "b" + "c" + 1234
```

Retourneert &quot;abc1234&quot;.

## Datum {#date}

### +

```json
<expression> + <duration>
```

Voeg een duur aan dateTime, een dateTimeOnly of een duur toe.

Voorbeeld:

```json
(toDateTime("2023-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

Keert a _dateTime_ 2023-12-03T15 :30: 30Z terug

```json
(toDateTimeOnly("2023-12-03T15:15:30")) + (toDuration("PT15M"))
```

Keert a _dateTimeOnly_ 2023-12-03T15 :30: 30 terug

```json
(now()) + (toDuration("PT1H"))
```

Keert a _dateTime_ (met UTC tijdzone) één uur later van huidige tijd terug

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

Keert a _duur_ PT2H terug
