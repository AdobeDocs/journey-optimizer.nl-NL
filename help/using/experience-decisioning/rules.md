---
title: Besluitvormingsregels
description: Leer hoe u met beslissingsregels werkt
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 29228a17176421ccf29598d6ebba815b800db7a2
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 1%

---

# Besluitvormingsregels {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Beslissingsregels maken"
>abstract="Met beslissingsregels kunt u het publiek voor beslissingsitems definiëren door beperkingen toe te passen, rechtstreeks op het niveau van de beslissingsitems of binnen een specifieke selectiestrategie. Hierdoor kunt u precies bepalen welke items aan wie moeten worden gepresenteerd."

>[!BEGINSHADEBOX &quot;Wat u vindt in deze documentatiehandleiding&quot;]

* [Aan de slag met Experience Decisition](gs-experience-decisioning.md)
* Je beslissingsobjecten beheren: [De itemcatalogus configureren](catalogs.md) - [Beslissingsitems maken](items.md) - [Objectverzamelingen beheren](collections.md)
* Selectie van items configureren: **[Beslissingsregels maken](rules.md)** - [Classificatiemethoden maken](ranking.md)
* [Selectiestrategieën maken](selection-strategies.md)
* [Beslissingsbeleid maken](create-decision.md)

>[!ENDSHADEBOX]

Met beslissingsregels kunt u het publiek voor beslissingsitems definiëren door beperkingen toe te passen, rechtstreeks op het niveau van de beslissingsitems of binnen een specifieke selectiestrategie. Hierdoor kunt u precies bepalen welke items aan wie moeten worden gepresenteerd.

Laten we bijvoorbeeld een scenario overwegen waarin u beslissingsitems hebt die Yoga-gerelateerde producten bevatten die zijn ontworpen voor vrouwen. Met beslissingsregels kunt u aangeven dat deze items alleen mogen worden weergegeven in profielen waarvan het geslacht &quot;Vrouwelijk&quot; is en die in &#39;Yoga&#39; een &#39;Belangenpunt&#39; hebben aangegeven.

>[!NOTE]
>
>Naast de besluitvormingsregels op het niveau van de item- en selectiestrategie kunt u ook het doelpubliek op campagnereniveau definiëren. [Meer informatie](../campaigns/create-campaign.md#audience)

De lijst met besluitvormingsregels is toegankelijk in het **[!UICONTROL Configuration]** / **[!UICONTROL Decisions rules]** -menu.

![](assets/decision-rules-list.png)

## Een beslissingsregel maken {#create}

Voer de volgende stappen uit om een beslissingsregel te maken:

1. Navigeren naar **[!UICONTROL Configuration]** / **[!UICONTROL Decision rules]** klik vervolgens op **[!UICONTROL Create rule]** knop.

1. Het scherm van de besluitvormingsregels opent. Geef de regel een naam en geef een beschrijving op.

1. Bouw de beslissingsregel aan uw behoeften gebruikend de Bouwer van het Segment van Adobe Experience Platform. Hiertoe kunt u verschillende gegevensbronnen gebruiken, zoals profielkenmerken, soorten publiek of contextgegevens die uit Adobe Experience Platform afkomstig zijn. [Leer hoe u contextgegevens kunt gebruiken in beslissingsregels](#context-data)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >De opsteller van het Segment die wordt verstrekt om besluitvormingsregels tot stand te brengen stelt wat specifieke kenmerken in vergelijking met die gebruikt met de dienst van de Segmentatie van Adobe Experience Platform.  Nochtans, is het globale proces dat in de documentatie wordt beschreven nog geldig om besluitvormingsregels te bouwen. [Leer hoe te om segmentdefinities te bouwen](../audience/creating-a-segment-definition.md)

1. Terwijl u nieuwe velden toevoegt en configureert in de werkruimte, worden de **[!UICONTROL Audience properties]** wordt informatie weergegeven over de geschatte profielen die bij het publiek horen. Klikken **[!UICONTROL Refresh estimate]** gegevens bijwerken.

   >[!NOTE]
   >
   >Profielramingen zijn niet beschikbaar wanneer regelparameters gegevens bevatten die niet in het profiel staan, zoals contextgegevens.

1. Als uw beslissingsregel gereed is, klikt u op **[!UICONTROL Save]**. De gemaakte regel wordt in de lijst weergegeven en kan worden gebruikt in besluitvormingselementen en selectiestrategieën om de presentatie van beslissingsitems in profielen te regelen.

## Gebruik van contextgegevens in besluitvormingsregels {#context-data}

Met het scherm Experience Decisioning Rule creation kunt u alle beschikbare informatie in Adobe Experience Platform gebruiken om beslissingsregels te maken. U kunt bijvoorbeeld een beslissingsregel ontwerpen waarvoor het huidige weer ≥ 80 graden moet zijn.

Hiervoor moet u eerst de gegevens definiëren die u beschikbaar wilt maken in Experience Decisioning. Als deze gegevens eenmaal zijn uitgevoerd, worden ze naadloos geïntegreerd in de weergave Experience Decisioning in de **[!UICONTROL Context Data]** beschikbaar bij het maken van een beslissingsregel.

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
