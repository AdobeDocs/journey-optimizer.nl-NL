---
solution: Journey Optimizer
product: journey optimizer
title: Werken met geordende campagneactiviteiten
description: Meer informatie over geordende campagneactiviteiten
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
version: Campaign Orchestration
source-git-commit: 43fa71d7ec05e8c4b1ccd8d8c0ff8727128f5030
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 3%

---


# Informatie over geordende campagneactiviteiten {#orchestrated-campaign-activities}

De geordende campagneactiviteiten zijn gegroepeerd in drie categorieën. Afhankelijk van de context kunnen de beschikbare activiteiten afwijken.

Alle activiteiten worden beschreven in de volgende onderdelen:

* [Targetingactiviteiten](#targeting)
* [Kanaalactiviteiten](#channel)
* [Workflowbeheeractiviteiten](#flow-control)

![ Lijst van activiteiten beschikbaar in het canvas ](../assets/orchestrated-activities.png){width="80%" align="left"}


>[!NOTE]
>
>* Afhankelijk van uw licentiemodel, uw machtigingen en uw implementatie kunnen de beschikbare activiteiten afwijken.
>
>* Het aantal activiteiten in een geordende campagne is beperkt tot 500.


## Targetingactiviteiten {#targeting}

Deze activiteiten zijn specifiek gericht op de doelgroepen. Met deze instructies kunt u een of meer doelen maken door een publiek te definiëren en deze soorten publiek te splitsen of te combineren met een doorsnede-, samenvoegings- of uitsluitingsbewerking.

![ Lijst van het richten van activiteiten ](../assets/targeting-activities.png){width="40%" align="left"}

De beschikbare gerichte activiteiten zijn:

* [ bouwt publiek ](build-audience.md): Bepaal uw doelbevolking. U kunt of een bestaand publiek selecteren of de regelbouwer gebruiken om uw eigen vraag te bepalen.
* [ dimensie van de Verandering ](change-dimension.md): Verander de het richten dimensie aangezien u uw Geordende campagne bouwt.
* [ combineren ](combine.md): Voer segmentatie op uw binnenkomende bevolking uit. U kunt een samenvoeging, een doorsnede of een uitsluiting gebruiken.
* [ Deduplicatie ](deduplication.md): Schrap duplicaten in het resultaat(en) van de binnenkomende activiteiten.
* [ Verrijking ](enrichment.md): Bepaal extra gegevens om in uw Geordende campagne te verwerken. Met deze activiteit, kunt u hefboomwerking de binnenkomende overgang en de activiteit vormen om de outputovergang met extra gegevens te voltooien.
* [ Verzoening ](reconciliation.md): Bepaal het verband tussen de gegevens in de gegevens van Journey Optimizer en de gegevens in een het werklijst, bijvoorbeeld gegevens die van een extern dossier worden geladen.
* [ Gesplitst ](split.md): De inkomende bevolking van het segment in verscheidene ondergroepen.

## Kanaalactiviteiten {#channel}

Met Adobe Journey Optimizer kunt u marketingcampagnes op meerdere kanalen automatiseren en uitvoeren. U kunt [ kanaalactiviteiten ](channels.md) in het canvas combineren om dwars-kanaal Geordende campagne tot stand te brengen die acties kan teweegbrengen die op klantengedrag worden gebaseerd.

Leer hoe te om [ een kanaalactie in een Geordende campagne ](channels.md) tot stand te brengen.

## Workflowbeheeractiviteiten {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Eindactiviteit"
>abstract="Het **Eind** activiteit staat u toe om het eind van een Geordende campagne grafisch te merken. Deze activiteit heeft geen functioneel effect en is daarom optioneel."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_signal"
>title="Extern signaal"
>abstract="extern signaal"

De volgende activiteiten zijn specifiek gericht op het organiseren en uitvoeren van geordende campagnes. Hun belangrijkste taak is de coördinatie van de andere activiteiten.

![ Lijst van de activiteiten van de debietcontrole ](../assets/flow-control-activities.png){width="20%" align="left"}

Beschikbare activiteiten op het gebied van stroombeheersing zijn:

* [ en-sluit zich aan ](and-join.md): Synchroniseer veelvoudige uitvoeringstakken van een Geordende campagne.
* [ Fork ](fork.md): Creeer uitgaande overgangen om verscheidene activiteiten tezelfdertijd te beginnen.
* [ wacht ](wait.md): Onderbreek tijdelijk uitvoering van een deel van een Geordende campagne.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>Het **Eind** activiteit merkt grafisch het eind van een Geordende campagne. Deze activiteit heeft geen functioneel effect en is daarom optioneel
