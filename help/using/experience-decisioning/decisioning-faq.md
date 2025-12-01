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
source-git-commit: 59e85eb7a14f88d95b2ef97e3ace11a65f115b75
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---

# Veelgestelde vragen over besluitvorming {#decisioning-faq}

Deze pagina biedt antwoorden op veelgestelde vragen over beslissingsmogelijkheden in Adobe Journey Optimizer.

## Afdekregels {#capping-rules}

+++**wat gebeurt wanneer u meer dan één het afschilderen regel voor een aanbieding creeert? Zullen wij ophouden tonend het aanbod wanneer wij om het even welke het begrenzen regels, of allen van hen aanpassen?**

De aanbieding wordt beperkt zodra **één voorwaarde wordt voldaan aan**. Dit betekent dat een van de plafondregels het aanbod zal beletten om te worden getoond zodra de drempel is bereikt.

Bijvoorbeeld, als u twee het begrenzen regels hebt:
* 5 keer per profiel per week
* 100 keer totaal voor alle gebruikers

Het aanbod wordt niet meer weergegeven aan een gebruiker als deze het vijf keer per week heeft gezien, zelfs als de totale limiet van 100 nog niet is bereikt. Op dezelfde manier, zodra 100 totale indrukken worden bereikt, houdt de aanbieding op worden getoond aan alle gebruikers.

Leer meer over [ het begrenzen regels ](items.md#capping).

+++

## Beoordelingsformule {#ranking-formulas}

+++**waarom zou ik een publiek aan een AI model toevoegen? Wat is het voordeel om publiek tegenover een volledige dataset toe te voegen? Zal het het model beperken of het model uitbreiden?**

Wanneer het werken met AI modellen (specifiek [ gepersonaliseerde optimaliseringsmodellen ](ranking/personalized-optimization-model.md)):

* **Datasets** worden toegevoegd om uw omzettingsgebeurtenissen (kliks, orden, opbrengst) te verzamelen. Dit zijn de resultaten die het model probeert te optimaliseren.
* **Soorten publiek** worden toegevoegd om als voorspellende variabelen in het model worden gebruikt. Zij helpen voorspelling personaliseren om te proberen om kliks, orden, of opbrengst voor verschillende klantensegmenten te voorspellen.

Zowel zijn datasets als publiek nodig voor het gepersonaliseerde optimaliseringsmodel om effectief te werken. Het publiek **beperkt noch breidt** model-in plaats daarvan uit, verstrekken zij extra context die het model helpt betere gepersonaliseerde besluiten maken.

Leer meer over [ AI modellen ](ranking/ai-models.md).

+++

+++**zal toevoegen of aanbiedingen verwijderen aan een inzameling om het even welk effect op het model hebben als ik auto-optimalisering of gepersonaliseerde optimaliseringsmodellen gebruik?**

Beide modellen zullen verkeer aan de volgende beste beschikbare aanbieding leveren die op verkeersgegevens van de laatste 30 dagen wordt gebaseerd.

Als meerdere aanbiedingen tegelijk worden verwijderd en de resterende aanbiedingen in de afgelopen 30 dagen zeer weinig verkeer hebben ontvangen, kan de aanbiedingsdistributie onverwacht gedrag vertonen. Dit zou kunnen leiden tot willekeurige verdeling of vertekening ten aanzien van bepaalde aanbiedingen met een hogere omrekeningskoers op basis van slechts enkele indrukken.

**Beste praktijken**: Wanneer het aanbrengen van significante veranderingen om inzamelingen aan te bieden, zorg ervoor dat de resterende aanbiedingen voldoende historische prestatiesgegevens hebben om optimale modelprestaties te handhaven.

+++

+++**hoe lang neemt het voor de AI modellen om te begrijpen dat er nieuwe toegevoegde inhoud is en beginnen hen aan de mengeling toe te voegen?**

Beide AI-modellen identificeren nieuwe aanbiedingen op de volgende trainingsreeks:

* **auto-optimalisering**: De dagelijkse trainingslooppas
* **Gepersonaliseerde optimalisering**: Wekelijkse opleidingslooppas

Zodra beide modellen zijn geïdentificeerd, zullen zij onmiddellijk de nieuwe aanbiedingen aan sommige bezoekers gaan bedienen om hun prestaties te testen en gegevens over hun doeltreffendheid te verzamelen.

Leer meer over [ auto-optimalisering ](ranking/auto-optimization-model.md) en [ gepersonaliseerde optimalisering ](ranking/personalized-optimization-model.md) modellen.

+++

+++**als wij geen controlegroepen in de modellen AI hebben, leren wij en optimaliseren al verkeer, allen tezelfdertijd?**

Ja. Beide AI-modellen (automatische optimalisatie en gepersonaliseerde optimalisatie) maken gebruik van een &#39;verkennen en benutten&#39;-aanpak:

* Aanvankelijk, zijn beide modellen **100% exploratie**, betekenend zij verschillende aanbiedingen testen om prestatiesgegevens te verzamelen.
* In tijd, leiden de modellen **automatisch de verkenning/exploiteer handel** aangezien de gedragsgebeurtenissen worden verzameld en de voorspellingen verbeteren.
* De modellen verschuiven geleidelijk meer verkeer naar beter presterende aanbiedingen en blijven andere opties onderzoeken en testen.

Dit verzekert ononderbroken het leren en optimalisering over al verkeer zonder afzonderlijke controlegroepen te vereisen.

+++

+++**hoeveel optimaliseringsgebeurtenissen moeten wij statistisch significant zijn? Is er een minimumverkeersdrempel voor een oppervlakte?**

Adobe raadt de volgende minimale vereisten aan om optimale modelprestaties te garanderen:

**geadviseerde minimum (per week):**
* Minstens **1.000 beelden** per aanbieding/punt
* Minstens **100 omzettingsgebeurtenissen** per aanbieding/punt

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

Standaard probeert het systeem geen gepersonaliseerde modellen te maken voor aanbiedingen/items met minder dan 1000 afbeeldingen of 50 conversiegebeurtenissen.

**Belangrijk**: In praktijk, hebben sommige klanten vele aanbiedingen (~300) in één enkel model, en sommige aanbiedingen kunnen zeer beperkende bedrijfsregels hebben. De absolute minima (250 indrukkingen/25 omzettingen per 30 dagen) vertegenwoordigen de laagste drempel die het systeem voor bouwmodellen kan steunen.

Leer meer over [ vereisten van de gegevensinzameling ](data-collection/data-collection.md).

+++

+++**moet de inhoud van de aanbiedingen duidelijk voor de modellen van AI worden onderscheiden om goed te werken? Wat gebeurt als ik veelvoudige aanbiedingen heb die aan elkaar te gelijkaardig zijn?**

Over het algemeen, zal het AI model waarschijnlijker voordelen van verpersoonlijking produceren wanneer **aanbiedingen aan verschillende soorten klanten** worden aangepast.

Wanneer de aanbiedingen zeer gelijkaardig zijn, is één van twee resultaten waarschijnlijk:

* **Vergelijkbare prestaties**: De aanbiedingen zullen identiek presteren en een relatief gelijk aandeel van verkeer ontvangen.
* **Dominantie**: De kleine verschillen kunnen één aanbieding veroorzaken om anderen over alle klantentypes te domineren, en het zal het grootste deel van verkeer ontvangen.

>[!NOTE]
>
>Verschillen in aanbiedingen zijn geen garantie dat één aanbod de andere niet zal domineren. Een aanbieding van 100 euro zal bijvoorbeeld bijna altijd een aanbieding van 50 euro overtreffen voor alle soorten klanten, ongeacht personalisatie.

**Beste praktijken**: Verzeker uw aanbiedingen betekenisvolle differentiatie verstrekken die aan verschillende klantensegmenten voor optimale AI modelprestaties kan aantrekken.

+++

+++**wat gebeurt met het model als er een verkeersanomalie, zoals een enorme verkeerspiek is? Zal het kwesties veroorzaken of onbehagen opheffen?**

In de modellering zou een verkeerspiek worden opgenomen die evenredig is met het andere verkeer in de laatste 30 dagen.

Bijvoorbeeld, zal een 2x dagelijkse verkeerspiek een vrij bescheiden effect op het algemene model hebben, omdat er 29 dagen van normaal verkeer zijn die beduidend meer van de algemene gedragsgegevens vertegenwoordigen.

**Zeer belangrijk punt**: Het het rollen venster van 30 dagen helpt het model stabiliteit tijdens tijdelijke verkeersanomalieën handhaven. Snijden of dips op korte termijn verstoren de prestaties van het model niet significant.

+++

## Verwante onderwerpen {#related-topics}

<!--* [Get started with Decisioning](gs-experience-decisioning.md)-->
* [Beslissingsitems maken](items.md)
* [Overzicht van AI-modellen](ranking/ai-models.md)
* [Afbakening en beperkingen](decisioning-guardrails.md)

