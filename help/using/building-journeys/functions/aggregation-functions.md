---
product: journey optimizer
title: Samenvoegingsfuncties
description: Meer informatie over aggregatiefuncties
feature: Journeys
role: Developer
level: Experienced
keywords: aggregatie, functies, expressie, transport, avg, count, max, min, sum
version: Journey Orchestration
source-git-commit: 6102fba3ba30b462654e218f08835be53b75e2cc
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 4%

---

# Samenvoegingsfuncties {#aggregation-functions}

Met aggregatiefuncties kunt u berekeningen uitvoeren op een set waarden en één samengevat resultaat retourneren. Met deze functies kunt u gegevens in uw reisexpressies analyseren door gemiddelden te berekenen, minimum- en maximumwaarden te zoeken, elementen te tellen en numerieke waarden op te tellen.

Gebruik aggregatiefuncties wanneer u dat nodig hebt:

* Statische waarden berekenen op basis van lijsten of arrays (gemiddelde, som, min, max)
* Elementen tellen in verzamelingen met opties voor het opnemen of uitsluiten van null-waarden
* Unieke waarden in gegevenssets bepalen
* Gegevensgestuurde beslissingen nemen op basis van berekende meetwaarden

Samenvoegingsfuncties verwerken automatisch null-waarden op basis van hun specifieke gedrag, waardoor het eenvoudiger wordt om te werken met gegevens in de praktijk die ontbrekende of niet-gedefinieerde waarden kunnen bevatten.


## avg {#avg}

Geeft als resultaat de gemiddelde waarde tussen een reeks expressies, opgegeven als een lijst of twee expressies. Null-waarden worden genegeerd.

+++Syntaxis

`avg(<parameter>)`

+++

+++Parameters

Ondersteunde typen:

* listInteger
* listDecimal
* decimaal
* integer

+++

+++Handtekeningen en type geretourneerd

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Retourneert een decimaal.

+++

+++Voorbeelden

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Retourneert 7.0.

`avg(10.2, 3)`

Retourneert 6.6.

+++

## count {#count}

Telt de elementen van de lijst die geen rekening houden met de ongeldige waarden.

+++Syntaxis

`count(<listAny>)`

`count(<listObject>)`

+++

+++Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te verwerken lijst. Voor listObject moet dit een veldverwijzing zijn. Een listObject kan geen null-object bevatten. |

+++

+++Handtekeningen en type geretourneerd

`count(<listAny>)`

Retourneert een geheel getal.

+++

+++Voorbeelden

`count([10,2,10,null])`

Retourneert 3.

`count(@event{my_event.productListItems})`

Retourneert het aantal objecten in de opgegeven array met objecten (type listObject). Opmerking: een listObject kan geen null-object bevatten

+++

## countOnlyNull {#countOnlyNull}

Telt het aantal null-waarden in de lijst.

+++Syntaxis

`countOnlyNull(<listAny>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Handtekeningen en type geretourneerd

`countOnlyNull(<listAny>)`

Retourneert een geheel getal.

+++

+++Voorbeelden

`countOnlyNull([10,2,10,null])`

Retourneert 1.

+++

**Nota:** de parameter `<listObject>` wordt niet gesteund in deze functie.

## countWithNull {#countWithNull}

Telt alle elementen van de lijst met inbegrip van ongeldige waarden.

+++Syntaxis

`countWithNull(<listAny>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Handtekeningen en type geretourneerd

`countWithNull(<listAny>)`

Retourneert een geheel getal.

+++

+++Voorbeelden

`countWithNull([10,2,10,null])`

Retourneert 4.

+++

**Nota:** de parameter `<listObject>` wordt niet gesteund in deze functie.

## distinctCount {#distinctCount}

Telt het aantal verschillende waarden waarbij de null-waarden worden genegeerd.

+++Syntaxis

`distinctCount(<listAny>)`

+++

+++Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te verwerken lijst. Voor listObject moet dit een veldverwijzing zijn. |
| keyAttributeName | string | Deze parameter is optioneel en alleen voor listObject. Wanneer de parameter niet wordt opgegeven, wordt een object als gedupliceerd beschouwd wanneer alle kenmerken dezelfde waarden hebben. Anders wordt een object als gedupliceerd beschouwd wanneer het opgegeven kenmerk dezelfde waarde heeft. |

+++

+++Handtekeningen en type geretourneerd

`distinctCount(<listAny>)`

Retourneert een geheel getal.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Retourneert een lijst met objecten.

+++

+++Voorbeelden

`distinctCount([10,2,10,null])`

Retourneert 2.

`distinctCount(@event{my_event.productListItems})`

Retourneert het aantal strikt verschillende objecten in de opgegeven array met objecten (type listObject).

`distinctCount(@event{my_event.productListItems}, "SKU")`

Keert het aantal voorwerpen terug die een duidelijke &quot;SKU&quot;attributenwaarde {} hebben.

+++

## distinctCountWithNull {#distinctCountWithNull}

Telt het aantal verschillende waarden inclusief de null-waarden.

+++Syntaxis

`distinctCountWithNull(<listAny>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Handtekeningen en type geretourneerd

`distinctCountWithNull(<listAny>)`

Retourneert een geheel getal.

+++

+++Voorbeelden

`distinctCountWithNull([10,2,10,null])`

Retourneert 3.

+++

**Nota:** de parameter `<listObject>` wordt niet gesteund in deze functie.

## max {#max}

Geeft als resultaat de maximale waarde tussen een reeks expressies, opgegeven als een lijst of twee expressies. Null-waarden worden genegeerd.

+++Syntaxis

`max(<parameter>)`

+++

+++Parameters

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duur
* integer
* decimaal
* dateTime
* dateTimeOnly

+++

+++Handtekeningen en geretourneerde typen

`max(<listDuration>)`

Retourneert een duur.

`max(<listInteger>)`

Retourneert een duur.

`max(<listDateTimeOnly>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

`max(<listDateTime>)`

Retourneert een datetime.

`max(<listDateOnly>)`

Retourneert een datum.

`max(<listDecimal>)`

Retourneert een decimaal.

`max(<decimal>,<decimal>)`

Retourneert een decimaal.

`max(<duration>,<duration>)`

Retourneert een duur.

`max(<dateTime>,<dateTime>)`

Retourneert een datetime.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

`max(<integer>,<integer>)`

Retourneert een geheel getal.

+++

+++Voorbeelden

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

Retourneert 10.

`max([10,null,8])`

Retourneert 10.

+++

## min {#min}

Geeft als resultaat de minimumwaarde tussen een reeks expressies, opgegeven als een lijst of twee expressies. Null-waarden worden genegeerd.

+++Syntaxis

`min(<parameters>)`

+++

+++Parameters

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duur
* integer
* decimaal
* dateTime
* dateTimeOnly

+++

+++Handtekeningen en geretourneerde typen

`min(<listDuration>)`

Retourneert een duur.

`min(<listInteger>)`

Retourneert een duur.

`min(<listDateTimeOnly>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

`min(<listDateTime>)`

Retourneert een datetime.

`min(<listDateOnly>)`

Retourneert een datum.

`min(<listDecimal>)`

Retourneert een decimaal.

`min(<decimal>,<decimal>)`

Retourneert een decimaal.

`min(<duration>,<duration>)`

Retourneert een duur.

`min(<dateTime>,<dateTime>)`

Retourneert een datetime.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

`min(<integer>,<integer>)`

Retourneert een geheel getal.

+++

+++Voorbeelden

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Retourneert 3.

`min([10,null,8])`

Retourneert 8.

+++

## sum {#sum}

Retourneert de som van de waarden van een set expressies. Null-waarden worden genegeerd.

+++Syntaxis

`sum(<parameters>)`

+++

+++Parameters

* listInteger
* listDecimal
* duur
* integer
* decimaal

+++

+++Handtekeningen en geretourneerde typen

`sum(<listDecimal>)`

Retourneert een decimaal.

`sum(<listInteger>)`

Retourneert een geheel getal.

`sum(<integer>,<integer>)`

Retourneert een geheel getal.

`sum(<decimal>,<decimal>)`

Retourneert een decimaal.

+++

+++Voorbeelden

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Retourneert 21.

`sum([10.5,null,8.1])`

Retourneert 18.6.

+++
