---
title: Arrays-functies, bibliotheek
description: Arrays-functies, bibliotheek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 2%

---

# Arrays en lijstfuncties {#arrays}

Gebruik deze functies om interactie met arrays, lijsten en tekenreeksen eenvoudiger te maken.

## Alleen aantal null {#count-only-null}

De `countOnlyNull` Deze functie wordt gebruikt om het aantal null-waarden in een lijst te tellen.

**Indeling**

```sql
{%= countOnlyNull(array) %}
```

**Voorbeeld**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Retourneert 3.

## Tellen met null {#count-with-null}

De `countWithNull` Deze functie wordt gebruikt om alle elementen van een lijst te tellen, inclusief null-waarden.

**Indeling**

```sql
{%= countWithNull(array) %}
```

**Voorbeeld**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Retourneert 6.

## Afzonderlijk{#distinct}

De `distinct` functie wordt gebruikt om waarden op te halen uit een array of lijst waarvan dubbele waarden zijn verwijderd.

**Indeling**

```sql
{%= distinct(array) %}
```

**Voorbeeld**

Met de volgende bewerking worden personen opgegeven die orders in meer dan één winkel hebben geplaatst.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Aantal zonder onderscheid met null {#distinct-count-with-null}

De `distinctCountWithNull` Deze functie wordt gebruikt om het aantal verschillende waarden in een lijst te tellen, inclusief de null-waarden.

**Indeling**

```sql
{%= distinctCountWithNull(array) %}
```

**Voorbeeld**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Retourneert 3.

## Eerste object{#head}

De `head` functie wordt gebruikt om het eerste item in een array of lijst te retourneren.

**Indeling**

```sql
{%= head(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de eerste van de bovenste vijf bestellingen met de hoogste prijs. Meer informatie over de `topN` kan worden gevonden in de [first `n` in array](#first-n) sectie.

```sql
{%= head(topN(orders,price, 5)) %}
```

## Eerste `n` in array {#first-n}

De `topN` function wordt gebruikt om de eerste te retourneren `N` items in een array, indien gesorteerd in oplopende volgorde op basis van de opgegeven numerieke expressie.

**Indeling**

```sql
{%= topN(array, value, amount) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{ARRAY}` | De array of lijst die moet worden gesorteerd. |
| `{VALUE}` | De eigenschap waarin de array of de lijst moet worden gesorteerd. |
| `{AMOUNT}` | Het aantal objecten dat moet worden geretourneerd. |

**Voorbeeld**

De volgende bewerking retourneert de bovenste vijf bestellingen met de hoogste prijs.

```sql
{%= topN(orders,price, 5) %}
```

## In{#in}

De `in` wordt gebruikt om te bepalen of een punt een lid van een serie of een lijst is.

**Indeling**

```sql
{%= in(value, array) %}
```

**Voorbeeld**

De volgende bewerking definieert personen met verjaardagen in maart, juni of september.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Inclusief{#includes}

De `includes` wordt gebruikt om te bepalen of een array of lijst een bepaald item bevat.

**Indeling**

```sql
{%= includes(array,item) %}
```

**Voorbeeld**

De volgende bewerking definieert personen van wie de favoriete kleur rood bevat.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Doorsnede{#intersects}

De `intersects` functie wordt gebruikt om te bepalen of twee series of lijsten minstens één gemeenschappelijk lid hebben.

**Indeling**

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

**Format**

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

De `bottomN` function wordt gebruikt om de laatste te retourneren `N` items in een array, indien gesorteerd in oplopende volgorde op basis van de opgegeven numerieke expressie.

**Indeling**

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Beschrijving |
| --------- | ----------- | 
| `{ARRAY}` | De array of lijst die moet worden gesorteerd. |
| `{VALUE}` | De eigenschap waarin de array of de lijst moet worden gesorteerd. |
| `{AMOUNT}` | Het aantal objecten dat moet worden geretourneerd. |

**Voorbeeld**

De volgende bewerking retourneert de bovenste vijf bestellingen met de laagste prijs.

```sql
{%= bottomN(orders,price, 5) %}
```

## Niet in{#notin}

De `notIn` wordt gebruikt om te bepalen of een item geen lid is van een array of lijst.

>[!NOTE]
>
>De `notIn` function *ook* zorgt ervoor dat geen van beide waarden gelijk is aan null. Daarom zijn de resultaten geen exacte ontkenning van de `in` functie.

**Indeling**

```sql
{%= notIn(value, array) %}
```

**Voorbeeld**

De volgende bewerking definieert personen met verjaardagen die zich niet in maart, juni of september bevinden.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Subset van{#subset}

De `subsetOf` wordt gebruikt om te bepalen of een specifieke array (array A) een subset is van een andere array (array B). Met andere woorden, alle elementen in array A zijn elementen van array B.

**Indeling**

```sql
{%= subsetOf(array1, array2) %}
```

**Voorbeeld**

De volgende bewerking definieert mensen die al hun favoriete steden hebben bezocht.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Superset van{#superset}

De `supersetOf` wordt gebruikt om te bepalen of een specifieke array (array A) een superset is van een andere array (array B). Met andere woorden, die array A bevat alle elementen in array B.

**Indeling**

```sql
{%= supersetOf(array1, array2) %}
```

**Voorbeeld**

De volgende bewerking definieert mensen die sushi en pizza hebben gegeten ten minste één keer.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
