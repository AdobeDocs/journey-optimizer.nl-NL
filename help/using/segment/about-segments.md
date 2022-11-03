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
source-git-commit: df16e6be53629ef529b765c9e36a293234244867
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Aan de slag met Adobe Experience Platform-segmenten {#about-segments}

[!DNL Journey Optimizer]  kunt u Adobe Experience Platform-segmenten rechtstreeks vanuit het dialoogvenster **[!UICONTROL Segments]** en ze te gebruiken voor uw reizen.

Merk op dat de segmenten ook van de dienst van de Segmentatie zelf kunnen worden tot stand gebracht. Meer informatie in het dialoogvenster [Adobe Experience Platform Segmentation Service-documentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

U kunt segmenten in reizen op verschillende manieren benutten:

* Een **Segment lezen** orkestwerkzaamheden om ervoor te zorgen dat alle personen die tot het gespecificeerde segment behoren, de reis betreden. De berichten inbegrepen in uw reis worden verzonden naar de individuen die tot het segment behoren. Laten we zeggen dat je een &quot;zilveren klant&quot;-segment hebt. Met deze activiteit, kunt u alle zilveren klanten een reis maken en hen een reeks gepersonaliseerde berichten verzenden.

   Voor meer informatie over het gebruik van de **[!UICONTROL Read segment]** activiteit, zie [deze sectie](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Gebruik de **Segmentkwalificatie** gebeurtenisactiviteiten om ervoor te zorgen dat individuen op reis gaan of vooruit gaan op basis van de toegang tot en de uitgangen van Adobe Experience Platform-segmenten. U kunt bijvoorbeeld alle nieuwe zilverklanten een reis laten maken en hun berichten sturen. Raadpleeg voor meer informatie over het gebruik van deze activiteit [deze sectie](../building-journeys/segment-qualification-events.md).

* Opbouwen **complexe omstandigheden** op reis met de eenvoudige of geavanceerde expressieeditor. Meer informatie in [deze sectie](../building-journeys/condition-activity.md#using-a-segment).

## Evaluatiemethode in Adobe Journey Optimizer {#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer wordt het publiek op basis van segmentdefinities op basis van een van de volgende evaluatiemethoden gegenereerd:

* Streaming segmentatie: de publiekslijst voor het segment wordt in real-time bijgewerkt terwijl nieuwe gegevens in het systeem stromen. Streaming segmentatie is een doorlopend proces voor gegevensselectie dat uw segmenten bijwerkt als reactie op gebruikersactiviteit. Nadat een segment is gemaakt en opgeslagen, wordt de segmentdefinitie toegepast op inkomende gegevens naar Journey Optimizer. Segmenttoevoegingen en verwijderingen worden regelmatig verwerkt, zodat het doelpubliek relevant blijft.

* De segmentatie van de partij - de publiekslijst voor het segment wordt geëvalueerd om de 24 uur. Als alternatief voor een lopend proces van de gegevensselectie, verplaatst de partijsegmentatie alle profielgegevens in één keer door segmentdefinities om het overeenkomstige publiek te veroorzaken. Zodra gecreeerd, wordt dit segment bewaard en opgeslagen zodat u het voor gebruik kunt uitvoeren.

De bepaling tussen partijsegmentatie en het stromen segmentatie wordt gemaakt door het systeem voor elke segmentdefinitie, die op de ingewikkeldheid en de kosten wordt gebaseerd om de segmentregel te evalueren.

U kunt de evaluatiemethode voor elk segment in bekijken **[!UICONTROL Evaluation method]** kolom van de segmentlijst.

Nadat u een segment hebt gedefinieerd, worden profielen toegevoegd aan het publiek wanneer deze in aanmerking komen.

Het ondersteunen van het publiek op basis van eerdere gegevens kan 24 uur in beslag nemen. Nadat het publiek is teruggevuld, wordt het publiek voortdurend bijgewerkt en is altijd klaar om zich te richten.
