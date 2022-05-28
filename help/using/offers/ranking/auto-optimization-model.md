---
product: experience platform
solution: Experience Platform
title: Modellen voor automatische optimalisatie
description: Meer informatie over modellen voor automatische optimalisatie
feature: Ranking Formulas
role: User
level: Intermediate
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '1404'
ht-degree: 0%

---

# Modellen voor automatische optimalisatie {#auto-optimization-model}

Een model voor automatische optimalisatie is bedoeld voor aanbiedingen die het rendement (KPI&#39;s) maximaliseren dat door zakelijke klanten is ingesteld. Deze KPI’s kunnen de vorm aannemen van omrekeningskoersen, inkomsten, enz. Op dit punt, richt de auto-optimalisering zich op optimaliserend aanbiedingskliks met aanbiedingsomzetting als ons doel. Automatisch optimaliseren is niet-gepersonaliseerd en optimaliseert op basis van &#39;algemene&#39; prestaties van de aanbiedingen.

## Beperkingen {#limitations}

Voor het gebruik van modellen voor automatische optimalisatie voor Offer decisioning gelden de onderstaande beperkingen:

* Modellen voor automatische optimalisatie werken niet met de API voor het bepalen van batch.
* Feedback die nodig is om het model te maken, moet worden verzonden als een ervaringsgebeurtenis. Het mag niet automatisch worden verzonden in [!DNL Journey Optimizer] kanalen.

## Terminologie {#terminology}

De volgende termen zijn handig wanneer u het over automatisch optimaliseren hebt:

* **Meervoudig bewapende bandit**: A [meerbewapende bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=&quot;_blank&quot;} -benadering om een optimale balans te vinden tussen exploratief leren en gebruik van dat leren.

* **Thomson sampling**: Thompson sampling is een algoritme voor online beslissingsproblemen waarbij acties opeenvolgend worden genomen op een manier die evenwicht moet vinden tussen het exploiteren van wat bekend is om het maximaliseren van de directe prestaties en het investeren om nieuwe informatie te verzamelen die toekomstige prestaties kan verbeteren. [Meer informatie](#thompson-sampling)

* [**Beta-distributie**](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}: Ononderbroken set [kansverdeling](https://en.wikipedia.org/wiki/Probability_distribution){target=&quot;_blank&quot;} gedefinieerd op het interval [0,1] [geparametriseerd](https://en.wikipedia.org/wiki/Statistical_parameter){target=&quot;_blank&quot;} door twee positieve waarden [vormparameters](https://en.wikipedia.org/wiki/Shape_parameter){target=&quot;_blank&quot;}.

## Thompson Sampling {#thompson-sampling}

Het algoritme dat aan Auto-optimalisering ten grondslag ligt is **Thompson sampling**. In deze sectie bespreken we de intuïtie achter Thompson-steekproeven.

[Thompson sampling](https://en.wikipedia.org/wiki/Thompson_sampling){target=&quot;_blank&quot;}, of Bayesiaanse banits, is een Bayesiaanse benadering van het multi-gewapende bandit probleem.  Het basisidee is om de gemiddelde beloning te behandelen? van elke aanbieding als **willekeurige variabele** en gebruik de gegevens die we tot nu toe hebben verzameld om ons &quot; geloof &quot; over de gemiddelde beloning bij te werken . Dit &quot;geloof&quot; wordt wiskundig weergegeven door een **waarschijnlijkheidsverdeling achter de hand** - in wezen een reeks waarden voor de gemiddelde beloning, samen met de plausibiliteit (of waarschijnlijkheid) die de beloning voor elke aanbieding heeft. Dan, voor elk besluit zullen we **monster een punt van elk van deze beloningsverdelingen achteraf** en selecteer het bod waarvan de in de steekproef opgenomen beloning de hoogste waarde had.

Dit proces wordt geïllustreerd in onderstaande afbeelding, waar we drie verschillende aanbiedingen hebben. Aanvankelijk hebben we geen bewijs van de gegevens en we gaan ervan uit dat alle aanbiedingen een uniforme posterior-beloningspreiding hebben. We nemen een monster van de posterior beloningsdistributie van elk aanbod. Het voorbeeld dat u hebt geselecteerd bij de distributie van Aanbieding 2, heeft de hoogste waarde. Dit is een voorbeeld van **exploratie**. Na het tonen van Aanbieding 2, verzamelen wij om het even welke potentiële beloning (bijvoorbeeld omzetting/geen-omzetting) en werken de posterior distributie van Aanbieding 2 bij gebruikend Bayes Theorem zoals hieronder verklaard.  We zetten dit proces voort en werken de posterior distributies bij telkens wanneer een aanbieding wordt getoond en de beloning wordt geïnd. In het tweede cijfer, wordt Aanbieding 3 geselecteerd - hoewel Aanbieding 1 de hoogste gemiddelde beloning heeft (zijn posterior beloningsdistributie is het verst naar rechts), heeft het proces van bemonstering van elke distributie ertoe geleid dat wij een schijnbaar suboptimale Aanbieding 3 kozen. Zo geven we onszelf de kans om meer te leren over de werkelijke beloningsverdeling van aanbieding 3.

Aangezien meer monsters worden verzameld, neemt het vertrouwen toe en wordt een nauwkeuriger schatting van de mogelijke beloning verkregen (die overeenkomt met een kleinere beloningsverdeling). Dit proces om onze overtuigingen bij te werken naarmate er meer bewijs beschikbaar komt, wordt bekend als **Bayesiaanse conferentie**.

Uiteindelijk, als één aanbieding (b.v. Aanbieding 1) een duidelijke winnaar is, zal zijn posterior beloningsdistributie van anderen worden gescheiden. Op dit moment zal de in de steekproef opgenomen beloning van aanbod 1 voor elk besluit waarschijnlijk de hoogste zijn, en we zullen er met een hogere waarschijnlijkheid voor kiezen. Dit is **exploitatie** - we zijn er sterk van overtuigd dat aanbod 1 het beste is, en daarom wordt gekozen om beloningen te maximaliseren.

![](../assets/ai-ranking-thompson-sampling.png)

**Figuur 1**: *Voor elk besluit, nemen wij een punt van de posterior beloningsverdelingen. Het aanbod met de hoogste steekproefwaarde (omrekeningskoers) wordt gekozen. In de eerste fase hebben alle aanbiedingen een uniforme verdeling, omdat we geen enkel bewijs hebben over de omrekeningskoersen van de aanbiedingen uit de gegevens. Terwijl we meer monsters verzamelen, worden de posterior distributies smaller en nauwkeuriger. Uiteindelijk wordt het aanbod met de hoogste omrekeningskoers telkens gekozen.*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**Technische details**

Voor het berekenen/bijwerken van distributies gebruiken we **Bayes Theorem**. Voor elke aanbieding ***i***, willen we hun ***P(??i | gegevens)***, d.w.z. voor elke aanbieding ***i***, hoe waarschijnlijk een beloningswaarde is **??i** is, gezien de gegevens die we tot nu toe voor dat aanbod hebben verzameld.

Van Bayes Theorem:

***Posterior = Likeliability * Voorafgaand***

De **voorafgaande waarschijnlijkheid** Dit is de eerste schatting van de waarschijnlijkheid om een uitvoer te produceren. De waarschijnlijkheid, nadat enig bewijs is verzameld, wordt bekend als **achterste waarschijnlijkheid**. 

De auto-optimalisering wordt ontworpen om binaire beloningen (klik/geen-klik) te overwegen. In dit geval vertegenwoordigt de waarschijnlijkheid het aantal successen van N-proeven en wordt zij gemodelleerd door een **Binomiale distributie**. Voor sommige waarschijnlijkheidsfuncties, als u een bepaalde vroegere kiest, uiteindelijk is de achter-achter in de zelfde distributie zoals vroeger. Zo&#39;n vroeger dan wordt een **voorafgaand samenvoegen**. Dit soort van vroeger maakt de berekening van posterior distributie zeer eenvoudig. De **Beta-distributie** is een conjugaat voorafgaand aan de binomiale waarschijnlijkheid (binaire beloningen), en is zo een geschikte en verstandige keuze voor de voorafgaande en posterior kansverdelingen.De bètadistributie neemt twee parameters; ***α*** en ***β***. Deze parameters kunnen worden beschouwd als het aantal successen en mislukkingen en de gemiddelde waarde die wordt gegeven door:

![](../assets/ai-ranking-beta-distribution.png)

De functie van de Waarschijnlijkheid zoals wij hierboven verklaren wordt gemodelleerd door een Binomiale distributie, met s successes (omzettingen) en f mislukkingen (geen omzettingen) en q is a [willekeurige variabele](https://en.wikipedia.org/wiki/Random_variable){target=&quot;_blank&quot;} met een [bèta-distributie](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}.

De bovenstaande methode wordt gemodelleerd door bètadistributie en de posterior-distributie heeft de volgende vorm:

![](../assets/ai-ranking-posterior-distribution.svg)

De waarde achteraf wordt berekend door het aantal successen en mislukkingen toe te voegen aan de bestaande parameters ***α***, ***β***.

Voor automatische optimalisatie, zoals in het bovenstaande voorbeeld wordt getoond, beginnen we met een eerdere distributie ***Bèta(1, 1)*** (uniforme distributie) voor alle aanbiedingen en na het krijgen van successen en van mislukkingen voor een bepaalde aanbieding, wordt de posterior een bètadistributie met parameters ***(s+α, f+β)*** voor dat aanbod.
+++

**Verwante onderwerpen**:

Lees de volgende onderzoeksdocumenten voor een dieper inzicht in Thompson sampling:
* [Een empirische evaluatie van Thompson Sampling](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target=&quot;_blank&quot;}
* [Analyse van Thompson Sampling voor het probleem van de multigewapende bandit](http://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target=&quot;_blank&quot;}

## Koudstartprobleem {#cold-start}

Het probleem van de &quot;koude start&quot; doet zich voor wanneer een nieuwe aanbieding aan een campagne wordt toegevoegd en er geen gegevens beschikbaar zijn over de omrekeningskoers van de nieuwe aanbieding. In deze periode moeten we een strategie bedenken voor de vraag hoe vaak dit nieuwe aanbod wordt gekozen, zodat de prestatievermindering tot een minimum wordt beperkt, terwijl we informatie verzamelen over de omrekeningskoers van dit nieuwe aanbod. Er zijn meerdere oplossingen beschikbaar om dit probleem aan te pakken. De sleutel is om een evenwicht te vinden tussen de verkenning van dit nieuwe aanbod, terwijl we de exploitatie niet veel opofferen. Momenteel gebruiken we &quot;uniforme distributie&quot; als eerste schatting van de omrekeningskoers van de nieuwe aanbieding (voorafgaande distributie). In feite geven we alle conversiesnelheidswaarden dezelfde kans op voorkomen.


![](../assets/ai-ranking-cold-start-strategies.png)

**Figuur 2**: *Neem een campagne met 3 aanbiedingen. Terwijl de campagne live is, wordt aanbieding 4 toegevoegd aan de campagne. Aanvankelijk hebben we geen gegevens over de omrekeningskoers van aanbod 4 en moeten we het probleem van de koudstartprocedure aanpakken. We gebruiken uniforme distributie als onze eerste schatting van de omrekeningskoers van Aanbieding 4, terwijl we gegevens verzamelen voor dit nieuwe aanbod. Zoals uiteengezet in de [Thompson sampling](#thompson-sampling) in de sectie waarin wordt aangegeven welke aanbieding aan een gebruiker wordt getoond, nemen we een monster van de achterwaartse beloningen van de aanbiedingen en selecteren we de aanbieding met de hoogste samplewaarde. In het bovenstaande voorbeeld wordt Aanbieding 4 gekozen en later op basis van de geïnde beloning, wordt de posterior-distributie van dit aanbod bijgewerkt zoals uiteengezet in het [Thompson sampling](#thompson-sampling) sectie.*

## Liftmeting {#lift}

&quot;Lift&quot;is metrisch die wordt gebruikt om de prestaties van om het even welke strategie te meten die in het rangschikken van de dienst, in vergelijking met basislijnstrategie wordt opgesteld (het dienen van aanbiedingen enkel willekeurig).

Als we bijvoorbeeld geïnteresseerd zijn in het meten van de prestaties van een Thompson Sampling-strategie (TS) die wordt gebruikt bij ranking service, en de KPI is de conversiesnelheid (CVR), wordt de &#39;lift&#39; van de TS-strategie ten opzichte van de basislijnstrategie als volgt gedefinieerd:

![](../assets/ai-ranking-lift.png)
