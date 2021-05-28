---
title: Informatie over Adobe Experience Platform-segmenten
description: Leer hoe u een Adobe Experience Platform-segment configureert
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Informatie over Adobe Experience Platform-segmenten {#about-segments}

![](../assets/do-not-localize/badge.png)

Met Journey Optimizer kunt u Adobe Experience Platform-segmenten rechtstreeks vanuit het menu **[!UICONTROL Segments]** maken met behulp van realtime klantprofielgegevens en deze gebruiken voor uw reizen.

Merk op dat de segmenten ook van de dienst van de Segmentatie zelf kunnen worden tot stand gebracht. Meer informatie vindt u in de documentatie [Adobe Experience Platform Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

U kunt segmenten in reizen op verschillende manieren benutten:

* Gebruik een **Leessegment** orchestratie activiteit om alle individuen die tot het gespecificeerde segment behoren de reis te maken. De berichten inbegrepen in uw reis worden verzonden naar de individuen die tot het segment behoren. Laten we zeggen dat je een &quot;zilveren klant&quot;-segment hebt. Met deze activiteit, kunt u alle zilveren klanten een reis maken en hen een reeks gepersonaliseerde berichten verzenden.

   Raadpleeg [deze sectie](../building-journeys/read-segment.md#configuring-segment-trigger-activity) voor meer informatie over het gebruik van de **[!UICONTROL Read segment]**-activiteit.

* Met de **Segmentkwalificatie**-gebeurtenisactiviteit kunnen personen een reis maken of vooruit gaan op basis van de toegang en het afsluiten van Adobe Experience Platform-segmenten. U kunt bijvoorbeeld alle nieuwe zilverklanten een reis laten maken en hun berichten sturen. Raadpleeg [deze sectie](../building-journeys/segment-qualification-events.md) voor meer informatie over het gebruik van deze activiteit.

* Bouw **complexe voorwaarden** in uw reizen gebruikend de eenvoudige of geavanceerde uitdrukkingsredacteur. Meer informatie vindt u in [deze sectie](../building-journeys/condition-activity.md#using-a-segment).
