---
title: Aangepaste handelingen gebruiken
description: Leer hoe u aangepaste handelingen kunt gebruiken
feature: Actions
topic: Content Management
role: User
level: Intermediate
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 18%

---

# Aangepaste handelingen gebruiken {#use-custom-actions}

Met aangepaste acties kunt u een verbinding met een extern systeem configureren voor het verzenden van berichten of API-aanroepen. Een actie kan worden geconfigureerd met elke service van elke provider die door een REST-API met een payload in JSON-indeling kan worden aangeroepen.

## URL-configuratie

Het configuratievenster van het dialoogvenster **Aangepaste actie** De activiteit toont de URL configuratieparameters en de authentificatieparameters die voor de douaneactie worden gevormd. U kunt niet opstelling het statische deel van URL in de reis, maar in de globale configuratie van de douaneactie. [Meer informatie](../action/about-custom-action-configuration.md).

### Dynamisch pad

Als de URL een dynamisch pad bevat, geeft u het pad op in het dialoogvenster **[!UICONTROL Path]** veld.

Als u velden en onbewerkte teksttekenreeksen wilt samenvoegen, gebruikt u de tekenreeksfuncties of het plusteken (+) in de geavanceerde expressie-editor. Plaats normale teksttekenreeksen tussen enkele aanhalingstekens (&#39;) of tussen dubbele aanhalingstekens (&#39;). [Meer informatie](expression/expressionadvanced.md).

In deze tabel ziet u een voorbeeld van configuratie:

| Veld | Waarde |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Pad | `The id of marketingCampaign + '/messages'` |

De samengevoegde URL heeft de volgende vorm:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](assets/journey-custom-action-url.png)

### Kopteksten

De **[!UICONTROL URL Configuration]** in deze sectie worden de dynamische koptekstvelden weergegeven, maar niet de constante koptekstvelden. Dynamische headervelden zijn HTTP-headervelden waarvan de waarde is geconfigureerd als een variabele. [Meer informatie](../action/about-custom-action-configuration.md).

Geef zo nodig de waarde van dynamische koptekstvelden op:

1. Selecteer de aangepaste handeling tijdens de rit.
1. Klik in het configuratievenster op het potloodpictogram naast het koptekstveld in het dialoogvenster **[!UICONTROL URL Configuration]** sectie.

   ![](assets/journey-dynamicheaderfield.png)

1. Selecteer een veld en klik op **[!UICONTROL OK]**.

## Handelingsparameters

In de **[!UICONTROL Action parameters]** sectie, zult u de berichtparameters zien die als worden bepaald _&quot;Variabele&quot;_. Voor deze parameters kunt u definiëren waar deze informatie moet worden opgehaald (voorbeeld: gebeurtenissen, gegevensbronnen), geeft u waarden handmatig door of gebruikt u de geavanceerde expressie-editor voor gevallen van geavanceerd gebruik. Gevallen van geavanceerd gebruik kunnen gegevensmanipulatie en ander functiegebruik zijn. Zie [Adobe Journey Orchestration-documentatie](expression/expressionadvanced.md).

**Verwante onderwerpen**

[Een actie configureren](../action/about-custom-action-configuration.md)