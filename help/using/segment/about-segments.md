---
title: Informatie over Adobe Experience Platform-segmenten
description: Leer hoe u een Adobe Experience Platform-segment configureert
feature: Journeys
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: 9e93a97ff793fec9fdf4aecd645f1df95b65b31a
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Informatie over Adobe Experience Platform-segmenten {#about-segments}

[!DNL Journey Optimizer]  kunt u Adobe Experience Platform-segmenten rechtstreeks vanuit het  **[!UICONTROL Segments]** menu maken met behulp van realtime klantprofielgegevens en deze gebruiken voor uw reizen.

Merk op dat de segmenten ook van de dienst van de Segmentatie zelf kunnen worden tot stand gebracht. Meer informatie vindt u in de documentatie [Adobe Experience Platform Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

U kunt segmenten in reizen op verschillende manieren benutten:

* Gebruik een **Leessegment** orchestratie activiteit om alle individuen die tot het gespecificeerde segment behoren de reis te maken. De berichten inbegrepen in uw reis worden verzonden naar de individuen die tot het segment behoren. Laten we zeggen dat je een &quot;zilveren klant&quot;-segment hebt. Met deze activiteit, kunt u alle zilveren klanten een reis maken en hen een reeks gepersonaliseerde berichten verzenden.

   Raadpleeg [deze sectie](../building-journeys/read-segment.md#configuring-segment-trigger-activity) voor meer informatie over het gebruik van de **[!UICONTROL Read segment]**-activiteit.

* Met de **Segmentkwalificatie**-gebeurtenisactiviteit kunnen personen een reis maken of vooruit gaan op basis van de toegang en het afsluiten van Adobe Experience Platform-segmenten. U kunt bijvoorbeeld alle nieuwe zilverklanten een reis laten maken en hun berichten sturen. Raadpleeg [deze sectie](../building-journeys/segment-qualification-events.md) voor meer informatie over het gebruik van deze activiteit.

* Bouw **complexe voorwaarden** in uw reizen gebruikend de eenvoudige of geavanceerde uitdrukkingsredacteur. Meer informatie vindt u in [deze sectie](../building-journeys/condition-activity.md#using-a-segment).

## Evaluatiemethode in Adobe Journey Optimizer {#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer wordt het publiek op basis van segmentdefinities op basis van een van de volgende evaluatiemethoden gegenereerd:

* Streaming segmentering — de publiekslijst voor het segment wordt bijgewerkt in real-time terwijl nieuwe gegevens in het systeem stromen.
* Batchsegmentatie — de publiekslijst voor het segment wordt per uur bijgewerkt op basis van gegevens die in het afgelopen uur zijn aangekomen.

De bepaling tussen partijsegmentatie en het stromen segmentatie wordt gemaakt door het systeem voor elke segmentdefinitie, die op de ingewikkeldheid en de kosten wordt gebaseerd om de segmentregel te evalueren.

U kunt de evaluatiemethode voor elk segment in **[!UICONTROL Evaluation method]** kolom van de segmentlijst bekijken.

Nadat u een segment hebt gedefinieerd, worden profielen toegevoegd aan het publiek wanneer deze in aanmerking komen.

Het ondersteunen van het publiek op basis van eerdere gegevens kan 24 uur in beslag nemen. Nadat het publiek is teruggevuld, wordt het publiek voortdurend bijgewerkt en is altijd klaar om zich te richten.
