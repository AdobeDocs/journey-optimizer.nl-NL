---
solution: Journey Optimizer
product: journey optimizer
title: Gebeurtenisvariabelen voor meerdere stappen
description: Leer hoe u gebeurtenisvariabelen kunt gebruiken in uw multi-step campagnes
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Gebeurtenisvariabelen voor meerdere stappen {#event-variables}

Bij sommige campagneactiviteiten met meerdere stappen kunt u scripts bewerken in de expressie-editor om specifieke handelingen uit te voeren, zoals het ophalen van gegevens uit eerdere activiteiten, het bouwen van voorwaarden of het berekenen van bestandsnamen op basis van gebeurtenisvariabelen.

## Wat zijn gebeurtenisvariabelen {#scripting}

De manuscripten die in de context van een multi-step campagnetoegang worden uitgevoerd tot een reeks extra globale **voorwerpen** zoals de multi-step campagne zelf die (`ìnstance`) wordt uitgevoerd, zijn diverse taken (`task`), of de gebeurtenissen die een bepaalde taak (`event`) activeerde.

Aan elk type van **voorwerp** wordt geassocieerd een categorie van **variabelen** die in de uitdrukkingsredacteur kunnen worden leveraged wanneer het uitgeven van manuscripten in activiteiten zoals **[!UICONTROL JavaScript code]** of **[!UICONTROL Test]**.

* **de variabelen van de Instantie** (`instance.vars.xxx`) zijn vergelijkbaar met globale variabelen. Ze worden door alle activiteiten gedeeld.
* **de variabelen van de Taak** (`task.vars.xxx`) zijn vergelijkbaar met lokale variabelen. Ze worden alleen gebruikt door de huidige taak. Deze variabelen worden gebruikt door permanente activiteiten om gegevens te bewaren en worden soms gebruikt om gegevens tussen de verschillende manuscripten van een zelfde activiteit uit te wisselen.
* **de variabelen van de Gebeurtenis** (`vars.xxx`) laten de uitwisseling van gegevens tussen de elementaire taken van een multi-step campagneproces toe. Deze variabelen worden doorgegeven door de taak die de actieve taak heeft geactiveerd. Deze worden vervolgens doorgegeven aan de volgende activiteiten. **de variabelen van de Gebeurtenis** zijn de het vaakst gebruikte variabelen, en zij zouden in voorkeur aan instantievariabelen moeten worden gebruikt.

## Gebeurtenisvariabelen in de expressieeditor benutten {#expression-editor}

Vooraf gedefinieerde gebeurtenisvariabelen zijn beschikbaar voor gebruik in het linkerdeelvenster van de expressieeditor. U kunt ook nieuwe maken door een nieuwe variabele in uw code te initialiseren.

![](assets/event-variables.png)

Naast deze gebeurtenisvariabelen kunt u ook het menu **[!UICONTROL Conditions]** in het linkerdeelvenster gebruiken om voorwaarden te maken en het menu **[!UICONTROL Add current date]** om functies te gebruiken die te maken hebben met datumopmaak.
