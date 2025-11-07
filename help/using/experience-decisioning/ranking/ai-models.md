---
product: experience platform
solution: Experience Platform
title: Aan de slag met AI-modellen
description: Meer informatie over AI-modellen waarmee aanbiedingen kunnen worden beoordeeld
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 07679823-2288-4528-b09a-12fd76a69482
source-git-commit: 18a1020971dc6a1101e4e35c1523d004f3fd4188
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 3%

---

# Aan de slag met AI-modellen {#ai-models}

Met [!DNL Journey Optimizer] kunt u een getraind modelsysteem gebruiken dat voor een bepaald profiel wordt weergegeven.

Deze eigenschap laat u toe om verschillende **modellen van AI** tot stand te brengen die op uw bedrijfsdoelstellingen worden gebaseerd. Gebruikend deze verschillende op doel-gebaseerde strategieën in een besluit, zal het opgeleide modelsysteem u helpen begrijpen hoe de verschillende AI modellen uw doelstellingen beïnvloeden.

<!--For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given decision policy?, rather than taking into account the offers' priority scores or a [ranking formula](create-ranking-formulas.md).

>[!IMPORTANT]
>
>For now, ranking models are not supported in Journey Optimizer authored channels.-->

## AI-modeltypen {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_type"
>title="Het modeltype kiezen"
>abstract="Selecteer het type van AI model u wilt tot stand brengen: **auto-optimalisering** optimaliseert aanbiedingen die op het verleden aanbiedingsprestaties worden gebaseerd, terwijl **Gepersonaliseerde optimalisering** optimaliseert en verpersoonlijkt aanbiedingen die op publiek worden gebaseerd en prestaties aanbieden."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Een AI-model maken"

Er zijn twee typen AI-modellen beschikbaar in [!DNL Journey Optimizer] :

* **auto-optimalisatiemodellen** streven om aanbiedingen te dienen die het rendement (KPIs) maximaliseren dat door bedrijfscliënten wordt geplaatst. Deze KPI’s kunnen de vorm aannemen van omrekeningskoersen, inkomsten, enz. Op dit punt, richt de auto-optimalisering zich op optimaliserend aanbiedingskliks met aanbiedingsomzetting als ons doel. Automatisch optimaliseren is niet-gepersonaliseerd en optimaliseert op basis van &#39;algemene&#39; prestaties van de aanbiedingen. [Meer informatie](auto-optimization-model.md)

* **Gepersonaliseerde optimalisatiemodellen** staan u toe om bedrijfsdoelstellingen te bepalen en klantengegevens te gebruiken om zaken-georiënteerde modellen op te leiden om gepersonaliseerde aanbiedingen te dienen en KPIs te maximaliseren. [Meer informatie](personalized-optimization-model.md)

## Een AI-model maken {#create-ai-model}

De belangrijkste stappen om AI-modellen te kunnen maken en gebruiken zijn:

1. Maak een gegevensset waarin conversie- en impliciete gebeurtenissen worden verzameld. [Meer informatie](../data-collection/create-dataset.md)

1. Maak een AI-model dat gebeurtenissen van de dataset gebruikt om aanbiedingen te rangschikken. [Meer informatie](create-ai-models.md)

1. Configureer uw aanbiedingsschema om automatisch gebeurtenissen vast te leggen. [Meer informatie](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Het rangschikken modellen vereisen terugkoppelt gebeurtenissen die binnen als ervaringsgebeurtenissen worden verzonden om worden verzameld. [&#x200B; Leer meer over de inzameling van beslissingsgegevens &#x200B;](../data-collection/data-collection.md)

1. Wijs het AI-model toe aan een selectiestrategie om in aanmerking komende aanbiedingen te classificeren. [Meer informatie](../selection-strategies.md#select-ranking-method)
