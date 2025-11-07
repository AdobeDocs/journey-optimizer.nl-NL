---
product: journey optimizer
title: Lijstfuncties
description: Meer informatie over lijstfuncties
feature: Journeys
role: Developer
level: Experienced
keywords: lijst, functies, expressie, transport, array, collectie
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 5%

---

# Lijstfuncties {#list-functions}

Met lijstfuncties kunt u verzamelingen van waarden bewerken en ermee werken in uw reisexpressies. Deze functies zijn essentieel voor het filteren, sorteren, transformeren en analyseren van arrays en lijsten in uw klantritten.

Gebruik lijstfuncties wanneer u wilt:

* Filter en haal specifieke punten uit inzamelingen uit die op criteria worden gebaseerd ([ filter ](#filter), [ getListItem ](#getListItem))
* Soort en organiseert lijstelementen in het stijgen of dalende orde ([ soort ](#sort))
* Verwijder duplicaten en krijg unieke waarden uit lijsten ([ verschillend ](#distinct), [ separatelyWithNull ](#distinctWithNull))
* Controle als de waarden binnen inzamelingen bestaan ([ binnen ](#in))
* Beperk het aantal punten van een lijst zijn teruggekeerd ([ grens ](#limit))
* Krijg de grootte van een lijst ([ listSize ](#listSize)) of transformatielijsten in verschillende formaten ([ serializeList ](#serializeList))
* Voer vastgestelde verrichtingen als het vinden van gemeenschappelijke elementen tussen lijsten uit ([ snijdt ](#intersect))

Lijstfuncties bieden krachtige gereedschappen voor het werken met complexe gegevensstructuren, waardoor geavanceerde gegevensmanipulatie en voorwaardelijke logica op basis van de inhoud van de verzameling mogelijk zijn.

## distinct {#distinct}

Geeft als resultaat de verschillende waarden of objecten van een bepaalde lijst. Null-items worden genegeerd.

+++Syntaxis

`distinct(<parameters>)`

+++

+++Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te verwerken lijst. Voor listObject moet dit een veldverwijzing zijn. |
| keyAttributeName | string | Deze parameter is optioneel en alleen voor listObject. Wanneer de parameter niet wordt opgegeven, wordt een object als gedupliceerd beschouwd wanneer alle kenmerken dezelfde waarden hebben. Anders wordt een object als gedupliceerd beschouwd wanneer het opgegeven kenmerk dezelfde waarde heeft. |

+++

+++Handtekeningen en geretourneerde typen

`distinct(<listInteger>)`

Retourneert een lijst met gehele getallen.

`distinct(<listDecimal>)`

Retourneert een lijst met decimalen.

`distinct(<listString>)`

Retourneert een lijst met tekenreeksen.

`distinct(<listDateTimeOnly>)`

Keert een lijst van datetimes zonder tijdzone terug te overwegen.

`distinct(<listDateTime>)`

Retourneert een lijst met datetimes.

`distinct(<listDateOnly>)`

Retourneert een lijst met datums.

`distinct(<listBoolean>)`

Retourneert een lijst met laarzen.

`distinct(<listDuration>)`

Retourneert een lijst met tijdsduur.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Retourneert een lijst met objecten.

+++

+++Voorbeelden

`distinct([10,2,10,null])`

Retourneert `[10, 2]` .

+++

## distinctWithNull {#distinctWithNull}

Geeft als resultaat de verschillende waarden of objecten van een bepaalde lijst. Als de lijst ten minste één null-item heeft, wordt een null-waarde weergegeven in de geretourneerde lijst.

+++Syntaxis

`distinctWithNull(<parameters>)`

+++

+++Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Te verwerken lijst. |

+++

+++Handtekeningen en geretourneerde typen

`distinctWithNull(<listInteger>)`

Retourneert een lijst met gehele getallen.

`distinctWithNull(<listDecimal>)`

Retourneert een lijst met decimalen.

`distinctWithNull(<listString>)`

Retourneert een lijst met tekenreeksen.

`distinctWithNull(<listDateTimeOnly>)`

Keert een lijst van datetimes zonder tijdzone terug te overwegen.

`distinctWithNull(<listDateTime>)`

Retourneert een lijst met datetimes.

`distinctWithNull(<listDateOnly>)`

Retourneert een lijst met datums.

`distinctWithNull(<listBoolean>)`

Retourneert een lijst met laarzen.

`distinctWithNull(<listDuration>)`

Retourneert een lijst met tijdsduur.

+++

+++Voorbeelden

`distinctWithNull([10,2,10,null])`

Keert [ 10, 2 terug, ongeldig ]

+++

**Nota:** de parameter `<listObject>` wordt niet gesteund in deze functie.

## filter {#filter}

Retourneert een listObject met objecten waarvan het kenmerk key overeenkomt met een van de opgegeven sleutelwaarden.

+++Syntaxis

`filter(<parameters>)`

+++

+++Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToFilter | listObject | lijst met te filteren objecten. Dit moet een veldverwijzing zijn. |
| keyAttributeName | string | kenmerknaam in de objecten van de opgegeven lijst, gebruikt als sleutel voor filteren |
| keyValueList | list | array van sleutelwaarden voor filteren |

+++

+++Handtekeningen en geretourneerde typen

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Retourneert een listObject.

+++

+++Voorbeelden

Hier volgt een voorbeeld van een payload die wordt doorgegeven in een binnenkomende gebeurtenis &quot;myevent&quot;:

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

U kunt de volgende expressie gebruiken:

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Retourneert een listObject met de twee objecten met &#39;product2&#39; en &#39;product3&#39; als id.

+++

## getListItem {#getListItem}

Retourneert het item van de lijst bij de opgegeven index.

+++Syntaxis

`getListItem(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| index | integer |

+++

+++Handtekeningen en type geretourneerd

`getListItem(<listInteger>,<index>)`

Retourneert een geheel getal.

`getListItem(<listDecimal>,<index>)`

Retourneert een decimaal.

`getListItem(<listString>,<index>)`

Retourneert een tekenreeks.

`getListItem(<listDateTimeOnly>,<index>)`

Retourneert een datetime zonder rekening te houden met tijdzone.

`getListItem(<listDateTime>,<index>)`

Retourneert een datetime.

`getListItem(<listDateOnly>,<index>)`

Retourneert een lijst met datums.

`getListItem(<listBoolean>,<index>)`

Retourneert een Booleaanse waarde.

`getListItem(<listDuration>,<index>)`

Retourneert een duur.

+++

+++Voorbeelden

`getListItem([10, 2, 3], 1)`

Retourneert &quot;2&quot;

`getListItem(["A", "B", "C"], 2)`

Retourneert &quot;C&quot;

Voorbeelden met een gebeurtenisveld &#39;event.appVersion&#39; met waarde: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Retourneert `["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

Retourneert &quot;20&quot;

+++

## in {#in}

Controleert of de waarde van het eerste argument in de lijst voorkomt. De controle wordt uitgevoerd door Gelijk op elke argumentwaarde. De waarde wordt true geretourneerd als de argumentwaarde wordt gevonden, anders false.

Het type van `<expression>` moet met punten van de lijst aanpassen. Typen items in de lijst moeten, ter herinnering, met elkaar overeenkomen.

+++Syntaxis

`in(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| String | String |
| Boolean | Boolean |
| Geheel | Geheel |
| Decimaal | Decimaal |
| Duur | Duur |
| DateTime | DateTime |
| DateTimeOnly | DateTimeOnly |
| Lijst | listString |
| Lijst | listBoolean |
| Lijst | listInteger |
| Lijst | listDecimal |
| Lijst | listDuration |
| Lijst | listDateTime |
| Lijst | listDateTimeOnly |
| Lijst | listDateOnly |

+++

+++Handtekening en type geretourneerd

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Retourneer een booleaanse waarde.

+++

+++Voorbeelden

`in(4,[4,5,3,4])`

Retourneert true.

`in(8,[4,5,3,4])`

Retourneert false.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`

+++

## intersect {#intersect}

Retourneert de gemeenschappelijke waarden in de twee invoerlijsten. Als een van de twee lijsten null is, wordt een lege lijst geretourneerd.

+++Syntaxis

`intersect(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| lijst 1 | list |
| lijst 2 | list |

+++

+++Handtekeningen en geretourneerde typen

`intersect(listString,listString)`: listString

`intersect(listDecimal,listDecimal)`: listDecimal

`intersect(listInteger,listInteger)`: listInteger

`intersect(listDateTime,listDateTime)`: listDateTime

`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly

`intersect(listDateOnly,listDateOnly)`: listDateOnly

`intersect(listDuration,listDuration)`: listDuration

`intersect(listBoolean,listBoolean)` : listBoolean

Retourneert een lijst.

+++

+++Voorbeelden

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Keert [ &quot;sport&quot;terug, &quot;nieuws&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

Hiermee worden algemene items tussen profielkenmerken en een lijst met categorieën geretourneerd.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

Retourneert algemene items tussen profielkenmerken en opgegeven gebeurtenisveld.

+++

## limiet {#limit}

Retourneert de eerste of laatste N-elementen van een lijst.

+++Syntaxis

`limit(<parameters>)`

+++

+++Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te overwegen lijst. Voor listObject moet dit een veldverwijzing zijn. |
| numberOfItems | integer | Aantal items dat moet worden geretourneerd uit de opgegeven lijst. |
| firstOrLastItems | boolean | Deze parameter is optioneel (standaard true). true retourneert de eerste items. false retourneert de laatste items. |

+++

+++Handtekening en type geretourneerd

`limit(<listString>,<integer>)`

`limit(<listString>,<integer>,<boolean>)`

Retourneert een lijst met tekenreeksen.

`limit(<listInteger>,<integer>)`

`limit(<listInteger>,<integer>,<boolean>)`

Retourneert een lijst met gehele getallen.

`limit(<listDecimal>,<integer>)`

`limit(<listDecimal>,<integer>,<boolean>)`

Retourneert een lijst met decimalen.

`limit(<listBoolean>,<integer>)`

`limit(<listBoolean>,<integer>,<boolean>)`

Retourneert een lijst met laarzen.

`limit(<listDateOnly>,<integer>)`

`limit(<listDateOnly>,<integer>,<boolean>)`

Retourneert een lijst met datums.

`limit(<listDateTimeOnly>,<integer>)`

`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Keert een lijst van datetimes zonder tijdzone terug te overwegen.

`limit(<listDateTime>,integer>)`

`limit(<listDateTime>,<integer>,<boolean>)`

Retourneert een lijst met datetimes.

`limit(<listDuration>,<integer>)`

`limit(<listDuration>,<integer>,<boolean>)`

Retourneert een lijst met tijdsduur.

`limit(<listObject>,<integer>)`

`limit(<listObject>,<integer>,<boolean>)`

Retourneert een lijst met objecten.

+++

+++Voorbeelden

`limit(["A", "B", "C", "D", "E"], 3)`

Retourneert `["A","B","C"]` .

`limit(["A", "B", "C", "D", "E"], 3, false)`

Retourneert `["C","D","E"]` .

+++

## listSize {#listSize}

Telt het aantal elementen in de lijst.

+++Syntaxis

`listSize(<parameters>)`

+++

+++Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te verwerken lijst. Voor listObject moet dit een veldverwijzing zijn. Een listObject kan geen null-object bevatten. |

+++

+++Handtekeningen en type geretourneerd

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Retourneer een geheel getal.

`listSize(<listObject>)`

+++

+++Voorbeelden

`listSize([10,2,3])`

Retourneert 3.

`listSize(@event{my_event.productListItems})`

Retourneert het aantal objecten in de opgegeven array met objecten (type listObject).

+++

## serializeList {#serializeList}

Hiermee wordt een bepaalde lijst (elk type behalve listObject) omgezet in een tekenreeks.

+++Syntaxis

`serializeList(<parameters>)`

+++

+++Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Lijst die moet worden omgezet in een tekenreeks. |
| scheidingsteken | string | Scheidingsteken tussen elk lijstelement in de uitvoertekenreeks. |
| addQuotes | boolean | Deze parameter geeft aan of elk element in de uitvoertekenreeks aanhalingstekens moet bevatten (true) of niet (false). |

+++

+++Handtekening en type geretourneerd

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Retourneer een tekenreeks.

+++

+++Voorbeelden

`serializeList(["Hello","World"], " ", false)`

Retourneert &quot;Hello World&quot;.

`serializeList(["Hello", "World"], ",", true)`

Retourneert &quot;&quot;Hello&quot;,&quot;World&quot;&quot;.

+++

## sort {#sort}

Hiermee sorteert u een lijst met waarden of objecten in natuurlijke volgorde.

+++Syntaxis

`sort(<parameters>)`

+++

+++Parameters

| Parameter | Type | Beschrijving |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly of listObject | Te sorteren lijst. Voor listObject moet dit een veldverwijzing zijn. |
| keyAttributeName | string | Deze parameter is alleen voor listObject. De kenmerknaam in de objecten in de lijst wordt gebruikt als sleutel voor sorteren. |
| sortingOrder | boolean | Oplopend (true) of aflopend (false) |

+++

+++Handtekening en type geretourneerd

`sort(<listInteger>,<boolean>)`

Retourneert een lijst met gehele getallen.

`sort(<listDecimal>,<boolean>)`

Retourneert een lijst met decimalen.

`sort(<listString>,<boolean>)`

Retourneert een lijst met tekenreeksen.

`sort(<listDateTimeOnly>,<boolean>)`

Keert een lijst van datetimes zonder tijdzone terug te overwegen.

`sort(<listDateTime>,<boolean>)`

Retourneert een lijst met datetimes.

`sort(<listDateOnly>,<boolean>)`

Retourneert een lijst met datums.

`sort(<listBoolean>,<boolean>)`

Retourneert een lijst met laarzen.

`sort(<listObject>,<string>,<boolean>)`

Retourneert een lijst met objecten.

+++

+++Voorbeelden

`sort(["A", "C", "B"], true)`

Retourneert `["A","B","C"]` .

`sort([1, 3, 2], false)`

Retourneert `[3, 2, 1]` .

`sort(@event{my_event.productListItems}, "SKU", true)`

Retourneert het listObject dat is geordend door het SKU-kenmerk (oplopende volgorde)

+++

