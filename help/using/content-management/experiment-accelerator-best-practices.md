---
solution: Journey Optimizer
product: journey optimizer
title: Aanbevolen procedures voor Journey Optimizer Experimentation Accelerator
description: Verbeter uw vermogen om experimenten effectief uit te voeren en inzichten te genereren
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: inhoud, experiment, meerdere, publiek, behandeling
hide: true
hidefromtoc: true
source-git-commit: ddeb3512fbe1d1de86456fe2c3ccd2b3805b5684
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Aanbevolen procedures voor Journey Optimizer Experimentation Accelerator {#content-experiment-best-practices}

>[!BEGINSHADEBOX]

* [Aan de slag met de Journey Optimizer Experimentation Accelerator](experiment-accelerator.md)
* **[de beste praktijken van Journey Optimizer Experimentation Accelerator](experiment-accelerator-best-practices.md)**
* [Privacy, beveiliging en bestuur in Journey Optimizer Experimentation Accelerator](experiment-accelerator-security.md)
* [Monitorexperimenten](experiment-accelerator-monitor.md)
* [Metrische experimenten](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

## Wat is een A/B-test?

A/B het testen is het proces om twee of meer versies van iets te vergelijken om te bepalen wat beter tegen een bepaald doel presteert.

Deelnemers worden willekeurig toegewezen aan één versie, een zogenaamde variant, en hun gedrag wordt bijgehouden. De resultaten laten zien of de ene versie de andere statistisch overtreft.

## Belangrijke terminologie

| Term | Definitie |
|-|-|
| Besturing | De oorspronkelijke versie die als basislijn voor vergelijking wordt gebruikt. |
| Variant of behandeling | Een nieuwe versie die wordt gecreeerd om tegen de controle te testen. |
| Hypothese | Een voorspelling over welke verandering een beter resultaat zal opleveren, en waarom. |
| Monstergrootte | Het aantal personen of sessies dat in de test is opgenomen. |
| Statistische significantie | Een zekere mate van vertrouwen dat de resultaten niet te wijten zijn aan willekeurige toeval. |
| Optillen | De procentuele verbetering of afname van een variant in vergelijking met de controle. |
| Primair metrisch | De belangrijkste maatstaf die wordt gebruikt om het succes van de test te bepalen. |
| Secundaire cijfers | Metrische gegevens ondersteunen die extra insight bieden of helpen bij het controleren op onbedoelde effecten. |
| Vertrouwelijk interval | Het geschatte bereik waarbinnen het werkelijke effect waarschijnlijk zal dalen. |
| Segment | Een specifieke deelgroep van het publiek die onafhankelijk wordt geanalyseerd (bijvoorbeeld nieuwe gebruikers, mobiele bezoekers). |

## Aanbevolen werkwijzen voor het uitvoeren van experimenten

* **Begin met een duidelijke hypothese**

  Een sterke hypothese omvat wat je verandert, wat je verwacht te gebeuren, en waarom.
Voorbeeld: _wij geloven dat het veranderen van X Y wegens Z zal verhogen._

* **bepaalt een zinvol metrisch succes**

  Kies metrisch die zich op uw bredere doelstellingen richt. Vermijd &#39;ijdelheid&#39; metriek die er goed uitziet, maar die geen echte impact weerspiegelt.

* **Test één verandering in tijd (wanneer mogelijk)**

  Door variabelen te isoleren, kunt u de resultaten beter interpreteren. Als u meerdere wijzigingen tegelijk test, weet u wellicht niet wat het effect heeft veroorzaakt.

* **laat de test lang genoeg lopen**

  Voortijdige conclusies kunnen misleidend zijn. Wacht op een statistisch significante steekproefgrootte alvorens te handelen.

* **ben zich bewust van externe factoren**

  Seizoensgebondenheid, feestdagen en andere wijzigingen in uw omgeving kunnen de resultaten scheeftrekken. Documenteer alles wat het gedrag tijdens de test kan beïnvloeden.

* **de segmentatie van het Gebruik bewust**

  Als u de resultaten opsplitst per publiekssegment, worden verborgen patronen zichtbaar, maar worden kleine voorbeeldgrootten niet te veel geïnterpreteerd.

* **Document en deel lessen**

  Houd een duidelijk overzicht van wat werd getest, waarom, en wat u leerde. Dit bouwt institutionele kennis op en voorkomt herhalende fouten.

## Algemene meetwaarden

| Metrisch | Wat zij doet | Wanneer gebruiken |
|-|-|-|
| Conversiesnelheid | Het percentage gebruikers dat een gewenste actie uitvoert | Nuttig voor het bijhouden van het succes van een doelgerichte ervaring |
| Doorkliksnelheid (CTR) | Het percentage gebruikers dat op een specifiek element klikt | Geeft aan hoe aansprekend de ervaring is |
| Betrokkenheid | Het niveau van interactie heeft de gebruikers met de ervaring | Goed voor het meten van interesse of aandacht |
| Stuitsnelheid | Het percentage gebruikers dat snel vertrekt zonder actie te ondernemen | Kan een slechte passie of verwarrende ervaring aangeven |
| Tijd op pagina | De hoeveelheid tijd die gebruikers besteden aan een specifiek deel van de ervaring | Kan diepte van interesse of complexiteit weerspiegelen |
| Opbrengst per bezoeker (RPV) | Gemiddelde opbrengst verdiend per gebruiker | Vaak gebruikt bij commerciële proeven |
| Bewaarfactor | Het percentage gebruikers dat na verloop van tijd terugkeert of betrokken blijft | Nuttig voor waardebeoordelingen op lange termijn |

## Wat maakt een goed experiment?

Een goed experiment levert niet alleen een win-winsituatie op, maar levert ook een duidelijk, actief leren op.
Hier is wat om te zoeken:

&controle; **Statistisch Vertrouwen**: Het verschil tussen varianten is waarschijnlijk niet toe te schrijven aan toeval.
&controle; **richt zich op Doelstellingen**: primaire metrisch wijst op betekenisvolle vooruitgang naar een bedrijfsdoelstelling.
&controle; **Secundaire Gevolgen**: Geen significante negatieve nevengevolgen op verwante metriek.
&controle; **Schaalbaarheid**: Het resultaat kan toekomstige besluiten informeren of aan andere gebieden worden algemeen gemaakt.
&controle; **Duidelijkheid**: De oorzaak van het resultaat is redelijk geïsoleerd en begrepen.

Experimentatie gaat niet alleen over het vinden van de &quot;beste&quot; versie, het gaat over het opbouwen van kennis door middel van testen en iteratie. Als het goed gaat, onthullen de experimenten inzichten die slimmere beslissingen, betere gebruikerservaring en betere resultaten stimuleren.

>[!BEGINSHADEBOX]

**Voorbeeld:**

* **Bedrijf**: De ketting van het hotel
* **Samenvatting**: Als wij urgentere taal op de homepage gebruiken, zal het tot meer reserveringen leiden.
   * **Controle**: Oorspronkelijke versie
   * **Variant**: Nieuwe toegevoegde versie met urgentie
   * **Primair Metrisch**: Het tarief van het boek
   * **Secundaire Metriek**: Stuiteren tarief, tijd op plaats
* **Resultaat**: De variant produceerde een 14% lift in boekingstarief, zonder negatieve verandering in andere metriek.
* **Actie**: Overweeg het rollen van de variant en de lopende follow-up experimenten om gelijkaardige benaderingen op andere gebieden te testen.

>[!ENDSHADEBOX]
