---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Experimentation Accelerator
description: Gegevensgebruik in AI met Journey Optimizer Experimentation Accelerator
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: inhoud, experiment, meerdere, publiek, behandeling
hide: true
hidefromtoc: true
source-git-commit: ddeb3512fbe1d1de86456fe2c3ccd2b3805b5684
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Gegevensgebruik in AI met Journey Optimizer Experimentation Accelerator{#experiment-accelerator-security}

>[!BEGINSHADEBOX]

* [Aan de slag met de Journey Optimizer Experimentation Accelerator](experiment-accelerator.md)
* [Gegevensgebruik in AI met Journey Optimizer Experimentation Accelerator](experiment-accelerator-security.md)
* [Aanbevolen procedures voor Journey Optimizer Experimentation Accelerator](experiment-accelerator-best-practices.md)
* [Monitorexperimenten](experiment-accelerator-monitor.md)
* [Metrische experimenten](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

**Adobe Journey Optimizer Journey Optimizer Experimentation Accelerator** staat u toe om automatisch inzichten te ontdekken en kansen aan te bevelen om uw experimenten en experimenteringsprogramma te verbeteren. De oplossing gebruikt AI en Machine Learning om deze aanbevelingen te verstrekken. Deze verklaring verduidelijkt hoe de gegevens van uw klanten in **Journey Optimizer Experimentation Accelerator** worden gebruikt.

## Welke gegevens gebruikt Journey Optimizer Experimentation Accelerator?

Momenteel zijn er drie soorten gegevens die door **Journey Optimizer Experimentation Accelerator** worden gebruikt:

* **Meta-gegevens van de Experimenteer**: experimenteer naam, de definitie van het publiek dat in het experiment wordt gebruikt en de behandelingen in het experiment, b.v. naam, gespleten percentages, plaats of oppervlakte het experiment wordt gediend.

* **Prestaties van de behandelingen**: aantal mensen, gemiddelde van het succes metrisch en standaardafwijking voor elke behandeling.

* **Inhoud van de behandeling**: teruggegeven HTML en het schermschot van de behandeling zoals het aan een gebruiker op uw website zou lijken.

## Wat doet Journey Optimizer Experimentation Accelerator met deze gegevens?

**Journey Optimizer Experimentation Accelerator** neemt de inhoud voor elke behandeling en leidt tot een inbedding, d.w.z. een wiskundige vertegenwoordiging van de inhoud, dan correleert die inbedingen met de prestaties van de behandelingen. Met dit proces kunnen de inhoudskenmerken worden opgehaald die het beste zijn uitgevoerd voor toekomstig gebruik. Die kenmerken worden vervolgens verwerkt in een door Adobe gehost groottaalmodel, dat ze omzet in leesbare instructies die worden gebruikt om inzichten te genereren en kansen voor te stellen.

## Welke beperkingen heeft Journey Optimizer Experimentation Accelerator op de gebruikte gegevens?

Elke klant wordt toegewezen aan een specifieke organisatie en sandbox. Voor elke sandbox wordt een speciaal model getraind. Wanneer een sandbox wordt verwijderd, worden alle verwante gegevens, signalen en modellen permanent verwijderd.

* We gebruiken alleen klantgegevens om het model van die klant op te leiden of te verfijnen.

* Wij mengen klanten nooit om een model op te leiden of te verfijnen.

## Zullen Adobe-modellen of AI de gebruikerservaring van een merk automatisch wijzigen?

Nee. **Journey Optimizer Experimentation Accelerator** slechts doet aanbevelingen van wat kon worden veranderd en hoe het kon worden veranderd. Alleen gebruikers die beschikken over de juiste machtigingen om de ervaring te wijzigen met Journey Optimizer of Target, kunnen aan deze aanbevelingen gevolg geven. Alle aanbevelingen kunnen worden herzien en worden uitgegeven alvorens uit wordt gedrukt.

## Bestaat er enig risico voor hun gegevens of systeemstabiliteit?

**Journey Optimizer Experimentation Accelerator** neemt slechts gegevens op en analyseert, producerend inzichten en aanbevelingen voor het toekomstige testen. Het heeft geen toegang om het even welke testmontages te wijzigen. Alle suggesties die binnen het hulpmiddel worden geproduceerd worden verzonden naar Doel en Journey Optimizer voor implementatie, die ervoor zorgen dat geen invloed op de huidige activiteiten van een klant wordt gewaarborgd.
