---
solution: Journey Optimizer
product: journey optimizer
title: Experimentation Accelerator
description: Gegevensgebruik in AI met Experimentation Accelerator
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: inhoud, experiment, meerdere, publiek, behandeling
hide: true
hidefromtoc: true
source-git-commit: 50dcdd30e21fe1b12d502a2b9c478f4ceb546c49
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Gegevensgebruik in AI met Experimentation Accelerator{#experiment-accelerator-security}

>[!BEGINSHADEBOX]

* [Aan de slag met de Experimentation Accelerator](experiment-accelerator.md)
* [Gegevensgebruik in AI met Experimentation Accelerator](experiment-accelerator-security.md)
* [Aanbevolen procedures voor Experimentation Accelerator](experiment-accelerator-best-practices.md)
* [Monitorexperimenten](experiment-accelerator-monitor.md)
* [Metrische experimenten](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

**Adobe Journey Optimizer Experimentation Accelerator** staat u toe om automatisch inzichten te ontdekken en kansen aan te bevelen om uw experimenten en experimenteringsprogramma te verbeteren. De oplossing gebruikt AI en Machine Learning om deze aanbevelingen te verstrekken. Deze verklaring verduidelijkt hoe de gegevens van uw klanten in **Experimentation Accelerator** worden gebruikt.

## Welke gegevens gebruikt de experimenteerversneller?

Momenteel zijn er drie soorten gegevens die door **worden gebruikt de accelerator van de Experimentatie**:

* **Meta-gegevens van de Experimenteer**: experimenteer naam, de definitie van het publiek dat in het experiment wordt gebruikt en de behandelingen in het experiment, b.v. naam, gespleten percentages, plaats of oppervlakte het experiment wordt gediend.

* **Prestaties van de behandelingen**: aantal mensen, gemiddelde van het succes metrisch en standaardafwijking voor elke behandeling.

* **Inhoud van de behandeling**: teruggegeven HTML en het schermschot van de behandeling zoals het aan een gebruiker op uw website zou lijken.

## Wat doet de experimenteerversneller met deze gegevens?

**de accelerator van de Experimentatie** neemt de inhoud voor elke behandeling en leidt tot een inbedding, d.w.z. een wiskundige vertegenwoordiging van de inhoud, dan correleert die inbedingen met de prestaties van de behandelingen. Met dit proces kunnen de inhoudskenmerken worden opgehaald die het beste zijn uitgevoerd voor toekomstig gebruik. Die kenmerken worden vervolgens verwerkt in een door Adobe gehost groottaalmodel, dat ze omzet in leesbare instructies die worden gebruikt om inzichten te genereren en kansen voor te stellen.

## Welke beperkingen heeft Experimentation Accelerator op de gebruikte gegevens?

Elke klant wordt toegewezen aan een specifieke organisatie en sandbox. Voor elke sandbox wordt een speciaal model getraind. Wanneer een sandbox wordt verwijderd, worden alle verwante gegevens, signalen en modellen permanent verwijderd.

* We gebruiken alleen klantgegevens om het model van die klant op te leiden of te verfijnen.

* Wij mengen klanten nooit om een model op te leiden of te verfijnen.

## Zullen Adobe-modellen of AI de gebruikerservaring van een merk automatisch wijzigen?

Nee. **Experimentation Accelerator** slechts doet aanbevelingen van wat kon worden veranderd en hoe het kon worden veranderd. Alleen gebruikers die beschikken over de juiste machtigingen om de ervaring te wijzigen met Journey Optimizer of Target, kunnen aan deze aanbevelingen gevolg geven. Alle aanbevelingen kunnen worden herzien en worden uitgegeven alvorens uit wordt gedrukt.

## Bestaat er enig risico voor hun gegevens of systeemstabiliteit?

**Experimentation Accelerator** neemt slechts gegevens op en analyseert, producerend inzichten en aanbevelingen voor het toekomstige testen. Het heeft geen toegang om het even welke testmontages te wijzigen. Alle suggesties die binnen het hulpmiddel worden geproduceerd worden verzonden naar Doel en Journey Optimizer voor implementatie, die ervoor zorgen dat geen invloed op de huidige activiteiten van een klant wordt gewaarborgd.
