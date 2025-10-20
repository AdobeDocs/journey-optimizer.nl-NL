---
title: Arrays-functies, bibliotheek
description: Arrays-functies, bibliotheek
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 2%

---

# Arrays en lijstfuncties {#arrays}

Gebruik deze functies om interactie met arrays, lijsten en tekenreeksen eenvoudiger te maken.

## Alleen aantal null {#count-only-null}

De functie `countOnlyNull` wordt gebruikt om het aantal null-waarden in een lijst te tellen.

**Syntaxis**

```sql
{%= countOnlyNull(array) %}
```

**Voorbeeld**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Retourneert 3.

## Tellen met null {#count-with-null}

De functie `countWithNull` wordt gebruikt om alle elementen van een lijst te tellen met inbegrip van ongeldige waarden.

**Syntaxis**

```sql
{%= countWithNull(array) %}
```

**Voorbeeld**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Retourneert 6.

## Afzonderlijk{#distinct}

De functie `distinct` wordt gebruikt om waarden op te halen uit een array of lijst waarvan dubbele waarden zijn verwijderd.

**Syntaxis**

```sql
{%= distinct(array) %}
```

**Voorbeeld**

Met de volgende bewerking worden personen opgegeven die orders in meer dan één winkel hebben geplaatst.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Aantal zonder onderscheid met null {#distinct-count-with-null}

De functie `distinctCountWithNull` wordt gebruikt om het aantal verschillende waarden in een lijst te tellen met inbegrip van de ongeldige waarden.

**Syntaxis**

```sql
{%= distinctCountWithNull(array) %}
```

**Voorbeeld**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Retourneert 3.

## Eerste object{#head}

De functie `head` wordt gebruikt om het eerste item in een array of lijst te retourneren.

**Syntaxis**

```sql
{%= head(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de eerste van de bovenste vijf bestellingen met de hoogste prijs. Meer informatie over de `topN` functie kan in [ eerst `n` in serie ](#first-n) sectie worden gevonden.

```sql
{%= head(topN(orders,price, 5)) %}
```

## Eerste `n` in array {#first-n}

De functie `topN` wordt gebruikt om de eerste `N` -items in een array te retourneren, wanneer deze in oplopende volgorde worden gesorteerd op basis van de opgegeven numerieke expressie.

**Syntaxis**

```sql
{%= topN(array, value, amount) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{ARRAY}` | De array of lijst die moet worden gesorteerd. |
| `{VALUE}` | De eigenschap waarin de array of de lijst moet worden gesorteerd. |
| `{AMOUNT}` | Het aantal objecten dat moet worden geretourneerd. |

**Voorbeeld**

De volgende bewerking retourneert de eerste vijf bestellingen met de laagste prijs.

```sql
{%= topN(orders,price, 5) %}
```

## In{#in}

De functie `in` wordt gebruikt om te bepalen of een item lid is van een array of lijst.

**Syntaxis**

```sql
{%= in(value, array) %}
```

**Voorbeeld**

De volgende bewerking definieert personen met verjaardagen in maart, juni of september.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Inclusief{#includes}

De functie `includes` wordt gebruikt om te bepalen of een array of lijst een bepaald item bevat.

**Syntaxis**

```sql
{%= includes(array,item) %}
```

**Voorbeeld**

De volgende bewerking definieert personen van wie de favoriete kleur rood bevat.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Doorsnede{#intersects}

De functie `intersects` wordt gebruikt om te bepalen of twee arrays of lijsten ten minste één gemeenschappelijk lid hebben.

**Syntaxis**

```sql
{%= intersects(array1, array2) %}
```

**Voorbeeld**

De volgende bewerking definieert personen van wie de favoriete kleuren ten minste een van de kleuren rood, blauw of groen zijn.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## Laatste `n` in array{#last-n}

De functie `bottomN` wordt gebruikt om de laatste `N` -items in een array te retourneren, wanneer deze in oplopende volgorde worden gesorteerd op basis van de opgegeven numerieke expressie.

**Syntaxis**

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Beschrijving |
| --------- | ----------- | 
| `{ARRAY}` | De array of lijst die moet worden gesorteerd. |
| `{VALUE}` | De eigenschap waarin de array of de lijst moet worden gesorteerd. |
| `{AMOUNT}` | Het aantal objecten dat moet worden geretourneerd. |

**Voorbeeld**

De volgende bewerking retourneert de laatste vijf bestellingen met de hoogste prijs.

```sql
{%= bottomN(orders,price, 5) %}
```

## Niet in{#notin}

De functie `notIn` wordt gebruikt om te bepalen of een item geen lid is van een array of lijst.

>[!NOTE]
>
>De `notIn` functie ** zorgt ook ervoor dat geen van beide waarde aan ongeldig is. Daarom zijn de resultaten geen exacte negatie van de functie `in` .

**Syntaxis**

```sql
{%= notIn(value, array) %}
```

**Voorbeeld**

De volgende bewerking definieert personen met verjaardagen die zich niet in maart, juni of september bevinden.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Subset van{#subset}

De functie `subsetOf` wordt gebruikt om te bepalen of een specifieke array (array A) een subset is van een andere array (array B). Met andere woorden, alle elementen in array A zijn elementen van array B.

**Syntaxis**

```sql
{%= subsetOf(array1, array2) %}
```

**Voorbeeld**

De volgende bewerking definieert mensen die al hun favoriete steden hebben bezocht.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Superset van{#superset}

De functie `supersetOf` wordt gebruikt om te bepalen of een specifieke array (array A) een superset is van een andere array (array B). Met andere woorden, die array A bevat alle elementen in array B.

**Syntaxis**

```sql
{%= supersetOf(array1, array2) %}
```

**Voorbeeld**

De volgende bewerking definieert mensen die sushi en pizza hebben gegeten ten minste één keer.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```
