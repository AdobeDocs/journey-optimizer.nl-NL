---
product: experience platform
solution: Experience Platform
title: Aan de slag met AI-modellen
description: Meer informatie over AI-modellen waarmee aanbiedingen kunnen worden beoordeeld
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 4f331eff73991c32682ba2c1ca5f6b7341a561e1
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 3%

---

# Aan de slag met AI-modellen {#ai-models}

[!DNL Journey Optimizer] kunt u een getraind modelsysteem gebruiken dat aanbiedingen aan vertoning voor een bepaald profiel rangschikt.

Met deze functie kunt u verschillende **AI-modellen** gebaseerd op uw bedrijfsdoelstellingen. Gebruikend deze verschillende op doel-gebaseerde strategieën in een besluit, zal het opgeleide modelsysteem u helpen begrijpen hoe de verschillende AI modellen uw doelstellingen beïnvloeden.

U kunt bijvoorbeeld een AI-model selecteren voor het e-mailkanaal en een ander model voor het pushkanaal. Voor elk kanaal zal het opgeleide modelsysteem veelvoudige gegevenspunten gebruiken om te bepalen welk aanbod eerst voor een bepaalde plaatsing zou moeten worden voorgesteld eerder dan rekening houdend met de prioritaire scores van de aanbiedingen of a [waarderingsformule](create-ranking-formulas.md).

>[!IMPORTANT]
>
>Vooralsnog worden classificatiemodellen niet ondersteund in door Journey Optimizer geschreven kanalen.

## AI-modeltypen {#ai-model-types}

Er zijn twee typen AI-modellen beschikbaar in [!DNL Journey Optimizer]:

* **Modellen voor automatische optimalisatie** ernaar streven aanbiedingen te leveren die het rendement (KPI&#39;s) maximaliseren dat door zakelijke klanten wordt vastgesteld. Deze KPI’s kunnen de vorm aannemen van omrekeningskoersen, inkomsten, enz. Op dit punt, richt de auto-optimalisering zich op optimaliserend aanbiedingskliks met aanbiedingsomzetting als ons doel. Automatisch optimaliseren is niet-gepersonaliseerd en optimaliseert op basis van &#39;algemene&#39; prestaties van de aanbiedingen. [Meer informatie](auto-optimization-model.md)

* **Aangepaste optimalisatiemodellen** staat u toe om bedrijfsdoelstellingen te bepalen en klantengegevens te gebruiken om zaken-georiënteerde modellen op te leiden om gepersonaliseerde aanbiedingen te dienen en KPIs te maximaliseren. [Meer informatie](personalized-optimization-model.md)

## Een AI-model maken {#create-ai-model}

U kunt als volgt AI-modellen maken en gebruiken:

1. Maak een gegevensset waarin conversie- en importeergebeurtenissen worden verzameld. [Meer informatie](../data-collection/create-dataset.md)

1. Maak een AI-model dat gebeurtenissen van de dataset gebruikt om aanbiedingen te rangschikken. [Meer informatie](create-ranking-strategies.md)

1. Configureer uw aanbiedingsschema om automatisch gebeurtenissen vast te leggen. [Meer informatie](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Het rangschikken modellen vereisen terugkoppelt gebeurtenissen die binnen als ervaringsgebeurtenissen worden verzonden om worden verzameld. [Meer informatie over het verzamelen van gegevens over het beheer van beslissingen](../data-collection/data-collection.md)

1. Wijs het AI-model toe aan een plaatsing in een besluit om in aanmerking komende aanbiedingen te classificeren. [Meer informatie](../offer-activities/configure-offer-selection.md)
