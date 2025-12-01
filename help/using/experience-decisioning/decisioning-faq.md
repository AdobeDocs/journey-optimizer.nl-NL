---
title: Veelgestelde vragen over besluitvorming
description: Antwoorden ophalen voor algemene vragen over mogelijkheden voor besluitvorming
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: e42640e791e6bec3bfd09a3095bad5e44e2ab128
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---

# Veelgestelde vragen over besluitvorming {#decisioning-faq}

Deze pagina biedt antwoorden op veelgestelde vragen over beslissingsmogelijkheden in Adobe Journey Optimizer.

## Afdekregels {#capping-rules}

+++**wat gebeurt wanneer de veelvoudige het capken regels op één enkele aanbieding worden toegepast?**

Een aanbieding wordt beperkt zodra **om het even welke enige voorwaarde wordt voldaan**. Wanneer de veelvoudige het begrenzen regels bestaan, houdt de aanbieding op worden getoond zodra om het even welke regel zijn drempel bereikt.

**Voorbeeld:**
Als u twee plafondregels voor een aanbieding definieert:
* 5 keer per profiel per week
* 100 keer totaal voor alle gebruikers

Het aanbod wordt niet meer weergegeven aan een gebruiker als deze het vijf keer per week heeft gezien, zelfs als de totale limiet van 100 nog niet is bereikt. Op dezelfde manier, zodra 100 totale indrukken worden bereikt, houdt de aanbieding op worden getoond aan alle gebruikers.

Leer meer over [ het begrenzen regels ](items.md#capping).

+++

## Beoordelingsformule {#ranking-formulas}

+++**wat is de rol van publiek in AI modellen?**

Wanneer het vormen van [ gepersonaliseerde optimaliseringsmodellen ](ranking/personalized-optimization-model.md), zowel dienen de datasets als het publiek verschillende doeleinden:

* **Datasets**: De omzettingsgebeurtenissen van de Vangst (kliks, orden, opbrengst) die als optimaliseringsdoelstellingen voor het model dienen.
* **Soorten publiek**: Functie als voorspellende variabelen die het model toelaten om aanbevelingen te personaliseren die op het lidmaatschap van het klantensegment worden gebaseerd.

Het publiek beperkt of vergroot het bereik van het model niet. In plaats daarvan, verstrekken zij contextafhankelijke attributen die de capaciteit van het model verbeteren om gepersonaliseerde voorspellingen over verschillende klantensegmenten te maken.

Beide componenten zijn vereist voor effectieve gepersonaliseerde prestaties van het optimalisatiemodel. Leer meer over [ AI modellen ](ranking/ai-models.md).

+++

+++**hoe veranderingen om inzamelingen aan te bieden AI modellen als het gebruiken van auto-optimalisering of gepersonaliseerde optimalisatiemodellen beïnvloeden?**

Beide modellen zullen verkeer aan de volgende beste beschikbare aanbieding leveren die op verkeersgegevens van de laatste 30 dagen wordt gebaseerd.

Wanneer verscheidene aanbiedingen gelijktijdig worden verwijderd en de resterende aanbiedingen minimale verkeersgegevens binnen het venster van 30 dagen hebben, kan het model suboptimaal gedrag, met inbegrip van vertonen:
* Willekeurige distributiepatronen
* Bias naar aanbiedingen met hogere omrekeningskoersen op basis van beperkte beeldgegevens

**Beste praktijken**: Wanneer het wijzigen van aanbiedingsinzamelingen beduidend, verifieer dat de resterende aanbiedingen voldoende historische prestatiesgegevens hebben om modeldoeltreffendheid te handhaven.

+++

+++**hoe snel AI modellen nieuwe aanbiedingen opnemen?**

In AI-modellen worden nieuwe aanbiedingen tijdens de volgende trainingscyclus geïdentificeerd en getest:

* **auto-optimalisering**: De dagelijkse trainingslooppas
* **Gepersonaliseerde optimalisering**: Wekelijkse opleidingslooppas

Zodra beide modellen zijn geïdentificeerd, zullen zij onmiddellijk de nieuwe aanbiedingen aan sommige bezoekers gaan bedienen om hun prestaties te testen en gegevens over hun doeltreffendheid te verzamelen.

Leer meer over [ auto-optimalisering ](ranking/auto-optimization-model.md) en [ gepersonaliseerde optimalisering ](ranking/personalized-optimization-model.md) modellen.

+++

+++**hoe AI modellen zonder controlegroepen optimaliseren?**

Zowel auto-optimalisering als gepersonaliseerde optimalisatiemodellen maken gebruik van een onderzoek-exploiterende strategie die de behoefte aan specifieke controlegroepen elimineert:

* **Aanvankelijke fase**: De modellen beginnen met 100% exploratie, testend verschillende aanbiedingen om basislijnprestatiesgegevens te vestigen.
* **Aangepaste optimalisering**: Aangezien de gedragsgebeurtenissen zich ophopen en de voorspellingsnauwkeurigheid verbetert, brengen de modellen automatisch exploratie en exploitatie in evenwicht.
* **het Leren**: Het systeem wijst progressief meer verkeer aan hoog-presterende aanbiedingen toe terwijl het blijven om alternatieven te testen.

Dit verzekert ononderbroken het leren en optimalisering over al verkeer zonder afzonderlijke controlegroepen te vereisen.

+++

+++**wat zijn de minimumverkeersvereisten voor optimale AI modelprestaties?**

Adobe beveelt de volgende minimumdrempels aan om effectieve modelprestaties te garanderen:

**geadviseerde minimum (per week):**
* 1.000 afbeeldingen per aanbieding/object
* 100 conversiegebeurtenissen per aanbieding/object

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

Standaard probeert het systeem geen gepersonaliseerde modellen te maken voor aanbiedingen/items met minder dan 1000 afbeeldingen of 50 conversiegebeurtenissen.

>[!NOTE]
>
>In productieomgevingen met grote aanbiedingen voor catalogi (~300 aanbiedingen) en restrictieve bedrijfsregels, kunnen sommige aanbiedingen lagere absolute drempels benaderen (250 beelden en 25 omzettingen per 30 dagen). Deze zijn de minimale gegevensvereisten voor modeltraining, maar bieden mogelijk geen garantie voor optimale prestaties.

Leer meer over [ vereisten van de gegevensinzameling ](data-collection/data-collection.md).

+++

+++**hoe aanbiedt gelijkenis AI modelprestaties beïnvloedt?**

AI-modellen leveren grotere voordelen op voor de personalisatie wanneer ze een beroep doen op verschillende klantsegmenten. Wanneer aanbiedingen sterk op elkaar lijken, zijn twee resultaten typisch:

* **Equivalente prestaties**: De aanbiedingen presteren identiek en ontvangen ongeveer gelijke verkeersdistributie.
* **Dominante aanbieding**: De kleine verschillen veroorzaken één aanbieding om anderen over alle segmenten te overtreffen, die de meerderheid van verkeer vangen.

>[!NOTE]
>
>De differentiatie van het aanbod waarborgt geen evenwichtige verkeersverdeling. Aanbiedingen met objectief superieure waardevoorstellen (bijvoorbeeld een korting van € 100 tegenover een korting van € 50) zullen doorgaans overheersen in alle klantensegmenten, ongeacht de inspanningen voor personalisatie.

**Beste praktijken**: De aanbiedingen van het ontwerp met betekenisvolle differentiatie die zich op verschillende voorkeur van het klantensegment richten om AI modeldoeltreffendheid te maximaliseren.

+++

+++**hoe beïnvloedt verkeersanomalieën AI modelprestaties?**

Verkeersanomalieën worden proportioneel in het model opgenomen binnen het rolvenster van 30 dagen.

**Gevolgen beoordeling:**
Een tijdelijke verkeerspiek (bijvoorbeeld, 2x dagelijks verkeer) heeft minimaal effect op algemene modelprestaties omdat het afwijkende verkeer een kleine fractie van de dataset van 30 dagen vertegenwoordigt.

**Zeer belangrijke insight**: Het het rollen gegevensvenster van 30 dagen verstrekt modelstabiliteit tijdens tijdelijke verkeersschommelingen. Snellerechikes of druppels verstoren modelvoorspellingen of prestaties niet significant.

+++

## Verwante onderwerpen {#related-topics}

<!--* [Get started with Decisioning](gs-experience-decisioning.md)-->
* [Beslissingsitems maken](items.md)
* [Overzicht van AI-modellen](ranking/ai-models.md)
* [Afbakening en beperkingen](decisioning-guardrails.md)

