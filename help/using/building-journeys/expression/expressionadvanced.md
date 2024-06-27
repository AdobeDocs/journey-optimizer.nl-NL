---
solution: Journey Optimizer
product: journey optimizer
title: Werken met de geavanceerde expressie-editor
description: Geavanceerde expressies maken
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: expression editor, data, trip
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: 2de94e8ce3fe77399c8dc1d515ae73d58cb8f43d
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 63%

---

# Werken met de geavanceerde expressie-editor {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="De geavanceerde expressie-editor"
>abstract="Gebruik de geavanceerde uitdrukkingsredacteur om geavanceerde uitdrukkingen in diverse schermen van de interface te bouwen. U kunt bijvoorbeeld expressies maken bij het configureren en gebruiken van reizen en bij het definiëren van een gegevensbronvoorwaarde."

Gebruik de Journey Geavanceerde uitdrukkingsredacteur om geavanceerde uitdrukkingen in diverse schermen van de interface te bouwen. U kunt bijvoorbeeld expressies maken bij het configureren en gebruiken van reizen en bij het definiëren van een gegevensbronvoorwaarde.

De editor is ook altijd beschikbaar wanneer u actieparameters moet definiëren waarvoor specifieke datamanipulaties nodig zijn. U kunt data gebruiken die afkomstig zijn van gebeurtenissen of aanvullende informatie die is opgehaald uit de databron. In een journey is de weergegeven lijst met gebeurtenisvelden contextafhankelijk en deze varieert op basis van de gebeurtenissen die tijdens de journey worden toegevoegd.

![](../assets/journey65.png)


De geavanceerde expressie-editor biedt een reeks ingebouwde functies en operatoren waarmee u waarden kunt manipuleren en een expressie kunt definiëren die precies bij uw wensen past. Met de geavanceerde expressie-editor kunt u ook de waarden van de externe databronbronparameter definiëren en toewijzingsvelden en verzamelingen zoals ervaringsgebeurtenissen bewerken.

>[!NOTE]
>
>De functies en mogelijkheden die beschikbaar zijn in de geavanceerde expressie-editor voor Journey verschillen van die in de [personalisatie-editor](../../personalization/functions/functions.md).

## De geavanceerde expressie-editor openen {#accessing-the-advanced-expression-editor}

De geavanceerde expressie-editor kan worden gebruikt om:

* [Geavanceerde voorwaarden](../condition-activity.md#about_condition) te maken voor databronnen en gebeurtenisinformatie
* Aangepaste [wachtactiviteiten](../wait-activity.md#custom) te definiëren
* De toewijzing van actieparameters te definiëren

Indien mogelijk kunt u tussen de twee modi schakelen met de knop **[!UICONTROL Advanced mode]**/**[!UICONTROL Simple mode]**. De eenvoudige modus wordt [hier](../condition-activity.md#about_condition) beschreven.

>[!NOTE]
>
>De voorwaarden kunnen in de eenvoudige of geavanceerde expressie-editor worden gedefinieerd. Ze retourneren altijd een booleaans type.
>
>Actieparameters kunnen worden gedefinieerd door velden te selecteren of via de geavanceerde expressie-editor. Ze retourneren een specifiek datatype op basis van hun expressie.

U kunt de geavanceerde expressie-editor op verschillende manieren openen:

* Wanneer u een databronvoorwaarde maakt, kunt u de geavanceerde editor openen door te klikken op **[!UICONTROL Advanced mode]**.

  ![](../assets/journeyuc2_33.png)

* Wanneer u een aangepaste timer maakt, wordt de geavanceerde editor direct weergegeven.
* Wanneer u een actieparameter toewijst, klikt u op **[!UICONTROL Advanced mode]**.

## De interface detecteren {#discovering-the-interface}

In dit scherm kunt u uw expressie handmatig schrijven.

![](../assets/journey70.png)

Links in het scherm worden de beschikbare velden en functies weergegeven:

* **[!UICONTROL Events]**: kies een van de velden die worden ontvangen van de binnenkomende gebeurtenis. De weergegeven lijst met gebeurtenisvelden is contextueel en varieert afhankelijk van de gebeurtenis(sen) die tijdens de reis zijn toegevoegd. [Meer informatie](../../event/about-events.md)
* **[!UICONTROL Audiences]**: als u een **[!UICONTROL Audience qualification]** kiest u het publiek dat u in uw expressie wilt gebruiken. [Meer informatie](../condition-activity.md#using-a-segment)
* **[!UICONTROL Data Sources]**: maak een keuze in de lijst met velden die beschikbaar zijn in de veldgroepen van de gegevensbronnen. [Meer informatie](../../datasource/about-data-sources.md)
* **[!UICONTROL Journey properties]**: in dit deel worden de technische gebieden met betrekking tot de reis voor een bepaald profiel gegroepeerd. [Meer informatie](journey-properties.md)
* **[!UICONTROL Functions]**: kies uit de lijst met ingebouwde functies die complexe filtering mogelijk maken. Functies zijn ingedeeld in categorieën. [Meer informatie](functions.md)

![](../assets/journey65.png)

Een mechanisme voor automatisch aanvullen geeft contextafhankelijke suggesties weer.

![](../assets/journey68.png)

Een mechanisme voor de syntaxisvalidatie controleert de integriteit van uw code. Fouten worden over de editor heen weergegeven.

![](../assets/journey69.png)

**Parameters vereist tijdens het samenstellen van voorwaarden met de geavanceerde expressie-editor**

Als u een veld selecteert uit een externe gegevensbron waarvoor een parameter moet worden aangeroepen (zie [deze pagina](../../datasource/external-data-sources.md)), wordt er een nieuw tabblad weergegeven aan de rechterkant waarin u deze parameter kunt opgeven. De parameterwaarde kan afkomstig zijn van de gebeurtenissen in de reis of de gegevensbron van het Experience Platform (en niet uit andere externe gegevensbronnen). In een databron met betrekking tot weersomstandigheden is ‘city’ bijvoorbeeld een veelgebruikte parameter. Dit betekent dat u moet selecteren waar u deze parameter ‘city’ wilt ophalen. Functies kunnen ook op parameters worden toegepast om opmaakwijzigingen of samenvoegingen uit te voeren.

![](../assets/journeyuc2_19.png)

Als u bij complexere gebruiksscenario’s de parameters van de databron wilt opnemen in de hoofdexpressie, kunt u de waarden ervan definiëren met het trefwoord ‘params’. Zie [deze pagina](../expression/field-references.md).
