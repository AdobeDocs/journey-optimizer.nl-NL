---
title: Gebruik contextgegevens in Experience Decisition
description: Leer hoe u contextgegevens kunt gebruiken in Experience Decisition
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Beperkte beschikbaarheid"
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Gebruik contextgegevens in Experience Decisition {#context}

Met Experience Decisioning kunt u alle beschikbare informatie in Adobe Experience Platform gebruiken om verschillende handelingen uit te voeren, zoals het maken van [beslissingsregels](rules.md) of [waarderingsformules](ranking.md). U kunt bijvoorbeeld een beslissingsregel ontwerpen waarvoor het huidige weer 80 graden moet zijn op het moment dat het beslissingsverzoek wordt gedaan.

>[!NOTE]
>
>Contextgegevens worden gedefinieerd in Adobe Experience Platform en worden verzonden op het moment dat een beslissing wordt gevraagd. Het omvat geen historische gegevens.

Als u contextgegevens wilt gebruiken, moet u eerst de gegevens definiëren die u beschikbaar wilt maken in Experience Definition. Als deze gegevens eenmaal zijn uitgevoerd, worden ze naadloos geïntegreerd in de weergave Experience Decisioning in de **[!UICONTROL Context Data]** beschikbaar bij het maken van een beslissingsregel. U kunt de gegevens ook gebruiken wanneer u een waarderingsformule bewerkt.

![](assets/decision-rules-context.png)

De stappen om Ervaring Beslissing met gegevens van Adobe Experience Platform te voeren zijn als volgt:

1. Een **Experience Event-schema**  in Adobe Experience Platform en de geassocieerde **gegevensset**. [Leer hoe u schema&#39;s maakt](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. Een nieuwe Adobe Experience Platform-gegevensstroom maken:

   1. Ga naar de **[!UICONTROL Datastreams]** en selecteert u **[!UICONTROL New Datastream]**.

   1. In de **[!UICONTROL Event Schema]** vervolgkeuzelijst, selecteert u het eerder gemaakte Experience Event-schema en klikt u op **[!UICONTROL Save]**.

      ![](assets/decision-rule-context-datastream.png)

   1. Klikken **[!UICONTROL Add service]** en selecteer &quot;Adobe Experience Platform&quot; als de service. In de **[!UICONTROL Event Dataset]** vervolgkeuzelijst, selecteert u de eerder gemaakte gebeurtenisdataset en schakelt u de **[!UICONTROL Adobe Journey Optimizer]** -optie.

      ![](assets/decision-rules-context-datastream-service.png)

Zodra de gegevensstroom wordt bewaard, wordt de geselecteerde informatie van de dataset automatisch opgehaald en in het Beslissen van de Ervaring geïntegreerd, die typisch binnen ongeveer 24 uren beschikbaar wordt.

Raadpleeg de volgende bronnen voor meer informatie over hoe u met Adobe Experience Platform kunt werken:

* [XDM-schema&#39;s (Experience Data Model)](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [Gegevenssets](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [Gegevensstromen](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
