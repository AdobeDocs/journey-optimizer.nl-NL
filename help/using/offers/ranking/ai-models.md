---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Aan de slag met AI-modellen
description: Meer informatie over AI-modellen waarmee aanbiedingen kunnen worden beoordeeld
badge: label="Verouderd" type="Informative"
feature: Ranking, Decision Management
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 4%

---

# Aan de slag met AI-modellen {#ai-models}

>[!TIP]
>
>Het besluit, de nieuwe beslissingsmogelijkheden van [!DNL Adobe Journey Optimizer], is nu beschikbaar via de op code gebaseerde ervaring en e-mailkanalen! [Meer informatie](../../experience-decisioning/gs-experience-decisioning.md)

Met [!DNL Journey Optimizer] kunt u een getraind modelsysteem gebruiken dat voor een bepaald profiel wordt weergegeven.

Deze eigenschap laat u toe om verschillende **modellen van AI** tot stand te brengen die op uw bedrijfsdoelstellingen worden gebaseerd. Gebruikend deze verschillende op doel-gebaseerde strategieën in een besluit, zal het opgeleide modelsysteem u helpen begrijpen hoe de verschillende AI modellen uw doelstellingen beïnvloeden.

U kunt bijvoorbeeld een AI-model selecteren voor het e-mailkanaal en een ander model voor het pushkanaal. Voor elk kanaal, zal het opgeleide modelsysteem veelvoudige gegevenspunten hefboomwerking bepalen welke aanbieding eerst voor een bepaalde plaatsing zou moeten worden voorgesteld, eerder dan rekening houdend met de de prioritaire scores van aanbiedingen of a [&#x200B; rangschikkende formule &#x200B;](create-ranking-formulas.md).

>[!IMPORTANT]
>
>AI-modellen worden momenteel niet ondersteund in door Journey Optimizer geschreven kanalen.

➡️ [Ontdek deze functie in video](#video)

## AI-modeltypen {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_type"
>title="Het modeltype kiezen"
>abstract="Selecteer het type van AI model u wilt tot stand brengen: **auto-optimalisering** optimaliseert aanbiedingen die op het verleden aanbiedingsprestaties worden gebaseerd, terwijl **Gepersonaliseerde optimalisering** optimaliseert en verpersoonlijkt aanbiedingen die op publiek worden gebaseerd en prestaties aanbieden."
>additional-url="https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Een AI-model maken"

Er zijn twee typen AI-modellen beschikbaar in [!DNL Journey Optimizer] :

* **auto-optimalisatiemodellen** streven om aanbiedingen te dienen die het rendement (KPIs) maximaliseren dat door bedrijfscliënten wordt geplaatst. Deze KPI’s kunnen de vorm aannemen van omrekeningskoersen, inkomsten, enz. Op dit punt, richt de auto-optimalisering zich op optimaliserend aanbiedingskliks met aanbiedingsomzetting als ons doel. Automatisch optimaliseren is niet-gepersonaliseerd en optimaliseert op basis van &#39;algemene&#39; prestaties van de aanbiedingen. [Meer informatie](auto-optimization-model.md)

* **Gepersonaliseerde optimalisatiemodellen** staan u toe om bedrijfsdoelstellingen te bepalen en klantengegevens te gebruiken om zaken-georiënteerde modellen op te leiden om gepersonaliseerde aanbiedingen te dienen en KPIs te maximaliseren. [Meer informatie](personalized-optimization-model.md)

## Een AI-model maken {#create-ai-model}

U kunt als volgt AI-modellen maken en gebruiken:

1. Maak een gegevensset waarin conversie- en impliciete gebeurtenissen worden verzameld. [Meer informatie](../data-collection/create-dataset.md)

1. Maak een AI-model dat gebeurtenissen van de dataset gebruikt om aanbiedingen te rangschikken. [Meer informatie](create-ranking-strategies.md)

1. Configureer uw aanbiedingsschema om automatisch gebeurtenissen vast te leggen. [Meer informatie](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >AI-modellen vereisen dat feedbackgebeurtenissen worden verzonden als ervaringsgebeurtenissen om te worden verzameld. [&#x200B; Leer meer over de inzameling van de gegevens van het Beheer van Besluit &#x200B;](../data-collection/data-collection.md)

1. Wijs het AI-model toe aan een plaatsing in een besluit om in aanmerking komende aanbiedingen te classificeren. [Meer informatie](../offer-activities/configure-offer-selection.md)

## Hoe kan ik-video {#video}

Leer hoe u een AI-model voor Offer Decisioning maakt en hoe u dit model toepast op een beslissing.

>[!VIDEO](https://video.tv.adobe.com/v/3419959?quality=12)
