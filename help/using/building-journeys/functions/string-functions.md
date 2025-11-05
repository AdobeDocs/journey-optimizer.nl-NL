---
product: journey optimizer
title: Reeksfuncties
description: Meer informatie over tekenreeksfuncties
feature: Journeys
role: Developer
level: Experienced
keywords: tekenreeks, functies, expressie, reis, tekst, manipulatie
version: Journey Orchestration
source-git-commit: d58319d687d113ce680c415524fdea0400cb38f0
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 6%

---

# Reeksfuncties {#string-functions}

Met tekenreeksfuncties kunt u tekstwaarden bewerken en ermee werken binnen uw reisexpressies. Deze functies zijn van essentieel belang voor tekstverwerking, validatie, transformatie en analyse in uw klantenreizen.

Gebruik tekenreeksfuncties wanneer u wilt:

* Meerdere tekstwaarden samenvoegen en combineren
* Specifieke tekstpatronen of subtekenreeksen zoeken
* Tekenreeksen vergelijken met hoofdlettergevoelig of hoofdlettergevoelig zoeken
* Delen van tekst extraheren met subtekenreeksbewerkingen
* Tekst omzetten in hoofdletters of kleine letters
* Controleren of tekenreeksen leeg zijn of specifieke waarden bevatten
* Tekstpatronen vervangen door nieuwe waarden
* Tekenreeksen splitsen in arrays voor verdere verwerking
* Tekst valideren met reguliere expressies

Tekenreeksfuncties bieden uitgebreide mogelijkheden voor tekstmanipulatie, waardoor geavanceerde gegevensverwerking en voorwaardelijke logica mogelijk zijn op basis van tekstinhoud in uw reisexpressies.

## concat {#concat}

Voegt twee tekenreeksparameters of een lijst met tekenreeksen samen.

+++Syntaxis

`concat(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| Lijst | listString |
| string | string |

+++

+++Handtekening en type geretourneerd

`concat(<string>,<string>)`

`concat(<listString>)`

Retourneert een tekenreeks.

+++

+++Voorbeelden

`concat("Hello","World")`

Retourneert &quot;HelloWorld&quot;.

`concat(["Hello"," ","World"])`

Retourneert &quot;Hello World&quot;.

+++

## contain {#contain}

Controleert of de tweede argumenttekenreeks zich in de eerste argumenttekenreeks bevindt.

+++Syntaxis

`contain(<parameters>)`

+++

+++Parameters

* string

+++

+++Handtekening en type geretourneerd

`contain(<string>,<string>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`contain("rowing is great", "great")`

Retourneert true.

+++

## containIgnoreCase {#containIgnoreCase}

Controleert of de tweede argumenttekenreeks zich in de eerste argumenttekenreeks bevindt, zonder rekening te houden met de case.

+++Syntaxis

`containIgnoreCase(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| string | string |
| doorzocht tekenreeks | string |

+++

+++Handtekening en type geretourneerd

`containIgnoreCase(<string>,<string>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`containIgnoreCase("rowing is great", "GREAT")`

Retourneert true.

+++

## endWith {#endWith}

Retourneert true als de tweede parameter een achtervoegsel van de eerste parameter is.

+++Syntaxis

`endWith(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| string | string |
| achtervoegsel | string |

+++

+++Handtekening en type geretourneerd

`endWith(<string>,<string>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`endWith("Hello World", "World")`

Retourneert true.

`endWith("Hello World", "Hello")`

Retourneert false.

+++

## endWithIgnoreCase {#endWithIgnoreCase}

Controleert of de tekenreeks van het eerste argument eindigt met een specifieke tekenreeks (tekenreeks van het tweede argument), waarbij geen rekening wordt gehouden met het geval.

+++Syntaxis

`endWithIgnoreCase(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| string | string |
| achtervoegsel | string |

+++

+++Handtekening en type geretourneerd

`endWithIgnoreCase(<string>,<string>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`endWithIgnoreCase("rowing is great", "AT")`

Retourneert true.

+++

## equalIgnoreCase {#equalIgnoreCase}

Vergelijkt de eerste argumenttekenreeks met de tweede argumenttekenreeks, waarbij rekening wordt gehouden met hoofdletters en kleine letters.

+++Syntaxis

`equalIgnoreCase(<parameters>)`

+++

+++Parameters

* string

+++

+++Handtekening en type geretourneerd

`equalIgnoreCase(<string>,<string>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`equalIgnoreCase("rowing is great", "rowing is GREAT")`

Retourneert true.

+++

## indexOf {#indexOf}

Retourneert de positie (in het eerste argument) van de eerste instantie van de tweede parameter. Retourneert -1 als er geen overeenkomend actiepunt is.

+++Syntaxis

`indexOf(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| string | String |
| opgegeven waarde | String |

+++

+++Handtekening en type geretourneerd

`indexOf(<string>,<string>)`

Retourneert een geheel getal.

+++

+++Voorbeelden

`indexOf("Hello", "l")`

Retourneert 2.

Uitleg:

In &quot;Hello&quot; staat de eerste instantie van &quot;l&quot; op positie 2.

+++

## isEmpty {#isEmpty}

Retourneert true als de tekenreeks in de parameter geen teken heeft.

+++Syntaxis

`isEmpty(<parameters>)`

+++

+++Parameters

* string

+++

+++Handtekening en type geretourneerd

`isEmpty(<string>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`isEmpty("")`

Retourneert true.

`isEmpty("Hello World")`

Retourneert false.

+++

## isNotEmpty {#isNotEmpty}

Retourneert true als de tekenreeks in de parameter niet leeg is.

+++Syntaxis

`isNotEmpty(<parameters>)`

+++

+++Parameters

* string

+++

+++Handtekening en type geretourneerd

`isNotEmpty(<string>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`isNotEmpty("")`

Retourneert false.

`isNotEmpty("hello")`

Retourneert true.

+++

## lastIndexOf {#lastIndexOf}

Retourneert de positie (in het eerste argument) van de laatste instantie van de tweede parameter. Retourneert -1 als er geen overeenkomend actiepunt is.

+++Syntaxis

`lastIndexOf(<parameters>)`

+++

+++Parameter

| Parameter | Type |
|-----------|------------------|
| string | String |
| opgegeven waarde | String |

+++

+++Handtekening en type geretourneerd

`lastIndexOf(<string>,<string>)`

Retourneert een geheel getal.

+++

+++Voorbeelden

`lastIndexOf("Hello", "l")`

Retourneert 3.

Uitleg:

In &quot;Hello&quot; bevindt de laatste instantie van &quot;l&quot; zich op positie 3.

+++

## lengte {#length}

Retourneert het aantal tekens van de tekenreeksexpressie in de parameter.

+++Syntaxis

`length(<parameters>)`

+++

+++Parameter

* string

+++

+++Handtekening en type geretourneerd

`length(<string>)`

Retourneert een geheel getal.

+++

+++Voorbeelden

`length("Hello World")`

Retourneert 11.

+++

## lower {#lower}

Retourneert een versie in kleine letters van de parameter.

+++Syntaxis

`lower(<parameter>)`

+++

+++Parameter

* string

+++

+++Handtekening en type geretourneerd

`lower(<string>)`

Retourneert een tekenreeks.

+++

+++Voorbeelden

`lower("A")`

Retourneert &quot;a&quot;.

+++

## matchRegExp {#matchRegExp}

Retourneert true als de tekenreeks in de eerste parameter overeenkomt met de reguliere expressie in de tweede parameter. Voor meer informatie, zie [&#x200B; deze pagina &#x200B;](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

+++Syntaxis

`matchRegExp(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|--- |--- |
| string | string |
| regexp | string |

+++

+++Handtekening en type geretourneerd

`matchRegExp(<string>,<string>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`matchRegExp("12345", "\\d+")`

Retourneert true.

+++

## notEqualIgnoreCase {#notEqualIgnoreCase}

Controleer of de eerste argumenttekenreeks met de tweede argumenttekenreeks anders is, waarbij rekening wordt gehouden met hoofdletters en kleine letters.

+++Syntaxis

`notEqualIgnoreCase(<parameters>)`

+++

+++Parameters

* string

+++

+++Handtekening en type geretourneerd

`notEqualIgnoreCase(<string>,<string>)`

Retourneert een Booleaanse waarde.

+++

+++Voorbeelden

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`

+++

## replace {#replace}

Vervangt de eerste instantie die overeenkomt met de doeltekenreeks door de vervangende tekenreeks in de basistekenreeks.

De vervanging vindt plaats vanaf het begin van de tekenreeks tot het einde. Als u bijvoorbeeld &quot;aa&quot; vervangt door &quot;b&quot; in de tekenreeks &quot;aaa&quot;, resulteert dit in &quot;ba&quot; in plaats van &quot;ab&quot;.

+++Syntaxis

`replace(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|--------------|
| basis | string |
| target | tekenreeks (RegExp) |
| vervanging | string |

+++

+++Handtekening en type geretourneerd

`replace(<base>,<target>,<replacement>)`

Retourneer een tekenreeks.

+++

+++Voorbeelden

`replace("Hello World", "l", "x")`

Retourneert &quot;Hexlo World&quot;.

**Voorbeeld met RegExp:**

Omdat de doelparameter een RegExp is, moet u, afhankelijk van de tekenreeks die u wilt vervangen, mogelijk enkele tekens verwijderen. Hier volgt een voorbeeld:

* te evalueren tekenreeks: `|OFFER_A|OFFER_B`
* opgegeven door een profielkenmerk `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Te vervangen tekenreeks: `|OFFER_A`
* Tekenreeks vervangen door: `''`
* U moet `\\` vóór het `|` -teken toevoegen.

De expressie is:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

De geretourneerde tekenreeks is: `|OFFER_B`

U kunt ook de tekenreeks maken die moet worden vervangen door een bepaald kenmerk:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`

+++

## replaceAll {#replaceAll}

Vervangt alle instanties die overeenkomen met de doeltekenreeks door de vervangende tekenreeks in de basistekenreeks.

De vervanging vindt plaats vanaf het begin van de tekenreeks tot het einde. Als u bijvoorbeeld &quot;aa&quot; vervangt door &quot;b&quot; in de tekenreeks &quot;aaa&quot;, resulteert dit in &quot;ba&quot; in plaats van &quot;ab&quot;.

+++Syntaxis

`replaceAll(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|--------------|
| basis | string |
| target | tekenreeks (RegExp) |
| vervanging | string |

+++

+++Handtekening en type geretourneerd

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Retourneert een tekenreeks.

+++

+++Voorbeelden

`replaceAll("Hello World", "l", "x")`

Retourneert &quot;hexo Worxd&quot;.

Omdat de doelparameter een RegExp is, moet u, afhankelijk van de tekenreeks die u wilt vervangen, mogelijk enkele tekens verwijderen. Verwijs naar het voorbeeld in [&#x200B; vervangen &#x200B;](#replace) functie.

+++

## split {#split}

Splitst de eerste argumenttekenreeks op met een scheidingstekenreeks (tweede argumenttekenreeks, die een reguliere expressie kan zijn) om een lijst met tekenreeksen (tokens) te maken.

+++Syntaxis

`split(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-----------|------------------|
| invoertekenreeks | string |
| scheidingstekenreeks | string |

+++

+++Handtekeningen en type geretourneerd

`split(<input string>, <separator string>)`

Retourneert een listString.

+++

+++Voorbeelden

`split("A_B_C", "_")`

Retourneert `["A","B","C"]`

Voorbeeld met een gebeurtenisveld &#39;event.appVersion&#39; met waarde: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Retourneert `["20", "45", "2", "3434"]`

+++

## startWith {#startWith}

Retourneert true als de tweede parameter een voorvoegsel van de eerste is.

+++Syntaxis

`startWith(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-------------|--------|
| string | string |
| prefix | string |

+++

+++Handtekening en type geretourneerd

`startWith(<string>,<string>)`

Retourneer een booleaanse waarde.

+++

+++Voorbeelden

`startWith("Hello World", "Hello")`

Retourneert true.

`startWith("Hello World", "World")`

Retourneert false.

+++

## startWithIgnoreCase {#startWithIgnoreCase}

Retourneert true als de tweede parameter een voorvoegsel van de eerste is zonder rekening te houden met hoofdletters en kleine letters.

+++Syntaxis

`startWithIgnoreCase(<parameters>)`

+++

+++Parameters

| Parameter | Type |
|-------------|--------|
| string | string |
| prefix | string |

+++

+++Handtekening en type geretourneerd

`startWithIgnoreCase(<string>,<string>)`

Retourneer een booleaanse waarde.

+++

+++Voorbeelden

`startWithIgnoreCase("rowing is great", "RO")`

Retourneert true.

+++

## substr {#substr}

Retourneert de subtekenreeks van de tekenreeksexpressie tussen de beginindex en de eindindex. Als de eindindex niet is gedefinieerd, ligt deze tussen de beginindex en het einde.

+++Syntaxis

`substr(<parameters>)`

+++

+++Parameters

| Parameter | type |
|-------------|----------|
| string | string |
| beginIndex | integer |
| endIndex | integer |

+++

+++Handtekening en type geretourneerd

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Retourneer een tekenreeks.

+++

+++Voorbeelden

`substr("Hello World",6)`

Retourneert &quot;World&quot;.

`substr("Hello World", 0, 5)`

Retourneert &quot;Hello&quot;.

+++

## trim {#trim}

Hiermee verwijdert u begin- en eindruimten.

+++Syntaxis

`trim(<parameters>)`

+++

+++Parameter

| Parameter | Type |
|-----------|------------------|
| string | string |

+++

+++Handtekening en type geretourneerd

`trim(<string>)`

Retourneer een tekenreeks.

+++

+++Voorbeelden

`trim(" Hello ")`

Retourneert &quot;Hello&quot;.

+++

## upper {#upper}

Retourneert een hoofdletterversie van de parameter.

+++Syntaxis

`upper(<parameters>)`

+++

+++Handtekening en type geretourneerd

`upper(<string>)`

Retourneer een tekenreeks.

+++

+++Voorbeelden

`upper("b")`

Retourneert &quot;B&quot;.

+++

## uuid {#uuid}

Genereert een willekeurige UUID (Universal Unique IDentifier).

+++Syntaxis

`uuid()`

+++

+++Parameters 

Voor deze functie zijn geen parameters vereist.

+++

+++Handtekening en type geretourneerd

`uuid()`

Retourneert een tekenreeks.

+++

+++Voorbeelden

`uuid()`

Retourneert &quot;79e70b7f-8a85-400b-97a1-9f9826121553&quot;.

+++

