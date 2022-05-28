---
product: experience platform
solution: Experience Platform
title: Aan de slag met AI-modellen
description: Meer informatie over AI-modellen waarmee aanbiedingen kunnen worden beoordeeld
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 3%

---

# Aan de slag met AI-modellen {#ai-models}

[!DNL Journey Optimizer] kunt u een getraind modelsysteem gebruiken dat aanbiedingen aan vertoning voor een bepaald profiel rangschikt.

Met deze functie kunt u verschillende **AI-modellen** gebaseerd op uw bedrijfsdoelstellingen. Gebruikend deze verschillende op doel-gebaseerde strategieën in een besluit, zal het opgeleide modelsysteem u helpen begrijpen hoe de verschillende AI modellen uw doelstellingen beïnvloeden.

U kunt bijvoorbeeld een AI-model selecteren voor het e-mailkanaal en een ander model voor het pushkanaal. Voor elk kanaal zal het opgeleide modelsysteem veelvoudige gegevenspunten gebruiken om te bepalen welk aanbod eerst voor een bepaalde plaatsing zou moeten worden voorgesteld eerder dan rekening houdend met de prioritaire scores van de aanbiedingen of a [waarderingsformule](create-ranking-formulas.md).

## AI-modeltypen {#ai-model-types}

Voor nu, [!DNL Journey Optimizer]*** één AI-model biedt, **Automatische optimalisatie**, die de aanbiedingen optimaliseert op basis van de prestaties van de vorige aanbieding. Gedetailleerde informatie over dit type AI-model is beschikbaar in [deze sectie](auto-optimization-model.md).

## Een AI-model maken {#create-ai-model}

U kunt als volgt AI-modellen maken en gebruiken:

1. Maak een gegevensset waarin conversie- en importeergebeurtenissen worden verzameld. [Meer informatie](create-dataset.md)
1. Maak een AI-model dat gebeurtenissen van de dataset gebruikt om aanbiedingen te rangschikken. [Meer informatie](create-ranking-strategies.md)
1. Configureer uw aanbiedingsschema om automatisch gebeurtenissen vast te leggen. [Meer informatie](schema-requirement.md)
1. Wijs het AI-model toe aan een plaatsing in een besluit om in aanmerking komende aanbiedingen te classificeren. [Meer informatie](../offer-activities/configure-offer-selection.md)
