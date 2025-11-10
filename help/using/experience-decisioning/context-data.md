---
title: De contextgegevens van de hefboomwerking in Beslissing
description: Leer hoe u contextgegevens kunt gebruiken in Beslissing
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: ddc4b681-020b-4433-b4b3-3791c41907c9
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# De contextgegevens van de hefboomwerking in Beslissing {#context}

Met Beslissing, kunt u hefboomwerking om het even welke informatie beschikbaar in Adobe Experience Platform om diverse acties uit te voeren zoals het creëren van [&#x200B; besluitvormingsregels &#x200B;](rules.md) of [&#x200B; het rangschikken formules &#x200B;](ranking/ranking.md).

U kunt bijvoorbeeld een beslissingsregel ontwerpen waarvoor het huidige weer 80 graden moet zijn op het moment dat het beslissingsverzoek wordt gedaan.

>[!NOTE]
>
>Contextgegevens worden gedefinieerd in Adobe Experience Platform en worden verzonden op het moment dat een beslissing wordt gevraagd. Het omvat geen historische gegevens.

Om contextgegevens te gebruiken, moet u eerst de gegevens bepalen u in Beslissing ter beschikking wilt stellen. Zodra gereed, integreren deze gegevens naadloos in Beslissing in het **[!UICONTROL Context Data]** lusje beschikbaar wanneer het creëren van een besluitvormingsregel. U kunt de gegevens ook gebruiken wanneer u een waarderingsformule bewerkt.

![](assets/decision-rules-context.png)

De stappen om Beslissing met de gegevens van Adobe Experience Platform te voeren zijn als volgt:

1. Creeer een **schema van de Gebeurtenis van de Ervaring** in Adobe Experience Platform en zijn bijbehorende **dataset**. [&#x200B; leer hoe te om schema&#39;s &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"} tot stand te brengen

1. Een nieuwe Adobe Experience Platform-gegevensstroom maken:

   1. Navigeer naar het menu **[!UICONTROL Datastreams]** en selecteer **[!UICONTROL New Datastream]** .

   1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Event Schema]** het eerder gemaakte Experience Event-schema en klik op **[!UICONTROL Save]** .

      ![](assets/decision-rule-context-datastream.png)

   1. Klik op **[!UICONTROL Add service]** en selecteer &quot;Adobe Experience Platform&quot; als service. Selecteer in de vervolgkeuzelijst **[!UICONTROL Event Dataset]** de eerder gemaakte gebeurtenisdataset en schakel de optie **[!UICONTROL Adobe Journey Optimizer]** in.

      ![](assets/decision-rules-context-datastream-service.png)

Zodra de gegevensstroom wordt bewaard, wordt de geselecteerde informatie van de dataset automatisch opgehaald en in Beslissing geïntegreerd, die typisch binnen ongeveer 24 uren beschikbaar wordt.

Raadpleeg de volgende bronnen voor meer informatie over hoe u met Adobe Experience Platform kunt werken:

* [&#x200B; schema&#39;s van de Gegevens van de Ervaring Model (XDM) &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [&#x200B; Datasets &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [&#x200B; Datastreams &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
