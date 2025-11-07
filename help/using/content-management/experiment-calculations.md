---
solution: Journey Optimizer
product: journey optimizer
title: Door het Adobe Journey Optimizer-experiment gebruikte statistische berekeningen
description: Meer informatie over statistische berekeningen die tijdens experimenten worden gebruikt
feature: Experimentation
topic: Content Management
role: User
level: Experienced
keywords: inhoud, experiment, statistiek, berekening
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '1067'
ht-degree: 0%

---

# Statistische berekeningen begrijpen {#experiment-calculations}

In dit artikel worden de statistische berekeningen beschreven die worden gebruikt bij het uitvoeren van experimenten in Adobe Journey Optimizer.

De experimentatie gebruikt [&#x200B; geavanceerde statistische methodes &#x200B;](../content-management/assets/confidence_sequence_technical_details.pdf) om **opeenvolgingen van het Vertrouwen** en **Vertrouwen** te berekenen, die u toestaan om uw experimenten zolang als nodig in werking te stellen, en uw resultaten onophoudelijk te controleren.

Dit artikel beschrijft hoe de Experimentatie werkt, en verstrekt een intuïtieve inleiding aan Adobe **Om het even welke Geldige Reeksen van het Vertrouwen van de Tijd**.

Voor deskundige gebruikers, zijn de technische details en de verwijzingen gedetailleerd op [&#x200B; deze pagina &#x200B;](../content-management/assets/confidence_sequence_technical_details.pdf).

## Statistische test- en controlefouten {#statistical-testing}

Wanneer u een experiment uitvoert, probeert u te bepalen of er een verschil is tussen twee populaties en de waarschijnlijkheid dat dat verschil toe te schrijven is aan toeval.

Over het algemeen zijn er twee hypothesen:

* **Null Hypothese** betekenend dat er geen effect aan de behandeling is.
* de **Alternatieve Hypothese** betekenis is er een effect aan de behandeling.

In statistisch opzicht is het de bedoeling te proberen de kracht van het bewijs te beoordelen om de nulhypothese af te wijzen. Een belangrijk punt om op te merken is dat statistische significantie wordt gebruikt om te beoordelen hoe waarschijnlijk de behandelingen zullen zijn, niet hoe waarschijnlijk ze zullen zijn. Dit is waarom de statistische betekenis in combinatie met **Lift** wordt gebruikt.

Effectieve experimenten vereisen dat rekening wordt gehouden met verschillende soorten fouten die onjuiste conclusies kunnen veroorzaken.

![](assets/technote_1.png)

In de bovenstaande tabel worden de verschillende fouttypen geïllustreerd:

* **Vals Positives (Type-I fouten)**: zijn een onjuiste verwerping van de ongeldige hypothese, wanneer in feite het waar is. In de context van online experimenten betekent dit dat we ten onrechte concluderen dat de uitkomst per behandeling verschilt, hoewel het dezelfde was.
  </br> alvorens wij het experiment in werking stellen, kiezen wij typisch een drempel `\alpha`. Nadat het experiment is uitgevoerd, wordt de `p-value` berekend en wijzen we `null if p < \alpha` .Choosing an `/alpha` af op basis van de gevolgen van het krijgen van het verkeerde antwoord, bijvoorbeeld in een klinische proef waarin het leven van iemand zou kunnen worden beïnvloed, zou u kunnen besluiten om een `\alpha = 0.005` te hebben. Een veel gebruikte drempel in online experimenten is `\alpha = 0.05`, wat betekent dat we op lange termijn verwachten dat 5 van elke 100 experimenten valse positieven zijn.

* **False Negatieven (Type-II Fouten)**: betekent dat wij er niet in slagen om de ongeldige hypothese te verwerpen hoewel het vals is. Voor experimenten betekent dit dat we de nulhypothese niet verwerpen, terwijl die in feite anders is. Om dit type fout te kunnen besturen, moeten we in ons experiment over het algemeen voldoende gebruikers hebben om een bepaalde macht te garanderen, gedefinieerd als `1 - \beta` (dat wil zeggen een min de waarschijnlijkheid van een type II-fout).

Voor de meeste statistische bepalingstechnieken moet u de grootte van de steekproef vooraf bepalen op basis van de effectgrootte die u wilt bepalen en de fouttolerantie (`\alpha` en `\beta` ). De Adobe Journey Optimizer-methodologie is echter ontworpen om u in staat te stellen uw resultaten voortdurend te bekijken, voor elke voorbeeldgrootte.

## Statistische methodologie voor Adobe: alle tijdgeldige betrouwbaarheidsreeksen

A **Opeenvolging van het Vertrouwen** is een opeenvolgend analogon van het Interval van het Vertrouwen van a **&#x200B;**, bijvoorbeeld als u uw experimenten honderd keer herhaalt, en een schatting van metrisch gemiddelde en zijn bijbehorende 95%-Vertrouwensvolgorde voor elke nieuwe gebruiker berekent die het experiment ingaat. Een 95% Vertrouwensreeks zal de ware waarde van metrisch in 95 van de 100 experimenten omvatten die u in werking stelde. Een betrouwbaarheidsinterval van 95% kon slechts eenmaal per experiment worden berekend om dezelfde 95% dekkingsgarantie te bieden, niet bij elke nieuwe gebruiker. De Reeksen van het vertrouwen staan daarom u toe om experimenten onophoudelijk te controleren, zonder het verhogen van vals Positieve foutenpercentages.

Het verschil tussen betrouwbaarheidsreeksen en betrouwbaarheidsintervallen voor één experiment wordt in de onderstaande animatie getoond:

![](assets/technote_2.gif)

**de opeenvolgingen van het Vertrouwen** verschuiven de nadruk van Experimentaties aan raming eerder dan hypothesetesten, d.w.z., die op nauwkeurige raming van het verschil in middelen tussen behandelingen concentreren, eerder dan of om een nulhypothese af te wijzen die op een drempel van statistische betekenis wordt gebaseerd.

Nochtans, op een gelijkaardige manier aan het verband tussen `p-values`, of **Vertrouwen**, en **Intervallen van het Vertrouwen**, is er ook een verband tussen **Opeenvolgingen van het Vertrouwen** en om het even welke tijd geldig `p-values`, of om het even welk tijd geldig Vertrouwen. Gezien de vertrouwdheid van hoeveelheden zoals het Vertrouwen, verstrekt Adobe zowel de **Reeksen van het Vertrouwen** als om het even welk tijd geldig Vertrouwen in zijn rapporten.

De theoretische stichtingen van **Reeksen van het Vertrouwen** komen uit de studie van opeenvolgingen van willekeurige die variabelen als martingales worden bekend. Hieronder vindt u een aantal belangrijke resultaten voor ervaren lezers, maar de vakmensen zijn duidelijk:

>[!NOTE]
>
>De opeenvolgingen van het vertrouwen kunnen als veilige opeenvolgende analogen van betrouwbaarheidsintervallen worden geïnterpreteerd. Met betrouwbaarheidsintervallen kunt u het experiment alleen interpreteren als u de vooraf bepaalde steekproefgrootte hebt bereikt. Met vertrouwensreeksen kunt u echter op elk gewenst moment gegevens in uw experimenten bekijken en interpreteren, en experimenten veilig stoppen of voortzetten. Het overeenkomstige Elke geldige Vertrouwen van de Tijd, of `p-value`, is ook veilig om op om het even welk ogenblik te interpreteren.

Aangezien vertrouwensreeksen &quot;op elk moment geldig&quot; zijn, zijn ze conservatiever dan een methode met een vaste tijdshorizon die bij dezelfde steekproefgrootte wordt gebruikt. De grenzen van de vertrouwensreeks zijn over het algemeen breder dan een berekening van het betrouwbaarheidsinterval, terwijl het tijdsverloop van een geldig vertrouwen kleiner zal zijn dan een berekening van het vaste horizonvertrouwen. Het voordeel van dit conservatisme is dat je je resultaten altijd veilig kunt interpreteren.

## Een experiment declareren als &quot;Sluiten&quot;

![](assets/experimentation_report_2.png)

Telkens als je het experimentatierapport bekijkt, analyseert Adobe de gegevens die in het experiment tot op heden zijn verzameld en zal een experiment als &quot;Sluiten&quot; worden aangemerkt wanneer het altijd geldige vertrouwen een drempel van 95% overschrijdt voor ten minste een van de behandelingen.

Op dit punt, zal de behandeling die het best (gebaseerd op de omzettingspercentage, of profiel-genormaliseerde metrische waarde) uitvoert worden benadrukt bij de bovenkant van het rapportscherm, en met een ster in het tabelrapport vermeld. Alleen behandelingen met een betrouwbaarheid van meer dan 95%, samen met de uitgangswaarde, worden in deze bepaling in aanmerking genomen.

Wanneer er meer dan twee behandelingen zijn, wordt de Bonferroni correctieverbinding gebruikt om voor veelvoudige vergelijkingsproblemen te verbeteren, en het familie wijze foutenpercentage te controleren. In dit scenario is het ook mogelijk dat er meerdere behandelingen zijn met een betrouwbaarheid van meer dan 95% en waarvan de betrouwbaarheidsintervallen elkaar overlappen. In dit geval zal Adobe Journey Optimizer de klasse met de hoogste omzettingssnelheid (of profiel-genormaliseerde metrische waarde) aanmerken als de best presterende instantie.
