---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform-segmenten
description: Leer hoe u een Adobe Experience Platform-segment configureert
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 6c255d66fb89ba756add062d8a4315dd622fd8e7
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 1%

---

# Aan de slag met Adobe Experience Platform-segmenten {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Segment"
>abstract="Door gebruik te maken van realtime klantprofielgegevens kunt u in Adobe Experience Platform eenvoudig doelsegmenten maken die de unieke gedragingen en voorkeuren van uw klanten vastleggen."

[!DNL Journey Optimizer]  kunt u Adobe Experience Platform-segmenten rechtstreeks vanuit het dialoogvenster **[!UICONTROL Segments]** en gebruikt u deze voor reizen of campagnes.

Bovendien, kunnen de segmenten ook van de dienst van de Segmentatie zelf worden gecreeerd. Meer informatie in het dialoogvenster [Adobe Experience Platform Segmentation Service-documentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## Segmenten gebruiken in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

U kunt segmenten benutten in **[!DNL Journey Optimizer]** op verschillende manieren:

* Een segment kiezen als de **publiek voor een campagne**, waarbij het bericht wordt verzonden naar alle personen die tot het geselecteerde segment behoren. [Leer hoe u het publiek van een campagne definieert](../campaigns/create-campaign.md#define-the-audience-audience).

* Een **Segment lezen** Orchestratie-activiteit op een reis om ervoor te zorgen dat alle individuen in het segment de reis binnenkomen en de berichten ontvangen inbegrepen in uw reis.

   Laten we zeggen dat je een &quot;zilveren klant&quot;-segment hebt. Met deze activiteit, kunt u alle zilveren klanten een reis maken en hen een reeks gepersonaliseerde berichten verzenden. [Leer hoe te om een Gelezen segmentactiviteit te vormen](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Gebruik de **Segmentkwalificatie** gebeurtenisactiviteit op een reis om ervoor te zorgen dat individuen de reis binnenkomen of zich voortbewegen op basis van de toegang tot en de uitgangen van Adobe Experience Platform-segmenten.

   U kunt bijvoorbeeld alle nieuwe zilverklanten een reis laten maken en hun berichten sturen. Raadpleeg voor meer informatie over het gebruik van deze activiteit [Leer hoe te om een de kwalificatieactiviteit van het Segment te vormen](../building-journeys/segment-qualification-events.md).

* Gebruik de **Voorwaarde** activiteit op een reis om voorwaarden te creëren die op segmentlidmaatschap worden gebaseerd. [Leer hoe u segmenten in voorwaarden kunt gebruiken](../building-journeys/condition-activity.md#using-a-segment).

## Methoden voor de evaluatie van het publiek{#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer worden publiek op basis van segmentdefinities gegenereerd met behulp van een van de volgende twee evaluatiemethoden:

* **Streaming segmentering**: De publiekslijst voor het segment wordt bijgewerkt in real time aangezien de nieuwe gegevens in het systeem stromen.

   Streaming segmentatie is een doorlopend proces voor gegevensselectie dat uw segmenten bijwerkt als reactie op gebruikersactiviteit. Nadat een segment is gemaakt en opgeslagen, wordt de segmentdefinitie toegepast op inkomende gegevens naar Journey Optimizer. Dit betekent dat personen aan het segment worden toegevoegd of uit het segment worden verwijderd wanneer hun profielgegevens veranderen, zodat het doelpubliek altijd relevant is.

* **Batchsegmentatie**: De publiekslijst voor het segment wordt om de 24 uur geëvalueerd.

   De segmentatie van de partij is een alternatief aan het stromen segmentatie die alle profielgegevens in één keer door segmentdefinities verwerkt. Zo maakt u een momentopname van het publiek die u kunt opslaan en exporteren voor gebruik. Nochtans, in tegenstelling tot het stromen segmentatie, werkt de partijsegmentatie niet onophoudelijk de publiekslijst in real time bij, en de nieuwe gegevens die binnen na het partijproces komen zullen niet in het segment tot het volgende partijproces worden weerspiegeld.&quot;

De bepaling tussen partijsegmentatie en het stromen segmentatie wordt gemaakt door het systeem voor elke segmentdefinitie, die op de ingewikkeldheid en de kosten wordt gebaseerd om de segmentregel te evalueren. U kunt de evaluatiemethode voor elk segment in bekijken **[!UICONTROL Evaluation method]** kolom van de segmentlijst.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Als de **[!UICONTROL Evaluation method]** de kolom niet toont, moet u het toevoegen gebruikend configuratieknoop op de hoogste recht van de lijst.

Nadat u een segment hebt gedefinieerd, worden profielen toegevoegd aan het publiek wanneer deze in aanmerking komen.

Het ondersteunen van het publiek op basis van eerdere gegevens kan 24 uur in beslag nemen. Nadat het publiek is teruggevuld, wordt het publiek voortdurend bijgewerkt en is altijd klaar om zich te richten.
