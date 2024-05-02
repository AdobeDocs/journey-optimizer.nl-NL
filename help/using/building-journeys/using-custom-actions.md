---
solution: Journey Optimizer
product: journey optimizer
title: Aangepaste handelingen gebruiken
description: Leer hoe u aangepaste handelingen kunt gebruiken
feature: Journeys, Actions, Custom Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: actie, douane, API, reis, configuratie, de dienst
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 23%

---

# Aangepaste handelingen gebruiken {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Aangepaste acties"
>abstract="Met aangepaste acties kunt u een verbinding met een extern systeem configureren voor het verzenden van berichten of API-aanroepen. Een actie kan worden geconfigureerd met elke service van elke provider die door een REST-API met een payload in JSON-indeling kan worden aangeroepen."

Met aangepaste acties kunt u een verbinding met een extern systeem configureren voor het verzenden van berichten of API-aanroepen. Een actie kan worden geconfigureerd met elke service van elke provider die door een REST-API met een payload in JSON-indeling kan worden aangeroepen.

## Toestemming en gegevensbeheer {#privacy}

In Journey Optimizer kunt u beleid voor gegevensbeheer en toestemming toepassen op uw aangepaste acties om te voorkomen dat bepaalde velden worden geëxporteerd naar systemen van derden of om klanten uit te sluiten die niet hebben ingestemd met het ontvangen van e-mail, push- of SMS-berichten. Raadpleeg de volgende pagina&#39;s voor meer informatie:

* [Gegevensbeheer](../action/action-privacy.md).
* [Toestemming](../action/consent.md).

## URL-configuratie

Het configuratievenster van de **Aangepaste actie** De activiteit toont de URL configuratieparameters en de authentificatieparameters die voor de douaneactie worden gevormd. U kunt niet opstelling het statische deel van URL in de reis, maar in de globale configuratie van de douaneactie. [Meer informatie](../action/about-custom-action-configuration.md).

### Dynamisch pad

Als de URL een dynamisch pad bevat, geeft u het pad op in het dialoogvenster **[!UICONTROL Path]** veld.

Als u velden en onbewerkte teksttekenreeksen wilt samenvoegen, gebruikt u de tekenreeksfuncties of het plusteken (+) in de geavanceerde expressie-editor. Plaats normale teksttekenreeksen tussen enkele aanhalingstekens (&#39;) of tussen dubbele aanhalingstekens (&#39;). [Meer informatie](expression/expressionadvanced.md).

In deze tabel ziet u een voorbeeld van configuratie:

| Veld | Waarde |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Pad | `The _id + '/messages'` |

De samengevoegde URL heeft de volgende vorm:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;id>`/messages`

![](assets/journey-custom-action-url.png)

### Kopteksten en queryparameters {#headers}

De **[!UICONTROL URL Configuration]** in deze sectie worden de velden voor dynamische koptekst- en queryparameters weergegeven, maar niet de velden voor constante waarden. Dynamische kopbal en de gebieden van de vraagparameter worden bepaald als variabele in het scherm van de actieconfiguratie. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)

Als u de waarde van dynamische koptekst- en queryparametervelden wilt opgeven, klikt u in het veld of op het potloodpictogram en selecteert u het gewenste veld.

![](assets/journey-dynamicheaderfield.png)

## Handelingsparameters

In de **[!UICONTROL Action parameters]** sectie, zult u de berichtparameters zien die als worden bepaald _&quot;Variabele&quot;_. Voor deze parameters kunt u bepalen waar u deze informatie wilt ophalen (bijvoorbeeld: gebeurtenissen, gegevensbronnen), waarden handmatig doorgeven of de geavanceerde expressie-editor voor geavanceerde gebruiksgevallen gebruiken. Gevallen van geavanceerd gebruik kunnen gegevensmanipulatie en ander functiegebruik zijn. Zie dit [page](expression/expressionadvanced.md).

**Verwante onderwerpen**

[Een handeling configureren](../action/about-custom-action-configuration.md)
