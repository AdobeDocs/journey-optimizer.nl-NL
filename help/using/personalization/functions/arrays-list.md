---
title: Arrays-functies, bibliotheek
description: Arrays-functies, bibliotheek
feature: Personalisatie
topic: Personalisatie
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 3%

---

# Arrays en lijstfuncties {#arrays}

Gebruik deze functies om interactie met arrays, lijsten en tekenreeksen eenvoudiger te maken.

## Afzonderlijk{#distinct}

De functie `distinct` wordt gebruikt om waarden op te halen uit een array of lijst met verwijderde dubbele waarden.

**Indeling**

```sql
{%= distinct(array) %}
```

**Voorbeeld**

Met de volgende bewerking worden personen opgegeven die orders in meer dan één winkel hebben geplaatst.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Eerste object{#head}

De functie `head` wordt gebruikt om het eerste item in de array of lijst te retourneren.

**Indeling**

```sql
{%= head({array}) %}
```

**Voorbeeld**

De volgende bewerking retourneert de eerste van de bovenste vijf bestellingen met de hoogste prijs. Meer informatie over de functie `topN` vindt u in de sectie [first `n` in array](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

## Eerste `n` in array {#first-n}

De functie `topN` wordt gebruikt om de eerste `N` punten in een serie terug te keren, wanneer gesorteerd in oplopende orde die op de bepaalde numerieke uitdrukking wordt gebaseerd.

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

De functie `in` wordt gebruikt om te bepalen of een punt een lid van een serie of een lijst is.

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

De functie `includes` wordt gebruikt om te bepalen of een serie of een lijst een bepaald punt bevat.

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

De functie `intersects` wordt gebruikt om te bepalen of twee series of lijsten minstens één gemeenschappelijk lid hebben.

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

De functie `bottomN` wordt gebruikt om de laatste `N` punten in een serie terug te keren, wanneer gesorteerd in oplopende orde die op de bepaalde numerieke uitdrukking wordt gebaseerd.

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

De functie `notIn` wordt gebruikt om te bepalen als een punt geen lid van een serie of een lijst is.

>[!NOTE]
>
>De `notIn` functie *also* zorgt ervoor dat geen van beide waarden gelijk aan null is. Daarom zijn de resultaten geen exacte negatie van de functie `in`.

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

De functie `subsetOf` wordt gebruikt om te bepalen of een specifieke array (array A) een subset is van een andere array (array B). Met andere woorden, alle elementen in array A zijn elementen van array B.

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

De functie `supersetOf` wordt gebruikt om te bepalen of een specifieke array (array A) een superset is van een andere array (array B). Met andere woorden, die array A bevat alle elementen in array B.

**Indeling**

```sql
{%= supersetOf(array1, array2) %}
```

**Voorbeeld**

De volgende bewerking definieert mensen die sushi en pizza hebben gegeten ten minste één keer.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```







