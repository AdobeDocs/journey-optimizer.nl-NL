---
solution: Journey Optimizer
product: journey optimizer
title: Werken met geordende campagneactiviteiten
description: Meer informatie over geordende campagneactiviteiten
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
version: Campaign Orchestration
source-git-commit: 4d5505cbb46bdff846218bfc3657c6a6e5447af3
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 2%

---


# Informatie over geordende campagneactiviteiten {#orchestrated-campaign-activities}

De geordende campagneactiviteiten zijn gegroepeerd in drie categorieën. Afhankelijk van de context kunnen de beschikbare activiteiten afwijken.

Alle activiteiten worden beschreven in de volgende onderdelen:

* [Targetingactiviteiten](#targeting)
* [Kanaalactiviteiten](#channel)
* [Workflowbeheeractiviteiten](#flow-control)

![&#x200B; Lijst van activiteiten beschikbaar in het canvas &#x200B;](../assets/orchestrated-activities.png){width="80%" align="left"}


>[!NOTE]
>
>* Afhankelijk van uw licentiemodel, uw machtigingen en uw implementatie kunnen de beschikbare activiteiten afwijken.
>
>* Het aantal activiteiten in een geordende campagne is beperkt tot 500.


## Targetingactiviteiten {#targeting}

Deze activiteiten zijn specifiek gericht op de doelgroepen. Met deze instructies kunt u een of meer doelen maken door een publiek te definiëren en deze soorten publiek te splitsen of te combineren met een doorsnede-, samenvoegings- of uitsluitingsbewerking.

![&#x200B; Lijst van het richten van activiteiten &#x200B;](../assets/targeting-activities.png){width="40%" align="left"}

De beschikbare gerichte activiteiten zijn:

* [&#x200B; bouwt publiek &#x200B;](build-audience.md): Bepaal uw doelbevolking. U kunt of een bestaand publiek selecteren of de regelbouwer gebruiken om uw eigen vraag te bepalen.
* [&#x200B; dimensie van de Verandering &#x200B;](change-dimension.md): Verander de het richten dimensie aangezien u uw Geordende campagne bouwt.
* [&#x200B; combineren &#x200B;](combine.md): Voer segmentatie op uw binnenkomende bevolking uit. U kunt een samenvoeging, een doorsnede of een uitsluiting gebruiken.
* [&#x200B; Deduplicatie &#x200B;](deduplication.md): Schrap duplicaten in het resultaat(en) van de binnenkomende activiteiten.
* [&#x200B; Verrijking &#x200B;](enrichment.md): Bepaal extra gegevens om in uw Geordende campagne te verwerken. Met deze activiteit, kunt u hefboomwerking de binnenkomende overgang en de activiteit vormen om de outputovergang met extra gegevens te voltooien.
* [&#x200B; Verzoening &#x200B;](reconciliation.md): Bepaal het verband tussen de gegevens in de gegevens van Journey Optimizer en de gegevens in een het werklijst, bijvoorbeeld gegevens die van een extern dossier worden geladen.
* [&#x200B; Gesplitst &#x200B;](split.md): De inkomende bevolking van het segment in verscheidene ondergroepen.

## Kanaalactiviteiten {#channel}

Met Adobe Journey Optimizer kunt u marketingcampagnes op meerdere kanalen automatiseren en uitvoeren. U kunt [&#x200B; kanaalactiviteiten &#x200B;](channels.md) in het canvas combineren om dwars-kanaal Geordende campagne tot stand te brengen die acties kan teweegbrengen die op klantengedrag worden gebaseerd.

Leer hoe te om [&#x200B; een kanaalactie in een Geordende campagne &#x200B;](channels.md) tot stand te brengen.

## Workflowbeheeractiviteiten {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Eindactiviteit"
>abstract="Het **Eind** activiteit staat u toe om het eind van een Geordende campagne grafisch te merken. Deze activiteit heeft geen functioneel effect en is daarom optioneel."

De volgende activiteiten zijn specifiek gericht op het organiseren en uitvoeren van geordende campagnes. Hun belangrijkste taak is de coördinatie van de andere activiteiten.

![&#x200B; Lijst van de activiteiten van de debietcontrole &#x200B;](../assets/flow-control-activities.png){width="20%" align="left"}

Beschikbare activiteiten op het gebied van stroombeheersing zijn:

* [&#x200B; en-sluit zich aan &#x200B;](and-join.md): Synchroniseer veelvoudige uitvoeringstakken van een Geordende campagne.
* [&#x200B; Fork &#x200B;](fork.md): Creeer uitgaande overgangen om verscheidene activiteiten tezelfdertijd te beginnen.
* [&#x200B; wacht &#x200B;](wait.md): Onderbreek tijdelijk uitvoering van een deel van een Geordende campagne.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>Het **Eind** activiteit merkt grafisch het eind van een Geordende campagne. Deze activiteit heeft geen functioneel effect en is daarom optioneel
