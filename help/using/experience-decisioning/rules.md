---
title: Besluitvormingsregels
description: Leer hoe u met beslissingsregels werkt
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 58389860e5e0b07f32dd62b95a508e80579aaa73
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 1%

---

# Besluitvormingsregels {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Beslissingsregels maken"
>abstract="Met beslissingsregels kunt u het publiek voor beslissingsitems definiëren door beperkingen toe te passen, rechtstreeks op het niveau van de beslissingsitems of binnen een specifieke selectiestrategie. Hierdoor kunt u precies bepalen welke items aan wie moeten worden gepresenteerd.<br/><br/> selecteer **[!UICONTROL Create rule with dataset]** om de gegevens van Adobe Experience Platform in besluitvormingsregels te gebruiken. Op deze manier kunt u beleenbaarheidscriteria definiëren op basis van dynamische, externe kenmerken, zodat de beslissingsitems alleen worden weergegeven wanneer dat relevant is."

## Over beslissingsregels {#about}

Met beslissingsregels kunt u het publiek voor beslissingsitems definiëren door beperkingen toe te passen, rechtstreeks op het niveau van de beslissingsitems of binnen een specifieke selectiestrategie. Hierdoor kunt u precies bepalen welke items aan wie moeten worden gepresenteerd.

Laten we bijvoorbeeld een scenario overwegen waarin u beslissingsitems hebt die Yoga-gerelateerde producten bevatten die zijn ontworpen voor vrouwen. Met beslissingsregels kunt u aangeven dat deze items alleen mogen worden weergegeven in profielen waarvan het geslacht &quot;Vrouwelijk&quot; is en die in &#39;Yoga&#39; een &#39;Belangenpunt&#39; hebben aangegeven.

>[!NOTE]
>
>Naast de besluitvormingsregels op het niveau van de item- en selectiestrategie kunt u ook het doelpubliek op campagnereniveau definiëren. [Meer informatie](../campaigns/create-campaign.md#audience)

De lijst met beslissingsregels is toegankelijk in het menu **[!UICONTROL Strategy setup]** .

![](assets/decision-rules-list.png)

## Een beslissingsregel maken {#create}

Voer de volgende stappen uit om een beslissingsregel te maken:

1. Navigeer naar de knop **[!UICONTROL Strategy setup]** / **[!UICONTROL Decision rules]** en klik vervolgens op de knop **[!UICONTROL Create rule]** .

   >[!NOTE]
   >
   >U kunt gegevens van Adobe Experience Platform ook gebruiken om uw besluitvormingslogica met externe gegevens te verrijken. Dit is vooral nuttig voor attributen die vaak veranderen, zoals productbeschikbaarheid, of prijs in real time. Deze mogelijkheid is momenteel beschikbaar voor alle klanten als een openbare bètaversie. Neem contact op met uw accountvertegenwoordiger als u toegang wilt. [&#x200B; Leer hoe te om de gegevens van Adobe Experience Platform voor besluit te gebruiken &#x200B;](../experience-decisioning/aep-data-exd.md)

1. Het scherm van de besluitvormingsregels opent. Geef de regel een naam en geef een beschrijving op.

1. Bouw de beslissingsregel aan uw behoeften gebruikend de Bouwer van het Segment van Adobe Experience Platform. Hiervoor kunt u verschillende gegevensbronnen gebruiken, zoals:
   * Eigenschappen van profiel- en beslissingsitems,
   * Soorten publiek
   * Contextgegevens afkomstig van Adobe Experience Platform. [&#x200B; Leer hoe te hefboomwerking contextgegevens &#x200B;](context-data.md)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >De opsteller van het Segment die wordt verstrekt om besluitvormingsregels tot stand te brengen stelt wat specifieke kenmerken in vergelijking met die gebruikt met de dienst van de Segmentatie van Adobe Experience Platform. Nochtans, is het globale proces dat in de documentatie wordt beschreven nog geldig om besluitvormingsregels te bouwen. [&#x200B; leer hoe te om segmentdefinities te bouwen &#x200B;](../audience/creating-a-segment-definition.md)

1. Terwijl u nieuwe velden toevoegt en configureert in de werkruimte, wordt in het deelvenster **[!UICONTROL Audience properties]** informatie weergegeven over de geschatte profielen die bij het publiek horen. Klik op **[!UICONTROL Refresh estimate]** om gegevens bij te werken.

   >[!NOTE]
   >
   >Profielramingen zijn niet beschikbaar wanneer regelparameters gegevens bevatten die niet in het profiel staan, zoals contextgegevens.

1. Klik op **[!UICONTROL Save]** als de beslissingsregel gereed is. De gemaakte regel wordt in de lijst weergegeven en kan worden gebruikt in besluitvormingselementen en selectiestrategieën om de presentatie van beslissingsitems in profielen te regelen.

   >[!NOTE]
   >
   >De nestdiepte in een toelatingsregel is beperkt tot 30 niveaus. Dit wordt gemeten door de `)` haakjes sluiten in de PQL-tekenreeks te tellen. Een regeltekenreeks kan maximaal 15 kB groot zijn voor UTF-8-gecodeerde tekens. Dit komt overeen met 15.000 ASCII-tekens (1 byte elk) of 3.750-7.500 niet-ASCII-tekens (2-4 bytes elk). [&#x200B; leer meer over het Beslissen van gidsen &amp; beperkingen &#x200B;](gs-experience-decisioning.md#guardrails)
