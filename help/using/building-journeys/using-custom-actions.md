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
version: Journey Orchestration
source-git-commit: 221368c7766e942143639fcd554b32f9de5ab0c9
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 17%

---

# Aangepaste handelingen gebruiken {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Aangepaste acties"
>abstract="Met aangepaste acties kunt u een verbinding met een extern systeem configureren voor het verzenden van berichten of API-aanroepen. Een actie kan worden geconfigureerd met elke service van elke provider die door een REST-API met een payload in JSON-indeling kan worden aangeroepen."

Gebruik aangepaste handelingen om verbinding met een systeem van derden mogelijk te maken voor het verzenden van berichten of API-aanroepen. Een actie kan worden geconfigureerd met elke service van elke provider die door een REST-API met een payload in JSON-indeling kan worden aangeroepen.

Leer meer over douaneacties in [ deze sectie ](../action/action.md).

Leer hoe te om een douaneactie op [ tot stand te brengen en te vormen deze pagina ](../action/about-custom-action-configuration.md).

Leer hoe te om API vraagreacties van douaneacties voor verpersoonlijking op [ te gebruiken deze pagina ](../action/action-response.md).

## Toestemming en gegevensbeheer {#privacy}

In Journey Optimizer kunt u beleid voor gegevensbeheer en toestemming toepassen op uw aangepaste acties om te voorkomen dat bepaalde velden worden geëxporteerd naar systemen van derden of om klanten uit te sluiten die niet hebben ingestemd met het ontvangen van e-mail, push- of SMS-berichten. Raadpleeg de volgende pagina&#39;s voor meer informatie:

* [ het bestuur van Gegevens ](../action/action-privacy.md).
* [ Toestemming ](../action/consent.md).

## URL-configuratie

De configuratieruit van de **actie van de Douane** activiteit toont de URL configuratieparameters en de authentificatieparameters die voor de douaneactie worden gevormd. U kunt niet opstelling het statische deel van URL in de reis, maar in de globale configuratie van de douaneactie. [Meer informatie](../action/about-custom-action-configuration.md).

### Dynamisch pad

Als de URL een dynamisch pad bevat, geeft u het pad op in het veld **[!UICONTROL Path]** .

Als u velden en onbewerkte teksttekenreeksen wilt samenvoegen, gebruikt u de tekenreeksfuncties of het plusteken (+) in de geavanceerde expressie-editor. Plaats normale teksttekenreeksen tussen enkele aanhalingstekens (&#39;) of tussen dubbele aanhalingstekens (&#39;). [Meer informatie](expression/expressionadvanced.md).

In deze tabel ziet u een voorbeeld van configuratie:

| Veld | Waarde |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Pad | `The _id + '/messages'` |

De samengevoegde URL heeft de volgende vorm:

`https://xxx.yyy.com:8080/somethingstatic/` \&lt;ID> `/messages`

![](assets/journey-custom-action-url.png)

### Kopteksten en queryparameters {#headers}

De sectie **[!UICONTROL URL Configuration]** toont de dynamische kopbal en vraagparametergebieden, maar niet de constante gebieden. Dynamische kopbal en de gebieden van de vraagparameter worden bepaald als variabele in het scherm van de actieconfiguratie. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)

Als u de waarde van dynamische koptekst- en queryparametervelden wilt opgeven, klikt u in het veld of op het potloodpictogram en selecteert u het gewenste veld.

![](assets/journey-dynamicheaderfield.png)

## Handelingsparameters

In de **[!UICONTROL Action parameters]** sectie, zult u de berichtparameters zien die als _worden bepaald &quot;Variabele&quot;_. Voor deze parameters kunt u bepalen waar u deze informatie wilt ophalen (bijvoorbeeld: gebeurtenissen, gegevensbronnen), waarden handmatig doorgeven of de geavanceerde expressie-editor voor geavanceerde gebruiksgevallen gebruiken. Gevallen van geavanceerd gebruik kunnen gegevensmanipulatie en ander functiegebruik zijn. Verwijs naar deze [ pagina ](expression/expressionadvanced.md).

