---
solution: Journey Optimizer
product: journey optimizer
title: Werken met georkestreerde campagneactiviteiten
description: Meer informatie over georkestreerde campagneactiviteiten
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: a6b293a5eb1358f692d53c9611b794cf8f7fc753
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Informatie over georkestreerde campagneactiviteiten {#ms-campaign-activities}

De geordende campagneactiviteiten zijn gegroepeerd in drie categorieën. Afhankelijk van de context kunnen de beschikbare activiteiten afwijken.

Alle activiteiten worden beschreven in de volgende onderdelen:

* [Gerichte activiteiten en gegevensbeheer](#targeting)
* [Kanaalactiviteiten](#channel)
* [Stroombeheeractiviteiten](#flow-control)

![](../assets/workflow-activities.png)

## Gerichte activiteiten {#targeting}

Deze activiteiten zijn specifiek gericht op de doelgroepen. Met deze instructies kunt u een of meer doelen maken door een publiek te definiëren en deze soorten publiek te splitsen of te combineren met een doorsnede-, samenvoegings- of uitsluitingsbewerking.

* [ bouwt publiek ](build-audience.md): Bepaal uw doelbevolking. U kunt of een bestaand publiek selecteren of de vraagmodeler gebruiken om uw eigen vraag te bepalen.
* [ dimensie van de Verandering ](change-dimension.md): Verander de het richten dimensie aangezien u uw georkestreerde campagne bouwt.
* [ combineren ](combine.md): Voer segmentatie op uw binnenkomende bevolking uit. U kunt een samenvoeging, een doorsnede of een uitsluiting gebruiken.
* [ Deduplicatie ](deduplication.md): Schrap duplicaten in het resultaat(en) van de binnenkomende activiteiten.
* [ Verrijking ](enrichment.md): Bepaal extra gegevens om in uw georkestreerde campagne te verwerken. Met deze activiteit, kunt u hefboomwerking de binnenkomende overgang en de activiteit vormen om de outputovergang met extra gegevens te voltooien.
* [ Verzoening ](reconciliation.md): Bepaal het verband tussen de gegevens in de gegevens van Journey Optimizer en de gegevens in een het werklijst, bijvoorbeeld gegevens die van een extern dossier worden geladen.
* [ sparen publiek ](save-audience.md): Werk een bestaand publiek bij of creeer een nieuw publiek van de bevolking die stroomopwaarts in een georkestreerde campagne wordt berekend.
* [ Gesplitst ](split.md): De inkomende bevolking van het segment in verscheidene ondergroepen.

## Kanaalactiviteiten {#channel}

Met Adobe Journey Optimizer kunt u marketingcampagnes op meerdere kanalen automatiseren en uitvoeren. U kunt kanaalactiviteiten in het canvas combineren om dwars-kanaal georkestreerde campagne tot stand te brengen die acties kan teweegbrengen die op klantengedrag worden gebaseerd. De volgende **activiteiten van het Kanaal** zijn beschikbaar: E-mail, SMS, Android en de Push van iOS berichten. [ Leer hoe te opstelling een levering in de context van een georkestreerde campagne ](channels.md).

## Stroombeheeractiviteiten {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Eindactiviteit"
>abstract="Het **Eind** activiteit staat u toe om het eind van een georkestreerde campagne grafisch te merken. Deze activiteit heeft geen functioneel effect en is daarom optioneel."

De volgende activiteiten zijn specifiek gericht op het organiseren en uitvoeren van georkestreerde campagnes. Hun voornaamste taak is de coördinatie van de andere activiteiten:

* [ en-sluit zich aan ](and-join.md): Synchroniseer veelvoudige uitvoeringstakken van een georkestreerde campagne.
* **Eind**: Merk grafisch het eind van een georkestreerde campagne. Deze activiteit heeft geen functioneel effect en is daarom optioneel
* [ Fork ](fork.md): Creeer uitgaande overgangen om verscheidene activiteiten tezelfdertijd te beginnen.
* [ Test ](test.md): laat overgangen toe die op gespecificeerde voorwaarden worden gebaseerd.
* [ wacht ](wait.md): Onderbreek tijdelijk uitvoering van een deel van een georkestreerde campagne.
