---
solution: Journey Optimizer
product: journey optimizer
title: Werken met uit meerdere stappen bestaande campagneactiviteiten
description: Meer informatie over het uitvoeren van multi-step campagneactiviteiten
hide: true
hidefromtoc: true
source-git-commit: 658d82820d3f307481c44a142c38727f777fd879
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---


# Informatie over multi-step campagneactiviteiten {#ms-campaign-activities}

De campagneactiviteiten met meerdere stappen worden in drie categorieën gegroepeerd. Afhankelijk van de context kunnen de beschikbare activiteiten afwijken.

Alle activiteiten worden beschreven in de volgende onderdelen:

* [Gerichte activiteiten en gegevensbeheer](#targeting)
* [Kanaalactiviteiten](#channel)
* [Stroombeheeractiviteiten](#flow-control)

![](../assets/workflow-activities.png)

## Gerichte activiteiten {#targeting}

Deze activiteiten zijn specifiek gericht op de doelgroepen. Met deze instructies kunt u een of meer doelen maken door een publiek te definiëren en deze soorten publiek te splitsen of te combineren met een doorsnede-, samenvoegings- of uitsluitingsbewerking.

* [ bouwt publiek ](build-audience.md): Bepaal uw doelbevolking. U kunt of een bestaand publiek selecteren of de vraagmodeler gebruiken om uw eigen vraag te bepalen.
* [ dimensie van de Verandering ](change-dimension.md): Verander de het richten dimensie aangezien u uw multi-step campagne bouwt.
* [ combineren ](combine.md): Voer segmentatie op uw binnenkomende bevolking uit. U kunt een samenvoeging, een doorsnede of een uitsluiting gebruiken.
* [ Deduplicatie ](deduplication.md): Schrap duplicaten in het resultaat(en) van de binnenkomende activiteiten.
* [ Verrijking ](enrichment.md): Bepaal extra gegevens om in uw multi-step campagne te verwerken. Met deze activiteit, kunt u hefboomwerking de binnenkomende overgang en de activiteit vormen om de outputovergang met extra gegevens te voltooien.
* [ Verzoening ](reconciliation.md): Bepaal het verband tussen de gegevens in de gegevens van Journey Optimizer en de gegevens in een het werklijst, bijvoorbeeld gegevens die van een extern dossier worden geladen.
* [ sparen publiek ](save-audience.md): Werk een bestaand publiek bij of creeer een nieuw publiek van de bevolking die stroomopwaarts in een multi-step campagne wordt berekend.
* [ Gesplitst ](split.md): De inkomende bevolking van het segment in verscheidene ondergroepen.

## Gegevensbeheeractiviteiten {#data}

Deze activiteiten zijn specifiek gericht op het manipuleren en verrijken van bevolkingsgegevens.

* [ het dossier van de Lading ](load-file.md): Het werk met profielen en gegevens die in een extern dossier worden opgeslagen.
* [ gegevens van de Update ](update-data.md): Voer massa-updates op gebieden in het gegevensbestand uit. Met verschillende opties kunt u de gegevensupdate aanpassen.

## Kanaalactiviteiten {#channel}

Met Adobe Journey Optimizer kunt u marketingcampagnes op meerdere kanalen automatiseren en uitvoeren. U kunt kanaalactiviteiten combineren tot het canvas om multi-step campagne voor meerdere kanalen te maken die acties kan activeren op basis van het gedrag van de klant. De volgende **activiteiten van het Kanaal** zijn beschikbaar: E-mail, SMS, Android en de Push van iOS berichten. [ Leer hoe te opstelling een levering in de context van een multi-step campagne ](channels.md).

## Stroombeheeractiviteiten {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Eindactiviteit"
>abstract="Het **Eind** activiteit staat u toe om het eind van een multi-step campagne grafisch te merken. Deze activiteit heeft geen functioneel effect en is daarom optioneel."

De volgende activiteiten zijn specifiek gericht op het organiseren en uitvoeren van meerfasencampagnes. Hun voornaamste taak is de coördinatie van de andere activiteiten:

* [ en-sluit zich aan ](and-join.md): Synchroniseer veelvoudige uitvoeringstakken van een multi-step campagne.
* **Eind**: Merk grafisch het eind van een multi-step campagne. Deze activiteit heeft geen functioneel effect en is daarom optioneel
* [ Fork ](fork.md): Creeer uitgaande overgangen om verscheidene activiteiten tezelfdertijd te beginnen.
* [ Planner ](scheduler.md): Plan wanneer de multi-step campagne begonnen wordt.
* [ Test ](test.md): laat overgangen toe die op gespecificeerde voorwaarden worden gebaseerd.
* [ wacht ](wait.md): Onderbreek tijdelijk uitvoering van een deel van een multi-step campagne.
