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
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '1067'
ht-degree: 0%

---

# Statistische berekeningen begrijpen {#experiment-calculations}

In dit artikel worden de statistische berekeningen beschreven die worden gebruikt bij het uitvoeren van experimenten in Adobe Journey Optimizer.

Gebruik van experimenten [geavanceerde statistische methoden](../content-management/assets/confidence_sequence_technical_details.pdf) om te berekenen **Vertrouwensreeksen** en **Vertrouwen**, zodat u uw experimenten zo lang als nodig kunt uitvoeren en de resultaten voortdurend kunt controleren.

In dit artikel wordt beschreven hoe de experimenten werken en wordt een intuïtieve inleiding gegeven op de **Elke geldige betrouwbaarheidsreeks**.

Voor gebruikers van deskundigen worden de technische details en de verwijzingen in [deze pagina](../content-management/assets/confidence_sequence_technical_details.pdf).

## Statistische test- en controlefouten {#statistical-testing}

Wanneer u een experiment uitvoert, probeert u te bepalen of er een verschil is tussen twee populaties en de waarschijnlijkheid dat dat verschil toe te schrijven is aan toeval.

Over het algemeen zijn er twee hypothesen:

* de **Null Hypothese** dat er geen effect op de behandeling is.
* de **Alternatieve hypothese** wat betekent dat er een effect is op de behandeling.

In statistisch opzicht is het de bedoeling te proberen de kracht van het bewijs te beoordelen om de nulhypothese af te wijzen. Een belangrijk punt om op te merken is dat statistische significantie wordt gebruikt om te beoordelen hoe waarschijnlijk de behandelingen zullen zijn, niet hoe waarschijnlijk ze zullen zijn. Daarom wordt statistische significantie gebruikt in combinatie met **Optillen**.

Effectieve experimenten vereisen dat rekening wordt gehouden met verschillende soorten fouten die onjuiste conclusies kunnen veroorzaken.

![](assets/technote_1.png)

In de bovenstaande tabel worden de verschillende fouttypen geïllustreerd:

* **False Positives (Type-I-fouten)**: is een onjuiste afwijzing van de nulhypothese, terwijl dat juist is. In de context van online experimenten betekent dit dat we ten onrechte concluderen dat de uitkomst per behandeling verschilt, hoewel het dezelfde was.
  </br>Voordat we het experiment uitvoeren, kiezen we doorgaans een drempelwaarde `\alpha`. Nadat het experiment is uitgevoerd, `p-value` is berekend en wij verwerpen `null if p < \alpha`Een `/alpha` is gebaseerd op de gevolgen van het krijgen van het verkeerde antwoord, bijvoorbeeld in een klinische proef waarbij het leven van iemand kan worden beïnvloed u zou kunnen besluiten om een `\alpha = 0.005`. Een veel gebruikte drempelwaarde in online experimenten is `\alpha = 0.05`Dat betekent dat we op de lange termijn verwachten dat 5 van de 100 experimenten valse positieven zijn.

* **False Negatives (Type-II fouten)**: betekent dat wij de nulhypothese niet verwerpen, hoewel deze onjuist is. Voor experimenten betekent dit dat we de nulhypothese niet verwerpen, terwijl die in feite anders is. Om dit soort fouten te kunnen beheren, moeten we in ons experiment over het algemeen voldoende gebruikers hebben om een bepaalde macht te garanderen, gedefinieerd als `1 - \beta`(d.w.z. één min de waarschijnlijkheid van een fout van type II).

Voor de meeste statistische bepalingstechnieken moet u de grootte van de steekproef vooraf bepalen op basis van de effectgrootte die u wilt bepalen en de fouttolerantie (`\alpha` en `\beta`). De Adobe Journey Optimizer-methodologie is echter ontworpen om u in staat te stellen uw resultaten voortdurend te bekijken, voor elke voorbeeldgrootte.

## Statistische methodologie van de Adobe: Alle tijdgeldige betrouwbaarheidsreeksen

A **Vertrouwensvolgorde** is een sequentieel analoog van een **Vertrouwelijk interval**, bijvoorbeeld als u uw experimenten honderd keer herhaalt en een schatting berekent van de gemiddelde metrische waarde en de bijbehorende 95%-betrouwbaarheidsvolgorde voor elke nieuwe gebruiker die het experiment uitvoert. Een 95% Vertrouwensreeks zal de ware waarde van metrisch in 95 van de 100 experimenten omvatten die u in werking stelde. Een betrouwbaarheidsinterval van 95% kon slechts eenmaal per experiment worden berekend om dezelfde 95% dekkingsgarantie te bieden, niet bij elke nieuwe gebruiker. De Reeksen van het vertrouwen staan daarom u toe om experimenten onophoudelijk te controleren, zonder het verhogen van vals Positieve foutenpercentages.

Het verschil tussen betrouwbaarheidsreeksen en betrouwbaarheidsintervallen voor één experiment wordt in de onderstaande animatie getoond:

![](assets/technote_2.gif)

**Vertrouwensreeksen** de focus van experimenten verschuiven naar schattingen in plaats van hypothesetests, d.w.z. waarbij de nadruk ligt op een nauwkeurige schatting van het verschil in middelen tussen behandelingen, in plaats van of een nulhypothese op basis van een statistisch significante drempel wordt afgewezen.

Op vergelijkbare wijze als de relatie tussen `p-values`, of **Vertrouwen**, en **Vertrouwelijke intervallen** er ook een verband bestaat tussen **Vertrouwensreeksen** en elke geldige tijd `p-values`of een geldig vertrouwen. Gezien de bekendheid van hoeveelheden zoals het Vertrouwen, biedt Adobe zowel de **Vertrouwensreeksen** en een geldig vertrouwen in haar verslagen.

De theoretische grondslagen van **Vertrouwensreeksen** afkomstig zijn uit het onderzoek naar reeksen van willekeurige variabelen, martingales genoemd. Hieronder vindt u een aantal belangrijke resultaten voor ervaren lezers, maar de vakmensen zijn duidelijk:

>[!NOTE]
>
>De opeenvolgingen van het vertrouwen kunnen als veilige opeenvolgende analogen van betrouwbaarheidsintervallen worden geïnterpreteerd. Met betrouwbaarheidsintervallen kunt u het experiment alleen interpreteren als u de vooraf bepaalde steekproefgrootte hebt bereikt. Met vertrouwensreeksen kunt u echter op elk gewenst moment gegevens in uw experimenten bekijken en interpreteren, en experimenten veilig stoppen of voortzetten. het overeenkomstige, op elk moment geldige vertrouwen, of `p-value`, is ook veilig om op elk ogenblik te interpreteren.

Aangezien vertrouwensreeksen &quot;op elk moment geldig&quot; zijn, zijn ze conservatiever dan een methode met een vaste tijdshorizon die bij dezelfde steekproefgrootte wordt gebruikt. De grenzen van de vertrouwensreeks zijn over het algemeen breder dan een berekening van het betrouwbaarheidsinterval, terwijl het tijdsverloop van een geldig vertrouwen kleiner zal zijn dan een berekening van het vaste horizonvertrouwen. Het voordeel van dit conservatisme is dat je je resultaten altijd veilig kunt interpreteren.

## Een experiment declareren als &quot;Sluiten&quot;

![](assets/experimentation_report_2.png)

Telkens als je het experimentatierapport bekijkt, analyseert de Adobe de gegevens die in het experiment tot op heden zijn verzameld en zal een experiment als &quot;Sluiten&quot; worden aangemerkt wanneer het op elk moment geldige vertrouwen een drempel van 95% overschrijdt voor ten minste een van de behandelingen.

Op dit punt, zal de behandeling die het best (gebaseerd op de omzettingspercentage, of profiel-genormaliseerde metrische waarde) uitvoert worden benadrukt bij de bovenkant van het rapportscherm, en met een ster in het tabelrapport vermeld. Alleen behandelingen met een betrouwbaarheid van meer dan 95%, samen met de uitgangswaarde, worden in deze bepaling in aanmerking genomen.

Wanneer er meer dan twee behandelingen zijn, wordt de Bonferroni correctieverbinding gebruikt om voor veelvoudige vergelijkingsproblemen te verbeteren, en het familie wijze foutenpercentage te controleren. In dit scenario is het ook mogelijk dat er meerdere behandelingen zijn met een betrouwbaarheid van meer dan 95% en waarvan de betrouwbaarheidsintervallen elkaar overlappen. In dit geval zal Adobe Journey Optimizer de klasse met de hoogste omzettingssnelheid (of profiel-genormaliseerde metrische waarde) aanmerken als de best presterende instantie.
