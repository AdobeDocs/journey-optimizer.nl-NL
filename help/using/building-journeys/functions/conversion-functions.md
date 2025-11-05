---
product: journey optimizer
title: Conversiefuncties
description: Meer informatie over conversiefuncties
feature: Journeys
role: Developer
level: Experienced
keywords: conversie, functies, expressie, reis, type, gegoten
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 3%

---

# Conversiefuncties {#conversion-functions}

Met conversiefuncties kunt u gegevens van het ene naar het andere type transformeren binnen de expressies. Deze functies zijn essentieel voor het waarborgen van gegevenscompatibiliteit en een juiste manier van omgaan wanneer u met verschillende gegevensbronnen en -bewerkingen werkt.

Gebruik conversiefuncties wanneer dat nodig is:

* Zet koordwaarden in numeriek, booleaanse, of datumtypes ([&#x200B; toInteger &#x200B;](#toInteger), [&#x200B; toDecimal &#x200B;](#toDecimal), [&#x200B; toBool &#x200B;](#toBool)) om
* Transformeer data en tijden tussen verschillende formaten en vertegenwoordiging ([&#x200B; toDateTime &#x200B;](#toDateTime), [&#x200B; toDateTimeOnly &#x200B;](#toDateTimeOnly), [&#x200B; toDateOnly &#x200B;](#toDateOnly))
* Gegoten numerieke waarden tussen geheel en decimale types ([&#x200B; toInteger &#x200B;](#toInteger), [&#x200B; toDecimal &#x200B;](#toDecimal))
* Zet waarden in koordformaat ([&#x200B; toString &#x200B;](#toString)) of duur ([&#x200B; toDuration &#x200B;](#toDuration)) om
* Zorg voor typecompatibiliteit voor vergelijkingen en bewerkingen
* Gegevens verwerken uit externe bronnen met verschillende typen opmaak

Elke omzettingsfunctie behandelt type-specifieke regels en randgevallen automatisch, die gegevenstransformatie betrouwbaarder en voorspelbaarder in uw reisuitdrukkingen maken.

## toBool {#toBool}

Zet een argumentwaarde in een booleaanse waarde om, afhankelijk van het type.

* Van tekenreeks: probeer de tekenreekswaarde om te zetten als een booleaanse waarde, van &quot;true&quot; als de tekenreekswaarde &quot;true&quot; is, anders false
* Uit numeriek: true wanneer de numerieke waarde niet gelijk is aan 0, anders false

+++Syntaxis

`toBool(<parameter>)`

+++

+++Parameters

* decimaal
* boolean
* string
* integer

+++

+++Handtekeningen en geretourneerde typen

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Retourneer een booleaanse waarde.

+++

+++Voorbeelden

`toBool("true")`

`toBool(1)`

Retourneert true.

`toBool("this is not a boolean")`

Retourneert false.

+++

## toDateOnly {#toDateOnly}

Zet een argument in een dateOnly typewaarde om. Meer over gegevenstypes leren, verwijs naar deze [&#x200B; sectie &#x200B;](../expression/data-types.md).

+++Syntaxis

`toDateOnly(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| Tekenreeksrepresentatie van een datum als &quot;YYYY-MM-DD&quot; (XDM-indeling). Ook steunt formaat ISO-8601: slechts **volledig-datum** deel wordt overwogen (verwijs naar [&#x200B; RFC 3339, sectie 5.6 &#x200B;](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | string |
| datumtijd | dateTime |
| datumtijd zonder tijdzone | dateTimeOnly |
| geheel-getalwaarde van een tijdperk in milliseconden | integer |

+++

+++Handtekeningen en geretourneerde typen

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Retourneert een waarde van het type dateOnly.

+++

+++Voorbeelden

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

retourneren alle objecten dateOnly die 2023-08-18 vertegenwoordigen.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Retourneert alleen date.

+++

## toDateTime {#toDateTime}

Zet parameters om in een datumtijdwaarde, afhankelijk van hun types.

+++Syntaxis

`toDateTime(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd in ISO-8601-indeling | string |
| tijdzone-id | string |
| datumtijd zonder tijdzone | dateTimeOnly |
| geheel-getalwaarde van een tijdperk in milliseconden | integer |

+++

+++Handtekeningen en geretourneerde typen

`toDateTime(<string>)`

`toDateTime(<stringified time zone id>, <dateTimeOnly>)`

`toDateTime(<integer>)`

Keer a **dateTime** terug.

+++

+++Voorbeelden

`toDateTime ("2023-08-18T23:17:59.123Z")`

Keert 2023-08-18T23 :17: 59.123Z terug

`toDateTime(toDateTimeOnly("UTC", "2023-08-18T23:17:59.123"))`

Keert 2023-08-18T23 :17: 59.123Z terug

`toDateTime(1560762190189)`

Keert 2023-06-17T09 :03: 10.189Z terug

+++

>[!NOTE]
>
>Tijdzone-id moet een tekenreeksconstante zijn. Het kan geen veldverwijzing of expressie zijn. Voor meer informatie over gegevenstypes, verwijs naar [&#x200B; deze pagina &#x200B;](../expression/data-types.md).

## toDateTimeOnly {#toDateTimeOnly}

Zet een argumentwaarde in een waarde van de datumtijd slechts om.

+++Syntaxis

`toDateTimeOnly(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| datumtijd in de notatie ISO-8601 of &quot;JJJ-MM-DD&quot; (XDM-datumnotatie) | string |
| datumtijd | dateTime |

+++

+++Handtekeningen en geretourneerde typen

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`

Retourneer een datetime zonder rekening te houden met tijdzone.

+++

+++Voorbeelden

`toDateTimeOnly ("2023-08-18")`

keert dateTime terug die 2023-08-18T00 :00: 00.000 vertegenwoordigt

`toDateTimeOnly(now())`

+++

## toDecimal {#toDecimal}

Zet een argumentwaarde in een decimale waarde om, afhankelijk van het type.

+++Syntaxis

`toDecimal(<parameter>)`

+++

+++Parameters

| Parameter | Beschrijving |
|--- |--- |
| string | converteert de tekenreekswaarde als een decimaal |
| dateTime | zet de datum om als aantal milliseconden (epoch milliseconds) |
| boolean | Zet de booleaanse waarde om als 1 indien waar (true), 0 indien onwaar (false) |
| integer | wordt omgezet in decimaal (voorbeeld.: 1 wordt 1,0) |

+++

+++Handtekeningen en geretourneerde typen

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Retourneer een decimaal.

+++

+++Voorbeelden

`toDecimal("4.0")`

Retourneert 4.0.

+++

## toDuration {#toDuration}

Zet een argumentwaarde in een duur om. Voor meer informatie over gegevenstypes, verwijs naar [&#x200B; deze pagina &#x200B;](../expression/data-types.md).

+++Syntaxis

`toDuration(<parameter>)`

+++

+++Parameters

| Parameter | Beschrijving |
|--- |--- |
| string | formaten die gebaseerd zijn op de ISO-8601-duurnotatie PnDTnHnMn.nS met dagen waarvan wordt aangenomen dat ze precies 24 uur zijn |
| integer | aantal milliseconden |

Als tekenreeksexpressie: geaccepteerde notaties zijn gebaseerd op de ISO-8601-duurnotatie PnDTnHnMn.nS met dagen die worden beschouwd als precies 24 uur.

De tekenreeks begint met een optioneel teken, aangeduid met het negatieve of positieve ASCII-symbool. Indien negatief, wordt de hele periode genegeerd. De ASCII-letter &quot;P&quot; staat vervolgens in hoofdletters of kleine letters. Er zijn dan vier secties, elk bestaande uit een getal en een achtervoegsel. De secties hebben achtervoegsels in ASCII van &quot;D&quot;, &quot;H&quot;, &quot;M&quot; en &quot;S&quot; gedurende dagen, uren, minuten en seconden, die in hoofdletters of in kleine letters worden geaccepteerd. De achtervoegsels moeten op volgorde voorkomen. De ASCII-letter &quot;T&quot; moet vóór het eerste exemplaar van een uur-, minuut- of tweede sectie plaatsvinden, indien aanwezig. Ten minste één van de vier delen moet aanwezig zijn en indien &quot;T&quot; aanwezig is, moet er ten minste één deel na &quot;T&quot; aanwezig zijn. Het nummerdeel van elke sectie moet uit een of meer ASCII-cijfers bestaan. Het getal kan worden voorafgegaan door het negatieve of positieve ASCII-symbool. Het aantal dagen, uren en minuten moet worden geparseerd. Het aantal seconden moet samen met de optionele breuk parseren. Het decimale punt kan een punt of een komma zijn. Het fractionele deel kan van nul tot 9 cijfers hebben.

+++

+++Handtekeningen en type geretourneerd

`toDuration(<string>)`

`toDuration(<integer>)`

Retourneert een duur.

+++

+++Voorbeelden

`toDuration("PT10H")`

Geeft een duur van 10 uur.

`toDuration("PT4S")`

Retourneert de duur van 4s.

`toDuration(4000)`

Retourneert de duur van 4s.

+++

## toInteger {#toInteger}

Zet een argumentwaarde in een geheel getal om.

+++Syntaxis

`toInteger(<parameter>)`

+++

+++Parameters

| Parameter | Beschrijving |
|--- |--- |
| string | converteert de tekenreekswaarde als een geheel getal |
| dateTime | zet de datum om als aantal milliseconden (epoch milliseconds) |
| decimaal | converteert naar geheel getal door het decimale gedeelte te verwijderen (1,5 wordt bijvoorbeeld 1). |
| boolean | Zet de booleaanse waarde om als 1 indien waar (true), 0 indien onwaar (false) |

+++

+++Handtekeningen en type geretourneerd

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Retourneer een geheel getal.

+++

+++Voorbeelden

`toInteger("4")`

Retourneert 4.

+++

## toString {#toString}

Zet een argumentwaarde in een koordwaarde om, afhankelijk van zijn type. Voor meer informatie over gegevenstypes, verwijs naar [&#x200B; deze pagina &#x200B;](../expression/data-types.md).

+++Syntaxis

`toString(<parameter>)`

+++

+++Parameters

| Parameter | Beschrijving |
|--- |--- |
| dateTime | converteert de datum in UTC-datumnotatie |
| dateTimeOnly | converteert de datum in UTC-datumnotatie |
| duur | converteren naar het overeenkomstige aantal milliseconden als een tekenreeks |
| integer | converteert naar tekenreeksrepresentatie van de waarde (1 wordt &quot;1&quot;) |
| decimaal | converteert naar tekenreeksrepresentatie van de waarde (1,5 wordt &quot;1,5&quot;) |
| boolean | Zet de booleaanse waarde om als &#39;true&#39; (waar), &#39;false&#39; (onwaar) |

+++

+++Handtekeningen en type geretourneerd

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Retourneer een tekenreeks.

+++

+++Voorbeelden

`toString(4)`

Retourneert &quot;4&quot;.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Retourneert de tekenreeksrepresentatie van het opgegeven veld dateOnly (XDM Date-veld), bijvoorbeeld &quot;2023-08-18&quot;.

`toString(toDuration(1520))`

Retourneert &quot;PT1.52S&quot;.

+++

