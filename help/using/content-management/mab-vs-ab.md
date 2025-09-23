---
title: Statistische berekeningen in het kader van het experimentatierapport
description: Meer informatie over A/B testen versus multigewapende bandit
feature: A/B Testing, Experimentation
role: User
level: Experienced
source-git-commit: 397fad9c95e0c11c0496ab5c9adfb6f8169de4f6
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# A/B vs. Multi-gewapende bandit experimenten {#mab-vs-ab}

<!--
>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Experiment type"
>abstract="Experiment type determines how traffic is allocated between treatments during your test. Choose the method that best aligns with your goals:</br>
>
>* **A/B Experiment**: Splits traffic as you define between treatments and measures performance until results are statistically significant. Best for learning which treatment performs better in a controlled comparison.
>
>* **Multi-armed Bandit**: Shifts traffic toward higher-performing treatments as data is collected, balancing speed and optimization. Useful when you want to maximize conversions during the experiment.
>
>* **Bring your own Multi-armed Bandit**: Use your own algorithm to decide traffic allocation, giving you flexibility if you have a custom model or strategy."
-->

Deze pagina verstrekt een gedetailleerde vergelijking van **A/B** en **Multi-Armed Bandit** experimenten, die hun respectieve sterke punten, beperkingen, en de scenario&#39;s verklaren waarin elke benadering het meest effectief is.

## A/B {#ab-test}

Bij traditioneel A/B-experiment wordt het verkeer gelijkmatig over de behandelingen verdeeld en blijft deze toewijzing gehandhaafd totdat het experiment is afgerond. Zodra de statistische significantie is bereikt, wordt de winnende behandeling geïdentificeerd en vervolgens geschaald.

### Voordelen

De belangrijkste sterke punten van het traditionele A/B-experiment zijn:

* **Statistische Groter**

  Het vaste ontwerp biedt duidelijk gedefinieerde foutpercentages en betrouwbaarheidsintervallen.

  Hypothesetests, bijvoorbeeld een betrouwbaarheid van 95%, zijn gemakkelijker toe te passen en te interpreteren.

  Goed aangedreven experimenten verminderen de kans op valse positieven.

* **Eenvoud**

  De methode is eenvoudig te ontwerpen en uit te voeren.

  De resultaten kunnen duidelijk aan niet-technische belanghebbenden worden meegedeeld.

* **Uitgebreide Inzameling van Gegevens**

  Elke behandeling krijgt een adequate blootstelling, waardoor niet alleen de winnende variant, maar ook de ondermaatse alternatieven kunnen worden geanalyseerd.

  Deze aanvullende informatie kan de strategische beslissingen op lange termijn beïnvloeden.

* **controle van de Bias**

  Vaste toewijzing vermindert de gevoeligheid voor vooroordelen zoals de &quot;curse van de winnaar&quot; of regressie tot het gemiddelde.

### Beperkingen

De belangrijkste beperkingen van het traditionele A/B-experiment zijn:

* **Kosten van de Kans**

  Een aanzienlijk deel van het verkeer is gericht op minder goede behandelingen, waardoor omzettingen of inkomsten tijdens de test mogelijk worden verminderd.

  De winnende behandeling kan pas worden uitgevoerd nadat het experiment is beëindigd.

* **Vaste Vereiste van de Duur**

  De tests moeten over het algemeen gedurende de vooraf bepaalde periode worden uitgevoerd, zelfs als externe omstandigheden, zoals seizoensgebondenheid, marktverschuivingen, halverwege de looptijd veranderen.

  De aanpassing tijdens het experiment is beperkt.

## Meervoudig bewapende bandit {#mab-experiment}

Meergewapende bankwampjes maken gebruik van adaptieve toewijzing: naarmate het bewijsmateriaal zich ophopen, wordt meer verkeer gericht op beter presterende behandelingen. Het doel is de cumulatieve beloning tijdens het experiment te maximaliseren in plaats van zich uitsluitend te richten op het eindresultaat.

### Voordelen

De belangrijkste sterke punten van de multi-gewapende banimethoden zijn:

* **Snellere Optimalisering**

  Belofende behandelingen krijgen eerder prioriteit, waardoor de algehele prestaties tijdens de test verbeteren.

* **Aanpassing**

  Toewijzingen worden voortdurend bijgewerkt terwijl er gegevens worden verzameld, zodat Multi-gewapende bandit geschikt is voor dynamische omgevingen.

* **Verminderde Kosten van de Kansen**

  Slechte behandelingen worden snel afgeschaft, waardoor het verspilde verkeer wordt geminimaliseerd.

* **Geschiktheid voor het Ononderbroken Testen**

  Geschikt voor lopende experimenten of contexten waar verkeer kostbaar is.

### Beperkingen

De belangrijkste beperkingen van de multi-gewapende banimethoden zijn:

* **De zwakkere Statistische Garanties**

  Traditionele hypothesetests zijn moeilijker toe te passen en stopregels zijn minder duidelijk.

* **Verminderde Transparantie**

  Aangepaste toewijzing kan moeilijk aan de belanghebbenden worden uitgelegd.

* **Beperkte Informatie over Ondermaatse Behandelingen**

  Zwakke behandelingen krijgen weinig blootstelling, waardoor diagnostische insight wordt beperkt.

* **Complexiteit van de Implementatie**

  Vereist geavanceerde algoritmen en infrastructuur, met groter potentieel voor verkeerde configuratie.

## Wanneer moet u een B-bericht of een meervoudig bewapende bandit gebruiken?

| Scenario | Aanbevolen methode |
|-|-|
| U voert verkennende of door onderzoek gedreven tests uit | A/B |
| U voert altijd-op campagnes, bijvoorbeeld advertenties, aanbevelingen | Meervoudig bewapende banaan |
| U wilt conversies maximaliseren tijdens de test | Meervoudig bewapende banaan |
| U wilt duidelijke, betrouwbare inzichten | A/B |
| Je moet snel aanpassen, bijvoorbeeld seizoensverschuivingen | Meervoudig bewapende banaan |
| U hebt beperkt verkeer en wilt rendement van investeringen snel optimaliseren | Meervoudig bewapende banaan |
| Je hebt veel verkeer en je kunt het trager leren betalen | A/B |
| Belanghebbenden hebben duidelijke beslissingspunten nodig | A/B |

