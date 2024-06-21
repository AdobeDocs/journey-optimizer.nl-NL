---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met het experimenteren met inhoud
description: Meer informatie over content experimenteren in Journey Optimizer
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: aan de slag, starten, inhoud, experimenteren
exl-id: 7fe4b24e-f60a-4107-a064-00010b0cbbfc
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '1961'
ht-degree: 0%

---

# Aan de slag met content-experimenten {#get-started-experiment}

## Wat is een inhoudexperiment?

Met experimenten met inhoud kunt u inhoud optimaliseren voor de acties in uw campagnes.

Experimenten bestaan uit een reeks gerandomiseerde onderzoeken, die in de context van online tests betekenen dat sommige willekeurig geselecteerde gebruikers worden blootgesteld aan een bepaalde variatie van een bericht en een andere willekeurig gekozen groep gebruikers aan een andere behandeling. Nadat u het bericht hebt verzonden, kunt u de resultaten meten die u interesseert, bijvoorbeeld wanneer u e-mailberichten opent of klikt.

## Waarom experimenten uitvoeren?

![](assets/content_experiment_schema.png)

Met behulp van experimenten kunt u de wijzigingen isoleren die tot verbeteringen in uw metriek leiden. Zoals in bovenstaande afbeelding wordt geïllustreerd: sommige willekeurig geselecteerde gebruikers worden blootgesteld aan elke behandelingsgroep, wat betekent dat de groepen gemiddeld dezelfde kenmerken zullen hebben. Elk verschil in uitkomsten kan dus worden geïnterpreteerd als zijnde te wijten aan de verschillen in de ontvangen behandelingen, dat wil zeggen dat u een oorzakelijk verband kunt vaststellen tussen de veranderingen die u hebt aangebracht en de uitkomsten waarin u geïnteresseerd bent.

Dit staat u toe om gegevens gedreven besluiten in het optimaliseren van uw bedrijfsdoelstellingen te nemen.

Voor Inhoud-experimenten in Adobe Journey Optimizer kunt u ideeën testen, zoals:

* **Onderwerpregel**: Wat kan het effect zijn van een wijziging in de toon of de mate van personalisatie van een onderwerpregel?
* **Berichtinhoud**: Zal het wijzigen van de visuele lay-out van een e-mailbericht ertoe leiden dat er meer op de e-mail wordt geklikt?

## Hoe werkt content experimenteren? {#content-experiment-work}

### Willekeurige toewijzing

Bij het experimenteren met inhoud in Adobe Journey Optimizer wordt een pseudo-willekeurige hash van de identiteit van de bezoeker gebruikt om gebruikers in het doelpubliek willekeurig toe te wijzen aan een van de behandelingen die u hebt gedefinieerd. Het hashingmechanisme zorgt ervoor dat in scenario&#39;s waar de bezoeker een campagne veelvoudige tijden ingaat, zij deterministisch de zelfde behandeling zullen ontvangen.

In detail, wordt het algoritme MumurHash3 met 32 bits gebruikt om het koord van de gebruikersidentiteit in één van 10.000 emmers te hakken. In een inhoudexperiment met 50% van het verkeer dat aan elke behandeling wordt toegewezen, zullen gebruikers die in emmers 1-5.000 vallen de eerste behandeling krijgen, terwijl gebruikers in de emmers 5.001 tot 10.000 de tweede behandeling zullen krijgen. Aangezien pseudo-willekeurige hashing wordt gebruikt, is het mogelijk dat de bezoeker niet precies 50-50 splitst. De splitsing is echter statistisch gelijk aan het splitsingspercentage van het doel.

Merk op dat als deel van het vormen van elke campagne met een inhoudexperiment, u een identiteitsnamespace moet kiezen waarvan userId voor het randomisatiealgoritme zal worden geselecteerd. Dit staat los van de [uitvoeringsadressen](../configuration/primary-email-addresses.md).

### Gegevensverzameling en -analyse

Op het tijdstip van taak d.w.z., wanneer het bericht in uitgaande kanalen wordt verzonden, of wanneer de gebruiker de campagne in binnenkomende kanalen ingaat, wordt een &quot;taakverslag&quot;geregistreerd aan de aangewezen systeemdataset. Hiermee wordt vastgelegd aan welke behandeling de gebruiker is toegewezen, samen met experiment- en campagne-id&#39;s.

De objectieve metriek kan in twee hoofdklassen worden gegroepeerd:

* Directe cijfers, waarbij de gebruiker rechtstreeks op de behandeling reageert, bijvoorbeeld door een e-mail te openen of op een koppeling te klikken.
* Indirecte of &quot;bodem van trechter&quot; metriek, die optreedt nadat de gebruiker aan de behandeling is blootgesteld.

Voor directe objectieve metriek waar Adobe Journey Optimizer uw berichten bijhoudt, worden de reactiegebeurtenissen van eind - gebruikers automatisch geëtiketteerd met campagne en behandelingsidentificateurs, die directe vereniging van reactie metrisch met een behandeling toestaan. [Meer informatie over bijhouden](../email/message-tracking.md).

![](assets/technote_2.png)

Voor indirecte of &quot;onderste van funnel&quot; doelstellingen zoals aankopen, worden de responsgebeurtenissen van eindgebruikers niet getagd met campagne- en behandelingsidentificatoren, d.w.z. dat een aankoopgebeurtenis plaatsvindt na blootstelling aan een behandeling, er is geen directe koppeling tussen die aankoop en een voorafgaande behandelingstoewijzing. Voor deze metriek zal de Adobe de behandeling koppelen aan de onderkant van de trechter-conversiegebeurtenis als:

* De gebruikersidentiteit is hetzelfde op het moment van de toewijzing en conversie.
* De conversie vindt plaats binnen zeven dagen na de toezending van de behandeling.

![](assets/technote_3.png)

Adobe Journey Optimizer gebruikt vervolgens geavanceerde &#39;op elk moment geldige&#39; statistische methoden om deze onbewerkte rapportgegevens te interpreteren, zodat u uw experimentatierapporten kunt interpreteren. Raadpleeg [deze pagina](../content-management/experiment-calculations.md) voor meer informatie.

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
Het aantal gebruikers dat in uw experiment moet worden omvat hangt van de effect grootte af u wenst te ontdekken, de variantie of de spreiding van uw doel metrisch, evenals uw tolerantie voor vals positieve en vals negatieve fouten. In klassieke experimenten kunt u een [voorbeeldgroottecalculator](https://experienceleague.adobe.com/tools/calculator/testcalculator.html){_blank} om te bepalen hoe lang u uw test moet in werking stellen.
+++

+++Statistische onzekerheid begrijpen

Als u een experiment uitvoert waarbij 1000 gebruikers één behandeling hebben gezien, en de conversiesnelheid wordt ingesteld op 5%. Zou dit de werkelijke omrekeningskoers zijn als al uw gebruikers hierin zouden worden opgenomen? Wat zou de werkelijke omrekeningskoers zijn?
Statistische methoden bieden ons een manier om die onzekerheid te formaliseren. Een van de belangrijkste concepten die u moet begrijpen wanneer u online experimenten uitvoert, is dat de waargenomen conversietarieven consistent zijn met een reeks onderliggende werkelijke conversiekoersen. Dit houdt in dat u moet wachten tot deze schattingen precies genoeg zijn voordat u een conclusie probeert te trekken. Betrouwbaarheidsintervallen en Vertrouwen helpen ons deze onzekerheid te kwantificeren.
+++

+++Nieuwe hypothesen maken en voortdurend testen

Om echte bedrijfsinzichten te bereiken, zou u zich aan enkel één Experiment moeten houden. In plaats daarvan, follow-up experimenten door nieuwe hypothesen te formuleren, en nieuwe tests met verschillende veranderingen, op verschillende soorten publiek, en door de invloed op de verschillende metriek te onderzoeken.
+++

## De resultaten van uw experimenten interpreteren {#interpret-results}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_summary"
>title="Widget Overzicht"
>abstract="De widget Samenvatting geeft een overzicht van de resultaten van uw experiment, bijvoorbeeld of deze overtuigend zijn of niet. Het biedt een snelle en gemakkelijke manier om het resultaat van uw experiment te begrijpen."

![](assets/experimentation_report_3.png)

In dit gedeelte worden de experimentele rapporten beschreven en wordt uitgelegd hoe de verschillende statistische hoeveelheden die worden gepresenteerd, moeten worden geïnterpreteerd.

Hier volgen enkele richtlijnen voor het interpreteren van de resultaten van uw Content Experiment.

Bij een volledige beschrijving van de resultaten moet rekening worden gehouden met alle beschikbare gegevens (bv. steekproefgrootten, omrekeningskoersen, betrouwbaarheidsintervallen enz.) en niet alleen met de verklaring van afdoend of niet. Zelfs als een resultaat nog niet overtuigend is, kan er nog steeds overtuigend bewijs zijn dat de ene behandeling anders is dan de andere.

Voor meer begrip van statistische berekeningen, verwijs naar dit [page](../content-management/experiment-calculations.md).

### 1. Vergelijk genormaliseerde meetgegevens {#normalized-metrics}

Wanneer u de prestaties van twee behandelingen vergelijkt, moet u altijd de genormaliseerde meetwaarden vergelijken om rekening te houden met eventuele verschillen in het aantal profielen dat aan elke behandeling wordt blootgesteld.

Als het experimentele doel bijvoorbeeld is ingesteld op **[!UICONTROL Unique Opens]** en een bepaalde behandeling werd getoond aan 10.000 Profielen met 200 Unieke Opens geregistreerd, dan vertegenwoordigt dit een **[!UICONTROL Conversion Rate]** van 2%. Voor niet-unieke metriek, bijvoorbeeld Opens metrisch, wordt genormaliseerde metrisch getoond als a **[!UICONTROL Count per Profile]**, terwijl voor ononderbroken metriek zoals het Totaal van de Prijs, genormaliseerde metrisch wordt getoond als **[!UICONTROL Total per Profile]**.

### 2. Focus op betrouwbaarheidsintervallen {#confidence-intervals}

Wanneer u experimenteert met monsters van uw profielen, geeft de conversiekoers die voor een bepaalde behandeling wordt waargenomen een schatting van de werkelijke onderliggende conversiesnelheid.

Bijvoorbeeld als Behandeling A een **[!UICONTROL Conversion Rate]** van 3%, terwijl behandeling B een waargenomen waarde heeft **[!UICONTROL Conversion Rate]** van 2%, is Behandeling A beter dan Behandeling B? Om dit te kunnen beantwoorden, moeten we eerst de onzekerheid in deze waargenomen omrekeningskoersen kwantificeren.

Vertrouwensintervallen helpen de mate van onzekerheid in de geschatte omrekeningskoersen te kwantificeren, maar bredere betrouwbaarheidsintervallen impliceren meer onzekerheid. Als er meer profielen aan het experiment worden toegevoegd, worden de intervallen kleiner, wat een nauwkeurigere schatting is. Het betrouwbaarheidsinterval vertegenwoordigt een reeks conversiekoersen die compatibel zijn met de waargenomen gegevens.

Als de betrouwbaarheidsintervallen voor twee behandelingen nauwelijks overlappen, betekent dit dat de twee behandelingen verschillende conversiesnelheden hebben. Maar als er veel overlap is tussen de betrouwbaarheidsintervallen voor twee behandelingen, is het waarschijnlijker dat de twee behandelingen dezelfde conversiesnelheid hebben.

Adobe gebruikt 95% altijd geldige betrouwbaarheidsintervallen, of betrouwbaarheidsreeksen, wat betekent dat de resultaten op elk moment tijdens het experiment veilig kunnen worden bekeken.

### 3. Begrijp optillen {#understand-lift}

De samenvatting van het Experimentenrapport bevat de **[!UICONTROL Lift over Baseline]**, hetgeen een maatstaf is voor de procentuele verbetering van de conversiesnelheid van een bepaalde behandeling ten opzichte van de uitgangswaarde. Dit is het verschil in prestaties tussen een bepaalde behandeling en de basislijn, gedeeld door de prestaties van de basislijn, uitgedrukt als een percentage.

### 3. Begrijp vertrouwen {#understand-confidence}

Terwijl u zich vooral op de **[!UICONTROL Confidence interval]** Voor de uitvoering van elke behandeling toont de Adobe ook het Vertrouwen, wat een probabilistische maat is van hoeveel bewijs er is dat een bepaalde behandeling gelijk is aan de basisbehandeling. Een hoger vertrouwen wijst op minder bewijs voor de veronderstelling dat de basislijn en de niet-basislijn behandelingen gelijke prestaties hebben. Meer in het bijzonder is het vertrouwen dat wordt weergegeven een waarschijnlijkheid (uitgedrukt als een percentage) dat we een kleiner verschil in omrekeningskoersen tussen een bepaalde behandeling en de basislijn zouden hebben gezien, als er in werkelijkheid geen verschil is in de werkelijke onderliggende omrekeningskoersen. Wat de p-waarden betreft, wordt een vertrouwen van 1 tot p-waarde weergegeven.

De Adobe gebruikt het Vertrouwen van &quot;om het even welk Geldige&quot;, en &quot;om het even welk Geldige&quot;p-waarden die met de hierboven beschreven Vertrouwensopeenvolgingen verenigbaar zijn.

### 4. Statistisch belang

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

  De behandeling die goed werkt voor één publiek is soms niet de beste behandeling voor een ander publiek. Door diepgaande analyses uit te voeren over de manier waarop behandelingen voor verschillende doelgroepen zich gedragen, worden ideeën voor nieuwe tests gegenereerd.

  Op dezelfde manier kan het bestuderen van de prestaties van elke behandeling met verschillende meetwaarden ook een uitgebreider beeld van uw experimenten geven.

  >[!CAUTION]
  >
  >Meer analyses betekenen een grotere kans om een ongewenst effect, of vals positief te ontdekken.
