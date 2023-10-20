---
title: Beslissingsregels
description: Leer hoe u met beslissingsregels werkt
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: f92e3882d3b5e515e672a4af8e787813d4d939ce
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 4%

---

# Beslissingsregels {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Beslissingsregels maken"
>abstract="Met beslissingsregels kunt u het publiek voor beslissingsitems definiëren door beperkingen toe te passen, rechtstreeks op het niveau van de beslissingsitems of binnen een specifieke selectiestrategie. Hierdoor kunt u precies bepalen welke items aan wie moeten worden gepresenteerd."

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Aan de slag met Experience Decisition](gs-experience-decisioning.md)
* Je beslissingsobjecten beheren
   * [De itemcatalogus configureren](catalogs.md)
   * [Beslissingsitems maken](items.md)
   * [Objectverzamelingen beheren](collections.md)
* Selectie van items configureren
   * **[Beslissingsregels maken](rules.md)**
   * [Classificatiemethoden maken](ranking.md)
* [Selectiestrategieën maken](selection-strategies.md)
* [Beslissingsbeleid maken](create-decision.md)

>[!ENDSHADEBOX]

Met beslissingsregels kunt u het publiek voor beslissingsitems definiëren door beperkingen toe te passen, rechtstreeks op het niveau van de beslissingsitems of binnen een specifieke selectiestrategie. Hierdoor kunt u precies bepalen welke items aan wie moeten worden gepresenteerd.

Laten we bijvoorbeeld een scenario overwegen waarin u beslissingsitems hebt die Yoga-gerelateerde producten bevatten die zijn ontworpen voor vrouwen. Met de besluitvormingsregels kunt u zeggen dat deze items alleen mogen worden weergegeven aan profielen waarvan het geslacht &quot;Vrouwelijk&quot; is en die in &#39;Yoga&#39; een &#39;belangenpunt&#39; hebben aangegeven.

>[!NOTE]
>
>Naast de besluitvormingsregels op het niveau van de item- en selectiestrategie kunt u ook het doelpubliek op campagnereniveau definiëren. [Meer informatie](../campaigns/create-campaign.md#audience)


De lijst met besluitvormingsregels is toegankelijk in het **[!UICONTROL Configuration]** / **[!UICONTROL Decisions rules]** -menu.

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>Momenteel worden de besluitvormingsregels beheerd met Journey Optimizer **Beslissingsbeheer** -menu. Dientengevolge, **[!UICONTROL Decision rules]** De lijst in Ervaring Beslissing omvat regels die van beide Journey Optimizer worden gecreeerd **[!UICONTROL Decision Management]** of **[!UICONTROL Experience Decisioning]** menu&#39;s.

Ga als volgt te werk om een regel te maken:

1. Ga naar **[!UICONTROL Configuration]** / **[!UICONTROL Decision rules]**.
1. Journey Optimizer-gebruikersinterface voor beslissingsbeheer wordt in het centrale gebied weergegeven. Voer de stappen uit die in het dialoogvenster [Beslissingsbeheersdocumentatie](../offers/offer-library/creating-decision-rules.md) om uw regel te bouwen die op uw behoeften wordt gebaseerd.

1. Nadat de regel is gemaakt, wordt deze weergegeven in de lijst en kan deze worden gebruikt in besluitvormings- en selectiestrategieën om de presentatie van beslissingsitems in profielen te regelen.
