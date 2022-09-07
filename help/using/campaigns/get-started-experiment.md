---
title: Aan de slag met het experimenteren met inhoud
description: Meer informatie over het experimenteren met inhoud in [!DNL Journey Optimizer]
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 7fe4b24e-f60a-4107-a064-00010b0cbbfc
source-git-commit: f0e2f80a815aebb7574582fbf33770aa5da0abab
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 0%

---

# Aan de slag met content-experimenten {#get-started-experiment}

>[!AVAILABILITY]
>
>De functie Experimenteren met inhoud is momenteel alleen beschikbaar voor een set organisaties (beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

## Wat is een contentexperiment?

Met Inhoud-experimenten kunt u inhoud optimaliseren voor de acties in uw campagnes.

Experimenten bestaan uit een reeks gerandomiseerde onderzoeken, die in de context van online tests betekenen dat sommige willekeurig geselecteerde gebruikers worden blootgesteld aan een bepaalde variatie van een bericht en een andere willekeurig gekozen groep gebruikers aan een andere behandeling. Nadat u het bericht hebt verzonden, kunt u de resultaten meten die u interesseert, bijvoorbeeld wanneer u e-mails opent of klikt.

## Waarom experimenten uitvoeren?

![](assets/content_experiment_schema.png)

Met behulp van experimenten kunt u de wijzigingen isoleren die tot verbeteringen in uw metriek leiden. Zoals geïllustreerd in de bovenstaande afbeelding: sommige willekeurig geselecteerde gebruikers worden blootgesteld aan elke behandelingsgroep wat betekent dat de groepen gemiddeld dezelfde kenmerken zullen hebben . Elk verschil in resultaten kan dus worden geïnterpreteerd als zijnde te wijten aan verschillen in de ontvangen behandelingen, d.w.z. dat u een oorzakelijk verband kunt vaststellen tussen de veranderingen die u hebt aangebracht en de resultaten waarin u geïnteresseerd bent.

Dit staat u toe om gegevens gedreven besluiten in het optimaliseren van uw bedrijfsdoelstellingen te nemen.

Voor Inhoud-experimenten in Adobe Journey Optimizer kunt u ideeën testen, zoals:

* **Onderwerpregel**: Wat zou het effect van een verandering in de toon of in de graad van personalisatie van een onderwerpregel kunnen zijn?
* **Berichtinhoud**: Zal het veranderen van de visuele lay-out van een e-mail in meer klikken op e-mail resulteren?

## Tips voor het uitvoeren van experimenten

Bij het uitvoeren van experimenten is het belangrijk om bepaalde beste praktijken te volgen. Hier volgen enkele tips voor het uitvoeren van deze experimenten:

+++Isoleer de variabelen u probeert te testen

Formuleer een hypothese die u wilt testen, en beperk deze hypothese tot zo weinig mogelijk veranderingen om te bepalen wat een effect op uw levering maakte.

Een goede hypothese kan bijvoorbeeld zijn of personalisatie in e-mailonderwerpregel leidt tot betere open tarieven. Het toevoegen van een wijziging in de inhoud van het bericht of in afbeeldingen kan echter leiden tot een verwarrende conclusie.
+++

+++Zorg ervoor u juiste metrisch gebruikt

Bepaal metrisch u zou willen richten, en of de veranderingen u aanbrengt één of andere directe invloed op deze metrisch kunnen hebben.

Als u bijvoorbeeld de inhoud van de berichttekst wijzigt, is het onwaarschijnlijk dat dit invloed heeft op de e-mailopeningen.
+++

+++Voer de test uit op de juiste publieksgrootte of voor lang genoeg

Als je langer tests uitvoert, kun je kleinere verschillen in het doel meten tussen behandelingen. Nochtans, als de basislijnwaarde van uw doel metrisch is, dan zult u grotere steekproefgrootte nodig hebben.
Het aantal gebruikers dat in uw experiment moet worden omvat hangt van de effect grootte af u wenst te ontdekken, de variantie of de spreiding van uw doel metrisch, evenals uw tolerantie voor vals positieve en vals negatieve fouten. In klassieke experimenten kunt u een [voorbeeldgroottecalculator](https://experienceleague.adobe.com/tools/calculator/testcalculator.html){_blank} om te bepalen hoe lang u de test moet uitvoeren.
+++

+++Statistische onzekerheid begrijpen

Als u een experiment uitvoert waarbij 1000 gebruikers één behandeling hebben gezien, en de conversiesnelheid wordt ingesteld op 5%. Zou dit de werkelijke omrekeningskoers zijn als al uw gebruikers hierin zouden worden opgenomen? Wat zou de werkelijke omrekeningskoers zijn?
Statistische methoden bieden ons een manier om die onzekerheid te formaliseren. Een van de belangrijkste concepten die u moet begrijpen wanneer u online experimenten uitvoert, is dat de waargenomen conversietarieven consistent zijn met een reeks onderliggende werkelijke conversiekoersen. Dit houdt in dat u moet wachten tot deze schattingen precies genoeg zijn voordat u een conclusie probeert te trekken. Betrouwbaarheidsintervallen en Vertrouwen helpen ons deze onzekerheid te kwantificeren.
+++

+++Nieuwe hypothesen maken en voortdurend testen

Om echte bedrijfsinzichten te bereiken, zou u zich aan enkel één Experiment moeten houden. In plaats daarvan, follow-up experimenten door nieuwe hypothesen te formuleren, en nieuwe tests met verschillende veranderingen, op verschillende segmenten, en door het effect op de verschillende metriek te onderzoeken.
+++

## De resultaten van uw experimenten interpreteren {#interpret-results}

![](assets/experimentation_report_3.png)

In dit gedeelte worden de experimentele rapporten beschreven en wordt uitgelegd hoe de verschillende statistische hoeveelheden die worden gepresenteerd, moeten worden geïnterpreteerd.

Hier volgen enkele richtlijnen voor het interpreteren van de resultaten van uw Content Experiment.

Bij een volledige beschrijving van de resultaten moet rekening worden gehouden met alle beschikbare gegevens (bv. steekproefgrootten, omrekeningskoersen, betrouwbaarheidsintervallen enz.) en niet alleen met de vermelding van overtuigend of niet. Zelfs als een resultaat nog niet overtuigend is, kan er nog steeds overtuigend bewijs zijn dat de ene behandeling anders is dan de andere.

Voor meer begrip van statistische berekeningen, verwijs naar dit [page](../campaigns/experiment-calculations.md).

### 1. Genormaliseerde metriek vergelijken {#normalized-metrics}

Wanneer u de prestaties van twee behandelingen vergelijkt, moet u altijd de genormaliseerde meetwaarden vergelijken om rekening te houden met eventuele verschillen in het aantal profielen dat aan elke behandeling wordt blootgesteld.

Als het experimentele doel bijvoorbeeld is ingesteld op **[!UICONTROL Unique Opens]** en een bepaalde behandeling werd getoond aan 10.000 Profielen met 200 Unieke Opens geregistreerd, dan vertegenwoordigt dit een **[!UICONTROL Conversion Rate]** van 2%. Voor niet-unieke metriek, bijvoorbeeld Opens metrisch, wordt genormaliseerde metrisch getoond als a **[!UICONTROL Count per Profile]**, terwijl voor ononderbroken metriek zoals het Totaal van de Prijs, genormaliseerde metrisch wordt getoond als **[!UICONTROL Total per Profile]**.

### 2. Focus op betrouwbaarheidsintervallen {#confidence-intervals}

Wanneer u experimenteert met monsters van uw profielen, geeft de conversiekoers die voor een bepaalde behandeling wordt waargenomen een schatting van de werkelijke onderliggende conversiesnelheid.

Bijvoorbeeld als Behandeling A een **[!UICONTROL Conversion Rate]** van 3%, terwijl behandeling B een waargenomen **[!UICONTROL Conversion Rate]** van 2%, is Behandeling A beter dan Behandeling B? Om dit te kunnen beantwoorden, moeten we eerst de onzekerheid in deze waargenomen omrekeningskoersen kwantificeren.

Vertrouwensintervallen helpen de mate van onzekerheid in de geschatte omrekeningskoersen te kwantificeren, maar bredere betrouwbaarheidsintervallen impliceren meer onzekerheid. Als er meer profielen aan het experiment worden toegevoegd, worden de intervallen kleiner, wat een nauwkeurigere schatting is. Het betrouwbaarheidsinterval vertegenwoordigt een reeks conversiekoersen die compatibel zijn met de waargenomen gegevens.

Als de betrouwbaarheidsintervallen voor twee behandelingen nauwelijks overlappen, betekent dit dat de twee behandelingen verschillende conversiesnelheden hebben. Maar als er veel overlap is tussen de betrouwbaarheidsintervallen voor twee behandelingen, is het waarschijnlijker dat de twee behandelingen dezelfde conversiesnelheid hebben.

Adobe gebruikt 95% altijd geldige betrouwbaarheidsintervallen, of betrouwbaarheidsreeksen, wat betekent dat de resultaten op elk moment tijdens het experiment veilig kunnen worden bekeken.

### 3. Optillen begrijpen {#understand-lift}

De samenvatting van het Experimentenrapport bevat de **[!UICONTROL Lift over Baseline]**, hetgeen een maatstaf is voor de procentuele verbetering van de conversiesnelheid van een bepaalde behandeling ten opzichte van de uitgangswaarde. Het is precies gedefinieerd als het verschil in prestaties tussen een bepaalde behandeling en de basislijn, gedeeld door de prestaties van de basislijn, uitgedrukt als een percentage.

### 3. Vertrouwen begrijpen {#understand-confidence}

Terwijl u zich vooral op de **[!UICONTROL Confidence interval]** Voor de uitvoering van elke behandeling toont Adobe ook het Vertrouwen, wat een probabilistische maat is van hoeveel bewijs er is dat een bepaalde behandeling gelijk is aan de basisbehandeling. Een hoger vertrouwen wijst op minder bewijs voor de veronderstelling dat de basislijn en de niet-basislijn behandelingen gelijke prestaties hebben. Meer in het bijzonder is het vertrouwen dat wordt weergegeven een waarschijnlijkheid (uitgedrukt als een percentage) dat we een kleiner verschil in omrekeningskoersen tussen een bepaalde behandeling en de basislijn zouden hebben gezien, als er in werkelijkheid geen verschil is in de werkelijke onderliggende omrekeningskoersen. Wat de p-waarden betreft, wordt een vertrouwen van 1 tot p-waarde weergegeven.

Adobe gebruikt het Vertrouwen van &quot;om het even welk Geldige&quot;Vertrouwen, en &quot;Om het even welk Geldige&quot;p-waarden die met de hierboven beschreven Vertrouwensopeenvolgingen verenigbaar zijn.

### 4. Statistische significantie

Bij het uitvoeren van experimenten wordt een resultaat statistisch significant geacht als het zeer onwaarschijnlijk was dat het werd waargenomen als er een nulhypothese bestond dat een bepaalde behandeling en de basislijn identieke werkelijke onderliggende conversiekoersen/prestaties hebben.

Adobe verklaart dat een experiment overtuigend is wanneer het vertrouwen boven 95% ligt.

## Wat moet u doen na het uitvoeren van een experiment

Nadat u uw experiment hebt uitgevoerd, zijn er verschillende mogelijke vervolgacties:

* **Winnende ideeën implementeren**

   Met een eenduidig resultaat kunt u dit winnende idee implementeren door de best presterende behandeling naar al uw klanten te sturen of door nieuwe campagnes te maken waar de structuur van de best presterende behandeling wordt gerepliceerd.
   </br>Let op: in een dynamische omgeving, wat goed werkt in één keer, werkt later misschien niet goed.

* **Follow-uptests uitvoeren**

   Soms zijn de resultaten van uw experimenten onduidelijk, ofwel omdat er onvoldoende profielen waren om verschillen in behandeling op te sporen, ofwel omdat de door u gedefinieerde behandelingen niet voldoende verschillend waren.

   Als de hypothese die u aan het testen was nog steeds relevant is, kan het uitvoeren van een follow-uptest op een groter of ander publiek, of het aanpassen van uw behandelingen zodat er duidelijkere verschillen zijn, de beste follow-upactie zijn.

* **Diepgaande analyses uitvoeren**

   De behandeling die goed werkt voor één publiek is soms niet de beste behandeling voor een ander publiek. Het doen van diepgaande analyses over hoe de behandelingen zich voor verschillende segmenten gedragen helpen ideeën voor nieuwe tests produceren.

   Op dezelfde manier kan het bestuderen van de prestaties van elke behandeling met verschillende meetwaarden ook een uitgebreider beeld van uw experimenten geven.

   >[!CAUTION]
   >
   >Meer analyses betekenen een grotere kans om een ongewenst effect, of vals positief te ontdekken.
