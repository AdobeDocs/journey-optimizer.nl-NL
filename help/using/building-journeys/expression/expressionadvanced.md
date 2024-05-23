---
solution: Journey Optimizer
product: journey optimizer
title: Over de geavanceerde expressie-editor
description: Leer hoe u geavanceerde expressies kunt maken
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: expression editor, data, trip
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 1%

---

# Over de geavanceerde expressie-editor {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="Over de geavanceerde expressie-editor"
>abstract="Gebruik de geavanceerde uitdrukkingsredacteur om geavanceerde uitdrukkingen in diverse schermen van de interface te bouwen. U kunt bijvoorbeeld expressies maken bij het configureren en gebruiken van reizen en bij het definiëren van een gegevensbronvoorwaarde."

Gebruik de Journey Geavanceerde uitdrukkingsredacteur om geavanceerde uitdrukkingen in diverse schermen van de interface te bouwen. U kunt bijvoorbeeld expressies maken bij het configureren en gebruiken van reizen en bij het definiëren van een gegevensbronvoorwaarde.

>[!NOTE]
>
>De functies en mogelijkheden die beschikbaar zijn in de geavanceerde expressie-editor voor Journey verschillen van die in de [personalisatie-editor](../../personalization/functions/functions.md).

Het is ook beschikbaar telkens als u actieparameters moet bepalen die specifieke gegevensmanipulaties vereisen. U kunt gegevens die afkomstig zijn van gebeurtenissen of aanvullende informatie die is opgehaald uit de gegevensbron, gebruiken. Op een reis is de weergegeven lijst met gebeurtenisvelden contextueel en varieert afhankelijk van de gebeurtenis(sen) die tijdens de reis zijn toegevoegd.

De geavanceerde uitdrukkingsredacteur biedt een reeks ingebouwde functies en exploitanten aan om u waarden te laten manipuleren en een uitdrukking te bepalen die specifiek uw behoeften past. Met de geavanceerde expressie-editor kunt u ook de waarden van de externe gegevensbronparameter definiëren, kaartvelden en verzamelingen bewerken, zoals ervaringsgebeurtenissen.

![](../assets/journey65.png)

_De geavanceerde interface van de uitdrukkingsredacteur_

De geavanceerde uitdrukkingsredacteur kan worden gebruikt om:

* maken [geavanceerde omstandigheden](../condition-activity.md#about_condition) over gegevensbronnen en informatie over gebeurtenissen
* aangepaste definiëren [wachtactiviteiten](../wait-activity.md#custom)
* parametertoewijzing voor handelingen definiëren

Indien mogelijk kunt u tussen de twee modi schakelen met de opdracht **[!UICONTROL Advanced mode]** / **[!UICONTROL Simple mode]** knop. De eenvoudige modus wordt beschreven [hier](../condition-activity.md#about_condition).

>[!NOTE]
>
>De voorwaarden kunnen in de eenvoudige of geavanceerde uitdrukkingsredacteur worden bepaald. Ze retourneren altijd een booleaans type.
>
>Handelingsparameters kunnen worden gedefinieerd door velden te selecteren of via de geavanceerde expressie-editor. Ze retourneren een specifiek gegevenstype op basis van hun expressie.

## De geavanceerde expressie-editor openen {#accessing-the-advanced-expression-editor}

U kunt de geavanceerde expressieeditor op verschillende manieren openen:

* Wanneer u een gegevensbronvoorwaarde creeert, kunt u tot de geavanceerde redacteur toegang hebben door op te klikken **[!UICONTROL Advanced mode]**.

  ![](../assets/journeyuc2_33.png)

* Wanneer u een douanetijdopnemer creeert, zal de geavanceerde redacteur direct worden getoond.
* Wanneer u de actieparameter toewijst, klikt u op **[!UICONTROL Advanced mode]**.

## De interface detecteren{#discovering-the-interface}

In dit scherm kunt u uw expressie handmatig schrijven.

![](../assets/journey70.png)

Links op het scherm worden beschikbare velden en functies weergegeven:

* **[!UICONTROL Events]**: kies een van de velden die u van de binnenkomende gebeurtenis hebt ontvangen. De weergegeven lijst met gebeurtenisvelden is contextueel en varieert afhankelijk van de gebeurtenis(sen) die tijdens de reis zijn toegevoegd. [Meer informatie](../../event/about-events.md)
* **[!UICONTROL Audiences]**: als u een **[!UICONTROL Audience qualification]** kiest u het publiek dat u in uw expressie wilt gebruiken. [Meer informatie](../condition-activity.md#using-a-segment)
* **[!UICONTROL Data Sources]**: maak een keuze in de lijst met velden die beschikbaar zijn in de veldgroepen van de gegevensbronnen. [Meer informatie](../../datasource/about-data-sources.md)
* **[!UICONTROL Journey properties]**: in dit deel worden de technische gebieden met betrekking tot de reis voor een bepaald profiel gegroepeerd. [Meer informatie](journey-properties.md)
* **[!UICONTROL Functions]**: kies een optie in de lijst met ingebouwde functies waarmee u complexe filters kunt toepassen. Functies zijn ingedeeld in categorieën. [Meer informatie](functions.md)

![](../assets/journey65.png)

Een mechanisme voor automatisch aanvullen geeft contextuele suggesties weer.

![](../assets/journey68.png)

Een mechanisme van de syntaxisbevestiging controleert de integriteit van uw code. Fouten worden boven op de editor weergegeven.

![](../assets/journey69.png)

**Behoefte aan parameters wanneer het bouwen van voorwaarden met de geavanceerde uitdrukkingsredacteur**

Als u een veld selecteert uit een externe gegevensbron waarvoor een parameter moet worden aangeroepen (zie [deze pagina](../../datasource/external-data-sources.md)), wordt er een nieuw tabblad weergegeven aan de rechterkant waarin u deze parameter kunt opgeven. De parameterwaarde kan afkomstig zijn van de gebeurtenissen in de reis of de gegevensbron van het Experience Platform (en niet uit andere externe gegevensbronnen). In een gegevensbron met betrekking tot weersomstandigheden is een veelgebruikte parameter bijvoorbeeld &quot;stad&quot;. Dit betekent dat u moet selecteren waar u deze parameter city wilt ophalen. Functies kunnen ook op parameters worden toegepast om opmaakwijzigingen of aaneenschakelingen uit te voeren.

![](../assets/journeyuc2_19.png)

Als u de parameters van de gegevensbron wilt opnemen in de hoofdexpressie, kunt u voor complexere gebruiksgevallen de waarden definiëren met het trefwoord &quot;params&quot;. Zie [deze pagina](../expression/field-references.md).
