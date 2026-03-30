---
solution: Journey Optimizer
product: Journey Optimizer
title: Modellen voor automatische optimalisatie
description: Meer informatie over modellen voor automatische optimalisatie
feature: Ranking, Decisioning
role: User
level: Experienced
exl-id: 8a8b66cb-dd96-4373-bbe0-a67e0dc0b2c0
version: Journey Orchestration
source-git-commit: ca31e819b0d120f54adfe2035ecacb21ac4f1f15
workflow-type: tm+mt
source-wordcount: '1675'
ht-degree: 0%

---

# Modellen voor automatische optimalisatie {#auto-optimization-model}

Het model van de auto-optimalisering van [!DNL Adobe Journey Optimizer] is een versterkend het leren model dat het aanbieden doorklikkingstarief (CTR) maximaliseert door alle aanbiedingen (of inhoud) te onderzoeken, dan rangschikkend punten die op voorspelde CTR worden gebaseerd, nadat de toelatingsregels en de frequentiedappen worden toegepast.

## Gebruik gevallen en voordelen {#use-cases-benefits}

Automatisch optimaliseren kan worden gebruikt op elk moment dat u snel en eenvoudig wilt instellen, algemene winnende aanbiedingen wilt zoeken en de aanbiedingsklikken wilt maximaliseren binnen één kanaal. Bijvoorbeeld:

* Kies de beste aanbiedingen die u op een webpagina wilt invoegen om de opties voor klikken te maximaliseren.
* Kies de beste aanbiedingen om in een e-mail in te voegen om de aanbiedingen te maximaliseren klikt.
* Kies de beste aanbiedingen om in een mobiel toepassingsscherm op te nemen om de aanbiedingen te maximaliseren klikt.

Automatische optimalisatie is een goede keuze als:

* Aanbiedingen veranderen in de loop der tijd of vaak: het model voor automatische optimalisatie wordt om de zes uur opnieuw opgeleid.

## Vereisten en beperkingen {#requirements-limitations}

Automatische optimalisatie heeft de volgende vereisten en beperkingen:

* De auto-optimalisering vereist een trainingsdataset die de gebeurtenissen van de aanbiedingsvertoning, de aanbieding klikgebeurtenissen, en de het gebiedsgroep van de Interacties van de Gebeurtenis van de Beleving - van de Positie bevat.
* Auto-optimalisatiemodellen kunnen niet worden gebruikt in aanvragen voor de Batch-beslissings-API.
* Automatisch optimaliseren optimaliseert altijd voor het klikken van aanbiedingen. Om voor een doelstelling buiten aanbieding te maximaliseren klikt, gebruik het [&#x200B; Gepersonaliseerde optimalisering &#x200B;](personalized-optimization-model.md) model.
* Automatisch optimaliseren probeert algemene winnende aanbiedingen te vinden en vindt geen persoonlijke rangorde voor elke klant. Om gepersonaliseerde classificaties voor elke klant te vinden, gebruik het [&#x200B; Gepersonaliseerde optimalisering &#x200B;](personalized-optimization-model.md) model.

Om een model voor automatische optimalisatie te trainen, moet de dataset aan de volgende minimumvereisten voldoen:

* Ten minste 2 aanbiedingen in de dataset moeten minstens 100 vertoningsgebeurtenissen en 5 klikgebeurtenissen binnen de laatste 14 dagen hebben.
* Aanbiedingen met minder dan 100 beeldschermen en/of 5 klikgebeurtenissen in de afgelopen 14 dagen worden door het model behandeld als nieuwe aanbiedingen, en komen alleen in aanmerking om door het exploratiebandit te worden gediend.
* Aanbiedingen met meer dan 100 beeldschermen en 5 klikgebeurtenissen in de afgelopen 14 dagen worden door het model behandeld als bestaande aanbiedingen, en komen in aanmerking om door zowel exploratie- als exploitatiepunten te worden gediend.

Tot de eerste keer dat een model voor automatische optimalisatie wordt getraind, worden aanbiedingen binnen een selectiestrategie met behulp van een model voor automatische optimalisatie willekeurig aangeboden.

## Optimalisatie afstemmen met leren {#balancing-optimization-learning}

De auto-optimalisering is a [&#x200B; versterking het leren &#x200B;](https://en.wikipedia.org/wiki/Reinforcement_learning){target="_blank"} model dat over de klikthrough prestaties van aanbiedingen leert die op echt-wereldklantengedrag worden gebaseerd. Versterking van leermodellen is bedoeld om een doel te maximaliseren door acties met beter voorspelde resultaten te kiezen. Een model dat echter altijd elke klant de producten met de beste voorspelde resultaten voorlegde, zou nooit leren over de prestaties van nieuwe items die in de loop der tijd werden geïntroduceerd (het zogenaamde &quot;koudstartprobleem&quot;), noch zou het leren over wijzigingen in de prestaties van andere bestaande items die het gevolg zijn van veranderingen in het gedrag van klanten in de loop der tijd. Versterking het leren modellen moeten daarom beheren wat algemeen [&#x200B; verkenning-uitgebuit handel &#x200B;](https://en.wikipedia.org/wiki/Exploration%E2%80%93exploitation_dilemma){target="_blank"} wordt genoemd, d.w.z. evenwichtsoptimalisering met het leren.

De auto-optimalisering gebruikt een gemeenschappelijke benadering genoemd a [&#x200B; multi-gewapende bandit &#x200B;](https://en.wikipedia.org/wiki/Multi-armed_bandit){target="_blank"} om de afweging te beheren. De veelbewapende bandiet neemt rangschikkingsbeslissingen op basis van:

* de voorspelde doorkliksnelheid van elk item
* de verschillen in de voorspelde doorkliksnelheid van elk punt
* de mate waarin het model onzeker is over zijn voorspellingen voor elk item.

Meervoudig bewapende banden gebruiken deze informatie, samen met willekeurige variabiliteit, om de te nemen acties te kiezen. Auto-optimalisering is een [&#x200B; ensemble algoritme &#x200B;](https://en.wikipedia.org/wiki/Ensemble_learning){target="_blank"} dat veelvoudige multi-gewapende banden bevat om ervoor te zorgen alle aanbiedingen behoorlijk worden onderzocht terwijl het maximaliseren van algemene prestaties.

Bij het beantwoorden van een rangordeverzoek maakt een &quot;toezichthoudende&quot; veelbewapende banaan eerst de keuze of dit verzoek moet worden verward met exploratie of moet worden verward met uitbuiting. Dit besluit wordt genomen met behulp van een &quot;epsilon-greedy&quot;-aanpak.

De tweede laag van het rangschikken wordt uitgevoerd door één van twee [&#x200B; Thompson steekproefsgewijze &#x200B;](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"} banden:

* 10% van het verkeer wordt toegewezen aan een op exploratie gerichte bandit die waarschijnlijker nieuwe aanbiedingen of die met beperkte gegevens zal adviseren, op de veronderstelling dat het model van meer leren over klantengedrag in antwoord op deze aanbiedingen zou profiteren.
* 90% van het verkeer wordt toegewezen aan een exploitatiegerichte banening die meer waarschijnlijk in de loop der tijd krachtige aanbiedingen zal adviseren, in de veronderstelling dat nieuwe of lage gegevensaanbiedingen eerder onderpresteren tot anders bewezen.

In technische zin, zijn deze veronderstellingen parameters van de vroegere kansverdeling, die ook als [&#x200B; worden bedoeld preors &#x200B;](https://en.wikipedia.org/wiki/Prior_probability){target="_blank"}. Aangezien de aanbiedingen meer vertoning en klikgegevens verzamelen, wordt de invloed van de gekozen priors lager, en de voorspellingen die door de twee banden worden gemaakt neigen in tijd samen te komen.

Onze benadering van het combineren van veelvoudige banden en het toewijzen van wat specifiek verkeer voor exploratie verstrekt verscheidene voordelen:

* het model leert het snelst over de nieuwste aanbiedingen met de minste gegevens
* het model blijft over alle aanbiedingen leren en reageert op veranderingen in klantengedrag in tijd
* het model is niet overdreven door agressieve aanbiedingen met een hogere zichtbare CTR, maar weinig waarnemingen, of agressief ongunstige aanbiedingen met een lagere zichtbare CTR, maar weinig waarnemingen
* het model is robuust voor de afhandeling van beslissingen inzake verkeerstoewijzing over honderden aanbiedingen met een kleine klik en met zeer verschillende hoeveelheden historische gegevens

## Thompson sampling {#thompson-sampling}

[&#x200B; Thompson bemonstering &#x200B;](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}, of Badesische banden, is een Bayesiaanse benadering van het multi-gewapende bandit probleem. Het model behandelt de gemiddelde beloning 𝛍 van elk aanbod als een willekeurige variabele en gebruikt de gegevens die we tot nu toe hebben verzameld om ons &#39;geloof&#39; over de gemiddelde beloning bij te werken. Deze &quot;overtuiging&quot; wordt wiskundig weergegeven door een posterior kansverdeling - in wezen een reeks waarden voor de gemiddelde beloning, samen met de plausibiliteit (of waarschijnlijkheid) die de beloning voor elke aanbieding heeft. Vervolgens zullen we voor elk besluit een punt uit elk van deze posterior beloningdistributies kopiëren en het aanbod selecteren waarvan de in de steekproef opgenomen beloning de hoogste waarde had.

Dit proces wordt geïllustreerd in onderstaande afbeelding, waar we drie verschillende aanbiedingen hebben. Aanvankelijk hebben we geen bewijs uit de gegevens en we gaan ervan uit dat alle aanbiedingen een uniforme posterior beloningsverdeling hebben. We nemen een monster van de posterior beloningsdistributie van elk aanbod. Het voorbeeld dat u hebt geselecteerd bij de distributie van Aanbieding 2, heeft de hoogste waarde. Dit is een voorbeeld van verkenning. Na het tonen van Aanbieding 2, verzamelen wij om het even welke potentiële beloning (bijvoorbeeld omzetting/geen-omzetting) en werken de posterior distributie van Aanbieding 2 bij gebruikend Bayes Theorem zoals hieronder verklaard. We zetten dit proces voort en werken de posterior distributies bij telkens wanneer een aanbieding wordt getoond en de beloning wordt geïnd. In het tweede cijfer, wordt Aanbieding 3 geselecteerd - hoewel Aanbieding 1 de hoogste gemiddelde beloning heeft (zijn posterior beloningsdistributie is het verst naar rechts), heeft het proces van bemonstering van elke distributie ertoe geleid dat wij een schijnbaar suboptimale Aanbieding 3 kozen. Daarmee geven we onszelf de kans om meer te leren over de ware beloningsverdeling van Aanbieding 3.

Aangezien meer monsters worden verzameld, neemt het vertrouwen toe en wordt een nauwkeuriger schatting van de mogelijke beloning verkregen (die overeenkomt met een kleinere beloningsverdeling). Dit proces om onze overtuigingen bij te werken aangezien het meer bewijsmateriaal beschikbaar wordt is gekend als **Bayesiaanse Inferentie**.

Uiteindelijk, als één aanbieding (b.v. Aanbieding 1) een duidelijke winnaar is, zal zijn posterior beloningsdistributie van anderen worden gescheiden. Op dit moment zal de in de steekproef opgenomen beloning van aanbod 1 voor elk besluit waarschijnlijk de hoogste zijn, en we zullen er met een hogere waarschijnlijkheid voor kiezen. Dit is uitbuiting - we zijn er sterk van overtuigd dat aanbod 1 het beste is, en dus wordt gekozen om beloningen te maximaliseren.

![](../assets/ai-ranking-thompson-sampling.png)

**Figuur 1**: *voor elk besluit, steekproef wij een punt van de posterior beloningsverdelingen. Het aanbod met de hoogste steekproefwaarde (omrekeningskoers) wordt gekozen. In de eerste fase hebben alle aanbiedingen een uniforme verdeling, aangezien we geen enkel bewijs hebben van de omrekeningskoersen van de aanbiedingen op basis van de gegevens. Terwijl we meer monsters verzamelen, worden de posterior distributies smaller en nauwkeuriger. Uiteindelijk, zal de aanbieding met de hoogste omzettingspercentages elke keer worden gekozen.*

+++ Berekeningsgegevens

Om distributies te berekenen/bij te werken, gebruiken wij **de Theorem van Bayes&#39;**. Voor elke aanbieding ***i***, willen wij hun ***P (𝛍 i | gegevens)**, d.w.z. voor elke aanbieding ***i*** berekenen, hoe waarschijnlijk een beloningswaarde **𝛍i** is, gezien de gegevens die wij tot dusverre voor die aanbieding hebben verzameld.

Van Bayes Theorem:

***Posterior = Waarschijnlijkheid * Voorafgaand***

De **vroegere waarschijnlijkheid** is de aanvankelijke gok over de waarschijnlijkheid om een output te veroorzaken. De waarschijnlijkheid, nadat één of ander bewijsmateriaal is verzameld, is gekend als **achterste waarschijnlijkheid**.

De auto-optimalisering wordt ontworpen om binaire beloningen (klik/geen-klik) te overwegen. In dit geval vertegenwoordigt de waarschijnlijkheid het aantal successen van N-proeven en wordt zij gemodelleerd door een binomiale distributie. Voor sommige waarschijnlijkheidsfuncties, als u een bepaalde vroegere kiest, uiteindelijk is de achter-achter in de zelfde distributie zoals vroeger. Zulk vroeger dan wordt genoemd a **conjugaat voorafgaand**. Dit soort van vroeger maakt de berekening van posterior distributie zeer eenvoudig. De [&#x200B; distributie van Beta &#x200B;](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"} is een conjugaat voorafgaand aan de binomiale waarschijnlijkheid (binaire beloningen), en is zo een geschikte en verstandige keus voor de vroegere en posterior kansverdelingen. De distributie van Beta neemt twee parameters, ***α*** en ***β***. Deze parameters kunnen worden beschouwd als het aantal successen en mislukkingen en de gemiddelde waarde die wordt gegeven door:

![](../assets/ai-ranking-beta-distribution.png)

De functie van de Waarschijnlijkheid zoals hierboven verklaard wordt gemodelleerd door een Binomiale distributie, met s successes (omzettingen) en f mislukkingen (geen omzettingen) en q is een willekeurige variabele met een distributie van Beta.

Het bovenstaande voorbeeld wordt gemodelleerd door Beta-distributie en de posterior-distributie heeft de volgende vorm:

![](../assets/ai-ranking-posterior-distribution.svg)

+++

### Onderzoeksvooringenomenheid en exploitatievooroordelen {#exploration-exploitation-bias}

Een aanvankelijke waarde moet voor de parameters ***worden gekozen α***, ***β***. De auto-optimalisering omvat zowel een exploratie-bevooroordeelde Thompson steekproefbandit en een exploitatie-georiënteerde Thompson steekproefbandit die verschillende aanvankelijke ***α***, ***β*** priors in hun bèta distributies gebruiken.

In een algemene de steekproefbenadering van Thompson, wordt achteraan berekend door het aantal successen en mislukkingen aan de bestaande parameters ***α***, ***β*** eenvoudig toe te voegen. Automatische optimalisatie gebruikt verschillende wegingsfactoren voor nieuwe successen en mislukkingen om de impact van nieuwe gegevens ten opzichte van eerdere gegevens te wijzigen in zowel de ontdekkingsgebonden als de misbruikgebonden verbanden.

## Verwijzingen {#references}

Raadpleeg de volgende onderzoeksdocumenten voor een dieper inzicht in Thompson sampling bandits:

* [&#x200B; een Empirische Evaluatie van Thompson Steekproef &#x200B;](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target="_blank"}
* [&#x200B; Analyse van Thompson Steekproef voor het Meervoudig-gewapende Probleem van de Bandit &#x200B;](https://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target="_blank"}
