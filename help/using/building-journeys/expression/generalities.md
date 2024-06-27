---
solution: Journey Optimizer
product: journey optimizer
title: Syntaxis van geavanceerde expressie-editor
description: Meer informatie over de syntaxis die wordt gebruikt in de geavanceerde expressie-editor
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: syntaxis, redacteur, reis
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: 2de94e8ce3fe77399c8dc1d515ae73d58cb8f43d
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Syntaxis van geavanceerde expressie-editor {#syntax}

Basisbeginselen van syntaxis bij gebruik van de [Geavanceerde expressie-editor](expressionadvanced.md) worden hieronder weergegeven. Voorbeelden van het gebruik van de geavanceerde expressie-editor zijn beschikbaar in [deze pagina](advanced-editor-use-cases.md).

## Haakjes en prioriteit van expressie {#parentheses-and-expression-priority}

U kunt ronde haakjes gebruiken om een complexe expressie leesbaarder te maken. _(&lt;expression>)_ is het equivalent van _&lt;expression>_. Het haakje kan ook worden gebruikt om de evaluatievolgorde en de associatie te bepalen.

De expressies worden van links naar rechts geëvalueerd. De associatie bij rekenkundige operatoren moet worden toegepast: vermenigvuldigingen en verdelingen hebben voorrang op toevoegingen en aftrekken. Om een bepaalde volgorde op te leggen, moet een haakje worden toegevoegd om de bewerkingen te begrenzen. Bijvoorbeeld:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Uitdrukking | Evaluatie |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39; heeft prioriteit boven &#39;+&#39;: 2 * 10 wordt geëvalueerd → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>De haakjes wijzigen de prioriteit: (4 + 2) wordt geëvalueerd → 6</li><li> 6 * 10 → 60</li></ul> |

## Hoofdlettergevoeligheid {#case-sensitivity}

Hier volgen de verschillende regels voor hoofdlettergevoeligheid:

* Alle operatoren (en, enz.) moet in kleine letters worden geschreven. Bijvoorbeeld: _`<expression1>`en`<expression2>`_ is een geldige expressie terwijl de expressie _`<expression1>`EN`<expression2>`_ is niet.
* Alle functienamen zijn hoofdlettergevoelig. Bijvoorbeeld: _inAudience()_ is geldig terwijl de functie _INAUDIENCE()_ is niet.
* Veldverwijzingen en constante waarden zijn hoofdlettergevoelig: het zijn geen ingebouwde elementen van de taal (in tegenstelling tot operatoren en functies), maar worden ontworpen door de eindgebruiker.

## Type geretourneerde expressie {#returned-expression-type}

Afhankelijk van de context van het gebruik, kan de uitdrukkingsredacteur verschillende waarden terugkeren.

| Geavanceerd gebruik van expressieeditor | Type geretourneerde expressie verwacht |
|--- |--- |
| Voorwaarde (gegevensbronvoorwaarde, datumvoorwaarde) | boolean |
| Aangepaste timer | dateTimeOnly |
| Toewijzing van Action Parameters | Alle |
