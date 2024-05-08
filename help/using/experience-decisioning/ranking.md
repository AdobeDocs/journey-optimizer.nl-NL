---
title: Rangschikkingsmethoden
description: Leer hoe u met waarderingsmethoden werkt
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
badge: label="Beperkte beschikbaarheid"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 1%

---

# Rangschikkingsmethoden {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Rangschikkingsformules maken"
>abstract="Met indelingen kunt u regels definiëren die bepalen welk item als eerste moet worden weergegeven, in plaats van rekening te houden met de prioriteitsscores van het item. Nadat u een waarderingsmethode hebt gemaakt, kunt u deze toewijzen aan een selectiestrategie om te bepalen welke items als eerste moeten worden geselecteerd."

Met behulp van rankeringsmethoden kunt u items voor een bepaald profiel rangschikken. Nadat u een waarderingsmethode hebt gemaakt, kunt u deze toewijzen aan een selectiestrategie om te bepalen welke items als eerste moeten worden geselecteerd.

Er zijn twee typen waarderingsmethoden beschikbaar:

* **Formulas** kunt u regels definiëren die bepalen welk item als eerste moet worden gepresenteerd, in plaats van rekening te houden met de prioriteitsscores van het item.

* **AI-modellen** kunt u getrainde modelsystemen gebruiken die meerdere gegevenspunten gebruiken om te bepalen welk item als eerste moet worden gepresenteerd.

## Classificatiemethoden maken {#create}

Ga als volgt te werk om een waarderingsmethode te maken:

1. Ga naar de **[!UICONTROL Strategy setup]** selecteert u vervolgens het menu **[!UICONTROL Formulas]** of **[!UICONTROL AI models]** afhankelijk van het type rangschikking dat u wilt gebruiken.

1. Klik op de knop **[!UICONTROL Create formula]** of **[!UICONTROL Create AI model]** rechtsboven in het scherm.

   ![](assets/ranking-create.png)

1. Configureer de formule of het AI-model naar wens en sla het op.

   Gedetailleerde informatie over het maken van rangschikkingsformules en AI-modellen is beschikbaar in de documentatie van het besluitvormingsbeheer:

   * [Beoordelingsformule](../offers/ranking/create-ranking-formulas.md)
   * [AI-modellen](../offers/ranking/ai-models.md)


## Kenmerken van besluitvormingsposten in formules gebruiken {#items}

De rangschikkingsformules worden uitgedrukt in **PQL-syntaxis** en kan verschillende kenmerken gebruiken, zoals profielkenmerken, [contextgegevens](context-data.md) en kenmerken met betrekking tot uw beslissingsitems.

Om attributen met betrekking tot uw beslissingspunten in formules te hefboomwerking, zorg ervoor u de syntaxis hieronder in de code van uw rangschikkende formule volgt. Breid elke sectie voor meer informatie uit:

+++Standaardeigenschappen van besluitvormingsposten voor hefboomwerking

![](assets/formula-attribute.png)

+++

+++Aangepaste kenmerken van besluitvormingspunten voor hefboomwerking

![](assets/formula-attribute-custom.png)

+++
