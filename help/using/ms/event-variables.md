---
solution: Journey Optimizer
product: journey optimizer
title: Werken met gebeurtenisvariabelen in georkestreerde campagnes
description: Leer hoe u gebeurtenisvariabelen in uw georkestreerde campagnes kunt gebruiken
hide: true
hidefromtoc: true
exl-id: f86dd262-0209-42f6-a180-736f1de98d78
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Werken met gebeurtenisvariabelen {#event-variables}

Sommige georkestreerde campagneactiviteiten staan u toe om manuscripten in de uitdrukkingsredacteur uit te geven om specifieke acties uit te voeren zoals het terugwinnen van gegevens die uit vorige activiteiten komen, bouwvoorwaarden, of gegevensverwerkingsdossiernamen die op gebeurtenisvariabelen worden gebaseerd.

## Wat zijn gebeurtenisvariabelen {#scripting}

De manuscripten die in de context van een georkestreerde campagnetoegang worden uitgevoerd tot een reeks extra globale **voorwerpen** zoals de georkestreerde campagne zelf die (`ìnstance`) wordt uitgevoerd, zijn diverse taken (`task`), of de gebeurtenissen die een bepaalde taak (`event`) activeerde.

Aan elk type van **voorwerp** wordt geassocieerd een categorie van **variabelen** die in de uitdrukkingsredacteur kunnen worden leveraged wanneer het uitgeven van manuscripten in activiteiten zoals **[!UICONTROL JavaScript code]** of **[!UICONTROL Test]**.

* **de variabelen van de Instantie** (`instance.vars.xxx`) zijn vergelijkbaar met globale variabelen. Ze worden door alle activiteiten gedeeld.
* **de variabelen van de Taak** (`task.vars.xxx`) zijn vergelijkbaar met lokale variabelen. Ze worden alleen gebruikt door de huidige taak. Deze variabelen worden gebruikt door permanente activiteiten om gegevens te bewaren en worden soms gebruikt om gegevens tussen de verschillende manuscripten van een zelfde activiteit uit te wisselen.
* **de variabelen van de Gebeurtenis** (`vars.xxx`) laten de uitwisseling van gegevens tussen de elementaire taken van een geordend campagneproces toe. Deze variabelen worden doorgegeven door de taak die de actieve taak heeft geactiveerd. Deze worden vervolgens doorgegeven aan de volgende activiteiten. **de variabelen van de Gebeurtenis** zijn de het vaakst gebruikte variabelen, en zij zouden in voorkeur aan instantievariabelen moeten worden gebruikt.

## Gebeurtenisvariabelen in de expressieeditor benutten {#expression-editor}

Vooraf gedefinieerde gebeurtenisvariabelen zijn beschikbaar voor gebruik in het linkerdeelvenster van de expressieeditor. U kunt ook nieuwe maken door een nieuwe variabele in uw code te initialiseren.

![](assets/event-variables.png)

Naast deze gebeurtenisvariabelen kunt u ook het menu **[!UICONTROL Conditions]** in het linkerdeelvenster gebruiken om voorwaarden te maken en het menu **[!UICONTROL Add current date]** om functies te gebruiken die te maken hebben met datumopmaak.
