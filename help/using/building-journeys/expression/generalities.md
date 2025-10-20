---
solution: Journey Optimizer
product: journey optimizer
title: Syntaxis van geavanceerde expressie-editor
description: Meer informatie over de syntaxis die wordt gebruikt in de geavanceerde expressie-editor
feature: Journeys
role: Engineer
level: Experienced
keywords: syntaxis, redacteur, reis
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Syntaxis van geavanceerde expressie-editor {#syntax}

De grondbeginselen van de syntaxis wanneer het gebruiken van de [ Geavanceerde uitdrukkingsredacteur ](expressionadvanced.md) zijn hieronder vermeld. <!-- Samples of use of the advanced expression editor are available on [this page](advanced-editor-use-cases.md).-->

## Haakjes en prioriteit van expressie {#parentheses-and-expression-priority}

U kunt ronde haakjes gebruiken om een complexe expressie leesbaarder te maken. _(&lt;expression>)_ is het equivalent van _&lt;expression>_. Het haakje kan ook worden gebruikt om de evaluatievolgorde en de associatie te bepalen.

De expressies worden van links naar rechts geëvalueerd. De associatie bij rekenkundige operatoren moet worden toegepast: vermenigvuldigingen en verdelingen hebben voorrang op toevoegingen en aftrekken. Om een bepaalde volgorde op te leggen, moet een haakje worden toegevoegd om de bewerkingen te begrenzen. Bijvoorbeeld:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Uitdrukking | Evaluatie |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39; heeft prioriteit boven &#39;+&#39;: 2 \* 10 is geëvalueerd → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>De haakjes wijzigen de prioriteit: (4 + 2) wordt geëvalueerd → 6</li><li> 6 * 10 → 60</li></ul> |

## Hoofdlettergevoeligheid {#case-sensitivity}

Hier volgen de verschillende regels voor hoofdlettergevoeligheid:

* Alle operatoren (en, enz.) moeten in kleine letters worden geschreven. _`<expression1>`en`<expression2>`_ zijn bijvoorbeeld een geldige expressie, maar de expressie _`<expression1>`AND`<expression2>`_ niet.
* Alle functienamen zijn hoofdlettergevoelig. Bijvoorbeeld, _inAudience ()_ is geldig terwijl de functie _INAUDIENCE ()_ niet is.
* Veldverwijzingen en constante waarden zijn hoofdlettergevoelig: het zijn geen ingebouwde elementen van de taal (in tegenstelling tot operatoren en functies), maar worden ontworpen door de eindgebruiker.

## Type geretourneerde expressie {#returned-expression-type}

Afhankelijk van de context van het gebruik, kan de uitdrukkingsredacteur verschillende waarden terugkeren.

| Geavanceerd gebruik van expressieeditor | Type geretourneerde expressie verwacht |
|--- |--- |
| Voorwaarde (gegevensbronvoorwaarde, datumvoorwaarde) | boolean |
| Aangepaste timer | dateTimeOnly |
| Toewijzing van Action Parameters | Alle |
